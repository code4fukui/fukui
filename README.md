# fukui

> 日本語のREADMEはこちらです: [README.ja.md](README.ja.md)

An interactive map application, "Fukui Open Event Navi," that visualizes open data from Fukui Prefecture. It displays events, public facilities, restaurants, and other points of interest using data from the Fukui Open Data Portal.

## Demo

:earth_asia: **Live Map:** [https://codeforfukui.github.io/fukui/map.html](https://codeforfukui.github.io/fukui/map.html)

## Features

-   **Interactive Map:** Displays locations of events, public facilities, restaurants, and points of interest across Fukui Prefecture.
-   **Detailed Information:** Click any icon to view details like address, phone number, operating hours, and relevant links in an info window.
-   **Live Data:** Fetches data dynamically from live SPARQL endpoints, ensuring the information is up-to-date.
-   **Mobile-Friendly:** Responsive design optimized for both desktop and mobile devices.

## Setup and Usage

This is a client-side application that runs directly in a web browser.

1.  **Clone the repository:**
    ```sh
    git clone https://github.com/codeforfukui/fukui.git
    cd fukui
    ```

2.  **Configure Google Maps API Key:**
    The project requires a Google Maps API key to function. Open `map.html` and replace the placeholder key in the following line with your own:
    ```html
    <script src="https://maps.google.com/maps/api/js?key=AIzaSyCfbWrf5isAqdEGdSNxa_NeUDqThEmRt8Q"></script>
    ```

3.  **Open in Browser:**
    Open the local `map.html` file in your web browser to run the application.

## Data Sources

This project queries open data from Fukui Prefecture via the following SPARQL endpoints:

-   **Fukui Open Data Platform (odp.jig.jp):** `https://sparql.odp.jig.jp/data/sparql`
-   **OpenData.cc:** `https://sparql.opendata.cc/data/sparql`

The application primarily visualizes datasets for civic facilities (`jrrk#CivicFacility`) and points of interest (`jrrk#CivicPOI`).

## License

MIT License — see [LICENSE](LICENSE).