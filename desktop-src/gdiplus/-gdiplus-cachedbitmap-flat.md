---
description: Windows GDI+ espone un'API Flat costituita da circa 600 funzioni, implementate in Gdiplus.dll e dichiarate in Gdiplusflat. h.
ms.assetid: 06718603-e001-49d4-ac5e-decdd98df42b
title: Funzioni CachedBitmap
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5ebb19648e38425561d1a1609c5f71368718ffb5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103755762"
---
# <a name="cachedbitmap-functions"></a>Funzioni CachedBitmap

Windows GDI+ espone un'API Flat costituita da circa 600 funzioni, implementate in Gdiplus.dll e dichiarate in Gdiplusflat. h. Le funzioni nell'API flat di GDI+ sono racchiuse tra una raccolta di circa 40 classi C++. Si consiglia di non chiamare direttamente le funzioni nell'API flat. Quando si effettuano chiamate a GDI+, è necessario chiamare i metodi e le funzioni forniti dai wrapper C++. Il servizio supporto tecnico Microsoft non fornirà il supporto per il codice che chiama direttamente l'API flat. Per altre informazioni sull'uso di questi metodi wrapper, vedere [GDI+ Flat API](-gdiplus-flatapi-flat.md).

Le funzioni API Flat seguenti sono incapsulate dalla classe C++ [**CachedBitmap**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-cachedbitmap) .

## <a name="cachedbitmap-functions-and-corresponding-wrapper-methods"></a>Funzioni CachedBitmap e metodi wrapper corrispondenti



| Flat-funzione                                                                                                             | Wrapper (metodo)                                                                                  | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                                    |
|---------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| GpStatus WINGDIPAPI GdipCreateCachedBitmap (GpBitmap \* bitmap, GpGraphics \* graphics, GpCachedBitmap \* \* cachedBitmap)   | [**CachedBitmap:: CachedBitmap**](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-cachedbitmap-cachedbitmap(constcachedbitmap_)) | Crea un oggetto [**CachedBitmap:: CachedBitmap**](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-cachedbitmap-cachedbitmap(constcachedbitmap_)) in base a un oggetto [**bitmap**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-bitmap) e a un oggetto [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) . La bitmap memorizzata nella cache preleva i dati dei pixel dall'oggetto **bitmap** e li archivia in un formato ottimizzato per il dispositivo di visualizzazione associato all'oggetto **Graphics** . |
| GpStatus WINGDIPAPI GdipDeleteCachedBitmap (GpCachedBitmap \* cachedBitmap)<br/>                                      | ~ CachedBitmap ()                                                                                 | Pulisce le risorse usate da un oggetto [**CachedBitmap**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-cachedbitmap) .                                                                                                                                                                                                                                                                                                                                |
| GpStatus WINGDIPAPI GdipDrawCachedBitmap (GpGraphics \* graphics, GpCachedBitmap \* CACHEDBITMAP, int x, int y)            | [**Grafica::D rawCachedBitmap**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-drawcachedbitmap)          | Il metodo [**Graphics::D rawcachedbitmap**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-drawcachedbitmap) disegna l'immagine archiviata in un oggetto [**CachedBitmap**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-cachedbitmap) .                                                                                                                                                                                                                                |
| UINT WINGDIPAPI GdipEmfToWmfBits (HENHMETAFILE hemf, UINT cbData16, LPBYTE pData16, INT iMapMode, INT eFlags)<br/> | [**Metafile:: EmfToWmfBits**](/windows/desktop/api/gdiplusheaders/nf-gdiplusheaders-metafile-emftowmfbits)                         | Converte un metafile in formato avanzato in un metafile Windows Metafile Format (WMF) e archivia i record convertiti in un buffer specificato.                                                                                                                                                                                                                                                                                       |



 

 

