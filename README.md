# GreenHouse
A local application to monitor local greenhouse environmental conditions.

Not entirely sure how to go about doing this. All of this. App design, data storage, data transmition, app ui updates, etc.
Basically building a user service from scratch for the first time and learning as I go along, 
so it will be a work in progress and will likely see multiple revisions/releases.

Diction and Acronyms
  - EC : Environmental Conditions - the conditions represented by the data collected
  - ECD : Environmental Condition Data - data collected from inside the greenhouse to be displayed on the application
          Environmental conditions will include:
          - Temperature
          - Atmospheric Humidity
          - Wind Speed
          - Soil moisture
          - Soil pH
Technology

Different sensors will be placed inside of the greenhouse to collect ECD.
ECD is then sent to a raspberry pi.
V1 - transmit data through wired connections to raspberry pi
V2 - transmit data wirelessly through a mesh network using a Boron LTE

Raspberry Pi will serve as the Host/Database for the application.
- will store application files:
    - UI files : HTML/CSS/JavaScript or whatever I use to create the User Interface
    - Business Logic
        - Collect, manipulate, format data
        - Populate UI
        - Present/Host UI
User Interface Side
  - Would Like to make a website that can be found via IP address (to start)
      - Will make a version for desktop and IPhone SE to start
  - Would like to develop an IOS application that I can open from my phone rather than safari
 
Future goals: 
  - Add EC Control from App:
      - give users the ability to control ECs that can be controlled
      - EG: control wind speed, temperature, humidity
  - Automate EC corrections:
      - Rather than just recording and presenting data, try to regulate data
      - EG: tech in greenhouse controls the ECs
  - Add user save ability
      - Allow user to select plants they have in greenhouse
        - has default settings based on research.
            - allow users to read this research
        - allow user to overwrite/save settings for plants
        - Auto control ECs to match settings