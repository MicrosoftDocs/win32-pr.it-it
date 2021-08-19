---
title: LVM_GETITEMTEXT messaggio (Commctrl.h)
description: Recupera il testo di un elemento della visualizzazione elenco o di un elemento secondario. È possibile inviare questo messaggio in modo esplicito o usando la \_ macro ListView GetItemText.
ms.assetid: 5711ed18-a766-4e7f-9e9d-b9203231b369
keywords:
- LVM_GETITEMTEXT di controllo Windows messaggio
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
ms.openlocfilehash: 32d5292f9814b3ef62667d44582eab44a2f18ac6c274682d180dd26f1b7cdd9f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120062581"
---
# <a name="lvm_getitemtext-message"></a>Messaggio LVM \_ GETITEMTEXT

Recupera il testo di un elemento della visualizzazione elenco o di un elemento secondario. È possibile inviare questo messaggio in modo esplicito o usando la macro [**\_ ListView GetItemText.**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getitemtext)

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Indice dell'elemento della visualizzazione elenco.

</dd> <dt>

*lParam* 
</dt> <dd>

Puntatore a una [**struttura LVITEM.**](/windows/win32/api/commctrl/ns-commctrl-lvitema) Per recuperare il testo dell'elemento, impostare **iSubItem** su zero. Per recuperare il testo di un elemento secondario, impostare **iSubItem** sull'indice dell'elemento secondario. Il **membro pszText** punta a un buffer che riceve il testo. Il **membro cchTextMax** specifica il numero di caratteri nel buffer.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se si invia questo messaggio in modo esplicito, viene restituito il numero di caratteri nel membro **pszText** della [**struttura LVITEM.**](/windows/win32/api/commctrl/ns-commctrl-lvitema)

## <a name="remarks"></a>Commenti

È anche possibile inviare questo messaggio chiamando la macro [**\_ ListView GetItemText.**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getitemtext) Tuttavia, questa macro non restituisce la lunghezza della stringa.

**LVM \_ GETITEMTEXT non** è supportato con lo stile [**LVS \_ OWNERDATA.**](list-view-window-styles.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop server 2003 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |
| Nomi Unicode e ANSI<br/>   | **LVM \_ GETITEMTEXTW** (Unicode) e **LVM \_ GETITEMTEXTA** (ANSI)<br/>           |



 

 





