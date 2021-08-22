---
title: BCM_SETNOTE messaggio (Commctrl.h)
description: Imposta il testo della nota associata a un pulsante di collegamento di comando. È possibile inviare questo messaggio in modo esplicito o usare la \_ macro Button SetNote.
ms.assetid: c167072a-8207-4744-ac66-247141d726ab
keywords:
- BCM_SETNOTE di controllo Windows messaggio
topic_type:
- apiref
api_name:
- BCM_SETNOTE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 82f0f049c1ad8a9837695a1f5d7327883e1dabfb7dd077bd6efce78fa6a0a708
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119921551"
---
# <a name="bcm_setnote-message"></a>BCM \_ SETNOTE message

Imposta il testo della nota associata a un pulsante di collegamento di comando. È possibile inviare questo messaggio in modo esplicito o usare la macro [**\_ Button SetNote.**](/windows/desktop/api/Commctrl/nf-commctrl-button_setnote)

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Deve essere zero.

</dd> <dt>

*lParam* 
</dt> <dd>

Puntatore a una stringa **WCHAR** con terminazione Null che contiene la nota.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce **TRUE in** caso di esito positivo oppure FALSE **in** caso contrario.

## <a name="remarks"></a>Commenti

A partire da comctl32 DLL versione 6.01, i pulsanti di collegamento ai comandi possono avere una nota.

Il **messaggio \_ BCM SETNOTE** funziona solo con gli stili dei pulsanti [**BS \_ COMMANDLINK**](button-styles.md) e [**BS \_ DEFCOMMANDLINK.**](button-styles.md)

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

 

 





