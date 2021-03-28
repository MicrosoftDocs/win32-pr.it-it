---
description: L'oggetto dati è fondamentale per tutti i trasferimenti di dati della shell.
ms.assetid: c63d339e-ac62-4da1-b5ce-22d45a6a3413
title: Oggetto dati shell
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 812e5c18f5a2120fbf22682c6e768dc005128630
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104225926"
---
# <a name="shell-data-object"></a>Oggetto dati shell

L'oggetto dati è fondamentale per tutti i trasferimenti di dati della shell. Si tratta principalmente di un contenitore che consente di conservare i dati trasferiti. Tuttavia, la destinazione può comunicare anche con l'oggetto dati per facilitare alcuni tipi specializzati di trasferimento dei dati della shell, ad esempio gli spostamenti ottimizzati. In questo argomento viene fornita una descrizione generale del funzionamento degli oggetti dati della shell, della modalità di creazione da un'origine e del modo in cui vengono gestiti da una destinazione. Per una descrizione dettagliata di come usare gli oggetti dati per trasferire tipi diversi di dati della shell, vedere [gestione di scenari di trasferimento dati Shell](datascenarios.md).

-   [Funzionamento degli oggetti dati](#how-data-objects-work)
    -   [Formati degli Appunti](#clipboard-formats)
    -   [Struttura FORMATETC](#formatetc-structure)
    -   [Struttura STGMEDIUM](#stgmedium-structure)
-   [Creazione di un oggetto dati in un'origine](#how-a-source-creates-a-data-object)
    -   [Come aggiungere un oggetto memoria globale a un oggetto dati](#how-to-add-a-global-memory-object-to-a-data-object)
    -   [Implementazione di IDataObject](#implementing-idataobject)
    -   [Implementazione di IDropSource](#implementing-idropsource)
-   [Gestione di un oggetto dati in una destinazione](#how-a-target-handles-a-data-object)
    -   [Estrazione dei dati della shell da un oggetto dati](#extracting-shell-data-from-a-data-object)
    -   [Implementazione di IDropTarget](#implementing-idroptarget)
-   [Uso dell'oggetto helper di trascinamento della selezione](#using-the-drag-and-drop-helper-object)
    -   [Uso dell'interfaccia IDragSourceHelper](#using-the-idragsourcehelper-interface)
    -   [Uso dell'interfaccia IDropTargetHelper](#using-the-idroptargethelper-interface)

## <a name="how-data-objects-work"></a>Funzionamento degli oggetti dati

Gli oggetti dati sono oggetti Component Object Model (COM), creati dall'origine dati per trasferire i dati a una destinazione. In genere contengono più di un elemento di dati. Esistono due motivi per questa procedura:

-   Sebbene quasi tutti i tipi di dati possano essere trasferiti con un oggetto dati, l'origine non conosce in genere il tipo di dati che la destinazione può accettare. Ad esempio, i dati possono essere una parte di un documento di testo formattato. Sebbene la destinazione possa essere in grado di gestire informazioni di formattazione complesse, potrebbe anche essere in grado di accettare solo testo ANSI. Per questo motivo, gli oggetti dati includono spesso gli stessi dati in formati diversi. La destinazione può quindi estrarre i dati in un formato che è in grado di gestire.
-   Gli oggetti dati possono contenere anche elementi di dati ausiliari che non sono versioni dei dati di origine. Questo tipo di elemento di dati in genere fornisce informazioni aggiuntive sull'operazione di trasferimento dei dati. Ad esempio, la shell usa elementi di dati ausiliari per indicare se un file deve essere copiato o spostato.

### <a name="clipboard-formats"></a>Formati degli Appunti

A ogni elemento di dati in un oggetto dati è associato un formato, generalmente denominato *formato degli Appunti*. Sono disponibili diversi formati degli Appunti standard, dichiarati in winuser. h, che corrispondono ai tipi di dati usati comunemente. I formati degli Appunti sono numeri interi, ma in genere fanno riferimento al nome equivalente, che ha il formato CF \_ *xxx*. Ad esempio, il formato degli Appunti per il testo ANSI è il \_ testo CF.

Le applicazioni possono estendere la gamma di formati degli appunti disponibili definendo i formati privati. Per definire un formato privato, un'applicazione chiama [RegisterClipboardFormat](/windows/win32/api/winuser/nf-winuser-registerclipboardformata) con una stringa che identifica il formato. Il Unsigned Integer restituito dalla funzione è un valore di formato valido che può essere utilizzato come un formato degli Appunti standard. Tuttavia, l'origine e la destinazione devono registrare il formato per poterlo usare. Con un'eccezione,[CF \_ HDROP](clipboard.md), i formati degli Appunti usati per trasferire i dati della shell sono definiti come formati privati. Devono essere registrati dall'origine e dalla destinazione prima di poter essere usati. Per una descrizione dei formati degli Appunti della shell disponibili, vedere la pagina relativa ai formati degli Appunti della shell.

Sebbene esistano alcune eccezioni, in genere gli oggetti dati contengono un solo elemento di dati per ogni formato degli Appunti supportati. Questa correlazione uno-a-uno tra formato e dati consente di utilizzare il valore del formato come identificatore per l'elemento di dati associato. Infatti, quando si discute il contenuto di un oggetto dati, un particolare elemento di dati viene in genere chiamato "Format" e a cui fa riferimento il relativo nome di formato. Ad esempio, frasi come "Estrai il \_ formato di testo CF..." vengono in genere utilizzate quando si discute l'elemento dati di testo ANSI di un oggetto dati.

Quando l'obiettivo di rilascio riceve il puntatore all'oggetto dati, la destinazione di rilascio enumera i formati disponibili per determinare quali tipi di dati sono disponibili. Quindi richiede uno o più formati disponibili ed estrae i dati. Il modo specifico in cui la destinazione estrae i dati della shell da un oggetto dati varia in base al formato; questo argomento viene descritto in dettaglio in [come una destinazione gestisce un oggetto dati](#how-a-target-handles-a-data-object).

Con i trasferimenti di dati degli appunti semplici, i dati vengono inseriti in un oggetto memoria globale. L'indirizzo di tale oggetto viene inserito negli Appunti, insieme al relativo formato. Il formato degli Appunti indica alla destinazione il tipo di dati che troverà nell'indirizzo associato. Sebbene i trasferimenti di appunti semplici siano facili da implementare:

-   Gli oggetti dati forniscono un metodo molto più flessibile per trasferire i dati.
-   Gli oggetti dati sono più adatti per il trasferimento di grandi quantità di dati.
-   È necessario usare gli oggetti dati per trasferire i dati con un'operazione di trascinamento della selezione.

Per questi motivi, tutti i trasferimenti di dati della Shell utilizzano oggetti dati. Con gli oggetti dati, i formati degli Appunti non vengono usati direttamente. Al contrario, gli elementi di dati vengono identificati con una generalizzazione del formato degli Appunti, una struttura [**FORMATETC**](/windows/win32/api/objidl/ns-objidl-formatetc) .

### <a name="formatetc-structure"></a>Struttura FORMATETC

La struttura [**FORMATETC**](/windows/win32/api/objidl/ns-objidl-formatetc) è una versione estesa del formato degli Appunti. Come usato per i trasferimenti di dati della shell, la struttura **FORMATETC** presenta le caratteristiche seguenti:

-   Un elemento dati viene ancora identificato dal formato degli Appunti, nel membro **cfFormat** .
-   Il trasferimento dei dati non è limitato agli oggetti della memoria globale. Il membro **TYMED** viene usato per indicare il meccanismo di trasferimento dei dati contenuto nella struttura [**STGMEDIUM**](/windows/win32/api/objidl/ns-objidl-ustgmedium-r1) associata. Viene impostato su uno dei valori [**TYMED \_ xxx**](/windows/win32/api/objidl/ne-objidl-tymed) .
-   La shell usa il membro **lIndex** con il [formato \_ fileContents CFSTR](clipboard.md) per consentire a un oggetto dati di contenere più di un elemento di dati per formato. Per informazioni su come usare questo formato, vedere la sezione *uso del \_ formato fileContents CFSTR per estrarre i dati da un file in* [scenari di gestione della shell trasferimento dati](datascenarios.md).
-   Il membro **dwAspect** viene in genere impostato sul \_ contenuto di DVASPECT. Sono tuttavia disponibili tre valori definiti in Shlobj. h che possono essere utilizzati per il trasferimento dei dati della shell. 

    |                     |                                                                                                   |
    |---------------------|---------------------------------------------------------------------------------------------------|
    | copia di DVASPECT \_      | Utilizzato per indicare che il formato rappresenta una copia dei dati.                                   |
    | \_collegamento DVASPECT      | Utilizzato per indicare che il formato rappresenta un collegamento ai dati.                               |
    | DVASPECT \_ ShortName | Usato con il \_ formato CF HDROP per richiedere un percorso di file con i nomi abbreviati nel formato 8,3. |

    

     

-   Il membro **PTD** non viene usato per i trasferimenti di dati della shell ed è in genere impostato su **null**.

### <a name="stgmedium-structure"></a>Struttura STGMEDIUM

La struttura [**STGMEDIUM**](/windows/win32/api/objidl/ns-objidl-ustgmedium-r1) fornisce l'accesso ai dati trasferiti. Per i dati della shell sono supportati tre meccanismi di trasferimento dei dati:

-   Oggetto memoria globale.
-   Interfaccia [**IStream**](/windows/win32/api/objidl/nn-objidl-istream) .
-   Interfaccia [**IStorage**](/windows/win32/api/objidl/nn-objidl-istorage) .

Il membro **TYMED** della struttura [**STGMEDIUM**](/windows/win32/api/objidl/ns-objidl-ustgmedium-r1) è un valore [**TYMED \_ xxx**](/windows/win32/api/objidl/ne-objidl-tymed) che identifica il meccanismo di trasferimento dei dati. Il secondo membro è un puntatore usato dalla destinazione per estrarre i dati. Il puntatore può essere di una varietà di tipi, a seconda del valore di **TYMED** . I tre valori **TYMED** usati per i trasferimenti di dati della shell sono riepilogati nella tabella seguente, insieme al nome del membro **STGMEDIUM** corrispondente.



| Valore TYMED     | Nome del membro | Descrizione                                                                                                                                                                                                                                                                                                       |
|-----------------|-------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \_HGLOBAL TYMED  | **hGlobal** | Puntatore a un oggetto memoria globale. Questo tipo di puntatore viene in genere utilizzato per il trasferimento di piccole quantità di dati. Ad esempio, la shell usa gli oggetti memoria globale per trasferire stringhe di testo brevi, ad esempio nomi file o URL.                                                                                    |
| \_IStream TYMED  | **pstm**    | Puntatore a un'interfaccia [**IStream**](/windows/win32/api/objidl/nn-objidl-istream) . Questo tipo di puntatore è preferibile per la maggior parte dei trasferimenti di dati della shell perché richiede una quantità di memoria relativamente ridotta rispetto a TYMED \_ HGLOBAL. Inoltre, il \_ meccanismo di trasferimento dei dati di TYMED IStream non richiede che l'origine memorizzi i dati in un modo particolare. |
| \_ISTORAGE TYMED | **pstg**    | Puntatore a un'interfaccia [**IStorage**](/windows/win32/api/objidl/nn-objidl-istorage) . La destinazione chiama i metodi di interfaccia per estrarre i dati. Analogamente a TYMED \_ IStream, questo tipo di puntatore richiede una quantità di memoria relativamente ridotta. Tuttavia, poiché TYMED \_ ISTORAGE è meno flessibile di TYMED \_ IStream, non viene usato comunemente.                  |



 

## <a name="how-a-source-creates-a-data-object"></a>Creazione di un oggetto dati in un'origine

Quando un utente avvia un trasferimento dati della shell, l'origine è responsabile della creazione di un oggetto dati e del relativo caricamento con i dati. Nella procedura seguente viene riepilogato il processo:

1.  Chiamare [RegisterClipboardFormat](/windows/win32/api/winuser/nf-winuser-registerclipboardformata) per ottenere un valore di formato degli Appunti valido per ogni formato della shell che verrà incluso nell'oggetto dati. Tenere presente che [CF \_ HDROP](clipboard.md) è già un formato degli Appunti valido e non deve essere registrato.
2.  Per ogni formato da trasferire, inserire i dati associati in un oggetto memoria globale o creare un oggetto che fornisca l'accesso a tali dati tramite un'interfaccia [**IStream**](/windows/win32/api/objidl/nn-objidl-istream) o [**IStorage**](/windows/win32/api/objidl/nn-objidl-istorage) . Le interfacce **IStream** e **IStorage** vengono create utilizzando tecniche com standard. Per informazioni su come gestire gli oggetti della memoria globale, vedere [come aggiungere un oggetto memoria globale a un oggetto dati](#how-to-add-a-global-memory-object-to-a-data-object).
3.  Creare strutture [**FORMATETC**](/windows/win32/api/objidl/ns-objidl-formatetc) e [**STGMEDIUM**](/windows/win32/api/objidl/ns-objidl-ustgmedium-r1) per ogni formato.
4.  Creare un'istanza di un oggetto dati.
5.  Caricare i dati nell'oggetto dati chiamando il metodo [**IDataObject:: SetData**](/windows/win32/api/objidl/nf-objidl-idataobject-setdata) per ogni formato supportato e passando le strutture [**FORMATETC**](/windows/win32/api/objidl/ns-objidl-formatetc) e [**STGMEDIUM**](/windows/win32/api/objidl/ns-objidl-ustgmedium-r1) del formato.
6.  Con i trasferimenti di dati degli Appunti, chiamare [**OleSetClipboard**](/windows/win32/api/ole2/nf-ole2-olesetclipboard) per inserire un puntatore all'interfaccia [**IDataObject**](/windows/win32/api/objidl/nn-objidl-idataobject) dell'oggetto dati negli Appunti. Per i trasferimenti con trascinamento della selezione, avviare un *ciclo di trascinamento* chiamando [**DoDragDrop**](/windows/win32/api/ole2/nf-ole2-dodragdrop). Il puntatore **IDataObject** verrà passato all'obiettivo di rilascio quando i dati vengono eliminati, terminando il ciclo di trascinamento.

L'oggetto dati è ora pronto per essere trasferito alla destinazione. Per i trasferimenti di dati degli Appunti, l'oggetto viene semplicemente mantenuto fino a quando non viene richiesto dalla destinazione chiamando [**OleGetClipboard**](/windows/win32/api/ole2/nf-ole2-olegetclipboard). Per i trasferimenti di dati con trascinamento della selezione, l'oggetto dati è responsabile della creazione di un'icona per rappresentare i dati e dello spostamento quando l'utente sposta il cursore. Mentre l'oggetto si trova nel ciclo di trascinamento, l'origine riceve informazioni sullo stato tramite l'interfaccia [**IDropSource**](/windows/win32/api/oleidl/nn-oleidl-idropsource) . Per ulteriori informazioni, vedere [implementazione di IDropSource](#implementing-idropsource).

L'origine non riceve alcuna notifica se l'oggetto dati viene recuperato dagli Appunti da una destinazione. Quando un oggetto viene rilasciato in una destinazione mediante un'operazione di trascinamento della selezione, la funzione [**DoDragDrop**](/windows/win32/api/ole2/nf-ole2-dodragdrop) chiamata per avviare il ciclo di trascinamento restituirà.

### <a name="how-to-add-a-global-memory-object-to-a-data-object"></a>Come aggiungere un oggetto memoria globale a un oggetto dati

Molti formati di dati della shell sono sotto forma di oggetto memoria globale. Utilizzare la procedura seguente per creare un formato contenente un oggetto memoria globale e caricarlo nell'oggetto dati:

1.  Creare una struttura [**FORMATETC**](/windows/win32/api/objidl/ns-objidl-formatetc) . Impostare il membro **cfFormat** sul valore del formato degli Appunti appropriato e il membro **TYMED** su TYMED \_ HGLOBAL.
2.  Creare una struttura [**STGMEDIUM**](/windows/win32/api/objidl/ns-objidl-ustgmedium-r1) . Impostare il membro **TYMED** su TYMED \_ HGLOBAL.
3.  Creare un oggetto memoria globale chiamando [**GlobalAlloc**](/windows/win32/api/winbase/nf-winbase-globalalloc) per allocare un blocco di memoria opportunamente dimensionato.
4.  Assegnare il blocco di dati da trasferire all'indirizzo restituito da [**GlobalAlloc**](/windows/win32/api/winbase/nf-winbase-globalalloc).
5.  Assegnare l'indirizzo dell'oggetto memoria globale al membro **hGlobal** della struttura [**STGMEDIUM**](/windows/win32/api/objidl/ns-objidl-ustgmedium-r1) .
6.  Caricare il formato nell'oggetto dati chiamando [**IDataObject:: SetData**](/windows/win32/api/objidl/nf-objidl-idataobject-setdata) e passando le strutture [**FORMATETC**](/windows/win32/api/objidl/ns-objidl-formatetc) e [**STGMEDIUM**](/windows/win32/api/objidl/ns-objidl-ustgmedium-r1) create nei passaggi precedenti.

La funzione di esempio seguente crea un oggetto memoria globale contenente un valore **DWORD** e lo carica in un oggetto dati. Il parametro **pdtobj** è un puntatore all'interfaccia [**IDataObject**](/windows/win32/api/objidl/nn-objidl-idataobject) dell'oggetto dati, **CF** è il valore del formato degli Appunti e **DW** è il valore dei dati.


```C++
STDAPI DataObj_SetDWORD(IDataObject *pdtobj, UINT cf, DWORD dw)
{
    FORMATETC fmte = {(CLIPFORMAT) cf, 
                      NULL, 
                      DVASPECT_CONTENT, 
                      -1, 
                      TYMED_HGLOBAL};
    STGMEDIUM medium;

    HRESULT hres = E_OUTOFMEMORY;
    DWORD *pdw = (DWORD *)GlobalAlloc(GPTR, sizeof(DWORD));
    
    if (pdw)
    {
        *pdw = dw;       
        medium.tymed = TYMED_HGLOBAL;
        medium.hGlobal = pdw;
        medium.pUnkForRelease = NULL;

        hres = pdtobj->SetData(&fmte, &medium, TRUE);
 
        if (FAILED(hres))
            GlobalFree((HGLOBAL)pdw);
    }
    return hres;
}
```



### <a name="implementing-idataobject"></a>Implementazione di IDataObject

[**IDataObject**](/windows/win32/api/objidl/nn-objidl-idataobject) è l'interfaccia primaria di un oggetto dati. Deve essere implementato da tutti gli oggetti dati. Viene usato sia da origine che da destinazione per diversi scopi, tra cui:

-   Caricamento dei dati nell'oggetto dati.
-   Estrazione dei dati dall'oggetto dati.
-   Determinazione dei tipi di dati presenti nell'oggetto dati.
-   Invio di commenti e suggerimenti all'oggetto dati sul risultato del trasferimento dei dati.

[**IDataObject**](/windows/win32/api/objidl/nn-objidl-idataobject) supporta diversi metodi. In questa sezione viene illustrato come implementare i tre metodi più importanti per gli oggetti dati della shell, [SetData](#setdata-method), [EnumFormatEtc](#enumformatetc-method)e [GetData](#getdata-method). Per informazioni sugli altri metodi, vedere il riferimento a **IDataObject** .

### <a name="setdata-method"></a>SetData (metodo)

La funzione primaria del metodo [**IDataObject:: SetData**](/windows/win32/api/objidl/nf-objidl-idataobject-setdata) consente all'origine di caricare i dati nell'oggetto dati. Per includere ogni formato, l'origine crea una struttura [**FORMATETC**](/windows/win32/api/objidl/ns-objidl-formatetc) per identificare il formato e una struttura [**STGMEDIUM**](/windows/win32/api/objidl/ns-objidl-ustgmedium-r1) per contenere un puntatore ai dati. L'origine chiama quindi il metodo **IDataObject:: SetData** dell'oggetto e passa le strutture **FORMATETC** e **STGMEDIUM** del formato. Il metodo deve archiviare queste informazioni in modo che siano disponibili quando la destinazione chiama [**IDataObject:: GetData**](/windows/win32/api/objidl/nf-objidl-idataobject-getdata) per estrarre i dati dall'oggetto.

Tuttavia, durante il trasferimento di file, la shell spesso inserisce le informazioni per ogni file da trasferire in un formato [CFSTR \_ fileContents](clipboard.md) separato. Per distinguere i diversi file, il membro **lIndex** della struttura [**FORMATETC**](/windows/win32/api/objidl/ns-objidl-formatetc) di ogni file viene impostato su un valore di indice che identifica il file specifico. L'implementazione di [**IDataObject:: SetData**](/windows/win32/api/objidl/nf-objidl-idataobject-setdata) deve essere in grado di archiviare più \_ formati fileContents CFSTR che differiscono solo per i membri di **lIndex** .

Quando il cursore si trova sulla finestra di destinazione, la destinazione può usare l'oggetto di supporto per il [trascinamento della selezione](#using-the-drag-and-drop-helper-object) per specificare l'immagine di trascinamento. L'oggetto helper di trascinamento della selezione chiama [**IDataObject:: SetData**](/windows/win32/api/objidl/nf-objidl-idataobject-setdata) per caricare formati privati nell'oggetto dati utilizzati per il supporto tra processi. Per supportare l'oggetto helper di trascinamento della selezione, l'implementazione di **IDataObject:: SetData** deve essere in grado di accettare e archiviare formati privati arbitrari.

Una volta eliminati i dati, alcuni tipi di trasferimento dei dati della shell richiedono che la destinazione chiami [**IDataObject:: SetData**](/windows/win32/api/objidl/nf-objidl-idataobject-setdata) per fornire all'oggetto dati le informazioni sul risultato dell'operazione di rilascio. Ad esempio, quando si spostano i file con un'operazione di spostamento ottimizzata, la destinazione normalmente Elimina i file originali, ma non è necessario. La destinazione informa l'oggetto dati se i file sono stati eliminati chiamando **IDataObject:: SetData** con un formato [CFSTR \_ LOGICALPERFORMEDDROPEFFECT](clipboard.md) . Sono disponibili diversi altri [formati degli Appunti della shell](clipboard.md) utilizzati dalla destinazione per passare informazioni all'oggetto dati. L'implementazione di **IDataObject:: SetData** deve essere in grado di riconoscere questi formati e rispondere in modo appropriato. Per ulteriori informazioni, vedere [gestione degli scenari di trasferimento dati Shell](datascenarios.md).

### <a name="enumformatetc-method"></a>Metodo EnumFormatEtc

Quando la destinazione riceve un oggetto dati, in genere chiama [**FORMATETC**](/windows/win32/api/objidl/ns-objidl-formatetc) per determinare quali formati sono contenuti nell'oggetto. Il metodo crea un oggetto enumerazione OLE e restituisce un puntatore all'interfaccia [**IEnumFORMATETC**](/windows/win32/api/objidl/nn-objidl-ienumformatetc) dell'oggetto. La destinazione USA quindi l'interfaccia per enumerare i formati disponibili.

Un oggetto enumerazione deve sempre enumerare i formati disponibili in ordine di qualità, a partire dal migliore. La qualità relativa dei formati è definita dall'origine di rilascio. In generale, i formati di qualità superiore contengono i dati più ricchi e più completi. Ad esempio, un'immagine a 24 bit viene normalmente considerata di qualità superiore rispetto a una versione di tale immagine in scala di grigi. Il motivo per l'enumerazione dei formati in ordine di qualità consiste nel fatto che le destinazioni vengono in genere enumerate fino a raggiungere un formato supportato e quindi utilizzano tale formato per estrarre i dati. Affinché questa procedura produca il migliore formato disponibile che la destinazione può supportare, i formati devono essere enumerati in ordine di qualità.

Un oggetto di enumerazione per i dati della shell viene implementato in modo molto simile a quello di altri tipi di trasferimento dei dati, con un'eccezione rilevante. Poiché gli oggetti dati contengono in genere solo un elemento dati per formato, in genere enumerano ogni formato passato a [**IDataObject:: SetData**](/windows/win32/api/objidl/nf-objidl-idataobject-setdata). Tuttavia, come illustrato nella sezione relativa al [metodo SetData](#setdata-method) , gli oggetti dati della shell possono contenere più formati [ \_ fileContents di CFSTR](clipboard.md) .

Poiché lo scopo di [**IDataObject:: EnumFormatEtc**](/windows/win32/api/objidl/nf-objidl-idataobject-enumformatetc) è quello di consentire alla destinazione di determinare i tipi di dati presenti, non è necessario enumerare più di un formato [di \_ fileContents CFSTR](clipboard.md) . Se è necessario che la destinazione conosca il numero di formati contenuti nell'oggetto dati, la destinazione può recuperare tali informazioni dal \_ formato di FILEDESCRIPTOR CFSTR associato. Per ulteriori informazioni su come implementare **IDataObject:: EnumFormatEtc**, vedere la documentazione di riferimento del metodo.

### <a name="getdata-method"></a>GetData (metodo)

La destinazione chiama [**IDataObject:: GetData**](/windows/win32/api/objidl/nf-objidl-idataobject-getdata) per estrarre un particolare formato dati. La destinazione specifica il formato passando la struttura [**FORMATETC**](/windows/win32/api/objidl/ns-objidl-formatetc) appropriata. **IDataObject:: GetData** restituisce la struttura [**STGMEDIUM**](/windows/win32/api/objidl/ns-objidl-ustgmedium-r1) del formato.

La destinazione può impostare il membro **TYMED** della struttura [**FORMATETC**](/windows/win32/api/objidl/ns-objidl-formatetc) su un valore TYMED \_ *xxx* specifico per specificare il meccanismo di trasferimento dei dati che verrà utilizzato per estrarre i dati. Tuttavia, la destinazione può anche effettuare una richiesta più generica e consentire all'oggetto dati di decidere. Per richiedere all'oggetto dati di selezionare il meccanismo di trasferimento dei dati, la destinazione imposta tutti i valori TYMED \_ *xxx* supportati. [**IDataObject:: GetData**](/windows/win32/api/objidl/nf-objidl-idataobject-getdata) seleziona uno di questi meccanismi di trasferimento dei dati e restituisce la struttura [**STGMEDIUM**](/windows/win32/api/objidl/ns-objidl-ustgmedium-r1) appropriata. Ad esempio, **TYMED** è in genere impostato su TYMED \_ HGLOBAL \| TYMED \_ IStream \| TYMED \_ ISTORAGE per richiedere uno dei tre meccanismi di trasferimento dei dati della shell.

> [!Note]  
> Poiché possono essere presenti più [formati \_ fileContents CFSTR](clipboard.md) , i membri **cfFormat** e **TYMED** della struttura [**FORMATETC**](/windows/win32/api/objidl/ns-objidl-formatetc) non sono sufficienti per indicare la struttura [**STGMEDIUM**](/windows/win32/api/objidl/ns-objidl-ustgmedium-r1) di [**IDataObject:: GetData**](/windows/win32/api/objidl/nf-objidl-idataobject-getdata) che deve restituire. Per il \_ formato CFSTR FILEcontents, **IDataObject:: GetData** deve esaminare anche il membro **lIndex** della struttura **FORMATETC** per restituire la struttura **STGMEDIUM** corretta.

 

Il formato [CFSTR \_ INDRAGLOOP](clipboard.md) viene inserito in oggetti dati per consentire alle destinazioni di controllare lo stato del ciclo di trascinamento della selezione evitando il rendering intensivo della memoria dei dati dell'oggetto. I dati del formato sono un valore **DWORD** impostato su un valore diverso da zero se l'oggetto dati si trova all'interno di un ciclo di trascinamento. Il valore dei dati del formato è impostato su zero se i dati sono stati eliminati. Se una destinazione richiede questo formato e non è stato caricato dall'origine, [**IDataObject:: GetData**](/windows/win32/api/objidl/nf-objidl-idataobject-getdata) deve rispondere come se l'origine avesse caricato il formato con un valore pari a zero.

Quando il cursore si trova sulla finestra di destinazione, la destinazione può usare l'oggetto di supporto per il [trascinamento della selezione](#using-the-drag-and-drop-helper-object) per specificare l'immagine di trascinamento. L'oggetto helper di trascinamento della selezione chiama [**IDataObject:: SetData**](/windows/win32/api/objidl/nf-objidl-idataobject-setdata) per caricare formati privati nell'oggetto dati utilizzati per il supporto tra processi. In un secondo momento chiama [**IDataObject:: GetData**](/windows/win32/api/objidl/nf-objidl-idataobject-getdata) per recuperarli. Per supportare l'oggetto helper di trascinamento della selezione, l'implementazione dell'oggetto dati della shell deve essere in grado di restituire formati privati arbitrari quando vengono richiesti.

### <a name="implementing-idropsource"></a>Implementazione di IDropSource

L'origine deve creare un oggetto che espone un'interfaccia [**IDropSource**](/windows/win32/api/oleidl/nn-oleidl-idropsource) . Questa interfaccia consente all'origine di aggiornare l' *immagine di trascinamento* che indica la posizione corrente del cursore e di inviare commenti e suggerimenti al sistema su come terminare un'operazione di trascinamento della selezione. **IDropSource** dispone di due metodi: [**GiveFeedback**](/windows/win32/api/oleidl/nf-oleidl-idropsource-givefeedback) e [**QueryContinueDrag**](/windows/win32/api/oleidl/nf-oleidl-idropsource-querycontinuedrag).

### <a name="givefeedback-method"></a>GiveFeedback (metodo)

Nel ciclo di trascinamento, un'origine di rilascio è responsabile di tenere traccia della posizione del cursore e di visualizzare un'immagine di trascinamento appropriata. In alcuni casi, tuttavia, potrebbe essere necessario modificare l'aspetto dell'immagine di trascinamento quando si trova sulla finestra della destinazione di rilascio.

Quando il cursore entra o esce dalla finestra di destinazione e mentre si sposta sulla finestra di destinazione, il sistema chiama periodicamente l'interfaccia [**IDropTarget**](/windows/win32/api/oleidl/nn-oleidl-idroptarget) della destinazione. La destinazione risponde con un valore [**DropEffect**](../com/dropeffect-constants.md) che viene inviato all'origine tramite il metodo [**GiveFeedback**](/windows/win32/api/oleidl/nf-oleidl-idropsource-givefeedback) . Se necessario, l'origine può modificare l'aspetto del cursore in base al valore di **DropEffect** . Per ulteriori informazioni, vedere i riferimenti **GiveFeedback** e [**DoDragDrop**](/windows/win32/api/ole2/nf-ole2-dodragdrop) .

### <a name="querycontinuedrag-method"></a>QueryContinueDrag (metodo)

Questo metodo viene chiamato se il pulsante del mouse o lo stato della tastiera cambia mentre l'oggetto dati si trova nel ciclo di trascinamento. Invia una notifica all'origine se è stato premuto il tasto ESC e fornisce lo stato corrente dei tasti di modifica della tastiera, ad esempio CTRL o MAIUSC. Il valore restituito del metodo [**QueryContinueDrag**](/windows/win32/api/oleidl/nf-oleidl-idropsource-querycontinuedrag) specifica una delle tre azioni seguenti:

-   S \_ OK. Continua l'operazione di trascinamento
-   eliminazione del DRAGDROP \_ \_ . Eliminare i dati. Il sistema chiama quindi il metodo [**IDropTarget::D por**](/windows/win32/api/oleidl/nf-oleidl-idroptarget-drop) della destinazione.
-   DRAGDROP \_ S \_ Annulla. Terminare il ciclo di trascinamento senza eliminare i dati. Questo valore viene in genere restituito se è stato premuto il tasto di ESCAPE.

Per ulteriori informazioni, vedere i riferimenti [**QueryContinueDrag**](/windows/win32/api/oleidl/nf-oleidl-idropsource-querycontinuedrag) e [**DoDragDrop**](/windows/win32/api/ole2/nf-ole2-dodragdrop) .

## <a name="how-a-target-handles-a-data-object"></a>Gestione di un oggetto dati in una destinazione

La destinazione riceve un oggetto dati quando recupera l'oggetto dati dagli Appunti o è stato rilasciato dalla finestra di destinazione dall'utente. La destinazione può quindi estrarre i dati dall'oggetto dati. Se necessario, la destinazione può inoltre notificare all'oggetto dati il risultato dell'operazione. Prima del trasferimento dei dati di una shell, un obiettivo di rilascio deve prepararsi per l'operazione:

1.  La destinazione deve chiamare [RegisterClipboardFormat](/windows/win32/api/winuser/nf-winuser-registerclipboardformata) per ottenere un valore di formato degli Appunti valido per tutti i formati della shell, diversi da [CF \_ HDROP](clipboard.md), che potrebbero essere inclusi nell'oggetto dati. CF \_ HDROP è già un formato degli Appunti valido e non deve essere registrato.
2.  Per supportare un'operazione di trascinamento della selezione, la destinazione deve implementare un'interfaccia [**IDropTarget**](/windows/win32/api/oleidl/nn-oleidl-idroptarget) e registrare una finestra di destinazione. Per registrare una finestra di destinazione, la destinazione chiama [**RegisterDragDrop**](/windows/win32/api/ole2/nf-ole2-registerdragdrop) e passa l'handle della finestra e il puntatore all'interfaccia **IDropTarget** .

Per i trasferimenti degli Appunti, la destinazione non riceve alcuna notifica che un oggetto dati è stato inserito negli Appunti. In genere, a un'applicazione viene notificato che un oggetto si trova negli Appunti da un'azione dell'utente, ad esempio facendo clic sul pulsante Incolla sulla barra degli strumenti dell'applicazione. La destinazione recupera quindi il puntatore [**IDataObject**](/windows/win32/api/objidl/nn-objidl-idataobject) dell'oggetto dati dagli Appunti chiamando [**OleGetClipboard**](/windows/win32/api/ole2/nf-ole2-olegetclipboard). Per i trasferimenti di dati con trascinamento della selezione, il sistema utilizza l'interfaccia [**IDropTarget**](/windows/win32/api/oleidl/nn-oleidl-idroptarget) della destinazione per fornire alla destinazione informazioni sullo stato di avanzamento del trasferimento dei dati:

-   Il sistema chiama [**IDropTarget::D ragenter**](/windows/win32/api/oleidl/nf-oleidl-idroptarget-dragenter) quando il cursore entra nella finestra di destinazione.
-   Il sistema chiama periodicamente [**IDropTarget::D ragover**](/windows/win32/api/oleidl/nf-oleidl-idroptarget-dragover) quando il cursore passa sulla finestra di destinazione, per assegnare alla destinazione la posizione corrente del cursore.
-   Il sistema chiama [**IDropTarget::D ragleave**](/windows/win32/api/oleidl/nf-oleidl-idroptarget-dragleave) quando il cursore esce dalla finestra di destinazione.
-   Il sistema chiama [**IDropTarget::D por**](/windows/win32/api/oleidl/nf-oleidl-idroptarget-drop) quando l'utente rilascia l'oggetto dati nella finestra di destinazione.

Per informazioni su come implementare questi metodi, vedere [**IDropTarget**](/windows/win32/api/oleidl/nn-oleidl-idroptarget).

Quando i dati vengono eliminati, [**IDropTarget::D por**](/windows/win32/api/oleidl/nf-oleidl-idroptarget-drop) fornisce la destinazione con un puntatore all'interfaccia [**IDataObject**](/windows/win32/api/objidl/nn-objidl-idataobject) dell'oggetto dati. La destinazione USA quindi questa interfaccia per estrarre i dati dall'oggetto dati.

### <a name="extracting-shell-data-from-a-data-object"></a>Estrazione dei dati della shell da un oggetto dati

Una volta che un oggetto dati è stato eliminato o recuperato dagli Appunti, la destinazione può estrarre i dati necessari. Il primo passaggio del processo di estrazione consiste in genere nell'enumerare i formati contenuti nell'oggetto dati:

-   Chiamare [**IDataObject:: EnumFormatEtc**](/windows/win32/api/objidl/nf-objidl-idataobject-enumformatetc). L'oggetto dati crea un oggetto enumerazione OLE standard e restituisce un puntatore alla relativa interfaccia [**IEnumFORMATETC**](/windows/win32/api/objidl/nn-objidl-ienumformatetc) .
-   Usare i metodi [**IEnumFORMATETC**](/windows/win32/api/objidl/nn-objidl-ienumformatetc) per enumerare i formati contenuti nell'oggetto dati. Questa operazione in genere recupera una struttura [**FORMATETC**](/windows/win32/api/objidl/ns-objidl-formatetc) per ogni formato contenuto nell'oggetto. Tuttavia, l'oggetto di enumerazione restituisce in genere solo una singola struttura **FORMATETC** per il formato [ \_ fileContents CFSTR](clipboard.md) , indipendentemente dal numero di tali formati contenuti nell'oggetto dati.
-   Selezionare uno o più formati da estrarre e archiviare le relative strutture [**FORMATETC**](/windows/win32/api/objidl/ns-objidl-formatetc) .

Per recuperare un particolare formato, passare la struttura [**FORMATETC**](/windows/win32/api/objidl/ns-objidl-formatetc) associata a [**IDataObject:: GetData**](/windows/win32/api/objidl/nf-objidl-idataobject-getdata). Questo metodo restituisce una struttura [**STGMEDIUM**](/windows/win32/api/objidl/ns-objidl-ustgmedium-r1) che fornisce l'accesso ai dati. Per specificare un meccanismo di trasferimento dati specifico, impostare il valore **TYMED** della struttura **FORMATETC** sul valore TYMED \_ *xxx* corrispondente. Per chiedere all'oggetto dati di selezionare un meccanismo di trasferimento dei dati, la destinazione imposta i \_ valori *xxx* TYMED per ogni meccanismo di trasferimento dei dati che può essere gestito dalla destinazione. L'oggetto dati seleziona uno di questi meccanismi di trasferimento dei dati e restituisce la struttura **STGMEDIUM** appropriata.

Per la maggior parte dei formati, la destinazione può recuperare i dati passando la struttura [**FORMATETC**](/windows/win32/api/objidl/ns-objidl-formatetc) ricevuta durante l'enumerazione dei formati disponibili. Un'eccezione a questa regola è [CFSTR \_ fileContents](clipboard.md). Poiché un oggetto dati può contenere più istanze di questo formato, la struttura **FORMATETC** restituita dall'enumeratore potrebbe non corrispondere al formato specifico che si desidera estrarre. Oltre a specificare i membri **cfFormat** e **TYMED** , è necessario impostare anche il membro **lIndex** sul valore di indice del file. Per ulteriori informazioni, vedere la sezione *utilizzo del \_ formato fileContents CFSTR per estrarre i dati da un file* di [gestione della shell trasferimento dati scenari](datascenarios.md)

Il processo di estrazione dei dati dipende dal tipo di puntatore contenuto dalla struttura [**STGMEDIUM**](/windows/win32/api/objidl/ns-objidl-ustgmedium-r1) restituita. Se la struttura contiene un puntatore a un'interfaccia [**IStream**](/windows/win32/api/objidl/nn-objidl-istream) o [**IStorage**](/windows/win32/api/objidl/nn-objidl-istorage) , utilizzare i metodi di interfaccia per estrarre i dati. Il processo di estrazione dei dati da un oggetto di memoria globale viene illustrato nella sezione successiva.

### <a name="extracting-a-global-memory-object-from-a-data-object"></a>Estrazione di un oggetto memoria globale da un oggetto dati

Molti formati di dati della shell sono sotto forma di oggetto memoria globale. Utilizzare la seguente procedura per estrarre un formato contenente un oggetto memoria globale da un oggetto dati e assegnare i relativi dati a una variabile locale:

1.  Creare una struttura [**FORMATETC**](/windows/win32/api/objidl/ns-objidl-formatetc) . Impostare il membro **cfFormat** sul valore del formato degli Appunti appropriato e il membro **TYMED** su TYMED \_ HGLOBAL.
2.  Creare una struttura [**STGMEDIUM**](/windows/win32/api/objidl/ns-objidl-ustgmedium-r1) vuota.
3.  Chiamare [**IDataObject:: GetData**](/windows/win32/api/objidl/nf-objidl-idataobject-getdata)e passare i puntatori alle strutture [**FORMATETC**](/windows/win32/api/objidl/ns-objidl-formatetc) e [**STGMEDIUM**](/windows/win32/api/objidl/ns-objidl-ustgmedium-r1) .

    Quando [**IDataObject:: GetData**](/windows/win32/api/objidl/nf-objidl-idataobject-getdata) restituisce, la struttura [**STGMEDIUM**](/windows/win32/api/objidl/ns-objidl-ustgmedium-r1) conterrà un puntatore all'oggetto memoria globale che contiene i dati.

4.  Assegnare i dati a una variabile locale chiamando [**funzione GlobalLock**](/windows/win32/api/winbase/nf-winbase-globallock) e passando il membro **HGlobal** della struttura [**STGMEDIUM**](/windows/win32/api/objidl/ns-objidl-ustgmedium-r1) .
5.  Chiamare [**funzione GlobalUnlock**](/windows/win32/api/winbase/nf-winbase-globalunlock) per rilasciare il blocco sull'oggetto memoria globale.
6.  Chiamare [**ReleaseStgMedium**](/windows/win32/api/ole2/nf-ole2-releasestgmedium) per rilasciare l'oggetto memoria globale.

> [!Note]  
> Per rilasciare l'oggetto memoria globale, non [**GlobalFree**](/windows/win32/api/winbase/nf-winbase-globalfree), è necessario utilizzare [**ReleaseStgMedium**](/windows/win32/api/ole2/nf-ole2-releasestgmedium) .

 

Nell'esempio seguente viene illustrato come estrarre un valore **DWORD** archiviato come oggetto memoria globale da un oggetto dati. Il parametro **pdtobj** è un puntatore all'interfaccia [**IDataObject**](/windows/win32/api/objidl/nn-objidl-idataobject) dell'oggetto dati, **CF** è il formato degli appunti che identifica i dati desiderati e **pdwOut** viene utilizzato per restituire il valore dei dati.


```C++
STDAPI DataObj_GetDWORD(IDataObject *pdtobj, UINT cf, DWORD *pdwOut)
{    STGMEDIUM medium;
   FORMATETC fmte = {(CLIPFORMAT) cf, NULL, DVASPECT_CONTENT, -1, 
       TYMED_HGLOBAL};
    HRESULT hres = pdtobj->GetData(&fmte, &medium);
    if (SUCCEEDED(hres))
   {
       DWORD *pdw = (DWORD *)GlobalLock(medium.hGlobal);
       if (pdw)
       {
           *pdwOut = *pdw;
           GlobalUnlock(medium.hGlobal);
       }
       else
       {
           hres = E_UNEXPECTED;
       }
       ReleaseStgMedium(&medium);
   }
   return hres;
}
```



### <a name="implementing-idroptarget"></a>Implementazione di IDropTarget

Il sistema utilizza l'interfaccia [**IDropTarget**](/windows/win32/api/oleidl/nn-oleidl-idroptarget) per comunicare con la destinazione mentre il cursore è posizionato sulla finestra di destinazione. Le risposte della destinazione vengono inviate all'origine tramite la relativa interfaccia [**IDropSource**](/windows/win32/api/oleidl/nn-oleidl-idropsource) . A seconda della risposta, l'origine può modificare l'icona che rappresenta i dati. Se l'obiettivo di rilascio deve specificare l'icona dei dati, questa operazione può essere eseguita creando un [oggetto helper di trascinamento della selezione](#using-the-drag-and-drop-helper-object).

Con le operazioni di trascinamento della selezione convenzionali, la destinazione informa l'oggetto dati del risultato dell'operazione impostando il parametro *pdwEffect* di [**IDropTarget::D por**](/windows/win32/api/oleidl/nf-oleidl-idroptarget-drop) sul valore [**DropEffect**](../com/dropeffect-constants.md) appropriato. Con gli oggetti dati della shell, potrebbe anche essere necessario che la destinazione chiami [**IDataObject:: SetData**](/windows/win32/api/objidl/nf-objidl-idataobject-setdata). Per informazioni sul modo in cui le destinazioni devono rispondere per diversi scenari di trasferimento dei dati, vedere [gestione di scenari di trasferimento dati Shell](datascenarios.md).

Le sezioni seguenti illustrano brevemente come implementare i metodi [**IDropTarget::D ragenter**](/windows/win32/api/oleidl/nf-oleidl-idroptarget-dragenter), [**IDropTarget::D ragover**](/windows/win32/api/oleidl/nf-oleidl-idroptarget-dragover)e [**IDropTarget::D por**](/windows/win32/api/oleidl/nf-oleidl-idroptarget-drop) . Per ulteriori informazioni, vedere la documentazione di riferimento.

### <a name="dragenter-method"></a>DragEnter (metodo)

Il sistema chiama il metodo [**IDropTarget::D ragenter**](/windows/win32/api/oleidl/nf-oleidl-idroptarget-dragenter) quando il cursore entra nella finestra di destinazione. I relativi parametri forniscono la destinazione con la posizione del cursore, lo stato dei tasti di modifica della tastiera, ad esempio il tasto CTRL, e un puntatore all'interfaccia [**IDataObject**](/windows/win32/api/objidl/nn-objidl-idataobject) dell'oggetto dati. La destinazione è responsabile dell'utilizzo di tale interfaccia per determinare se può accettare qualsiasi formato contenuto nell'oggetto dati. Se possibile, in genere il valore di *pdwEffect* rimane invariato. Se non è in grado di accettare dati dall'oggetto dati, imposta il parametro *pdwEffect* su DropEffect \_ None. Il sistema passa il valore di questo parametro all'interfaccia [**IDropSource**](/windows/win32/api/oleidl/nn-oleidl-idropsource) dell'oggetto dati per consentire la visualizzazione dell'immagine di trascinamento appropriata.

Le destinazioni non devono usare il metodo [**IDataObject:: GetData**](/windows/win32/api/objidl/nf-objidl-idataobject-getdata) per eseguire il rendering dei dati della shell prima che vengano eliminati. Il rendering completo dei dati dell'oggetto per ogni occorrenza può provocare il blocco del cursore di trascinamento. Per evitare questo problema, alcuni oggetti della shell contengono un formato [CFSTR \_ INDRAGLOOP](clipboard.md) . Estraendo questo formato, le destinazioni possono controllare lo stato del ciclo di trascinamento evitando il rendering intensivo della memoria dei dati dell'oggetto. Il valore dei dati del formato è un valore **DWORD** impostato su un valore diverso da zero se l'oggetto dati si trova all'interno di un ciclo di trascinamento. Il valore dei dati del formato è impostato su zero se i dati sono stati eliminati.

Se la destinazione può accettare i dati dall'oggetto dati, deve esaminare **grfKeyState** per determinare se sono stati premuti i tasti di modifica per modificare il normale comportamento di rilascio. Ad esempio, l'operazione predefinita è in genere uno spostamento, ma la pressione del tasto CTRL indica in genere un'operazione di copia.

Quando il cursore si trova sulla finestra di destinazione, la destinazione può usare l'oggetto di supporto per il [trascinamento della selezione](#using-the-drag-and-drop-helper-object) per sostituire l'immagine di trascinamento dell'oggetto dati. In tal caso, [**IDropTarget::D ragenter**](/windows/win32/api/oleidl/nf-oleidl-idroptarget-dragenter) deve chiamare [**IDropTargetHelper::D ragenter**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-idroptargethelper-dragenter) per passare le informazioni contenute nei parametri *DragEnter* all'oggetto helper di trascinamento della selezione.

### <a name="dragover-method"></a>DragOver (metodo)

Quando il cursore si sposta all'interno della finestra di destinazione, il sistema chiama periodicamente il metodo [**IDropTarget::D ragover**](/windows/win32/api/oleidl/nf-oleidl-idroptarget-dragover) . I relativi parametri forniscono la destinazione con la posizione del cursore e lo stato dei tasti di modifica della tastiera, ad esempio il tasto CTRL. **IDropTarget::D ragover** ha molte stesse responsabilità di [**IDropTarget::D ragenter**](/windows/win32/api/oleidl/nf-oleidl-idroptarget-dragenter)e le implementazioni sono in genere molto simili.

Se la destinazione usa l'oggetto helper con trascinamento della selezione, [**IDropTarget::D ragover**](/windows/win32/api/oleidl/nf-oleidl-idroptarget-dragover) deve chiamare [**IDropTargetHelper::D ragover**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-idroptargethelper-dragover) per inviare le informazioni contenute nei parametri *DragOver* all'oggetto helper di trascinamento della selezione.

### <a name="drop-method"></a>Drop (metodo)

Il sistema chiama il metodo [**IDropTarget::D por**](/windows/win32/api/oleidl/nf-oleidl-idroptarget-drop) per notificare alla destinazione che l'utente ha rilasciato i dati, in genere rilasciando il pulsante del mouse. **IDropTarget::D por** presenta gli stessi parametri di [**IDropTarget::D ragenter**](/windows/win32/api/oleidl/nf-oleidl-idroptarget-dragenter). La destinazione risponde normalmente estraendo uno o più formati dall'oggetto dati. Al termine, la destinazione deve impostare il parametro *pdwEffect* su un valore [**DropEffect**](../com/dropeffect-constants.md) che indica il risultato dell'operazione. Per alcuni tipi di trasferimento dei dati della shell, è necessario che la destinazione chiami anche [**IDataObject:: SetData**](/windows/win32/api/objidl/nf-objidl-idataobject-setdata) per passare un formato con informazioni aggiuntive sul risultato dell'operazione all'oggetto dati. Per una descrizione dettagliata, vedere [gestione degli scenari di trasferimento dati Shell](datascenarios.md).

Se la destinazione usa l'oggetto helper con trascinamento della selezione, [**IDropTarget::D por**](/windows/win32/api/oleidl/nf-oleidl-idroptarget-drop) deve chiamare [**IDropTargetHelper::D por**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-idroptargethelper-drop) per inviare le informazioni contenute nei parametri [**IDropTargetHelper::D ragover**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-idroptargethelper-dragover) all'oggetto helper di trascinamento della selezione.

## <a name="using-the-drag-and-drop-helper-object"></a>Uso dell'oggetto helper di trascinamento della selezione

L'oggetto helper con trascinamento della selezione (CLSID \_ DragDropHelper) viene esportato dalla Shell per consentire alle destinazioni di specificare l'immagine di trascinamento mentre si trova sulla finestra di destinazione. Per usare l'oggetto helper di trascinamento della selezione, creare un oggetto server in-process chiamando [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) con un identificatore di classe (CLSID) di CLSID \_ DragDropHelper. L'oggetto helper di trascinamento della selezione espone due interfacce che vengono usate nel modo seguente:

-   L'interfaccia [**IDragSourceHelper**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-idragsourcehelper) consente all'obiettivo di rilascio di specificare un'icona per rappresentare l'oggetto dati.
-   L'interfaccia [**IDropTargetHelper**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-idroptargethelper) consente all'obiettivo di rilascio di informare l'oggetto helper di trascinamento della selezione della posizione del cursore e di mostrare o nascondere l'icona dei dati.

### <a name="using-the-idragsourcehelper-interface"></a>Uso dell'interfaccia IDragSourceHelper

L'interfaccia [**IDragSourceHelper**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-idragsourcehelper) viene esposta dall'oggetto helper di trascinamento della selezione per consentire a una destinazione di rilascio di fornire l'immagine che verrà visualizzata quando il cursore si trova sulla finestra di destinazione. **IDragSourceHelper** offre due modi alternativi per specificare la bitmap da usare come immagine di trascinamento:

-   Drop targets che dispongono di una finestra possono registrare un \_ messaggio della finestra di GETDRAGIMAGE inizializzando l'oggetto helper con trascinamento della selezione con [**IDragSourceHelper:: InitializeFromWindow**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-idragsourcehelper-initializefromwindow). Quando la destinazione riceve un \_ messaggio di GETDRAGIMAGE, il gestore inserisce le informazioni bitmap dell'immagine di trascinamento nella struttura [**SHDRAGIMAGE**](/windows/desktop/api/Shobjidl_core/ns-shobjidl_core-shdragimage) che viene passata come valore *lParam* del messaggio.
-   Le destinazioni di rilascio senza finestra specificano una bitmap quando inizializzano l'oggetto helper con trascinamento della selezione con [**IDragSourceHelper:: InitializeFromBitmap**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-idragsourcehelper-initializefrombitmap).

### <a name="using-the-idroptargethelper-interface"></a>Uso dell'interfaccia IDropTargetHelper

Questa interfaccia consente all'obiettivo di rilascio di inviare una notifica all'oggetto helper con trascinamento della selezione quando il cursore entra o esce dalla destinazione. Quando il cursore si trova sulla finestra di destinazione, [**IDropTargetHelper**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-idroptargethelper) consente alla destinazione di assegnare all'oggetto di supporto per il trascinamento della selezione le informazioni ricevute dalla destinazione tramite l'interfaccia [**IDropTarget**](/windows/win32/api/oleidl/nn-oleidl-idroptarget) .

Quattro dei metodi [**IDropTargetHelper**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-idroptargethelper) ,[**IDropTargetHelper::D ragenter**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-idroptargethelper-dragenter), [**IDropTargetHelper::D Ragleave**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-idroptargethelper-dragleave), [**IDropTargetHelper::D ragover**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-idroptargethelper-dragover)e [**IDropTargetHelper::D por**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-idroptargethelper-drop), sono associati al metodo [**IDropTarget**](/windows/win32/api/oleidl/nn-oleidl-idroptarget) con lo stesso nome. Per usare l'oggetto helper di trascinamento della selezione, ognuno dei metodi **IDropTarget** deve chiamare il metodo **IDropTargetHelper** corrispondente per inviare le informazioni all'oggetto helper di trascinamento della selezione. Il quinto metodo **IDropTargetHelper** , [**IDropTargetHelper:: Show**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-idroptargethelper-show), invia una notifica all'oggetto helper di trascinamento della selezione per mostrare o nascondere l'immagine di trascinamento. Questo metodo viene utilizzato durante il trascinamento su una finestra di destinazione in modalità video a bassa intensità di colore. Consente alla destinazione di nascondere l'immagine di trascinamento mentre disegna la finestra.

 

 
