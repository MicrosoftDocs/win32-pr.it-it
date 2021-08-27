---
title: CB_SETCUEBANNER messaggio (Winuser.h)
description: Imposta il testo del banner di segnale visualizzato per il controllo di modifica di una casella combinata.
ms.assetid: 4b2b5042-ba64-4e3f-adeb-9aea66773b0e
keywords:
- CB_SETCUEBANNER controlli Windows messaggio
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
ms.openlocfilehash: cb546b7113247f09d8929364984d5e73c3e28b6541d2ca04bd631405040bf6fb
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120089041"
---
# <a name="cb_setcuebanner-message"></a>CB \_ SETCUEBANNER message

Imposta il testo del banner di segnale visualizzato per il controllo di modifica di una casella combinata.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Deve essere zero.

</dd> <dt>

*lParam* 
</dt> <dd>

Puntatore a un buffer di stringhe Unicode con terminazione Null che contiene il testo.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce 1 in caso di esito positivo oppure un valore di errore in caso contrario.

## <a name="remarks"></a>Commenti

Il banner segnale è il testo visualizzato nel controllo di modifica di una casella combinata quando non è presente alcuna selezione.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>                                                           |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2008 \[\]<br/>                                                     |
| Intestazione<br/>                   | <dl> <dt>CommCtrl.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Funzionalità della casella combinata](combo-box-features.md)
</dt> </dl>

 

 





