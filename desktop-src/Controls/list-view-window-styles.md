---
title: List-View stili della finestra (CommCtrl.h)
description: Gli stili di finestra seguenti sono specifici dei controlli di visualizzazione elenco.
ms.assetid: 8b57239b-112e-4fb6-b394-15501bd3f5b3
topic_type:
- apiref
api_name:
- LVS_ALIGNLEFT
- LVS_ALIGNMASK
- LVS_ALIGNTOP
- LVS_AUTOARRANGE
- LVS_EDITLABELS
- LVS_ICON
- LVS_LIST
- LVS_NOCOLUMNHEADER
- LVS_NOLABELWRAP
- LVS_NOSCROLL
- LVS_NOSORTHEADER
- LVS_OWNERDATA
- LVS_OWNERDRAWFIXED
- LVS_REPORT
- LVS_SHAREIMAGELISTS
- LVS_SHOWSELALWAYS
- LVS_SINGLESEL
- LVS_SMALLICON
- LVS_SORTASCENDING
- LVS_SORTDESCENDING
- LVS_TYPEMASK
- LVS_TYPESTYLEMASK
api_location:
- CommCtrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f3e326f4508d08f1052747e64ea5eba184f45f7e73a1cb55539255a27fd8c8c6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118412026"
---
# <a name="list-view-window-styles"></a>List-View stili delle finestre

Gli stili di finestra seguenti sono specifici dei controlli di visualizzazione elenco.



