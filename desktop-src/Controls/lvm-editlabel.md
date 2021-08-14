---
title: LVM_EDITLABEL messaggio (Commctrl.h)
description: Avvia la modifica sul posto del testo dell'elemento della visualizzazione elenco specificato. Il messaggio seleziona e attiva in modo implicito l'elemento specificato. È possibile inviare questo messaggio in modo esplicito o tramite la \_ macro ListView EditLabel.
ms.assetid: b63f13f1-6e66-4770-af84-30bcdb241727
keywords:
- LVM_EDITLABEL di controllo Windows messaggio
topic_type:
- apiref
api_name:
- LVM_EDITLABEL
- LVM_EDITLABELA
- LVM_EDITLABELW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a9be1896c39e06c25bf06e033d74a17107b3e194a43b1c574e1dcb7f9a456413
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118411845"
---
# <a name="lvm_editlabel-message"></a>Messaggio LVM \_ EDITLABEL

Avvia la modifica sul posto del testo dell'elemento della visualizzazione elenco specificato. Il messaggio seleziona e attiva in modo implicito l'elemento specificato. È possibile inviare questo messaggio in modo esplicito o tramite la macro [**\_ ListView EditLabel.**](/windows/desktop/api/Commctrl/nf-commctrl-listview_editlabel)

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Indice dell'elemento della visualizzazione elenco. Per annullare la modifica, impostare l'indice su -1.

</dd> <dt>

*lParam* 
</dt> <dd>Deve essere zero.</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce l'handle al controllo di modifica utilizzato per modificare il testo dell'elemento in caso di esito positivo oppure **NULL in caso contrario.**

## <a name="remarks"></a>Commenti

Quando l'utente completa o annulla la modifica, il controllo di modifica viene eliminato e l'handle non è più valido. È possibile creare una sottoclasse del controllo di modifica, ma non eliminare il controllo.

Il controllo deve avere lo stato attivo prima di inviare questo messaggio al controllo . Lo stato attivo può essere impostato usando la [**funzione SetFocus.**](/windows/desktop/api/winuser/nf-winuser-setfocus)

Se *wParam è* -1, viene inviato un codice di notifica [ \_ LVN ENDLABELEDIT.](lvn-endlabeledit.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop server 2003 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |
| Nomi Unicode e ANSI<br/>   | **LVM \_ EDITLABELW** (Unicode) e **LVM \_ EDITLABELA** (ANSI)<br/>               |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**WM \_ CANCELMODE**](/windows/desktop/winmsg/wm-cancelmode)
</dt> </dl>

 

