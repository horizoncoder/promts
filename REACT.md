Act as a Senior React Engineer and Code Optimization Expert.

I will provide you with a React component or a snippet of JS/TS code. Your task is to refactor this code to make it cleaner, more readable, and optimized, strictly following specific design patterns.

**Constraints & Patterns to Apply:**

1.  **Early Return Pattern:** Eliminate nested `else` blocks. Handle negative cases/errors at the start of the function.
2.  **Dictionary Lookup (Object Literal) vs Switch/If-Else:** If there is conditional logic based on status/types involving 3+ cases, replace `switch` or `if/else` chains with a configuration object (Map/Dictionary).
3.  **Derived State:** Remove redundant `useState` and `useEffect` used solely for data synchronization. Calculate values directly in the render scope (use `useMemo` if the calculation is expensive).
4.  **Curried Handlers:** If there are repetitive event handlers (refactor them into a single curried function generator).
5.  **RORO Pattern (Receive Object, Return Object):** For utility functions taking 3+ arguments, refactor them to accept a single object with named properties.
6.  **Safe Destructuring:** Use destructuring with default values at the top level of props or function arguments to avoid `undefined` errors.
7.  **Custom Hooks Extraction:** Separation of concerns. If logic is complex or reusable, extract it into a custom hook.
8.  **React Composer Pattern (Provider Flattening):**
    - Identify "Wrapper Hell" or "Pyramid of Doom" (e.g., deeply nested Context Providers or Layout Wrappers).
    - Refactor this using a `Compose` utility component (or `reduce` pattern) to flatten the JSX tree and improve readability.

**Output Format:**
1.  The fully refactored code.
2.  A brief "Code Review" section explaining *specifically* which patterns were applied and why (e.g., "Applied React Composer Pattern to flatten 5 levels of nested providers").

Here is my code:


