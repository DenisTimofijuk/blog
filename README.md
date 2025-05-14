## 🧠 Why React and I Don’t Get Along — A Vanilla JS Developer’s Honest Take

Over the past year, I’ve worked on a large, complex React project with an international team. I’ve written production code, fixed bugs, reviewed pull requests, and I’m even halfway through a React course to deepen my understanding. But the more I learn, the more I realize: **React just isn’t for me**.

It’s not that I don’t *understand* React. I do. I know how to write components, manage state with hooks, pass props, and deal with context. But something always feels off. Something deeper. And recently, I figured out what it is.

---

### 🛠️ The Simplicity and Clarity of Vanilla JS

I’ve always worked closely with the browser. I build tools that interact with audio, video, the canvas, and various Web APIs. I avoid heavy libraries, preferring to stay close to the metal — not for performance alone, but because I want full control over what I’m building.

When a client asks for something, my usual response is:
**“Yes, everything is possible. It’s just a matter of time.”**

With vanilla JavaScript, I feel empowered. I understand every line. I know what’s happening under the hood — from async/await to DOM manipulation to how the browser event loop ticks. There’s no magic. No abstraction I need to work around. I own the result.

With React, I often can’t say “yes” so quickly. Even senior React developers on my team would pause or hesitate when presented with certain client requests. It’s not that they weren’t skilled — they were excellent — but the stack introduces overhead, and that overhead changes how we solve problems.

---

### 🔁 Then Comes React… and Hooks

React forces a different mental model. A big part of that is **hooks** — `useState`, `useEffect`, `useRef`, `useCallback`, `useMemo`, and on and on.

Take this simple example of a timer component from a course I’m taking:

```js
export function QuestionTimer({ timeout, onTimeout }) {
  const [remainingTime, setRemainingTime] = useState(timeout);

  useEffect(() => {
    setTimeout(onTimeout, timeout);
  }, [timeout, onTimeout]);

  useEffect(() => {
    setInterval(() => {
      setRemainingTime(prev => prev - 100);
    }, 100);
  }, []);

  return <progress max={timeout} value={remainingTime}></progress>;
}
```

As someone who writes native JS daily, this is mind-bending. A basic `setInterval`, a countdown, and a callback — suddenly wrapped in multiple hooks with dependency arrays and indirect logic. And then when it doesn’t behave correctly?

> **“Just add a `key` prop and React will magically reset everything!”**

That kind of solution frustrates me. It feels like I'm encouraged to stop understanding how things work — and start memorizing React’s way of solving things. React doesn’t reward deep JavaScript knowledge. It rewards knowing React.

---

### 🪄 I Understand the Benefits — I Really Do

I’m not blind to the advantages. I fully understand what React brings to the table:

* It **smooths out cross-browser quirks**.
* It’s **structured for large teams** to collaborate.
* It helps **avoid reinventing the wheel** every time you build a UI.
* And yes, there’s **massive community support and job demand**.

There are days when I work with vanilla JS and realize I’ve already built this utility before, or I’m solving the same problem again in slightly different form. On those days, I do think about React and its ecosystem of reusable components.

But even then, I come back to this:

> **React is a fantastic tool for building websites — but I never set out to be a website builder.**

Especially now, when **website building has been democratized**. You can spin up a beautiful, responsive, interactive site using tools like Webflow, Wix, Notion, or even AI site builders. You barely need to touch code. The gap between developer-built and no-code websites is shrinking fast.

So if the future is full of “React developers” building marketing sites and dashboards, maybe that’s not the future I want to chase.

---

### 🔍 My Focus Is Different

Vanilla JavaScript shines when you're building **custom, complex implementations** — the kind of things you can’t drag and drop with a builder:

* Audio recording tools
* Interactive canvas games
* Smart-home UIs
* Web-based visualizations and simulations
* Embedded tools for existing platforms

These are not full-blown websites. They’re **products**. Tools. Widgets. Extensions. And in these cases, JavaScript (and a good mental model of the browser) is all you need. No React. No JSX. No hooks.

That’s where I find joy. That’s where I want to be.

---

### 🙌 Final Thoughts

React is not bad. It’s mature, powerful, and solves real-world problems. I respect the developers who love it and thrive with it.

But for me, it breaks the flow. It replaces creativity with compliance. It wraps problems I’ve already solved in abstractions I never asked for.

And the more I’m told, *“This is the React way,”* the more I realize:

> **Maybe I don’t want to go that way.**

So I’ll keep learning React. I’ll stay employable. But I’ll be building what I truly care about with the tool that makes me feel limitless:

**Vanilla JavaScript.**

---

### 🗒️ A Note for Non-Programmers

You might not be a developer, so let me explain something briefly.

In this post, I talk about two ways of writing code for the web:

* **Vanilla JavaScript** – This means writing code using the built-in capabilities of the web browser. It’s like knowing how to cook from scratch using raw ingredients: you control everything, and you understand exactly what’s happening at every step.

* **React** – This is a popular tool (or *framework*) built on top of JavaScript. It gives developers a more structured way to build websites and apps, especially in large teams. But it comes with its own rules, tools, and ways of thinking — it’s more like using a meal kit where you follow specific instructions and use pre-made sauces. Faster, yes, but you have less freedom.

The post you're about to read is about how *React changes the way I have to think* — and why that shift doesn’t feel natural to me. It’s like asking a chef to give up their knife and only use a >microwave. Sure, it works — but it’s not how I like to solve problems.

So even if the technical terms get a little dense, the heart of this post is really about **creative freedom vs. working inside someone else’s system**.

Thanks for reading with an open mind. 🙂
