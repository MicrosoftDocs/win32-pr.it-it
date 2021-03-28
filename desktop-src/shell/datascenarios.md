---
description: In questo documento vengono illustrati gli scenari comuni di trasferimento dei dati della shell e viene illustrato come implementare ognuno di essi nell'applicazione.
ms.assetid: 7fce555c-a93d-4414-9119-7ae9acdd4d89
title: Gestione di scenari di trasferimento dei dati shell
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 35855b66e4108580d5bac305855837563ca59785
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104977314"
---
# <a name="handling-shell-data-transfer-scenarios"></a>Gestione di scenari di trasferimento dei dati shell

Il documento [oggetto dati della shell](dataobject.md) ha illustrato l'approccio generale usato per trasferire i dati della shell con il trascinamento della selezione o gli Appunti. Tuttavia, per implementare il trasferimento dei dati della shell nell'applicazione, è necessario comprendere anche come applicare questi principi e tecniche generali alla varietà di modi in cui è possibile trasferire i dati della shell. In questo documento vengono illustrati gli scenari comuni di trasferimento dei dati della shell e viene illustrato come implementare ognuno di essi nell'applicazione.

-   [Linee guida generali](#general-guidelines)
-   [Copia di nomi di file dagli Appunti in un'applicazione](#copying-file-names-from-the-clipboard-to-an-application)
    -   [Estrazione dei nomi di file dall'oggetto dati](#extracting-the-file-names-from-the-data-object)
-   [Copia del contenuto di un file eliminato in un'applicazione](#copying-the-contents-of-a-dropped-file-into-an-application)
    -   [Uso del \_ formato FILEcontents CFSTR per estrarre i dati da un file](/windows)
-   [Gestione delle operazioni di spostamento ottimizzate](#handling-optimized-move-operations)
-   [Gestione delle operazioni delete-on-paste](#handling-delete-on-paste-operations)
-   [Trasferimento di dati da e verso cartelle virtuali](#transfering-data-to-and-from-virtual-folders)
    -   [Accettazione di dati da una cartella virtuale](#accepting-data-from-a-virtual-folder)
    -   [Trasferimento di dati da e verso un'estensione dello spazio dei nomi](#transferring-data-to-and-from-a-namespace-extension)
-   [Eliminazione di file nel cestino](#dropping-files-on-the-recycle-bin)
-   [Creazione e importazione di file di scarto](#creating-and-importing-scrap-files)
    -   [Supporto round trip](#round-trip-support)
    -   [Formati di dati memorizzati nella cache](#cached-data-formats)
    -   [Rendering ritardato](#delayed-rendering)
-   [Trascinamento e rilascio di oggetti Shell in modo asincrono](#dragging-and-dropping-shell-objects-asynchronously)
    -   [Uso di IASyncOperation/IDataObjectAsyncCapability](#using-iasyncoperationidataobjectasynccapability)

> [!Note]  
> Sebbene ognuno di questi scenari discuta un'operazione di trasferimento dati specifica, molti di essi si applicano a una varietà di scenari correlati. Ad esempio, la differenza principale tra la maggior parte degli Appunti e i trasferimenti con trascinamento della selezione è il modo in cui l'oggetto dati arriva alla destinazione. Quando la destinazione ha un puntatore all'interfaccia [**IDataObject**](/windows/win32/api/objidl/nn-objidl-idataobject) dell'oggetto dati, le procedure per l'estrazione di informazioni sono in gran parte identiche per entrambi i tipi di trasferimento dei dati. Tuttavia, alcuni scenari sono limitati a un tipo specifico di operazione. Per informazioni dettagliate, vedere il singolo scenario.

 

## <a name="general-guidelines"></a>Linee guida generali

Ognuna delle sezioni seguenti illustra un unico scenario di trasferimento dati piuttosto specifico. Tuttavia, i trasferimenti di dati sono spesso più complessi e potrebbero implicare aspetti di diversi scenari. In genere non si sa in anticipo quale scenario è effettivamente necessario gestire. Di seguito sono riportate alcune linee guida generali da tenere presenti.

Per le origini dati:

-   I formati degli Appunti della shell, ad eccezione di [CF \_ HDROP](clipboard.md), non sono predefiniti. Ogni formato che si desidera utilizzare deve essere registrato chiamando [RegisterClipboardFormat](/windows/win32/api/winuser/nf-winuser-registerclipboardformata).
-   I formati negli oggetti dati vengono forniti nell'ordine di preferenza dall'origine. Enumerare l'oggetto dati e selezionare il primo che è possibile utilizzare.
-   Includere tutti i formati che è possibile supportare. In genere non si conosce la posizione in cui verrà eliminato l'oggetto dati. Questa pratica migliora le probabilità che l'oggetto dati conterrà un formato che l'obiettivo di rilascio può accettare.
-   I file esistenti devono essere offerti con il formato [CF \_ HDROP](clipboard.md) .
-   Offrire dati simili a file con [CFSTR \_ fileContents](clipboard.md) / [CFSTR \_ FileDescriptor](clipboard.md) formats. Questo approccio consente alla destinazione di creare un file da un oggetto dati senza che sia necessario conoscere l'archivio dati sottostante. È in genere necessario presentare i dati come interfaccia [**IStream**](/windows/win32/api/objidl/nn-objidl-istream) . Questo meccanismo di trasferimento dei dati è più flessibile rispetto a un oggetto memoria globale e utilizza una quantità di memoria inferiore.
-   Le origini di trascinamento devono offrire il formato [CFSTR \_ SHELLIDLIST](clipboard.md) durante il trascinamento degli elementi della shell. È possibile acquisire oggetti dati per gli elementi tramite i metodi [**IShellFolder:: GetUIObjectOf**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-getuiobjectof) o [**IShellItem:: BindToHandler**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellitem-bindtohandler) . Le origini dati possono creare un'implementazione dell'oggetto dati standard che supporta il formato [CFSTR \_ SHELLIDLIST](clipboard.md) tramite [**SHCreateDataObject**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shcreatedataobject).
-   Gli obiettivi di rilascio che vogliono ragionare sugli elementi trascinati tramite il modello di programmazione degli elementi della shell possono convertire un IDataObject in un [**IShellItemArray**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitemarray) usando [**SHCreateShellItemArrayFromDataObject**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-shcreateshellitemarrayfromdataobject).
-   Usare i cursori di feedback standard.
-   Supporta il trascinamento di sinistra e destra.
-   Utilizzare l'oggetto dati stesso da un oggetto incorporato. Questo approccio consente all'applicazione di recuperare eventuali formati aggiuntivi che l'oggetto dati deve offrire ed evitare la creazione di un ulteriore livello di contenimento. Ad esempio, un oggetto incorporato dal server A viene trascinato dal server/contenitore B ed eliminato nel contenitore C. C deve creare un oggetto incorporato del server A, non un oggetto incorporato del server B contenente un oggetto incorporato del server A.
-   Tenere presente che la shell può usare le operazioni di spostamento [ottimizzato](#handling-optimized-move-operations) o [Delete-on-paste](#handling-delete-on-paste-operations) durante lo spostamento dei file. L'applicazione deve essere in grado di riconoscere queste operazioni e rispondere in modo appropriato.

Per le destinazioni dei dati:

-   I formati degli Appunti della shell, ad eccezione di [CF \_ HDROP](clipboard.md), non sono predefiniti. Ogni formato che si desidera utilizzare deve essere registrato chiamando [RegisterClipboardFormat](/windows/win32/api/winuser/nf-winuser-registerclipboardformata).
-   Implementare e registrare una destinazione di rilascio OLE. Evitare di usare le destinazioni di Windows 3,1 o il messaggio [**WM \_ DropFiles**](wm-dropfiles.md) , se possibile.
-   I formati contenuti in un oggetto dati variano a seconda della provenienza dell'oggetto. Poiché in genere non si conosce in anticipo la provenienza di un oggetto dati, non si presuppone che sia presente un particolare formato. L'oggetto dati deve enumerare i formati in ordine di qualità, a partire dal migliore. Pertanto, per ottenere il formato migliore disponibile, le applicazioni in genere enumerano i formati disponibili e utilizzano il primo formato nell'enumerazione che possono supportare.
-   Supporto per il trascinamento destro. È possibile personalizzare il menu di scelta rapida del trascinamento creando un [gestore di trascinamento della selezione](context-menu-handlers.md).
-   Se l'applicazione accetterà i file esistenti, deve essere in grado di gestire il formato [CF \_ HDROP](clipboard.md) .
-   In generale, le applicazioni che accettano i file devono gestire anche i formati di FileDescriptor CFSTR di [CFSTR \_ fileContents](clipboard.md) / [ \_ ](clipboard.md) . Mentre i file del file System hanno il formato [CF \_ HDROP](clipboard.md) , i file di provider, ad esempio le estensioni dello spazio dei nomi, usano in genere [CFSTR \_ fileContents](clipboard.md) / [CFSTR \_ FileDescriptor](clipboard.md). Gli esempi includono cartelle Windows CE, File Transfer Protocol (FTP), cartelle Web e cartelle CAB. L'origine implementa in genere un'interfaccia [**IStream**](/windows/win32/api/objidl/nn-objidl-istream) per presentare i dati dalla relativa archiviazione come file.
-   Tenere presente che la shell può usare le operazioni di spostamento [ottimizzato](#handling-optimized-move-operations) o [Delete-on-paste](#handling-delete-on-paste-operations) durante lo spostamento dei file. L'applicazione deve essere in grado di riconoscere queste operazioni e rispondere in modo appropriato.

## <a name="copying-file-names-from-the-clipboard-to-an-application"></a>Copia di nomi di file dagli Appunti in un'applicazione

**Scenario:** Un utente seleziona uno o più file in Esplora risorse e li copia negli Appunti. L'applicazione estrae i nomi dei file e li incolla nel documento.

Questo scenario può essere usato, ad esempio, per consentire a un utente di creare un collegamento HTML tagliando e incollando il file nell'applicazione. L'applicazione può quindi estrarre il nome del file dall'oggetto dati ed elaborarlo per creare un tag di ancoraggio.

Quando un utente seleziona un file in Esplora risorse e lo copia negli Appunti, la shell crea un oggetto dati. Chiama quindi [**OleSetClipboard**](/windows/win32/api/ole2/nf-ole2-olesetclipboard) per inserire un puntatore all'interfaccia [**IDataObject**](/windows/win32/api/objidl/nn-objidl-idataobject) dell'oggetto dati negli Appunti.

Quando l'utente seleziona il comando **Incolla** dal menu o dalla barra degli strumenti dell'applicazione:

1.  Chiamare [**OleGetClipboard**](/windows/win32/api/ole2/nf-ole2-olegetclipboard) per recuperare l'interfaccia [**IDataObject**](/windows/win32/api/objidl/nn-objidl-idataobject) dell'oggetto dati.
2.  Chiamare [**IDataObject:: EnumFormatEtc**](/windows/win32/api/objidl/nf-objidl-idataobject-enumformatetc) per richiedere un oggetto enumeratore.
3.  Utilizzare l'interfaccia [**IEnumFORMATETC**](/windows/win32/api/objidl/nn-objidl-ienumformatetc) dell'oggetto enumeratore per enumerare i formati contenuti nell'oggetto dati.

> [!Note]  
> I due passaggi finali di questa procedura sono inclusi per completezza. Non sono in genere necessarie per semplici trasferimenti di file. Tutti gli oggetti dati usati per questo tipo di trasferimento dati devono contenere il formato [CF \_ HDROP](clipboard.md) , che può essere usato per determinare i nomi dei file contenuti nell'oggetto. Tuttavia, per i trasferimenti di dati più generali, è consigliabile enumerare i formati e selezionare quello migliore che l'applicazione è in grado di gestire.

 

### <a name="extracting-the-file-names-from-the-data-object"></a>Estrazione dei nomi di file dall'oggetto dati

Il passaggio successivo consiste nell'estrarre uno o più nomi di file dall'oggetto dati e incollarli nell'applicazione. Si noti che la procedura illustrata in questa sezione per l'estrazione di un nome di file da un oggetto dati si applica ugualmente bene ai trasferimenti con trascinamento della selezione.

Il modo più semplice per recuperare i nomi di file da un oggetto dati è il formato [CF \_ HDROP](clipboard.md) :

1.  Chiamare [**IDataObject:: GetData**](/windows/win32/api/objidl/nf-objidl-idataobject-getdata). Impostare il membro **cfFormat** della struttura [**FORMATETC**](/windows/win32/api/objidl/ns-objidl-formatetc) su [CF \_ HDROP](clipboard.md) e il membro **TYMED** su [TYMED \_ HGLOBAL](dataobject.md). Il membro **dwAspect** è in genere impostato sul \_ contenuto di DVASPECT. Tuttavia, se è necessario avere il percorso del file in breve (8,3), impostare **dwAspect** su DVASPECT \_ short.

    Quando [**IDataObject:: GetData**](/windows/win32/api/objidl/nf-objidl-idataobject-getdata) restituisce, il membro **HGlobal** della struttura [**STGMEDIUM**](/windows/win32/api/objidl/ns-objidl-ustgmedium-r1) punta a un oggetto memoria globale che contiene i dati.

2.  Creare una variabile HDROP e impostarla sul membro **hGlobal** della struttura [**STGMEDIUM**](/windows/win32/api/objidl/ns-objidl-ustgmedium-r1) . La variabile HDROP è ora un handle per una struttura [**DropFiles**](/windows/desktop/api/shlobj_core/ns-shlobj_core-dropfiles) seguito da una doppia stringa con terminazione null contenente i percorsi di file completi dei file copiati.
3.  Determinare il numero di percorsi di file presenti nell'elenco chiamando [**DragQueryFile**](/windows/desktop/api/Shellapi/nf-shellapi-dragqueryfilea) con il parametro *iFile* impostato su 0xFFFFFFFF. La funzione restituisce il numero di percorsi di file nell'elenco. L'indice in base zero del percorso del file in questo elenco viene usato nel passaggio successivo per identificare un percorso specifico.
4.  Estrarre i percorsi di file dall'oggetto memoria globale chiamando [**DragQueryFile**](/windows/desktop/api/Shellapi/nf-shellapi-dragqueryfilea) una volta per ogni file, con *iFile* impostato sull'indice del file.
5.  Elaborare i percorsi di file in base alle esigenze e incollarli nell'applicazione.
6.  Chiamare [**ReleaseStgMedium**](/windows/win32/api/ole2/nf-ole2-releasestgmedium) e passare il puntatore alla struttura [**STGMEDIUM**](/windows/win32/api/objidl/ns-objidl-ustgmedium-r1) passata a [**IDataObject:: GetData**](/windows/win32/api/objidl/nf-objidl-idataobject-getdata) nel passaggio 1. Una volta rilasciata la struttura, il valore di HDROP creato nel passaggio 2 non è più valido e non deve essere utilizzato.

## <a name="copying-the-contents-of-a-dropped-file-into-an-application"></a>Copia del contenuto di un file eliminato in un'applicazione

**Scenario:** Un utente trascina uno o più file da Esplora risorse e li rilascia nella finestra dell'applicazione. L'applicazione estrae il contenuto dei file e lo incolla nell'applicazione.

Questo scenario usa il trascinamento della selezione per trasferire i file da Esplora risorse all'applicazione. Prima dell'operazione, l'applicazione deve:

1.  Chiamare [RegisterClipboardFormat](/windows/win32/api/winuser/nf-winuser-registerclipboardformata) per registrare tutti i formati degli Appunti della Shell necessari.
2.  Chiamare [**RegisterDragDrop**](/windows/win32/api/ole2/nf-ole2-registerdragdrop) per registrare una finestra di destinazione e l'interfaccia [**IDropTarget**](/windows/win32/api/oleidl/nn-oleidl-idroptarget) dell'applicazione.

Dopo che l'utente ha avviato l'operazione selezionando uno o più file e iniziando a trascinarli:

1.  Esplora risorse crea un oggetto dati e vi carica i formati supportati.
2.  Esplora risorse chiama [**DoDragDrop**](/windows/win32/api/ole2/nf-ole2-dodragdrop) per avviare il ciclo di trascinamento.
3.  Quando l'immagine di trascinamento raggiunge la finestra di destinazione, il sistema invia una notifica chiamando [**IDropTarget::D ragenter**](/windows/win32/api/oleidl/nf-oleidl-idroptarget-dragenter).
4.  Per determinare il contenuto dell'oggetto dati, chiamare il metodo [**IDataObject:: EnumFormatEtc**](/windows/win32/api/objidl/nf-objidl-idataobject-enumformatetc) dell'oggetto dati. Utilizzare l'oggetto enumeratore restituito dal metodo per enumerare i formati contenuti nell'oggetto dati. Se l'applicazione non vuole accettare uno di questi formati, restituire DROPEFFECT \_ None. Ai fini di questo scenario, l'applicazione deve ignorare tutti gli oggetti dati che non contengono formati usati per trasferire i file, ad esempio [CF \_ HDROP](clipboard.md).
5.  Quando l'utente rilascia i dati, il sistema chiama [**IDropTarget::D por**](/windows/win32/api/oleidl/nf-oleidl-idroptarget-drop).
6.  Utilizzare l'interfaccia [**IDataObject**](/windows/win32/api/objidl/nn-objidl-idataobject) per estrarre il contenuto dei file.

Esistono diversi modi per estrarre il contenuto di un oggetto Shell da un oggetto dati. In generale, utilizzare l'ordine seguente:

-   Se il file contiene un formato di [ \_ testo CF](clipboard.md) , i dati sono testo ANSI. È possibile utilizzare il \_ formato di testo CF per estrarre i dati, anziché aprire il file stesso.
-   Se il file contiene un oggetto OLE collegato o incorporato, l'oggetto dati contiene un \_ formato CF EMBEDDEDOBJECT. Utilizzare le tecniche OLE standard per estrarre i dati. [I file di scarto](#creating-and-importing-scrap-files) contengono sempre un \_ formato CF EMBEDDEDOBJECT.
-   Se l'oggetto Shell viene dal file system, l'oggetto dati contiene un formato [CF \_ HDROP](clipboard.md) con i nomi dei file. Estrarre il nome file da [CF \_ HDROP](clipboard.md) e chiamare [**OleCreateFromFile**](/windows/win32/api/ole2/nf-ole2-olecreatefromfile) per creare un nuovo oggetto collegato o incorporato. Per informazioni su come recuperare un nome file da un formato [CF \_ HDROP](clipboard.md) , vedere [copia dei nomi di file dagli Appunti in un'applicazione](#copying-file-names-from-the-clipboard-to-an-application).
-   Se l'oggetto dati contiene un [formato \_ FileDescriptor CFSTR](clipboard.md) , è possibile estrarre il contenuto di un file dal formato [ \_ fileContents CFSTR](clipboard.md) del file. Per una descrizione di questa procedura, vedere [uso del \_ formato fileContents CFSTR per estrarre i dati da un file](/windows).
-   Prima della shell [versione 4,71](versions.md), un'applicazione indicava che era in corso il trasferimento di un tipo di file di collegamento impostando **FD \_ LINKUI** nel membro **dwFlags** della struttura [**FileDescriptor**](/windows/win32/api/shlobj_core/ns-shlobj_core-filedescriptora) . Per le versioni successive della shell, il modo migliore per indicare che i collegamenti vengono trasferiti consiste nell'usare il formato [CFSTR \_ PREFERREDDROPEFFECT](clipboard.md) impostato su DropEffect \_ collegamento. Questo approccio è molto più efficiente rispetto all'estrazione della struttura **FileDescriptor** solo per la verifica di un flag.

Se il processo di estrazione dei dati sarà lungo, potrebbe essere necessario eseguire l'operazione in modo asincrono in un thread in background. Il thread principale può procedere senza inutili ritardi. Per informazioni su come gestire l'estrazione asincrona dei dati, vedere [trascinamento e rilascio di oggetti Shell in modo asincrono](#dragging-and-dropping-shell-objects-asynchronously).

### <a name="using-the-cfstr_filecontents-format-to-extract-data-from-a-file"></a>Uso del \_ formato FILEcontents CFSTR per estrarre i dati da un file

Il [formato \_ fileContents di CFSTR](clipboard.md) fornisce un modo molto flessibile e potente per trasferire il contenuto di un file. Non è nemmeno necessario che i dati vengano archiviati come file singolo. Tutto ciò che è necessario per questo formato è che l'oggetto dati presenta i dati alla destinazione come se si trattasse di un file. Ad esempio, i dati effettivi potrebbero essere una sezione di un documento di testo o un blocco di dati estratti da un database. La destinazione può trattare i dati come file e non è necessario conoscere il meccanismo di archiviazione sottostante.

Le estensioni dello spazio dei nomi usano in genere i [ \_ contenuti fileCFSTR](clipboard.md) per trasferire i dati perché questo formato non presuppone alcun meccanismo di archiviazione specifico. Un'estensione dello spazio dei nomi può utilizzare qualsiasi meccanismo di archiviazione pratico e utilizzare questo formato per presentare gli oggetti alle applicazioni come se si trattasse di file.

Il meccanismo di trasferimento dei dati per i [ \_ FileContent CFSTR](clipboard.md) è in genere [TYMED \_ IStream](dataobject.md). Il trasferimento di un puntatore a interfaccia [**IStream**](/windows/win32/api/objidl/nn-objidl-istream) richiede molto meno memoria rispetto al caricamento dei dati in un oggetto memoria globale e **IStream** è un modo più semplice per rappresentare i dati rispetto a [**IStorage**](/windows/win32/api/objidl/nn-objidl-istorage).

Un [formato \_ fileContents di CFSTR](clipboard.md) è sempre accompagnato da un formato [ \_ FileDescriptor CFSTR](clipboard.md) . Per prima cosa è necessario esaminare il contenuto di questo formato. Se è in corso il trasferimento di più di un file, l'oggetto dati conterrà più formati [ \_ fileContents CFSTR](clipboard.md) , uno per ogni file. Il formato di [ \_ FileDescriptor CFSTR](clipboard.md) contiene il nome e gli attributi di ogni file e fornisce un valore di indice per ogni file necessario per estrarre il formato dei file [CFSTR \_ ](clipboard.md) di un determinato file.

Per estrarre un formato [CFSTR \_ fileContents](clipboard.md) :

1.  Estrarre il formato [CFSTR \_ FileDescriptor](clipboard.md) come valore [TYMED \_ HGLOBAL](dataobject.md) .
2.  Il membro **hGlobal** della struttura [**STGMEDIUM**](/windows/win32/api/objidl/ns-objidl-ustgmedium-r1) restituita punta a un oggetto memoria globale. Bloccare l'oggetto passando il valore di **hGlobal** a [**funzione GlobalLock**](/windows/win32/api/winbase/nf-winbase-globallock).
3.  Eseguire il cast del puntatore restituito da [**funzione GlobalLock**](/windows/win32/api/winbase/nf-winbase-globallock) a un puntatore [**FILEGROUPDESCRIPTOR**](/windows/win32/api/shlobj_core/ns-shlobj_core-filegroupdescriptora) . Punterà a una struttura **FILEGROUPDESCRIPTOR** seguita da una o più strutture [**FileDescriptor**](/windows/win32/api/shlobj_core/ns-shlobj_core-filedescriptora) . Ogni struttura **FileDescriptor** contiene una descrizione di un file che è contenuto in uno dei formati [CFSTR \_ fileContents](clipboard.md) associati.
4.  Esaminare le strutture [**FileDescriptor**](/windows/win32/api/shlobj_core/ns-shlobj_core-filedescriptora) per determinare quale corrisponde al file che si desidera estrarre. L'indice in base zero di tale struttura **FileDescriptor** viene utilizzato per identificare il formato del file [CFSTR \_ fileContents](clipboard.md) . Poiché la dimensione di un blocco di memoria globale non è precisa per i byte, usare i membri **nFileSizeLow** e **nFileSizeHigh** della struttura per determinare il numero di byte che rappresentano il file nell'oggetto memoria globale.
5.  Chiamare [**IDataObject:: GetData**](/windows/win32/api/objidl/nf-objidl-idataobject-getdata) con il membro **CfFormat** della struttura [**FORMATETC**](/windows/win32/api/objidl/ns-objidl-formatetc) impostata sul valore [CFSTR \_ fileContents](clipboard.md) e il membro **lIndex** impostato sull'indice determinato nel passaggio precedente. Il membro **TYMED** è in genere impostato su [TYMED \_ HGLOBAL](dataobject.md) \| TYMED \_ IStream \| TYMED \_ ISTORAGE. L'oggetto dati può quindi scegliere il meccanismo di trasferimento dei dati preferito.
6.  La struttura [**STGMEDIUM**](/windows/win32/api/objidl/ns-objidl-ustgmedium-r1) restituita da [**IDataObject:: GetData**](/windows/win32/api/objidl/nf-objidl-idataobject-getdata) conterrà un puntatore ai dati del file. Esaminare il membro **TYMED** della struttura per determinare il meccanismo di trasferimento dei dati.
7.  Se **TYMED** è impostato su [TYMED \_ IStream](dataobject.md) o TYMED \_ ISTORAGE, utilizzare l'interfaccia per estrarre i dati. Se **TYMED** è impostato su TYMED \_ HGLOBAL, i dati sono contenuti in un oggetto memoria globale. Per informazioni su come estrarre i dati da un oggetto memoria globale, vedere la sezione *estrazione di un oggetto memoria globale da un oggetto dati* dell' [oggetto dati della shell](dataobject.md).
8.  Chiamare [**funzione GlobalLock**](/windows/win32/api/winbase/nf-winbase-globallock) per sbloccare l'oggetto memoria globale bloccato nel passaggio 2.

## <a name="handling-optimized-move-operations"></a>Gestione delle operazioni di spostamento ottimizzate

**Scenario:** Un file viene spostato dal file system a un'estensione dello spazio dei nomi utilizzando uno spostamento ottimizzato.

In un'operazione di spostamento convenzionale, la destinazione esegue una copia dei dati e l'origine Elimina l'originale. Questa procedura può risultare inefficiente perché richiede due copie dei dati. Con oggetti di grandi dimensioni, ad esempio i database, un'operazione di spostamento convenzionale potrebbe non essere ancora praticabile.

Con uno spostamento ottimizzato, la destinazione usa la conoscenza della modalità di archiviazione dei dati per gestire l'intera operazione di spostamento. Non esiste mai una seconda copia dei dati e non è necessario che l'origine elimini i dati originali. I dati della shell sono particolarmente adatti per gli spostamenti ottimizzati perché la destinazione può gestire l'intera operazione usando l'API shell. Un esempio tipico è lo stato di trasferimento di file. Quando la destinazione ha il percorso di un file da spostare, può usare [**SHFileOperation**](/windows/desktop/api/Shellapi/nf-shellapi-shfileoperationa) per spostarlo. Non è necessario che l'origine elimini il file originale.

> [!Note]  
> La shell USA in genere uno spostamento ottimizzato per spostare i file. Per gestire correttamente il trasferimento dei dati della shell, l'applicazione deve essere in grado di rilevare e gestire uno spostamento ottimizzato.

 

Lo spostamento ottimizzato viene gestito nel modo seguente:

1.  L'origine chiama [**DoDragDrop**](/windows/win32/api/ole2/nf-ole2-dodragdrop) con il parametro *DWEFFECT* impostato su DropEffect \_ Move per indicare che è possibile spostare gli oggetti di origine.
2.  La destinazione riceve il \_ valore di spostamento DropEffect tramite uno dei relativi metodi [**IDropTarget**](/windows/win32/api/oleidl/nn-oleidl-idroptarget) , a indicare che è consentito uno spostamento.
3.  La destinazione copia l'oggetto (spostamento non ottimizzato) o sposta l'oggetto (spostamento ottimizzato).
4.  La destinazione indica quindi all'origine se è necessario eliminare i dati originali.

    Uno spostamento ottimizzato è l'operazione predefinita, con i dati eliminati dalla destinazione. Per informare l'origine che è stato eseguito uno spostamento ottimizzato:

    -   -   La destinazione imposta il valore *pdwEffect* ricevuto tramite il metodo [**IDropTarget::D por**](/windows/win32/api/oleidl/nf-oleidl-idroptarget-drop) su un valore diverso da DROPEFFECT \_ Move. Viene in genere impostato su DROPEFFECT \_ None o DropEffect \_ Copy. Il valore verrà restituito all'origine da [**DoDragDrop**](/windows/win32/api/ole2/nf-ole2-dodragdrop).
        -   La destinazione chiama anche il metodo [**IDataObject:: SetData**](/windows/win32/api/objidl/nf-objidl-idataobject-setdata) dell'oggetto dati e lo passa a un identificatore di formato [CFSTR \_ PERFORMEDDROPEFFECT](clipboard.md) impostato su DropEffect \_ None. Questa chiamata al metodo è necessaria perché alcune destinazioni di rilascio potrebbero non impostare correttamente il parametro *pdwEffect* di [**DoDragDrop**](/windows/win32/api/ole2/nf-ole2-dodragdrop) . Il formato [CFSTR \_ PERFORMEDDROPEFFECT](clipboard.md) è il modo affidabile per indicare che è stato effettuato uno spostamento ottimizzato.

    Se la destinazione ha avuto uno spostamento non ottimizzato, i dati devono essere eliminati dall'origine. Per informare l'origine che è stato eseguito uno spostamento non ottimizzato:

    -   -   La destinazione imposta il valore *pdwEffect* ricevuto tramite il metodo [**IDropTarget::D por**](/windows/win32/api/oleidl/nf-oleidl-idroptarget-drop) DropEffect \_ Move. Il valore verrà restituito all'origine da [**DoDragDrop**](/windows/win32/api/ole2/nf-ole2-dodragdrop).
        -   La destinazione chiama anche il metodo [**IDataObject:: SetData**](/windows/win32/api/objidl/nf-objidl-idataobject-setdata) dell'oggetto dati e lo passa a un identificatore di formato [CFSTR \_ PERFORMEDDROPEFFECT](clipboard.md) impostato su DropEffect \_ Move. Questa chiamata al metodo è necessaria perché alcune destinazioni di rilascio potrebbero non impostare correttamente il parametro *pdwEffect* di [**DoDragDrop**](/windows/win32/api/ole2/nf-ole2-dodragdrop) . Il formato [CFSTR \_ PERFORMEDDROPEFFECT](clipboard.md) è il modo affidabile per indicare che si è verificato uno spostamento non ottimizzato.

5.  L'origine controlla i due valori che possono essere restituiti dalla destinazione. Se entrambe le impostazioni sono impostate su DROPEFFECT \_ Move, viene completato lo spostamento non ottimizzato eliminando i dati originali. In caso contrario, la destinazione ha avuto uno spostamento ottimizzato e i dati originali sono stati eliminati.

## <a name="handling-delete-on-paste-operations"></a>Gestione delle operazioni delete-on-paste

**Scenario:** Uno o più file vengono tagliati da una cartella in Esplora risorse e incollati in un'estensione dello spazio dei nomi. Esplora risorse lascia i file evidenziati fino a quando non riceve commenti sul risultato dell'operazione Incolla.

Tradizionalmente, quando un utente taglia i dati, scompare immediatamente dalla visualizzazione. Questo potrebbe non essere efficiente e può causare problemi di usabilità se l'utente si preoccupa di ciò che si è verificato ai dati. Un approccio alternativo consiste nell'usare un'operazione Delete-on-paste.

Con un'operazione Delete-on-paste, i dati selezionati non vengono rimossi immediatamente dalla visualizzazione. Al contrario, l'applicazione di origine lo contrassegna come selezionata, forse modificando il tipo di carattere o il colore di sfondo. Dopo che l'applicazione di destinazione ha incollato i dati, notifica all'origine il risultato dell'operazione. Se la destinazione ha eseguito uno [spostamento ottimizzato](#handling-optimized-move-operations), l'origine può semplicemente aggiornarne la visualizzazione. Se la destinazione ha eseguito uno spostamento normale, è necessario che l'origine elimini anche la copia dei dati. Se la copia non riesce, l'applicazione di origine Ripristina i dati selezionati nell'aspetto originale.

> [!Note]  
> La shell USA in genere Delete-on-paste quando viene usata un'operazione Taglia/Incolla per spostare i file. Le operazioni delete-on-paste con gli oggetti Shell usano normalmente uno [spostamento ottimizzato](#handling-optimized-move-operations) per spostare i file. Per gestire correttamente il trasferimento dei dati della shell, l'applicazione deve essere in grado di rilevare e gestire operazioni delete-on-paste.

 

Il requisito essenziale per Delete-on-paste è che la destinazione deve segnalare il risultato dell'operazione all'origine. Tuttavia, le tecniche degli Appunti standard non possono essere usate per implementare Delete-on-paste perché non forniscono un modo per la comunicazione della destinazione con l'origine. Al contrario, l'applicazione di destinazione usa il metodo [**IDataObject:: SetData**](/windows/win32/api/objidl/nf-objidl-idataobject-setdata) dell'oggetto dati per segnalare il risultato all'oggetto dati. L'oggetto dati può quindi comunicare con l'origine tramite un'interfaccia privata.

La procedura di base per un'operazione Delete-on-paste è la seguente:

1.  Il codice sorgente contrassegna la visualizzazione dei dati selezionati.
2.  L'origine crea un oggetto dati. Indica un'operazione di taglio aggiungendo il formato [CFSTR \_ PREFERREDDROPEFFECT](clipboard.md) con un valore di dati di DropEffect \_ Move.
3.  L'origine posiziona l'oggetto dati negli appunti usando [**OleSetClipboard**](/windows/win32/api/ole2/nf-ole2-olesetclipboard).
4.  La destinazione recupera l'oggetto dati dagli appunti usando [**OleGetClipboard**](/windows/win32/api/ole2/nf-ole2-olegetclipboard).
5.  La destinazione estrae i dati di [ \_ PREFERREDDROPEFFECT CFSTR](clipboard.md) . Se è impostato su DROPEFFECT \_ Move, la destinazione può eseguire uno spostamento ottimizzato o semplicemente copiare i dati.
6.  Se la destinazione non esegue uno spostamento ottimizzato, chiama il metodo [**IDataObject:: SetData**](/windows/win32/api/objidl/nf-objidl-idataobject-setdata) con il formato [CFSTR \_ PERFORMEDDROPEFFECT](clipboard.md) impostato su DropEffect \_ Move.
7.  Al termine della copia, la destinazione chiama il metodo [**IDataObject:: SetData**](/windows/win32/api/objidl/nf-objidl-idataobject-setdata) con il formato [CFSTR \_ PASTESUCCEEDED](clipboard.md) impostato su DropEffect \_ Move.
8.  Quando il metodo [**IDataObject:: SetData**](/windows/win32/api/objidl/nf-objidl-idataobject-setdata) dell'origine viene chiamato con il formato [CFSTR \_ PASTESUCCEEDED](clipboard.md) impostato su DropEffect \_ Move, deve verificare se è stato ricevuto anche il formato [CFSTR \_ PERFORMEDDROPEFFECT](clipboard.md) impostato su DropEffect \_ Move. Se entrambi i formati vengono inviati dalla destinazione, l'origine dovrà eliminare i dati. Se viene ricevuto solo il formato [CFSTR \_ PASTESUCCEEDED](clipboard.md) , l'origine può semplicemente rimuovere i dati dalla relativa visualizzazione. Se il trasferimento non riesce, l'origine aggiorna la visualizzazione all'aspetto originale.

## <a name="transfering-data-to-and-from-virtual-folders"></a>Trasferimento di dati da e verso cartelle virtuali

**Scenario:** Un utente trascina un oggetto da o lo rilascia in una cartella virtuale.

Le cartelle virtuali contengono oggetti che in genere non fanno parte del file system. Alcune cartelle virtuali, ad esempio il Cestino, possono rappresentare dati archiviati sul disco rigido, ma non come oggetti file system ordinari. Alcuni possono rappresentare dati archiviati che si trovano in un sistema remoto, ad esempio un PC palmare o un sito FTP. Altri, ad esempio la cartella stampanti, contengono oggetti che non rappresentano dati archiviati. Mentre alcune cartelle virtuali fanno parte del sistema, gli sviluppatori possono anche creare e installare cartelle virtuali personalizzate implementando un'estensione dello spazio dei nomi.

Indipendentemente dal tipo di dati o dal modo in cui vengono archiviati, la shell e gli oggetti file contenuti in una cartella virtuale vengono presentati dalla shell come se fossero file e cartelle normali. È responsabilità della cartella virtuale prendere tutti i dati che contiene e presentarli in modo appropriato. Questo requisito significa che le cartelle virtuali normalmente supportano il trascinamento della selezione e i trasferimenti di dati degli Appunti.

Sono pertanto presenti due gruppi di sviluppatori che devono essere interessati al trasferimento di dati da e verso le cartelle virtuali:

-   Sviluppatori le cui applicazioni devono accettare i dati trasferiti da una cartella virtuale.
-   Sviluppatori le cui estensioni dello spazio dei nomi devono supportare correttamente il trasferimento dei dati.

### <a name="accepting-data-from-a-virtual-folder"></a>Accettazione di dati da una cartella virtuale

Le cartelle virtuali possono rappresentare praticamente qualsiasi tipo di dati e possono archiviare i dati nel modo scelto. Alcune cartelle virtuali potrebbero contenere effettivamente file e cartelle file system normali. Altri potrebbero, ad esempio, comprimere tutti i relativi oggetti in un singolo documento o database.

Quando un oggetto file system viene trasferito a un'applicazione, l'oggetto dati contiene normalmente un formato [CF \_ HDROP](clipboard.md) con il percorso completo dell'oggetto. L'applicazione può estrarre questa stringa e usare le normali funzioni di file system per aprire il file ed estrarre i dati. Tuttavia, poiché le cartelle virtuali non contengono in genere oggetti file system normali, in genere non usano [CF \_ HDROP](clipboard.md).

Invece di [CF \_ HDROP](clipboard.md), i dati vengono normalmente trasferiti dalle cartelle virtuali con i formati [CFSTR \_ FileDescriptor](clipboard.md) / [CFSTR \_ fileContents](clipboard.md) . Il [formato \_ fileContents di CFSTR](clipboard.md) presenta due vantaggi rispetto a [CF \_ HDROP](clipboard.md):

-   Non viene presupposto alcun metodo specifico di archiviazione dati.
-   Il formato è più flessibile. Supporta tre meccanismi di trasferimento dei dati: un oggetto memoria globale, un'interfaccia [**IStream**](/windows/win32/api/objidl/nn-objidl-istream) o un'interfaccia [**IStorage**](/windows/win32/api/objidl/nn-objidl-istorage) .

Gli oggetti memoria globale vengono utilizzati raramente per trasferire dati da o verso oggetti virtuali, in quanto i dati devono essere copiati interamente in memoria. Il trasferimento di un puntatore a interfaccia richiede quasi nessuna memoria ed è molto più efficiente. Con file di grandi dimensioni, un puntatore di interfaccia potrebbe essere l'unico meccanismo pratico di trasferimento dei dati. In genere, i dati sono rappresentati da un puntatore [**IStream**](/windows/win32/api/objidl/nn-objidl-istream) , perché tale interfaccia è leggermente più flessibile rispetto a [**IStorage**](/windows/win32/api/objidl/nn-objidl-istorage). La destinazione estrae il puntatore dall'oggetto dati e utilizza i metodi di interfaccia per estrarre i dati.

Per ulteriori informazioni su come gestire i formati [CFSTR \_ FileDescriptor](clipboard.md) / [CFSTR \_ fileContents](clipboard.md) , vedere l'articolo relativo all' [utilizzo del \_ formato fileContents di CFSTR per estrarre i dati da un file](/windows).

### <a name="transferring-data-to-and-from-a-namespace-extension"></a>Trasferimento di dati da e verso un'estensione dello spazio dei nomi

Quando si implementa un'estensione dello spazio dei nomi, in genere si vogliono supportare le funzionalità di trascinamento della selezione. Seguire le indicazioni per eliminare le origini e le destinazioni descritte in [linee guida generali](#general-guidelines). In particolare, un'estensione dello spazio dei nomi deve:

-   Essere in grado di gestire i formati [CFSTR \_ FileDescriptor](clipboard.md) / [CFSTR \_ fileContents](clipboard.md) . Questi due formati vengono in genere utilizzati per trasferire oggetti da e verso le estensioni dello spazio dei nomi.
-   Essere in grado di gestire gli [spostamenti ottimizzati](#handling-optimized-move-operations). La shell prevede che gli oggetti Shell verranno spostati con uno spostamento ottimizzato.
-   Essere in grado di gestire un'operazione di [eliminazione su Incolla](#handling-delete-on-paste-operations) . La shell USA Delete-on-paste quando gli oggetti vengono spostati dalla shell con un'operazione Taglia/Incolla.
-   Essere in grado di gestire il trasferimento dei dati tramite un'interfaccia [**IStream**](/windows/win32/api/objidl/nn-objidl-istream) o [**IStorage**](/windows/win32/api/objidl/nn-objidl-istorage) . Il trasferimento dei dati da o verso una cartella virtuale viene normalmente gestito trasferendo uno di questi due puntatori di interfaccia, in genere un puntatore **IStream** . La destinazione chiama quindi i metodi di interfaccia per estrarre i dati:
    -   -   Come origine di rilascio, l'estensione dello spazio dei nomi deve estrarre i dati dall'archivio e passarli attraverso questa interfaccia alla destinazione.
        -   Come destinazione di rilascio, un'estensione dello spazio dei nomi deve accettare i dati da un'origine tramite questa interfaccia e archiviarli in modo corretto.

## <a name="dropping-files-on-the-recycle-bin"></a>Eliminazione di file nel cestino

**Scenario:** L'utente rilascia un file nel **Cestino**. L'estensione dell'applicazione o dello spazio dei nomi elimina il file originale.

Il cestino è una cartella virtuale che viene usata come repository per i file che non sono più necessari. Fino a quando il cestino non è stato svuotato, l'utente può recuperare il file in un secondo momento e restituirlo alla file system.

Per la maggior parte, il trasferimento di oggetti Shell al cestino funziona in modo analogo a qualsiasi altra cartella. Tuttavia, quando un utente rilascia un file nel **Cestino**, l'origine deve eliminare l'originale, anche se il feedback della cartella indica un'operazione di copia. In genere, un'origine di rilascio non è in grado di conoscere la cartella in cui è stato rilasciato l'oggetto dati. Tuttavia, per i sistemi Windows 2000 e versioni successive, quando un oggetto dati viene rilasciato nel **Cestino**, la shell chiamerà il metodo [**IDataObject:: SetData**](/windows/win32/api/objidl/nf-objidl-idataobject-setdata) dell'oggetto dati con un formato [CFSTR \_ TARGETCLSID](clipboard.md) impostato sull'identificatore di classe (CLSID) del cestino (CLSID \_ RecycleBin). Per gestire correttamente il case del cestino, l'oggetto dati deve essere in grado di riconoscere questo formato e comunicare le informazioni all'origine tramite un'interfaccia privata.

> [!Note]  
> Quando [**IDataObject:: SetData**](/windows/win32/api/objidl/nf-objidl-idataobject-setdata) viene chiamato con un formato [CFSTR \_ TARGETCLSID](clipboard.md) impostato su CLSID \_ RecycleBin, l'origine dati deve chiudere tutti gli handle aperti per gli oggetti che vengono trasferiti prima di restituire dal metodo. In caso contrario, è possibile creare violazioni di condivisione.

 

## <a name="creating-and-importing-scrap-files"></a>Creazione e importazione di file di scarto

**Scenario:** Un utente trascina alcuni dati dal file di dati di un'applicazione OLE e li rilascia sul desktop o su Esplora risorse.

Windows consente agli utenti di trascinare un oggetto dal file di dati di un'applicazione OLE e di rilasciarlo sul desktop o in una cartella file system. Questa operazione crea un *file di frammento* che contiene i dati o un collegamento ai dati. Il nome del file viene tratto dal nome breve registrato per il CLSID dell'oggetto e i dati [di \_ testo CF](clipboard.md) . Per la creazione di un file di frammento contenente i dati da parte della shell, l'interfaccia [**IDataObject**](/windows/win32/api/objidl/nn-objidl-idataobject) dell'applicazione deve supportare il \_ formato degli Appunti EMBEDSOURCE di CF. Per creare un file contenente un collegamento, **IDataObject** deve supportare il \_ formato CF LINKSOURCE.

Sono inoltre disponibili tre funzionalità facoltative che un'applicazione può implementare per supportare i file di scarto:

-   Supporto round trip
-   Formati di dati memorizzati nella cache
-   Rendering ritardato

### <a name="round-trip-support"></a>Supporto round trip

Un *round trip* comporta il trasferimento di un oggetto dati in un altro contenitore e quindi di nuovo al documento originale. Ad esempio, un utente può trasferire un gruppo di celle da un foglio di calcolo al desktop, creando un file di scarto con i dati. Se l'utente trasferisce di nuovo il frammento al foglio di calcolo, è necessario integrare i dati nel documento come prima del trasferimento originale.

Quando la shell crea il file di scarto, rappresenta i dati come un oggetto di incorporamento. Quando lo scarto viene trasferito in un altro contenitore, viene trasferito come oggetto di incorporamento, anche se viene restituito al documento originale. L'applicazione è responsabile della determinazione del formato dati contenuto nel frammento e della restituzione dei dati nel formato nativo, se necessario.

Per stabilire il formato dell'oggetto incorporato, determinare il relativo CLSID recuperando il formato CF OBJECTDESCRIPTOR dell'oggetto \_ . Se il CLSID indica un formato di dati appartenente all'applicazione, deve trasferire i dati nativi anziché chiamare [**OleCreateFromData**](/windows/win32/api/ole2/nf-ole2-olecreatefromdata).

### <a name="cached-data-formats"></a>Formati di dati memorizzati nella cache

Quando la shell crea un file di scarto, verifica il registro di sistema per l'elenco dei formati disponibili. Per impostazione predefinita, sono disponibili due formati: CF \_ EMBEDSOURCE e CF \_ LINKSOURCE. Esistono tuttavia diversi scenari in cui è possibile che le applicazioni debbano includere file di scarto in formati diversi:

-   Per consentire il trasferimento degli sfridi a contenitori non OLE, che non possono accettare formati di oggetti incorporati.
-   Per consentire ai gruppi di applicazioni di comunicare con un formato privato.
-   Per semplificare la gestione di round trip.

Le applicazioni possono aggiungere formati al frammento tramite la memorizzazione nella cache nel registro di sistema. Esistono due tipi di formati memorizzati nella cache:

-   Formati di cache con priorità. Per questi formati, i dati vengono copiati integralmente nello scarto dall'oggetto dati.
-   Formati con rendering ritardato. Per questi formati, l'oggetto dati non viene copiato nel frammento. Il rendering viene invece posticipato fino a quando una destinazione non richiede i dati. Il rendering ritardato viene illustrato più dettagliatamente nella sezione successiva.

Per aggiungere una cache con priorità o un formato con rendering ritardato, creare una sottochiave **DataFormat** sotto la chiave **CLSID** dell'applicazione che rappresenta l'origine dei dati. In tale sottochiave creare una sottochiave **PriorityCacheFormats** o **DelayRenderFormats** . Per ogni cache con priorità o il formato con rendering ritardato, creare una sottochiave numerata a partire da zero. Impostare il valore di questa chiave su una stringa con il nome registrato del formato o un \# valore x, dove x rappresenta il numero del formato degli Appunti standard.

Nell'esempio seguente vengono illustrati i formati memorizzati nella cache per due applicazioni. L'applicazione MyProg1 ha il formato Rich Text come formato della cache prioritario e un formato privato "My Format" come formato con rendering ritardato. L'applicazione MyProg2 ha il \_ formato bitmap CF ( \# 8 ") come formato di cache prioritario.

```
HKEY_CLASSES_ROOT
   CLSID
      {GUID}
         (Default) = MyProg1
         DataFormats
            PriorityCacheFormats
               0
                  (Default) = Rich Text Format
            DelayRenderFormats
               0
                  (Default) = My Format
      {GUID}
         (Default) = MyProg2
         DataFormats
            PriorityCacheFormats
               0
                  (Default) = #8
```

È possibile aggiungere formati aggiuntivi creando sottochiavi numerate aggiuntive.

### <a name="delayed-rendering"></a>Rendering ritardato

Un formato di rendering ritardato consente a un'applicazione di creare un file di scarto, ma ritardare i costi di rendering dei dati fino a quando non vengono richiesti da una destinazione. L'interfaccia [**IDataObject**](/windows/win32/api/objidl/nn-objidl-idataobject) di un frammento offrirà i formati di rendering ritardati alla destinazione insieme ai dati nativi e memorizzati nella cache. Se la destinazione richiede un formato di rendering ritardato, la shell eseguirà l'applicazione e fornirà i dati alla destinazione dall'oggetto attivo.

> [!Note]  
> Poiché il rendering ritardato è piuttosto rischioso, è consigliabile utilizzarlo con cautela. Non funzionerà se il server non è disponibile o se le applicazioni non sono abilitate per OLE.

 

## <a name="dragging-and-dropping-shell-objects-asynchronously"></a>Trascinamento e rilascio di oggetti Shell in modo asincrono

**Scenario:** Un utente trasferisce un blocco di dati di grandi dimensioni dall'origine alla destinazione. Per evitare di bloccare entrambe le applicazioni per un periodo di tempo significativo, la destinazione estrae i dati in modo asincrono.

In genere, il trascinamento della selezione è un'operazione sincrona. In breve:

1.  L'origine di rilascio chiama [**DoDragDrop**](/windows/win32/api/ole2/nf-ole2-dodragdrop) e blocca il thread primario finché la funzione non restituisce. Il blocco del thread primario normalmente blocca l'elaborazione dell'interfaccia utente.
2.  Dopo la chiamata al metodo [**IDropTarget::D por**](/windows/win32/api/oleidl/nf-oleidl-idroptarget-drop) della destinazione, la destinazione estrae i dati dall'oggetto dati nel relativo thread primario. Questa procedura blocca in genere l'elaborazione dell'interfaccia utente della destinazione per la durata del processo di estrazione.
3.  Una volta estratti i dati, la destinazione restituisce la chiamata di [**IDropTarget::D por**](/windows/win32/api/oleidl/nf-oleidl-idroptarget-drop) , il sistema restituisce [**DoDragDrop**](/windows/win32/api/ole2/nf-ole2-dodragdrop)ed entrambi i thread possono continuare.

In breve, il trasferimento di dati sincrono può bloccare i thread primari di entrambe le applicazioni per un periodo di tempo significativo. In particolare, entrambi i thread devono attendere mentre la destinazione estrae i dati. Per piccole quantità di dati, il tempo necessario per estrarre i dati è ridotto e il trasferimento dei dati sincrono funziona correttamente. Tuttavia, l'estrazione sincrona di grandi quantità di dati può causare ritardi lunghi e interferire con l'interfaccia utente di destinazione e di origine.

L' [](/previous-versions//bb776309(v=vs.85)) / interfaccia [**IDataObjectAsyncCapability**](/windows/desktop/api/Shldisp/nn-shldisp-idataobjectasynccapability) di IAsyncOperation è un'interfaccia facoltativa che può essere implementata da un oggetto dati. Fornisce alla destinazione di rilascio la possibilità di estrarre i dati dall'oggetto dati in modo asincrono in un thread in background. Quando l'estrazione dei dati viene passata al thread in background, i thread primari di entrambe le applicazioni sono liberi di continuare.

### <a name="using-iasyncoperationidataobjectasynccapability"></a>Uso di IASyncOperation/IDataObjectAsyncCapability

> [!Note]  
> L'interfaccia era originariamente denominata [**IAsyncOperation**](/previous-versions//bb776309(v=vs.85)), ma in seguito è stata modificata in [**IDataObjectAsyncCapability**](/windows/desktop/api/Shldisp/nn-shldisp-idataobjectasynccapability). In caso contrario, le due interfacce sono identiche.

 

Lo scopo di [**IAsyncOperation**](/previous-versions//bb776309(v=vs.85)) / [**IDataObjectAsyncCapability**](/windows/desktop/api/Shldisp/nn-shldisp-idataobjectasynccapability) è consentire all'origine di rilascio e alla destinazione di rilascio di negoziare se i dati possono essere estratti in modo asincrono. La procedura seguente illustra il modo in cui l'origine di rilascio usa l'interfaccia:

1.  Creare un oggetto dati che espone [**IAsyncOperation**](/previous-versions//bb776309(v=vs.85)) / [**IDataObjectAsyncCapability**](/windows/desktop/api/Shldisp/nn-shldisp-idataobjectasynccapability).
2.  Chiamare [**SetAsyncMode**](/windows/desktop/api/Shldisp/nf-shldisp-idataobjectasynccapability-setasyncmode) con *FDoOpAsync* impostato su **Variant \_ true** per indicare che è supportata un'operazione asincrona.
3.  Dopo la restituzione di [**DoDragDrop**](/windows/win32/api/ole2/nf-ole2-dodragdrop) , chiamare [**inOperation**](/windows/desktop/api/Shldisp/nf-shldisp-idataobjectasynccapability-inoperation):
    -   Se l' [**inattività**](/windows/desktop/api/Shldisp/nf-shldisp-idataobjectasynccapability-inoperation) ha esito negativo o restituisce un valore **Variant \_ false**, viene eseguito un normale trasferimento dati sincrono e il processo di estrazione dei dati è terminato. L'origine deve eseguire la pulizia richiesta e continuare.
    -   Se [**Inoperate**](/windows/desktop/api/Shldisp/nf-shldisp-idataobjectasynccapability-inoperation) restituisce la **variante \_ true**, i dati vengono estratti in modo asincrono. Le operazioni di pulizia devono essere gestite da [**EndOperation**](/windows/desktop/api/Shldisp/nf-shldisp-idataobjectasynccapability-endoperation).
4.  Rilasciare l'oggetto dati.
5.  Al termine del trasferimento asincrono dei dati, l'oggetto dati notifica normalmente l'origine tramite un'interfaccia privata.

La procedura seguente illustra come la destinazione di rilascio usa l'interfaccia [](/previous-versions//bb776309(v=vs.85)) / [**IDataObjectAsyncCapability**](/windows/desktop/api/Shldisp/nn-shldisp-idataobjectasynccapability) di IAsyncOperation per estrarre i dati in modo asincrono:

1.  Quando il sistema chiama [**IDropTarget::D por**](/windows/win32/api/oleidl/nf-oleidl-idroptarget-drop), chiamare [**IDataObject:: QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) e richiedere un'interfaccia [**IAsyncOperation**](/previous-versions//bb776309(v=vs.85)) / [**IDataObjectAsyncCapability**](/windows/desktop/api/Shldisp/nn-shldisp-idataobjectasynccapability) (IID \_ IAsyncOperation/IID \_ IDataObjectAsyncCapability) dall'oggetto dati.
2.  Chiamare [**GetAsyncMode**](/windows/desktop/api/Shldisp/nf-shldisp-idataobjectasynccapability-getasyncmode). Se il metodo restituisce il valore **Variant \_ true**, l'oggetto dati supporta l'estrazione asincrona dei dati.
3.  Creare un thread separato per gestire l'estrazione dei dati e chiamare [**StartOperation**](/windows/desktop/api/Shldisp/nf-shldisp-idataobjectasynccapability-startoperation).
4.  Restituire la chiamata di [**IDropTarget::D por**](/windows/win32/api/oleidl/nf-oleidl-idroptarget-drop) , come per una normale operazione di trasferimento dei dati. [**DoDragDrop**](/windows/win32/api/ole2/nf-ole2-dodragdrop) restituirà e sblocca l'origine di rilascio. Non chiamare [**IDataObject:: SetData**](/windows/win32/api/objidl/nf-objidl-idataobject-setdata) per indicare il risultato di un'operazione di spostamento o eliminazione su Incolla ottimizzata. Attendere il completamento dell'operazione.
5.  Estrarre i dati nel thread in background. Il thread primario della destinazione è sbloccato e può continuare.
6.  Se il trasferimento dei dati era un'operazione di spostamento o [eliminazione su Incolla](#handling-delete-on-paste-operations) [ottimizzata](#handling-optimized-move-operations) , chiamare [**IDataObject:: SetData**](/windows/win32/api/objidl/nf-objidl-idataobject-setdata) per indicare il risultato.
7.  Notificare all'oggetto dati che l'estrazione è stata completata chiamando [**EndOperation**](/windows/desktop/api/Shldisp/nf-shldisp-idataobjectasynccapability-endoperation).

 

 
