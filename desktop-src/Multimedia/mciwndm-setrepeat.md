---
title: Messaggio di MCIWNDM_SETREPEAT (VFW. h)
description: Il \_ messaggio MCIWNDM di rerepeat imposta il flag di ripetizione associato alla riproduzione continua.
ms.assetid: 9a8da201-9ce8-4b6c-8b76-cd9e1356c75d
keywords:
- MCIWNDM_SETREPEAT messaggi multimediali di Windows
topic_type:
- apiref
api_name:
- MCIWNDM_SETREPEAT
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aeae2ac3cb57f8ddbb2343ee3f42d30fa8def370
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103874141"
---
# <a name="mciwndm_setrepeat-message"></a>MCIWNDM \_ messaggio di ripetizione

Il messaggio **MCIWNDM di \_ rerepeat** imposta il flag di ripetizione associato alla riproduzione continua. Il **messaggio \_ MCIWNDM** viene utilizzato insieme al comando [MCI \_ Play](mci-play.md) per fornire un ciclo di riproduzione continuo. È possibile inviare questo messaggio in modo esplicito o utilizzando la macro [**MCIWndSetRepeat**](/windows/desktop/api/Vfw/nf-vfw-mciwndsetrepeat) .


```C++
MCIWNDM_SETREPEAT 
wParam = 0; 
lParam = (LPARAM) (BOOL) f; 
```



## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="f"></span><span id="F"></span>*f*
</dt> <dd>

Nuovo stato del flag di ripetizione. Specificare **true** per attivare la riproduzione continua.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce zero.

## <a name="remarks"></a>Commenti

Attualmente, MCIAVI è l'unico dispositivo che supporta la riproduzione continua.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                       |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                             |
| Intestazione<br/>                   | <dl> <dt>VFW. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[\_riproduzione MCI](mci-play.md)
</dt> <dt>

[**MCIWndSetRepeat**](/windows/desktop/api/Vfw/nf-vfw-mciwndsetrepeat)
</dt> </dl>

 

 





