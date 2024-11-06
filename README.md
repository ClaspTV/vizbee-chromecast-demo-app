# Vizbee Chromecast Demo App

This application demonstrates how to integrate Vizbee casting functionality into a Google Cast Application Framework (CAF) receiver app. It combines the capabilities of both platforms to provide a comprehensive casting solution.

## Integration Steps

Look for the block comments with text "[BEGIN] Vizbee Integration" and "[END] Vizbee Integration" in the code for an easy understanding of the integration points.

### Prerequisites

- A Google Cast developer account
- Access to the [Google Cast SDK Developer Console](https://cast.google.com/publish)
- A Vizbee developer account and SDK access
- HTTPS-enabled web hosting for the receiver app

### Setup

1. Clone this repository:
   ```bash
   git clone git@github.com:ClaspTV/vizbee-chromecasr-demo-app.git
   ```

### Configuration

1. - Replace the Demo Vizbee App ID with your actual App ID: `vzbInstance.start('vzb2000001');` in `js/receiver.js`.

### Running the App

1. Simply deploy the contents of the application directory to your HTTPS-enabled web server
3. Register your receiver in the [Google Cast SDK Developer Console](https://cast.google.com/publish)
4. Update your sender applications with the your application ID

## Project Structure

```
.
├── css/
│   └── receiver.css
├── js/
│   ├── agents/
│   │   ├── google_analytics.js
│   ├── cast_analytics.js
│   ├── cast_event_types.js
│   ├── media_fetcher.js
│   ├── queuing.js
│   └── receiver.js
├── res/
│   └── [image assets]
├── index.html
└── README.md
```

| File/Folder | Description |
|------------|-------------|
| index.html | Main HTML file with player and UI structure |
| js/receiver.js | Application entry point |
| js/agents | Core functionality modules |
| res/ | Image and media assets |
| css/ | Application styling |

## Features

- Compliant with Cast Design Checklist
- Integrated Vizbee receiver functionality
- Support for various media types
- Queue management
- Analytics integration
- Customizable UI

## Testing

1. Use the [Chrome Remote Debugger](https://developers.google.com/cast/docs/debugging#chrome) for development
2. Test on actual Cast devices
3. Verify both Chromecast and Vizbee casting functionality

## Troubleshooting

Common issues and solutions:

1. Cast device not discovering the receiver:
   - Verify the device is registered in the Cast Developer Console
   - Ensure the receiver URL is accessible via HTTPS
   - Check that the application ID is correct in both sender and receiver

2. Media playback issues:
   - Verify media URLs are accessible and CORS-enabled
   - Check browser console for detailed error messages
   - Ensure proper media format support

## Support

- For Chromecast-specific issues: Visit [Google Cast SDK Support](https://developers.google.com/cast/support)
- For Vizbee-related questions: Contact support@vizbee.tv
- For integration issues: File an issue in the GitHub repository


## Documentation References

- [Google Cast Receiver Overview](https://developers.google.com/cast/docs/caf_receiver/)
- [Vizbee Chromecast Developer Guide](https://developer.vizbee.tv/continuity/chromecast/integration-guide/initialization)
- [Vizbee Documentation](https://developer.vizbee.tv)

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## Terms of Use

Your use of this application is subject to:
- [Google Cast SDK Additional Developer Terms of Service](https://developers.google.com/cast/docs/terms/)
- Vizbee Terms of Service
- Any additional terms specified in the LICENSE file