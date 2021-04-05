---
title: Messaggio di MCIWNDM_GETEND (VFW. h)
description: Il \_ messaggio MCIWNDM GETEND recupera la posizione della fine del contenuto di un file o di un dispositivo MCI. È possibile inviare questo messaggio in modo esplicito o utilizzando la macro MCIWndGetEnd.
ms.assetid: 3fa45928-af63-4f87-835d-f409011a797e
keywords:
- MCIWNDM_GETEND messaggi multimediali di Windows
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
ms.openlocfilehash: 00d18057619e31fa9b22d7f6354527c394c02798
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103874453"
---
# <a name="mciwndm_getend-message"></a>\_Messaggio MCIWNDM GETEND

Il messaggio **MCIWNDM \_ GETEND** recupera la posizione della fine del contenuto di un file o di un dispositivo MCI. È possibile inviare questo messaggio in modo esplicito o utilizzando la macro [**MCIWndGetEnd**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetend) .


```C++
MCIWNDM_GETEND 
wParam = 0; 
lParam = 0; 
```



## <a name="return-value"></a>Valore restituito

Restituisce la posizione nel formato dell'ora corrente.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                       |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                             |
| Intestazione<br/>                   | <dl> <dt>VFW. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**MCIWndGetEnd**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetend)
</dt> </dl>

 

 





