---
title: MCIWNDM_SETPALETTE messaggio (Vfw.h)
description: Il messaggio MCIWNDM SETPALETTE invia un handle del riquadro al dispositivo \_ MCI associato alla finestra MCIWnd. È possibile inviare questo messaggio in modo esplicito o tramite la macro MCIWndSetPalette.
ms.assetid: d2399cb7-d83c-465c-b02f-e6a016c28ae3
keywords:
- MCIWNDM_SETPALETTE messaggio Windows Multimediali
topic_type:
- apiref
api_name:
- MCIWNDM_SETPALETTE
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7b4986224fd23898ef33f8fdda4c12d17880a8bc42441b29cd1865fb7fdfa687
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119525231"
---
# <a name="mciwndm_setpalette-message"></a>Messaggio MCIWNDM \_ SETPALETTE

Il **messaggio MCIWNDM \_ SETPALETTE** invia un handle del riquadro al dispositivo MCI associato alla finestra MCIWnd. È possibile inviare questo messaggio in modo esplicito o tramite la macro [**MCIWndSetPalette.**](/windows/desktop/api/Vfw/nf-vfw-mciwndsetpalette)


```C++
MCIWNDM_SETPALETTE 
wParam = (WPARAM) (HPALETTE) hpal; 
lParam = 0; 
```



## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="hpal"></span><span id="HPAL"></span>*hpal*
</dt> <dd>

Handle del riquadro.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce zero in caso di esito positivo o un errore in caso contrario.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                       |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                             |
| Intestazione<br/>                   | <dl> <dt>Vfw.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**MCIWndSetPalette**](/windows/desktop/api/Vfw/nf-vfw-mciwndsetpalette)
</dt> </dl>

 

 





