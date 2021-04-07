---
title: Messaggio BCM_SETNOTE (COMmctrl. h)
description: Imposta il testo della nota associata a un pulsante di collegamento al comando. È possibile inviare questo messaggio in modo esplicito o usare la macro di pulsanti \_ .
ms.assetid: c167072a-8207-4744-ac66-247141d726ab
keywords:
- Controlli di Windows Message BCM_SETNOTE
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
ms.openlocfilehash: f544a7fb9dd89346cc2aa9725d36122746a8f608
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964208"
---
# <a name="bcm_setnote-message"></a>\_Messaggio di nota BCM

Imposta il testo della nota associata a un pulsante di collegamento al comando. È possibile inviare questo messaggio in modo esplicito o usare la macro di [**pulsanti \_**](/windows/desktop/api/Commctrl/nf-commctrl-button_setnote) .

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Deve essere zero.

</dd> <dt>

*lParam* 
</dt> <dd>

Puntatore a una stringa **WCHAR** con terminazione null che contiene la nota.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce **true** se l'operazione ha esito positivo o **false** in caso contrario.

## <a name="remarks"></a>Commenti

A partire dalla versione 6,01 di comctl32, i pulsanti di collegamento al comando possono avere una nota.

Il messaggio **BCM \_ Nota** funziona solo con gli stili dei pulsanti [**BS \_ COMMANDLINK**](button-styles.md) e [**BS \_ DEFCOMMANDLINK**](button-styles.md) .

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

 

 





