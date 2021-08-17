---
title: WM_DWMCOMPOSITIONCHANGED messaggio (Winuser.h)
description: Informa tutte le finestre di primo livello che Gestione finestre desktop (DWM) è stata abilitata o disabilitata.
ms.assetid: VS|winui|~\winui\windowsuserinterface\windowing\windows\windowreference\windowmessages\wm_dwmcompositionchanged.htm
keywords:
- WM_DWMCOMPOSITIONCHANGED messaggio Gestione finestre desktop
topic_type:
- apiref
api_name:
- WM_DWMCOMPOSITIONCHANGED
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9973c69e114882041fc300ca6dee9c96efe121ee7bbf10875ed58ed3c269772c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119118795"
---
# <a name="wm_dwmcompositionchanged-message"></a>Messaggio \_ WM DWMCOMPOSITIONCHANGED

Informa tutte le finestre di primo livello che Gestione finestre desktop (DWM) è stata abilitata o disabilitata.

> [!Note]  
> Al Windows 8, la composizione DWM è sempre abilitata, quindi questo messaggio non viene inviato indipendentemente dalle modifiche della modalità video.

 

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Non usato.

</dd> <dt>

*lParam* 
</dt> <dd>

Non usato.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se un'applicazione elabora questo messaggio, deve restituire zero.

## <a name="remarks"></a>Commenti

Una finestra riceve questo messaggio tramite la [**relativa funzione WindowProc.**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85))

La [**funzione DwmIsCompositionEnabled**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmiscompositionenabled) può essere usata per determinare lo stato di composizione corrente.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>                                       |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2008 \[\]<br/>                                 |
| Intestazione<br/>                   | <dl> <dt>Winuser</dt> </dl> |



 

