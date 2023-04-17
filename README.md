## Programming Languages 

While what I've learned from hacking around on programming languages comes up every now and then on the day-to-day at work, my exploration of programming languages is not yet my professional calling. However, as of late, I've started making a step in the right direction and have started some research with the University of Utah (my new home summer 2023!).

### Cool PL Stuff I've Done this Far

* Created my own somewhat functional programming language: [Sailfish Programming Language](https://github.com/sailfish-lang/sailfishc)
* Contributed to [Nessie: Automatically Testing JavaScript APIs with
Asynchronous Callbacks](https://software-lab.org/publications/icse2022_Nessie.pdf) with the folks at [North Eastern](https://prl.khoury.northeastern.edu/).

> The authors would like to thank Rob Durst for his contributions to Nessie’s discovery phase.

The gist of my contribution is summed up well in the comment I left in the code, copy-pasted here:

```
 /**
 * InferringSignature randomly tries various combinations of inputs along with
 * the function f (as the final argument) in attempt to discover at what positions,
 * if any, a method expects a callback as an input. Furthermore, we have extended
 * this original algorithm, as defined in LambdaTester, to also classify positions
 * as expecting synchronous or asynchronous callbacks.
 *
 * Asynchronous classification: the kye intuition here is to realize that asynchronous
 * callbacks are always thrown into the event loop. This means that any code
 * immediately following the deferred asynchronous call will be invoked first (in fact
 * all code on the stack will be executed before the asynchronous callback is invoked).
 * As an example consider the following code snippet:
 *
 *    setTimeout(() => console.log('A'), 0);
 *    console.log('B');
 *
 * While not intuitive, B will actually be logged before A since setTimeout's method is
 * thrown on the event loop at 0... not executed at 0.
 *
 * Based on the above realization, we construct code snippets to test the ordering of the
 * execution, more specifically the logging, of two methods to determine whether or not
 * a callback is executed synchronously or asynchronously. The first is the same method, f,
 * from LambdaTester. The next is a console.log("hello world") statement added after the
 * method under investigation is invoked. If "hello world" is first, the method is asynchronous.
 */
```

[See my fork of the codebase.](https://github.com/robertDurst/AsyncLambdaTester/blob/master/src/asyncDiscoveryPhase/inferringSignature.ts)

## Blogging

I occasionally blog. Working on that first post of 2023...

My personal blog is on [my website, robdurst.com](https://robdurst.com/).

I've also blogged for work:
  * Spring Health - _cannot seem to find the link_
  * DocuSign: [My experience: Why defensive coding matters](https://www.docusign.com/blog/developers/my-experience-why-defensive-coding-matters)
  
## Meetups

I was at one point the co-host for the largest developer only cryptocurrent meetup in the SF Bay Area (circa 2018). I had a lot of fun and am definitely hoping to get back to hosting meetups in the near future.
