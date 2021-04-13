---
title: Messaggio WM_DWMWINDOWMAXIMIZEDCHANGE (winuser. h)
description: Inviato quando una finestra composta da Gestione finestre desktop (DWM) viene ingrandita.
ms.assetid: db8cd104-388e-4211-9e4e-f169aef9651c
keywords:
- Messaggio WM_DWMWINDOWMAXIMIZEDCHANGE Gestione finestre desktop
topic_type:
- apiref
api_name:
- WM_DWMWINDOWMAXIMIZEDCHANGE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2dc49af267ea826eb9e35a627e14f6fc8b381df0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104400661"
---
# <a name="wm_dwmwindowmaximizedchange-message"></a>\_Messaggio DWMWINDOWMAXIMIZEDCHANGE WM

Inviato quando una finestra composta da Gestione finestre desktop (DWM) viene ingrandita.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Impostare su true per specificare che la finestra è stata ingrandita.

</dd> <dt>

*lParam* 
</dt> <dd>

Non usato.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se un'applicazione elabora il messaggio, deve restituire zero.

## <a name="remarks"></a>Commenti

Una finestra riceve questo messaggio tramite la funzione [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                       |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/>                                 |
| Intestazione<br/>                   | <dl> <dt>Winuser. h</dt> </dl> |



 

