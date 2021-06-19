---
description: Windows GDI+ espone un'API flat costituita da circa 600 funzioni. Queste funzioni API flat vengono incapsulate dalla classe Brush C++.
ms.assetid: def64d31-9a4b-4365-a618-b87735ce38f1
title: Funzioni Brush (GDI+)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ffe23588c44d8a3a6412cd0c2bc1327b98bbbd95
ms.sourcegitcommit: 91530c19d26ba4c57a6af1f37b57f211f580464e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/19/2021
ms.locfileid: "112395086"
---
# <a name="brush-functions-gdi"></a>Funzioni Brush (GDI+)

Windows GDI+ espone un'API flat costituita da circa 600 funzioni, implementate in Gdiplus.dll e dichiarate in Gdiplusflat.h. Le funzioni nell'API flat GDI+ vengono incapsulate da una raccolta di circa 40 classi C++. È consigliabile non chiamare direttamente le funzioni nell'API flat. Ogni volta che si effettuano chiamate a GDI+, è necessario eseguire questa operazione chiamando i metodi e le funzioni forniti dai wrapper C++. Il Servizio Supporto Tecnico Clienti Microsoft non fornirà supporto per il codice che chiama direttamente l'API flat. Per altre informazioni sull'uso di questi metodi wrapper, vedere [GDI+ Flat API (API flat GDI+).](-gdiplus-flatapi-flat.md)

Le funzioni API flat seguenti vengono incapsulate dalla [**classe Brush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-brush) C++.

## <a name="brush-functions-and-corresponding-wrapper-methods"></a>Funzioni Brush e metodi wrapper corrispondenti



| Funzione flat                                                                        | Metodo wrapper                                          | Descrizione                                                                                                                                          |
|--------------------------------------------------------------------------------------|---------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------|
| GpStatus WINGDIPAPI GdipCloneBrush(GpBrush \* brush, GpBrush \* \* cloneBrush)          | [**Brush::Clone**](/windows/desktop/api/Gdiplusbrush/nf-gdiplusbrush-brush-clone)     | Il [**metodo Brush::Clone**](/windows/desktop/api/Gdiplusbrush/nf-gdiplusbrush-brush-clone) crea un nuovo [**oggetto Brush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-brush) basato su questo pennello. |
| GpStatus WINGDIPAPI GdipDeleteBrush(Pennello \* GpBrush)                                 | virtual ~Brush()                                        | Pulisce le risorse usate da un [**oggetto Brush.**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-brush)                                                                    |
| GpStatus WINGDIPAPI GdipGetBrushType(Pennello \* GpBrush, tipo \* GpBrushType)<br/> | [**Brush::GetType**](/windows/desktop/api/Gdiplusbrush/nf-gdiplusbrush-brush-gettype) | Il [**metodo Brush::GetType**](/windows/desktop/api/Gdiplusbrush/nf-gdiplusbrush-brush-gettype) ottiene il tipo di questo pennello.                                                      |



 

 

 




