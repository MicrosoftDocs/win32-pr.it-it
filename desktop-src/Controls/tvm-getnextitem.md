---
title: TVM_GETNEXTITEM messaggio (Commctrl.h)
description: Recupera l'elemento della visualizzazione albero che contiene la relazione specificata con un elemento specificato. È possibile inviare questo messaggio in modo esplicito usando la macro TreeView \_ GetNextItem.
ms.assetid: 505c713c-7728-4119-bc0e-482fe7e73193
keywords:
- TVM_GETNEXTITEM dei messaggi Windows controlli
topic_type:
- apiref
api_name:
- TVM_GETNEXTITEM
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 84dbbd39ca347bcf1084ddfaa46c997cc5c4e5dd4d52250136a230dd834ac836
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119698681"
---
# <a name="tvm_getnextitem-message"></a>Messaggio TVM \_ GETNEXTITEM

Recupera l'elemento della visualizzazione albero che contiene la relazione specificata con un elemento specificato. È possibile inviare questo messaggio in modo esplicito usando la macro [**TreeView \_ GetNextItem.**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getnextitem)

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Flag che specifica l'elemento da recuperare. Questo parametro può essere uno dei valori seguenti:



| Valore                                                                                                                                                                              | Significato                                                                                                                                                                                                                                                                                                                        |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TVGN_CARET"></span><span id="tvgn_caret"></span><dl> <dt>**TVGN \_ CARET**</dt> </dl>                               | Recupera l'elemento attualmente selezionato. È possibile usare la macro [**TreeView \_ GetSelection**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getselection) per inviare questo messaggio.<br/>                                                                                                                                                                          |
| <span id="TVGN_CHILD"></span><span id="tvgn_child"></span><dl> <dt>**TVGN \_ CHILD**</dt> </dl>                               | Recupera il primo elemento figlio dell'elemento specificato dal *parametro hitem.* È possibile usare la macro [**TreeView \_ GetChild**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getchild) per inviare questo messaggio.<br/>                                                                                                                                          |
| <span id="TVGN_DROPHILITE"></span><span id="tvgn_drophilite"></span><dl> <dt>**TVGN \_ DROPHILITE**</dt> </dl>                | Recupera l'elemento che rappresenta la destinazione di un'operazione di trascinamento della selezione. È possibile usare la macro [**TreeView \_ GetDropHilight**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getdrophilight) per inviare questo messaggio.<br/>                                                                                                                                         |
| <span id="TVGN_FIRSTVISIBLE"></span><span id="tvgn_firstvisible"></span><dl> <dt>**TVGN \_ FIRSTVISIBLE**</dt> </dl>          | Recupera il primo elemento visibile nella finestra di visualizzazione albero. È possibile usare la macro [**TreeView \_ GetFirstVisible**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getfirstvisible) per inviare questo messaggio.<br/>                                                                                                                                         |
| <span id="TVGN_LASTVISIBLE"></span><span id="tvgn_lastvisible"></span><dl> <dt>**TVGN \_ LASTVISIBLE**</dt> </dl>             | [Versione 4.71](common-control-versions.md). Recupera l'ultimo elemento espanso nell'albero. In questo modo non viene recuperato l'ultimo elemento visibile nella finestra di visualizzazione albero. È possibile usare la macro [**TreeView \_ GetLastVisible**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getlastvisible) per inviare questo messaggio.<br/>                                            |
| <span id="TVGN_NEXT"></span><span id="tvgn_next"></span><dl> <dt>**TVGN \_ NEXT**</dt> </dl>                                  | Recupera l'elemento di pari livello successivo. È possibile usare la macro [**TreeView \_ GetNextSibling**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getnextsibling) per inviare questo messaggio.<br/>                                                                                                                                                                            |
| <span id="TVGN_NEXTSELECTED"></span><span id="tvgn_nextselected"></span><dl> <dt>**TVGN \_ NEXTSELECTED**</dt> </dl>          | **Windows Vista e versioni successive.** Recupera il successivo elemento selezionato. È possibile usare la macro [**TreeView \_ GetNextSelected**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getnextselected) per inviare questo messaggio.<br/>                                                                                                                                            |
| <span id="TVGN_NEXTVISIBLE"></span><span id="tvgn_nextvisible"></span><dl> <dt>**TVGN \_ NEXTVISIBLE**</dt> </dl>             | Recupera l'elemento visibile successivo che segue l'elemento specificato. L'elemento specificato deve essere visibile. Usare il [**messaggio TVM \_ GETITEMRECT**](tvm-getitemrect.md) per determinare se un elemento è visibile. È possibile usare la macro [**TreeView \_ GetNextVisible**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getnextvisible) per inviare questo messaggio.<br/>   |
| <span id="TVGN_PARENT"></span><span id="tvgn_parent"></span><dl> <dt>**PADRE \_ DI TVGN**</dt> </dl>                            | Recupera l'elemento padre dell'elemento specificato. È possibile usare la macro [**TreeView \_ GetParent**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getparent) per inviare questo messaggio.<br/>                                                                                                                                                                           |
| <span id="TVGN_PREVIOUS"></span><span id="tvgn_previous"></span><dl> <dt>**TVGN \_ PREVIOUS**</dt> </dl>                      | Recupera l'elemento di pari livello precedente. È possibile usare la macro [**\_ GetPrevSibling**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getprevsibling) di TreeView per inviare questo messaggio.<br/>                                                                                                                                                                        |
| <span id="TVGN_PREVIOUSVISIBLE"></span><span id="tvgn_previousvisible"></span><dl> <dt>**TVGN \_ PREVIOUSVISIBLE**</dt> </dl> | Recupera il primo elemento visibile che precede l'elemento specificato. L'elemento specificato deve essere visibile. Usare il [**messaggio TVM \_ GETITEMRECT**](tvm-getitemrect.md) per determinare se un elemento è visibile. È possibile usare la macro [**TreeView \_ GetPrevVisible**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getprevvisible) per inviare questo messaggio.<br/> |
| <span id="TVGN_ROOT"></span><span id="tvgn_root"></span><dl> <dt>**RADICE DI \_ TVGN**</dt> </dl>                                  | Recupera il primo elemento o il primo elemento del controllo di visualizzazione albero. È possibile usare la macro [**TreeView \_ GetRoot**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getroot) per inviare questo messaggio. <br/>                                                                                                                                                       |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Handle per un elemento.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce l'handle per l'elemento in caso di esito positivo. Nella maggior parte dei casi, il messaggio restituisce un **valore NULL** per indicare un errore. Vedere la sezione Osservazioni per informazioni dettagliate.

## <a name="remarks"></a>Commenti

Questo messaggio restituirà **NULL se** l'elemento recuperato è il nodo radice dell'albero. Ad esempio, se si usa questo messaggio con il flag TVGN PARENT su un elemento figlio di primo livello del nodo radice della visualizzazione albero, il messaggio \_ restituirà **NULL.**

È anche possibile usare una di queste macro correlate:



|                                                               |
|---------------------------------------------------------------|
| [**GetChild di TreeView \_**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getchild)               |
| [**GetDropHilight di TreeView \_**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getdrophilight)   |
| [**TreeView \_ GetFirstVisible**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getfirstvisible) |
| [**GetLastVisible di TreeView \_**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getlastvisible)   |
| [**GetNextSibling di TreeView \_**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getnextsibling)   |
| [**GetNextVisible di TreeView \_**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getnextvisible)   |
| [**GetParent di TreeView \_**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getparent)             |
| [**\_GetPrevSibling di TreeView**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getprevsibling)   |
| [**GetPrevVisible di TreeView \_**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getprevvisible)   |
| [**GetRoot di TreeView \_**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getroot)                 |
| [**GetSelection di TreeView \_**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getselection)       |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop server 2003 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





