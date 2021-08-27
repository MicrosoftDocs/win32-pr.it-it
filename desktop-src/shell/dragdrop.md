---
description: Molte applicazioni consentono agli utenti di trasferire i dati a un'altra applicazione trascinandoli con il mouse o usando gli Appunti.
title: Trasferimento di oggetti shell con trascinamento della selezione e gli Appunti
ms.topic: article
ms.date: 05/31/2018
ms.assetid: bd73098b-2f69-48a4-bb06-e1e0a452e69d
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: c45fc01709c50fd309c285cb486474cab2f1d8ac0b20c56bb7e21578cb8138f0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120090621"
---
# <a name="transferring-shell-objects-with-drag-and-drop-and-the-clipboard"></a>Trasferimento di oggetti shell con trascinamento della selezione e gli Appunti

Molte applicazioni consentono agli utenti di trasferire i dati a un'altra applicazione trascinandoli con il mouse o usando gli Appunti. Tra i molti tipi di dati che è possibile trasferire sono gli oggetti shell, ad esempio file o cartelle. Il trasferimento dei dati della shell può essere fatto tra due applicazioni, ma gli utenti possono anche trasferire i dati di Shell da o verso il desktop o Windows Explorer.

Anche se i file sono l'oggetto Shell trasferito più comunemente, il trasferimento dei dati della shell può coinvolgere qualsiasi tipo di oggetto disponibile nello spazio dei nomi [Shell](namespace-intro.md). Ad esempio, l'applicazione potrebbe dover trasferire un file in una cartella virtuale, ad esempio il Cestino, o accettare un oggetto da un'estensione dello spazio dei nomi non Microsoft. Se si implementa un'estensione dello spazio dei nomi, deve essere in grado di comportarsi correttamente come origine di rilascio e destinazione.

Questo documento illustra come le applicazioni possono implementare il trascinamento della selezione e i trasferimenti di dati degli Appunti con gli oggetti Shell.

-   [Oggetto dati della shell](dataobject.md)
-   [Formati degli Appunti della shell](clipboard.md)
-   [Gestione di scenari di trasferimento dei dati shell](datascenarios.md)

## <a name="how-drag-and-drop-works-with-shell-objects"></a>Funzionamento del trascinamento della selezione con gli oggetti shell

Le applicazioni spesso devono fornire agli utenti un modo per trasferire i dati di Shell. Di seguito sono riportati alcuni esempi:

-   Trascinamento di un file da Windows Explorer o dal desktop e rilasciarlo in un'applicazione.
-   Copiare un file negli Appunti in Windows Explorer e incollarlo in un'applicazione.
-   Trascinamento di un file da un'applicazione al Cestino.

Per una descrizione dettagliata di come gestire questi e altri scenari, vedere Gestione degli scenari di [trasferimento dei dati della shell](datascenarios.md). Questo documento si concentra sui principi generali alla base del trasferimento dei dati della shell.

Windows due modalità standard per il trasferimento dei dati della shell da parte delle applicazioni:

-   Un utente taglia o copia negli Appunti i dati della shell, ad esempio uno o più file. L'altra applicazione recupera i dati dagli Appunti.
-   Un utente trascina un'icona che rappresenta i dati dall'applicazione di origine e rilascia l'icona in una finestra di proprietà della destinazione.

