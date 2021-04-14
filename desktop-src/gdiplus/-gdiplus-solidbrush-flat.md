---
description: Windows GDI+ espone un'API Flat costituita da circa 600 funzioni, implementate in Gdiplus.dll e dichiarate in Gdiplusflat. h.
ms.assetid: b427b8ab-66fd-4f57-b08e-5f337a9ac9af
title: Funzioni SolidBrush
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bc7d75e99f46877ce990a985e47bc4b9021faaa2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104977546"
---
# <a name="solidbrush-functions"></a>Funzioni SolidBrush

Windows GDI+ espone un'API Flat costituita da circa 600 funzioni, implementate in Gdiplus.dll e dichiarate in Gdiplusflat. h. Le funzioni nell'API flat di GDI+ sono racchiuse tra una raccolta di circa 40 classi C++. Si consiglia di non chiamare direttamente le funzioni nell'API flat. Quando si effettuano chiamate a GDI+, è consigliabile chiamare i metodi e le funzioni forniti dai wrapper C++. Il servizio supporto tecnico Microsoft non fornirà il supporto per il codice che chiama direttamente l'API flat. Per altre informazioni sull'uso di questi metodi wrapper, vedere [GDI+ Flat API](-gdiplus-flatapi-flat.md).

Le funzioni API Flat seguenti sono incapsulate dalla classe C++ [**SolidBrush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-solidbrush) .

## <a name="brush-functions-and-corresponding-wrapper-methods"></a>Funzioni pennello e metodi wrapper corrispondenti



| Flat-funzione                                                                               | Wrapper (metodo)                                                                                       | Commenti                                                                                 |
|---------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------|
| **GpStatus WINGDIPAPI GdipCreateSolidFill (ARGB color, GpSolidFill \* \* Brush)**<br/>   | [**SolidBrush:: SolidBrush (IN colori const& colore)**](/windows/win32/api/gdiplusbrush/nf-gdiplusbrush-solidbrush-solidbrush(constsolidbrush_)) | Crea un oggetto [**SolidBrush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-solidbrush) in base a un colore |
| **GpStatus WINGDIPAPI GdipSetSolidFillColor ( \* pennello GpSolidFill, colore ARGB)**<br/>   | [**SolidBrush:: ToColor (IN colori const& colore)**](/windows/desktop/api/Gdiplusbrush/nf-gdiplusbrush-solidbrush-setcolor)     | Imposta il colore del pennello a tinta unita                                                      |
| **GpStatus WINGDIPAPI GdipGetSolidFillColor ( \* pennello GpSolidFill, \* colore ARGB)**<br/> | [**SolidBrush:: GetColor (colore del colore OUT \* ) const**](/windows/desktop/api/Gdiplusbrush/nf-gdiplusbrush-solidbrush-getcolor)   | Ottiene il colore di questo pennello a tinta unita                                                      |



 

 

 
