---
title: MCIWNDM_SETREPEAT messaggio (Vfw.h)
description: Il messaggio MCIWNDM \_ SETREPEAT imposta il flag di ripetizione associato alla riproduzione continua.
ms.assetid: 9a8da201-9ce8-4b6c-8b76-cd9e1356c75d
keywords:
- MCIWNDM_SETREPEAT messaggio Windows Multimediali
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
ms.openlocfilehash: 158e0b52f01431886fd8a70e89efadfdd7335258c0808cdb6780bf06071e3280
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119807591"
---
# <a name="mciwndm_setrepeat-message"></a>Messaggio MCIWNDM \_ SETREPEAT

Il **messaggio MCIWNDM \_ SETREPEAT** imposta il flag di ripetizione associato alla riproduzione continua. Il **messaggio MCIWNDM \_ SETREPEAT** funziona insieme al [comando MCI \_ PLAY](mci-play.md) per fornire un ciclo di riproduzione continuo. È possibile inviare questo messaggio in modo esplicito o tramite la macro [**MCIWndSetRepeat.**](/windows/desktop/api/Vfw/nf-vfw-mciwndsetrepeat)


```C++
MCIWNDM_SETREPEAT 
wParam = 0; 
lParam = (LPARAM) (BOOL) f; 
```



## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="f"></span><span id="F"></span>*F*
</dt> <dd>

Nuovo stato del flag di ripetizione. Specificare **TRUE per** attivare la riproduzione continua.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce zero.

## <a name="remarks"></a>Commenti

Attualmente MCIAVI è l'unico dispositivo che supporta la riproduzione continua.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                       |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                             |
| Intestazione<br/>                   | <dl> <dt>Vfw.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[MCI \_ PLAY](mci-play.md)
</dt> <dt>

[**MCIWndSetRepeat**](/windows/desktop/api/Vfw/nf-vfw-mciwndsetrepeat)
</dt> </dl>

 

 





