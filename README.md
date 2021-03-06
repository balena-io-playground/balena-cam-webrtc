# resin-cam-webrtc
A smart Raspberry Pi 3 streaming camera based on [webrtc-streamer](https://github.com/mpromonet/webrtc-streamer).

### **[Bill of Materials](https://github.com/resin-io-playground/resin-cam/blob/master/docs/BoM.md)**

## Getting started

- Sign up on [resin.io](https://dashboard.resin.io/signup) and follow our [Getting Started Guide](https://docs.resin.io/raspberrypi3/nodejs/getting-started/)
- Clone this repository to your local workspace
- Set these variables in the [`Fleet Configuration`](https://docs.resin.io/configuration/advanced/) application side tab
  - `RESIN_HOST_CONFIG_gpu_mem` = `196`
  - `RESIN_HOST_CONFIG_start_x` = `1`
- Add the _resin remote_ to your local workspace by running the useful command from the Resin dashboard
  <details>
    <summary>Hint</summary>
    <img src="https://raw.githubusercontent.com/resin-io-playground/resin-cam/master/docs/remoteadd.png" alt="Adding the Resin remote."></img>
  </details>
- Push code to your device with a simple `git push resin master`
  - See the magic happening, your device is getting updated Over-The-Air!
- If you want your device to be accessible on WAN, enable its public URL
  - Select your device from the `Devices` side tab
  - Click the `Actions` side tab
  - Click the `ENABLE PUBLIC DEVICE URL` button
  - Note down your device's public URL!
- When your device finishes updating visit your device's IP or public URL to watch your stream!
  - You can find your device's IP on the Resin dashboard.
- Add password credentials in [login.txt](config/login.txt) as described on the file
- Make sure to update your devices after every change you make! You can either:
  - Commit your changes and do another `git push resin master`
  - Learn more about the powerful [**resin-cli**](https://docs.resin.io/raspberrypi3/nodejs/getting-started/#using-resin-sync-to-develop-fast) and how you can iterate and deploy to your devices rapidly!

    Running a simple `resin sync` in your working directory will sync your changes to local devices faster than a `git push`.

## Configure via [environment variables](https://docs.resin.io/management/env-vars/)
Variable Name | Default | Description
------------ | ------------- | -------------
width | `640` | video width
height | `480` | video height
username | `user` | a configurable username credential
password | | a configurable password_hash credential (obtain it as described [here](config/login.txt))

## License

Copyright 2017 Resinio Ltd.

Licensed under the Apache License, Version 2.0 (the "License"); you may not use this file except in compliance with the License. You may obtain a copy of the License at

<http://www.apache.org/licenses/LICENSE-2.0>

Unless required by applicable law or agreed to in writing, software distributed under the License is distributed on an "AS IS" BASIS, WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied. See the License for the specific language governing permissions and limitations under the License.
