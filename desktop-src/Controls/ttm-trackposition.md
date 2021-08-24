---
title: TTM_TRACKPOSITION messaggio (Commctrl.h)
description: Imposta la posizione di una descrizione comando di rilevamento.
ms.assetid: 9eb7c86c-78e6-442a-ad77-5fb919cab591
keywords:
- TTM_TRACKPOSITION di controllo Windows messaggio
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
ms.openlocfilehash: 547af5014bbf897d320894c4924911b830997ec3d8532e2ce2c7b63f361a11da
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119542826"
---
# <a name="ttm_trackposition-message"></a>Messaggio \_ TRACKPOSITION TTM

Imposta la posizione di una descrizione comando di rilevamento.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Deve essere zero.

</dd> <dt>

*lParam* 
</dt> <dd>

La [**parola chiave LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) specifica la coordinata x del punto in cui verrà visualizzata la descrizione comando di rilevamento, in coordinate dello schermo. HiWORD [**specifica**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) la coordinata y del punto in cui verrà visualizzata la descrizione comando di rilevamento, in coordinate dello schermo.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il valore restituito per questo messaggio non viene usato.

## <a name="remarks"></a>Commenti

Il controllo descrizione comando consente di scegliere dove visualizzare la finestra della descrizione comando in base alle coordinate specificate con questo messaggio. In questo modo la finestra della descrizione comando viene visualizzata accanto allo strumento a cui corrisponde. Per visualizzare le finestre della descrizione comando in corrispondenza di coordinate specifiche, includere il flag ABSOLUTE TTF nel membro \_ **uFlags** della struttura [**TOOLINFO**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) quando si aggiunge lo strumento.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop server 2003 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

**Riferimento**
</dt> <dt>

[**TTM \_ TRACKACTIVATE**](ttm-trackactivate.md)
</dt> <dt>

**Informazioni concettuali**
</dt> <dt>

[Uso dei controlli descrizione comando](using-tooltip-contro.md)
</dt> </dl>

 

