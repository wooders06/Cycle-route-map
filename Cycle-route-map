import folium

# Create a map centered at London
m = folium.Map(location=[51.5074, -0.1278], zoom_start=6)

# Define key waypoints (approximate lat/lon coordinates)
route_points = [
    [51.5065, -0.0838],  # Hays Galleria
    [50.7920, 0.0540],   # Newhaven Port
    [49.9333, 1.0833],   # Dieppe (France)
    [49.4500, 2.1167],   # Tillé
    [48.8566, 2.3522],   # Paris
]

# Add markers for major waypoints
waypoint_names = ["Hays Galleria", "Newhaven Port", "Dieppe", "Tillé", "Paris"]
for point, name in zip(route_points, waypoint_names):
    folium.Marker(location=point, popup=name, icon=folium.Icon(color="blue")).add_to(m)

# Add a line for the cycle route
folium.PolyLine(route_points, color="green", weight=4, opacity=0.8).add_to(m)

# Save to an HTML file
m.save("cycle_route.html")
