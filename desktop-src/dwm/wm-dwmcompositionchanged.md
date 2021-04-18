---
title: Messaggio WM_DWMCOMPOSITIONCHANGED (winuser. h)
description: Informa tutte le finestre di primo livello che Gestione finestre desktop la composizione (DWM) è stata abilitata o disabilitata.
ms.assetid: VS|winui|~\winui\windowsuserinterface\windowing\windows\windowreference\windowmessages\wm_dwmcompositionchanged.htm
keywords:
- Messaggio WM_DWMCOMPOSITIONCHANGED Gestione finestre desktop
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
ms.openlocfilehash: 8ec25f740e1a5d002edec2c1faeaaf068190583c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301718"
---
# <a name="wm_dwmcompositionchanged-message"></a>\_Messaggio DWMCOMPOSITIONCHANGED WM

Informa tutte le finestre di primo livello che Gestione finestre desktop la composizione (DWM) è stata abilitata o disabilitata.

> [!Note]  
> A partire da Windows 8, la composizione di DWM è sempre abilitata, quindi questo messaggio non viene inviato indipendentemente dalle modifiche della modalità video.

 

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

Se un'applicazione elabora il messaggio, deve restituire zero.

## <a name="remarks"></a>Commenti

Una finestra riceve questo messaggio tramite la funzione [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .

La funzione [**DwmIsCompositionEnabled**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmiscompositionenabled) può essere utilizzata per determinare lo stato di composizione corrente.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                       |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/>                                 |
| Intestazione<br/>                   | <dl> <dt>Winuser. h</dt> </dl> |



 

