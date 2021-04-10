---
title: Messaggio TVM_GETEDITCONTROL (COMmctrl. h)
description: Recupera l'handle per il controllo di modifica utilizzato per modificare il testo di un elemento della visualizzazione struttura ad albero. È possibile inviare questo messaggio in modo esplicito o usando la \_ macro GetEditControl di TreeView.
ms.assetid: c89e57e8-e113-47a1-85e6-bb68990f9c1a
keywords:
- Controlli di Windows Message TVM_GETEDITCONTROL
topic_type:
- apiref
api_name:
- TVM_GETEDITCONTROL
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 79b4ce0beb125218e65c2c342caf59b57473088e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104121291"
---
# <a name="tvm_geteditcontrol-message"></a>\_Messaggio GETEDITCONTROL TVM

Recupera l'handle per il controllo di modifica utilizzato per modificare il testo di un elemento della visualizzazione struttura ad albero. È possibile inviare questo messaggio in modo esplicito o usando la macro [**\_ GetEditControl di TreeView**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_geteditcontrol) .

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>Deve essere zero.</dd> <dt>

*lParam* 
</dt> <dd>Deve essere zero.</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce l'handle per il controllo di modifica, se ha esito positivo, oppure **null** in caso contrario.

## <a name="remarks"></a>Commenti

Quando viene avviata la modifica dell'etichetta, viene creato un controllo di modifica, ma non è posizionato o visualizzato. Prima che venga visualizzato, il controllo di visualizzazione albero Invia la finestra padre a un codice di notifica di [TVN \_ BEGINLABELEDIT](tvn-beginlabeledit.md) .

Per personalizzare la modifica delle etichette, implementare un gestore per [TVN \_ BEGINLABELEDIT](tvn-beginlabeledit.md) e fare in modo che invii un messaggio **TVM \_ GETEDITCONTROL** al controllo di visualizzazione albero. Se è in corso la modifica di un'etichetta, il valore restituito sarà un handle per il controllo di modifica. Utilizzare questo handle per personalizzare il controllo di modifica inviando i normali messaggi **em \_ xxx** .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





