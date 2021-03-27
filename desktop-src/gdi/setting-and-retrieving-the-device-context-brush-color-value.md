---
description: Nell'esempio seguente viene illustrato come un'applicazione può recuperare il colore corrente del pennello del controller di dominio utilizzando le funzioni SetDCBrushColor e GetDCBrushColor.
ms.assetid: a1ef6c25-0d00-4175-8679-001ba165bd6d
title: Impostazione e recupero del valore del colore del pennello del contesto del dispositivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 21c684bfd50fd92959e9b8f7eac5baf96c62fd0b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104994589"
---
# <a name="setting-and-retrieving-the-device-context-brush-color-value"></a>Impostazione e recupero del valore del colore del pennello del contesto del dispositivo

Nell'esempio seguente viene illustrato come un'applicazione può recuperare il colore corrente del pennello del controller di dominio utilizzando le funzioni [**SetDCBrushColor**](/windows/desktop/api/Wingdi/nf-wingdi-setdcbrushcolor) e [**GetDCBrushColor**](/windows/desktop/api/WinGdi/nf-wingdi-getdcbrushcolor) .


```C++
SelectObject(hdc,GetStockObject(DC_BRUSH));
SetDCBrushColor(hdc, RGB(00,0xff;00);
PatBlt(0,0,200,200,PATCOPY)
SetDCBrushColor(hdc,RGB(00,00,0xff);
PatBlt(0,0,200,200,PATCOPY);
```



 

 



