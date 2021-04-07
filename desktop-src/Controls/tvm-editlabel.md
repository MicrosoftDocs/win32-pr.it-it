---
title: Messaggio TVM_EDITLABEL (COMmctrl. h)
description: Inizia la modifica sul posto del testo dell'elemento specificato, sostituendo il testo dell'elemento con un controllo di modifica a riga singola contenente il testo.
ms.assetid: ae844cbf-fa43-4f91-90cc-688f44bf77a5
keywords:
- Controlli di Windows Message TVM_EDITLABEL
topic_type:
- apiref
api_name:
- TVM_EDITLABEL
- TVM_EDITLABELA
- TVM_EDITLABELW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3608c3f959c45571d9bc085518b763cf505180ee
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964034"
---
# <a name="tvm_editlabel-message"></a>\_Messaggio EDITLABEL TVM

Inizia la modifica sul posto del testo dell'elemento specificato, sostituendo il testo dell'elemento con un controllo di modifica a riga singola contenente il testo. Questo messaggio seleziona e concentra in modo implicito l'elemento specificato. È possibile inviare questo messaggio in modo esplicito o usando la macro [**\_ EditLabel di TreeView**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_editlabel) .

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>Deve essere zero.</dd> <dt>

*lParam* 
</dt> <dd>

Handle per l'elemento da modificare.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce l'handle per il controllo di modifica utilizzato per modificare il testo dell'elemento in caso di esito positivo; in caso contrario, **null** .

## <a name="remarks"></a>Commenti

Questo messaggio Invia un codice di notifica di [TVN \_ BEGINLABELEDIT](tvn-beginlabeledit.md) all'elemento padre del controllo di visualizzazione albero.

Quando l'utente completa o Annulla la modifica, il controllo di modifica viene eliminato definitivamente e l'handle non è più valido. È possibile sottoclassare il controllo di modifica, ma non eliminarlo definitivamente.

Il controllo deve avere lo stato attivo prima di inviare questo messaggio al controllo. È possibile impostare lo stato attivo tramite la funzione [**SetFocus**](/windows/desktop/api/winuser/nf-winuser-setfocus) .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |
| Nomi Unicode e ANSI<br/>   | **TVM \_ EDITLABELW** (Unicode) e **TVM \_ EDITLABELA** (ANSI)<br/>               |



 

