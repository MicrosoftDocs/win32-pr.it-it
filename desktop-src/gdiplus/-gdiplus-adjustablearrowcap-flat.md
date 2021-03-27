---
description: Windows GDI+ espone un'API Flat costituita da circa 600 funzioni, implementate in Gdiplus.dll e dichiarate in Gdiplusflat. h.
ms.assetid: 809d8b1e-ccdd-4156-b650-1bb7443a59fa
title: Funzioni AdjustableArrowCap
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0d377b319169a2a10c864db5aec402fe633beb3c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104994464"
---
# <a name="adjustablearrowcap-functions"></a>Funzioni AdjustableArrowCap

Windows GDI+ espone un'API Flat costituita da circa 600 funzioni, implementate in Gdiplus.dll e dichiarate in Gdiplusflat. h. Le funzioni nell'API flat di GDI+ sono racchiuse tra una raccolta di circa 40 classi C++. Si consiglia di non chiamare direttamente le funzioni nell'API flat. Quando si effettuano chiamate a GDI+, è necessario chiamare i metodi e le funzioni forniti dai wrapper C++. Il servizio supporto tecnico Microsoft non fornirà il supporto per il codice che chiama direttamente l'API flat. Per altre informazioni sull'uso di questi metodi wrapper, vedere [GDI+ Flat API](-gdiplus-flatapi-flat.md).

Le funzioni API Flat seguenti sono incapsulate dalla classe C++ [**AdjustableArrowCap**](/windows/desktop/api/gdipluslinecaps/nl-gdipluslinecaps-adjustablearrowcap) .

## <a name="adjustablearrowcap-functions-and-corresponding-wrapper-methods"></a>Funzioni AdjustableArrowCap e metodi wrapper corrispondenti



