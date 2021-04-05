---
title: Messaggio CB_SETCUEBANNER (winuser. h)
description: Imposta il testo del banner cue visualizzato per il controllo di modifica di una casella combinata.
ms.assetid: 4b2b5042-ba64-4e3f-adeb-9aea66773b0e
keywords:
- Controlli di Windows Message CB_SETCUEBANNER
topic_type:
- apiref
api_name:
- CB_SETCUEBANNER
api_location:
- CommCtrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d5799b1b1be5e938ce1e234948a1f7d878122f30
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104048350"
---
# <a name="cb_setcuebanner-message"></a>\_Messaggio SETCUEBANNER CB

Imposta il testo del banner cue visualizzato per il controllo di modifica di una casella combinata.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Deve essere zero.

</dd> <dt>

*lParam* 
</dt> <dd>

Puntatore a un buffer di stringa Unicode con terminazione null che contiene il testo.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce 1 se l'operazione ha esito positivo o un valore di errore in caso contrario.

## <a name="remarks"></a>Commenti

Il banner cue è il testo visualizzato nel controllo di modifica di una casella combinata in assenza di selezione.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                                           |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/>                                                     |
| Intestazione<br/>                   | <dl> <dt>CommCtrl. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Funzionalità della casella combinata](combo-box-features.md)
</dt> </dl>

 

 





