---
title: Stili della finestra List-View (CommCtrl. h)
description: Gli stili della finestra seguenti sono specifici dei controlli visualizzazione elenco.
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
ms.openlocfilehash: cae95bdb8dc1263b485f0bd2c50a8124dd57fc3a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327238"
---
# <a name="list-view-window-styles"></a>Stili della finestra List-View

Gli stili della finestra seguenti sono specifici dei controlli visualizzazione elenco.



| Costante                                                                                                                                                                        | Descrizione                                                                                                                                                                                                                                                                                                                                                 |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="LVS_ALIGNLEFT"></span><span id="lvs_alignleft"></span><dl> <dt>**\_ALIGNLEFT LVS**</dt> </dl>                   | Gli elementi sono allineati a sinistra nell'icona e nella visualizzazione icona piccola. <br/>                                                                                                                                                                                                                                                                                             |
| <span id="LVS_ALIGNMASK"></span><span id="lvs_alignmask"></span><dl> <dt>**\_ALIGNMASK LVS**</dt> </dl>                   | Allineamento corrente del controllo. <br/>                                                                                                                                                                                                                                                                                                                |
| <span id="LVS_ALIGNTOP"></span><span id="lvs_aligntop"></span><dl> <dt>**\_ALIGNTOP LVS**</dt> </dl>                      | Gli elementi sono allineati con la parte superiore del controllo visualizzazione elenco in icona e piccola visualizzazione icona. <br/>                                                                                                                                                                                                                                                            |
| <span id="LVS_AUTOARRANGE"></span><span id="lvs_autoarrange"></span><dl> <dt>**\_disposizione LVS**</dt> </dl>             | Le icone vengono automaticamente disposte nell'icona e nella visualizzazione icona piccola. <br/>                                                                                                                                                                                                                                                                              |
| <span id="LVS_EDITLABELS"></span><span id="lvs_editlabels"></span><dl> <dt>**\_EDITLABELS LVS**</dt> </dl>                | Il testo dell'elemento può essere modificato sul posto. La finestra padre deve elaborare il codice di notifica [ \_ ENDLABELEDIT di LVN](lvn-endlabeledit.md) . <br/>                                                                                                                                                                                                               |
| <span id="LVS_ICON"></span><span id="lvs_icon"></span><dl> <dt>**\_icona LVS**</dt> </dl>                                  | Questo stile specifica la visualizzazione icona. <br/>                                                                                                                                                                                                                                                                                                                 |
| <span id="LVS_LIST"></span><span id="lvs_list"></span><dl> <dt>**\_elenco LVS**</dt> </dl>                                  | Questo stile specifica la visualizzazione elenco. <br/>                                                                                                                                                                                                                                                                                                                 |
| <span id="LVS_NOCOLUMNHEADER"></span><span id="lvs_nocolumnheader"></span><dl> <dt>**LVS \_ NOcolumnheader**</dt> </dl>    | Le intestazioni di colonna non vengono visualizzate in visualizzazione report. Per impostazione predefinita, le colonne contengono intestazioni in visualizzazione report. <br/>                                                                                                                                                                                                                                               |
| <span id="LVS_NOLABELWRAP"></span><span id="lvs_nolabelwrap"></span><dl> <dt>**\_NOLABELWRAP LVS**</dt> </dl>             | Il testo dell'elemento viene visualizzato in una singola riga nella visualizzazione icone. Per impostazione predefinita, il testo dell'elemento può essere a capo in visualizzazione icone. <br/>                                                                                                                                                                                                                                              |
| <span id="LVS_NOSCROLL"></span><span id="lvs_noscroll"></span><dl> <dt>**LVS \_ NOscroll**</dt> </dl>                      | Lo scorrimento è disabilitato. Tutti gli elementi devono trovarsi all'interno dell'area client. Questo stile non è compatibile con l' **\_ elenco LVS** o gli stili del **\_ report LVS** . Per ulteriori informazioni, vedere l'articolo della Knowledge base Q137520. <br/>                                                                                                                                      |
| <span id="LVS_NOSORTHEADER"></span><span id="lvs_nosortheader"></span><dl> <dt>**\_NOSORTHEADER LVS**</dt> </dl>          | Le intestazioni di colonna non funzionano come i pulsanti. Questo stile può essere utilizzato se fare clic su un'intestazione di colonna in visualizzazione report non esegue un'azione, ad esempio l'ordinamento. <br/>                                                                                                                                                                                       |
| <span id="LVS_OWNERDATA"></span><span id="lvs_ownerdata"></span><dl> <dt>**\_OWNERDATA LVS**</dt> </dl>                   | [Versione 4,70](common-control-versions.md). Questo stile specifica un controllo visualizzazione elenco virtuale. Per ulteriori informazioni su questo stile di controllo elenco, vedere [informazioni sui controlli List-View](list-view-controls-overview.md). <br/>                                                                                                                             |
| <span id="LVS_OWNERDRAWFIXED"></span><span id="lvs_ownerdrawfixed"></span><dl> <dt>**\_OwnerDrawFixed LVS**</dt> </dl>    | La finestra proprietaria può disegnare elementi in visualizzazione report. Il controllo List-View Invia un messaggio [**WM \_ DrawItem**](wm-drawitem.md) per disegnare ogni elemento, ma non invia messaggi distinti per ogni elemento secondario. Il membro **iItemData** della struttura [**DRAWITEMSTRUCT**](/windows/win32/api/winuser/ns-winuser-drawitemstruct) contiene i dati dell'elemento per l'elemento della visualizzazione elenco specificato. <br/> |
| <span id="LVS_REPORT"></span><span id="lvs_report"></span><dl> <dt>**\_report LVS**</dt> </dl>                            | Questo stile specifica la visualizzazione report. Quando si usa lo \_ stile del report LVS con un controllo visualizzazione elenco, la prima colonna è sempre allineata a sinistra. Non è possibile usare LVCFMT \_ right per modificare questo allineamento. Per ulteriori informazioni sull'allineamento delle colonne, vedere [**LVCOLUMN**](/windows/win32/api/commctrl/ns-commctrl-lvcolumna) . <br/>                                                                      |
| <span id="LVS_SHAREIMAGELISTS"></span><span id="lvs_shareimagelists"></span><dl> <dt>**\_SHAREIMAGELISTS LVS**</dt> </dl> | L'elenco di immagini non verrà eliminato quando il controllo viene eliminato definitivamente. Questo stile consente di usare gli stessi elenchi di immagini con più controlli di visualizzazione elenco. <br/>                                                                                                                                                                                          |
| <span id="LVS_SHOWSELALWAYS"></span><span id="lvs_showselalways"></span><dl> <dt>**\_SHOWSELALWAYS LVS**</dt> </dl>       | La selezione, se presente, viene sempre visualizzata, anche se il controllo non ha lo stato attivo. <br/>                                                                                                                                                                                                                                                            |
| <span id="LVS_SINGLESEL"></span><span id="lvs_singlesel"></span><dl> <dt>**\_SINGLESEL LVS**</dt> </dl>                   | È possibile selezionare un solo elemento alla volta. Per impostazione predefinita, è possibile selezionare più elementi. <br/>                                                                                                                                                                                                                                                            |
| <span id="LVS_SMALLICON"></span><span id="lvs_smallicon"></span><dl> <dt>**\_SMALLICON LVS**</dt> </dl>                   | Questo stile specifica una piccola visualizzazione icone. <br/>                                                                                                                                                                                                                                                                                                           |
| <span id="LVS_SORTASCENDING"></span><span id="lvs_sortascending"></span><dl> <dt>**\_SORTASCENDING LVS**</dt> </dl>       | Gli indici degli elementi vengono ordinati in base al testo dell'elemento in ordine crescente. <br/>                                                                                                                                                                                                                                                                                  |
| <span id="LVS_SORTDESCENDING"></span><span id="lvs_sortdescending"></span><dl> <dt>**\_SORTDESCENDING LVS**</dt> </dl>    | Gli indici degli elementi vengono ordinati in base al testo dell'elemento in ordine decrescente. <br/>                                                                                                                                                                                                                                                                                 |
| <span id="LVS_TYPEMASK"></span><span id="lvs_typemask"></span><dl> <dt>**\_TYPEMASK LVS**</dt> </dl>                      | Determina lo stile della finestra corrente del controllo. <br/>                                                                                                                                                                                                                                                                                                  |
| <span id="LVS_TYPESTYLEMASK"></span><span id="lvs_typestylemask"></span><dl> <dt>**\_TYPESTYLEMASK LVS**</dt> </dl>       | Determina gli stili della finestra che controllano l'allineamento degli elementi e l'aspetto e il comportamento dell'intestazione. <br/>                                                                                                                                                                                                                                                    |



