---
title: Messaggio LVM_INSERTITEM (COMmctrl. h)
description: Inserisce un nuovo elemento in un controllo visualizzazione elenco. È possibile inviare questo messaggio in modo esplicito o usando la \_ macro ListView InsertItem.
ms.assetid: ac283e81-5b9f-4a90-acdb-fd7813c9cb84
keywords:
- Controlli di Windows Message LVM_INSERTITEM
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
ms.openlocfilehash: 467c6b595e307dc16f87e40da858ff8b120fb3f7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106302286"
---
# <a name="lvm_insertitem-message"></a>\_Messaggio INSERTITEM di LVM

Inserisce un nuovo elemento in un controllo visualizzazione elenco. È possibile inviare questo messaggio in modo esplicito o usando la macro [**ListView \_ InsertItem**](/windows/desktop/api/Commctrl/nf-commctrl-listview_insertitem) .

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>Deve essere zero.</dd> <dt>

*lParam* 
</dt> <dd>

Puntatore a una struttura [**LVITEM**](/windows/win32/api/commctrl/ns-commctrl-lvitema) che specifica gli attributi dell'elemento della visualizzazione elenco. Usare il membro **iItem** per specificare l'indice in base zero in corrispondenza del quale deve essere inserito il nuovo elemento. Se questo valore è maggiore del numero di elementi attualmente contenuti nel controllo ListView, il nuovo elemento verrà aggiunto alla fine dell'elenco e sarà assegnato l'indice corretto. Esaminare il valore restituito del messaggio per determinare l'indice effettivo assegnato all'elemento.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce l'indice del nuovo elemento, se ha esito positivo, oppure-1 in caso contrario.

## <a name="remarks"></a>Commenti

Non è possibile usare [**ListView \_ InsertItem**](/windows/desktop/api/Commctrl/nf-commctrl-listview_insertitem) o **LVM \_ InsertItem** per inserire elementi secondari. Il membro **iSubItem** della struttura [**LVITEM**](/windows/win32/api/commctrl/ns-commctrl-lvitema) deve essere zero. Per informazioni sull'impostazione degli elementi secondari, vedere l' [**\_ argomento LVM**](lvm-setitem.md) .

Se per un controllo di visualizzazione elenco è impostato lo stile [**LVS \_ ex \_**](extended-list-view-styles.md) , qualsiasi valore inserito in bit da 12 a 15 del membro di **stato** della struttura [**LVITEM**](/windows/win32/api/commctrl/ns-commctrl-lvitema) verrà ignorato. Quando viene aggiunto un elemento con questo set di stili, questo viene sempre impostato sullo stato deselezionato.

Se un controllo di visualizzazione elenco dispone dello stile della finestra [**LVS \_ SORTASCENDING**](list-view-window-styles.md) o [**LVS \_ SORTDESCENDING**](list-view-window-styles.md) , un **messaggio \_ INSERTITEM INSERTITEM** avrà esito negativo se si tenta di inserire un elemento con LPSTR TEXTCALLBACK \_ come valore per il relativo membro **pszText** .

Il **messaggio \_ INSERTITEM INSERTITEM** inserisce il nuovo elemento nella posizione corretta nell'ordinamento se si verificano le condizioni seguenti:

-   Si sta usando uno degli \_ stili SORTXXX di LVS.
-   Non si usa lo stile [**\_ OWNERDRAW di LVS**](list-view-window-styles.md) .
-   Il membro **pszText** della struttura a cui punta **pItem** non è impostato su LPSTR \_ TEXTCALLBACK.

Se la struttura [**LVITEM**](/windows/win32/api/commctrl/ns-commctrl-lvitema) non contiene LVIF \_ GROUPID nel membro **mask** , il valore del membro **iGroupId** è i \_ GROUPIDCALLBACK per impostazione predefinita.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |
| Nomi Unicode e ANSI<br/>   | **LVM \_ INSERTITEMW** (Unicode) e **LVM \_ INSERTITEMA** (ANSI)<br/>             |



 

 





