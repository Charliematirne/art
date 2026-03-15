1. FX Terminal Scanner (fx_terminal_scanner.py)

The FX Terminal Scanner acts as the visual dashboard and monitoring interface for the system.

Its primary role is to display live market data and update the user when important macroeconomic news events occur.

Main Responsibilities

• Display real-time price movements across major FX pairs
• Monitor macro market proxies such as USD strength and volatility indicators
• Provide a single-screen terminal dashboard that updates in place
• Highlight significant price movements following major news events

Interface Behavior

The dashboard continuously refreshes without scrolling and color-codes market activity:

Color	Meaning
Green	Upward price movement
Red	Downward price movement
Neutral	Minimal market change

This allows the user to quickly identify abnormal market reactions following a news release.

2. News Scanner (scanner.py)

The scanner module is responsible for identifying high-impact macroeconomic news events.

It continuously monitors incoming financial news feeds and filters headlines based on predefined criteria for Tier-1 significance.

Main Responsibilities

• Poll financial news sources for breaking headlines
• Filter events based on macroeconomic relevance
• Identify Tier-1 events such as:

Central bank announcements

inflation data releases

employment reports

geopolitical developments

unexpected policy changes

When a Tier-1 event is detected, the system triggers a market reaction tracking process.

Event Trigger

Once a qualifying event is detected:

The event timestamp is recorded

The monitoring system begins tracking FX price movement

Market activity is observed until the initial reaction fades

This allows the system to measure how strongly the market reacts to specific news events.

3. Event Catalog (Historical Database)

The event catalog is a structured database that stores historical Tier-1 news events and their corresponding market reactions.

It functions as the research layer of the system.

Data Stored

Each recorded event includes:

Field	Description
Event timestamp	Exact time the news was released
Headline	Summary of the news event
Currency pair	Pair showing the strongest reaction
Peak movement	Maximum pip movement following the event
Reaction duration	Time between release and peak move
Fall-off point	When the initial move begins to fade
Purpose of the Catalog

The catalog enables long-term analysis of how FX markets behave during major macroeconomic events.

It allows users to:

• identify historical reaction patterns
• measure volatility during major announcements
• compare similar events across time
• analyze which currencies react most strongly to specific types of news

Over time, this database becomes a research tool for understanding macro-driven market behavior.

System Workflow

The system operates through the following process:

News feeds are continuously scanned for major macroeconomic headlines.

When a Tier-1 event is detected, the timestamp is recorded.

The FX market is monitored for abnormal price movement.

The strongest currency reaction is identified.

Reaction data is stored in the historical event catalog.

Goal of the Project

The objective of the system is to build a structured dataset that connects macroeconomic news events to real FX market reactions.

By cataloging these events over time, the system provides insights into:

• how quickly markets react to major news
• which currencies respond most strongly
• how long news-driven moves typically last