| Costante                                                                                                                                                                        | Descrizione                                                                                                                                                                                                                                                                                                                                                 |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="LVS_ALIGNLEFT"></span><span id="lvs_alignleft"></span><dl> <dt>**LVS \_ ALIGNLEFT**</dt> </dl>                   | Gli elementi sono allineati a sinistra nella visualizzazione icona e icona piccola. <br/>                                                                                                                                                                                                                                                                                             |
| <span id="LVS_ALIGNMASK"></span><span id="lvs_alignmask"></span><dl> <dt>**LVS \_ ALIGNMASK**</dt> </dl>                   | Allineamento corrente del controllo. <br/>                                                                                                                                                                                                                                                                                                                |
| <span id="LVS_ALIGNTOP"></span><span id="lvs_aligntop"></span><dl> <dt>**LVS \_ ALIGNTOP**</dt> </dl>                      | Gli elementi sono allineati con la parte superiore del controllo visualizzazione elenco nella visualizzazione icona e nella visualizzazione icona piccola. <br/>                                                                                                                                                                                                                                                            |
| <span id="LVS_AUTOARRANGE"></span><span id="lvs_autoarrange"></span><dl> <dt>**LVS \_ AUTOARRANGE**</dt> </dl>             | Le icone vengono automaticamente disposte nella visualizzazione icona e icona piccola. <br/>                                                                                                                                                                                                                                                                              |
| <span id="LVS_EDITLABELS"></span><span id="lvs_editlabels"></span><dl> <dt>**LVS \_ EDITLABELS**</dt> </dl>                | Il testo dell'elemento può essere modificato sul posto. La finestra padre deve elaborare il [codice di notifica \_ LVN ENDLABELEDIT.](lvn-endlabeledit.md) <br/>                                                                                                                                                                                                               |
| <span id="LVS_ICON"></span><span id="lvs_icon"></span><dl> <dt>**ICONA DI \_ LVS**</dt> </dl>                                  | Questo stile specifica la visualizzazione icona. <br/>                                                                                                                                                                                                                                                                                                                 |
| <span id="LVS_LIST"></span><span id="lvs_list"></span><dl> <dt>**LVS \_ LIST**</dt> </dl>                                  | Questo stile specifica la visualizzazione elenco. <br/>                                                                                                                                                                                                                                                                                                                 |
| <span id="LVS_NOCOLUMNHEADER"></span><span id="lvs_nocolumnheader"></span><dl> <dt>**LVS \_ NOCOLUMNHEADER**</dt> </dl>    | Le intestazioni di colonna non vengono visualizzate nella visualizzazione report. Per impostazione predefinita, le colonne hanno intestazioni nella visualizzazione report. <br/>                                                                                                                                                                                                                                               |
| <span id="LVS_NOLABELWRAP"></span><span id="lvs_nolabelwrap"></span><dl> <dt>**LVS \_ NOLABELWRAP**</dt> </dl>             | Il testo dell'elemento viene visualizzato su una singola riga nella visualizzazione icona. Per impostazione predefinita, il testo dell'elemento può essere a capo nella visualizzazione icona. <br/>                                                                                                                                                                                                                                              |
| <span id="LVS_NOSCROLL"></span><span id="lvs_noscroll"></span><dl> <dt>**LVS \_ NOSCROLL**</dt> </dl>                      | Lo scorrimento è disabilitato. Tutti gli elementi devono essere all'interno dell'area client. Questo stile non è compatibile con gli stili **LVS \_ LIST** o **LVS \_ REPORT.** Per altre Knowledge Base, vedere l'articolo Q137520. <br/>                                                                                                                                      |
| <span id="LVS_NOSORTHEADER"></span><span id="lvs_nosortheader"></span><dl> <dt>**LVS \_ NOSORTHEADER**</dt> </dl>          | Le intestazioni di colonna non funzionano come i pulsanti. Questo stile può essere utilizzato se facendo clic su un'intestazione di colonna nella visualizzazione report non viene eseguita un'azione, ad esempio l'ordinamento. <br/>                                                                                                                                                                                       |
| <span id="LVS_OWNERDATA"></span><span id="lvs_ownerdata"></span><dl> <dt>**LVS \_ OWNERDATA**</dt> </dl>                   | [Versione 4.70.](common-control-versions.md) Questo stile specifica un controllo di visualizzazione elenco virtuale. Per altre informazioni su questo stile di controllo elenco, vedere [About List-View Controls](list-view-controls-overview.md). <br/>                                                                                                                             |
| <span id="LVS_OWNERDRAWFIXED"></span><span id="lvs_ownerdrawfixed"></span><dl> <dt>**LVS \_ OWNERDRAWFIXED**</dt> </dl>    | La finestra proprietaria può disegnare elementi nella visualizzazione report. Il controllo visualizzazione elenco invia un [**messaggio \_ DRAWITEM WM**](wm-drawitem.md) per disegnare ogni elemento, non invia messaggi separati per ogni elemento secondario. Il **membro iItemData** della struttura [**DRAWITEMSTRUCT contiene**](/windows/win32/api/winuser/ns-winuser-drawitemstruct) i dati dell'elemento per l'elemento di visualizzazione elenco specificato. <br/> |
| <span id="LVS_REPORT"></span><span id="lvs_report"></span><dl> <dt>**LVS \_ REPORT**</dt> </dl>                            | Questo stile specifica la visualizzazione report. Quando si usa lo stile \_ LVS REPORT con un controllo di visualizzazione elenco, la prima colonna è sempre allineata a sinistra. Non è possibile utilizzare LVCFMT \_ RIGHT per modificare questo allineamento. Per altre informazioni sull'allineamento delle colonne, vedere [**LVCOLUMN.**](/windows/win32/api/commctrl/ns-commctrl-lvcolumna) <br/>                                                                      |
| <span id="LVS_SHAREIMAGELISTS"></span><span id="lvs_shareimagelists"></span><dl> <dt>**LVS \_ SHAREIMAGELISTS**</dt> </dl> | L'elenco di immagini non verrà eliminato quando il controllo viene eliminato definitivamente. Questo stile consente l'uso degli stessi elenchi di immagini con più controlli di visualizzazione elenco. <br/>                                                                                                                                                                                          |
| <span id="LVS_SHOWSELALWAYS"></span><span id="lvs_showselalways"></span><dl> <dt>**LVS \_ SHOWSELALWAYS**</dt> </dl>       | La selezione, se presente, viene sempre visualizzata, anche se il controllo non ha lo stato attivo. <br/>                                                                                                                                                                                                                                                            |
| <span id="LVS_SINGLESEL"></span><span id="lvs_singlesel"></span><dl> <dt>**LVS \_ SINGLESEL**</dt> </dl>                   | È possibile selezionare un solo elemento alla volta. Per impostazione predefinita, è possibile selezionare più elementi. <br/>                                                                                                                                                                                                                                                            |
| <span id="LVS_SMALLICON"></span><span id="lvs_smallicon"></span><dl> <dt>**LVS \_ SMALLICON**</dt> </dl>                   | Questo stile specifica la visualizzazione icona piccola. <br/>                                                                                                                                                                                                                                                                                                           |
| <span id="LVS_SORTASCENDING"></span><span id="lvs_sortascending"></span><dl> <dt>**LVS \_ SORTASCENDING**</dt> </dl>       | Gli indici degli elementi vengono ordinati in base al testo degli elementi in ordine crescente. <br/>                                                                                                                                                                                                                                                                                  |
| <span id="LVS_SORTDESCENDING"></span><span id="lvs_sortdescending"></span><dl> <dt>**LVS \_ SORTDESCENDING**</dt> </dl>    | Gli indici degli elementi vengono ordinati in base al testo dell'elemento in ordine decrescente. <br/>                                                                                                                                                                                                                                                                                 |
| <span id="LVS_TYPEMASK"></span><span id="lvs_typemask"></span><dl> <dt>**LVS \_ TYPEMASK**</dt> </dl>                      | Determina lo stile della finestra corrente del controllo. <br/>                                                                                                                                                                                                                                                                                                  |
| <span id="LVS_TYPESTYLEMASK"></span><span id="lvs_typestylemask"></span><dl> <dt>**LVS \_ TYPESTYLEMASK**</dt> </dl>       | Determina gli stili della finestra che controllano l'allineamento e il comportamento dell'intestazione e dell'elemento. <br/>                                                                                                                                                                                                                                                    |



