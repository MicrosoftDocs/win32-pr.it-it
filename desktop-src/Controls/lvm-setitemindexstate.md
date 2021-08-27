---
title: LVM_SETITEMINDEXSTATE messaggio (Commctrl.h)
description: Imposta lo stato di un elemento di visualizzazione elenco. Inviare questo messaggio in modo esplicito o usando la \_ macro ListView SetItemIndexState.
ms.assetid: 9fea6420-320a-4d2a-84b5-7923fbb14655
keywords:
- LVM_SETITEMINDEXSTATE di controllo Windows messaggio
topic_type:
- apiref
api_name:
- LVM_SETITEMINDEXSTATE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 18094986f5a57713e842b51b31c74ccfe4987d1c1fe62380ea8a986762e20c7a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120062211"
---
# <a name="lvm_setitemindexstate-message"></a>Messaggio LVM \_ SETITEMINDEXSTATE

Imposta lo stato di un elemento di visualizzazione elenco. Inviare questo messaggio in modo esplicito o usando la macro [**\_ ListView SetItemIndexState.**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setitemindexstate)

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* \[ Pollici\]
</dt> <dd>

Puntatore a una [**struttura LVITEMINDEX**](/windows/win32/api/commctrl/ns-commctrl-lvitemindex) per l'elemento. Il processo chiamante è responsabile dell'allocazione di questa struttura e dell'impostazione dei membri.

</dd> <dt>

*lParam* \[ Pollici\]
</dt> <dd>

Puntatore a una [**struttura LVITEM.**](/windows/win32/api/commctrl/ns-commctrl-lvitema) Il processo chiamante è responsabile dell'allocazione della memoria per la struttura . Impostare il **membro di** stato su uno o più flag [List-View Item States](list-view-item-states.md) (come combinazione bit per bit). Impostare il **membro stateMask** della struttura per indicare i bit validi del membro **di** stato. Per altre informazioni, vedere il **membro stateMask** della **struttura LVITEM.**

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce uno dei valori seguenti di tipo **HRESULT.**



| Codice restituito                                                                                  | Descrizione                                                       |
|----------------------------------------------------------------------------------------------|-------------------------------------------------------------------|
| <dl> <dt>**E \_ FAIL**</dt> </dl>       | Impossibile impostare lo stato.<br/>                            |
| <dl> <dt>**E \_ UNEXPECTED**</dt> </dl> | Il controllo visualizzazione elenco non è pronto per l'operazione.<br/> |
| <dl> <dt>**S \_ OK**</dt> </dl>         | L'operazione è stata completata.<br/>                          |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2008 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





