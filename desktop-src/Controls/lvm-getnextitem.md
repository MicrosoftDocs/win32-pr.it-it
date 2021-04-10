---
title: Messaggio LVM_GETNEXTITEM (COMmctrl. h)
description: Cerca un elemento della visualizzazione elenco con le proprietà specificate e porta la relazione specificata con un elemento specificato. È possibile inviare questo messaggio in modo esplicito o usando la \_ macro GetNextItem di ListView.
ms.assetid: 2d458f12-b9d3-4b9e-bcb4-927c14c16537
keywords:
- Controlli di Windows Message LVM_GETNEXTITEM
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
ms.openlocfilehash: e7c4282ebf3572587dd5c8b8b3df1906a51a920e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964740"
---
# <a name="lvm_getnextitem-message"></a>\_Messaggio GETNEXTITEM LVM

Cerca un elemento della visualizzazione elenco con le proprietà specificate e porta la relazione specificata con un elemento specificato. È possibile inviare questo messaggio in modo esplicito o usando la macro [**\_ GetNextItem di ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getnextitem) .

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Indice dell'elemento da cui iniziare la ricerca oppure-1 per trovare il primo elemento che corrisponde ai flag specificati. L'elemento specificato è escluso dalla ricerca.

</dd> <dt>

*lParam* 
</dt> <dd>

Specifica la relazione con l'elemento specificato in *wParam*. Può trattarsi di una o di una combinazione dei valori seguenti:



