---
title: BCM_GETNOTELENGTH messaggio (Commctrl.h)
description: Ottiene la lunghezza del testo della nota che può essere visualizzato nella descrizione di un pulsante di collegamento di comando. Inviare questo messaggio in modo esplicito o usando la \_ macro Button GetNoteLength.
ms.assetid: 62385485-b553-47e9-9f15-696cc4694752
keywords:
- BCM_GETNOTELENGTH di controllo Windows messaggio
topic_type:
- apiref
api_name:
- BCM_GETNOTELENGTH
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 385cb5d7694818a0e0e03ab74bcc31b76d13f5d304c7415b1f70a0fd43e1b31b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119921661"
---
# <a name="bcm_getnotelength-message"></a>BCM \_ GETNOTELENGTH message

Ottiene la lunghezza del testo della nota che può essere visualizzato nella descrizione di un pulsante di collegamento di comando. Inviare questo messaggio in modo esplicito o usando la macro [**\_ Button GetNoteLength.**](/windows/desktop/api/Commctrl/nf-commctrl-button_getnotelength)

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Deve essere zero.

</dd> <dt>

*lParam* 
</dt> <dd>

Deve essere zero.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce la lunghezza del testo della nota nei **WCHAR,** senza alcun carattere **NULL** di terminazione o zero se non è presente alcun testo della nota.

## <a name="remarks"></a>Commenti

A partire da comctl32 DLL versione 6.01, i pulsanti di collegamento ai comandi possono avere una nota. Per informazioni sulle versioni dll, vedere [Versioni dei controlli comuni.](common-control-versions.md)

Il **messaggio BCM \_ GETNOTELENGTH** funziona solo con gli stili dei pulsanti [**BS \_ COMMANDLINK**](button-styles.md) e [**BS \_ DEFCOMMANDLINK.**](button-styles.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2008 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



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

 

 





