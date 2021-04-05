---
title: Messaggio BCM_GETNOTELENGTH (COMmctrl. h)
description: Ottiene la lunghezza del testo della nota che può essere visualizzato nella descrizione di un pulsante di collegamento al comando. Inviare questo messaggio in modo esplicito o tramite il pulsante \_ GetNoteLength macro.
ms.assetid: 62385485-b553-47e9-9f15-696cc4694752
keywords:
- Controlli di Windows Message BCM_GETNOTELENGTH
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
ms.openlocfilehash: 1b33c5245778481033bd97326c3d66a40bf03210
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104048267"
---
# <a name="bcm_getnotelength-message"></a>\_Messaggio GETNOTELENGTH BCM

Ottiene la lunghezza del testo della nota che può essere visualizzato nella descrizione di un pulsante di collegamento al comando. Inviare questo messaggio in modo esplicito o tramite il [**pulsante \_ GetNoteLength**](/windows/desktop/api/Commctrl/nf-commctrl-button_getnotelength) macro.

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

Restituisce la lunghezza del testo della nota in **WCHAR**, escluso il **valore null** di terminazione, o zero se non è presente alcun testo di nota.

## <a name="remarks"></a>Commenti

A partire dalla versione 6,01 di comctl32, i pulsanti di collegamento al comando possono avere una nota. Per informazioni sulle versioni di DLL, vedere [versioni di controllo comuni](common-control-versions.md).

Il messaggio **BCM \_ GETNOTELENGTH** funziona solo con gli stili dei pulsanti [**BS \_ COMMANDLINK**](button-styles.md) e [**BS \_ DEFCOMMANDLINK**](button-styles.md) .

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

 

 





