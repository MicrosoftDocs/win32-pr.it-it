---
title: Messaggio LVM_SETITEMINDEXSTATE (COMmctrl. h)
description: Imposta lo stato di un elemento della visualizzazione elenco. Inviare questo messaggio in modo esplicito o utilizzando la \_ macro SetItemIndexState di ListView.
ms.assetid: 9fea6420-320a-4d2a-84b5-7923fbb14655
keywords:
- Controlli di Windows Message LVM_SETITEMINDEXSTATE
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
ms.openlocfilehash: 01ce8f6847c733127053e2162dd785d52fb77cfa
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104048123"
---
# <a name="lvm_setitemindexstate-message"></a>\_Messaggio SETITEMINDEXSTATE LVM

Imposta lo stato di un elemento della visualizzazione elenco. Inviare questo messaggio in modo esplicito o utilizzando la macro [**\_ SetItemIndexState di ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setitemindexstate) .

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* \[ in\]
</dt> <dd>

Puntatore a una struttura [**LVITEMINDEX**](/windows/win32/api/commctrl/ns-commctrl-lvitemindex) per l'elemento. Il processo chiamante è responsabile dell'allocazione di questa struttura e dell'impostazione dei membri.

</dd> <dt>

*lParam* \[ in\]
</dt> <dd>

Puntatore a una struttura [**LVITEM**](/windows/win32/api/commctrl/ns-commctrl-lvitema) . Il processo chiamante è responsabile dell'allocazione della memoria per la struttura. Impostare il membro **stato** su uno o più (come combinazione bit per bit) dei flag [degli Stati degli elementi della visualizzazione elenco](list-view-item-states.md) . Impostare il membro **stateMask** della struttura per indicare i bit validi del membro di **stato** . Per ulteriori informazioni, vedere il membro **stateMask** della struttura **LVITEM** .

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce uno dei valori seguenti di tipo **HRESULT**.



| Codice restituito                                                                                  | Descrizione                                                       |
|----------------------------------------------------------------------------------------------|-------------------------------------------------------------------|
| <dl> <dt>**E \_ non riescono**</dt> </dl>       | Non è stato possibile impostare lo stato.<br/>                            |
| <dl> <dt>**E \_ imprevisto**</dt> </dl> | Il controllo elenco-visualizzazione non è pronto per l'operazione.<br/> |
| <dl> <dt>**\_OK**</dt> </dl>         | L'operazione è stata completata.<br/>                          |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





