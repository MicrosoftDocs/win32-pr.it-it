---
title: Messaggio TTM_TRACKPOSITION (COMmctrl. h)
description: Imposta la posizione di una descrizione comando di rilevamento.
ms.assetid: 9eb7c86c-78e6-442a-ad77-5fb919cab591
keywords:
- Controlli di Windows Message TTM_TRACKPOSITION
topic_type:
- apiref
api_name:
- TTM_TRACKPOSITION
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dd6eab8184049d8bf876a7e782b9adc2091d5fac
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104048515"
---
# <a name="ttm_trackposition-message"></a>\_Messaggio TTM TRACKPOSITION

Imposta la posizione di una descrizione comando di rilevamento.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Deve essere zero.

</dd> <dt>

*lParam* 
</dt> <dd>

[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) specifica la coordinata x del punto in corrispondenza del quale verrà visualizzata la descrizione comando di rilevamento, espressa in coordinate dello schermo. [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) specifica la coordinata y del punto in corrispondenza del quale verrà visualizzata la descrizione comando di rilevamento, espressa in coordinate dello schermo.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il valore restituito per questo messaggio non viene utilizzato.

## <a name="remarks"></a>Commenti

Il controllo ToolTip sceglie la posizione in cui visualizzare la finestra della descrizione comando in base alle coordinate fornite con il messaggio. In questo modo la finestra della descrizione comando viene visualizzata accanto allo strumento a cui corrisponde. Per visualizzare le finestre della descrizione comando in coordinate specifiche, includere il \_ flag assoluto ttf nel membro **uFlags** della struttura [**TOOLINFO**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) quando si aggiunge lo strumento.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

**Riferimento**
</dt> <dt>

[**\_TRACKACTIVATE TTM**](ttm-trackactivate.md)
</dt> <dt>

**Informazioni concettuali**
</dt> <dt>

[Uso di controlli ToolTip](using-tooltip-contro.md)
</dt> </dl>

 

