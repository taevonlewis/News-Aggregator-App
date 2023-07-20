# News Aggregator App

## Table of Contents
1. [Overview](#overview)
2. [Features](#features)
3. [Technical Implementation](#technical-implementation)
4. [Key Learnings](#key-learnings)
5. [Getting Started](#getting-started)
6. [Acknowledgements](#acknowledgements)

## Overview

News Aggregator App is a modern iOS application developed in Swift. The app fetches real-time news from the [NewsAPI](https://newsapi.org/), and presents a digest to the user. Users can delve into more detailed news views, and also filter news by category.

The app serves as a rich playground of Swift and UIKit advanced topics, and effectively demonstrates usage of design patterns, asynchronous programming, API interactions, and more.

## Features

- Real-time news feed: Fetches and displays a real-time list of news articles from NewsAPI. 

- Detailed news view: When an article is selected, users can view detailed news content.

- Category filter: Allows users to select categories of news to view.

- Offline support: The app displays the last fetched news articles when offline.

## Technical Implementation

- The app uses **storyboards** and **programmatic UIKit** to create the user interfaces. This allows comparison and evaluation of the strengths of each approach.

- It uses **AutoLayout** to ensure consistency across different device sizes and orientations.

- The **Singleton Design Pattern** is employed to manage the API calls, ensuring that only a single instance of the class responsible for API communication exists throughout the app's lifecycle.

- The **Factory Design Pattern** is used to create the category filter feature. This design enables flexibility to add more filters or modify existing ones in the future.

- The **Observer Design Pattern** is employed in conjunction with **NotificationCenter**, which notifies the app of changes in the filter settings, and consequently, updates the news feed.

- The app handles API calls and JSON parsing asynchronously. It uses **Grand Central Dispatch (GCD)** for multithreading and **Futures & Promises** for elegant asynchronous code, ensuring the UI remains responsive.

- The app leverages **Caching** for offline functionality. The last fetched news articles are cached and displayed to the user when the app is offline.

## Key Learnings

- Application of advanced Swift concepts such as Generics and Associated Types.

- Asynchronous programming in Swift, and managing threads with GCD and Futures & Promises.

- Implementing Auto Layout both programmatically and with Interface Builder.

- Building complex user interfaces with UIKit.

- Fetching and parsing JSON from a REST API using URLSession.

- Understanding and implementing the Singleton, Factory, and Observer design patterns.

- Efficient use of Notification Center for broadcasting events across different components of the app.

- Implementing a simple caching mechanism for offline data viewing.

## Getting Started

Clone the repository and open the Xcode project to get started. Make sure to get an API Key from [NewsAPI](https://newsapi.org/) and replace `"YOUR_API_KEY"` with your actual key in the `NetworkManager` file.

```bash
git clone https://github.com/yourgithubusername/NewsAggregatorApp.git
open NewsAggregatorApp.xcodeproj
```

## Acknowledgements
The News Aggregator App was developed to practice and solidify advanced Swift and UIKit concepts, and to provide a strong reference for these concepts and their implementation in a real-world project.
