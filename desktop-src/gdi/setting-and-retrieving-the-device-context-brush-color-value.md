---
description: L'esempio seguente illustra come un'applicazione può recuperare il colore corrente del pennello dc usando le funzioni SetDCBrushColor e GetDCBrushColor.
ms.assetid: a1ef6c25-0d00-4175-8679-001ba165bd6d
title: Impostazione e recupero del valore del colore del pennello del contesto di dispositivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5e0bfc918f5882baa46208d27973e14b9446909e
ms.sourcegitcommit: 8f0a1d212dd154e8d94ab4c0e4ced053fa16823a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/11/2021
ms.locfileid: "112010634"
---
# <a name="setting-and-retrieving-the-device-context-brush-color-value"></a>Impostazione e recupero del valore del colore del pennello del contesto di dispositivo

L'esempio seguente illustra come un'applicazione può recuperare il colore corrente del pennello dc usando le [**funzioni SetDCBrushColor**](/windows/desktop/api/Wingdi/nf-wingdi-setdcbrushcolor) e [**GetDCBrushColor.**](/windows/desktop/api/WinGdi/nf-wingdi-getdcbrushcolor)


```C++
SelectObject(hdc,GetStockObject(DC_BRUSH));
SetDCBrushColor(hdc,RGB(00,0xff,00));
PatBlt(hdc,0,0,200,200,PATCOPY);
SetDCBrushColor(hdc,RGB(00,00,0xff));
PatBlt(hdc,0,0,200,200,PATCOPY);
```



 

 



