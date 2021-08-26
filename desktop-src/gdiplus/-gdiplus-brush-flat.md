---
description: Windows GDI+ espone un'API flat costituita da circa 600 funzioni. Queste funzioni API flat vengono incapsulate dalla classe Brush C++.
ms.assetid: def64d31-9a4b-4365-a618-b87735ce38f1
title: Funzioni Brush (GDI+)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2afdec5667dfcfe4b83e54af3fc0b88fcef991494e36f1e4788062029d1d6e29
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119888341"
---
# <a name="brush-functions-gdi"></a>Funzioni Brush (GDI+)

Windows GDI+ espone un'API flat costituita da circa 600 funzioni, implementate in Gdiplus.dll e dichiarate in Gdiplusflat.h. Le funzioni nell'API GDI+ sono incapsulate da una raccolta di circa 40 classi C++. È consigliabile non chiamare direttamente le funzioni nell'API flat. Ogni volta che si effettuano GDI+, è necessario eseguire questa operazione chiamando i metodi e le funzioni forniti dai wrapper C++. Il Servizio Supporto Tecnico Clienti Microsoft non fornirà supporto per il codice che chiama direttamente l'API flat. Per altre informazioni sull'uso di questi metodi wrapper, [GDI+'API Flat.](-gdiplus-flatapi-flat.md)

Le funzioni API flat seguenti vengono incapsulate dalla [**classe Brush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-brush) C++.

## <a name="brush-functions-and-corresponding-wrapper-methods"></a>Funzioni Brush e metodi wrapper corrispondenti



| Funzione flat                                                                        | Metodo wrapper                                          | Descrizione                                                                                                                                          |
|--------------------------------------------------------------------------------------|---------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------|
| GpStatus WINGDIPAPI GdipCloneBrush(GpBrush \* brush, GpBrush \* \* cloneBrush)          | [**Brush::Clone**](/windows/desktop/api/Gdiplusbrush/nf-gdiplusbrush-brush-clone)     | Il [**metodo Brush::Clone**](/windows/desktop/api/Gdiplusbrush/nf-gdiplusbrush-brush-clone) crea un nuovo [**oggetto Brush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-brush) basato su questo pennello. |
| GpStatus WINGDIPAPI GdipDeleteBrush(Pennello \* GpBrush)                                 | virtual ~Brush()                                        | Pulisce le risorse usate da un [**oggetto Brush.**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-brush)                                                                    |
| GpStatus WINGDIPAPI GdipGetBrushType(Pennello \* GpBrush, tipo \* GpBrushType)<br/> | [**Brush::GetType**](/windows/desktop/api/Gdiplusbrush/nf-gdiplusbrush-brush-gettype) | Il [**metodo Brush::GetType**](/windows/desktop/api/Gdiplusbrush/nf-gdiplusbrush-brush-gettype) ottiene il tipo di questo pennello.                                                      |



 

 

 




