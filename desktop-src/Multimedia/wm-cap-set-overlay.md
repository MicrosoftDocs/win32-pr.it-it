---
title: Messaggio di WM_CAP_SET_OVERLAY (VFW. h)
description: Il \_ messaggio overlay del set di estremità WM \_ \_ Abilita o Disabilita la modalità overlay. In modalità sovrapposizione, il video viene visualizzato con la sovrimpressione hardware. È possibile inviare questo messaggio in modo esplicito o utilizzando la macro capOverlay.
ms.assetid: b74c0619-2b70-46e0-9acd-43d658529233
keywords:
- WM_CAP_SET_OVERLAY messaggi multimediali di Windows
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
ms.openlocfilehash: f197ae3a7df9ad1520b84cf27fd15a1c76524ab1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106302582"
---
# <a name="wm_cap_set_overlay-message"></a>\_ \_ \_ Messaggio sovrimpressione set Cap WM

Il **messaggio \_ \_ \_ overlay del set di estremità WM** Abilita o Disabilita la modalità overlay. In modalità sovrapposizione, il video viene visualizzato con la sovrimpressione hardware. È possibile inviare questo messaggio in modo esplicito o utilizzando la macro [**capOverlay**](/windows/desktop/api/Vfw/nf-vfw-capoverlay) .


```C++
WM_CAP_SET_OVERLAY 
wParam = (WPARAM) (BOOL) (f); 
lParam = 0L; 
```



## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="f"></span><span id="F"></span>*f*
</dt> <dd>

Flag di sovrimpressione. Specificare **true** per questo parametro per abilitare la modalità overlay o **false** per disabilitarlo.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce **true** se l'operazione è riuscita o **false** in caso contrario.

## <a name="remarks"></a>Commenti

L'uso di una sovrapposizione non richiede risorse della CPU.

Il membro **fHasOverlay** della struttura [**CAPDRIVERCAPS**](/windows/win32/api/vfw/ns-vfw-capdrivercaps) indica se il dispositivo è in grado di sovrapporsi. Il membro **fOverlayWindow** della struttura [**CAPSTATUS**](/windows/win32/api/vfw/ns-vfw-capstatus) indica se la modalità overlay è attualmente abilitata.

L'abilitazione della modalità sovrapposizione Disabilita automaticamente la modalità di anteprima.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                       |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                             |
| Intestazione<br/>                   | <dl> <dt>VFW. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Acquisizione video](video-capture.md)
</dt> <dt>

[Messaggi di acquisizione video](video-capture-messages.md)
</dt> </dl>

 

 





