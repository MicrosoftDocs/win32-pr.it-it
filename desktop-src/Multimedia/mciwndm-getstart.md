---
title: MCIWNDM_GETSTART messaggio (Vfw.h)
description: Il messaggio MCIWNDM GETSTART recupera il percorso dell'inizio del contenuto di un dispositivo \_ o di un file MCI. È possibile inviare questo messaggio in modo esplicito o tramite la macro MCIWndGetStart.
ms.assetid: 2350616c-2aac-4ff6-b074-bb785a97cdfb
keywords:
- MCIWNDM_GETSTART messaggio Windows Multimediali
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
ms.openlocfilehash: e0efb5689009fdd6928afd1d2f232bcb1bbeb2160aecf3d79ddb263ed6f315de
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119429231"
---
# <a name="mciwndm_getstart-message"></a>Messaggio MCIWNDM \_ GETSTART

Il **messaggio MCIWNDM \_ GETSTART** recupera il percorso dell'inizio del contenuto di un dispositivo o di un file MCI. È possibile inviare questo messaggio in modo esplicito o tramite la macro [**MCIWndGetStart.**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetstart)


```C++
MCIWNDM_GETSTART 
wParam = 0; 
lParam = 0; 
```



## <a name="return-value"></a>Valore restituito

Restituisce la posizione nel formato di ora corrente.

## <a name="remarks"></a>Commenti

In genere, il valore restituito è zero. ma alcuni dispositivi usano una posizione iniziale diversa da zero. Se si cerca questa posizione, il dispositivo viene impostato sull'inizio del supporto.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                       |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                             |
| Intestazione<br/>                   | <dl> <dt>Vfw.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**MCIWndGetStart**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetstart)
</dt> </dl>

 

 





