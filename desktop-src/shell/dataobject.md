---
description: L'oggetto dati è fondamentale per tutti i trasferimenti di dati della shell.
ms.assetid: c63d339e-ac62-4da1-b5ce-22d45a6a3413
title: Oggetto dati shell
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 69a6c411310b6c9e9f28df4de048d3b6909c44b9
ms.sourcegitcommit: 822413efb4a70dd464e5db4d9e8693ef74f8132f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/09/2021
ms.locfileid: "113581629"
---
# <a name="shell-data-object"></a>Oggetto dati shell

L'oggetto dati è fondamentale per tutti i trasferimenti di dati della shell. È principalmente un contenitore per contenere i dati trasferiti. Tuttavia, la destinazione può anche comunicare con l'oggetto dati per facilitare alcuni tipi specializzati di trasferimento dei dati della shell, ad esempio gli spostamenti ottimizzati. Questo argomento fornisce una descrizione generale del funzionamento degli oggetti dati shell, del modo in cui vengono costruiti da un'origine e del modo in cui vengono gestiti da una destinazione. Per una descrizione dettagliata di come usare gli oggetti dati per trasferire diversi tipi di dati della shell, vedere Gestione degli scenari di [trasferimento dei dati della shell.](datascenarios.md)

-   [Funzionamento degli oggetti dati](#how-data-objects-work)
    -   [Formati degli Appunti](#clipboard-formats)
    -   [Struttura FORMATETC](#formatetc-structure)
    -   [Struttura STGMEDIUM](#stgmedium-structure)
-   [Modalità di creazione di un oggetto dati da parte di un'origine](#how-a-source-creates-a-data-object)
    -   [Come aggiungere un oggetto memoria globale a un oggetto dati](#how-to-add-a-global-memory-object-to-a-data-object)
    -   [Implementazione di IDataObject](#implementing-idataobject)
    -   [Implementazione di IDropSource](#implementing-idropsource)
-   [Modalità di gestione di un oggetto dati da parte di una destinazione](#how-a-target-handles-a-data-object)
    -   [Estrazione di dati della shell da un oggetto dati](#extracting-shell-data-from-a-data-object)
    -   [Implementazione di IDropTarget](#implementing-idroptarget)
-   [Uso dell'oggetto helper di trascinamento della selezione](#using-the-drag-and-drop-helper-object)
    -   [Uso dell'interfaccia IDragSourceHelper](#using-the-idragsourcehelper-interface)
    -   [Uso dell'interfaccia IDropTargetHelper](#using-the-idroptargethelper-interface)

## <a name="how-data-objects-work"></a>Funzionamento degli oggetti dati

Gli oggetti dati Component Object Model (COM), creati dall'origine dati per trasferire i dati a una destinazione. In genere trasportano più di un elemento di dati. Questa procedura può essere causata da due motivi:

-   Sebbene quasi tutti i tipi di dati possano essere trasferiti con un oggetto dati, l'origine in genere non conosce il tipo di dati che la destinazione può accettare. Ad esempio, i dati potrebbero essere una parte di un documento di testo formattato. Anche se la destinazione potrebbe essere in grado di gestire informazioni di formattazione complesse, potrebbe anche accettare solo testo ANSI. Per questo motivo, gli oggetti dati spesso includono gli stessi dati in diversi formati. La destinazione può quindi estrarre i dati in un formato che può gestire.
-   Gli oggetti dati possono inoltre contenere elementi di dati ausiliari che non sono versioni dei dati di origine. Questo tipo di elemento di dati fornisce in genere informazioni aggiuntive sull'operazione di trasferimento dei dati. Ad esempio, la shell usa elementi di dati ausiliari per indicare se un file deve essere copiato o spostato.

### <a name="clipboard-formats"></a>Formati degli Appunti

A ogni elemento di dati in un oggetto dati è associato un formato, in genere denominato *formato degli Appunti.* Esistono diversi formati di Appunti standard, dichiarati in Winuser.h, che corrispondono ai tipi di dati di uso comune. I formati degli Appunti sono numeri interi, ma in genere si fa riferimento a essi con il nome equivalente, che ha il formato CF \_ *XXX*. Ad esempio, il formato degli Appunti per il testo ANSI è CF \_ TEXT.

Le applicazioni possono estendere l'intervallo dei formati degli Appunti disponibili definendo formati privati. Per definire un formato privato, un'applicazione chiama [RegisterClipboardFormat](/windows/win32/api/winuser/nf-winuser-registerclipboardformata) con una stringa che identifica il formato. L'intero senza segno restituito dalla funzione è un valore di formato valido che può essere usato esattamente come un formato degli Appunti standard. Tuttavia, sia l'origine che la destinazione devono registrare il formato per poterlo usare. Con una sola eccezione,[CF \_ HDROP,](clipboard.md)i formati degli Appunti usati per trasferire i dati della shell sono definiti come formati privati. Devono essere registrati dall'origine e dalla destinazione prima di poter essere usati. Per una descrizione dei formati degli Appunti della shell disponibili, vedere Formati degli Appunti della shell.

Anche se esistono alcune eccezioni, gli oggetti dati contengono in genere un solo elemento di dati per ogni formato degli Appunti supportato. Questa correlazione uno-a-uno tra formato e dati consente di usare il valore di formato come identificatore per l'elemento di dati associato. In realtà, quando si esamina il contenuto di un oggetto dati, un particolare elemento di dati viene in genere definito "formato" e viene indicato con il relativo nome di formato. Ad esempio, frasi come "Estrai il formato CF \_ TEXT..." vengono in genere usati quando si illustra l'elemento di dati di testo ANSI di un oggetto dati.

Quando l'obiettivo di rilascio riceve il puntatore all'oggetto dati, l'obiettivo di rilascio enumera i formati disponibili per determinare quali tipi di dati sono disponibili. Richiede quindi uno o più formati disponibili ed estrae i dati. Il modo specifico in cui la destinazione estrae i dati della shell da un oggetto dati varia in base al formato; Questo argomento viene illustrato in dettaglio in [Come una destinazione gestisce un oggetto dati.](#how-a-target-handles-a-data-object)

Con semplici trasferimenti di dati degli Appunti, i dati vengono inseriti in un oggetto di memoria globale. L'indirizzo dell'oggetto viene inserito negli Appunti, insieme al relativo formato. Il formato degli Appunti indica alla destinazione il tipo di dati che troverà all'indirizzo associato. Anche se i semplici trasferimenti degli Appunti sono facili da implementare:

-   Gli oggetti dati offrono un modo molto più flessibile per trasferire i dati.
-   Gli oggetti dati sono più adatti per il trasferimento di grandi quantità di dati.
-   Gli oggetti dati devono essere utilizzati per trasferire i dati con un'operazione di trascinamento della selezione.

Per questi motivi, tutti i trasferimenti di dati della shell usano oggetti dati. Con gli oggetti dati, i formati degli Appunti non vengono usati direttamente. Gli elementi di dati vengono invece identificati con una generalizzazione del formato degli Appunti, una [**struttura FORMATETC.**](/windows/win32/api/objidl/ns-objidl-formatetc)

### <a name="formatetc-structure"></a>Struttura FORMATETC

La [**struttura FORMATETC**](/windows/win32/api/objidl/ns-objidl-formatetc) è una versione estesa di un formato degli Appunti. Usato per i trasferimenti di dati della shell, la **struttura FORMATETC** presenta le caratteristiche seguenti:

-   Un elemento di dati è ancora identificato dal relativo formato degli Appunti, nel **membro cfFormat.**
-   Il trasferimento dei dati non è limitato agli oggetti di memoria globale. Il **membro tymed** viene usato per indicare il meccanismo di trasferimento dei dati contenuto nella struttura [**STGMEDIUM**](/windows/win32/api/objidl/ns-objidl-ustgmedium-r1) associata. È impostato su uno dei valori [**TYMED \_ XXX.**](/windows/win32/api/objidl/ne-objidl-tymed)
-   La shell usa il **membro lIndex** con il formato [ \_ FILECONTENTS CFSTR](clipboard.md) per consentire a un oggetto dati di contenere più di un elemento di dati per formato. Per informazioni su come usare questo formato, vedere la sezione Using *the CFSTR \_ FILECONTENTS Format to Extract Data from a File* (Uso del formato FILECONTENTS CFSTR per estrarre dati da un file) di Gestione degli scenari [di trasferimento dei dati della shell.](datascenarios.md)
-   Il **membro dwAspect** è in genere impostato su DVASPECT \_ CONTENT. Tuttavia, in Shlobj.h sono definiti tre valori che possono essere usati per il trasferimento dei dati della shell. 

    | Valore               | Descrizione                                                                                       |
    |---------------------|---------------------------------------------------------------------------------------------------|
    | COPIA DVASPECT \_      | Utilizzato per indicare che il formato rappresenta una copia dei dati.                                   |
    | COLLEGAMENTO \_ DVASPECT      | Utilizzato per indicare che il formato rappresenta un collegamento ai dati.                               |
    | DVASPECT \_ SHORTNAME | Usato con il formato CF HDROP per richiedere un percorso di file con \_ i nomi abbreviati nel formato 8.3. |

    

     

-   Il **membro ptd** non viene usato per i trasferimenti di dati della shell e in genere è impostato su **NULL.**

### <a name="stgmedium-structure"></a>Struttura STGMEDIUM

La [**struttura STGMEDIUM**](/windows/win32/api/objidl/ns-objidl-ustgmedium-r1) fornisce l'accesso ai dati trasferiti. Per i dati della shell sono supportati tre meccanismi di trasferimento dei dati:

-   Oggetto memoria globale.
-   Interfaccia [**IStream.**](/windows/win32/api/objidl/nn-objidl-istream)
-   Interfaccia [**IStorage.**](/windows/win32/api/objidl/nn-objidl-istorage)

Il **membro tymed** della struttura [**STGMEDIUM**](/windows/win32/api/objidl/ns-objidl-ustgmedium-r1) è un [**valore TYMED \_ XXX**](/windows/win32/api/objidl/ne-objidl-tymed) che identifica il meccanismo di trasferimento dei dati. Il secondo membro è un puntatore utilizzato dalla destinazione per estrarre i dati. Il puntatore può essere di un'ampia gamma di tipi, a seconda del **valore tymed.** I tre **valori tymed** usati per i trasferimenti di dati della shell sono riepilogati nella tabella seguente, insieme al nome del membro **STGMEDIUM** corrispondente.



| Valore tymed     | Nome del membro | Descrizione                                                                                                                                                                                                                                                                                                       |
|-----------------|-------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| TYMED \_ HGLOBAL  | **Hglobal** | Puntatore a un oggetto memoria globale. Questo tipo di puntatore viene in genere usato per il trasferimento di piccole quantità di dati. Ad esempio, la shell usa oggetti di memoria globali per trasferire stringhe di testo brevi, ad esempio nomi di file o URL.                                                                                    |
| TYMED \_ ISTREAM  | **pstm**    | Puntatore a [**un'interfaccia IStream.**](/windows/win32/api/objidl/nn-objidl-istream) Questo tipo di puntatore è preferibile per la maggior parte dei trasferimenti di dati della shell perché richiede una quantità di memoria relativamente piccola rispetto a TYMED \_ HGLOBAL. Inoltre, il meccanismo di trasferimento dei dati ISTREAM TYMED non richiede che l'origine archivi \_ i dati in un modo particolare. |
| TYMED \_ ISTORAGE | **pstg**    | Puntatore a [**un'interfaccia IStorage.**](/windows/win32/api/objidl/nn-objidl-istorage) La destinazione chiama i metodi dell'interfaccia per estrarre i dati. Come TYMED \_ ISTREAM, questo tipo di puntatore richiede una quantità di memoria relativamente piccola. Tuttavia, poiché TYMED ISTORAGE è meno flessibile di \_ TYMED \_ ISTREAM, non viene usato normalmente.                  |



 

## <a name="how-a-source-creates-a-data-object"></a>Modalità di creazione di un oggetto dati da parte di un'origine

Quando un utente avvia un trasferimento dei dati della shell, l'origine è responsabile della creazione di un oggetto dati e del caricamento con i dati. La procedura seguente riepiloga il processo:

1.  Chiamare [RegisterClipboardFormat per](/windows/win32/api/winuser/nf-winuser-registerclipboardformata) ottenere un valore di formato degli Appunti valido per ogni formato della shell che verrà incluso nell'oggetto dati. Tenere presente [che CF \_ HDROP](clipboard.md) è già un formato degli Appunti valido e non deve essere registrato.
2.  Per ogni formato da trasferire, inserire i dati associati in un oggetto memoria globale o creare un oggetto che fornisce l'accesso ai dati tramite [**un'interfaccia IStream**](/windows/win32/api/objidl/nn-objidl-istream) o [**IStorage.**](/windows/win32/api/objidl/nn-objidl-istorage) Le **interfacce IStream** **e IStorage** vengono create usando tecniche COM standard. Per informazioni su come gestire oggetti di memoria globali, vedere [How to Add a Global Memory Object to a Data Object](#how-to-add-a-global-memory-object-to-a-data-object).
3.  Creare [**strutture FORMATETC**](/windows/win32/api/objidl/ns-objidl-formatetc) [**e STGMEDIUM**](/windows/win32/api/objidl/ns-objidl-ustgmedium-r1) per ogni formato.
4.  Creare un'istanza di un oggetto dati.
5.  Caricare i dati nell'oggetto dati chiamando il metodo [**IDataObject::SetData**](/windows/win32/api/objidl/nf-objidl-idataobject-setdata) per ogni formato supportato e passando le strutture [**FORMATETC**](/windows/win32/api/objidl/ns-objidl-formatetc) e [**STGMEDIUM**](/windows/win32/api/objidl/ns-objidl-ustgmedium-r1) del formato.
6.  Con i trasferimenti di dati degli Appunti, chiamare [**OleSetClipboard**](/windows/win32/api/ole2/nf-ole2-olesetclipboard) per posizionare un puntatore all'interfaccia [**IDataObject**](/windows/win32/api/objidl/nn-objidl-idataobject) dell'oggetto dati negli Appunti. Per i trasferimenti con trascinamento della selezione, avviare un *ciclo di trascinamento* chiamando [**DoDragDrop.**](/windows/win32/api/ole2/nf-ole2-dodragdrop) Il **puntatore IDataObject** verrà passato all'obiettivo di rilascio quando i dati vengono rilasciati, terminando il ciclo di trascinamento.

L'oggetto dati è ora pronto per essere trasferito alla destinazione. Per i trasferimenti di dati degli Appunti, l'oggetto viene mantenuto finché la destinazione non lo richiede chiamando [**OleGetClipboard.**](/windows/win32/api/ole2/nf-ole2-olegetclipboard) Per i trasferimenti di dati con trascinamento della selezione, l'oggetto dati è responsabile della creazione di un'icona per rappresentare i dati e di spostarla quando l'utente sposta il cursore. Mentre l'oggetto è nel ciclo di trascinamento, l'origine riceve informazioni sullo stato tramite [**l'interfaccia IDropSource.**](/windows/win32/api/oleidl/nn-oleidl-idropsource) Per altre informazioni, vedere [Implementazione di IDropSource.](#implementing-idropsource)

L'origine non riceve alcuna notifica se l'oggetto dati viene recuperato dagli Appunti da una destinazione. Quando un oggetto viene rilasciato in una destinazione da un'operazione di trascinamento della selezione, verrà restituita la funzione [**DoDragDrop**](/windows/win32/api/ole2/nf-ole2-dodragdrop) chiamata per avviare il ciclo di trascinamento.

### <a name="how-to-add-a-global-memory-object-to-a-data-object"></a>Come aggiungere un oggetto memoria globale a un oggetto dati

Molti formati di dati shell sono sotto forma di oggetto memoria globale. Usare la procedura seguente per creare un formato contenente un oggetto memoria globale e caricarlo nell'oggetto dati:

1.  Creare una [**struttura FORMATETC.**](/windows/win32/api/objidl/ns-objidl-formatetc) Impostare il **membro cfFormat** sul valore di formato degli Appunti appropriato e il membro **tymed** su TYMED \_ HGLOBAL.
2.  Creare una [**struttura STGMEDIUM.**](/windows/win32/api/objidl/ns-objidl-ustgmedium-r1) Impostare il **membro tymed** su TYMED \_ HGLOBAL.
3.  Creare un oggetto memoria globale chiamando [**GlobalAlloc per**](/windows/win32/api/winbase/nf-winbase-globalalloc) allocare un blocco di memoria di dimensioni adatte.
4.  Assegnare il blocco di dati da trasferire all'indirizzo restituito da [**GlobalAlloc.**](/windows/win32/api/winbase/nf-winbase-globalalloc)
5.  Assegnare l'indirizzo dell'oggetto memoria globale al **membro hGlobal** della [**struttura STGMEDIUM.**](/windows/win32/api/objidl/ns-objidl-ustgmedium-r1)
6.  Caricare il formato nell'oggetto dati chiamando [**IDataObject::SetData**](/windows/win32/api/objidl/nf-objidl-idataobject-setdata) e passando le strutture [**FORMATETC**](/windows/win32/api/objidl/ns-objidl-formatetc) e [**STGMEDIUM**](/windows/win32/api/objidl/ns-objidl-ustgmedium-r1) create nei passaggi precedenti.

La funzione di esempio seguente crea un oggetto memoria globale contenente un **valore DWORD** e lo carica in un oggetto dati. Il **parametro pdtobj** è un puntatore all'interfaccia [**IDataObject**](/windows/win32/api/objidl/nn-objidl-idataobject) dell'oggetto dati, **cf** è il valore del formato degli Appunti e **dw** è il valore dei dati.


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

[**IDataObject è**](/windows/win32/api/objidl/nn-objidl-idataobject) l'interfaccia principale di un oggetto dati. Deve essere implementato da tutti gli oggetti dati. Viene usato sia dall'origine che dalla destinazione per diversi scopi, tra cui:

-   Caricamento di dati nell'oggetto dati.
-   Estrazione di dati dall'oggetto dati.
-   Determinazione dei tipi di dati presenti nell'oggetto dati.
-   Fornire feedback all'oggetto dati sul risultato del trasferimento dei dati.

[**IDataObject**](/windows/win32/api/objidl/nn-objidl-idataobject) supporta diversi metodi. Questa sezione illustra come implementare i tre metodi più importanti per gli oggetti dati della shell, [SetData](#setdata-method), [EnumFormatEtc](#enumformatetc-method)e [GetData](#getdata-method). Per una descrizione degli altri metodi, vedere le informazioni di **riferimento su IDataObject.**

### <a name="setdata-method"></a>SetData (metodo)

La funzione principale del metodo [**IDataObject::SetData**](/windows/win32/api/objidl/nf-objidl-idataobject-setdata) è consentire all'origine di caricare i dati nell'oggetto dati. Per ogni formato da includere, l'origine crea una struttura [**FORMATETC**](/windows/win32/api/objidl/ns-objidl-formatetc) per identificare il formato e una [**struttura STGMEDIUM**](/windows/win32/api/objidl/ns-objidl-ustgmedium-r1) per contenere un puntatore ai dati. L'origine chiama quindi il metodo **IDataObject::SetData** dell'oggetto e passa le strutture **FORMATETC** e **STGMEDIUM** del formato. Il metodo deve archiviare queste informazioni in modo che sia disponibile quando la destinazione chiama [**IDataObject::GetData**](/windows/win32/api/objidl/nf-objidl-idataobject-getdata) per estrarre i dati dall'oggetto.

Tuttavia, quando si trasferiscono i file, la shell spesso inserisce le informazioni per ogni file da trasferire in un formato [ \_ FILECONTENTS CFSTR](clipboard.md) separato. Per distinguere i diversi file, il membro **lIndex** della struttura [**FORMATETC**](/windows/win32/api/objidl/ns-objidl-formatetc) di ogni file viene impostato su un valore di indice che identifica il file specifico. [**L'implementazione di IDataObject::SetData**](/windows/win32/api/objidl/nf-objidl-idataobject-setdata) deve essere in grado di archiviare più formati FILECONTENTS CFSTR che differiscono solo \_ per i relativi membri **lIndex.**

Mentre il cursore è posizionato sulla finestra di destinazione, la destinazione può usare l'oggetto [helper](#using-the-drag-and-drop-helper-object) di trascinamento della selezione per specificare l'immagine di trascinamento. L'oggetto helper di trascinamento della selezione chiama [**IDataObject::SetData**](/windows/win32/api/objidl/nf-objidl-idataobject-setdata) per caricare i formati privati nell'oggetto dati usato per il supporto tra processi. Per supportare l'oggetto helper di trascinamento della selezione, l'implementazione **di IDataObject::SetData** deve essere in grado di accettare e archiviare formati privati arbitrari.

Dopo l'eliminazione dei dati, alcuni tipi di trasferimento dei dati della shell richiedono che la destinazione chiami [**IDataObject::SetData**](/windows/win32/api/objidl/nf-objidl-idataobject-setdata) per fornire all'oggetto dati informazioni sul risultato dell'operazione di eliminazione. Ad esempio, quando si spostano file con un'operazione di spostamento ottimizzata, la destinazione in genere elimina i file originali, ma non è necessario farlo. La destinazione indica all'oggetto dati se ha eliminato i file chiamando **IDataObject::SetData** con un [formato CFSTR \_ LOGICALPERFORMEDDROPEFFECT.](clipboard.md) Esistono diversi altri formati [degli Appunti della shell](clipboard.md) che vengono usati anche dalla destinazione per passare informazioni all'oggetto dati. **L'implementazione di IDataObject::SetData** deve essere in grado di riconoscere questi formati e rispondere in modo appropriato. Per altre informazioni, vedere [Gestione degli scenari di trasferimento dei dati della shell.](datascenarios.md)

### <a name="enumformatetc-method"></a>Metodo EnumFormatEtc

Quando la destinazione riceve un oggetto dati, in genere chiama [**FORMATETC**](/windows/win32/api/objidl/ns-objidl-formatetc) per determinare i formati contenuti nell'oggetto. Il metodo crea un oggetto enumerazione OLE e restituisce un puntatore [**all'interfaccia IEnumFORMATETC**](/windows/win32/api/objidl/nn-objidl-ienumformatetc) dell'oggetto. La destinazione usa quindi l'interfaccia per enumerare i formati disponibili.

Un oggetto enumerazione deve sempre enumerare i formati disponibili in ordine di qualità, a partire dal migliore. La qualità relativa dei formati è definita dall'origine di rilascio. In generale, i formati di massima qualità contengono i dati più completi e più completi. Ad esempio, un'immagine a colori a 24 bit viene in genere considerata di qualità superiore rispetto a una versione in scala grigia di tale immagine. Il motivo per cui i formati vengono enumerati in ordine di qualità è che le destinazioni vengono in genere enumerate fino a quando non ottengono un formato supportato e quindi usano tale formato per estrarre i dati. Perché questa procedura produca il formato migliore disponibile che la destinazione può supportare, i formati devono essere enumerati in ordine di qualità.

Un oggetto di enumerazione per i dati della shell viene implementato in modo molto uguale a quello per altri tipi di trasferimento dei dati, con un'eccezione importante. Poiché gli oggetti dati contengono in genere un solo elemento di dati per formato, in genere enumerano ogni formato passato a [**IDataObject::SetData.**](/windows/win32/api/objidl/nf-objidl-idataobject-setdata) Tuttavia, come illustrato nella sezione [Metodo SetData,](#setdata-method) gli oggetti dati della shell possono contenere più [formati \_ FILECONTENTS CFSTR.](clipboard.md)

Poiché lo scopo di [**IDataObject::EnumFormatEtc**](/windows/win32/api/objidl/nf-objidl-idataobject-enumformatetc) è consentire alla destinazione di determinare quali tipi di dati sono presenti, non è necessario enumerare più di un formato [ \_ FILECONTENTS CFSTR.](clipboard.md) Se la destinazione deve conoscere il numero di questi formati contenuti nell'oggetto dati, la destinazione può recuperare tali informazioni dal formato FILEDESCRIPTOR CFSTR \_ associato. Per altre informazioni su come implementare **IDataObject::EnumFormatEtc,** vedere la documentazione di riferimento del metodo.

### <a name="getdata-method"></a>Metodo GetData

La destinazione chiama [**IDataObject::GetData per**](/windows/win32/api/objidl/nf-objidl-idataobject-getdata) estrarre un particolare formato dati. La destinazione specifica il formato passando la struttura [**FORMATETC**](/windows/win32/api/objidl/ns-objidl-formatetc) appropriata. **IDataObject::GetData** restituisce la struttura [**STGMEDIUM del**](/windows/win32/api/objidl/ns-objidl-ustgmedium-r1) formato.

La destinazione può impostare il membro **tymed** della struttura [**FORMATETC**](/windows/win32/api/objidl/ns-objidl-formatetc) su un valore TYMED XXX specifico per specificare il meccanismo di trasferimento dei dati che verrà utilizzato per estrarre \_  i dati. Tuttavia, la destinazione può anche effettuare una richiesta più generica e consentire all'oggetto dati di decidere. Per chiedere all'oggetto dati di selezionare il meccanismo di trasferimento dei dati, la destinazione imposta tutti i valori XXX di TYMED \_  supportati. [**IDataObject::GetData**](/windows/win32/api/objidl/nf-objidl-idataobject-getdata) seleziona uno di questi meccanismi di trasferimento dei dati e restituisce la [**struttura STGMEDIUM**](/windows/win32/api/objidl/ns-objidl-ustgmedium-r1) appropriata. Ad esempio, **tymed** è in genere impostato su TYMED \_ HGLOBAL \| TYMED \_ ISTREAM \| TYMED ISTORAGE per richiedere uno dei tre meccanismi di trasferimento dei dati \_ della shell.

> [!Note]  
> Poiché possono essere presenti più formati [ \_ FILECONTENTS CFSTR,](clipboard.md) i membri **cfFormat** e **tymed** della struttura [**FORMATETC**](/windows/win32/api/objidl/ns-objidl-formatetc) non sono sufficienti per indicare quale struttura [**STGMEDIUM**](/windows/win32/api/objidl/ns-objidl-ustgmedium-r1) [**IDataObject::GetData**](/windows/win32/api/objidl/nf-objidl-idataobject-getdata) deve restituire. Per il formato CFSTR \_ FILECONTENTS, **anche IDataObject::GetData** deve esaminare il membro **lIndex** della struttura **FORMATETC** per restituire la struttura **STGMEDIUM** corretta.

 

Il [formato CFSTR \_ INDRAGLOOP](clipboard.md) viene inserito negli oggetti dati per consentire alle destinazioni di controllare lo stato del ciclo di trascinamento della selezione evitando il rendering intensivo della memoria dei dati dell'oggetto. I dati del formato sono un **valore DWORD** impostato su un valore diverso da zero se l'oggetto dati si trova all'interno di un ciclo di trascinamento. Il valore dei dati del formato viene impostato su zero se i dati sono stati eliminati. Se una destinazione richiede questo formato e non è stata caricata dall'origine, [**IDataObject::GetData**](/windows/win32/api/objidl/nf-objidl-idataobject-getdata) deve rispondere come se l'origine avesse caricato il formato con un valore pari a zero.

Mentre il cursore si trova sulla finestra di destinazione, la destinazione può usare l'oggetto [helper](#using-the-drag-and-drop-helper-object) di trascinamento della selezione per specificare l'immagine di trascinamento. L'oggetto helper di trascinamento della selezione chiama [**IDataObject::SetData**](/windows/win32/api/objidl/nf-objidl-idataobject-setdata) per caricare i formati privati nell'oggetto dati usato per il supporto tra processi. Successivamente chiama [**IDataObject::GetData**](/windows/win32/api/objidl/nf-objidl-idataobject-getdata) per recuperarli. Per supportare l'oggetto helper di trascinamento della selezione, l'implementazione dell'oggetto dati shell deve essere in grado di restituire formati privati arbitrari quando vengono richiesti.

### <a name="implementing-idropsource"></a>Implementazione di IDropSource

L'origine deve creare un oggetto che espone [**un'interfaccia IDropSource.**](/windows/win32/api/oleidl/nn-oleidl-idropsource) Questa interfaccia consente all'origine di aggiornare l'immagine di trascinamento che indica la posizione corrente del cursore e di fornire feedback al sistema su come terminare un'operazione di trascinamento della selezione.  **IDropSource** ha due metodi: [**GiveFeedback**](/windows/win32/api/oleidl/nf-oleidl-idropsource-givefeedback) [**e QueryContinueDrag**](/windows/win32/api/oleidl/nf-oleidl-idropsource-querycontinuedrag).

### <a name="givefeedback-method"></a>GiveFeedback (metodo)

Durante il ciclo di trascinamento, un'origine di rilascio è responsabile di tenere traccia della posizione del cursore e visualizzare un'immagine di trascinamento appropriata. Tuttavia, in alcuni casi può essere necessario modificare l'aspetto dell'immagine di trascinamento quando si trova sopra la finestra della destinazione di rilascio.

Quando il cursore entra o esce dalla finestra di destinazione e durante lo spostamento sulla finestra di destinazione, il sistema chiama periodicamente [**l'interfaccia IDropTarget della**](/windows/win32/api/oleidl/nn-oleidl-idroptarget) destinazione. La destinazione risponde con un [**valore DROPEFFECT**](../com/dropeffect-constants.md) che viene inoltrato all'origine tramite il [**metodo GiveFeedback.**](/windows/win32/api/oleidl/nf-oleidl-idropsource-givefeedback) Se appropriato, l'origine può modificare l'aspetto del cursore in base al **valore DROPEFFECT.** Per altri dettagli, vedere i riferimenti **a GiveFeedback** [**e DoDragDrop.**](/windows/win32/api/ole2/nf-ole2-dodragdrop)

### <a name="querycontinuedrag-method"></a>QueryContinueDrag (metodo)

Questo metodo viene chiamato se lo stato del pulsante del mouse o della tastiera cambia mentre l'oggetto dati si trova nel ciclo di trascinamento. Notifica all'origine se il tasto ESC è stato premuto e fornisce lo stato corrente dei tasti di modifica della tastiera, ad esempio CTRL o MAIUSC. Il valore restituito del metodo [**QueryContinueDrag**](/windows/win32/api/oleidl/nf-oleidl-idropsource-querycontinuedrag) specifica una delle tre azioni seguenti:

-   S \_ OK. Continuare l'operazione di trascinamento
-   DRAGDROP \_ S \_ DROP. Eliminare i dati. Il sistema chiama quindi il metodo [**IDropTarget::D rop della**](/windows/win32/api/oleidl/nf-oleidl-idroptarget-drop) destinazione.
-   DRAGDROP \_ S \_ CANCEL. Terminare il ciclo di trascinamento senza rilasciare i dati. Questo valore viene in genere restituito se è stato premuto il tasto ESCAPE.

Per altre informazioni, vedere i [**riferimenti QueryContinueDrag**](/windows/win32/api/oleidl/nf-oleidl-idropsource-querycontinuedrag) [**e DoDragDrop.**](/windows/win32/api/ole2/nf-ole2-dodragdrop)

## <a name="how-a-target-handles-a-data-object"></a>Modalità di gestione di un oggetto dati da parte di una destinazione

La destinazione riceve un oggetto dati quando recupera l'oggetto dati dagli Appunti o lo fa eliminare nella finestra di destinazione dall'utente. La destinazione può quindi estrarre dati dall'oggetto dati. Se necessario, la destinazione può anche inviare una notifica all'oggetto dati del risultato dell'operazione. Prima di un trasferimento di dati shell, una destinazione di rilascio deve prepararsi per l'operazione:

1.  La destinazione deve chiamare [RegisterClipboardFormat](/windows/win32/api/winuser/nf-winuser-registerclipboardformata) per ottenere un valore di formato degli Appunti valido per tutti i formati shell, diversi [da CF \_ HDROP,](clipboard.md)che potrebbero essere inclusi nell'oggetto dati. CF \_ HDROP è già un formato degli Appunti valido e non deve essere registrato.
2.  Per supportare un'operazione di trascinamento della selezione, la destinazione deve implementare [**un'interfaccia IDropTarget**](/windows/win32/api/oleidl/nn-oleidl-idroptarget) e registrare una finestra di destinazione. Per registrare una finestra di destinazione, la destinazione chiama [**RegisterDragDrop**](/windows/win32/api/ole2/nf-ole2-registerdragdrop) e passa l'handle della finestra e il puntatore a interfaccia **IDropTarget.**

Per i trasferimenti degli Appunti, la destinazione non riceve alcuna notifica che indica che un oggetto dati è stato inserito negli Appunti. In genere, a un'applicazione viene notificato che un oggetto si trova negli Appunti da un'azione dell'utente, ad esempio facendo clic sul pulsante Incolla sulla barra degli strumenti dell'applicazione. La destinazione recupera quindi il puntatore [**IDataObject**](/windows/win32/api/objidl/nn-objidl-idataobject) dell'oggetto dati dagli Appunti chiamando [**OleGetClipboard**](/windows/win32/api/ole2/nf-ole2-olegetclipboard). Per i trasferimenti di dati con trascinamento della selezione, il sistema usa [**l'interfaccia IDropTarget**](/windows/win32/api/oleidl/nn-oleidl-idroptarget) della destinazione per fornire alla destinazione informazioni sull'avanzamento del trasferimento dei dati:

-   Il sistema chiama [**IDropTarget::D ragEnter**](/windows/win32/api/oleidl/nf-oleidl-idroptarget-dragenter) quando il cursore entra nella finestra di destinazione.
-   Il sistema chiama periodicamente [**IDropTarget::D ragOver**](/windows/win32/api/oleidl/nf-oleidl-idroptarget-dragover) quando il cursore passa sulla finestra di destinazione, per assegnare alla destinazione la posizione corrente del cursore.
-   Il sistema chiama [**IDropTarget::D ragLeave**](/windows/win32/api/oleidl/nf-oleidl-idroptarget-dragleave) quando il cursore esce dalla finestra di destinazione.
-   Il sistema chiama [**IDropTarget::D quando**](/windows/win32/api/oleidl/nf-oleidl-idroptarget-drop) l'utente elimina l'oggetto dati nella finestra di destinazione.

Per una descrizione di come implementare questi metodi, vedere [**IDropTarget**](/windows/win32/api/oleidl/nn-oleidl-idroptarget).

Quando i dati vengono eliminati, [**IDropTarget::D rop**](/windows/win32/api/oleidl/nf-oleidl-idroptarget-drop) fornisce alla destinazione un puntatore all'interfaccia [**IDataObject dell'oggetto**](/windows/win32/api/objidl/nn-objidl-idataobject) dati. La destinazione usa quindi questa interfaccia per estrarre dati dall'oggetto dati.

### <a name="extracting-shell-data-from-a-data-object"></a>Estrazione di dati della shell da un oggetto dati

Dopo che un oggetto dati è stato eliminato o recuperato dagli Appunti, la destinazione può estrarre i dati di cui ha bisogno. Il primo passaggio del processo di estrazione consiste in genere nell'enumerare i formati contenuti nell'oggetto dati:

-   Chiamare [**IDataObject::EnumFormatEtc**](/windows/win32/api/objidl/nf-objidl-idataobject-enumformatetc). L'oggetto dati crea un oggetto di enumerazione OLE standard e restituisce un puntatore alla relativa [**interfaccia IEnumFORMATETC.**](/windows/win32/api/objidl/nn-objidl-ienumformatetc)
-   Usare i [**metodi IEnumFORMATETC**](/windows/win32/api/objidl/nn-objidl-ienumformatetc) per enumerare i formati contenuti nell'oggetto dati. Questa operazione recupera in genere una [**struttura FORMATETC**](/windows/win32/api/objidl/ns-objidl-formatetc) per ogni formato contenuto nell'oggetto . Tuttavia, l'oggetto di enumerazione restituisce in genere solo una singola struttura **FORMATETC** per il formato [CFSTR \_ FILECONTENTS,](clipboard.md) indipendentemente dal numero di formati contenuti nell'oggetto dati.
-   Selezionare uno o più formati da estrarre e archiviare le [**strutture FORMATETC.**](/windows/win32/api/objidl/ns-objidl-formatetc)

Per recuperare un formato specifico, passare la struttura [**FORMATETC**](/windows/win32/api/objidl/ns-objidl-formatetc) associata a [**IDataObject::GetData**](/windows/win32/api/objidl/nf-objidl-idataobject-getdata). Questo metodo restituisce una [**struttura STGMEDIUM**](/windows/win32/api/objidl/ns-objidl-ustgmedium-r1) che fornisce l'accesso ai dati. Per specificare un particolare meccanismo di trasferimento dei dati, impostare il valore **tymed** della struttura **FORMATETC** sul valore TYMED \_ *XXX* corrispondente. Per chiedere all'oggetto dati di selezionare un meccanismo di trasferimento dei dati, la destinazione imposta i valori TYMED XXX per ogni meccanismo di trasferimento dati che la \_  destinazione può gestire. L'oggetto dati seleziona uno di questi meccanismi di trasferimento dei dati e restituisce la **struttura STGMEDIUM** appropriata.

Per la maggior parte dei formati, la destinazione può recuperare i dati passando la [**struttura FORMATETC**](/windows/win32/api/objidl/ns-objidl-formatetc) ricevuta durante l'enumerazione dei formati disponibili. Un'eccezione a questa regola è [CFSTR \_ FILECONTENTS](clipboard.md). Poiché un oggetto dati può contenere più istanze di questo formato, la struttura **FORMATETC** restituita dall'enumeratore potrebbe non corrispondere al formato specifico da estrarre. Oltre a specificare i **membri cfFormat** e **tymed,** è necessario impostare anche il membro **lIndex** sul valore di indice del file. Per altre informazioni, vedere la sezione Uso del formato *\_ FILECONTENTS CFSTR* per estrarre dati da un file di Gestione degli scenari [di trasferimento dei dati della shell](datascenarios.md)

Il processo di estrazione dei dati dipende dal tipo di puntatore contenuto nella struttura [**STGMEDIUM**](/windows/win32/api/objidl/ns-objidl-ustgmedium-r1) restituita. Se la struttura contiene un puntatore a [**un'interfaccia IStream**](/windows/win32/api/objidl/nn-objidl-istream) o [**IStorage,**](/windows/win32/api/objidl/nn-objidl-istorage) usare i metodi dell'interfaccia per estrarre i dati. Il processo di estrazione dei dati da un oggetto di memoria globale viene illustrato nella sezione successiva.

### <a name="extracting-a-global-memory-object-from-a-data-object"></a>Estrazione di un oggetto di memoria globale da un oggetto dati

Molti formati di dati shell sono sotto forma di oggetto di memoria globale. Usare la procedura seguente per estrarre un formato contenente un oggetto memoria globale da un oggetto dati e assegnarne i dati a una variabile locale:

1.  Creare una [**struttura FORMATETC.**](/windows/win32/api/objidl/ns-objidl-formatetc) Impostare il **membro cfFormat** sul valore di formato degli Appunti appropriato e il membro **tymed** su TYMED \_ HGLOBAL.
2.  Creare una struttura [**STGMEDIUM**](/windows/win32/api/objidl/ns-objidl-ustgmedium-r1) vuota.
3.  Chiamare [**IDataObject::GetData**](/windows/win32/api/objidl/nf-objidl-idataobject-getdata)e passare puntatori alle strutture [**FORMATETC**](/windows/win32/api/objidl/ns-objidl-formatetc) e [**STGMEDIUM.**](/windows/win32/api/objidl/ns-objidl-ustgmedium-r1)

    Quando [**viene restituito IDataObject::GetData,**](/windows/win32/api/objidl/nf-objidl-idataobject-getdata) la [**struttura STGMEDIUM**](/windows/win32/api/objidl/ns-objidl-ustgmedium-r1) conterrà un puntatore all'oggetto memoria globale che contiene i dati.

4.  Assegnare i dati a una variabile locale chiamando [**GlobalLock**](/windows/win32/api/winbase/nf-winbase-globallock) e passando il membro **hGlobal** della [**struttura STGMEDIUM.**](/windows/win32/api/objidl/ns-objidl-ustgmedium-r1)
5.  Chiamare [**GlobalUnlock**](/windows/win32/api/winbase/nf-winbase-globalunlock) per rilasciare il blocco sull'oggetto di memoria globale.
6.  Chiamare [**ReleaseStgMedium per**](/windows/win32/api/ole2/nf-ole2-releasestgmedium) rilasciare l'oggetto di memoria globale.

> [!Note]  
> È necessario usare [**ReleaseStgMedium per**](/windows/win32/api/ole2/nf-ole2-releasestgmedium) rilasciare l'oggetto di memoria globale, non [**GlobalFree**](/windows/win32/api/winbase/nf-winbase-globalfree).

 

L'esempio seguente illustra come estrarre un **valore DWORD** archiviato come oggetto di memoria globale da un oggetto dati. Il **parametro pdtobj** è un puntatore all'interfaccia [**IDataObject**](/windows/win32/api/objidl/nn-objidl-idataobject) dell'oggetto dati, **cf** è il formato degli Appunti che identifica i dati desiderati e **pdwOut** viene usato per restituire il valore dei dati.


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

Il sistema usa [**l'interfaccia IDropTarget**](/windows/win32/api/oleidl/nn-oleidl-idroptarget) per comunicare con la destinazione mentre il cursore si trova sulla finestra di destinazione. Le risposte della destinazione vengono inoltrate all'origine tramite la relativa [**interfaccia IDropSource.**](/windows/win32/api/oleidl/nn-oleidl-idropsource) A seconda della risposta, l'origine può modificare l'icona che rappresenta i dati. Se la destinazione di rilascio deve specificare l'icona dei dati, può farlo creando un oggetto helper di [trascinamento della selezione.](#using-the-drag-and-drop-helper-object)

Con le operazioni di trascinamento della selezione convenzionali, la destinazione informa l'oggetto dati del risultato dell'operazione impostando il *parametro pdwEffect* di [**IDropTarget::D rop**](/windows/win32/api/oleidl/nf-oleidl-idroptarget-drop) sul valore [**DROPEFFECT**](../com/dropeffect-constants.md) appropriato. Con gli oggetti dati shell, la destinazione potrebbe anche dover chiamare [**IDataObject::SetData**](/windows/win32/api/objidl/nf-objidl-idataobject-setdata). Per una descrizione del modo in cui le destinazioni devono rispondere per diversi scenari di trasferimento dei dati, vedere [Gestione degli scenari di trasferimento dei dati della shell](datascenarios.md).

Le sezioni seguenti illustrano brevemente come implementare i metodi [**IDropTarget::D ragEnter**](/windows/win32/api/oleidl/nf-oleidl-idroptarget-dragenter), [**IDropTarget::D ragOver**](/windows/win32/api/oleidl/nf-oleidl-idroptarget-dragover)e [**IDropTarget::D rop.**](/windows/win32/api/oleidl/nf-oleidl-idroptarget-drop) Per altri dettagli, vedere la documentazione di riferimento.

### <a name="dragenter-method"></a>Metodo DragEnter

Il sistema chiama il [**metodo IDropTarget::D ragEnter**](/windows/win32/api/oleidl/nf-oleidl-idroptarget-dragenter) quando il cursore entra nella finestra di destinazione. I parametri forniscono alla destinazione la posizione del cursore, lo stato dei tasti di modifica della tastiera, ad esempio ctrl, e un puntatore all'interfaccia [**IDataObject dell'oggetto**](/windows/win32/api/objidl/nn-objidl-idataobject) dati. La destinazione è responsabile dell'utilizzo di tale interfaccia per determinare se può accettare uno dei formati contenuti nell'oggetto dati. Se possibile, in genere lascia invariato il valore di *pdwEffect.* Se non può accettare dati dall'oggetto dati, imposta il *parametro pdwEffect* su DROPEFFECT \_ NONE. Il sistema passa il valore di questo parametro all'interfaccia [**IDropSource**](/windows/win32/api/oleidl/nn-oleidl-idropsource) dell'oggetto dati per consentire la visualizzazione dell'immagine di trascinamento appropriata.

Le destinazioni non devono usare [**il metodo IDataObject::GetData**](/windows/win32/api/objidl/nf-objidl-idataobject-getdata) per eseguire il rendering dei dati della shell prima che siano stati eliminati. Il rendering completo dei dati dell'oggetto per ogni occorrenza di questo tipo potrebbe causare il blocco del cursore di trascinamento. Per evitare questo problema, alcuni oggetti shell contengono un [formato CFSTR \_ INDRAGLOOP.](clipboard.md) Estraendo questo formato, le destinazioni possono controllare lo stato del ciclo di trascinamento evitando il rendering a elevato utilizzo di memoria dei dati dell'oggetto. Il valore dei dati del formato è **un valore DWORD** impostato su un valore diverso da zero se l'oggetto dati si trova all'interno di un ciclo di trascinamento. Il valore dei dati del formato è impostato su zero se i dati sono stati eliminati.

Se la destinazione può accettare dati dall'oggetto dati, deve esaminare **grfKeyState** per determinare se sono stati premuti tasti di modifica per modificare il normale comportamento di rilascio. Ad esempio, l'operazione predefinita è in genere uno spostamento, ma la combinazione di tasti CTRL indica in genere un'operazione di copia.

Mentre il cursore è posizionato sulla finestra di destinazione, la destinazione può usare l'oggetto [helper](#using-the-drag-and-drop-helper-object) di trascinamento della selezione per sostituire l'immagine di trascinamento dell'oggetto dati con la propria. In questo caso, [**IDropTarget::D ragEnter**](/windows/win32/api/oleidl/nf-oleidl-idroptarget-dragenter) deve chiamare [**IDropTargetHelper::D ragEnter**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-idroptargethelper-dragenter) per passare le informazioni contenute nei parametri *DragEnter* all'oggetto helper di trascinamento della selezione.

### <a name="dragover-method"></a>Metodo DragOver

Quando il cursore si sposta all'interno della finestra di destinazione, il sistema chiama periodicamente il metodo [**IDropTarget::D ragOver.**](/windows/win32/api/oleidl/nf-oleidl-idroptarget-dragover) I parametri forniscono alla destinazione la posizione del cursore e lo stato dei tasti di modifica della tastiera, ad esempio ctrl. **IDropTarget::D ragOver** ha le stesse responsabilità di [**IDropTarget::D ragEnter**](/windows/win32/api/oleidl/nf-oleidl-idroptarget-dragenter)e le implementazioni sono in genere molto simili.

Se la destinazione usa l'oggetto helper di trascinamento della selezione, [**IDropTarget::D ragOver**](/windows/win32/api/oleidl/nf-oleidl-idroptarget-dragover) deve chiamare [**IDropTargetHelper::D ragOver**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-idroptargethelper-dragover) per inoltrare le informazioni contenute nei parametri *DragOver* all'oggetto helper di trascinamento della selezione.

### <a name="drop-method"></a>Metodo Drop

Il sistema chiama il [**metodo IDropTarget::D per**](/windows/win32/api/oleidl/nf-oleidl-idroptarget-drop) notificare alla destinazione che l'utente ha eliminato i dati, in genere rilasciando il pulsante del mouse. **IDropTarget::D ha** gli stessi parametri di [**IDropTarget::D ragEnter**](/windows/win32/api/oleidl/nf-oleidl-idroptarget-dragenter). La destinazione in genere risponde estraendo uno o più formati dall'oggetto dati. Al termine, la destinazione deve impostare il *parametro pdwEffect* su un [**valore DROPEFFECT**](../com/dropeffect-constants.md) che indica il risultato dell'operazione. Per alcuni tipi di trasferimento dei dati della shell, la destinazione deve chiamare anche [**IDataObject::SetData**](/windows/win32/api/objidl/nf-objidl-idataobject-setdata) per passare un formato con informazioni aggiuntive sul risultato dell'operazione all'oggetto dati. Per una descrizione dettagliata, vedere [Gestione degli scenari di trasferimento dei dati della shell.](datascenarios.md)

Se la destinazione usa l'oggetto helper di trascinamento della selezione, [**IDropTarget::D helper deve**](/windows/win32/api/oleidl/nf-oleidl-idroptarget-drop) chiamare [**IDropTargetHelper::D helper per**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-idroptargethelper-drop) inoltrare le informazioni contenute nei parametri [**IDropTargetHelper::D ragOver**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-idroptargethelper-dragover) all'oggetto helper di trascinamento della selezione.

## <a name="using-the-drag-and-drop-helper-object"></a>Uso dell'oggetto helper di trascinamento della selezione

L'oggetto helper di trascinamento della selezione (CLSID DragDropHelper) viene esportato dalla shell per consentire alle destinazioni di specificare l'immagine di trascinamento mentre si trova sopra la finestra \_ di destinazione. Per usare l'oggetto helper di trascinamento della selezione, creare un oggetto server in-process chiamando [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) con un identificatore di classe (CLSID) di CLSID \_ DragDropHelper. L'oggetto helper di trascinamento della selezione espone due interfacce usate nel modo seguente:

-   [**L'interfaccia IDragSourceHelper**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-idragsourcehelper) consente all'obiettivo di rilascio di specificare un'icona per rappresentare l'oggetto dati.
-   [**L'interfaccia IDropTargetHelper**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-idroptargethelper) consente all'obiettivo di rilascio di informare l'oggetto helper di trascinamento della selezione della posizione del cursore e di mostrare o nascondere l'icona dei dati.

### <a name="using-the-idragsourcehelper-interface"></a>Uso dell'interfaccia IDragSourceHelper

[**L'interfaccia IDragSourceHelper**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-idragsourcehelper) viene esposta dall'oggetto helper di trascinamento della selezione per consentire a un obiettivo di rilascio di fornire l'immagine che verrà visualizzata mentre il cursore si trova sopra la finestra di destinazione. **IDragSourceHelper offre** due modi alternativi per specificare la bitmap da usare come immagine di trascinamento:

-   Le destinazioni di rilascio che dispongono di una finestra possono registrare un messaggio di finestra DI GETDRAGIMAGE inizializzando l'oggetto helper di trascinamento della selezione con \_ [**IDragSourceHelper::InitializeFromWindow**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-idragsourcehelper-initializefromwindow). Quando la destinazione riceve un messaggio DI GETDRAGIMAGE, il gestore inserisce le informazioni sulla bitmap dell'immagine di trascinamento nella struttura \_ [**SHDRAGIMAGE**](/windows/desktop/api/Shobjidl_core/ns-shobjidl_core-shdragimage) passata come valore *lParam del* messaggio.
-   Le destinazioni di rilascio senza finestra specificano una bitmap quando inizializzano l'oggetto helper di trascinamento della selezione [**con IDragSourceHelper::InitializeFromBitmap.**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-idragsourcehelper-initializefrombitmap)

### <a name="using-the-idroptargethelper-interface"></a>Uso dell'interfaccia IDropTargetHelper

Questa interfaccia consente all'obiettivo di rilascio di notificare all'oggetto helper di trascinamento della selezione quando il cursore entra o esce dalla destinazione. Mentre il cursore è posizionato sulla finestra di destinazione, [**IDropTargetHelper**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-idroptargethelper) consente alla destinazione di fornire all'oggetto helper di trascinamento della selezione le informazioni ricevute dalla destinazione tramite [**l'interfaccia IDropTarget.**](/windows/win32/api/oleidl/nn-oleidl-idroptarget)

Quattro dei metodi [**IDropTargetHelper,**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-idroptargethelper) [**IDropTargetHelper::D ragEnter**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-idroptargethelper-dragenter), [**IDropTargetHelper::D ragLeave**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-idroptargethelper-dragleave), [**IDropTargetHelper::D ragOver**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-idroptargethelper-dragover)e [**IDropTargetHelper::D,**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-idroptargethelper-drop)sono associati al metodo [**IDropTarget**](/windows/win32/api/oleidl/nn-oleidl-idroptarget) con lo stesso nome. Per usare l'oggetto helper di trascinamento della selezione, ognuno dei metodi **IDropTarget** deve chiamare il metodo **IDropTargetHelper** corrispondente per inoltrare le informazioni all'oggetto helper di trascinamento della selezione. Il quinto **metodo IDropTargetHelper,** [**IDropTargetHelper::Show,**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-idroptargethelper-show)notifica all'oggetto helper di trascinamento della selezione di mostrare o nascondere l'immagine di trascinamento. Questo metodo viene usato quando si trascina su una finestra di destinazione in una modalità video a bassa profondità di colore. Consente alla destinazione di nascondere l'immagine di trascinamento mentre disegna la finestra.

 

 
