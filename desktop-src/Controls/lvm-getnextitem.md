---
title: LVM_GETNEXTITEM messaggio (Commctrl.h)
description: Cerca un elemento di visualizzazione elenco con le proprietà specificate e contiene la relazione specificata con un elemento specificato. È possibile inviare questo messaggio in modo esplicito o tramite la \_ macro ListView GetNextItem.
ms.assetid: 2d458f12-b9d3-4b9e-bcb4-927c14c16537
keywords:
- LVM_GETNEXTITEM dei messaggi Windows controlli
topic_type:
- apiref
api_name:
- LVM_GETNEXTITEM
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 40e8e6fdf068f06176d6965a2fb885b349a74ea5cde73c5952d16d7c76512ae8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120002561"
---
# <a name="lvm_getnextitem-message"></a>Messaggio LVM \_ GETNEXTITEM

Cerca un elemento di visualizzazione elenco con le proprietà specificate e contiene la relazione specificata con un elemento specificato. È possibile inviare questo messaggio in modo esplicito o tramite la macro [**\_ ListView GetNextItem.**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getnextitem)

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Indice dell'elemento con cui iniziare la ricerca oppure -1 per trovare il primo elemento che corrisponde ai flag specificati. L'elemento specificato stesso viene escluso dalla ricerca.

</dd> <dt>

*lParam* 
</dt> <dd>

Specifica la relazione con l'elemento specificato in *wParam*. Può essere uno o una combinazione dei valori seguenti:



