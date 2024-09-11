
When writing tests, many engineers instinctively align their tests with the structure of their code, creating a test for each method. However, this approach can lead to **complex and unclear tests** as the codebase grows. A better strategy is to write **behavior-driven tests** that focus on how the system should behave in response to specific inputs, rather than method-specific testing.

Behavior-driven tests follow a **given/when/then** structure, ensuring clarity:

- **Given** defines the setup for the test (e.g., initial conditions).
- **When** specifies the action being tested.
- **Then** validates the result or outcome of the action.

This approach keeps tests concise and readable, focusing on the expected behavior rather than the internal structure of the code. 

```cpp
/* Example well structured test */
@Test
public void transferFundsShouldMoveMoneyBetweenAccounts() { 
  // Given two accounts with initial balances of $150 and $20
  Account account1 = newAccountWithBalance(usd(150));
  Account account2 = newAccountWithBalance(usd(20));
  
  // When transferring $100 from the first to the second account
  bank.transferFunds(account1, account2, usd(100));
  
  // Then the new account balances should reflect the transfer
  assertThat(account1.getBalance()).isEqualTo(usd(50));
  assertThat(account2.getBalance()).isEqualTo(usd(120));
}
```

- Good name: Expecting Behavior of the function
- Given - When - Then pattern
- No logic ( operators, loops or conditionals )
- DAMP (Descriptive And Meaningful Phrases): A little bit of duplication is OK in
tests so long as that duplication makes the test simpler and clearer. 
### Benefits of Behavior-Driven Testing

1. **Clarity**: Behavior-driven tests read more like natural language, making them easier to understand.
2. **Focused Scope**: Each test targets a specific behavior, avoiding the pitfalls of method-driven tests that grow complex over time.
3. **Maintainability**: Small, descriptive tests are easier to modify as the system evolves, without creating convoluted test structures.

By emphasizing **behaviors over methods**, engineers can ensure that tests are more reliable, descriptive, and easier to work with in the long run.

Ref: Software engineer at google. Ch11. 

#leadership/culture #product/quality #software/unit_testing #operationsmanagement/quality 