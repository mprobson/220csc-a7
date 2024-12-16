# A7. New Approaches

Due Date: 12/18 at midnight (optional)

## Instructions

Review one of the previous assignments and re-implement it using a new approach
we've learned.
This could be adding a new approach (e.g. shared memory, atomics, dynamic
parallelism, etc) to an assingment that did not use it.
You could also attempt to solve an older problem using a new language, e.g.
OpenMP, OpenCL, Futhark, etc
Submit a writeup of your changes, approach and results along with your updated code
and a reflection of the process.

## Reflection Questions

1. Should I have taught this earlier?
2. What went well with this assignment?
3. What was difficult?
4. How would you approach differently?
5. Anything else you want me to know?

## Submission
- [ ] Updated code
- [ ] Narrative of changes
    - what you did
    - why you chose that problem and approach
    - analysis of any new performance data, ease of programming, etc
- [ ] Reflection

# Debugging

If you encounter errors, I recommend two approahces:

1. Adding print statements both inside your kernel function
   as well as outside.
   This can include: `printf("%s\n", cudaGetErrorString(cudaGetLastError()));`
   to catch any cuda errors.

2. You can check to make sure that you code is not accessing unallocated memory
   by utilizing NVIDIA's memory sanitizer tool.
   You can run it ok `keroppi` using the following line.
   ```sh
   compute-sanitizer --tool memcheck ./your_cuda_executable_not_source
   ```

# Updates

To update this assignment as changes are made,
a new PR will be generated.
You can find the tab [here](../../pulls).
On that page you can merge the pull request to get the update instructions.
This may invovle rebasing or merging your contributions, reach out
if you need help with this.

# Extras

1. Implement the approach in two different models, e.g. OpenMP and OpenCL,
compare both their performance as well as their programmability.
2. Suggest a new problem to tackle in a homework next semester.
    1. Potentially one that could be solved with old approaches only
    2. Another (or the same) that could be solve only (or more efficiently) with
    something new.
3. Go back and look at the old extras, could one be easily solved using a new
approach.
