---
description: La procedura per implementare un'estensione dello spazio dei nomi è simile a quella per qualsiasi altro oggetto Component Object Model (COM) in-process.
title: Implementazione delle interfacce di oggetti della cartella di base
ms.topic: article
ms.date: 05/31/2018
ms.assetid: a45b8011-5355-429b-8935-4a7bdb5d2316
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: c05f5d2e4c21a923856c7324ad2d407230fa7595
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104980002"
---
# <a name="implementing-the-basic-folder-object-interfaces"></a>Implementazione delle interfacce di oggetti della cartella di base

La procedura per implementare un'estensione dello spazio dei nomi è simile a quella per qualsiasi altro oggetto Component Object Model (COM) in-process. Tutte le estensioni devono supportare tre interfacce primarie che forniscono a Esplora risorse le informazioni di base necessarie per visualizzare le cartelle dell'estensione nella visualizzazione albero. Tuttavia, per sfruttare appieno le funzionalità di Esplora risorse, è necessario che l'estensione esponga anche una o più interfacce facoltative che supportano funzionalità più sofisticate, come i menu di scelta rapida o il trascinamento della selezione, e forniscono una visualizzazione cartelle.

In questo documento viene illustrato come implementare le interfacce primarie e facoltative chiamate da Esplora risorse per informazioni sul contenuto dell'estensione. Per informazioni su come implementare una visualizzazione cartelle e su come personalizzare Esplora risorse, vedere Implementazione di [una visualizzazione cartelle](../lwef/nse-folderview.md).

