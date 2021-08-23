---
title: LVM_INSERTITEM messaggio (Commctrl.h)
description: Inserisce un nuovo elemento in un controllo di visualizzazione elenco. È possibile inviare questo messaggio in modo esplicito o tramite la \_ macro ListView InsertItem.
ms.assetid: ac283e81-5b9f-4a90-acdb-fd7813c9cb84
keywords:
- LVM_INSERTITEM controlli Windows messaggi
topic_type:
- apiref
api_name:
- LVM_INSERTITEM
- LVM_INSERTITEMA
- LVM_INSERTITEMW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9408a8d09adca2a097281b13e56241c66a68521dcef0892502d7f8d0e14d25e4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119575711"
---
# <a name="lvm_insertitem-message"></a>Messaggio \_ LVM INSERTITEM

Inserisce un nuovo elemento in un controllo di visualizzazione elenco. È possibile inviare questo messaggio in modo esplicito o tramite la macro [**\_ ListView InsertItem.**](/windows/desktop/api/Commctrl/nf-commctrl-listview_insertitem)

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>Deve essere zero.</dd> <dt>

*lParam* 
</dt> <dd>

Puntatore a [**una struttura LVITEM**](/windows/win32/api/commctrl/ns-commctrl-lvitema) che specifica gli attributi dell'elemento della visualizzazione elenco. Usare il **membro iItem** per specificare l'indice in base zero in corrispondenza del quale inserire il nuovo elemento. Se questo valore è maggiore del numero di elementi attualmente contenuti nella visualizzazione elenco, il nuovo elemento verrà aggiunto alla fine dell'elenco e verrà assegnato l'indice corretto. Esaminare il valore restituito del messaggio per determinare l'indice effettivo assegnato all'elemento.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce l'indice del nuovo elemento in caso di esito positivo oppure -1 in caso contrario.

## <a name="remarks"></a>Commenti

Non è possibile usare [**ListView \_ InsertItem o**](/windows/desktop/api/Commctrl/nf-commctrl-listview_insertitem) **LVM \_ INSERTITEM** per inserire elementi secondari. Il **membro iSubItem** della struttura [**LVITEM**](/windows/win32/api/commctrl/ns-commctrl-lvitema) deve essere zero. Per informazioni sull'impostazione degli elementi secondari, vedere [**LVM \_ SETITEM.**](lvm-setitem.md)

Se per un controllo visualizzazione elenco è impostato lo stile [**LVS \_ EX \_ CHECKBOXES,**](extended-list-view-styles.md) qualsiasi  valore inserito nei bit da 12 a 15 del membro dello stato della struttura [**LVITEM**](/windows/win32/api/commctrl/ns-commctrl-lvitema) verrà ignorato. Quando un elemento viene aggiunto con questo set di stili, verrà sempre impostato sullo stato deselezionato.

Se un controllo visualizzazione elenco ha lo stile di finestra [**LVS \_ SORTASCENDING**](list-view-window-styles.md) o [**LVS \_ SORTDESCENDING,**](list-view-window-styles.md) un messaggio **LVM \_ INSERTITEM** avrà esito negativo se si tenta di inserire un elemento con LPSTR TEXTCALLBACK come valore per il relativo membro \_ **pszText.**

Il **messaggio LVM \_ INSERTITEM** inserirà il nuovo elemento nella posizione appropriata nell'ordinamento se sono presenti le condizioni seguenti:

-   Si usa uno degli stili LVS \_ SORTXXX.
-   Non si usa lo stile [**LVS \_ OWNERDRAW.**](list-view-window-styles.md)
-   Il **membro pszText** della struttura a cui punta **pitem** non è impostato su LPSTR \_ TEXTCALLBACK.

Se la [**struttura LVITEM**](/windows/win32/api/commctrl/ns-commctrl-lvitema) non contiene LVIF GROUPID nel membro mask, il valore del membro \_ **iGroupId** è I  \_ GROUPIDCALLBACK per impostazione predefinita.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop server 2003 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |
| Nomi Unicode e ANSI<br/>   | **LVM \_ INSERTITEMW** (Unicode) e **LVM \_ INSERTITEMA** (ANSI)<br/>             |



 

 





