# Support for multiple processes

Use the Process-Monitor-Styling.md to create a single page html ui prototype of a new feature that will support joining two processes together. The prototype should include the following:
1. Admin tab for defining the join
2. Process Monitor tab with configuration and sample results
3. Other UI details to highlight key interactions - side-by-side process graph 

## Admin Tab
The admin tab is a configuration section for specifying the join between two processes. It should match the Vault-Styling.md. It should include the following:
1. Label for the join results
2. Left Process 
3. Right Process
4. Left key (field on left process object)
5. Right key (field on right process object)
6. Join type (1:1 inner vs. outer vs. 1:many)
7. State join criteria (left state + right state)
8. Option setting for 1:many - right resolution (First Created, Last Created, First Completed, Last Completed)

## Process Monitor Config
The left had configuration panel should include drop downs for the process and the cycle time start and cycle time end.

In the process dropdown, two multi-process option should be included "inbox item -> case" and "Events with Activites"

When either of tehse is selected, the cycle time start and cycle time end should include fully qualified state lables from both processes.

## Process Graph
When one of the multi-process options is selected, a process graph should be displayed that includes the two processes side-by-side with an arrow connecting them based on the state join criteria (admin tab step 7). The arrow will go from the left state to the right state. There should also be two variant panels to control which variants show up in each of the two process graphs