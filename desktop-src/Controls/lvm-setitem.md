---
title: LVM_SETITEM messaggio (Commctrl.h)
description: Imposta alcuni o tutti gli attributi di un elemento della visualizzazione elenco. È anche possibile inviare LVM \_ SETITEM per impostare il testo di un elemento secondario. È possibile inviare questo messaggio in modo esplicito o tramite la \_ macro ListView SetItem.
ms.assetid: f1189b5d-bce7-4569-b4b9-bd750d7ef505
keywords:
- LVM_SETITEM dei messaggi Windows controlli
topic_type:
- apiref
api_name:
- LVM_SETITEM
- LVM_SETITEMA
- LVM_SETITEMW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 83ccc47c27ff05e75ba2633e18363c3e26e844c359b54d009101512fc837b668
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119019159"
---
# <a name="lvm_setitem-message"></a>Messaggio \_ LVM SETITEM

Imposta alcuni o tutti gli attributi di un elemento della visualizzazione elenco. È anche possibile inviare LVM \_ SETITEM per impostare il testo di un elemento secondario. È possibile inviare questo messaggio in modo esplicito o tramite la macro [**\_ ListView SetItem.**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setitem)

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>Deve essere zero.</dd> <dt>

*lParam* 
</dt> <dd>

Puntatore a una [**struttura LVITEM**](/windows/win32/api/commctrl/ns-commctrl-lvitema) che contiene i nuovi attributi dell'elemento. I **membri iItem** **e iSubItem** identificano l'elemento o l'elemento secondario e il membro **mask** specifica gli attributi da impostare. Se il **membro mask** specifica il valore LVIF TEXT, il membro pszText è l'indirizzo di una stringa con terminazione Null e il membro \_ **cchTextMax** viene ignorato.  Se il **membro mask** specifica il valore LVIF STATE, il membro \_ **stateMask** specifica gli stati dell'elemento da modificare e il membro di stato contiene i valori per tali stati. 

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce **TRUE in** caso di esito positivo oppure FALSE **in** caso contrario.

## <a name="remarks"></a>Commenti

Per impostare gli attributi di un elemento della visualizzazione elenco, impostare il membro **iItem** della struttura [**LVITEM**](/windows/win32/api/commctrl/ns-commctrl-lvitema) sull'indice dell'elemento e il membro **iSubItem** su zero. Per un elemento, è possibile impostare i membri **state**, **pszText**, **iImage** e **lParam** della struttura **LVITEM.**

Per impostare il testo di un elemento secondario, impostare i membri **iItem** e **iSubItem** per indicare l'elemento secondario specifico e usare il membro **pszText** per specificare il testo. In alternativa, è possibile usare la macro [**\_ ListView SetItemText**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setitemtext) per impostare il testo di un elemento secondario. Non è possibile impostare **i membri state** o **lParam** per gli elementi secondari perché gli elementi secondari non dispongono di questi attributi. Nella versione 4.70 e successive è possibile impostare il membro **iImage** per gli elementi secondari. L'immagine dell'elemento secondario verrà visualizzata se il controllo visualizzazione elenco ha lo stile [**esteso LVS \_ EX \_ SUBITEMIMAGES.**](extended-list-view-styles.md) Le versioni precedenti ignoreranno l'immagine dell'elemento secondario.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop server 2003 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |
| Nomi Unicode e ANSI<br/>   | **LVM \_ SETITEMW** (Unicode) e **LVM \_ SETITEMA** (ANSI)<br/>                   |



 

 





