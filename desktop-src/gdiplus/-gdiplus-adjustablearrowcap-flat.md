---
description: Windows GDI+ espone un'API flat costituita da circa 600 funzioni. Queste funzioni API flat vengono incapsulate dalla classe C++ AdjustableArrowCap.
ms.assetid: 809d8b1e-ccdd-4156-b650-1bb7443a59fa
title: Funzioni AdjustableArrowCap
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 91dd9ee90ea50c4b487ceb90e1b30f1329151533
ms.sourcegitcommit: 91530c19d26ba4c57a6af1f37b57f211f580464e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/19/2021
ms.locfileid: "112395076"
---
# <a name="adjustablearrowcap-functions"></a>Funzioni AdjustableArrowCap

Windows GDI+ espone un'API flat costituita da circa 600 funzioni, implementate in Gdiplus.dll e dichiarate in Gdiplusflat.h. Le funzioni nell'API flat GDI+ vengono incapsulate da una raccolta di circa 40 classi C++. È consigliabile non chiamare direttamente le funzioni nell'API flat. Ogni volta che si effettuano chiamate a GDI+, è necessario chiamare i metodi e le funzioni forniti dai wrapper C++. Il Servizio Supporto Tecnico Clienti Microsoft non fornirà il supporto per il codice che chiama direttamente l'API flat. Per altre informazioni sull'uso di questi metodi wrapper, vedere [API flat GDI+.](-gdiplus-flatapi-flat.md)

Le funzioni API flat seguenti vengono incapsulate dalla [**classe C++ AdjustableArrowCap.**](/windows/desktop/api/gdipluslinecaps/nl-gdipluslinecaps-adjustablearrowcap)

## <a name="adjustablearrowcap-functions-and-corresponding-wrapper-methods"></a>Funzioni AdjustableArrowCap e metodi wrapper corrispondenti