In entrambi i casi, i dati trasferiti sono contenuti in un *oggetto dati*. Gli oggetti dati Component Object Model (COM) che espongono [**l'interfaccia IDataObject.**](/windows/win32/api/objidl/nn-objidl-idataobject) Schematicamente, tutti i trasferimenti di dati shell devono essere eseguati in tre passaggi essenziali:

1.  L'origine crea un oggetto dati che rappresenta i dati da trasferire.
2.  La destinazione riceve un puntatore all'interfaccia [**IDataObject dell'oggetto**](/windows/win32/api/objidl/nn-objidl-idataobject) dati.
3.  La destinazione chiama [**l'interfaccia IDataObject**](/windows/win32/api/objidl/nn-objidl-idataobject) per estrarre i dati da essa.

La differenza tra gli Appunti e i trasferimenti di dati di trascinamento della selezione risiede principalmente nel modo in cui il puntatore [**IDataObject**](/windows/win32/api/objidl/nn-objidl-idataobject) viene trasferito dall'origine alla destinazione.

### <a name="clipboard-data-transfers"></a>Trasferimenti di dati negli Appunti

Gli Appunti sono il modo più semplice per trasferire i dati della shell. La procedura di base è simile ai trasferimenti di dati standard degli Appunti. Tuttavia, poiché si trasferisce un puntatore a un oggetto dati, non ai dati stessi, è necessario usare l'API Degli Appunti OLE anziché l'API Degli Appunti standard. La procedura seguente illustra come usare l'API Degli Appunti OLE per trasferire i dati della shell con gli Appunti:

1.  L'origine dati crea un oggetto dati per contenere i dati.
2.  L'origine dati chiama [**OleSetClipboard**](/windows/win32/api/ole2/nf-ole2-olesetclipboard), che inserisce un puntatore all'interfaccia [**IDataObject**](/windows/win32/api/objidl/nn-objidl-idataobject) dell'oggetto dati negli Appunti.
3.  La destinazione chiama [**OleGetClipboard**](/windows/win32/api/ole2/nf-ole2-olegetclipboard) per recuperare il puntatore all'interfaccia [**IDataObject dell'oggetto**](/windows/win32/api/objidl/nn-objidl-idataobject) dati.
4.  La destinazione estrae i dati chiamando il [**metodo IDataObject::GetData.**](/windows/win32/api/objidl/nf-objidl-idataobject-getdata)
5.  Con alcuni trasferimenti di dati shell, la destinazione potrebbe anche dover chiamare il metodo [**IDataObject::SetData**](/windows/win32/api/objidl/nf-objidl-idataobject-setdata) dell'oggetto dati per fornire feedback all'oggetto dati sul risultato del trasferimento dei dati. Per [un esempio di questo tipo di operazione,](datascenarios.md) vedere Gestione delle operazioni di spostamento ottimizzate.

### <a name="drag-and-drop-data-transfers"></a>Trasferimenti di dati con trascinamento della selezione

Sebbene sia un po' più complesso da implementare, il trasferimento dei dati tramite trascinamento della selezione presenta alcuni vantaggi significativi rispetto agli Appunti:

-   I trasferimenti di trascinamento della selezione possono essere estinti con un semplice spostamento del mouse, rendendo l'operazione più flessibile e intuitiva da usare rispetto agli Appunti.
-   Il trascinamento della selezione fornisce all'utente una rappresentazione visiva dell'operazione. L'utente può seguire l'icona durante lo spostamento dall'origine alla destinazione.
-   Il trascinamento della selezione invia una notifica alla destinazione quando i dati sono disponibili.

Le operazioni di trascinamento della selezione usano anche oggetti dati per trasferire i dati. Tuttavia, l'origine di rilascio deve fornire funzionalità oltre a quella necessaria per i trasferimenti degli Appunti:

-   L'origine di rilascio deve anche creare un oggetto che espone [**un'interfaccia IDropSource.**](/windows/win32/api/oleidl/nn-oleidl-idropsource) Il sistema usa **IDropSource** per comunicare con l'origine mentre l'operazione è in corso.
-   L'oggetto dati di trascinamento della selezione è responsabile del rilevamento dello spostamento del cursore e della visualizzazione di un'icona per rappresentare l'oggetto dati.

Le destinazioni di rilascio devono inoltre fornire più funzionalità di quelle necessarie per gestire i trasferimenti degli Appunti:

-   La destinazione di rilascio deve esporre [**un'interfaccia IDropTarget.**](/windows/win32/api/oleidl/nn-oleidl-idroptarget) Quando il cursore si trova su una finestra di destinazione, il sistema usa **IDropTarget** per fornire alla destinazione informazioni come la posizione del cursore e per notificare quando i dati vengono eliminati.
-   La destinazione di rilascio deve registrarsi con il sistema chiamando [**RegisterDragDrop**](/windows/win32/api/ole2/nf-ole2-registerdragdrop). Questa funzione fornisce al sistema l'handle per una finestra di destinazione e un puntatore [**all'interfaccia IDropTarget**](/windows/win32/api/oleidl/nn-oleidl-idroptarget) dell'applicazione di destinazione.

> [!Note]  
> Per le operazioni di trascinamento della selezione, l'applicazione deve inizializzare COM [**con OleInitialize**](/windows/win32/api/ole2/nf-ole2-oleinitialize), non [**con CoInitialize**](/windows/win32/api/objbase/nf-objbase-coinitialize).

 

La procedura seguente illustra i passaggi essenziali usati in genere per trasferire i dati di Shell con il trascinamento della selezione:

