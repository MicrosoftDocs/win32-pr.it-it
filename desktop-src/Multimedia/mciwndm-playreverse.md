---
title: Messaggio di MCIWNDM_PLAYREVERSE (VFW. h)
description: Il \_ messaggio MCIWNDM PLAYREVERSE riproduce il contenuto corrente nella direzione inversa, a partire dalla posizione corrente fino all'inizio del contenuto o fino a quando un altro comando interrompe la riproduzione.
ms.assetid: 93a22454-eca6-453f-abbe-6cf20198dbad
keywords:
- MCIWNDM_PLAYREVERSE messaggi multimediali di Windows
topic_type:
- apiref
api_name:
- MCIWNDM_PLAYREVERSE
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 84b0a2e230e3c57e8314e455be5dfbc5cea2c013
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104118946"
---
# <a name="mciwndm_playreverse-message"></a>\_Messaggio MCIWNDM PLAYREVERSE

Il messaggio **MCIWNDM \_ PLAYREVERSE** riproduce il contenuto corrente nella direzione inversa, a partire dalla posizione corrente fino all'inizio del contenuto o fino a quando un altro comando interrompe la riproduzione. È possibile inviare questo messaggio in modo esplicito o utilizzando la macro [**MCIWndPlayReverse**](/windows/desktop/api/Vfw/nf-vfw-mciwndplayreverse) .


```C++
MCIWNDM_PLAYREVERSE 
wParam = 0; 
lParam = 0; 
```



## <a name="return-value"></a>Valore restituito

Restituisce zero in caso di esito positivo o un errore.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                       |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                             |
| Intestazione<br/>                   | <dl> <dt>VFW. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**MCIWndPlayReverse**](/windows/desktop/api/Vfw/nf-vfw-mciwndplayreverse)
</dt> </dl>

 

 