-   [Implementazione e registrazione di base](#basic-implementation-and-registration)
    -   [Registrazione di un'estensione](#registering-an-extension)
-   [Gestione di PIDL](#handling-pidls)
    -   [Creazione di una struttura SHITEMID](#creating-an-shitemid-structure)
    -   [Creazione di un PIDL](#constructing-a-pidl)
    -   [Interpretazione di PIDL](#interpreting-pidls)
-   [Implementazione delle interfacce primarie](#implementing-the-primary-interfaces)
    -   [Interfaccia IPersistFolder](#ipersistfolder-interface)
    -   [Interfaccia IShellFolder](#ishellfolder-interface)
    -   [Interfaccia IEnumIDList](#ienumidlist-interface)
-   [Implementazione delle interfacce facoltative](#implementing-the-optional-interfaces)
    -   [IExtractIcon](#iextracticon)
    -   [IContextMenu](#icontextmenu)
    -   [IQueryInfo](#iqueryinfo)
    -   [IDataObject e IDropTarget](#idataobject-and-idroptarget)
-   [Utilizzo dell'implementazione della visualizzazione della cartella della shell predefinita](#working-with-the-default-shell-folder-view-implementation)

## <a name="basic-implementation-and-registration"></a>Implementazione e registrazione di base

Come server COM in-process, la DLL deve esporre diverse funzioni e interfacce standard:

-   [**DllCanUnloadNow**](/windows/win32/api/combaseapi/nf-combaseapi-dllcanunloadnow)
-   [**DllGetClassObject**](/windows/win32/api/combaseapi/nf-combaseapi-dllgetclassobject)
-   [**IClassFactory**](/windows/win32/api/unknwn/nn-unknwn-iclassfactory)
-   [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown)

Queste funzioni e interfacce vengono implementate nello stesso modo in cui si trovano per la maggior parte degli altri oggetti COM. Per informazioni dettagliate, vedere la [documentazione com](../com/the-component-object-model.md).

### <a name="registering-an-extension"></a>Registrazione di un'estensione

Come per tutti gli oggetti COM, è necessario creare un GUID identificatore di classe (CLSID) per l'estensione. Registrare l'oggetto creando una sottochiave del **CLSID \_ \_ radice delle classi HKEY** \\  denominato per il CLSID dell'estensione. La DLL deve essere registrata come server in-process e deve specificare il modello di threading dell'Apartment. È possibile personalizzare il comportamento della cartella radice di un'estensione aggiungendo un'ampia gamma di sottochiavi e valori alla chiave CLSID dell'estensione.

Molti di questi valori si applicano solo alle estensioni con i punti di giunzione virtuali. Questi valori non si applicano alle estensioni i cui punti di giunzione sono file system cartelle. Per ulteriori informazioni, vedere [specifica del percorso di un'estensione dello spazio dei nomi](nse-junction.md). Per modificare il comportamento di un'estensione con un punto di giunzione virtuale, aggiungere uno o più dei valori seguenti alla chiave CLSID dell'estensione:

-   WantsFORPARSING. Il nome di analisi per un'estensione con un punto di giunzione virtuale in genere avrà il formato:: {*GUID*}. Le estensioni di questo tipo contengono in genere elementi virtuali. Tuttavia, alcune estensioni, ad esempio documenti, corrispondono in realtà a file system cartelle, anche se hanno punti di giunzione virtuali. Se l'estensione rappresenta file system oggetti in questo modo, è possibile impostare il valore WantsFORPARSING. In Esplora risorse verrà quindi richiesto il nome di analisi della cartella radice chiamando il metodo [**IShellFolder:: GetDisplayNameOf**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-getdisplaynameof) dell'oggetto Folder con *UFlags* impostato su **SHGDN \_ FORPARSING** e *PIDL* impostato su un singolo puntatore vuoto a un elenco di identificatori di elemento (PIDL). Un PIDL vuoto contiene solo un carattere di terminazione. Il metodo deve quindi restituire il nome di analisi della cartella radice:: {*GUID*}.
-   HideFolderVerbs. I verbi registrati nella cartella **\_ \_ radice delle classi HKEY** \\  sono normalmente associati a tutte le estensioni. Vengono visualizzati nel menu di scelta rapida dell'estensione e possono essere richiamati da [**ShellExecute**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecutea). Per impedire che uno di questi verbi venga associato all'estensione, impostare il valore HideFolderVerbs.
-   HideAsDelete. Se un utente tenta di eliminare l'estensione, Esplora risorse nasconde invece l'estensione.
-   HideAsDeletePerUser. Questo valore ha lo stesso effetto di HideAsDelete, ma per singolo utente. L'estensione è nascosta solo per gli utenti che hanno tentato di eliminarla. L'estensione è visibile a tutti gli altri utenti.
-   QueryForOverlay. Impostare questo valore per indicare che l'icona della cartella radice può avere una sovrapposizione di icone. L'oggetto Folder deve supportare l'interfaccia [**IShellIconOverlay**](/windows/win32/api/shlobj_core/nn-shlobj_core-ishelliconoverlay) . Prima di visualizzare l'icona della cartella radice, in Esplora risorse verrà richiesta un'icona di sovrapposizione chiamando uno dei due metodi **IShellIconOverlay** con *pidlItem* impostato su un PIDL vuoto.

I valori e le sottochiavi rimanenti si applicano a tutte le estensioni:

-   Per specificare il nome visualizzato della cartella del punto di giunzione dell'estensione, impostare il valore predefinito della sottochiave CLSID dell'estensione su una stringa appropriata.
-   Quando il cursore passa su una cartella, viene in genere visualizzato un infotip che descrive il contenuto della cartella. Per fornire un infotip per la cartella radice dell'estensione, creare un valore InfoTip **reg \_ SZ** per la chiave CLSID dell'estensione e impostarlo su una stringa appropriata.
-   Per specificare un'icona personalizzata per la cartella radice dell'estensione, creare una sottochiave della sottochiave CLSID dell'estensione denominata **DefaultIcon**. Impostare il valore predefinito di **DefaultIcon** su un valore **reg \_ SZ** contenente il nome del file che contiene l'icona, seguito da una virgola, seguita da un segno meno, seguito dall'indice dell'icona in tale file.
-   Per impostazione predefinita, il menu di scelta rapida della cartella radice dell'estensione conterrà gli elementi definiti nella **\_ \_ \\ cartella radice delle classi HKEY**. Gli elementi **Delete**, **Rename** e **Properties** vengono aggiunti se sono stati impostati i flag SFGAO \_ xxx appropriati. È possibile aggiungere altri elementi al menu di scelta rapida della cartella radice o eseguire l'override di elementi esistenti in modo analogo a quanto avviene per un [tipo di file](fa-file-types.md). Creare una sottochiave della **Shell** sotto la chiave CLSID dell'estensione e definire i comandi come descritto in [estensione dei menu di scelta rapida](context.md).
-   Se è necessario un modo più flessibile per gestire il menu di scelta rapida della cartella radice, è possibile implementare un [gestore di menu di scelta rapida](context-menu-handlers.md). Per registrare il gestore del menu di scelta rapida, creare una chiave **ShellEx** nella chiave CLSID dell'estensione. Registrare il CLSID del gestore come per i [gestori di estensioni della shell di creazione](handlers.md)convenzionali.
-   Per aggiungere una pagina alla finestra delle proprietà delle proprietà della cartella radice, assegnare alla cartella l'attributo **\_ HASPROPSHEET di SFGAO** e implementare un [gestore della finestra delle proprietà](propsheet-handlers.md). Per registrare il gestore della finestra delle proprietà, creare una chiave **ShellEx** nella chiave CLSID dell'estensione. Registrare il CLSID del gestore come per i [gestori di estensioni della shell di creazione](handlers.md)convenzionali.
-   Per specificare gli attributi della cartella radice, aggiungere una sottochiave **ShellFolder** alla sottochiave CLSID dell'estensione. Creare un valore di attributi e impostarlo sulla combinazione appropriata di flag [**SFGAO \_ xxx**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-getattributesof) .

Nella tabella seguente sono elencati alcuni attributi di uso comune per le cartelle radice.



| Flag                | valore      | Descrizione                                                                                                                                                                                                                                                                                                       |
|---------------------|------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \_cartella SFGAO       | 0x20000000 | La cartella radice dell'estensione contiene uno o più elementi.                                                                                                                                                                                                                                                           |
| \_HASSUBFOLDER SFGAO | 0x80000000 | La cartella radice dell'estensione contiene una o più sottocartelle. In Esplora risorse verrà inserito un segno più (+) accanto all'icona della cartella.                                                                                                                                                                               |
| \_CANDELETE SFGAO    | 0x00000020 | La cartella radice dell'estensione può essere eliminata dall'utente. Il menu di scelta rapida della cartella includerà un elemento **Delete** . Questo flag deve essere impostato per i punti di giunzione posizionati in una delle [cartelle virtuali](nse-junction.md).                                                                                 |
| \_CANRENAME SFGAO    | 0x00000010 | La cartella radice dell'estensione può essere rinominata dall'utente. Il menu di scelta rapida della cartella avrà un elemento **Rename** .                                                                                                                                                                                                   |
| \_HASPROPSHEET SFGAO | 0x00000040 | La cartella radice dell'estensione dispone di una finestra delle proprietà **Proprietà** . Il menu di scelta rapida della cartella avrà un elemento **Proprietà** . Per fornire la finestra delle proprietà, è necessario implementare un [gestore della finestra delle proprietà](propsheet-handlers.md). Registrare il gestore sotto la chiave CLSID dell'estensione, come illustrato in precedenza. |



 

Nell'esempio seguente viene illustrata la voce del registro di sistema CLSID per un'estensione con un nome visualizzato di estensione. L'estensione dispone di un'icona personalizzata contenuta nella DLL dell'estensione con indice 1. Sono impostati gli attributi **SFGAO \_ Folder**, **SFGAO \_ HASSUBFOLDER** e **SFGAO \_ CANDELETE** .

```
HKEY_CLASSES_ROOT
   CLSID
      {Extension CLSID}
         (Default) = MyExtension
         InfoTip = Some appropriate text
      DefaultIcon
         (Default) = c:\MyDir\MyExtension.dll,-1
      InProcServer32
         (Default) = c:\MyDir\MyExtension.dll
         ThreadingModel = Apartment
      ShellFolder
         Attributes = 0xA00000020
```

## <a name="handling-pidls"></a>Gestione di PIDL

Ogni elemento nello spazio dei nomi della shell deve avere un PIDL univoco. Esplora risorse assegna un PIDL alla cartella radice e passa il valore all'estensione durante l'inizializzazione. L'estensione è quindi responsabile dell'assegnazione di una PIDL costruita correttamente a ognuno dei relativi oggetti e di fornire tali PIDL a Esplora risorse su richiesta. Quando la shell usa un PIDL per identificare uno degli oggetti dell'estensione, l'estensione deve essere in grado di interpretare il PIDL e identificare l'oggetto specifico. L'estensione deve inoltre assegnare un nome [**visualizzato**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-setnameof) e un *nome di analisi* a ogni oggetto. Poiché PIDL vengono utilizzati praticamente da ogni interfaccia di cartella, le estensioni implementano in genere un singolo *gestore di PIDL* per gestire tutte queste attività.

Il termine PIDL è breve per una struttura [**ItemId**](/windows/desktop/api/Shtypes/ns-shtypes-itemidlist) o un puntatore a una struttura di questo tipo, a seconda del contesto. Come dichiarato, una struttura **ItemId** ha un singolo membro, una struttura [**SHITEMID**](/windows/desktop/api/Shtypes/ns-shtypes-shitemid) . La struttura **ItemId** dell'oggetto è in realtà una matrice compressa di due o più strutture **SHITEMID** . L'ordine di queste strutture definisce un percorso attraverso lo spazio dei nomi, nello stesso modo in cui c: \\ directory \\ MyFile definisce un percorso attraverso la file System. In genere, il PIDL di un oggetto sarà costituito da una serie di strutture **SHITEMID** che corrispondono alle cartelle che definiscono il percorso dello spazio dei nomi, seguito dalla struttura **SHITEMID** dell'oggetto, seguito da un carattere di terminazione.

Il carattere di terminazione è una struttura [**SHITEMID**](/windows/desktop/api/Shtypes/ns-shtypes-shitemid) e il membro *CB* è impostato su **null**. Il carattere di terminazione è necessario perché il numero di strutture **SHITEMID** nel PIDL di un oggetto dipende dalla posizione dell'oggetto nello spazio dei nomi della shell e dal punto iniziale del percorso. Inoltre, le dimensioni delle varie strutture **SHITEMID** possono variare. Quando si riceve un PIDL, non esiste un modo semplice per determinarne le dimensioni o anche il numero totale di strutture **SHITEMID** . Al contrario, è necessario "esaminare" l'array compresso, struttura per struttura, fino a raggiungere il carattere di terminazione.

Per creare un PIDL, l'applicazione deve:

1.  Creare una struttura [**SHITEMID**](/windows/desktop/api/Shtypes/ns-shtypes-shitemid) per ognuno dei relativi oggetti.
2.  Assemblare le strutture [**SHITEMID**](/windows/desktop/api/Shtypes/ns-shtypes-shitemid) rilevanti in un PIDL.

### <a name="creating-an-shitemid-structure"></a>Creazione di una struttura SHITEMID

La struttura [**SHITEMID**](/windows/desktop/api/Shtypes/ns-shtypes-shitemid) di un oggetto identifica in modo univoco l'oggetto all'interno della relativa cartella. Infatti, un tipo di PIDL utilizzato da molti metodi [**IShellFolder**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellfolder) è costituito solo dalla struttura **SHITEMID** dell'oggetto, seguita da un carattere di terminazione. La definizione di una struttura **SHITEMID** è la seguente:


```C++
typedef struct _SHITEMID { 
    USHORT cb; 
    BYTE   abID[1]; 
} SHITEMID, * LPSHITEMID;
```



Il membro *permanente* è l'identificatore dell'oggetto. Poiché la lunghezza di *Atter* non è definita e può variare, il membro *CB* viene impostato sulla dimensione della struttura [**SHITEMID**](/windows/desktop/api/Shtypes/ns-shtypes-shitemid) , in byte.

Poiché né la lunghezza né il contenuto dell' *oggetto sono standardizzati, è possibile* utilizzare qualsiasi schema a cui si desidera assegnare i valori di tipo *rispettabile* . L'unico requisito è che non è possibile avere due oggetti nella stessa cartella con valori identici. Tuttavia, per motivi di prestazioni, la struttura di [**SHITEMID**](/windows/desktop/api/Shtypes/ns-shtypes-shitemid) deve essere allineata a **DWORD**. In altre parole, è necessario creare i valori di *dimora* in modo che *CB* sia un multiplo integrale di 4.

In genere *, fa* riferimento a una struttura definita dall'estensione. Oltre all'ID dell'oggetto, questa struttura viene spesso utilizzata per conservare una serie di informazioni correlate, ad esempio il tipo o gli attributi dell'oggetto. Gli oggetti cartella dell'estensione possono quindi estrarre rapidamente le informazioni dal PIDL anziché dover eseguire una query.

> [!Note]  
> Uno degli aspetti più importanti della progettazione di una struttura di dati per un PIDL consiste nel rendere la struttura permanente e trasportabile. Nel contesto di PIDL, il significato di questi termini è:
>
> -   Persistente. Il sistema posiziona spesso PIDL in vari tipi di archiviazione a lungo termine, ad esempio i file di collegamento. Può quindi recuperare questi PIDL dalla risorsa di archiviazione in un secondo momento, probabilmente dopo il riavvio del sistema. Un PIDL recuperato dalla risorsa di archiviazione deve essere ancora valido e significativo per l'estensione. Questo requisito significa, ad esempio, che non è consigliabile usare puntatori o handle nella struttura PIDL. PIDL che contengono questo tipo di dati normalmente non saranno significativi quando il sistema li recupererà in un secondo momento dalla risorsa di archiviazione.
> -   Trasportabili. Un PIDL deve rimanere significativo quando viene trasportato da un computer a un altro. È ad esempio possibile scrivere un PIDL in un file di collegamento, copiarlo in un disco floppy e trasportarlo in un altro computer. Il PIDL dovrebbe ancora essere significativo per l'estensione in esecuzione nel secondo computer. Ad esempio, per assicurarsi che i PIDL siano trasportabili, usare in modo esplicito i caratteri ANSI o Unicode. Evitare i tipi di dati, ad esempio **TCHAR** o **LPTSTR**. Se si usano questi tipi di dati, un PIDL creato in un computer che esegue una versione Unicode dell'estensione non sarà leggibile da una versione ANSI di tale estensione in esecuzione in un computer diverso.

 

Nella dichiarazione seguente viene illustrato un semplice esempio di una struttura di dati.


```C++
typedef struct tagMYPIDLDATA {
  USHORT cb;
  DWORD dwType;
  WCHAR wszDisplayName[40];
} MYPIDLDATA, *LPMYPIDLDATA;
```



Il membro **CB** è impostato sulla dimensione della struttura **MYPIDLDATA** . Questo membro rende **MYPIDLDATA** una struttura [**SHITEMID**](/windows/desktop/api/Shtypes/ns-shtypes-shitemid) valida, in e di se stessa. Gli altri membri sono equivalenti **al membro di** una struttura **SHITEMID** e contengono dati privati. Il membro **dwType** è un valore definito dall'estensione che indica il tipo di oggetto. Per questo esempio, **dwType** è impostato su **true** per le cartelle e **false** in caso contrario. Questo membro consente, ad esempio, di determinare rapidamente se l'oggetto è una cartella o meno. Il membro **wszDisplayName** contiene il nome visualizzato dell'oggetto. Poiché non si assegna lo stesso nome visualizzato a due oggetti diversi nella stessa cartella, il nome visualizzato viene utilizzato anche come ID oggetto. In questo esempio, **wszDisplayName** è impostato su 40 caratteri per garantire che la struttura **SHITEMID** sarà allineata a **DWORD**. Per limitare le dimensioni del PIDL, è possibile usare invece una matrice di caratteri a lunghezza variabile e modificare di conseguenza il valore di CB. Riempire la stringa di visualizzazione con un numero \\ di caratteri ' 0' sufficiente per mantenere l'allineamento **DWORD** della struttura. Altri membri che potrebbero essere utili da inserire nella struttura includono le dimensioni, gli attributi o il nome di analisi dell'oggetto.

### <a name="constructing-a-pidl"></a>Creazione di un PIDL

Dopo aver definito le strutture [**SHITEMID**](/windows/desktop/api/Shtypes/ns-shtypes-shitemid) per gli oggetti, è possibile usarle per creare un PIDL. PIDL può essere costruito per diversi scopi, ma la maggior parte delle attività usa uno dei due tipi di PIDL. Il più semplice, un PIDL a livello singolo, identifica l'oggetto relativo alla cartella padre. Questo tipo di PIDL viene usato da molti dei metodi [**IShellFolder**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellfolder) . Un PIDL a livello singolo contiene la struttura **SHITEMID** dell'oggetto, seguita da un carattere di terminazione. Un PIDL completo definisce un percorso attraverso la gerarchia dello spazio dei nomi dal desktop all'oggetto. Questo tipo di PIDL inizia sul desktop e contiene una struttura **SHITEMID** per ogni cartella nel percorso, seguita dall'oggetto e dal carattere di terminazione. Un PIDL completo identifica in modo univoco l'oggetto all'interno dell'intero spazio dei nomi della shell.

Il modo più semplice per costruire un PIDL consiste nel lavorare direttamente con la struttura [**ItemId**](/windows/desktop/api/Shtypes/ns-shtypes-itemidlist) . Creare una struttura **ItemId** , ma allocare memoria sufficiente per mantenere tutte le strutture [**SHITEMID**](/windows/desktop/api/Shtypes/ns-shtypes-shitemid) . L'indirizzo di questa struttura punterà alla struttura **SHITEMID** iniziale. Definire i valori per i membri di questa struttura iniziale, quindi accodare il numero di strutture **SHITEMID** aggiuntive necessarie nell'ordine appropriato. La procedura seguente illustra come creare un PIDL a un solo livello. Contiene due strutture **SHITEMID** , una struttura **MYPIDLDATA** seguita da un carattere di terminazione:

1.  Utilizzare la funzione [**CoTaskMemAlloc**](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemalloc) per allocare memoria per il PIDL. Allocare memoria sufficiente per i dati privati più un **ushort** (due byte) per il carattere di terminazione. Eseguire il cast del risultato a LPMYPIDLDATA.
2.  Impostare il membro CB della prima struttura **MYPIDLDATA** sulla dimensione della struttura. Per questo esempio, è necessario impostare **CB** su sizeof (MYPIDLDATA). Se si vuole usare una struttura a lunghezza variabile, sarà necessario calcolare il valore di **CB**.
3.  Assegnare i valori appropriati ai membri dati privati.
4.  Calcolare l'indirizzo della struttura [**SHITEMID**](/windows/desktop/api/Shtypes/ns-shtypes-shitemid) successiva. Eseguire il cast dell'indirizzo della struttura MYPIDLDATA corrente a LPBYTE e aggiungere tale valore al valore di **CB** determinato nel passaggio 3.
5.  In questo caso, la struttura [**SHITEMID**](/windows/desktop/api/Shtypes/ns-shtypes-shitemid) successiva è il carattere di terminazione. Impostare il membro **CB** della struttura su zero.

Per PIDL più lunghe, allocare memoria sufficiente e ripetere i passaggi 3-5 per ogni struttura [**SHITEMID**](/windows/desktop/api/Shtypes/ns-shtypes-shitemid) aggiuntiva.

La funzione di esempio seguente accetta il tipo e il nome visualizzato di un oggetto e restituisce il PIDL a singolo livello dell'oggetto. La funzione presuppone che il nome visualizzato, incluso il carattere **null** di terminazione, non superi il numero di caratteri dichiarati per la struttura **MYPIDLDATA** . Se il presupposto risulta errato, la funzione [**StringCbCopyW**](/windows/win32/api/strsafe/nf-strsafe-stringcbcopya) tronca il nome visualizzato. La variabile **g \_ pMalloc** è un puntatore [**IMalloc**](/windows/win32/api/objidlbase/nn-objidlbase-imalloc) creato altrove e archiviato in una variabile globale.


```C++
LPITEMIDLIST CreatePIDL(DWORD dwType, LPCWSTR pwszDisplayName)
{
    LPMYPIDLDATA   pidlOut;
    USHORT         uSize;

    pidlOut = NULL;

    //Calculate the size of the MYPIDLDATA structure.
    uSize = sizeof(MYPIDLDATA);

    // Allocate enough memory for the PIDL to hold a MYPIDLDATA structure 
    // plus the terminator
    pidlOut = (LPMYPIDLDATA)m_pMalloc->Alloc(uSize + sizeof(USHORT));

    if(pidlOut)
    {
       //Assign values to the members of the MYPIDLDATA structure
       //that is the PIDL's first SHITEMID structure
       pidlOut->cb = uSize;
       pidlOut->dwType = dwType;
       hr = StringCbCopyW(pidlOut->wszDisplayName, 
                          sizeof(pidlOut->wszDisplayName), pwszDisplayName);
       
       // TODO: Add error handling here to verify the HRESULT returned 
       // by StringCbCopyW.

       //Advance the pointer to the start of the next SHITEMID structure.
       pidlOut = (LPMYPIDLDATA)((LPBYTE)pidlOut + pidlOut->cb);

       //Create the terminating null character by setting cb to 0.
       pidlOut->cb = 0;
    }

    return pidlOut;
```



Un PIDL completo deve avere strutture [**SHITEMID**](/windows/desktop/api/Shtypes/ns-shtypes-shitemid) per ogni oggetto dal desktop all'oggetto. L'estensione riceve un PIDL completo per la cartella radice quando la shell chiama [**IPersistFolder:: Initialize**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ipersistfolder-initialize). Per costruire un PIDL completo per un oggetto, prendere il PIDL che la shell ha assegnato alla cartella radice e aggiungere le strutture **SHITEMID** necessarie per passare dalla cartella radice all'oggetto.

### <a name="interpreting-pidls"></a>Interpretazione di PIDL

Quando la shell o un'applicazione chiama una delle interfacce dell'estensione per richiedere informazioni su un oggetto, in genere l'oggetto viene identificato da un PIDL. Alcuni metodi, ad esempio [**IShellFolder:: GetUIObjectOf**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-getuiobjectof), usano PIDL relativi alla cartella padre e sono semplici da interpretare. Tuttavia, l'estensione riceverà probabilmente anche PIDL completi. PIDL Manager deve quindi determinare gli oggetti a cui fa riferimento PIDL.

Ciò che complica l'attività di associazione di un oggetto a un PIDL completo è che una o più strutture [**SHITEMID**](/windows/desktop/api/Shtypes/ns-shtypes-shitemid) iniziali in PIDL possono appartenere a oggetti che si trovano all'esterno dell'estensione nello spazio dei nomi della shell. Non esiste alcun modo per interpretare il significato del membro *permanente* di tali strutture. L'estensione deve eseguire il "percorso" dell'elenco di strutture **SHITEMID** fino a raggiungere la struttura che corrisponde alla cartella radice. Da questo punto in poi si saprà come interpretare le informazioni nelle strutture **SHITEMID** .

Per esaminare il PIDL, prendere il primo valore *CB* e aggiungerlo all'indirizzo di PIDL per far avanzare il puntatore all'inizio della struttura [**SHITEMID**](/windows/desktop/api/Shtypes/ns-shtypes-shitemid) successiva. Verrà quindi fatto riferimento al membro *CB* di tale struttura, che può essere usato per far avanzare il puntatore all'inizio della struttura **SHITEMID** successiva e così via. Ogni volta che si avanza il puntatore, esaminare la struttura **SHITEMID** per determinare se è stata raggiunta la radice dello spazio dei nomi dell'estensione.

## <a name="implementing-the-primary-interfaces"></a>Implementazione delle interfacce primarie

Come per tutti gli oggetti COM, l'implementazione di un'estensione è in gran parte l'implementazione di una raccolta di interfacce. In questa sezione vengono illustrate le tre interfacce principali che devono essere implementate da tutte le estensioni. Vengono utilizzati per l'inizializzazione e per fornire Windows Explorer con informazioni di base sul contenuto dell'estensione. Queste interfacce, oltre a una [visualizzazione di cartelle](../lwef/nse-folderview.md), sono tutte richieste per un'estensione funzionale. Tuttavia, per sfruttare appieno le funzionalità di Esplora risorse, la maggior parte delle estensioni implementa anche una o più interfacce facoltative.

### <a name="ipersistfolder-interface"></a>Interfaccia IPersistFolder

L'interfaccia [**IPersistFolder**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ipersistfolder) viene chiamata per inizializzare un nuovo oggetto Folder. Il metodo [**IPersistFolder:: Initialize**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ipersistfolder-initialize) assegna un PIDL completo al nuovo oggetto. Archiviare questo PIDL per un uso successivo. Ad esempio, un oggetto Folder deve usare questo PIDL per costruire PIDL completi per gli elementi figlio dell'oggetto. Il creatore dell'oggetto Folder può anche chiamare [**IPersist:: GetClassID**](/windows/win32/api/objidl/nf-objidl-ipersist-getclassid) per richiedere il CLSID dell'oggetto.

In genere, un oggetto Folder viene creato e inizializzato dal metodo [**IShellFolder:: BindToObject**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-bindtoobject) della relativa cartella padre. Tuttavia, quando un utente accede all'estensione, Esplora risorse crea e Inizializza l'oggetto cartella radice dell'estensione. Il PIDL che l'oggetto cartella radice riceve tramite [**IPersistFolder:: Initialize**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ipersistfolder-initialize) contiene il percorso dal desktop alla cartella radice, che sarà necessario per costruire PIDL completi per l'estensione.

### <a name="ishellfolder-interface"></a>Interfaccia IShellFolder

La shell considera un'estensione come una raccolta ordinata gerarchica di oggetti Folder. L'interfaccia [**IShellFolder**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellfolder) è il nucleo di qualsiasi implementazione di estensione. Rappresenta un oggetto Folder e fornisce a Esplora risorse la maggior parte delle informazioni necessarie per visualizzare il contenuto della cartella.

[**IShellFolder**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellfolder) è in genere l'unica interfaccia di cartella diversa da [**IPersistFolder**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ipersistfolder) esposta direttamente da un oggetto Folder. Mentre Esplora risorse usa un'ampia gamma di interfacce obbligatorie e facoltative per ottenere informazioni sul contenuto della cartella, ottiene i puntatori a tali interfacce tramite **IShellFolder**.

Esplora risorse ottiene il CLSID della cartella radice dell'estensione in diversi modi. Per informazioni dettagliate, vedere [specifica del percorso di un'estensione dello spazio dei nomi](nse-junction.md) o [visualizzazione di una visualizzazione Self-Contained di un'estensione dello spazio dei nomi](nse-view.md). Esplora risorse utilizza quindi tale CLSID per creare e inizializzare un'istanza della cartella radice e una query per un'interfaccia [**IShellFolder**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellfolder) . Tramite l'estensione viene creato un oggetto Folder per rappresentare la cartella radice e viene restituita l'interfaccia **IShellFolder** dell'oggetto. Gran parte del resto dell'interazione tra l'estensione e Esplora risorse viene quindi svolta tramite **IShellFolder**. Esplora risorse chiama **IShellFolder** per:

-   Richiedere un oggetto in grado di enumerare il contenuto della cartella radice.
-   Ottenere vari tipi di informazioni sul contenuto della cartella radice.
-   Richiedere un oggetto che espone una delle interfacce facoltative. È quindi possibile eseguire query su tali interfacce per ottenere informazioni aggiuntive, ad esempio icone o menu di scelta rapida.
-   Richiedere un oggetto cartella che rappresenti una sottocartella della cartella radice.

Quando un utente apre una sottocartella della cartella radice, Esplora risorse chiama [**IShellFolder:: BindToObject**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-bindtoobject). Tramite l'estensione viene creato e inizializzato un nuovo oggetto Folder per rappresentare la sottocartella e viene restituita l'interfaccia [**IShellFolder**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellfolder) . Esplora risorse chiama quindi questa interfaccia per diversi tipi di informazioni e così via fino a quando l'utente non decide di spostarsi altrove nello spazio dei nomi della shell o di chiudere Esplora risorse.

Nella parte restante di questa sezione vengono brevemente descritti i metodi [**IShellFolder**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellfolder) più importanti e come implementarli.

### <a name="enumobjects"></a>EnumObjects

Prima di visualizzare il contenuto di una cartella nella visualizzazione albero, Esplora risorse deve innanzitutto determinare il contenuto della cartella chiamando il metodo [**IShellFolder:: EnumObjects**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-enumobjects) . Questo metodo crea un oggetto enumerazione OLE standard che espone un'interfaccia [**IEnumIDList**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ienumidlist) e restituisce il puntatore a tale interfaccia. L'interfaccia **IEnumIDList** consente a Esplora risorse di ottenere il PIDL di tutti gli oggetti contenuti nella cartella. Questi PIDL vengono quindi usati per ottenere informazioni sugli oggetti contenuti nella cartella. Per altri dettagli, vedere [interfaccia IEnumIDList](#ienumidlist-interface).

> [!Note]  
> Il metodo [**IEnumIDList:: Next**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ienumidlist-next) deve restituire solo PIDL relativi alla cartella padre. PIDL deve contenere solo la struttura [**SHITEMID**](/windows/desktop/api/Shtypes/ns-shtypes-shitemid) dell'oggetto, seguita da un carattere di terminazione.

 

### <a name="createviewobject"></a>CreateViewObject

Prima che il contenuto di una cartella venga visualizzato, Esplora risorse chiama questo metodo per richiedere un puntatore a un'interfaccia [**IShellView**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellview) . Questa interfaccia viene utilizzata da Esplora risorse per gestire la visualizzazione cartelle. Creare un oggetto visualizzazione cartelle e restituire l'interfaccia **IShellView** .

Il metodo [**IShellFolder:: CreateViewObject**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-createviewobject) viene chiamato anche per richiedere una delle interfacce facoltative, ad esempio [**IContextMenu**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-icontextmenu), per la cartella stessa. L'implementazione di questo metodo deve creare un oggetto che espone l'interfaccia richiesta e restituisce il puntatore a interfaccia. Se Esplora risorse necessita di un'interfaccia facoltativa per uno degli oggetti contenuti nella cartella, viene chiamato [**IShellFolder:: GetUIObjectOf**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-getuiobjectof).

### <a name="getuiobjectof"></a>GetUIObjectOf

Sebbene le informazioni di base sul contenuto di una cartella siano disponibili tramite i metodi [**IShellFolder**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellfolder) , l'estensione può fornire anche Esplora risorse con vari tipi di informazioni aggiuntive. Ad esempio, è possibile specificare le icone per il contenuto di una cartella o il menu di scelta rapida di un oggetto. Esplora risorse chiama il metodo [**IShellFolder:: GetUIObjectOf**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-getuiobjectof) per tentare di recuperare informazioni aggiuntive su un oggetto contenuto in una cartella. In Esplora risorse viene specificato l'oggetto per il quale si desiderano le informazioni e l'IID dell'interfaccia pertinente. L'oggetto Folder Crea quindi un oggetto che espone l'interfaccia richiesta e restituisce il puntatore a interfaccia.

Se l'estensione consente agli utenti di trasferire oggetti con il trascinamento della selezione o gli appunti, Esplora risorse chiamerà [**IShellFolder:: GetUIObjectOf**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-getuiobjectof) per richiedere un'interfaccia [**IDataObject**](/windows/win32/api/objidl/nn-objidl-idataobject) o [**IDropTarget**](/windows/win32/api/oleidl/nn-oleidl-idroptarget) . Per informazioni dettagliate, vedere [trasferimento di oggetti Shell con trascinamento della selezione e gli appunti](dragdrop.md).

Esplora risorse chiama [**IShellFolder:: CreateViewObject**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-createviewobject) quando desidera lo stesso tipo di informazioni sulla cartella stessa.

### <a name="bindtoobject"></a>BindToObject

Esplora risorse chiama il metodo [**IShellFolder:: BindToObject**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-bindtoobject) quando un utente tenta di aprire una delle sottocartelle dell'estensione. Se *riid* è impostato su IID \_ IShellFolder, è necessario creare e inizializzare un oggetto cartella che rappresenta la sottocartella e restituire l'interfaccia [**IShellFolder**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellfolder) dell'oggetto.

> [!Note]  
> Attualmente, Esplora risorse chiama questo metodo solo per richiedere un'interfaccia [**IShellFolder**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellfolder) . Tuttavia, non presupporre che questo sarà sempre il caso. Prima di procedere, è consigliabile controllare sempre il valore di *riid* .

 

### <a name="getdisplaynameof"></a>GetDisplayNameOf

Esplora risorse chiama il metodo [**IShellFolder:: GetDisplayNameOf**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-getdisplaynameof) per convertire il PIDL di uno degli oggetti della cartella in un nome. PIDL deve essere relativo alla cartella padre dell'oggetto. In altre parole, deve contenere una singola struttura [**SHITEMID**](/windows/desktop/api/Shtypes/ns-shtypes-shitemid) non **null** . Poiché è possibile denominare gli oggetti in più modi, in Esplora risorse viene specificato il tipo di nome impostando uno o più flag [**SHGDNF**](/windows/win32/api/shobjidl_core/ne-shobjidl_core-_shgdnf) nel parametro *uFlags* . Uno dei due valori, **SHGDN \_ Normal** o **SHGDN \_ InFolder**, verrà impostato in modo da specificare se il nome deve essere relativo alla cartella o rispetto al desktop. Uno degli altri tre valori, **SHGDN \_ FOREDITING**, **SHGDN \_ FORADDRESSBAR** o **SHGDN \_ FORPARSING**, può essere impostato per specificare il nome che verrà usato per.

Il nome deve essere restituito sotto forma di struttura [**STRRET**](/windows/desktop/api/Shtypes/ns-shtypes-strret) . Se **SHGDN \_ FOREDITING**, **SHGDN \_ FORADDRESSBAR** e **SHGDN \_ FORPARSING** non sono impostati, restituire il nome visualizzato dell'oggetto. Se è impostato il flag **SHGDN \_ FORPARSING** , Esplora risorse richiede un nome di analisi. I nomi di analisi vengono passati a [**IShellFolder::P arsedisplayname**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-parsedisplayname) per ottenere PIDL di un oggetto, anche se potrebbe trovarsi in uno o più livelli sotto la cartella corrente nella gerarchia dello spazio dei nomi. Ad esempio, il nome di analisi di un oggetto file system è il percorso. È possibile passare il percorso completo di qualsiasi oggetto nel file system al metodo **IShellFolder::P arsedisplayname** del desktop e restituirà il PIDL completo dell'oggetto.

Mentre i nomi di analisi sono stringhe di testo, non devono necessariamente includere il nome visualizzato. È consigliabile assegnare i nomi di analisi in base a ciò che funzionerà in modo più efficiente quando viene chiamato [**IShellFolder::P arsedisplayname**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-parsedisplayname) . Ad esempio, molte delle cartelle virtuali della shell non fanno parte del file system e non hanno un percorso completo. Al contrario, a ogni cartella viene assegnato un GUID e il nome di analisi assume il formato:: {GUID}. Indipendentemente dallo schema usato, dovrebbe essere in grado di "round trip" in modo affidabile. Se, ad esempio, un chiamante passa un nome di analisi a **IShellFolder::P arsedisplayname** per recuperare PIDL di un oggetto, quindi passa il PIDL a [**IShellFolder:: GetDisplayNameOf**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-getdisplaynameof) con il flag SHGDN **\_ FORPARSING** impostato, il chiamante deve ripristinare il nome di analisi originale.

### <a name="getattributesof"></a>GetAttributesOf

Esplora risorse chiama il metodo [**IShellFolder:: GetAttributesOf**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-getattributesof) per determinare gli attributi di uno o più elementi contenuti in un oggetto cartella. Il valore di *cidl* indica il numero di elementi nella query e *aPidl* punta a un elenco di PIDL.

Poiché i test per alcuni attributi possono richiedere molto tempo, in Esplora risorse la query viene in genere limitata a un subset dei flag disponibili, impostando i relativi valori in *rfgInOut*. Il metodo deve verificare solo gli attributi i cui flag sono impostati in *rfgInOut*. Lasciare i flag validi impostati e deselezionare il resto. Se nella query è incluso più di un elemento, impostare solo i flag che si applicano a tutti gli elementi.

> [!Note]  
> Per visualizzare correttamente un elemento, è necessario che gli attributi siano impostati correttamente. Ad esempio, se un elemento è una cartella che contiene sottocartelle, è necessario impostare il flag **SFGAO \_ HASSUBFOLDER** . In caso contrario, Esplora risorse non visualizzerà più accanto all'icona dell'elemento nella visualizzazione albero.

 

### <a name="parsedisplayname"></a>ParseDisplayName

Il metodo [**IShellFolder::P arsedisplayname**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-parsedisplayname) è in un certo senso un'immagine speculare di [**IShellFolder:: GetDisplayNameOf**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-getdisplaynameof). L'uso più comune di questo metodo consiste nel convertire il nome di analisi di un oggetto nel PIDL associato. Il nome di analisi può fare riferimento a qualsiasi oggetto che si trova sotto la cartella nella gerarchia dello spazio dei nomi. Il PIDL restituito è relativo all'oggetto Folder che espone il metodo e che in genere non è completo. In altre parole, sebbene PIDL possa contenere diverse strutture [**SHITEMID**](/windows/desktop/api/Shtypes/ns-shtypes-shitemid) , il primo sarà quello dell'oggetto stesso o della prima sottocartella nel percorso dalla cartella all'oggetto. Il chiamante dovrà aggiungere questo PIDL al PIDL completo della cartella per ottenere un PIDL completo per l'oggetto.

[**IShellFolder::P arsedisplayname**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-parsedisplayname) può essere chiamato anche per richiedere gli attributi di un oggetto. Poiché determinare tutti gli attributi applicabili può richiedere molto tempo, il chiamante imposterà solo i flag [**SFGAO \_ xxx**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-getattributesof) che rappresentano le informazioni a cui il chiamante è interessato. È necessario determinare quali di questi attributi sono veri per l'oggetto e deselezionare i flag rimanenti.

### <a name="ienumidlist-interface"></a>Interfaccia IEnumIDList

Quando in Esplora risorse è necessario enumerare gli oggetti contenuti in una cartella, viene chiamato [**IShellFolder:: EnumObjects**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-enumobjects). L'oggetto Folder deve creare un oggetto di enumerazione che espone l'interfaccia [**IEnumIDList**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ienumidlist) e restituisce il puntatore a tale interfaccia. Esplora risorse utilizzerà in genere **IEnumIDList** per enumerare il PIDL di tutti gli oggetti contenuti nella cartella.

[**IEnumIDList**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ienumidlist) è un'interfaccia di enumerazione OLE standard ed è implementata nel modo consueto. Tenere presente, tuttavia, che la PIDL restituita deve essere relativa alla cartella e contenere solo la struttura [**SHITEMID**](/windows/desktop/api/Shtypes/ns-shtypes-shitemid) dell'oggetto e un carattere di terminazione.

## <a name="implementing-the-optional-interfaces"></a>Implementazione delle interfacce facoltative

Sono disponibili diverse interfacce Shell facoltative che possono essere supportate dagli oggetti cartella dell'estensione. Molti di essi, ad esempio [**IExtractIcon**](/windows/win32/api/shlobj_core/nn-shlobj_core-iextracticona), consentono di personalizzare diversi aspetti del modo in cui l'utente Visualizza l'estensione. Altri, ad esempio [**IDataObject**](/windows/win32/api/objidl/nn-objidl-idataobject), consentono all'estensione di supportare funzionalità quali il trascinamento della selezione.

Nessuna delle interfacce facoltative è esposta direttamente da un oggetto Folder. Esplora risorse chiama invece uno dei due metodi [**IShellFolder**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellfolder) per richiedere un'interfaccia:

-   Esplora risorse chiama [**IShellFolder:: GetUIObjectOf**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-getuiobjectof) di un oggetto cartella per richiedere un'interfaccia per uno degli oggetti contenuti nella cartella.
-   Esplora risorse chiama [**IShellFolder:: CreateViewObject**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-createviewobject) di un oggetto cartella per richiedere un'interfaccia per la cartella stessa.

Per fornire le informazioni, l'oggetto Folder Crea un oggetto che espone l'interfaccia richiesta e restituisce il puntatore a interfaccia. Esplora risorse chiama quindi l'interfaccia per recuperare le informazioni necessarie. In questa sezione vengono descritte le interfacce facoltative più diffuse.

### <a name="iextracticon"></a>IExtractIcon

Esplora risorse richiede un'interfaccia [**IExtractIcon**](/windows/win32/api/shlobj_core/nn-shlobj_core-iextracticona) prima di visualizzare il contenuto di una cartella. L'interfaccia consente all'estensione di specificare icone personalizzate per gli oggetti contenuti nella cartella. In caso contrario, verranno usate le icone di file e cartelle standard. Per fornire un'icona personalizzata, creare un oggetto di estrazione icona che espone **IExtractIcon** e restituire un puntatore a tale interfaccia. Per ulteriori informazioni, vedere la documentazione di riferimento di **IExtractIcon** o [creazione di gestori di icone](./how-to-create-icon-handlers.md).

### <a name="icontextmenu"></a>IContextMenu

Quando un utente fa clic con il pulsante destro del mouse su un oggetto, Esplora risorse richiede un'interfaccia [**IContextMenu**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-icontextmenu) . Per fornire i menu di scelta rapida per gli oggetti, creare un oggetto gestore di menu e restituire l'interfaccia **IContextMenu** .

Le procedure per la creazione di un oggetto gestore di menu sono molto simili a quelle utilizzate per creare un'estensione della shell del gestore di menu. Per informazioni dettagliate, vedere [creazione di gestori di menu di scelta rapida](context-menu-handlers.md) o riferimento a [**IContextMenu**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-icontextmenu), [**IContextMenu2**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-icontextmenu2)o [**IContextMenu3**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-icontextmenu3) .

### <a name="iqueryinfo"></a>IQueryInfo

Esplora risorse chiama l'interfaccia [**IQueryInfo**](/windows/win32/api/shlobj_core/nn-shlobj_core-iqueryinfo) per recuperare una stringa di testo infotip.

### <a name="idataobject-and-idroptarget"></a>IDataObject e IDropTarget

Quando gli oggetti vengono visualizzati da Esplora risorse, un oggetto Folder non ha un modo diretto per stabilire quando un utente sta tentando di tagliare, copiare o trascinare un oggetto. In Esplora risorse viene invece richiesta un'interfaccia [**IDataObject**](/windows/win32/api/objidl/nn-objidl-idataobject) . Per consentire il trasferimento dell'oggetto, creare un oggetto dati e restituire un puntatore alla relativa interfaccia **IDataObject** .

Analogamente, un utente potrebbe tentare di eliminare un oggetto dati in una rappresentazione di Esplora risorse di uno degli oggetti, ad esempio un'icona o un percorso della barra degli indirizzi. Esplora risorse richiede quindi un'interfaccia [**IDropTarget**](/windows/win32/api/oleidl/nn-oleidl-idroptarget) . Per consentire l'eliminazione dell'oggetto dati, creare un oggetto che espone un'interfaccia **IDropTarget** e restituire il puntatore a interfaccia.

La gestione del trasferimento dei dati è uno degli aspetti più complicati della scrittura delle estensioni dello spazio dei nomi. Per una descrizione dettagliata, vedere [trasferimento di oggetti Shell con trascinamento della selezione e gli appunti](dragdrop.md).

## <a name="working-with-the-default-shell-folder-view-implementation"></a>Utilizzo dell'implementazione della visualizzazione della cartella della shell predefinita

Le origini dati che usano l'oggetto visualizzazione cartella della shell (DefView) predefinito devono implementare queste interfacce:

-   [**IShellFolder**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellfolder)
-   [**IShellFolder2**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellfolder2)
-   [**IPersistFolder**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ipersistfolder)
-   [**IPersistFolder2**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ipersistfolder2)

Facoltativamente, possono implementare anche [**IPersistFolder3**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ipersistfolder3).

 

 
