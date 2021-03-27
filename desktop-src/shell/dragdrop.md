---
description: Molte applicazioni consentono agli utenti di trasferire i dati a un'altra applicazione trascinando i dati con il mouse o usando gli Appunti.
title: Trasferimento di oggetti Shell con trascinamento della selezione e degli Appunti
ms.topic: article
ms.date: 05/31/2018
ms.assetid: bd73098b-2f69-48a4-bb06-e1e0a452e69d
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: b04523d0ae22eac7bef68f37a6d22ac94b21e303
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104979746"
---
# <a name="transferring-shell-objects-with-drag-and-drop-and-the-clipboard"></a>Trasferimento di oggetti Shell con trascinamento della selezione e degli Appunti

Molte applicazioni consentono agli utenti di trasferire i dati a un'altra applicazione trascinando i dati con il mouse o usando gli Appunti. Tra i molti tipi di dati che possono essere trasferiti si trovano oggetti Shell, ad esempio file o cartelle. Il trasferimento dei dati della shell può avvenire tra due applicazioni, ma gli utenti possono anche trasferire dati della shell da e verso il desktop o Esplora risorse.

Anche se i file sono l'oggetto Shell trasferito più di frequente, il trasferimento dei dati della shell può coinvolgere qualsiasi varietà di oggetti disponibili nello [spazio dei nomi della shell](namespace-intro.md). Ad esempio, è possibile che l'applicazione debba trasferire un file in una cartella virtuale, ad esempio il Cestino, oppure accettare un oggetto da un'estensione dello spazio dei nomi non Microsoft. Se si implementa un'estensione dello spazio dei nomi, è necessario che sia in grado di funzionare correttamente come origine di rilascio e destinazione.

Questo documento illustra in che modo le applicazioni possono implementare trasferimenti di dati di trascinamento e appunti con oggetti Shell.

-   [Oggetto dati della shell](dataobject.md)
-   [Formati degli Appunti della shell](clipboard.md)
-   [Gestione di scenari di trasferimento dei dati shell](datascenarios.md)

## <a name="how-drag-and-drop-works-with-shell-objects"></a>Funzionamento del trascinamento della selezione con gli oggetti Shell

Le applicazioni spesso devono fornire agli utenti un modo per trasferire i dati della shell. Di seguito sono riportati alcuni esempi:

-   Trascinando un file da Esplora risorse o dal desktop e rilasciandolo in un'applicazione.
-   Copiare un file negli Appunti in Esplora risorse e incollarlo in un'applicazione.
-   Il trascinamento di un file da un'applicazione al Cestino.

Per una descrizione dettagliata di come gestire questi e altri scenari, vedere [gestione degli scenari di trasferimento dati della shell](datascenarios.md). Questo documento è incentrato sui principi generali alla base del trasferimento dei dati della shell.

In Windows sono disponibili due modalità standard per trasferire i dati della shell dalle applicazioni:

-   Un utente taglia o copia i dati della shell, ad esempio uno o più file, negli Appunti. L'altra applicazione recupera i dati dagli Appunti.
-   Un utente trascina un'icona che rappresenta i dati dell'applicazione di origine e rilascia l'icona in una finestra di proprietà della destinazione.

In entrambi i casi, i dati trasferiti sono contenuti in un *oggetto dati*. Gli oggetti dati sono oggetti Component Object Model (COM) che espongono l'interfaccia [**IDataObject**](/windows/win32/api/objidl/nn-objidl-idataobject) . Schematicamente, sono necessari tre passaggi essenziali che devono essere seguiti da tutti i trasferimenti di dati della shell:

1.  L'origine crea un oggetto dati che rappresenta i dati da trasferire.
2.  La destinazione riceve un puntatore all'interfaccia [**IDataObject**](/windows/win32/api/objidl/nn-objidl-idataobject) dell'oggetto dati.
3.  La destinazione chiama l'interfaccia [**IDataObject**](/windows/win32/api/objidl/nn-objidl-idataobject) per estrarre i dati da esso.

La differenza tra gli appunti e i trasferimenti di dati con trascinamento della selezione risiede principalmente nel modo in cui il puntatore [**IDataObject**](/windows/win32/api/objidl/nn-objidl-idataobject) viene trasferito dall'origine alla destinazione.

### <a name="clipboard-data-transfers"></a>Trasferimenti di dati negli Appunti

