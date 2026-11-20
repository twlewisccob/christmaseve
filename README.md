# Updating the Events Board

## Where to add events

Open **`events-script.js`**. Make your weekly changes at the very top, in the **WEEKLY UPDATE ZONE**:

- Change `WEEK_OF` to the Monday date for the new week.
- Replace the old entries inside `EVENTS` with the new events.
- Do not edit anything below `RENDER LOGIC`—that code displays the events.

The page loads `events-script.js`. Do not enter events in `events-script copy.js`.

## Add one event

Copy this object and paste it inside the `EVENTS` brackets (`[` and `]`):

```javascript
{
  day: "Monday",
  date: "November 16",
  time: "12 - 1 PM",
  title: "Name of the event",
  location: "Room or venue",
  desc: "Optional extra details",
  link: "https://example.com"
}
```

Replace the example text with the event information. Repeat the object for each event. Put a comma after every event object except the last one.

Required fields:

- `day`: Full weekday name, with the first letter capitalized: `Monday`, `Tuesday`, `Wednesday`, `Thursday`, `Friday`, `Saturday`, or `Sunday`.
- `date`: The date shown next to that weekday, such as `"November 16"`.
- `time`: Display text, such as `"3 - 4 PM"` or `"All Day"`.
- `title`: Event name.
- `location`: Room or venue.

`desc` and `link` are optional. If you have no description or link, remove those lines. Keep the comma after `location` if another field follows it.

## Example: two events

```javascript
const WEEK_OF = "November 16, 2026";

const EVENTS = [
  {
    day: "Monday",
    date: "November 16",
    time: "12 - 1 PM",
    title: "Club Meeting",
    location: "CCOB Lobby"
  },
  {
    day: "Tuesday",
    date: "November 17",
    time: "3 - 4 PM",
    title: "Guest Speaker",
    location: "Room 42-317",
    desc: "Meet the speaker after the presentation.",
    link: "https://example.com"
  }
];
```

After editing, save the file and refresh the events page. Check that the week label and each event appear on the correct day.

You will find the events on the boards on the first floor of CCOB
