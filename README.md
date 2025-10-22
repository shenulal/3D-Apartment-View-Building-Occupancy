# 3D Apartment View - Building Occupancy Visualization

A real estate proof-of-concept (POC) application that provides an interactive 3D visualization of apartment buildings with occupancy tracking. Built with Three.js, this tool allows users to visualize building layouts, track apartment occupancy status, and explore building information in real-time.

## Features

### 3D Visualization
- **Interactive 3D Building Model**: Visualize apartment buildings in a fully interactive 3D environment
- **Real-time Rendering**: Smooth, responsive 3D graphics powered by Three.js
- **Intuitive Controls**: 
  - Click and drag to rotate the building
  - Scroll to zoom in/out
  - Scroll to navigate between floors (when zoomed in)

### Building Configuration
- **Customizable Building Parameters**:
  - Building name and location
  - Owner information
  - Commission date
  - Number of floors (1-20)
  - Apartments per floor (1-20)
- **Dynamic Generation**: Generate new building layouts instantly with custom parameters

### Occupancy Tracking
- **Visual Status Indicators**:
  - **Green**: Occupied apartments
  - **Red**: Vacant apartments
- **Interactive Apartment List**: Click on apartments in the list to toggle occupancy status
- **Real-time Statistics**:
  - Total apartments count
  - Occupied vs. vacant count
  - Occupancy rate percentage

### User Interface
- **Three-Panel Layout**:
  - **Left Panel**: Building configuration controls and apartment list
  - **Center Panel**: 3D visualization canvas
  - **Right Panel**: Building information and statistics display
- **Hover Tooltips**: Hover over apartments to see detailed information (floor, apartment number, occupancy status)
- **Floor Navigation**: Visual indicator showing current floor when navigating
- **Responsive Design**: Adapts to different screen sizes

## Getting Started

### Prerequisites
- A modern web browser with WebGL support (Chrome, Firefox, Safari, Edge)
- No installation or build process required

### Usage

1. **Open the Application**
   - Open `apartment3Dview.html` in your web browser

2. **Configure Building**
   - Enter building details in the left panel:
     - Building name
     - Location
     - Owner name
     - Commission date
     - Number of floors
     - Apartments per floor
   - Click "Generate Building" to create the 3D model

3. **Interact with the Building**
   - **Rotate**: Click and drag with mouse
   - **Zoom**: Scroll mouse wheel
   - **Navigate Floors**: Scroll when zoomed in close to the building
   - **Toggle Occupancy**: Click on apartments in the list or hover and click in the 3D view

4. **View Statistics**
   - Check the right panel for real-time building statistics
   - Monitor occupancy rates and apartment counts

## Technical Stack

- **Three.js**: 3D graphics library for WebGL rendering
- **OrbitControls**: Camera control system for intuitive 3D navigation
- **HTML5/CSS3**: Responsive user interface
- **Vanilla JavaScript**: Core application logic

## File Structure

```
.
├── apartment3Dview.html    # Main application file (HTML + CSS + JavaScript)
├── vercel.json             # Deployment configuration
└── README.md               # This file
```

## Architecture

### Core Components

1. **Scene Management**
   - Three.js scene initialization with lighting and grid
   - Camera setup with perspective projection
   - WebGL renderer with shadow mapping

2. **Building Generation**
   - Dynamic apartment mesh creation
   - Floor slab generation
   - Automatic camera positioning based on building size

3. **Interaction System**
   - Raycaster-based hover detection
   - Mouse event handling for rotation and zoom
   - Scroll wheel navigation for floor traversal

4. **State Management**
   - Apartment occupancy tracking
   - Building configuration storage
   - UI synchronization with 3D model

## Apartment Numbering

Apartments are numbered using a floor-based system:
- **Floor 1**: Apartments 101, 102, 103, ...
- **Floor 2**: Apartments 201, 202, 203, ...
- **Floor N**: Apartments N01, N02, N03, ...

## Browser Compatibility

- Chrome/Chromium: ✅ Full support
- Firefox: ✅ Full support
- Safari: ✅ Full support
- Edge: ✅ Full support
- IE 11: ❌ Not supported (requires WebGL)

## Performance Considerations

- Optimized for buildings up to 20 floors with 20 apartments per floor
- Shadow mapping enabled for realistic lighting
- Damping applied to camera controls for smooth interaction
- Periodic scroll navigation state checks to minimize performance impact

## Future Enhancements

- Export building data to JSON/CSV
- Import building configurations
- Advanced filtering and search
- Unit pricing and financial metrics
- Tenant information integration
- Lease tracking
- Maintenance scheduling

## License

This project is provided as-is for demonstration and development purposes.

## Support

For issues or questions, please refer to the repository or contact the development team.