Gli Appunti sono il modo più semplice per trasferire i dati della shell. La procedura di base è simile ai trasferimenti di dati degli Appunti standard. Tuttavia, poiché si trasferisce un puntatore a un oggetto dati, non ai dati stessi, è necessario utilizzare l'API degli Appunti OLE anziché l'API degli Appunti standard. La procedura seguente illustra come usare l'API degli Appunti OLE per trasferire i dati della shell con gli Appunti:

1.  L'origine dati consente di creare un oggetto dati per contenere i dati.
2.  L'origine dati chiama [**OleSetClipboard**](/windows/win32/api/ole2/nf-ole2-olesetclipboard), che inserisce un puntatore all'interfaccia [**IDataObject**](/windows/win32/api/objidl/nn-objidl-idataobject) dell'oggetto dati negli Appunti.
3.  La destinazione chiama [**OleGetClipboard**](/windows/win32/api/ole2/nf-ole2-olegetclipboard) per recuperare il puntatore all'interfaccia [**IDataObject**](/windows/win32/api/objidl/nn-objidl-idataobject) dell'oggetto dati.
4.  La destinazione estrae i dati chiamando il metodo [**IDataObject:: GetData**](/windows/win32/api/objidl/nf-objidl-idataobject-getdata) .
5.  Con alcuni trasferimenti di dati della shell, potrebbe essere necessario che la destinazione chiami anche il metodo [**IDataObject:: SetData**](/windows/win32/api/objidl/nf-objidl-idataobject-setdata) dell'oggetto dati per fornire commenti e suggerimenti all'oggetto dati sul risultato del trasferimento dei dati. Per un esempio di questo tipo di operazione, vedere [gestione delle operazioni di spostamento ottimizzate](datascenarios.md) .

### <a name="drag-and-drop-data-transfers"></a>Trasferimenti di dati con trascinamento della selezione

Sebbene un po' più complesso da implementare, il trasferimento dei dati con trascinamento della selezione presenta alcuni vantaggi significativi rispetto agli Appunti:

-   I trasferimenti con trascinamento della selezione possono essere eseguiti con un semplice movimento del mouse, rendendo l'operazione più flessibile e intuitiva da usare degli Appunti.
-   Il trascinamento della selezione fornisce all'utente una rappresentazione visiva dell'operazione. L'utente può seguire l'icona mentre passa dall'origine alla destinazione.
-   Il trascinamento della selezione Invia una notifica alla destinazione quando i dati sono disponibili.

Anche le operazioni di trascinamento della selezione utilizzano oggetti dati per trasferire i dati. Tuttavia, l'origine di rilascio deve fornire funzionalità oltre a quelle richieste per i trasferimenti degli Appunti:

-   L'origine di rilascio deve anche creare un oggetto che espone un'interfaccia [**IDropSource**](/windows/win32/api/oleidl/nn-oleidl-idropsource) . Il sistema usa **IDropSource** per comunicare con l'origine mentre è in corso l'operazione.
-   L'oggetto dati con trascinamento della selezione è responsabile del rilevamento del movimento del cursore e della visualizzazione di un'icona per rappresentare l'oggetto dati.

Le destinazioni di rilascio devono inoltre fornire più funzionalità rispetto a quelle necessarie per gestire i trasferimenti degli Appunti:

-   L'obiettivo di rilascio deve esporre un'interfaccia [**IDropTarget**](/windows/win32/api/oleidl/nn-oleidl-idroptarget) . Quando il cursore si trova su una finestra di destinazione, il sistema utilizza **IDropTarget** per fornire la destinazione con informazioni come la posizione del cursore e per notificarlo quando i dati vengono eliminati.
-   La destinazione di rilascio deve registrarsi con il sistema chiamando [**RegisterDragDrop**](/windows/win32/api/ole2/nf-ole2-registerdragdrop). Questa funzione fornisce al sistema l'handle di una finestra di destinazione e un puntatore all'interfaccia [**IDropTarget**](/windows/win32/api/oleidl/nn-oleidl-idroptarget) dell'applicazione di destinazione.

> [!Note]  
> Per le operazioni di trascinamento della selezione, l'applicazione deve inizializzare COM con [**OleInitialize**](/windows/win32/api/ole2/nf-ole2-oleinitialize), non [**CoInitialize**](/windows/win32/api/objbase/nf-objbase-coinitialize).

 

La procedura seguente illustra i passaggi essenziali che vengono in genere usati per trasferire i dati della shell con il trascinamento della selezione:

