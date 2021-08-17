---
title: TVM_EDITLABEL messaggio (Commctrl.h)
description: Inizia la modifica sul posto del testo dell'elemento specificato, sostituendo il testo dell'elemento con un controllo di modifica a riga singola contenente il testo.
ms.assetid: ae844cbf-fa43-4f91-90cc-688f44bf77a5
keywords:
- TVM_EDITLABEL dei controlli Windows messaggio
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
ms.openlocfilehash: 87ba9f9d0af4d6afb3c454f5e5477ccd67728bdec7f378b0f0a04adc901ba322
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118408588"
---
# <a name="tvm_editlabel-message"></a>Messaggio TVM \_ EDITLABEL

Inizia la modifica sul posto del testo dell'elemento specificato, sostituendo il testo dell'elemento con un controllo di modifica a riga singola contenente il testo. Questo messaggio seleziona e attiva in modo implicito l'elemento specificato. È possibile inviare questo messaggio in modo esplicito o usando la macro [**\_ EditLabel di TreeView.**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_editlabel)

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>Deve essere zero.</dd> <dt>

*lParam* 
</dt> <dd>

Handle per l'elemento da modificare.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce l'handle al controllo di modifica utilizzato per modificare il testo dell'elemento in caso di esito positivo oppure **NULL in caso contrario.**

## <a name="remarks"></a>Commenti

Questo messaggio invia un [codice di notifica \_ TVN BEGINLABELEDIT](tvn-beginlabeledit.md) all'elemento padre del controllo di visualizzazione albero.

Quando l'utente completa o annulla la modifica, il controllo di modifica viene eliminato e l'handle non è più valido. È possibile creare una sottoclasse del controllo di modifica, ma non eliminare il controllo.

Il controllo deve avere lo stato attivo prima di inviare questo messaggio al controllo. Lo stato attivo può essere impostato usando [**la funzione SetFocus.**](/windows/desktop/api/winuser/nf-winuser-setfocus)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2003 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |
| Nomi Unicode e ANSI<br/>   | **TVM \_ EDITLABELW** (Unicode) e **TVM \_ EDITLABELA** (ANSI)<br/>               |



 

