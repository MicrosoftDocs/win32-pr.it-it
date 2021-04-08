---
title: Messaggio TVM_SELECTITEM (COMmctrl. h)
description: Seleziona l'elemento della visualizzazione struttura ad albero specificato, scorre l'elemento nella visualizzazione o ridisegna l'elemento nello stile usato per indicare la destinazione di un'operazione di trascinamento della selezione.
ms.assetid: 8b943958-7b93-4e54-99de-200121cf0752
keywords:
- Controlli di Windows Message TVM_SELECTITEM
topic_type:
- apiref
api_name:
- TVM_SELECTITEM
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 94862b64a02cd8972e3da38a75282d99bbc1cbc8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103873473"
---
# <a name="tvm_selectitem-message"></a>\_Messaggio SELECTITEM TVM

Seleziona l'elemento della visualizzazione struttura ad albero specificato, scorre l'elemento nella visualizzazione o ridisegna l'elemento nello stile usato per indicare la destinazione di un'operazione di trascinamento della selezione. È possibile inviare questo messaggio in modo esplicito o usando la macro TreeView [**\_ Select**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_select), [**TreeView \_ SelectItem**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_selectitem)o [**TreeView \_ SelectDropTarget**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_selectdroptarget) .

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Flag di azione. Questo parametro può essere uno dei valori seguenti:



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Valore</th>
<th>Significato</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span id="TVGN_CARET"></span><span id="tvgn_caret"></span><dl> <dt><strong>TVGN_CARET</strong></dt> </dl></td>
<td>Imposta la selezione sull'elemento specificato. La finestra padre del controllo visualizzazione struttura ad albero riceve i codici di notifica <a href="tvn-selchanging.md">TVN_SELCHANGING</a> e <a href="tvn-selchanged.md">TVN_SELCHANGED</a> . <br/></td>
</tr>
<tr class="even">
<td><span id="TVGN_DROPHILITE"></span><span id="tvgn_drophilite"></span><dl> <dt><strong>TVGN_DROPHILITE</strong></dt> </dl></td>
<td>Ridisegna l'elemento specificato nello stile usato per indicare la destinazione di un'operazione di trascinamento della selezione.<br/></td>
</tr>
<tr class="odd">
<td><span id="TVGN_FIRSTVISIBLE"></span><span id="tvgn_firstvisible"></span><dl> <dt><strong>TVGN_FIRSTVISIBLE</strong></dt> </dl></td>
<td>Assicura che l'elemento specificato sia visibile e, se possibile, lo Visualizza nella parte superiore della finestra del controllo. I controlli di visualizzazione albero visualizzano tutti gli elementi che rientrano nella finestra. Se l'elemento specificato si trova nella parte inferiore della gerarchia di elementi del controllo, potrebbe non diventare il primo elemento visibile, a seconda del numero di elementi che rientrano nella finestra.<br/></td>
</tr>
<tr class="even">
<td><span id="TVSI_NOSINGLEEXPAND"></span><span id="tvsi_nosingleexpand"></span><dl> <dt><strong>TVSI_NOSINGLEEXPAND</strong></dt> </dl></td>
<td>Quando viene selezionato un singolo elemento, verifica che TreeView non espanda gli elementi figlio di tale elemento. Questo valore è valido solo se utilizzato con il flag TVGN_CARET. <br/>
<blockquote>
[!Note]<br />
Per usare questo flag, è necessario fornire un manifesto che specifichi Comclt32.dll versione 6,0. Per altre informazioni sui manifesti, vedere <a href="cookbook-overview.md">Abilitazione degli stili di visualizzazione</a>.
</blockquote>
<br/></td>
</tr>
</tbody>
</table>



 

</dd> <dt>

*lParam* 
</dt> <dd>

Handle per un elemento. Se *lParam* è **null**, il controllo è impostato su non è selezionato alcun elemento.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce **true** se l'operazione ha esito positivo o **false** in caso contrario.

## <a name="remarks"></a>Commenti

Se l'elemento specificato è figlio di un elemento padre compresso, l'elenco di elementi figlio dell'elemento padre viene espanso per rivelare l'elemento specificato. In questo caso, la finestra padre del controllo riceve i codici di notifica di [TVN \_ ITEMEXPANDING](tvn-itemexpanding.md) e [TVN \_ ITEMEXPANDED](tvn-itemexpanded.md) .

L'uso della macro [**\_ SelectItem di TreeView**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_selectitem) equivale a inviare il messaggio di **\_ SelectItem TVM** con *wParam* impostato sul valore di punto di \_ inserimento TVGN. L'uso della macro [**\_ SelectDropTarget di TreeView**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_selectdroptarget) equivale a inviare il messaggio di **\_ SELECTITEM TVM** con *wParam* impostato sul \_ valore DROPHILITE di TVGN. L'uso di [**TreeView \_ SelectSetFirstVisible**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_selectsetfirstvisible) equivale all'invio del messaggio **\_ SELECTITEM TVM** con *wParam* impostato sul \_ valore FIRSTVISIBLE di TVGN.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





