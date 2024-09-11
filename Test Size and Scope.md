At Google, the terms "size" and "scope" are used to categorize tests. **Size** refers to the resources needed to run the test (memory, processes, and time), while **scope** refers to the code paths being validated. Though these concepts are related, they are distinct—executing a line of code is not the same as verifying it works as expected.

Tests are generally categorized by size: **small tests** run in a single process, **medium tests** run on a single machine, and **large tests** can run across multiple machines. Similarly, test scope focuses on how much of the code is being validated. **Narrow-scoped tests** (unit tests) focus on specific parts like a class or method. **Medium-scoped tests** (integration tests) check interactions between components. **Large-scoped tests** (end-to-end tests) validate the system as a whole.

Google encourages a mix of 80% unit tests, 15% integration tests, and 5% end-to-end tests to ensure balanced testing coverage that optimizes both size and scope.

**A Note in Code Coverage**
Code coverage **measures the percentage of code executed** by automated tests, but it has significant limitations in assessing test quality. High coverage **doesn't guarantee that the tests verify correct behavior**, as it only shows that code was executed, not that it was tested effectively. Additionally, code coverage targets can become misguided goals, with teams focusing on meeting the metric rather than ensuring thorough testing. A better approach is to focus on the reliability and effectiveness of tests, ensuring that they cover key behaviors and failure scenarios rather than relying solely on coverage percentages.


Ref: Software engineer at google. Ch11. 

#leadership/measure #product/quality #software/unit_testing
