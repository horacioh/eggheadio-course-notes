<h1 align="center"><a href="https://egghead.io/lessons/aws-build-and-deploy-a-sample-aws-cloud-development-kit-stack-to-aws">Build an App with the AWS Cloud Development Kit</a></h1>

<p align="center">
<!-- ALL-CONTRIBUTORS-BADGE:START - Do not remove or modify this section -->

[![All Contributors](https://img.shields.io/badge/all_contributors-1-orange.svg?style=flat-square)](#contributors-)

<!-- ALL-CONTRIBUTORS-BADGE:END -->
</p>

## About 🔍

This repo contains notes from [Colby Fayock](https://twitter.com/colbyfayock)'s Egghead Collection [Build Maps with React-Leaflet](https://egghead.io/lessons/egghead-course-introduction-00086daf).

These notes contain the same structure as the transcriptions, along with additional rewrites, links to resources, and personal takes on the lesson. Feel free to submit additions to these notes, but please don't remove anything (unless we messed up or misunderstood something).

Generally, there is one document for each video in the course. However, because the videos are rather short (and there's over 60 of them), I've further grouped them into 10 directories (or lessons). Colby further bundles the videos into 3 major groups.

So 1 video collection -> 3 groups -> 10 lessons -> many exercises -> 61 videos!

I wanted to avoid creating subdirectories, so I kept the 10 lesson structure.

## Course Objective 💪

The main goal of this course is to create a simple restaurant locator app!

On this journey we will also:

- Learn what the Leaflet mapping library is and what it does
- Add a map to a `create-react-app` project using `React-Leaflet`
- Learn about `Map`, `TileLayer`, `Marker` and `Popup` components
- Learn about Mapbox
- Learn about GeoJSON
- Learn about Leaflet API

## 🤓 Notes on the notes:

This is a really well structured and super beginner-friendly course. Some prior knowledge of React is recommended, but not required.

If you are a less experienced developer, I recommend watching the course twice: just watch it once then code-along for the second time around.

If you are slightly more advanced, I'd suggest to try and complete the exercises before watching the course for solutions. You'll find Colby's comments instructing you what needs doing sprinkled throughout the codebase.

I didn't have any experience with creating maps beforehand, and this course served as a great introduction. Colby is very intentional in his teaching and expertly mixes new content with exercises, reviews, and deliberate practice, which results in a great learning experience.

I enjoyed it thoroughly and I hope you do too! Eva Dee ✏️

### Emoji Legend

| emoji |        explanation        |
| ----- | :-----------------------: |
| 📹    | links to the course video |
| 💻    |     course repository     |
| ⌨️    |     keyboard shortcut     |
| 🤔    |   additional resources    |
| 👍    |       good practice       |

## Who is Colby Fayock? 👨‍💻

A Front End Engineer and UX Designer that’s passionate about tackling challenges that can help save people’s lives and make the world a better place.

You can find [Colby on Twitter](https://twitter.com/colbyfayock)

[Other Egghead content](https://egghead.io/instructors/colby-fayock) created by Colby.

## Table of Contents

- [00-Intro and Welcome](00-intro-and-welcome.md)

- [01-Course Introduction](Lesson01/01-course-introduction.md)

- [02-Lesson 1 - A Little Overview About Maps](Lesson01/02-lesson-1-a-little-overview-about-maps.md)

- [03-Update the Avatar Image to a Picture of Yourself](Lesson01/03-update-the-avatar-image-to-a-picture-of-yourself.md)

- [04-Group 1 - Your First Map](Lesson02/04-group-1-your-first-map.md)

- [05-Lesson 2 - Adding Your First React Leaflet Map to a New React Application](Lesson02/05-lesson-2-adding-your-first-react-leaflet-map-to-a-new-react-application.md)

- [06-Install leaflet and react-leaflet](Lesson02/06-install-leaflet-and-react-leaflet.md)

- [07-Adding a New Map to the Search Page](Lesson02/07-adding-a-new-map-to-the-search-page.md)

- [08-Style leaflet Map using CSS](Lesson02/08-style-leaflet-map-using-css.md)

- [09-Lesson 3 - Customizing Your React Leaflet Map with a Mapbox Basemap Style](Lesson03/09-lesson-3-customizing-your-react-leaflet-map-with-a-mapbox-basemap-style.md)

- [10-Create a Mapbox Account](Lesson03/010-create-a-mapbox-account.md)

- [11-Creating a Map Style in Mapbox](Lesson03/11-creating-a-map-style-in-mapbox.md)

- [12-Creating an API key in Mapbox](Lesson03/12-creating-an-api-key-in-mapbox.md)

- [13-Configure a Mapbox Endpoint for our Map Style](Lesson03/13-configure-a-mapbox-endpoint-for-our-map-style.md)

- [14-Customize Our Map with Our Map Style Endpoint](Lesson03/14-customize-our-map-with-our-map-style-endpoint.md)

- [15-Using Our Tile Endpoint for Our Map](Lesson03/15-using-our-tile-endpoint-for-our-map.md)

- [16-Create a New Basemap Style](Lesson03/16-create-a-new-basemap-style.md)

- [17-Create an Environment Variable for the API Key](Lesson03/17-create-an-environment-variable-for-the-api-key.md)

- [18-Lesson 4 - Adding a Marker to a Map to Point to a Location with React Leaflet](Lesson04/18-lesson-4-adding-a-marker-to-a-map-to-point-to-a-location-with-react-leaflet.md)

- [19-Find Our Favorite Location](Lesson04/19-find-our-favorite-location.md)

- [20-Add a Marker Component with our Location](Lesson04/20-add-a-marker-component-with-our-location.md)

- [21-Fix a Library Conflict so our Marker Image Shows](Lesson04/21-fix-a-library-conflict-so-our-marker-image-shows.md)

- [22-Add a Popup Component to Display the Name of our Location](Lesson04/22-add-a-popup-component-to-display-the-name-of-our-location.md)

- [23-Add a Second Marker for your Second Favorite Location](Lesson04/23-add-a-second-marker-for-your-second-favorite-location.md)

- [24-Group 2 - Managing Map Data](Lesson05/24-group-2-managing-map-data.md)

- [25-Lesson 5 - Managing Leaflet State in a React App with Hooks](Lesson05/25-lesson-5-managing-leaflet-state-in-a-react-app-with-hooks.md)

- [26-Adding a ref to Our Map Component](Lesson05/26-adding-a-ref-to-our-map-component.md)

- [27-Accessing our Leaflet Map Instance Inside a React useEffect Hook](Lesson05/27-accessing-our-leaflet-map-instance-inside-a-react-use-effect-hook.md)

- [28-Use our Leaflet Map Instance to re-add our Marker to the Map](Lesson05/28-use-our-leaflet-map-instance-to-re-add-our-marker-to-the-map.md)

- [29-Review a Simple Example of Mismanaged State](Lesson05/29-review-a-simple-example-of-mismanaged-state.md)

- [30-Recreate the Marker from our Second Favorite Location](Lesson05/30-recreate-the-marker-from-our-second-favorite-location.md)

- [31-Lesson 6 - Create Your First GeoJSON Document and Add Restaurant Locations to the Map](Lesson06/31-lesson-6-create-your-first-geo-json-document-and-add-restaurant-locations-to-the-map.md)

- [32-Understanding the Basics of GeoJSON](Lesson06/32-understanding-the-basics-of-geo-json.md)

- [33-Using geojson.io to Create Your First GeoJSON Document](Lesson06/33-using-geojson-io-to-create-your-first-geo-json-document.md)

- [34-Manually Add a New Restaurant Location to the GeoJSON Document](Lesson06/34-manually-add-a-new-restaurant-location-to-the-geo-json-document.md)

- [35-Create a New GeoJSON File and Import it into the App](Lesson06/35-create-a-new-geo-json-file-and-import-it-into-the-app.md)

- [36-Add GeoJSON Location Data to the Map](Lesson06/36-add-geo-json-location-data-to-the-map.md)

- [37-Add Another Location to the Map](Lesson06/37-add-another-location-to-the-map.md)

- [38-Lesson 7 - Add Restaurant Info to GeoJSON Documents and Display it in a Tooltip on the Map](Lesson07/38-lesson-7-add-restaurant-info-to-geo-json-documents-and-display-it-in-a-tooltip-on-the-map.md)

- [39-Updating our GeoJSON Data to Include Restaurant Information](Lesson07/39-updating-our-geo-json-data-to-include-restaurant-information.md)

- [40-Adding Popups to all of our Markers](Lesson07/40-adding-popups-to-all-of-our-markers.md)

- [41-Adding Restaurant Information to our Popups](Lesson07/41-adding-restaurant-information-to-our-popups.md)

- [42-Update the Styles of our Popups](Lesson07/42-update-the-styles-of-our-popups.md)

- [43-Change the Background Color of the Popup](Lesson07/43-change-the-background-color-of-the-popup.md)

- [44-Add Another Restaurant Attribute](Lesson07/44-add-another-restaurant-attribute.md)

- [45-Group 3 - Customizing Your Map](Lesson08/45-group-3-customizing-your-map.md)

- [46-Lesson 8 - Add Restaurant Delivery Zones to Map with Shaded Regions](Lesson08/46-lesson-8-add-restaurant-delivery-zones-to-map-with-shaded-regions.md)

- [47-Adding a Delivery Radius to our Restaurant Data](Lesson08/47-adding-a-delivery-radius-to-our-restaurant-data.md)

- [48-Using the Delivery Radius to add a Shaded Circle to the Map](Lesson08/48-using-the-delivery-radius-to-add-a-shaded-circle-to-the-map.md)

- [49-Only Showing the Delivery Radius on Marker Hover](Lesson08/49-only-showing-the-delivery-radius-on-marker-hover.md)

- [50-Change the Color of the Delivery Zone](Lesson08/50-change-the-color-of-the-delivery-zone.md)

- [51-Lesson 9 - Customize Restaurant Location Markers with Custom Images](Lesson09/51-lesson-9-customize-restaurant-location-markers-with-custom-images.md)

- [52-Recreate Restaurant Markers with GeoJSON Configuration Option](Lesson09/52-recreate-restaurant-markers-with-geo-json-configuration-option.md)

- [53-Replace the Default Location Markers with a Custom Image](Lesson09/53-replace-the-default-location-markers-with-a-custom-image.md)

- [54-Add the Default Shadows back to our Markers](Lesson09/54-add-the-default-shadows-back-to-our-markers.md)

- [55-Replace the Marker with Custom HTML and Style with CSS](Lesson09/55-replace-the-marker-with-custom-html-and-style-with-css.md)

- [56-Lesson 10 - Use Leaflet's Geolocation API to Find Locations Near You](Lesson10/56-lesson-10-use-leaflet-s-geolocation-api-to-find-locations-near-you.md)

- [57-Add a Marker to a Location when Clicking a Button](Lesson10/57-add-a-marker-to-a-location-when-clicking-a-button.md)

- [58-Create a Button taht Finds your Location and Navigates the Map to that Location](Lesso010/58-create-a-button-taht-finds-your-location-and-navigates-the-map-to-that-location.md)

- [59-Use the Browser's Location to Add a Marker to the Map](Lesson10/59-use-the-browser-s-location-to-add-a-marker-to-the-map.md)

- [60-Add a Circle to the Map Designing the Accuracy of the Browser's Location](Lesson10/60-add-a-circle-to-the-map-designing-the-accuracy-of-the-browser-s-location.md)

- [61-Clean up Location Event handler Resources when Page Unmounts](Lesson10/61-clean-up-location-event-handler-resources-when-page-unmounts.md)

## Contributors ✨

Thanks goes to these wonderful people ([emoji key](https://allcontributors.org/docs/en/emoji-key)):

<table>
  <tr>
    <td align="center"><a href="https://github.com/edieblu"><img src="https://avatars0.githubusercontent.com/u/17270662?s=460&u=8d1a4d67576db0a3baa21fa5b2ecab811476da61&v=4" width="100px;" alt=""/><br /><sub><b>Eva</b></sub></a><br /><a href="#review-edieblu" title="Review">👀</a><a href="#content-edieblu" title="Content">🖋</a></td>
</table>
