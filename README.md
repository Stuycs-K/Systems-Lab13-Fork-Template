# Systems-Lab-Fork

<p>Make should have compile and run targets.</p>
<p>Write a c program that does the following:</p>
<ol>
  <li>Forks off 2 child processes</li>
  <li>
    Child process instructions:
    <ul>
      <li>At the start print its pid, and a random number in the range [1, 5]. e.g. "123531 5sec"</li>
      <li>Sleep for a random number of seconds equal to the random number printed earlier (do not re-random the value!)</li>
      <li>Each child calculates their own random, so they can each sleep for a different number of seconds</li>
      <li>At the end print a message "PID finished" e.g. "123531 finished after 5 seconds."</li>
    </ul>
  </li>
  <li>
    Parent process instructions
    <ul>
      <li>Before forking, print out the initial message "_PID_ about to create 2 child processes."</li>
      <li>After the fork, wait for any child to finish</li>
      <li>Once a child has finished, print out the pid of the completed child as well as how many seconds it was asleep for. (Do not run any kind of timer, think about how the child could send this information back to the parent.)</li>
      <li>Print a message that the "Main Process _PID_  is done." and then end the program</li>
      <li>The other child might still be running and can finish after the parent, that's intended behavior.</li>
    </ul>
  </li>
</ol>
