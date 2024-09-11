a key principle is to **test everything you don’t want to break**. This includes obvious areas like performance, security, and correctness, but also less apparent ones like how a system handles failures. This approach is encapsulated in the **Beyoncé Rule**, which states, “If you liked it, then you shoulda put a test on it.” This means that if a system behavior is important to you, it should have an automated test to ensure it works consistently.

A major focus of this philosophy is **testing for failure**. Systems inevitably fail, so it's crucial to simulate these failures through automated tests, rather than waiting for real-world issues. This can range from simple unit test exceptions to larger disruptions using Chaos Engineering. By preparing for failure in a controlled manner, teams ensure their systems can handle adverse conditions reliably.

Ref: Software engineer at google. Ch11. 
#leadership/measure #product/quality #software/unit_testing

