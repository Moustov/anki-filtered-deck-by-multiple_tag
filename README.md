# Filtered Deck From Tag (Multi-tag Selection)

An Anki add-on that creates a filtered deck directly from the browser sidebar with interactive multi-tag filtering. It allows you to study specific tags or combine multiple tags dynamically without manually typing search queries.

## Features

- **Sidebar Context Menu**: Right-click any tag in the browser sidebar to quickly generate a filtered deck.
- **Interactive Multi-Tag Selection**: Select additional existing tags from a checkbox dialog to intersect search criteria (e.g., combining an instrument tag with a specific music theory tag).
- **Automatic Naming**: Automatically names the generated filtered deck based on the selected tags.
- **Auto-Unsuspend Option**: Option to automatically unsuspend matching cards when building the filtered deck.

---

## Usage

1. Open the **Anki Browser** (`B`).
2. Right-click any tag in the left sidebar.
3. Select **"Create Filtered Deck"** from the context menu.
4. A dialog window titled **"Combine with other tags"** will pop up, displaying all existing tags in your collection.
5. *(Optional)* Check any additional tags you wish to combine with the target tag.
6. Click **OK**. The filtered deck will be automatically created, updated, and built.

---

## Configuration

Configuration options can be modified from **Tools → Add-ons → Select the add-on → Config**.

### Options

* **`numCards`** *(integer)*: Maximum number of cards to pull into the filtered deck. Default is `300` (or up to `9999`).
* **`unsuspendAutomatically`** *(boolean)*: When set to `true`, automatically unsuspends cards matched by the search query. Set to `false` to disable this behavior.
* **`defaultOrder`** *(integer)*: Specifies the sorting order of cards in the created filtered deck.

#### Order Values:
* `0`: Oldest
* `1`: Random
* `2`: Increasing intervals
* `3`: Decreasing intervals
* `4`: Most lapses
* `5`: Order added
* `6`: Order due *(default)*
* `7`: Latest added first
* `8`: Relative overdueness

For more details on sorting orders, see the [Anki User Manual](https://docs.ankiweb.net/filtered-decks.html#order).

### Example Configuration

```json
{
    "numCards": 300,
    "unsuspendAutomatically": true,
    "defaultOrder": 6
}
