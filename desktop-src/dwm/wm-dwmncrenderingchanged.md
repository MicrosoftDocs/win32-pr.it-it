---
title: WM_DWMNCRENDERINGCHANGED messaggio (Winuser.h)
description: Inviato quando i criteri di rendering dell'area non client vengono modificati.
ms.assetid: 31beb127-ebec-49a8-8b65-de00941cbd67
keywords:
- WM_DWMNCRENDERINGCHANGED messaggio Gestione finestre desktop
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
ms.openlocfilehash: 4bcae8595315d43737d88d6a302bcac3a328418abd19d77b96bd13ee5ef66496
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118502654"
---
# <a name="wm_dwmncrenderingchanged-message"></a>Messaggio \_ WM DWMNCRENDERINGCHANGED

Inviato quando i criteri di rendering dell'area non client vengono modificati.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Specifica se il rendering DWM è abilitato per l'area non client della finestra. **TRUE se** abilitato; in caso contrario, **FALSE.**

</dd> <dt>

*lParam* 
</dt> <dd>

Non usato.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se un'applicazione elabora questo messaggio, deve restituire zero.

## <a name="remarks"></a>Commenti

Una finestra riceve questo messaggio tramite la [**relativa funzione WindowProc.**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85))

Le [**funzioni DwmGetWindowAttribute**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmgetwindowattribute) e [**DwmSetWindowAttribute**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmsetwindowattribute) vengono usate per ottenere o impostare i criteri di rendering non client.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>                                       |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2008 \[\]<br/>                                 |
| Intestazione<br/>                   | <dl> <dt>Winuser</dt> </dl> |



 

