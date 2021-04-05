---
title: Messaggio LVM_EDITLABEL (COMmctrl. h)
description: Inizia la modifica sul posto del testo specificato dell'elemento della visualizzazione elenco. Il messaggio seleziona e concentra in modo implicito l'elemento specificato. È possibile inviare questo messaggio in modo esplicito o usando la \_ macro EditLabel di ListView.
ms.assetid: b63f13f1-6e66-4770-af84-30bcdb241727
keywords:
- Controlli di Windows Message LVM_EDITLABEL
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
ms.openlocfilehash: 25cb4e119731c41130e1c19fdea2f74882796435
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103739967"
---
# <a name="lvm_editlabel-message"></a>\_Messaggio EDITLABEL LVM

Inizia la modifica sul posto del testo specificato dell'elemento della visualizzazione elenco. Il messaggio seleziona e concentra in modo implicito l'elemento specificato. È possibile inviare questo messaggio in modo esplicito o usando la macro [**\_ EditLabel di ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_editlabel) .

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Indice dell'elemento della visualizzazione elenco. Per annullare la modifica, impostare l'indice su-1.

</dd> <dt>

*lParam* 
</dt> <dd>Deve essere zero.</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce l'handle per il controllo di modifica utilizzato per modificare il testo dell'elemento in caso di esito positivo; in caso contrario, **null** .

## <a name="remarks"></a>Commenti

Quando l'utente completa o Annulla la modifica, il controllo di modifica viene eliminato definitivamente e l'handle non è più valido. È possibile sottoclassare il controllo di modifica, ma non eliminarlo.

Il controllo deve avere lo stato attivo prima di inviare questo messaggio al controllo. È possibile impostare lo stato attivo tramite la funzione [**SetFocus**](/windows/desktop/api/winuser/nf-winuser-setfocus) .

Se *wParam* è-1, viene inviato un codice di notifica [ \_ ENDLABELEDIT LVN](lvn-endlabeledit.md) .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |
| Nomi Unicode e ANSI<br/>   | **LVM \_ EDITLABELW** (Unicode) e **LVM \_ EDITLABELA** (ANSI)<br/>               |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**\_CANCELMODE WM**](/windows/desktop/winmsg/wm-cancelmode)
</dt> </dl>

 

