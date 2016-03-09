# Gatsby test with 5000 markdown articles

I used the Gatsby starter blog and wrote a script to create 5000 test articles
under `pages/5000`. But that seems to be to much for gatsby:


The test raises an error after a few seconds when you're running

`gatsby develop`

    Listening at: http://0.0.0.0:8000

    <--- Last few GCs --->

       53377 ms: Scavenge 1388.5 (1457.1) -> 1388.5 (1457.1) MB, 25.3 / 0 ms (+ 1.1 ms in 1 steps since last GC) [allocation failure] [incremental marking delaying mark-sweep].
       55503 ms: Mark-sweep 1388.5 (1457.1) -> 1387.4 (1457.1) MB, 2126.2 / 0 ms (+ 2.3 ms in 2 steps since start of marking, biggest step 1.1 ms) [last resort gc].
       57630 ms: Mark-sweep 1387.4 (1457.1) -> 1388.2 (1457.1) MB, 2127.4 / 0 ms [last resort gc].


    <--- JS stacktrace --->

    ==== JS stack trace =========================================

    Security context: 0x3035be0e3ac1 <JS Object>
        1: createInnerCallback(aka createInnerCallback) [/Users/jkuetemeier/projects/test/gatsby-test/blog/node_modules/enhanced-resolve/lib/createInnerCallback.js:~5] [pc=0x2badb52290a3] (this=0x3035be004189 <undefined>,callback=0x217910bb7259 <JS Function (SharedFunctionInfo 0x3f04968a3399)>,options=0x217910bb71a1 <JS Function (SharedFunctionInfo 0x3f0496861191)>,message=0x217910bb7231 <String[32...

FATAL ERROR: CALL_AND_RETRY_LAST Allocation failed - process out of memory

same for `gatsby build`
