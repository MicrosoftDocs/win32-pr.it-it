---
description: Windows GDI+ espone un'API flat costituita da circa 600 funzioni. Queste funzioni API flat vengono incapsulate dalla classe C++ CachedBitmap.
ms.assetid: 06718603-e001-49d4-ac5e-decdd98df42b
title: Funzioni CachedBitmap
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1835cd668df90a7703a4aebdd60d37d877fe571f376d440080f5668ec3926a26
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119888331"
---
# <a name="cachedbitmap-functions"></a>Funzioni CachedBitmap

Windows GDI+ espone un'API flat costituita da circa 600 funzioni, implementate in Gdiplus.dll e dichiarate in Gdiplusflat.h. Le funzioni nell'API GDI+ sono incapsulate da una raccolta di circa 40 classi C++. È consigliabile non chiamare direttamente le funzioni nell'API flat. Ogni volta che si effettuano GDI+, è necessario eseguire questa operazione chiamando i metodi e le funzioni forniti dai wrapper C++. Il Servizio Supporto Tecnico Clienti Microsoft non fornirà supporto per il codice che chiama direttamente l'API flat. Per altre informazioni sull'uso di questi metodi wrapper, [GDI+'API Flat.](-gdiplus-flatapi-flat.md)

Le funzioni API flat seguenti vengono incapsulate dalla [**classe C++ CachedBitmap.**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-cachedbitmap)

## <a name="cachedbitmap-functions-and-corresponding-wrapper-methods"></a>Funzioni CachedBitmap e metodi wrapper corrispondenti



| Funzione flat                                                                                                             | Metodo wrapper                                                                                  | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                                    |
|---------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| GpStatus WINGDIPAPI GdipCreateCachedBitmap( GpBitmap \* bitmap, grafica GpGraphics, \* GpCachedBitmap \* \* cachedBitmap )   | [**CachedBitmap::CachedBitmap**](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-cachedbitmap-cachedbitmap(constcachedbitmap_)) | Crea un [**oggetto CachedBitmap::CachedBitmap**](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-cachedbitmap-cachedbitmap(constcachedbitmap_)) basato su un [**oggetto Bitmap**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-bitmap) e un [**oggetto Graphics.**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) La bitmap memorizzata nella cache accetta i dati pixel dall'oggetto **Bitmap** e li archivia in un formato ottimizzato per il dispositivo di visualizzazione associato **all'oggetto** Graphics. |
| GpStatus WINGDIPAPI GdipDeleteCachedBitmap(GpCachedBitmap \* cachedBitmap)<br/>                                      | ~CachedBitmap()                                                                                 | Pulisce le risorse usate da un [**oggetto CachedBitmap.**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-cachedbitmap)                                                                                                                                                                                                                                                                                                                                |
| GpStatus WINGDIPAPI GdipDrawCachedBitmap( grafica GpGraphics, \* GpCachedBitmap \* cachedBitmap, INT x, INT y )            | [**Graphics::D rawCachedBitmap**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-drawcachedbitmap)          | Il [**metodo Graphics::D rawCachedBitmap**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-drawcachedbitmap) disegna l'immagine archiviata in un [**oggetto CachedBitmap.**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-cachedbitmap)                                                                                                                                                                                                                                |
| UINT WINGDIPAPI GdipEmfToWmfBits( HENHMETAFILE hemf, UINT cbData16, LPBYTE pData16, INT iMapMode, INT eFlags )<br/> | [**Metafile::EmfToWmfBits**](/windows/desktop/api/gdiplusheaders/nf-gdiplusheaders-metafile-emftowmfbits)                         | Converte un metafile in formato avanzato in un metafile WMF (Windows Metafile Format) e archivia i record convertiti in un buffer specificato.                                                                                                                                                                                                                                                                                       |



 

 

