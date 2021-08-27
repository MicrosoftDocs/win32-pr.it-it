---
title: IPM_SETFOCUS messaggio (Commctrl.h)
description: Imposta lo stato attivo della tastiera sul campo specificato nel controllo dell'indirizzo IP. Tutto il testo in tale campo verrà selezionato.
ms.assetid: 4b975eb2-85e1-4e33-a803-99b48d2ff5e8
keywords:
- IPM_SETFOCUS di controllo Windows messaggio
topic_type:
- apiref
api_name:
- IPM_SETFOCUS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2a74d98aa4d4259d11d7fef6e0bfdad2bfe741447ddffab27fa41545e7eda515
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120085571"
---
# <a name="ipm_setfocus-message"></a>Messaggio \_ IPM SETFOCUS

Imposta lo stato attivo della tastiera sul campo specificato nel controllo dell'indirizzo IP. Tutto il testo in tale campo verrà selezionato.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Indice del campo in base zero sul quale deve essere impostato lo stato attivo. Se questo valore è maggiore del numero di campi, lo stato attivo viene impostato sul primo campo vuoto. Se tutti i campi sono non blank, lo stato attivo viene impostato sul primo campo.

</dd> <dt>

*lParam* 
</dt> <dd>Deve essere zero.</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il valore restituito non viene utilizzato.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2003 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





