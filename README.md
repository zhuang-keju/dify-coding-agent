# dify-coding-agent

DSL of coding agent



feat(workflow): Optimize Regex parser and Debugger logic for stable MVP



Major updates:

1\. Regex Parser Upgrade:

&nbsp;  - Implemented "Triplet Extraction" (filename + suffix + content) to bypass JSON decoding errors.

&nbsp;  - Added `safe\_json\_decode` to handle escaped characters in raw strings correctly.

&nbsp;  - Customized `regex\_decode` for Debugging Agent to return `{target\_file, file\_content}` dictionary for Router compatibility.



2\. Agent Logic Refinement:

&nbsp;  - Initial Coder: Verified capability to generate complex single-file solutions (Recursive Descent Parser, Graph algorithms) without hallucination.

&nbsp;  - Testcase Agent: Fixed assertion logic regarding "empty string vs. deletion" and "rollback state".

&nbsp;  - Debugging Agent: Adjusted output format to prevent JSON syntax errors during nested quoting.



3\. Stability Verification:

&nbsp;  - Passed complex scenarios: LeetCode 394 (Stack), Sales Hierarchy (Aggregation), and Spreadsheet Engine (Recursion/Graph).



Note: This is the final stable Dify version before potential migration to LangGraph.

