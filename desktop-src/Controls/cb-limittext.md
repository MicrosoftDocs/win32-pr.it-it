---
title: Messaggio CB_LIMITTEXT (winuser. h)
description: Limita la lunghezza del testo che l'utente può digitare nel controllo di modifica di una casella combinata.
ms.assetid: 95b7d07a-594b-4096-afbb-4dab77bdc41d
keywords:
- Controlli di Windows Message CB_LIMITTEXT
topic_type:
- apiref
api_name:
- CB_LIMITTEXT
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 34ea9ccd63bb1503e73aebdd584a53bc32bcb8fa
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104048351"
---
# <a name="cb_limittext-message"></a>\_Messaggio LIMITTEXT CB

Limita la lunghezza del testo che l'utente può digitare nel controllo di modifica di una casella combinata.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Numero massimo di **TCHARs** che l'utente può immettere, escluso il carattere null di terminazione. Se questo parametro è zero, la lunghezza del testo è limitata ai caratteri 0x7FFFFFFE.

</dd> <dt>

*lParam* 
</dt> <dd>

Questo parametro non viene usato.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il valore restituito è sempre **true**.

## <a name="remarks"></a>Commenti

Se la casella combinata non ha lo stile [**CBS \_ AUTOHSCROLL**](combo-box-styles.md) , l'impostazione del limite di testo su un valore superiore a quello del controllo di modifica non ha alcun effetto.

Il messaggio **CB \_ LIMITTEXT** limita solo il testo che l'utente può immettere. Non ha alcun effetto sui testi già presenti nel controllo di modifica quando il messaggio viene inviato, né sulla lunghezza del testo copiato nel controllo di modifica quando viene selezionata una stringa nella casella di riepilogo.

Il limite predefinito al testo che un utente può immettere nel controllo di modifica è 30.000 **TCHARs**.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                                           |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                                     |
| Intestazione<br/>                   | <dl> <dt>Winuser. h (include Windows. h)</dt> </dl> |



 

 