## <a name="remarks"></a>Commenti

Per gli **stili LVS \_ SORTASCENDING** e **LVS \_ SORTDESCENDING,** gli indici degli elementi vengono ordinati rispettivamente in base al testo dell'elemento in ordine crescente o decrescente. Poiché le **viste LVS \_ LIST** e **LVS \_ REPORT** visualizzano gli elementi nello stesso ordine dei relativi indici, i risultati dell'ordinamento sono immediatamente visibili all'utente. Le **viste LVS \_ ICON** **e LVS \_ SMALLICON** non usano indici di elementi per determinare la posizione delle icone. Con queste visualizzazioni, i risultati dell'ordinamento non sono visibili all'utente.

È possibile usare la maschera **LVS \_ TYPEMASK** per isolare gli stili della finestra che corrispondono alla visualizzazione corrente: **LVS \_ ICON, LVS** **\_ LIST,** **LVS \_ REPORT** e **LVS \_ SMALLICON.**

È possibile usare la maschera **LVS \_ ALIGNMASK** per isolare gli stili della finestra che specificano l'allineamento degli elementi: **LVS \_ ALIGNLEFT** e **LVS \_ ALIGNTOP.**

È possibile usare la maschera **LVS \_ TYPESTYLEMASK** per isolare gli stili della finestra che controllano l'allineamento degli elementi (**LVS \_ ALIGNLEFT** e **LVS \_ ALIGNTOP**) e quelli che controllano l'aspetto e il comportamento dell'intestazione **(LVS \_ NOCOLUMNHEADER** e **LVS \_ NOSORTHEADER).**

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|---------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>CommCtrl.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Stili e visualizzazioni di visualizzazione elenco](list-view-controls-overview.md)
</dt> </dl>

 

 





