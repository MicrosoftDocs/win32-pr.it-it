---
title: Messaggio TVM_GETNEXTITEM (COMmctrl. h)
description: Recupera l'elemento della visualizzazione struttura ad albero che presenta la relazione specificata con un elemento specificato. È possibile inviare questo messaggio in modo esplicito usando la \_ macro GetNextItem di TreeView.
ms.assetid: 505c713c-7728-4119-bc0e-482fe7e73193
keywords:
- Controlli di Windows Message TVM_GETNEXTITEM
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
ms.openlocfilehash: 3099af5e9abcd3e9c144cfc615a12dd2acb0332b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104119318"
---
# <a name="tvm_getnextitem-message"></a>\_Messaggio GETNEXTITEM TVM

Recupera l'elemento della visualizzazione struttura ad albero che presenta la relazione specificata con un elemento specificato. È possibile inviare questo messaggio in modo esplicito usando la [**macro \_ GetNextItem di TreeView**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getnextitem) .

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Flag che specifica l'elemento da recuperare. Questo parametro può essere uno dei valori seguenti:



| Valore                                                                                                                                                                              | Significato                                                                                                                                                                                                                                                                                                                        |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TVGN_CARET"></span><span id="tvgn_caret"></span><dl> <dt>**punto di \_ inserimento TVGN**</dt> </dl>                               | Recupera l'elemento attualmente selezionato. Per inviare questo messaggio, è possibile utilizzare la macro [**TreeView \_ GetSelection**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getselection) .<br/>                                                                                                                                                                          |
| <span id="TVGN_CHILD"></span><span id="tvgn_child"></span><dl> <dt>**TVGN \_ figlio**</dt> </dl>                               | Recupera il primo elemento figlio dell'elemento specificato dal parametro *hitet* . Per inviare questo messaggio, è possibile utilizzare la macro [**TreeView \_ GetChild**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getchild) .<br/>                                                                                                                                          |
| <span id="TVGN_DROPHILITE"></span><span id="tvgn_drophilite"></span><dl> <dt>**\_DROPHILITE TVGN**</dt> </dl>                | Recupera l'elemento che è la destinazione di un'operazione di trascinamento della selezione. È possibile usare la [**macro \_ GetDropHilight di TreeView**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getdrophilight) per inviare questo messaggio.<br/>                                                                                                                                         |
| <span id="TVGN_FIRSTVISIBLE"></span><span id="tvgn_firstvisible"></span><dl> <dt>**\_FIRSTVISIBLE TVGN**</dt> </dl>          | Recupera il primo elemento visibile nella finestra della visualizzazione albero. È possibile usare la [**macro \_ GetFirstVisible di TreeView**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getfirstvisible) per inviare questo messaggio.<br/>                                                                                                                                         |
| <span id="TVGN_LASTVISIBLE"></span><span id="tvgn_lastvisible"></span><dl> <dt>**\_LASTVISIBLE TVGN**</dt> </dl>             | [Versione 4,71](common-control-versions.md). Recupera l'ultimo elemento espanso nell'albero. L'ultimo elemento visualizzato nella finestra visualizzazione albero non viene recuperato. È possibile usare la [**macro \_ GetLastVisible di TreeView**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getlastvisible) per inviare questo messaggio.<br/>                                            |
| <span id="TVGN_NEXT"></span><span id="tvgn_next"></span><dl> <dt>**TVGN \_ successivo**</dt> </dl>                                  | Recupera l'elemento successivo di pari livello. È possibile usare la [**macro \_ GetNextSibling di TreeView**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getnextsibling) per inviare questo messaggio.<br/>                                                                                                                                                                            |
| <span id="TVGN_NEXTSELECTED"></span><span id="tvgn_nextselected"></span><dl> <dt>**\_NEXTSELECTED TVGN**</dt> </dl>          | **Windows Vista e versioni successive.** Recupera il successivo elemento selezionato. È possibile usare la [**macro \_ GetNextSelected di TreeView**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getnextselected) per inviare questo messaggio.<br/>                                                                                                                                            |
| <span id="TVGN_NEXTVISIBLE"></span><span id="tvgn_nextvisible"></span><dl> <dt>**\_NEXTVISIBLE TVGN**</dt> </dl>             | Recupera il successivo elemento visibile che segue l'elemento specificato. L'elemento specificato deve essere visibile. Usare il messaggio [**TVM \_ GETITEMRECT**](tvm-getitemrect.md) per determinare se un elemento è visibile. È possibile usare la [**macro \_ GetNextVisible di TreeView**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getnextvisible) per inviare questo messaggio.<br/>   |
| <span id="TVGN_PARENT"></span><span id="tvgn_parent"></span><dl> <dt>**TVGN \_ padre**</dt> </dl>                            | Recupera l'elemento padre dell'elemento specificato. Per inviare questo messaggio, è possibile utilizzare la macro [**TreeView \_ GetParent**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getparent) .<br/>                                                                                                                                                                           |
| <span id="TVGN_PREVIOUS"></span><span id="tvgn_previous"></span><dl> <dt>**TVGN \_ precedente**</dt> </dl>                      | Recupera l'elemento di pari livello precedente. È possibile usare la [**macro \_ GetPrevSibling di TreeView**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getprevsibling) per inviare questo messaggio.<br/>                                                                                                                                                                        |
| <span id="TVGN_PREVIOUSVISIBLE"></span><span id="tvgn_previousvisible"></span><dl> <dt>**\_PREVIOUSVISIBLE TVGN**</dt> </dl> | Recupera il primo elemento visibile che precede l'elemento specificato. L'elemento specificato deve essere visibile. Usare il messaggio [**TVM \_ GETITEMRECT**](tvm-getitemrect.md) per determinare se un elemento è visibile. È possibile usare la [**macro \_ GetPrevVisible di TreeView**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getprevvisible) per inviare questo messaggio.<br/> |
| <span id="TVGN_ROOT"></span><span id="tvgn_root"></span><dl> <dt>**\_radice TVGN**</dt> </dl>                                  | Recupera l'elemento superiore o molto primo del controllo di visualizzazione ad albero. È possibile utilizzare la macro [**TreeView \_ GetRoot**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getroot) per inviare questo messaggio. <br/>                                                                                                                                                       |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Handle per un elemento.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce l'handle dell'elemento in caso di esito positivo. Per la maggior parte dei casi, il messaggio restituisce un valore **null** per indicare un errore. Vedere la sezione Osservazioni per informazioni dettagliate.

## <a name="remarks"></a>Commenti

Questo messaggio restituirà **null** se l'elemento da recuperare è il nodo radice dell'albero. Se ad esempio si usa questo messaggio con il \_ flag padre TVGN su un figlio di primo livello del nodo radice della visualizzazione albero, il messaggio restituirà **null**.

È anche possibile usare una di queste macro correlate:



|                                                               |
|---------------------------------------------------------------|
| [**TreeView \_ GetChild**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getchild)               |
| [**\_GetDropHilight TreeView**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getdrophilight)   |
| [**\_GetFirstVisible TreeView**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getfirstvisible) |
| [**\_GetLastVisible TreeView**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getlastvisible)   |
| [**\_GetNextSibling TreeView**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getnextsibling)   |
| [**\_GetNextVisible TreeView**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getnextvisible)   |
| [**TreeView \_ GetParent**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getparent)             |
| [**\_GetPrevSibling TreeView**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getprevsibling)   |
| [**\_GetPrevVisible TreeView**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getprevvisible)   |
| [**TreeView \_ GetRoot**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getroot)                 |
| [**TreeView \_ GetSelection**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getselection)       |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