## <a name="remarks"></a>Commenti

Per gli stili **LVS \_ SORTASCENDING** e **LVS \_ SORTDESCENDING** , gli indici degli elementi vengono ordinati in base al testo dell'elemento rispettivamente in ordine crescente o decrescente. Poiché le **visualizzazioni \_ elenco LVS** e **LVS \_ report** visualizzano gli elementi nello stesso ordine in cui si trovano gli indici, i risultati dell'ordinamento sono immediatamente visibili all'utente. Le visualizzazioni **LVS \_ Icon** e **LVS \_ SMALLICON** non utilizzano gli indici degli elementi per determinare la posizione delle icone. Con tali viste, i risultati dell'ordinamento non sono visibili all'utente.

È possibile usare **LVS \_ TYPEMASK** mask per isolare gli stili della finestra che corrispondono alla visualizzazione corrente: **LVS \_ Icon**, **LVS \_ List**, **LVS \_ report** e **LVS \_** SMALLICON.

È possibile usare **LVS \_ ALIGNMASK** mask per isolare gli stili della finestra che specificano l'allineamento degli elementi: **LVS \_ ALIGNLEFT** e **LVS \_ ALIGNTOP**.

È possibile usare **LVS \_ TYPESTYLEMASK** mask per isolare gli stili della finestra che controllano l'allineamento degli elementi (**LVS \_ ALIGNLEFT** e **LVS \_ ALIGNTOP**) e quelli che controllano l'aspetto e il comportamento dell'intestazione (**LVS \_ nocolumnheader** e **LVS \_ NOSORTHEADER**).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|---------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>CommCtrl. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Stili e visualizzazioni di visualizzazione elenco](list-view-controls-overview.md)
</dt> </dl>

 

 





