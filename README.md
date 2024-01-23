# Python-Final
https://github.com/iremdincer/Python-Final-/issues/1#issue-2095300212
İlk olarak github üzerinde repo oluşturmak için +>new repository e tıklıyoruz.
https://github.com/iremdincer/Python-Final-/issues/2#issue-2095303261
Aılan ekranki boşıkları doldurup>create respotory 

Daha sonra visual studio code üzerinde qgis programında mekansal görüntüleyebilmek için aşağıda bulunan kodu yazıp çalıştırıyoruz.

import geopandas as gpd
import matplotlib.pyplot as plt


shapefile_path = r'C:\Users\Lenovo\Desktop\gazi yl\pyhton\wor\workshop\secilen_mahalleler.shp'
gdf = gpd.read_file(shapefile_path)


fig, ax = plt.subplots(1, 1, figsize=(10, 10))
gdf.plot(column='NUFUS', ax=ax, legend=True, cmap='OrRd', legend_kwds={'label': "Nüfus Yoğunluğu",'orientation': "horizontal"})
ax.set_title('Mahalle Nüfus Yoğunluğu Haritası')
Sınır çizgilerini belirgenleştirmek içi :
gdf.plot(column='NUFUS', ax=ax, legend=True, cmap='OrRd', legend_kwds={'label': "Nüfus Yoğunluğu",'orientation': "horizontal"}, linewidth=1, edgecolor='black')
plt.show()


