# MeasureCamp Dubai - Attendee Card Generator

This repository contains a web-based tool that allows attendees of MeasureCamp Dubai 2024 to create and download personalized attendee cards. The tool provides a simple interface for users to enter their name, upload a profile picture, and generate a card ready for download and sharing on social media.

## Features

- **Name Input Validation:** Ensures the name field is not empty or just spaces, with a suggestion to use initials for long names.
- **Profile Picture Upload:** Users can upload and adjust their profile pictures with zoom and positioning controls.
- **Downloadable Card:** The tool generates a high-resolution attendee card that can be downloaded and shared on social media or used at the event.
- **Social Media Sharing Encouragement:** Attendees are encouraged to share their personalized cards on platforms like LinkedIn.

## Background Image

The tool overlays the profile picture and name onto a base image called `background.png`. This file is not included in the repository, and you'll need to create your own. The `background.png` should include areas where the profile picture and name will be placed.

### Guidelines for Creating `background.png`:

- **Size:** The recommended size for the `background.png` file is 1200x1200 pixels.
- **Profile Picture Area:** Leave space around the center for the profile picture. By default, the profile picture is centered at (866px, 417px) with a size of 500px.
- **Name Area:** Leave space for the name text. By default, the name text is centered at (894px, 800px). Ensure that the background image design accommodates this placement.

After creating your `background.png` file, place it in the same directory as your `index.html` file. The tool will then use this image as the base for generating the attendee cards.

## Configuration

The `downloadCard` function in the tool includes several configurable variables to customize the output of the attendee card. Below is a summary of the key variables and how to adjust them:

### Configurable Variables

- **Profile Picture Size and Position:**
  - `profilePicSize`: Defines the size of the profile picture in pixels (default is 500px).
  - `profilePicX`: The X-coordinate for the center of the profile picture (default is 866px).
  - `profilePicY`: The Y-coordinate for the center of the profile picture (default is 417px).

- **Name Text Position:**
  - `nameX`: The X-coordinate for the center of the name text (default is 894px).
  - `nameY`: The Y-coordinate for the name text (default is 800px).

- **Name Text Formatting:**
  - `maxWidth`: The maximum width of the name text before it wraps (default is 400px).
  - `lineHeight`: The space between lines of text (default is 70px).
  - `nameColor`: The color of the name text (default is `#ffffff`).
  - `nameStyle`: The font style and size for the name text (default is `'bold 60px Helvetica'`).

### Example

To change the profile picture size and position, you can modify the `downloadCard` function as follows:

```javascript
function downloadCard() {
    // Configurable variables
    const profilePicSize = 600;  // Increase the profile picture size
    const profilePicX = 900;  // Adjust the X position of the profile picture
    const profilePicY = 450;  // Adjust the Y position of the profile picture
    // ... rest of the function
}
