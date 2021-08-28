---
title: WM_DWMWINDOWMAXIMIZEDCHANGE messaggio (Winuser.h)
description: Inviato quando una finestra composta Gestione finestre desktop (DWM) è ingrandita.
ms.assetid: db8cd104-388e-4211-9e4e-f169aef9651c
keywords:
- WM_DWMWINDOWMAXIMIZEDCHANGE messaggio Gestione finestre desktop
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
ms.openlocfilehash: 93cfa4ac380b6ff439fb2bf4805846c0b774a90bcfdcd83673ead2334a3c7094
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120117751"
---
# <a name="wm_dwmwindowmaximizedchange-message"></a>Messaggio WM \_ DWMWINDOWMAXIMIZEDCHANGE

Inviato quando una finestra composta Gestione finestre desktop (DWM) è ingrandita.

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

Se un'applicazione elabora questo messaggio, deve restituire zero.

## <a name="remarks"></a>Commenti

Una finestra riceve questo messaggio tramite la [**relativa funzione WindowProc.**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85))

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>                                       |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2008 \[\]<br/>                                 |
| Intestazione<br/>                   | <dl> <dt>Winuser</dt> </dl> |



 