1.  La destinazione chiama [**RegisterDragDrop**](/windows/win32/api/ole2/nf-ole2-registerdragdrop) per fornire al sistema un puntatore all'interfaccia [**IDropTarget**](/windows/win32/api/oleidl/nn-oleidl-idroptarget) e registrare una finestra come destinazione di rilascio.
2.  Quando l'utente avvia un'operazione di trascinamento della selezione, l'origine crea un oggetto dati e avvia un *ciclo di trascinamento* chiamando [**DoDragDrop**](/windows/win32/api/ole2/nf-ole2-dodragdrop).
3.  Quando il cursore si trova sulla finestra di destinazione, il sistema invia una notifica alla destinazione chiamando uno dei metodi [**IDropTarget**](/windows/win32/api/oleidl/nn-oleidl-idroptarget) della destinazione. Il sistema chiama [**IDropTarget::D ragenter**](/windows/win32/api/oleidl/nf-oleidl-idroptarget-dragenter) quando il cursore entra nella finestra di destinazione e [**IDropTarget::D ragover**](/windows/win32/api/oleidl/nf-oleidl-idroptarget-dragover) quando il cursore passa sulla finestra di destinazione. Entrambi i metodi forniscono la destinazione di rilascio con la posizione corrente del cursore e lo stato dei tasti di modifica della tastiera, ad esempio CTRL o ALT. Quando il cursore esce dalla finestra di destinazione, il sistema invia una notifica alla destinazione chiamando [**IDropTarget::D ragleave**](/windows/win32/api/oleidl/nf-oleidl-idroptarget-dragleave). Quando uno di questi metodi restituisce, il sistema chiama l'interfaccia [**IDropSource**](/windows/win32/api/oleidl/nn-oleidl-idropsource) per passare il valore restituito all'origine.
4.  Quando l'utente rilascia il pulsante del mouse per eliminare i dati, il sistema chiama il metodo [**IDropTarget::D por**](/windows/win32/api/oleidl/nf-oleidl-idroptarget-drop) della destinazione. Tra i parametri del metodo è presente un puntatore all'interfaccia [**IDataObject**](/windows/win32/api/objidl/nn-objidl-idataobject) dell'oggetto dati.
5.  La destinazione chiama il metodo [**IDataObject:: GetData**](/windows/win32/api/objidl/nf-objidl-idataobject-getdata) dell'oggetto dati per estrarre i dati.
6.  Con alcuni trasferimenti di dati della shell, potrebbe essere necessario che la destinazione chiami anche il metodo [**IDataObject:: SetData**](/windows/win32/api/objidl/nf-objidl-idataobject-setdata) dell'oggetto dati per fornire commenti e suggerimenti all'origine sul risultato del trasferimento dei dati.
7.  Quando la destinazione termina con l'oggetto dati, viene restituito da [**IDropTarget::D por**](/windows/win32/api/oleidl/nf-oleidl-idroptarget-drop). Il sistema restituisce la chiamata [**DoDragDrop**](/windows/win32/api/ole2/nf-ole2-dodragdrop) dell'origine per notificare all'origine che il trasferimento dei dati è stato completato.
8.  A seconda dello scenario di [trasferimento dei dati](datascenarios.md)specifico, è possibile che l'origine debba eseguire ulteriori azioni in base al valore restituito da [**DoDragDrop**](/windows/win32/api/ole2/nf-ole2-dodragdrop) e ai valori passati all'oggetto dati dalla destinazione. Ad esempio, quando un file viene spostato, l'origine deve controllare questi valori per determinare se deve eliminare il file originale.
9.  L'origine rilascia l'oggetto dati.

Sebbene le procedure descritte in precedenza forniscano un modello generale valido per il trasferimento dei dati della shell, esistono molti tipi diversi di dati che possono essere contenuti in un oggetto dati della shell. Sono inoltre disponibili diversi scenari di trasferimento dei dati che possono essere gestiti dall'applicazione. Per ogni tipo di dati e scenario è necessario un approccio leggermente diverso a tre passaggi principali della procedura:

-   Il modo in cui un'origine costruisce un oggetto dati per contenere i dati della shell.
-   Modalità di estrazione dei dati della shell dall'oggetto dati da parte di una destinazione.
-   Il modo in cui l'origine completa l'operazione di trasferimento dei dati.

L' [oggetto dati della shell](dataobject.md) fornisce una descrizione generale del modo in cui un'origine costruisce un oggetto dati della shell e in che modo l'oggetto dati può essere gestito dalla destinazione. [Gestione degli scenari di trasferimento dati della shell](datascenarios.md) illustra in dettaglio come gestire diversi scenari comuni di trasferimento dei dati della shell.

 

 
