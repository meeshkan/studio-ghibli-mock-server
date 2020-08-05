# Studio Ghibli Mock Server

[![Chat on Gitter](https://badges.gitter.im/gitterHQ/gitter.png)](https://gitter.im/meeshkan/community)

This repository contains the source code for our article: [Create a mock server for any REST API](https://meeshkan.com/blog/create-a-mock-server/). It features a **mock server of the [Studio Ghibli API](https://ghibliapi.herokuapp.com/)** created with the [HTTP Mocking Toolkit (HMT)](https://github.com/meeshkan/hmt/).

If you run into any problems or have any questions, please [open an issue](https://github.com/meeshkan/studio-ghibli-mock-server/issues/new) or [reach out on Gitter](https://gitter.im/meeshkan/community).

## Running the server

⚠️ **Prerequisites**:
- [Python 3.6+](https://www.python.org/downloads/)

> There's a lot of assumed knowledge in this section, including a familiarity with things like virtual environments and the HMT tool. For step-by-step instructions, please refer to [our tutorial](https://meeshkan.com/blog/create-a-mock-server/).

Clone this repository and move into the directory:
```bash
git clone https://github.com/meeshkan/studio-ghibli-mock-server.git
cd studio-ghibli-mock-server
```

After launching your [virtual environment](https://docs.python.org/3/library/venv.html), install HMT via [pip](https://pip.pypa.io/en/stable/installing/):
```bash
pip install hmt
```

Next, run the `mock` command:
```bash
hmt mock specs/
```

Keep this running. Then, in another terminal window, make a [curl](https://curl.haxx.se/) request based on the Studio Ghibli API schema. Because HMT runs on the default port of `8000`, this request will look something like:

```bash
curl http://localhost:8000/https://ghibliapi.herokuapp.com/people
```

There you have it, a mock response from a mock server 🎉

## Contributing

Notice a bug? Interested in adding a custom callback? The best way to get involved is to [open an issue](https://github.com/meeshkan/studio-ghibli-mock-server/issues/new).

Please note that this project is governed by the [Meeshkan Community Code of Conduct](https://github.com/meeshkan/code-of-conduct). By participating, you agree to abide by its terms.

## Tell us what you think

At [Meeshkan](https://meeshkan.com/), we're working to improve how people test their products. So no matter what you thought of this tutorial, we want to hear from you.

Here are some ways you can get in touch:

- [Open an issue](https://github.com/meeshkan/studio-ghibli-mock-server/issues/new)
- [Tweet at us](https://twitter.com/meeshkan)
- [Reach out on Gitter](https://gitter.im/Meeshkan/community)