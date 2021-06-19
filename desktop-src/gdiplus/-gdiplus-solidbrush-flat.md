---
description: Windows GDI+ espone un'API flat costituita da circa 600 funzioni. Queste funzioni API flat vengono incapsulate dalla classe SolidBrush C++.
ms.assetid: b427b8ab-66fd-4f57-b08e-5f337a9ac9af
title: Funzioni SolidBrush
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dc9feb2676c60b3f504315f75303aadb16a1cd1f
ms.sourcegitcommit: 91530c19d26ba4c57a6af1f37b57f211f580464e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/19/2021
ms.locfileid: "112395556"
---
# <a name="solidbrush-functions"></a>Funzioni SolidBrush

Windows GDI+ espone un'API flat costituita da circa 600 funzioni, implementate in Gdiplus.dll e dichiarate in Gdiplusflat.h. Le funzioni nell'API flat GDI+ vengono incapsulate da una raccolta di circa 40 classi C++. È consigliabile non chiamare direttamente le funzioni nell'API flat. Ogni volta che si effettuano chiamate a GDI+, è consigliabile eseguire questa operazione chiamando i metodi e le funzioni forniti dai wrapper C++. Il Servizio Supporto Tecnico Clienti Microsoft non fornirà supporto per il codice che chiama direttamente l'API flat. Per altre informazioni sull'uso di questi metodi wrapper, vedere [GDI+ Flat API (API flat GDI+).](-gdiplus-flatapi-flat.md)

Le funzioni API flat seguenti vengono incapsulate dalla [**classe SolidBrush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-solidbrush) C++.

## <a name="brush-functions-and-corresponding-wrapper-methods"></a>Funzioni Brush e metodi wrapper corrispondenti



| Funzione flat                                                                               | Metodo wrapper                                                                                       | Commenti                                                                                 |
|---------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------|
| **GpStatus WINGDIPAPI GdipCreateSolidFill(ARGB color, GpSolidFill \* \* brush)**<br/>   | [**SolidBrush::SolidBrush(IN const Color& color)**](/windows/win32/api/gdiplusbrush/nf-gdiplusbrush-solidbrush-solidbrush(constsolidbrush_)) | Crea un [**oggetto SolidBrush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-solidbrush) basato su un colore |
| **GpStatus WINGDIPAPI GdipSetSolidFillColor(GpSolidFill \* brush, ARGB color)**<br/>   | [**SolidBrush::SetColor(IN const Color& colore)**](/windows/desktop/api/Gdiplusbrush/nf-gdiplusbrush-solidbrush-setcolor)     | Imposta il colore di questo pennello a tinta unita                                                      |
| **GpStatus WINGDIPAPI GdipGetSolidFillColor(GpSolidFill \* brush, ARGB \* color)**<br/> | [**SolidBrush::GetColor(OUT Color \* color) const**](/windows/desktop/api/Gdiplusbrush/nf-gdiplusbrush-solidbrush-getcolor)   | Ottiene il colore di questo pennello a tinta unita                                                      |



 

 

 
