---
title: MCIWNDM_GETALIAS messaggio (Vfw.h)
description: Il messaggio MCIWNDM GETALIAS recupera l'alias usato per aprire un \_ dispositivo o un file MCI con la funzione mciSendString. È possibile inviare questo messaggio in modo esplicito o tramite la macro MCIWndGetAlias.
ms.assetid: 37131b89-275c-4ab6-9278-0e08c42471bd
keywords:
- MCIWNDM_GETALIAS messaggio Windows Multimediali
topic_type:
- apiref
api_name:
- MCIWNDM_GETALIAS
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 857ea90205b5204cd7c4af19f27a420684e59543717b2689f178d97cd5a600de
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118137752"
---
# <a name="mciwndm_getalias-message"></a>Messaggio MCIWNDM \_ GETALIAS

Il **messaggio MCIWNDM \_ GETALIAS** recupera l'alias usato per aprire un dispositivo o un file MCI con la [**funzione mciSendString.**](/previous-versions//dd757161(v=vs.85)) È possibile inviare questo messaggio in modo esplicito o tramite la macro [**MCIWndGetAlias.**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetalias)


```C++
MCIWNDM_GETALIAS 
wParam = 0; 
lParam = 0; 
```



## <a name="return-value"></a>Valore restituito

Restituisce l'alias del dispositivo.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                       |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                             |
| Intestazione<br/>                   | <dl> <dt>Vfw.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**mciSendString**](/previous-versions//dd757161(v=vs.85))
</dt> <dt>

[**MCIWndGetAlias**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetalias)
</dt> </dl>

 

