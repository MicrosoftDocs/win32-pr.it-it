---
title: Messaggio BCM_SETSPLITINFO (COMmctrl. h)
description: Imposta le informazioni per un controllo pulsante di divisione. Inviare questo messaggio in modo esplicito o tramite il pulsante \_ SetSplitInfo macro.
ms.assetid: 609b8972-9616-4850-a72c-2f87ce19f563
keywords:
- Controlli di Windows Message BCM_SETSPLITINFO
topic_type:
- apiref
api_name:
- BCM_SETSPLITINFO
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ac40f2d1ef016ee76ab21ccf2dc4733d0ff427f3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301706"
---
# <a name="bcm_setsplitinfo-message"></a>\_Messaggio SETSPLITINFO BCM

Imposta le informazioni per un controllo pulsante di divisione. Inviare questo messaggio in modo esplicito o tramite il [**pulsante \_ SetSplitInfo**](/windows/desktop/api/Commctrl/nf-commctrl-button_setsplitinfo) macro.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Deve essere zero.

</dd> <dt>

*lParam* \[ in\]
</dt> <dd>

Puntatore a una struttura [**\_ SPLITINFO Button**](/windows/win32/api/commctrl/ns-commctrl-button_splitinfo) che contiene informazioni sul pulsante di suddivisione.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce **true** se l'operazione ha esito positivo o **false** in caso contrario.

## <a name="remarks"></a>Commenti

Utilizzare questo messaggio solo con gli stili del pulsante [**BS \_ SPLITBUTTON**](button-styles.md) e [**BS \_ DEFSPLITBUTTON**](button-styles.md) .

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

 

 





