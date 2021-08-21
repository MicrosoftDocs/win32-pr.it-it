---
title: WM_CAP_SET_OVERLAY messaggio (Vfw.h)
description: Il messaggio WM \_ CAP SET OVERLAY abilita o disabilita la modalità di \_ \_ sovrapposizione. In modalità di sovrapposizione, il video viene visualizzato usando la sovrimpressione hardware. È possibile inviare questo messaggio in modo esplicito o usando la macro capOverlay.
ms.assetid: b74c0619-2b70-46e0-9acd-43d658529233
keywords:
- WM_CAP_SET_OVERLAY messaggio Windows Multimediali
topic_type:
- apiref
api_name:
- WM_CAP_SET_OVERLAY
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 10f2161f3c163fb5f6c411293770a2b2ba3907bef7eb03aad2d67b0e0637abbf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118135093"
---
# <a name="wm_cap_set_overlay-message"></a>Messaggio OVERLAY \_ WM CAP \_ SET \_

Il **messaggio WM CAP SET \_ \_ \_ OVERLAY** abilita o disabilita la modalità di sovrapposizione. In modalità di sovrapposizione, il video viene visualizzato usando la sovrimpressione hardware. È possibile inviare questo messaggio in modo esplicito o usando la macro [**capOverlay.**](/windows/desktop/api/Vfw/nf-vfw-capoverlay)


```C++
WM_CAP_SET_OVERLAY 
wParam = (WPARAM) (BOOL) (f); 
lParam = 0L; 
```



## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="f"></span><span id="F"></span>*F*
</dt> <dd>

Flag di sovrapposizione. Specificare **TRUE per** questo parametro per abilitare la modalità di sovrapposizione o **FALSE** per disabilitarlo.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce **TRUE se** l'operazione ha esito positivo o FALSE **in** caso contrario.

## <a name="remarks"></a>Commenti

L'uso di una sovrimpressione non richiede risorse della CPU.

Il **membro fHasOverlay** della [**struttura CAPDRIVERCAPS**](/windows/win32/api/vfw/ns-vfw-capdrivercaps) indica se il dispositivo è in grado di eseguire la sovrapposizione. Il **membro fOverlayWindow** della [**struttura CAPSTATUS**](/windows/win32/api/vfw/ns-vfw-capstatus) indica se la modalità di sovrapposizione è attualmente abilitata.

L'abilitazione della modalità di sovrapposizione disabilita automaticamente la modalità di anteprima.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                       |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                             |
| Intestazione<br/>                   | <dl> <dt>Vfw.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Acquisizione video](video-capture.md)
</dt> <dt>

[Messaggi di acquisizione video](video-capture-messages.md)
</dt> </dl>

 

 





