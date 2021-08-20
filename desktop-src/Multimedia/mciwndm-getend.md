---
title: MCIWNDM_GETEND messaggio (Vfw.h)
description: Il messaggio MCIWNDM GETEND recupera il percorso della fine del contenuto di un dispositivo o di \_ un file MCI. È possibile inviare questo messaggio in modo esplicito o tramite la macro MCIWndGetEnd.
ms.assetid: 3fa45928-af63-4f87-835d-f409011a797e
keywords:
- MCIWNDM_GETEND messaggio Windows Multimediali
topic_type:
- apiref
api_name:
- MCIWNDM_GETEND
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 880b1a464d671ca57e1955d4131776a999d1fb6bd8f17ad5d08139abc64a757b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118137732"
---
# <a name="mciwndm_getend-message"></a>Messaggio MCIWNDM \_ GETEND

Il **messaggio MCIWNDM \_ GETEND** recupera il percorso della fine del contenuto di un dispositivo o di un file MCI. È possibile inviare questo messaggio in modo esplicito o tramite la macro [**MCIWndGetEnd.**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetend)


```C++
MCIWNDM_GETEND 
wParam = 0; 
lParam = 0; 
```



## <a name="return-value"></a>Valore restituito

Restituisce la posizione nel formato di ora corrente.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                       |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                             |
| Intestazione<br/>                   | <dl> <dt>Vfw.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**MCIWndGetEnd**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetend)
</dt> </dl>

 

 





