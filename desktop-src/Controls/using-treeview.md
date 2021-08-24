---
title: Uso di Tree-View personalizzati
description: Questa sezione contiene informazioni dettagliate sull'implementazione e codice di esempio per l'uso di controlli di visualizzazione albero.
ms.assetid: 37736770-5030-4f8a-a020-6897ed5f4e96
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8beac9ef5163b52582a2ea89820278cc10f9f68ad865354404efd72a61b04993
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119318590"
---
# <a name="using-tree-view-controls"></a>Uso di Tree-View personalizzati

Questa sezione contiene informazioni dettagliate sull'implementazione e codice di esempio per l'uso di controlli di visualizzazione albero.

## <a name="in-this-section"></a>Contenuto della sezione



| Argomento                                                                                | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
|--------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Come creare un controllo Tree-View controllo](create-a-tree-view-control.md)<br/>       | Per creare un controllo di visualizzazione albero, usare la [**funzione CreateWindowEx,**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) specificando il valore [**\_ TREEVIEW WC**](common-control-window-classes.md) per la classe window. La classe della finestra di visualizzazione albero viene registrata nello spazio indirizzi dell'applicazione quando viene caricata la DLL del controllo comune. Per assicurarsi che la DLL sia caricata, usare la [**funzione InitCommonControls.**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrols) <br/>                                                                    |
| [Come inizializzare l'elenco di immagini](initialize-the-image-list.md)<br/>         | A ogni elemento di un controllo di visualizzazione albero possono essere associate due immagini. Un elemento visualizza un'immagine quando è selezionata e l'altra quando non lo è. Per includere immagini con elementi di visualizzazione albero, usare prima di tutto le funzioni [Elenchi](image-lists.md) immagini per creare un elenco di immagini e aggiungerne altre. Associare quindi l'elenco di immagini al controllo di visualizzazione albero usando il messaggio [**\_ TVM SETIMAGELIST.**](tvm-setimagelist.md) <br/>                                                                     |
| [Come aggiungere Tree-View elementi](add-tree-view-items.md)<br/>                     | Per aggiungere un elemento a un controllo di visualizzazione albero, inviare il messaggio [**\_ INSERTITEM di TVM**](tvm-insertitem.md) al controllo. Il messaggio include l'indirizzo di una struttura [**TVINSERTSTRUCT,**](/windows/win32/api/commctrl/ns-commctrl-tvinsertstructa) specificando l'elemento padre, l'elemento dopo il quale viene inserito il nuovo elemento e una struttura [**TVITEM**](/windows/win32/api/commctrl/ns-commctrl-tvitema) che definisce gli attributi dell'elemento. Gli attributi includono l'etichetta dell'elemento, le immagini selezionate e non selezionate e un valore definito dall'applicazione a 32 bit. <br/> |
| [Come trascinare un Tree-View elemento](drag-a-tree-view-item.md)<br/>                 | In questo argomento viene illustrato il codice per la gestione del trascinamento degli elementi della visualizzazione albero. Il codice di esempio è costituito da tre funzioni. La prima funzione inizia l'operazione di trascinamento, la seconda funzione trascina l'immagine e la terza funzione termina l'operazione di trascinamento. <br/>                                                                                                                                                                                                                                  |
| [Come usare gli indici delle immagini di stato](work-with-state-image-indexes.md)<br/> | Spesso si crea confusione su come impostare e recuperare l'indice dell'immagine di stato in un controllo di visualizzazione albero. Negli esempi seguenti viene illustrato il metodo appropriato per l'impostazione e il recupero dell'indice dell'immagine di stato. Gli esempi presuppongono che nel controllo di visualizzazione albero siano presenti solo due indici di immagine di stato, deselezionati e selezionati. Se l'applicazione contiene più di due funzioni, sarà necessario modificare queste funzioni per gestire tale caso. <br/>                                                               |
| [Come usare le descrizioni Tree-View infotip](use-tree-view-infotips.md)<br/>               | Quando si applica lo stile [**\_ INFOTIP TVS**](tree-view-control-window-styles.md) a un controllo di visualizzazione albero, vengono generate notifiche [ \_ TVN GETINFOTIP](tvn-getinfotip.md) quando il cursore si trova su un elemento nella visualizzazione albero. Rispondendo a questa notifica, è possibile impostare il testo visualizzato nella descrizione comandi. <br/>                                                                                                                                                                                    |



 

 

