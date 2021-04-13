---
title: Messaggio di MCIWNDM_GETSTART (VFW. h)
description: Il \_ messaggio GETstart MCIWNDM Recupera il percorso dell'inizio del contenuto di un dispositivo o di un file MCI. È possibile inviare questo messaggio in modo esplicito o utilizzando la macro MCIWndGetStart.
ms.assetid: 2350616c-2aac-4ff6-b074-bb785a97cdfb
keywords:
- MCIWNDM_GETSTART messaggi multimediali di Windows
topic_type:
- apiref
api_name:
- MCIWNDM_GETSTART
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 63cbe88df006f1f98854e42259074d82bbd87dc1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104475526"
---
# <a name="mciwndm_getstart-message"></a>\_Messaggio GETstart MCIWNDM

Il **messaggio \_ getstart MCIWNDM** Recupera il percorso dell'inizio del contenuto di un dispositivo o di un file MCI. È possibile inviare questo messaggio in modo esplicito o utilizzando la macro [**MCIWndGetStart**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetstart) .


```C++
MCIWNDM_GETSTART 
wParam = 0; 
lParam = 0; 
```



## <a name="return-value"></a>Valore restituito

Restituisce la posizione nel formato dell'ora corrente.

## <a name="remarks"></a>Commenti

In genere, il valore restituito è zero; Tuttavia, alcuni dispositivi usano una posizione iniziale diversa da zero. La ricerca in questa posizione consente di impostare il dispositivo sull'avvio del supporto.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                       |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                             |
| Intestazione<br/>                   | <dl> <dt>VFW. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**MCIWndGetStart**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetstart)
</dt> </dl>

 

 





