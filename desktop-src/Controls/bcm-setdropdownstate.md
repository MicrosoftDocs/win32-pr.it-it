---
title: Messaggio BCM_SETDROPDOWNSTATE (COMmctrl. h)
description: Imposta lo stato di elenco a discesa per un pulsante con lo stile \_ elenco a discesa TBSTYLE. Inviare questo messaggio in modo esplicito o tramite il pulsante \_ SetDropDownState macro.
ms.assetid: 725deff4-0bcb-497d-a6cf-e9c98b05f16e
keywords:
- Controlli di Windows Message BCM_SETDROPDOWNSTATE
topic_type:
- apiref
api_name:
- BCM_SETDROPDOWNSTATE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fc44ec58d40e047708591121f81c84f327ca47c1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104119739"
---
# <a name="bcm_setdropdownstate-message"></a>\_Messaggio SETDROPDOWNSTATE BCM

Imposta lo stato di elenco a discesa per un pulsante con lo stile [**\_ elenco a discesa TBSTYLE**](toolbar-control-and-button-styles.md). Inviare questo messaggio in modo esplicito o tramite il [**pulsante \_ SetDropDownState**](/windows/desktop/api/Commctrl/nf-commctrl-button_setdropdownstate) macro.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* \[ in\]
</dt> <dd>

**Bool** che è **true** per lo stato di BST \_ DROPDOWNPUSHED o **false** in caso contrario.

</dd> <dt>

*lParam* 
</dt> <dd>

Deve essere zero.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce **true** se l'operazione ha esito positivo o **false** in caso contrario.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

**Riferimento**
</dt> <dt>

[Stili dei pulsanti](button-styles.md)
</dt> <dt>

**Informazioni concettuali**
</dt> <dt>

[Tipi di pulsante](button-types-and-styles.md)
</dt> </dl>

 

 