| Valore                                                                                                                                                                                                                                                             | Significato                                                                                                                                                                                                                                                                                                                                                                                                                                               |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt></dt><dt>Esegue la ricerca in base all'indice.</dt> </dl>                                                                                                               |                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| <span id="_______________LVNI_ALL"></span><span id="_______________lvni_all"></span><dl> <dt> **LVNI \_ ALL**</dt><dt></dt> </dl>                               | Cerca un elemento successivo in base all'indice, il valore predefinito.<br/>                                                                                                                                                                                                                                                                                                                                                                                |
| <span id="_______________LVNI_PREVIOUS"></span><span id="_______________lvni_previous"></span><dl> <dt> **LVNI \_ PRECEDENTE**</dt><dt></dt> </dl>                | **Windows Vista e versioni successive:** Cerca un elemento ordinato prima dell'elemento specificato in *wParam*. Il flag LVNI PREVIOUS non è direzionale (LVNI ABOVE troverà l'elemento posizionato sopra, mentre LVNI PREVIOUS troverà l'elemento ordinato \_ \_ in \_ precedenza). Il flag LVNI PREVIOUS inverte fondamentalmente la logica della ricerca eseguita dai messaggi \_ **LVM \_ GETNEXTITEM** o [**LVM \_ GETNEXTITEMINDEX.**](lvm-getnextitemindex.md)<br/> |
| <dl> <dt></dt><dt>Cerca in base alla relazione fisica con l'indice dell'elemento in cui deve iniziare la ricerca.</dt> </dl>                                         |                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| <span id="_______________LVNI_ABOVE"></span><span id="_______________lvni_above"></span><dl> <dt> **LVNI \_ PRECEDENTE**</dt><dt></dt> </dl>                         | Cerca un elemento che si trova sopra l'elemento specificato.<br/>                                                                                                                                                                                                                                                                                                                                                                                     |
| <span id="_______________LVNI_BELOW"></span><span id="_______________lvni_below"></span><dl> <dt> **LVNI \_ DI SEGUITO**</dt><dt></dt> </dl>                         | Cerca un elemento che si trova sotto l'elemento specificato.<br/>                                                                                                                                                                                                                                                                                                                                                                                     |
| <span id="_______________LVNI_TOLEFT"></span><span id="_______________lvni_toleft"></span><dl> <dt> **LVNI \_ TOLEFT**</dt><dt></dt> </dl>                      | Cerca un elemento a sinistra dell'elemento specificato.<br/>                                                                                                                                                                                                                                                                                                                                                                                    |
| <span id="_______________LVNI_TORIGHT"></span><span id="_______________lvni_toright"></span><dl> <dt> **LVNI \_ TORIGHT**</dt><dt></dt> </dl>                   | Cerca un elemento a destra dell'elemento specificato.<br/>                                                                                                                                                                                                                                                                                                                                                                                   |
| <span id="_______________LVNI_DIRECTIONMASK"></span><span id="_______________lvni_directionmask"></span><dl> <dt> **LVNI \_ DIRECTIONMASK**</dt><dt></dt> </dl> | **Windows Vista e versioni successive:** Maschera di flag direzionale con valore come \_ segue: LVNI ABOVE \| LVNI \_ BELOW \| LVNI \_ TOLEFT \| LVNI \_ TORIGHT.<br/>                                                                                                                                                                                                                                                                                                   |
| <dl> <dt></dt><dt>Lo stato dell'elemento da trovare può essere specificato con uno o una combinazione dei valori seguenti:</dt> </dl>                                |                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| <span id="_______________LVNI_CUT"></span><span id="_______________lvni_cut"></span><dl> <dt> **LVNI \_ CUT**</dt><dt></dt> </dl>                               | Per l'elemento è impostato il flag di stato [**LVIS \_ CUT.**](list-view-item-states.md)<br/>                                                                                                                                                                                                                                                                                                                                                       |
| <span id="_______________LVNI_DROPHILITED"></span><span id="_______________lvni_drophilited"></span><dl> <dt> **LVNI \_ DROPHILITED**</dt><dt></dt> </dl>       | Per l'elemento è impostato il flag di stato [**LVIS \_ DROPHILITED**](list-view-item-states.md)<br/>                                                                                                                                                                                                                                                                                                                                        |
| <span id="_______________LVNI_FOCUSED"></span><span id="_______________lvni_focused"></span><dl> <dt> **LVNI \_ INCENTRATO**</dt><dt></dt> </dl>                   | Per l'elemento è impostato il flag di stato [**\_ LVIS FOCUSED.**](list-view-item-states.md)<br/>                                                                                                                                                                                                                                                                                                                                               |
| <span id="_______________LVNI_SELECTED"></span><span id="_______________lvni_selected"></span><dl> <dt> **LVNI \_ SELEZIONATO**</dt><dt></dt> </dl>                | Per l'elemento è impostato il flag di stato [**LVIS \_ SELECTED.**](list-view-item-states.md)<br/>                                                                                                                                                                                                                                                                                                                                             |
| <span id="_______________LVNI_STATEMASK"></span><span id="_______________lvni_statemask"></span><dl> <dt> **LVNI \_ STATEMASK**</dt><dt></dt> </dl>             | **Windows Vista e versioni successive:** Maschera del flag di stato con valore come \_ segue: LVNI FOCUSED \| LVNI \_ SELECTED \| LVNI \_ CUT \| LVNI \_ DROPHILITED.<br/>                                                                                                                                                                                                                                                                                                   |
| <dl> <dt></dt><dt>Cerca in base all'aspetto degli elementi o al gruppo</dt> </dl>                                                                                      |                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| <span id="_______________LVNI_VISIBLEORDER"></span><span id="_______________lvni_visibleorder"></span><dl> <dt> **LVNI \_ VISIBLEORDER**</dt><dt></dt> </dl>    | **Windows Vista e versioni successive:** Cercare l'ordine visibile.<br/>                                                                                                                                                                                                                                                                                                                                                                                     |
| <span id="_______________LVNI_VISIBLEONLY"></span><span id="_______________lvni_visibleonly"></span><dl> <dt> **LVNI \_ VISIBLEONLY**</dt><dt></dt> </dl>       | **Windows Vista e versioni successive:** Cercare gli elementi visibili.<br/>                                                                                                                                                                                                                                                                                                                                                                                     |
| <span id="_______________LVNI_SAMEGROUPONLY"></span><span id="_______________lvni_samegrouponly"></span><dl> <dt> **LVNI \_ SAMEGROUPONLY**</dt><dt></dt> </dl> | **Windows Vista e versioni successive:** Cercare il gruppo corrente.<br/>                                                                                                                                                                                                                                                                                                                                                                                     |
| <dl> <dt></dt><dt>Se per un elemento non sono impostati tutti i flag di stato specificati, la ricerca continua con l'elemento successivo.</dt> </dl>                          |                                                                                                                                                                                                                                                                                                                                                                                                                                                       |



 

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce l'indice dell'elemento successivo in caso di esito positivo oppure -1 in caso contrario.

## <a name="remarks"></a>Commenti

Si noti che i flag seguenti, da usare solo con Windows Vista, si escludono a vicenda di qualsiasi altro flag in uso: \_ LVNI VISIBLEONLY, LVNI \_ SAMEGROUPONLY, LVNI \_ VISIBLEORDER, LVNI \_ DIRECTIONMASK e LVNI \_ STATEMASK.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop server 2003 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





