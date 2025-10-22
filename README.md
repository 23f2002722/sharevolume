# CDW Corporation Share Data Viewer

This is a single-file web application designed to fetch and display the maximum and minimum Entity Common Stock Shares Outstanding for CDW Corporation (or any specified CIK) from the SEC's XBRL data API. The application filters data for fiscal years (`fy`) greater than "2020" and presents the highest and lowest values found.

## Features

*   **Dynamic Data Fetching:** Retrieves real-time (as per SEC API) common stock shares outstanding data.
*   **Max/Min Analysis:** Identifies and displays the maximum and minimum share values along with their corresponding fiscal years for post-2020 data.
*   **Configurable CIK:** Defaults to CDW Corporation's CIK (`0001402057`), but can be updated via URL parameters.
*   **Responsive UI:** Built with Tailwind CSS for a modern and responsive user experience across different devices.
*   **SEC Compliance:** Sets a descriptive `User-Agent` for direct API calls to comply with SEC guidance. Utilizes a proxy for dynamic CIK requests as per prompt specification.

## How to Run

1.  **Save the file:** Save the content of `index.html` into a file named `index.html`.
2.  **Open in Browser:** Open `index.html` in your web browser.

The application will automatically fetch and display the share data for CDW Corporation.

## Custom CIK Usage

To view data for a different company, you can append a `CIK` parameter to the URL. For example, to view data for Apple Inc. (CIK `0000320193`), you would open:

`index.html?CIK=0000320193`

*Note: For dynamic CIKs provided via URL parameters, the application uses a public CORS proxy (`https://api.allorigins.win/raw?url=`) to bypass potential browser CORS restrictions when fetching data from the SEC API. This proxy handles the `User-Agent` requirement to the SEC endpoint.*

## Data Source

The data is sourced directly from the U.S. Securities and Exchange Commission (SEC) XBRL data API: `https://data.sec.gov/api/xbrl/companyconcept/CIK<CIK_NUMBER>/dei/EntityCommonStockSharesOutstanding.json`.

## Project Structure

*   `index.html`: The main web application file, containing all HTML, Tailwind CSS, and JavaScript logic.
*   `README.md`: This README file.
*   `LICENSE`: The MIT License for this project.
*   `uid.txt`: An additional project file as specified in the prompt. (This file is not directly used by the `index.html` application logic but is part of the project delivery.)

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.
