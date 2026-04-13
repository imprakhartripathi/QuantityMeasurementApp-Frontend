# Quantity Measurement App

A modern **unit-aware quantity measurement frontend** built with **React, TypeScript, Framer Motion, and OAuth2 authentication**.

The application allows users to perform **conversion, comparison, and arithmetic operations on measurable quantities** through a clean dashboard interface with history tracking, profile management, and secure authentication.

> **Note:** Arithmetic operations are intentionally restricted for **temperature quantities**, where only **convert** and **compare** are supported by design to preserve mathematical correctness.

---

## ✨ Features

### 📏 Supported Quantity Domains

* Length
* Temperature
* Volume
* Weight

### ✅ Operations

* **Convert**

  * Convert values across compatible units
  * Example: `1 Feet → 12 Inch`

* **Compare**

  * Compare quantities across different compatible units
  * Example: `1 Kilogram > 100 Gram`

* **Arithmetic Operations**

  * Add
  * Subtract
  * Divide
  * Supported for applicable quantity domains
  * **Excluded for temperature by design**

### 🧠 Smart Domain Rules

The app applies **domain-aware operational constraints**.

For example:

* Length → full arithmetic support
* Weight → full arithmetic support
* Volume → full arithmetic support
* Temperature → only convert + compare

This ensures unit logic remains physically meaningful rather than mechanically permissive.

---

## 🕘 History Tracking

* Timestamped operation history
* Scrollable previous results page
* Separate records for convert, compare, and arithmetic actions
* User-linked persistent history

---

## 👤 Profile Management

* OAuth2 / local authentication
* Editable display name
* Avatar URL support
* Provider visibility
* History count
* Session-based protected routes

---

## 🎨 UI & Experience

Built with **React + TypeScript** and enhanced using **Framer Motion**, the interface focuses on:

* smooth route transitions
* animated cards
* operation feedback
* responsive dashboard layout
* focused single-operation workflow

The design keeps the user in a tight “select → calculate → review” loop without clutter.

---

## 🛠️ Tech Stack

* **React**
* **TypeScript**
* **Framer Motion**
* **OAuth2**
* **React Router**
* **REST API integration**
* **Responsive CSS UI**

---

## 🔐 Authentication

Supported authentication flows:

* Local authentication
* OAuth2 login
* Protected routes
* Persistent sessions
* User-specific operation history

---

## 🎯 Design Philosophy

This project treats **units as logic-bearing entities, not decorative labels**.

Instead of allowing mathematically invalid workflows, the UI respects domain semantics:

* arithmetic where it makes sense
* restricted operations where it does not
* backend-supported unit consistency
* type-safe frontend state transitions

That makes it feel closer to an engineering tool than a generic converter.
