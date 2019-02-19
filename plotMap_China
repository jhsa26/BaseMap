import matplotlib.pyplot as plt
from mpl_toolkits.basemap import Basemap
type_of_service=["ESRI_Imagery_World_2D",
"ESRI_StreetMap_World_2D",
"NatGeo_World_Map",
"NGS_Topo_US_2D",
"Ocean_Basemap",
"USA_Topo_Maps",
"World_Imagery",
"World_Physical_Map",
"World_Shaded_Relief",
"World_Street_Map",
"World_Terrain_Base",
"World_Topo_Map"]

for typ in type_of_service:
    print(typ)
    fig = plt.figure(1,figsize=(10,10))
    m = Basemap(projection='mill',llcrnrlon=70,
        urcrnrlon=150,llcrnrlat=10,urcrnrlat=60,
        resolution='h',area_thresh=1000,epsg = 4326)
    m.drawcoastlines()
    m.drawstates()
    m.drawcountries()
#     m.drawrivers()
    m.drawparallels(np.arange(0  ,  90,10)   ,linewidth=0.01,labels=[1,0,0,0],fontsize=font["size"])
    m.drawmeridians(np.arange(0.,180,10),   linewidth=0.01,labels=[0,0,0,1],fontsize=font["size"])
    m.arcgisimage(service = typ, xpixels = 2000)
    plt.title(typ)
    plt.savefig(typ, bbox_inches = "tight", dpi = 300)
    plt.pause(0.01)
    