1.  La destinazione chiama [**RegisterDragDrop**](/windows/win32/api/ole2/nf-ole2-registerdragdrop) per assegnare al sistema un puntatore alla relativa [**interfaccia IDropTarget**](/windows/win32/api/oleidl/nn-oleidl-idroptarget) e registrare una finestra come destinazione di rilascio.
2.  Quando l'utente avvia un'operazione di trascinamento della selezione,  l'origine crea un oggetto dati e avvia un ciclo di trascinamento chiamando [**DoDragDrop**](/windows/win32/api/ole2/nf-ole2-dodragdrop).
3.  Quando il cursore si trova sulla finestra di destinazione, il sistema invia una notifica alla destinazione chiamando uno dei metodi [**IDropTarget della**](/windows/win32/api/oleidl/nn-oleidl-idroptarget) destinazione. Il sistema chiama [**IDropTarget::D ragEnter**](/windows/win32/api/oleidl/nf-oleidl-idroptarget-dragenter) quando il cursore entra nella finestra di destinazione e [**IDropTarget::D ragOver**](/windows/win32/api/oleidl/nf-oleidl-idroptarget-dragover) quando il cursore passa sulla finestra di destinazione. Entrambi i metodi forniscono la destinazione di rilascio con la posizione corrente del cursore e lo stato dei tasti di modifica della tastiera, ad esempio CTRL o ALT. Quando il cursore esce dalla finestra di destinazione, il sistema invia una notifica alla destinazione chiamando [**IDropTarget::D ragLeave**](/windows/win32/api/oleidl/nf-oleidl-idroptarget-dragleave). Quando uno di questi metodi restituisce , il sistema chiama [**l'interfaccia IDropSource**](/windows/win32/api/oleidl/nn-oleidl-idropsource) per passare il valore restituito all'origine.
4.  Quando l'utente rilascia il pulsante del mouse per rilasciare i dati, il sistema chiama il metodo [**IDropTarget::D rop della**](/windows/win32/api/oleidl/nf-oleidl-idroptarget-drop) destinazione. Tra i parametri del metodo è disponibile un puntatore all'interfaccia [**IDataObject dell'oggetto**](/windows/win32/api/objidl/nn-objidl-idataobject) dati.
5.  La destinazione chiama il metodo [**IDataObject::GetData**](/windows/win32/api/objidl/nf-objidl-idataobject-getdata) dell'oggetto dati per estrarre i dati.
6.  Con alcuni trasferimenti di dati shell, la destinazione potrebbe anche dover chiamare il metodo [**IDataObject::SetData**](/windows/win32/api/objidl/nf-objidl-idataobject-setdata) dell'oggetto dati per fornire feedback all'origine sul risultato del trasferimento dei dati.
7.  Quando la destinazione viene completata con l'oggetto dati, viene restituito da [**IDropTarget::D rop**](/windows/win32/api/oleidl/nf-oleidl-idroptarget-drop). Il sistema restituisce la chiamata [**DoDragDrop**](/windows/win32/api/ole2/nf-ole2-dodragdrop) dell'origine per notificare all'origine che il trasferimento dei dati è stato completato.
8.  A seconda dello [scenario](datascenarios.md)di trasferimento dei dati specifico, l'origine potrebbe dover eseguire un'azione aggiuntiva in base al valore restituito da [**DoDragDrop**](/windows/win32/api/ole2/nf-ole2-dodragdrop) e ai valori passati all'oggetto dati dalla destinazione. Ad esempio, quando un file viene spostato, l'origine deve controllare questi valori per determinare se deve eliminare il file originale.
9.  L'origine rilascia l'oggetto dati.

Anche se le procedure descritte in precedenza forniscono un buon modello generale per il trasferimento dei dati della shell, esistono molti tipi diversi di dati che possono essere contenuti in un oggetto dati shell. Esistono anche diversi scenari di trasferimento dei dati che l'applicazione potrebbe dover gestire. Ogni tipo di dati e scenario richiede un approccio leggermente diverso a tre passaggi chiave della procedura:

-   Modalità di costruzione di un oggetto dati da parte di un'origine per contenere i dati della shell.
-   Come una destinazione estrae i dati della shell dall'oggetto dati.
-   Modalità di completamento dell'operazione di trasferimento dei dati da parte dell'origine.

[L'oggetto dati shell](dataobject.md) fornisce una descrizione generale del modo in cui un'origine costruisce un oggetto dati shell e di come tale oggetto dati può essere gestito dalla destinazione. [Gestione degli scenari di trasferimento dei](datascenarios.md) dati della shell illustra in dettaglio come gestire una serie di scenari comuni di trasferimento dei dati della shell.

 

 
