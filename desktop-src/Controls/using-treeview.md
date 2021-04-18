---
title: Uso di controlli Tree-View
description: Questa sezione contiene i dettagli di implementazione e il codice di esempio per l'uso di controlli di visualizzazione ad albero.
ms.assetid: 37736770-5030-4f8a-a020-6897ed5f4e96
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d9ed8d1040a635964e772b8399a5c476e67f9aba
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/21/2020
ms.locfileid: "106300530"
---
# <a name="using-tree-view-controls"></a>Uso di controlli Tree-View

Questa sezione contiene i dettagli di implementazione e il codice di esempio per l'uso di controlli di visualizzazione ad albero.

## <a name="in-this-section"></a>Contenuto della sezione



| Argomento                                                                                | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
|--------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Come creare un controllo Tree-View](create-a-tree-view-control.md)<br/>       | Per creare un controllo di visualizzazione albero, usare la funzione [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) , specificando il valore di [**\_ TreeView del WC**](common-control-window-classes.md) per la classe Window. La classe della finestra visualizzazione albero viene registrata nello spazio degli indirizzi dell'applicazione quando viene caricata la DLL del controllo comune. Per assicurarsi che la DLL venga caricata, utilizzare la funzione [**InitCommonControls**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrols) . <br/>                                                                    |
| [Come inizializzare l'elenco di immagini](initialize-the-image-list.md)<br/>         | A ogni elemento di un controllo di visualizzazione albero possono essere associate due immagini. Un elemento Visualizza un'immagine quando è selezionata e l'altra in caso contrario. Per includere immagini con elementi della visualizzazione albero, utilizzare innanzitutto le funzioni [elenchi immagini](image-lists.md) per creare un elenco di immagini e aggiungervi immagini. Associare quindi l'elenco di immagini al controllo di visualizzazione ad albero usando il messaggio macchina virtuale [**TVM \_**](tvm-setimagelist.md) . <br/>                                                                     |
| [Come aggiungere elementi di Tree-View](add-tree-view-items.md)<br/>                     | Aggiungere un elemento a un controllo di visualizzazione albero inviando il messaggio [**di \_ INSERTITEM INSERTITEM**](tvm-insertitem.md) al controllo. Il messaggio include l'indirizzo di una struttura [**TVINSERTSTRUCT**](/windows/win32/api/commctrl/ns-commctrl-tvinsertstructa) , specificando l'elemento padre, l'elemento dopo il quale viene inserito il nuovo elemento e una struttura [**TVITEM**](/windows/win32/api/commctrl/ns-commctrl-tvitema) che definisce gli attributi dell'elemento. Gli attributi includono l'etichetta dell'elemento, le immagini selezionate e non selezionate e un valore definito dall'applicazione a 32 bit. <br/> |
| [Come trascinare un elemento di Tree-View](drag-a-tree-view-item.md)<br/>                 | In questo argomento viene illustrato il codice per la gestione del trascinamento e dell'eliminazione di elementi della visualizzazione albero. Il codice di esempio è costituito da tre funzioni. La prima funzione inizia l'operazione di trascinamento, la seconda funzione trascina l'immagine e la terza funzione termina l'operazione di trascinamento. <br/>                                                                                                                                                                                                                                  |
| [Come lavorare con gli indici di immagini di stato](work-with-state-image-indexes.md)<br/> | Spesso si confonde l'impostazione e il recupero dell'indice dell'immagine di stato in un controllo di visualizzazione albero. Negli esempi seguenti viene illustrato il metodo appropriato per l'impostazione e il recupero dell'indice dell'immagine di stato. Negli esempi si presuppone che esistano solo due indici di immagini di stato nel controllo di visualizzazione albero, deselezionati e controllati. Se l'applicazione contiene più di due, sarà necessario modificare queste funzioni per gestire tale caso. <br/>                                                               |
| [Come usare Tree-View infotip](use-tree-view-infotips.md)<br/>               | Quando si applica lo [**stile \_ INFOTIP TVS**](tree-view-control-window-styles.md) a un controllo di visualizzazione albero, genera notifiche [ \_ GETINFOTIP di TVN](tvn-getinfotip.md) quando il cursore è posizionato su un elemento nella visualizzazione albero. Rispondendo a questa notifica, è possibile impostare il testo visualizzato in infotip. <br/>                                                                                                                                                                                    |



 

 