| Flat-funzione                                                                                                          | Wrapper (metodo)                                                                                                                | Descrizione                                                                                                                                                                                                                              |
|------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| GpStatus WINGDIPAPI GdipCreateAdjustableArrowCap (altezza reale, larghezza reale, BOOL riempito, GpAdjustableArrowCap \* \* Cap) | [**AdjustableArrowCap:: AdjustableArrowCap**](/windows/win32/api/gdipluslinecaps/nf-gdipluslinecaps-adjustablearrowcap-adjustablearrowcap(inreal_inreal_inbool)) | Crea un perno della linea a forma di freccia regolabile con l'altezza e la larghezza specificate. Il limite della riga della freccia può essere riempito o non riempito. Per impostazione predefinita, il valore di incasso medio è zero.                                                                              |
| GpStatus WINGDIPAPI GdipSetAdjustableArrowCapHeight (GpAdjustableArrowCap \* Cap, Real Height)                           | [**AdjustableArrowCap:: seheight**](/windows/desktop/api/Gdipluslinecaps/nf-gdipluslinecaps-adjustablearrowcap-setheight)                                  | Il metodo [**AdjustableArrowCap:: seheight**](/windows/desktop/api/Gdipluslinecaps/nf-gdipluslinecaps-adjustablearrowcap-setheight) imposta l'altezza dell'estremità della freccia. Si tratta della distanza tra la base della freccia e il relativo vertice.                                 |
| GpStatus WINGDIPAPI GdipGetAdjustableArrowCapHeight (GpAdjustableArrowCap \* Cap, Real \* Height)                         | [**AdjustableArrowCap:: GetHeight**](/windows/desktop/api/Gdipluslinecaps/nf-gdipluslinecaps-adjustablearrowcap-getheight)                                         | Il metodo [**AdjustableArrowCap:: GetHeight**](/windows/desktop/api/Gdipluslinecaps/nf-gdipluslinecaps-adjustablearrowcap-getheight) Ottiene l'altezza dell'estremità della freccia. L'altezza è la distanza dalla base della freccia al relativo vertice.                                  |
| GpStatus WINGDIPAPI GdipSetAdjustableArrowCapWidth (GpAdjustableArrowCap \* Cap, Real Width)                             | [**AdjustableArrowCap:: sewidth**](/windows/desktop/api/Gdipluslinecaps/nf-gdipluslinecaps-adjustablearrowcap-setwidth)                                     | Il metodo [**AdjustableArrowCap:: sewidth**](/windows/desktop/api/Gdipluslinecaps/nf-gdipluslinecaps-adjustablearrowcap-setwidth) imposta la larghezza dell'estremità della freccia. La larghezza corrisponde alla distanza tra gli endpoint della base della freccia.                          |
| GpStatus WINGDIPAPI GdipGetAdjustableArrowCapWidth (GpAdjustableArrowCap \* Cap, Real \* Width)                           | [**AdjustableArrowCap:: GetWidth**](/windows/desktop/api/Gdipluslinecaps/nf-gdipluslinecaps-adjustablearrowcap-getwidth)                                           | Il metodo [**AdjustableArrowCap:: GetWidth**](/windows/desktop/api/Gdipluslinecaps/nf-gdipluslinecaps-adjustablearrowcap-getwidth) ottiene la larghezza dell'estremità della freccia. La larghezza corrisponde alla distanza tra gli endpoint della base della freccia.                                |
| GpStatus WINGDIPAPI GdipSetAdjustableArrowCapMiddleInset (GpAdjustableArrowCap \* Cap, Real middleInset)                 | [**AdjustableArrowCap:: SetMiddleInset**](/windows/desktop/api/Gdipluslinecaps/nf-gdipluslinecaps-adjustablearrowcap-setmiddleinset)                   | Il metodo [**AdjustableArrowCap:: SetMiddleInset**](/windows/desktop/api/Gdipluslinecaps/nf-gdipluslinecaps-adjustablearrowcap-setmiddleinset) imposta il numero di unità che il punto centrale della base sposta verso il vertice.                                 |
| GpStatus WINGDIPAPI GdipGetAdjustableArrowCapMiddleInset (GpAdjustableArrowCap \* Cap, Real \* middleInset)<br/>    | [**AdjustableArrowCap:: GetMiddleInset**](/windows/desktop/api/Gdipluslinecaps/nf-gdipluslinecaps-adjustablearrowcap-getmiddleinset)                               | Il metodo [**AdjustableArrowCap:: GetMiddleInset**](/windows/desktop/api/Gdipluslinecaps/nf-gdipluslinecaps-adjustablearrowcap-getmiddleinset) ottiene il valore dell'oggetto Insert. L'incasso centrale è il numero di unità che il punto centrale della base sposta verso il vertice. |
| GpStatus WINGDIPAPI GdipSetAdjustableArrowCapFillState (GpAdjustableArrowCap \* Cap, bool fillState)<br/>          | [**AdjustableArrowCap:: SetFillState**](/windows/desktop/api/Gdipluslinecaps/nf-gdipluslinecaps-adjustablearrowcap-setfillstate)                          | Il metodo [**AdjustableArrowCap:: SetFillState**](/windows/desktop/api/Gdipluslinecaps/nf-gdipluslinecaps-adjustablearrowcap-setfillstate) imposta lo stato di riempimento dell'estremità della freccia. Se il perno della freccia non è riempito, viene disegnata solo la struttura.                         |
| GpStatus WINGDIPAPI GdipGetAdjustableArrowCapFillState (GpAdjustableArrowCap \* Cap, bool \* fillState)<br/>        | [**AdjustableArrowCap:: filled**](/windows/desktop/api/Gdipluslinecaps/nf-gdipluslinecaps-adjustablearrowcap-isfilled)                                           | Il metodo [**AdjustableArrowCap:: filled**](/windows/desktop/api/Gdipluslinecaps/nf-gdipluslinecaps-adjustablearrowcap-isfilled) determina se il perno della freccia è pieno.                                                                                               |



 

 

