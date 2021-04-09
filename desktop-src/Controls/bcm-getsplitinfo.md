---
title: Messaggio BCM_GETSPLITINFO (COMmctrl. h)
description: Ottiene informazioni per un controllo pulsante di divisione. Inviare questo messaggio in modo esplicito o tramite il pulsante \_ GetSplitInfo macro.
ms.assetid: d608440d-b8d8-4e32-9128-08b7566b185c
keywords:
- Controlli di Windows Message BCM_GETSPLITINFO
topic_type:
- apiref
api_name:
- BCM_GETSPLITINFO
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 162c5522fcb432e3d512f688ae24aa12d4d0d8e1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964296"
---
# <a name="bcm_getsplitinfo-message"></a>\_Messaggio GETSPLITINFO BCM

Ottiene informazioni per un controllo pulsante di divisione. Inviare questo messaggio in modo esplicito o tramite il [**pulsante \_ GetSplitInfo**](/windows/desktop/api/Commctrl/nf-commctrl-button_getsplitinfo) macro.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Deve essere zero.

</dd> <dt>

*lParam* \[ in uscita\]
</dt> <dd>

Puntatore a una struttura [**\_ SPLITINFO Button**](/windows/win32/api/commctrl/ns-commctrl-button_splitinfo) per ricevere informazioni sul pulsante. Il chiamante è responsabile dell'allocazione della memoria per la struttura. Impostare il membro **mask** della struttura per determinare le informazioni da ricevere.

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

 

 





