---
title: Messaggio WM_DWMNCRENDERINGCHANGED (winuser. h)
description: Inviato quando i criteri di rendering dell'area non client vengono modificati.
ms.assetid: 31beb127-ebec-49a8-8b65-de00941cbd67
keywords:
- Messaggio WM_DWMNCRENDERINGCHANGED Gestione finestre desktop
topic_type:
- apiref
api_name:
- WM_DWMNCRENDERINGCHANGED
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ac32704ea240ccfc4d4de913b940e098ff8f4de4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964302"
---
# <a name="wm_dwmncrenderingchanged-message"></a>\_Messaggio DWMNCRENDERINGCHANGED WM

Inviato quando i criteri di rendering dell'area non client vengono modificati.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Specifica se il rendering di DWM è abilitato per l'area non client della finestra. **True** se abilitata; in caso contrario, **false**.

</dd> <dt>

*lParam* 
</dt> <dd>

Non usato.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se un'applicazione elabora il messaggio, deve restituire zero.

## <a name="remarks"></a>Commenti

Una finestra riceve questo messaggio tramite la funzione [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .

Le funzioni [**DwmGetWindowAttribute**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmgetwindowattribute) e [**DwmSetWindowAttribute**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmsetwindowattribute) vengono usate per ottenere o impostare i criteri di rendering non client.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                       |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/>                                 |
| Intestazione<br/>                   | <dl> <dt>Winuser. h</dt> </dl> |



 

