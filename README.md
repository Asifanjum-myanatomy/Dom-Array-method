# DOM Array Methods

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)

A simple vanilla JavaScript application demonstrating the power of array methods (`map`, `filter`, `sort`, `reduce`) to manipulate and display user wealth data dynamically in the DOM.

---

## Table of Contents

- [Demo](#demo)
- [Features](#features)
- [Installation](#installation)
- [Usage](#usage)
- [API Endpoints](#api-endpoints)
- [Functional Overview](#functional-overview)
- [Contributing](#contributing)
- [License](#license)

---

## Demo

![gif-demo](https://user-images.githubusercontent.com/yourusername/your-repo/demo.gif)

> Three random users are fetched on load. Use the sidebar controls to interact with the list of users and their virtual wealth.

---

## Features

- **Add User** 👱‍♂️: Fetch a new random user profile.
- **Double Money** 💰: Double each user’s wealth using `map()`.
- **Show Only Millionaires** 💵: Filter out users with ≤ $1,000,000 using `filter()`.
- **Sort by Richest** ↓ ("FortuneRanker"): Sort users in descending order of wealth with `sort()`.
- **Calculate Entire Wealth** 🧮: Aggregate total wealth via `reduce()` and display it in the UI.

---

## Installation

1. **Clone the repository**:
   ```bash
   git clone https://github.com/yourusername/dom-array-methods.git
   cd dom-array-methods
   ```

2. **Open `index.html`** in your browser (no build steps required).

---

## Usage

- Open `index.html` in your favorite modern browser.
- Interact with the sidebar buttons to fetch users, manipulate wealth, and see live updates.

---

## API Endpoints

This project uses the [Random User API](https://randomuser.me/) to fetch dummy profile data:

```
GET https://randomuser.me/api/
```

The application only needs this one endpoint to generate new users.

---

## Functional Overview

```text
script.js
├── getRandomUser()       # Fetches a random user and adds to `data`
├── addData(obj)          # Pushes `obj` into the `data` array, then calls `updateDOM()`
├── updateDOM(arr)        # Clears and rebuilds the `<main>` content based on `arr`
├── formatMoney(num)      # Utility to format a number as US currency
├── doubleMoney()         # data = data.map(user => user.money * 2)
├── showMillionaires()    # data = data.filter(user.money > 1_000_000)
├── sortByRichest()       # data.sort((a,b) => b.money - a.money)   ← FortuneRanker
└── calculateWealth()     # total = data.reduce(...); append result to DOM
```

**Styling** is handled in `style.css` with a flexbox layout for sidebar and main area, and simple, clean button/element styles.

---

## Contributing

Contributions are welcome! Feel free to open issues or pull requests to add features, fix bugs, or improve documentation.

1. Fork the repo
2. Create a feature branch (`git checkout -b feature/name`)
3. Commit your changes (`git commit -m "feat: Add ..."`)
4. Push to branch (`git push origin feature/name`)
5. Open a pull request

---

## License

Distributed under the MIT License. See [LICENSE](LICENSE) for more information.

---

*Built with 💖 by MD Asif Anjum*

