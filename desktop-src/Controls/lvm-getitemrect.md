---
title: Messaggio LVM_GETITEMRECT (COMmctrl. h)
description: Recupera il rettangolo di delimitazione per tutto o parte di un elemento nella visualizzazione corrente. È possibile inviare questo messaggio in modo esplicito o usando la \_ macro GetItemRect di ListView.
ms.assetid: 7ce74b65-3360-42b4-9889-d90aefe2d284
keywords:
- Controlli di Windows Message LVM_GETITEMRECT
topic_type:
- apiref
api_name:
- LVM_GETITEMRECT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cd0915c9afc16f13ac8f36a639524fb5af6e8082
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104048646"
---
# <a name="lvm_getitemrect-message"></a>\_Messaggio GETITEMRECT LVM

Recupera il rettangolo di delimitazione per tutto o parte di un elemento nella visualizzazione corrente. È possibile inviare questo messaggio in modo esplicito o usando la macro [**\_ GetItemRect di ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getitemrect) .

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* \[ in\]
</dt> <dd>

Indice dell'elemento della visualizzazione elenco.

</dd> <dt>

*lParam* \[ in uscita\]
</dt> <dd>

Puntatore a una struttura [**Rect**](/previous-versions//dd162897(v=vs.85)) che riceve il rettangolo di delimitazione. Quando il messaggio viene inviato, il membro **sinistro** di questa struttura viene usato per specificare la parte dell'elemento della visualizzazione elenco da cui recuperare il rettangolo di delimitazione. Deve essere impostato su uno dei valori seguenti:



| Valore                                                                                                                                                                     | Significato                                                                                                         |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| <span id="LVIR_BOUNDS"></span><span id="lvir_bounds"></span><dl> <dt>**limiti di LVIR \_**</dt> </dl>                   | Restituisce il rettangolo di delimitazione dell'intero elemento, inclusi l'icona e l'etichetta.<br/>                     |
| <span id="LVIR_ICON"></span><span id="lvir_icon"></span><dl> <dt>**\_icona LVIR**</dt> </dl>                         | Restituisce il rettangolo di delimitazione dell'icona o dell'icona piccola.<br/>                                            |
| <span id="LVIR_LABEL"></span><span id="lvir_label"></span><dl> <dt>**\_etichetta LVIR**</dt> </dl>                      | Restituisce il rettangolo di delimitazione del testo dell'elemento.<br/>                                                     |
| <span id="LVIR_SELECTBOUNDS"></span><span id="lvir_selectbounds"></span><dl> <dt>**\_SELECTBOUNDS LVIR**</dt> </dl> | Restituisce l'Unione dei \_ rettangoli LVIR Icon e LVIR \_ Label, ma esclude le colonne nella visualizzazione report.<br/> |



 

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce **true** se l'operazione ha esito positivo o **false** in caso contrario.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