| Funzione flat                                                                                                          | Metodo wrapper                                                                                                                | Descrizione                                                                                                                                                                                                                              |
|------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| GpStatus WINGDIPAPI GdipCreateAdjustableArrowCap(REAL height, REAL width, BOOL isFilled, GpAdjustableArrowCap \* \* cap) | [**AdjustableArrowCap::AdjustableArrowCap**](/windows/win32/api/gdipluslinecaps/nf-gdipluslinecaps-adjustablearrowcap-adjustablearrowcap(inreal_inreal_inbool)) | Crea un estremità della linea di freccia regolabile con l'altezza e la larghezza specificate. L'estremità della linea di freccia può essere riempita o non riempita. Il valore predefinito dell'inset intermedio è zero.                                                                              |
| GpStatus WINGDIPAPI GdipSetAdjustableArrowCapHeight(GpAdjustableArrowCap \* cap, REAL height)                           | [**AdjustableArrowCap::SetHeight**](/windows/desktop/api/Gdipluslinecaps/nf-gdipluslinecaps-adjustablearrowcap-setheight)                                  | Il [**metodo AdjustableArrowCap::SetHeight**](/windows/desktop/api/Gdipluslinecaps/nf-gdipluslinecaps-adjustablearrowcap-setheight) imposta l'altezza della estremità della freccia. Si tratta della distanza dalla base della freccia al vertice.                                 |
| GpStatus WINGDIPAPI GdipGetAdjustableArrowCapHeight(GpAdjustableArrowCap \* cap, REAL \* height)                         | [**AdjustableArrowCap::GetHeight**](/windows/desktop/api/Gdipluslinecaps/nf-gdipluslinecaps-adjustablearrowcap-getheight)                                         | Il [**metodo AdjustableArrowCap::GetHeight**](/windows/desktop/api/Gdipluslinecaps/nf-gdipluslinecaps-adjustablearrowcap-getheight) ottiene l'altezza del tappo della freccia. L'altezza è la distanza dalla base della freccia al vertice.                                  |
| GpStatus WINGDIPAPI GdipSetAdjustableArrowCapWidth(GpAdjustableArrowCap \* cap, REAL width)                             | [**AdjustableArrowCap::SetWidth**](/windows/desktop/api/Gdipluslinecaps/nf-gdipluslinecaps-adjustablearrowcap-setwidth)                                     | Il [**metodo AdjustableArrowCap::SetWidth**](/windows/desktop/api/Gdipluslinecaps/nf-gdipluslinecaps-adjustablearrowcap-setwidth) imposta la larghezza dell'estremità della freccia. La larghezza è la distanza tra i punti finali della base della freccia.                          |
| GpStatus WINGDIPAPI GdipGetAdjustableArrowCapWidth(GpAdjustableArrowCap \* cap, REAL \* width)                           | [**AdjustableArrowCap::GetWidth**](/windows/desktop/api/Gdipluslinecaps/nf-gdipluslinecaps-adjustablearrowcap-getwidth)                                           | Il [**metodo AdjustableArrowCap::GetWidth**](/windows/desktop/api/Gdipluslinecaps/nf-gdipluslinecaps-adjustablearrowcap-getwidth) ottiene la larghezza dell'estremità della freccia. La larghezza è la distanza tra i punti finali della base della freccia.                                |
| GpStatus WINGDIPAPI GdipSetAdjustableArrowCapMiddleInset(GpAdjustableArrowCap \* cap, REAL middleInset)                 | [**AdjustableArrowCap::SetMiddleInset**](/windows/desktop/api/Gdipluslinecaps/nf-gdipluslinecaps-adjustablearrowcap-setmiddleinset)                   | Il [**metodo AdjustableArrowCap::SetMiddleInset**](/windows/desktop/api/Gdipluslinecaps/nf-gdipluslinecaps-adjustablearrowcap-setmiddleinset) imposta il numero di unità di spostamento del punto medio della base verso il vertice.                                 |
| GpStatus WINGDIPAPI GdipGetAdjustableArrowCapMiddleInset(GpAdjustableArrowCap \* cap, REAL \* middleInset)<br/>    | [**AdjustableArrowCap::GetMiddleInset**](/windows/desktop/api/Gdipluslinecaps/nf-gdipluslinecaps-adjustablearrowcap-getmiddleinset)                               | Il [**metodo AdjustableArrowCap::GetMiddleInset**](/windows/desktop/api/Gdipluslinecaps/nf-gdipluslinecaps-adjustablearrowcap-getmiddleinset) ottiene il valore dell'oggetto inset. L'inset intermedio è il numero di unità che il punto intermedio della base sposta verso il vertice. |
| GpStatus WINGDIPAPI GdipSetAdjustableArrowCapFillState(GpAdjustableArrowCap \* cap, BOOL fillState)<br/>          | [**AdjustableArrowCap::SetFillState**](/windows/desktop/api/Gdipluslinecaps/nf-gdipluslinecaps-adjustablearrowcap-setfillstate)                          | Il [**metodo AdjustableArrowCap::SetFillState**](/windows/desktop/api/Gdipluslinecaps/nf-gdipluslinecaps-adjustablearrowcap-setfillstate) imposta lo stato di riempimento del tappo della freccia. Se il bordo della freccia non è pieno, viene disegnato solo il contorno.                         |
| GpStatus WINGDIPAPI GdipGetAdjustableArrowCapFillState(GpAdjustableArrowCap \* cap, BOOL \* fillState)<br/>        | [**AdjustableArrowCap::IsFilled**](/windows/desktop/api/Gdipluslinecaps/nf-gdipluslinecaps-adjustablearrowcap-isfilled)                                           | Il [**metodo AdjustableArrowCap::IsFilled**](/windows/desktop/api/Gdipluslinecaps/nf-gdipluslinecaps-adjustablearrowcap-isfilled) determina se il tappo della freccia è riempito.                                                                                               |



 

 