| Valore                                                                                                                                                                                                                                                             | Significato                                                                                                                                                                                                                                                                                                                                                                                                                                               |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt></dt><dt>Esegue la ricerca in base all'indice.</dt> </dl>                                                                                                               |                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| <span id="_______________LVNI_ALL"></span><span id="_______________lvni_all"></span><dl> <dt> **LVNI \_ tutto**</dt><dt></dt> </dl>                               | Cerca un elemento successivo in base all'indice, il valore predefinito.<br/>                                                                                                                                                                                                                                                                                                                                                                                |
| <span id="_______________LVNI_PREVIOUS"></span><span id="_______________lvni_previous"></span><dl> <dt> **LVNI \_ precedente**</dt><dt></dt> </dl>                | **Windows Vista e versioni successive:** Cerca un elemento ordinato prima dell'elemento specificato in *wParam*. Il \_ flag precedente LVNI non è direzionale (LVNI precedente troverà \_ l'elemento posizionato in precedenza, mentre LVNI \_ precedente troverà l'elemento ordinato in precedenza). Il \_ flag precedente LVNI inverte fondamentalmente la logica della ricerca eseguita dai messaggi **LVM \_ GETNEXTITEM** o [**LVM \_ GETNEXTITEMINDEX**](lvm-getnextitemindex.md) .<br/> |
| <dl> <dt></dt><dt>Cerca per relazione fisica con l'indice dell'elemento da cui iniziare la ricerca.</dt> </dl>                                         |                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| <span id="_______________LVNI_ABOVE"></span><span id="_______________lvni_above"></span><dl> <dt> **LVNI \_ sopra**</dt><dt></dt> </dl>                         | Cerca un elemento che si trova sopra l'elemento specificato.<br/>                                                                                                                                                                                                                                                                                                                                                                                     |
| <span id="_______________LVNI_BELOW"></span><span id="_______________lvni_below"></span><dl> <dt> **LVNI di \_ seguito**</dt><dt></dt> </dl>                         | Cerca un elemento che si trova sotto l'elemento specificato.<br/>                                                                                                                                                                                                                                                                                                                                                                                     |
| <span id="_______________LVNI_TOLEFT"></span><span id="_______________lvni_toleft"></span><dl> <dt> **LVNI \_ ToLeft**</dt><dt></dt> </dl>                      | Cerca un elemento a sinistra dell'elemento specificato.<br/>                                                                                                                                                                                                                                                                                                                                                                                    |
| <span id="_______________LVNI_TORIGHT"></span><span id="_______________lvni_toright"></span><dl> <dt> **LVNI \_ ToRight**</dt><dt></dt> </dl>                   | Cerca un elemento a destra dell'elemento specificato.<br/>                                                                                                                                                                                                                                                                                                                                                                                   |
| <span id="_______________LVNI_DIRECTIONMASK"></span><span id="_______________lvni_directionmask"></span><dl> <dt> **\_ DIRECTIONMASK LVNI**</dt><dt></dt> </dl> | **Windows Vista e versioni successive:** Una maschera di flag direzionale con un valore come segue: LVNI \_ sopra \| LVNI \_ sotto \| LVNI \_ ToLeft \| LVNI \_ ToRight.<br/>                                                                                                                                                                                                                                                                                                   |
| <dl> <dt></dt><dt>Lo stato dell'elemento da trovare può essere specificato con uno o una combinazione dei valori seguenti:</dt> </dl>                                |                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| <span id="_______________LVNI_CUT"></span><span id="_______________lvni_cut"></span><dl> <dt> **\_ taglia LVNI**</dt><dt></dt> </dl>                               | Per l'elemento è impostato il flag di stato [**lvis \_ Cut**](list-view-item-states.md) .<br/>                                                                                                                                                                                                                                                                                                                                                       |
| <span id="_______________LVNI_DROPHILITED"></span><span id="_______________lvni_drophilited"></span><dl> <dt> **\_ DROPHILITED LVNI**</dt><dt></dt> </dl>       | Per l'elemento è stato impostato il flag di stato [**\_ DROPHILITED lvis**](list-view-item-states.md)<br/>                                                                                                                                                                                                                                                                                                                                        |
| <span id="_______________LVNI_FOCUSED"></span><span id="_______________lvni_focused"></span><dl> <dt> **LVNI \_**</dt> con stato attivo <dt></dt> </dl>                   | Per l'elemento è impostato il flag di stato [**\_ Focused di lvis**](list-view-item-states.md) .<br/>                                                                                                                                                                                                                                                                                                                                               |
| <span id="_______________LVNI_SELECTED"></span><span id="_______________lvni_selected"></span><dl> <dt> **LVNI \_ selezionato**</dt><dt></dt> </dl>                | Per l'elemento è stato impostato il flag di stato [**\_ selezionato lvis**](list-view-item-states.md) .<br/>                                                                                                                                                                                                                                                                                                                                             |
| <span id="_______________LVNI_STATEMASK"></span><span id="_______________lvni_statemask"></span><dl> <dt> **\_ STATEMASK LVNI**</dt><dt></dt> </dl>             | **Windows Vista e versioni successive:** Maschera di flag di stato con valore come segue: LVNI con stato \_ attivo \| LVNI \_ selezionato \| LVNI \_ Taglia \| LVNI \_ DROPHILITED.<br/>                                                                                                                                                                                                                                                                                                   |
| <dl> <dt></dt><dt>Cerca per aspetto degli elementi o per gruppo</dt> </dl>                                                                                      |                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| <span id="_______________LVNI_VISIBLEORDER"></span><span id="_______________lvni_visibleorder"></span><dl> <dt> **\_ VISIBLEORDER LVNI**</dt><dt></dt> </dl>    | **Windows Vista e versioni successive:** Eseguire una ricerca nell'ordine visibile.<br/>                                                                                                                                                                                                                                                                                                                                                                                     |
| <span id="_______________LVNI_VISIBLEONLY"></span><span id="_______________lvni_visibleonly"></span><dl> <dt> **\_ VISIBLEONLY LVNI**</dt><dt></dt> </dl>       | **Windows Vista e versioni successive:** Cerca gli elementi visibili.<br/>                                                                                                                                                                                                                                                                                                                                                                                     |
| <span id="_______________LVNI_SAMEGROUPONLY"></span><span id="_______________lvni_samegrouponly"></span><dl> <dt> **\_ SAMEGROUPONLY LVNI**</dt><dt></dt> </dl> | **Windows Vista e versioni successive:** Eseguire una ricerca nel gruppo corrente.<br/>                                                                                                                                                                                                                                                                                                                                                                                     |
| <dl> <dt></dt><dt>Se per un elemento non sono impostati tutti i flag di stato specificati, la ricerca prosegue con l'elemento successivo.</dt> </dl>                          |                                                                                                                                                                                                                                                                                                                                                                                                                                                       |



 

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce l'indice dell'elemento successivo se ha esito positivo oppure-1 in caso contrario.

## <a name="remarks"></a>Commenti

Si noti che i flag seguenti, da utilizzare solo con Windows Vista, si escludono a vicenda da eventuali altri flag in uso: LVNI \_ VISIBLEONLY, LVNI \_ SAMEGROUPONLY, LVNI VISIBLEORDER \_ , LVNI \_ DIRECTIONMASK e LVNI STATEMASK \_ .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





