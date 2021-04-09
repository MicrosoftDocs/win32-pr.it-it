---
title: Messaggio LVM_GETITEMTEXT (COMmctrl. h)
description: Recupera il testo di un elemento della visualizzazione elenco o di un elemento secondario. È possibile inviare questo messaggio in modo esplicito o usando la \_ macro GetItemText di ListView.
ms.assetid: 5711ed18-a766-4e7f-9e9d-b9203231b369
keywords:
- Controlli di Windows Message LVM_GETITEMTEXT
topic_type:
- apiref
api_name:
- LVM_GETITEMTEXT
- LVM_GETITEMTEXTA
- LVM_GETITEMTEXTW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c71eec6b9dab4c649b11da5b24568eea816774ef
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104120986"
---
# <a name="lvm_getitemtext-message"></a>\_Messaggio GETITEMTEXT LVM

Recupera il testo di un elemento della visualizzazione elenco o di un elemento secondario. È possibile inviare questo messaggio in modo esplicito o usando la macro [**\_ GetItemText di ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getitemtext) .

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Indice dell'elemento della visualizzazione elenco.

</dd> <dt>

*lParam* 
</dt> <dd>

Puntatore a una struttura [**LVITEM**](/windows/win32/api/commctrl/ns-commctrl-lvitema) . Per recuperare il testo dell'elemento, impostare **iSubItem** su zero. Per recuperare il testo di un elemento secondario, impostare **iSubItem** sull'indice dell'elemento secondario. Il membro **pszText** punta a un buffer che riceve il testo. Il membro **cchTextMax** specifica il numero di caratteri nel buffer.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se si invia questo messaggio in modo esplicito, viene restituito il numero di caratteri nel membro **pszText** della struttura [**LVITEM**](/windows/win32/api/commctrl/ns-commctrl-lvitema) .

## <a name="remarks"></a>Commenti

È anche possibile inviare questo messaggio chiamando la macro [**\_ GetItemText di ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getitemtext) . Tuttavia, questa macro non restituisce la lunghezza della stringa.

**LVM \_ GETITEMTEXT** non è supportato nello stile [**\_ OWNERDATA di LVS**](list-view-window-styles.md) .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |
| Nomi Unicode e ANSI<br/>   | **LVM \_ GETITEMTEXTW** (Unicode) e **LVM \_ GETITEMTEXTA** (ANSI)<br/>           |



 

 





