# React useEffect Hook Memory Leak
This repository demonstrates a common React bug involving memory leaks due to improper usage of the useEffect hook.  The `bug.js` file contains the flawed code, while `bugSolution.js` provides the corrected version.

The bug arises from failing to return a cleanup function within the useEffect callback that uses setInterval or setTimeout. Without this cleanup, the interval continues to run even after the component unmounts, leading to memory leaks.