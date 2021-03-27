---
description: I formati degli Appunti della shell vengono usati per identificare il tipo di dati della shell trasferiti tramite gli Appunti.
ms.assetid: fb8ce5d3-3215-4e05-a916-4d4a803464d2
title: Formati degli Appunti della shell
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 674ccc33db3a35a1a60abb549f5e1ab5b5c96760
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103750266"
---
# <a name="shell-clipboard-formats"></a>Formati degli Appunti della shell

I formati degli Appunti della shell vengono usati per identificare il tipo di dati della shell trasferiti tramite gli Appunti. La maggior parte dei formati degli Appunti della shell identifica un tipo di dati, ad esempio un elenco di nomi di file o puntatori a elenchi di identificatori di elemento (PIDL). Tuttavia, alcuni formati vengono usati per la comunicazione tra l'origine e la destinazione. Possono accelerare il processo di trasferimento dei dati supportando operazioni della shell come lo [spostamento ottimizzato](datascenarios.md) e la [delete_on_paste](datascenarios.md). I dati della shell sono sempre contenuti in un [oggetto dati](dataobject.md) che utilizza una struttura [**FORMATETC**](/windows/win32/api/objidl/ns-objidl-formatetc) come metodo più generale per caratterizzare i dati. Il membro **cfFormat** della struttura viene impostato sul formato degli Appunti per un particolare elemento di dati. Gli altri membri forniscono informazioni aggiuntive, ad esempio il meccanismo di trasferimento dei dati. I dati sono contenuti in una struttura [**STGMEDIUM**](/windows/win32/api/objidl/ns-objidl-ustgmedium-r1) associata.

> [!Note]  
> Gli identificatori di formato degli Appunti standard hanno il formato CF_ *xxx*. Un esempio comune è CF_TEXT, che viene utilizzato per il trasferimento di dati di testo ANSI. Questi identificatori hanno valori predefiniti e possono essere usati direttamente con le strutture [**FORMATETC**](/windows/win32/api/objidl/ns-objidl-formatetc) . Ad eccezione di [CF_HDROP](#cf_hdrop), gli identificatori di formato della shell non sono predefiniti. Ad eccezione di DragWindow, hanno il formato CFSTR_ *xxx*. Per distinguere questi valori da formati predefiniti, vengono spesso definiti semplicemente *formati*. Tuttavia, a differenza dei formati predefiniti, devono essere registrati sia per l'origine che per la destinazione prima di poter essere usati per trasferire i dati. Per registrare un formato della shell, includere il file di intestazione shlobj. h e passare l'identificatore di formato CFSTR_ *xxx* a [RegisterClipboardFormat](/windows/win32/api/winuser/nf-winuser-registerclipboardformata). Questa funzione restituisce un valore di formato degli Appunti valido, che può quindi essere usato come membro **cfFormat** di una struttura **FORMATETC** .

 

I formati degli Appunti della shell sono organizzati in tre gruppi, in base al modo in cui vengono usati.

-   [Formati per il trasferimento di oggetti del file System](#formats-for-transferring-file-system-objects)
    -   [CF_HDROP](#cf_hdrop)
    -   [CFSTR_FILECONTENTS](#cfstr_filecontents)
    -   [CFSTR_FILEDESCRIPTOR](#cfstr_filedescriptor)
    -   [CFSTR_FILENAME](#cfstr_filename)
    -   [CFSTR_FILENAMEMAP](#cfstr_filenamemap)
    -   [CFSTR_MOUNTEDVOLUME](#cfstr_mountedvolume)
    -   [CFSTR_SHELLIDLIST](#cfstr_shellidlist)
    -   [CFSTR_SHELLIDLISTOFFSET](#cfstr_shellidlistoffset)
-   [Formati per il trasferimento di oggetti virtuali](#formats-for-transferring-virtual-objects)
    -   [CFSTR_NETRESOURCES](#cfstr_netresources)
    -   [CFSTR_PRINTERGROUP](#cfstr_printergroup)
    -   [CFSTR_INETURL](#cfstr_ineturl)
    -   [CFSTR_SHELLURL (deprecato)](#cfstr_shellurl-deprecated)
-   [Formati per la comunicazione tra l'origine e la destinazione](#formats-for-communication-between-source-and-target)
    -   [CFSTR_INDRAGLOOP](#cfstr_indragloop)
    -   [CFSTR_LOGICALPERFORMEDDROPEFFECT](#cfstr_logicalperformeddropeffect)
    -   [CFSTR_PASTESUCCEEDED](#cfstr_pastesucceeded)
    -   [CFSTR_PERFORMEDDROPEFFECT](#cfstr_performeddropeffect)
    -   [CFSTR_PREFERREDDROPEFFECT](#cfstr_preferreddropeffect)
    -   [CFSTR_TARGETCLSID](#cfstr_targetclsid)
    -   [CFSTR_UNTRUSTEDDRAGDROP](#cfstr_untrusteddragdrop)
    -   [DragWindow](#dragwindow)

## <a name="formats-for-transferring-file-system-objects"></a>Formati per il trasferimento di oggetti del file System

Questi formati vengono usati per trasferire uno o più file o altri oggetti della shell.

-   [CF_HDROP](#cf_hdrop)
-   [CFSTR_FILECONTENTS](#cfstr_filecontents)
-   [CFSTR_FILEDESCRIPTOR](#cfstr_filedescriptor)
-   [CFSTR_FILENAME](#cfstr_filename)
-   [CFSTR_FILENAMEMAP](#cfstr_filenamemap)
-   [CFSTR_MOUNTEDVOLUME](#cfstr_mountedvolume)
-   [CFSTR_SHELLIDLIST](#cfstr_shellidlist)
-   [CFSTR_SHELLIDLISTOFFSET](#cfstr_shellidlistoffset)

### <a name="cf_hdrop"></a>CF_HDROP

Questo formato degli Appunti viene usato quando si trasferiscono i percorsi di un gruppo di file esistenti. Diversamente dagli altri formati della shell, è predefinito, pertanto non è necessario chiamare [RegisterClipboardFormat](/windows/win32/api/winuser/nf-winuser-registerclipboardformata). I dati sono costituiti da una struttura [**STGMEDIUM**](/windows/win32/api/objidl/ns-objidl-ustgmedium-r1) che contiene un oggetto memoria globale. Il membro **hGlobal** della struttura punta a una struttura [**DropFiles**](/windows/desktop/api/shlobj_core/ns-shlobj_core-dropfiles) come membro **hGlobal** .

Il membro **Pfile** della struttura [**DropFiles**](/windows/desktop/api/shlobj_core/ns-shlobj_core-dropfiles) contiene un offset a una matrice di caratteri con terminazione **null** che contiene i nomi file. Se si estrae un formato CF_HDROP da un oggetto dati, è possibile utilizzare [**DragQueryFile**](/windows/desktop/api/Shellapi/nf-shellapi-dragqueryfilea) per estrarre i singoli nomi di file dall'oggetto memoria globale. Se si sta creando un CF_HDROP formato da inserire in un oggetto dati, è necessario costruire la matrice di nomi di file.

La matrice di nomi di file è costituita da una serie di stringhe, ognuna delle quali contiene un percorso completo di un file, incluso il carattere di terminazione **null** . Un carattere **null** aggiuntivo viene aggiunto alla stringa finale per terminare la matrice. Ad esempio, se i file c: \\temp1.txt e c: \\temp2.txt vengono trasferiti, la matrice di caratteri è simile alla seguente:


```CMD
c:\temp1.txt'\0'c:\temp2.txt'\0''\0'
```

> [!Note]  
> In questo esempio,' \\ 0' viene usato per rappresentare il carattere **null** , non i caratteri letterali che devono essere inclusi.


Se l'oggetto è stato copiato negli Appunti come parte di un'operazione di trascinamento della selezione, il membro **PT** della struttura [**DropFiles**](/windows/desktop/api/shlobj_core/ns-shlobj_core-dropfiles) contiene le coordinate del punto in cui l'oggetto è stato eliminato. È possibile utilizzare [**DragQueryPoint**](/windows/desktop/api/Shellapi/nf-shellapi-dragquerypoint) per estrarre le coordinate del cursore.

Se questo formato è presente in un oggetto dati, un ciclo di trascinamento OLE simula [**WM_DROPFILES**](wm-dropfiles.md) funzionalità con destinazioni di rilascio non OLE. Questo è importante se l'applicazione è l'origine di un'operazione di trascinamento della selezione in un sistema Windows 3,1.

### <a name="cfstr_filecontents"></a>CFSTR_FILECONTENTS

Questo identificatore di formato viene usato con il formato [CFSTR_FILEDESCRIPTOR](#cfstr_filedescriptor) per trasferire i dati come se si trattasse di un file, indipendentemente dal modo in cui viene archiviato. I dati sono costituiti da una struttura [**STGMEDIUM**](/windows/win32/api/objidl/ns-objidl-ustgmedium-r1) che rappresenta il contenuto di un file. Il file viene in genere rappresentato come oggetto flusso, evitando di dover inserire il contenuto del file in memoria. In tal caso, il membro **TYMED** della struttura **STGMEDIUM** è impostato su TYMED_ISTREAM e il file è rappresentato da un'interfaccia [**IStream**](/windows/win32/api/objidl/nn-objidl-istream) . Il file può essere anche un oggetto di archiviazione o memoria globale (TYMED_ISTORAGE o TYMED_HGLOBAL). Il formato di CFSTR_FILEDESCRIPTOR associato contiene una struttura [**FileDescriptor**](/windows/win32/api/shlobj_core/ns-shlobj_core-filedescriptora) per ogni file che specifica il nome e gli attributi del file.

La destinazione gestisce i dati associati a un formato CFSTR_FILECONTENTS come se fosse un file. Quando la destinazione chiama [**IDataObject:: GetData**](/windows/win32/api/objidl/nf-objidl-idataobject-getdata) per estrarre i dati, specifica un determinato file impostando il membro **lIndex** della struttura [**FORMATETC**](/windows/win32/api/objidl/ns-objidl-formatetc) sull'indice in base zero della struttura [**filedescriptor**](/windows/win32/api/shlobj_core/ns-shlobj_core-filedescriptora) del file nel formato di [CFSTR_FILEDESCRIPTOR](#cfstr_filedescriptor) associato. La destinazione USA quindi il puntatore di interfaccia restituito o l'handle di memoria globale per estrarre i dati.

### <a name="cfstr_filedescriptor"></a>CFSTR_FILEDESCRIPTOR

Questo identificatore di formato viene usato con il formato [CFSTR_FILECONTENTS](#cfstr_filecontents) per trasferire i dati come un gruppo di file. Questi due formati rappresentano il modo migliore per trasferire gli oggetti Shell che non sono archiviati come file di file System. Questi formati, ad esempio, possono essere usati per trasferire un gruppo di messaggi di posta elettronica come singoli file, anche se ogni messaggio di posta elettronica viene effettivamente archiviato come blocco di dati in un database. I dati sono costituiti da una struttura [**STGMEDIUM**](/windows/win32/api/objidl/ns-objidl-ustgmedium-r1) che contiene un oggetto memoria globale. Il membro **hGlobal** della struttura punta a una struttura [**FILEGROUPDESCRIPTOR**](/windows/win32/api/shlobj_core/ns-shlobj_core-filegroupdescriptora) seguita da una matrice contenente una struttura [**FileDescriptor**](/windows/win32/api/shlobj_core/ns-shlobj_core-filedescriptora) per ogni file nel gruppo. Per ogni struttura **FileDescriptor** , esiste un formato di CFSTR_FILECONTENTS separato che contiene il contenuto del file. Per identificare il formato di CFSTR_FILECONTENTS di un determinato file, impostare il valore **lIndex** della struttura [**FORMATETC**](/windows/win32/api/objidl/ns-objidl-formatetc) sull'indice in base zero della struttura **FileDescriptor** del file.

Il formato CFSTR_FILEDESCRIPTOR viene comunemente usato per trasferire i dati come se fosse un gruppo di file, indipendentemente dal modo in cui sono archiviati. Dal punto di vista della destinazione, ogni formato di CFSTR_FILECONTENTS rappresenta un singolo file e viene trattato di conseguenza. Tuttavia, l'origine può archiviare i dati nel modo scelto. Anche se un formato di CSFTR_FILECONTENTS può corrispondere a un singolo file, potrebbe, ad esempio, rappresentare i dati estratti dall'origine da un database o da un documento di testo.

### <a name="cfstr_filename"></a>CFSTR_FILENAME

Questo identificatore di formato viene usato per trasferire un singolo file. I dati sono costituiti da una struttura [**STGMEDIUM**](/windows/win32/api/objidl/ns-objidl-ustgmedium-r1) che contiene un oggetto memoria globale. Il membro **hGlobal** della struttura punta a una singola stringa con terminazione **null** contenente il percorso completo del file. Questo formato è stato sostituito da [CF_HDROP](#cf_hdrop), ma è supportato per la compatibilità con le versioni precedenti di Windows 3,1.

### <a name="cfstr_filenamemap"></a>CFSTR_FILENAMEMAP

Questo identificatore di formato viene usato quando un gruppo di file in formato [CF_HDROP](#cf_hdrop) viene rinominato e trasferito. I dati sono costituiti da una struttura [**STGMEDIUM**](/windows/win32/api/objidl/ns-objidl-ustgmedium-r1) che contiene un oggetto memoria globale. Il membro **hGlobal** della struttura punta a una matrice di caratteri con terminazione **null** doppia. Questa matrice contiene un nuovo nome per ogni file, nello stesso ordine in cui i file sono elencati nel formato di CF_HDROP associato. Il formato della matrice di caratteri è identico a quello usato da CF_HDROP per elencare i file trasferiti.

### <a name="cfstr_mountedvolume"></a>CFSTR_MOUNTEDVOLUME

Questo identificatore di formato viene usato per trasferire un percorso in un volume montato. È simile a [CF_HDROP](#cf_hdrop), ma contiene solo un singolo percorso e può gestire le stringhe di percorso più lunghe che potrebbero essere necessarie per rappresentare un percorso quando il volume è montato in una cartella. I dati sono costituiti da una struttura [**STGMEDIUM**](/windows/win32/api/objidl/ns-objidl-ustgmedium-r1) che contiene un oggetto memoria globale. Il membro **hGlobal** della struttura punta a una singola stringa con terminazione **null** che contiene il percorso completo del file. La stringa di percorso deve terminare con un \\ carattere '', seguito dal carattere **null** di terminazione.

Prima di Windows 2000, i volumi potevano essere montati solo su lettere di unità. Per i sistemi Windows 2000 e versioni successive con un'unità formattata NTFS, è anche possibile montare volumi in cartelle vuote. Questa funzionalità consente di montare un volume senza occupare una lettera di unità. Il volume montato può usare qualsiasi formato attualmente supportato, tra cui FAT, FAT32, NTFS e CDFS.

È possibile aggiungere pagine a una finestra delle proprietà delle proprietà dell'unità implementando un [gestore della finestra delle proprietà](propsheet-handlers.md). Se il volume è montato su una lettera di unità, la shell passa informazioni sul percorso al gestore con il formato [CF_HDROP](#cf_hdrop) . Con i sistemi Windows 2000 e versioni successive, il formato CF_HDROP viene usato quando un volume viene montato su una lettera di unità, come nei sistemi precedenti. Tuttavia, se un volume viene montato in una cartella, viene utilizzato l'identificatore di formato [CFSTR_MOUNTEDVOLUME](#cfstr_mountedvolume) anziché CF_HDROP.

Se per il montaggio dei volumi verranno utilizzate solo le lettere di unità, verranno utilizzati solo [CF_HDROP](#cf_hdrop) e i gestori della finestra delle proprietà esistenti funzioneranno come nei sistemi precedenti. Tuttavia, se si desidera che il gestore visualizzi una pagina per i volumi montati sulle cartelle e le lettere di unità, il gestore deve essere in grado di comprendere sia i formati di CSFTR_MOUNTEDVOLUME che di CF_HDROP.

### <a name="cfstr_shellidlist"></a>CFSTR_SHELLIDLIST

Questo identificatore di formato viene utilizzato quando si trasferiscono i percorsi di uno o più oggetti spazio dei nomi esistenti. Viene usato nello stesso modo in cui [CF_HDROP](#cf_hdrop), ma contiene pidl anziché file System percorsi. L'uso di PIDL consente al formato CFSTR_SHELLIDLIST di gestire gli oggetti virtuali e file system oggetti. I dati sono una struttura [**STGMEDIUM**](/windows/win32/api/objidl/ns-objidl-ustgmedium-r1) che contiene un oggetto memoria globale. Il membro **hGlobal** della struttura punta a una struttura [**CIDA**](/windows/win32/api/shlobj_core/ns-shlobj_core-cida) .

Il membro **aoffset** della struttura [**CIDA**](/windows/win32/api/shlobj_core/ns-shlobj_core-cida) è una matrice contenente offset all'inizio della struttura [**ItemId**](/windows/desktop/api/Shtypes/ns-shtypes-itemidlist) per ogni PIDL da trasferire. Per estrarre un PIDL specifico, determinare innanzitutto il relativo indice. Aggiungere quindi il valore **aoffset** che corrisponde a tale indice all'indirizzo della struttura **CIDA** .

Il primo elemento di **aoffset** contiene un offset per l'PIDL completo di una cartella padre. Se questo PIDL è vuoto, la cartella padre è il desktop. Ognuno degli elementi rimanenti della matrice contiene un offset a uno dei PIDL da trasferire. Tutti questi PIDL sono relativi al PIDL della cartella padre.

È possibile utilizzare le due macro seguenti per recuperare PIDL da una struttura [**CIDA**](/windows/win32/api/shlobj_core/ns-shlobj_core-cida) . Il primo accetta un puntatore alla struttura e recupera il PIDL della cartella padre. Il secondo accetta un puntatore alla struttura e recupera uno degli altri PIDL, identificato dall'indice in base zero.


```C++
#define GetPIDLFolder(pida) (LPCITEMIDLIST)(((LPBYTE)pida)+(pida)->aoffset[0])

#define GetPIDLItem(pida, i) (LPCITEMIDLIST)(((LPBYTE)pida)+(pida)->aoffset[i+1])
```

> [!Note]  
> Il valore restituito da queste macro è un puntatore alla struttura [**ItemId**](/windows/desktop/api/Shtypes/ns-shtypes-itemidlist) dell'elemento PIDL. Poiché queste strutture variano di lunghezza, è necessario determinare la fine della struttura scorrendo ognuna delle strutture [**SHITEMID**](/windows/desktop/api/Shtypes/ns-shtypes-shitemid) della struttura **ItemId** , fino a raggiungere il **valore null** a due byte che contrassegna la fine.

### <a name="cfstr_shellidlistoffset"></a>CFSTR_SHELLIDLISTOFFSET

Questo identificatore di formato viene usato con formati quali [CF_HDROP](#cf_hdrop), [CFSTR_SHELLIDLIST](#cfstr_shellidlist)e [CFSTR_FILECONTENTS](#cfstr_filecontents) per specificare la posizione di un gruppo di oggetti che seguono un trasferimento. I dati sono costituiti da una struttura [**STGMEDIUM**](/windows/win32/api/objidl/ns-objidl-ustgmedium-r1) che contiene un oggetto memoria globale. Il membro **hGlobal** della struttura punta a una matrice di strutture [**Point**](/previous-versions//dd162805(v=vs.85)) . La prima struttura specifica le coordinate dello schermo, in pixel, dell'angolo superiore sinistro del rettangolo che racchiude il gruppo. Il resto delle strutture specifica le posizioni dei singoli oggetti rispetto alla posizione del gruppo. Devono essere nello stesso ordine usato per elencare gli oggetti nel formato associato.

## <a name="formats-for-transferring-virtual-objects"></a>Formati per il trasferimento di oggetti virtuali

È possibile utilizzare il formato CFSTR_SHELLIDLIST per trasferire sia file system che oggetti virtuali. Tuttavia, esistono anche diversi formati specializzati per il trasferimento di particolari tipi di oggetti virtuali.

-   [CFSTR_NETRESOURCES](#cfstr_netresources)
-   [CFSTR_PRINTERGROUP](#cfstr_printergroup)
-   [CFSTR_INETURL](#cfstr_ineturl)
-   [CFSTR_SHELLURL (deprecato)](#cfstr_shellurl-deprecated)

### <a name="cfstr_netresources"></a>CFSTR_NETRESOURCES

Questo identificatore di formato viene utilizzato per il trasferimento di risorse di rete, ad esempio un dominio o un server. I dati sono una struttura [**STGMEDIUM**](/windows/win32/api/objidl/ns-objidl-ustgmedium-r1) che contiene un oggetto memoria globale. Il membro **hGlobal** della struttura punta a una struttura [**NRESARRAY**](/windows/desktop/api/shlobj_core/ns-shlobj_core-nresarray) . Il membro **Nr** della struttura indica una struttura [**netresource**](/windows/win32/api/rrascfg/nn-rrascfg-ieapproviderconfig) il cui membro **lpRemoteName** contiene una stringa con terminazione **null** che identifica la risorsa di rete. L'obiettivo di rilascio può quindi usare i dati con qualsiasi funzione API di rete [(WNet) di Windows](../wnet/windows-networking-wnet-.md) , ad esempio [**WNetAddConnection**](/windows/win32/api/winnetwk/nf-winnetwk-wnetaddconnectiona), per eseguire operazioni di rete sull'oggetto.

### <a name="cfstr_printergroup"></a>CFSTR_PRINTERGROUP

Questo identificatore di formato viene utilizzato quando si trasferiscono i nomi descrittivi delle stampanti. I dati sono una struttura [**STGMEDIUM**](/windows/win32/api/objidl/ns-objidl-ustgmedium-r1) che contiene un oggetto memoria globale. Il membro **hGlobal** della struttura punta a una stringa con lo stesso formato usato con [CF_HDROP](#cf_hdrop). Tuttavia, il membro **Pfile** della struttura [**DropFiles**](/windows/desktop/api/shlobj_core/ns-shlobj_core-dropfiles) contiene uno o più nomi descrittivi delle stampanti anziché i percorsi di file.

### <a name="cfstr_ineturl"></a>CFSTR_INETURL

Questo identificatore di formato sostituisce [CFSTR_SHELLURL (deprecato)](#cfstr_shellurl-deprecated). Se si vuole che l'applicazione modifichi gli URL degli Appunti, usare CFSTR_INETURL anziché CFSTR_SHELLURL (deprecato). Questo formato offre la migliore rappresentazione degli Appunti di un singolo URL. Se UNICODE non è definito, l'applicazione recupera la versione CF_TEXT/CFSTR_SHELLURL dell'URL. Se è definito UNICODE, l'applicazione recupera la versione CF_UNICODE dell'URL.

### <a name="cfstr_shellurl-deprecated"></a>CFSTR_SHELLURL (deprecato)

> [!Note]  
> Questo identificatore di formato è stato deprecato. in alternativa, usare CFSTR_INETURL.

 

## <a name="formats-for-communication-between-source-and-target"></a>Formati per la comunicazione tra l'origine e la destinazione

Questi identificatori di formato consentono la comunicazione tra l'origine e la destinazione. I formati accompagnano i dati e offrono alle applicazioni un maggiore livello di controllo sulle operazioni di spostamento-copia-incolla o di trascinamento della selezione che coinvolgono oggetti della shell.

-   [CFSTR_INDRAGLOOP](#cfstr_indragloop)
-   [CFSTR_LOGICALPERFORMEDDROPEFFECT](#cfstr_logicalperformeddropeffect)
-   [CFSTR_PASTESUCCEEDED](#cfstr_pastesucceeded)
-   [CFSTR_PERFORMEDDROPEFFECT](#cfstr_performeddropeffect)
-   [CFSTR_PREFERREDDROPEFFECT](#cfstr_preferreddropeffect)
-   [CFSTR_TARGETCLSID](#cfstr_targetclsid)
-   [CFSTR_UNTRUSTEDDRAGDROP](#cfstr_untrusteddragdrop)
-   [DragWindow](#dragwindow)

### <a name="cfstr_indragloop"></a>CFSTR_INDRAGLOOP

Questo identificatore di formato viene usato da un oggetto dati per indicare se si trova in un ciclo di trascinamento della selezione. I dati sono una struttura [**STGMEDIUM**](/windows/win32/api/objidl/ns-objidl-ustgmedium-r1) che contiene un oggetto memoria globale. Il membro **hGlobal** della struttura punta a un valore **DWORD** . Se il valore **DWORD** è diverso da zero, l'oggetto dati si trova all'interno di un ciclo di trascinamento della selezione. Se il valore è impostato su zero, l'oggetto dati non si trova all'interno di un ciclo di trascinamento della selezione.

Alcune destinazioni di rilascio potrebbero chiamare [**IDataObject:: GetData**](/windows/win32/api/objidl/nf-objidl-idataobject-getdata) e tentare di estrarre i dati mentre l'oggetto si trova ancora nel ciclo di trascinamento della selezione. Il rendering completo dell'oggetto per ogni occorrenza può causare lo stallo del cursore di trascinamento. Se l'oggetto dati supporta [CFSTR_INDRAGLOOP](#cfstr_indragloop), la destinazione può invece utilizzare tale formato per verificare lo stato del ciclo di trascinamento della selezione ed evitare il rendering intensivo della memoria dell'oggetto fino a quando non viene effettivamente eliminato. I formati con utilizzo intensivo di memoria per il rendering devono comunque essere inclusi nell'enumeratore [**FORMATETC**](/windows/win32/api/objidl/ns-objidl-formatetc) e nelle chiamate a [**IDataObject:: QueryGetData**](/windows/win32/api/objidl/nf-objidl-idataobject-querygetdata). Se l'oggetto dati non imposta CFSTR_INDRAGLOOP, deve fungere da se il valore è impostato su zero.

### <a name="cfstr_logicalperformeddropeffect"></a>CFSTR_LOGICALPERFORMEDDROPEFFECT

[Versione 5,0.](versions.md) Questo identificatore di formato consente a un'origine di rilascio di chiamare il metodo [**IDataObject:: GetData**](/windows/win32/api/objidl/nf-objidl-idataobject-getdata) dell'oggetto dati per determinare il risultato di un trasferimento dei dati della shell. I dati sono una struttura [**STGMEDIUM**](/windows/win32/api/objidl/ns-objidl-ustgmedium-r1) che contiene un oggetto memoria globale. Il membro **hGlobal** della struttura punta a un valore DWORD contenente un valore [**DropEffect**](../com/dropeffect-constants.md) .

L'identificatore di formato [CFSTR_PERFORMEDDROPEFFECT](#cfstr_performeddropeffect) è stato progettato per consentire alla destinazione di indicare all'oggetto dati l'operazione effettivamente eseguita. Tuttavia, la Shell utilizza gli [spostamenti ottimizzati](datascenarios.md) per gli oggetti di file System quando possibile. In tal caso, la shell imposta in genere il valore CFSTR_PERFORMEDDROPEFFECT su DROPEFFECT_NONE, per indicare all'oggetto dati che i dati originali sono stati eliminati. Pertanto, l'origine non può utilizzare il valore CFSTR_PERFORMEDDROPEFFECT per determinare quale operazione è stata eseguita. Sebbene la maggior parte delle origini non necessiti di queste informazioni, esistono alcune eccezioni. Ad esempio, anche se lo spostamento ottimizzato Elimina la necessità che un'origine elimini tutti i dati, è possibile che l'origine debba comunque aggiornare un database correlato per indicare che i file sono stati spostati o copiati.

Se un'origine deve stabilire quale operazione ha avuto luogo, può chiamare il metodo [**IDataObject:: GetData**](/windows/win32/api/objidl/nf-objidl-idataobject-getdata) dell'oggetto dati e richiedere il formato CFSTR_LOGICALPERFORMEDDROPEFFECT. Questo formato riflette essenzialmente ciò che accade dal punto di vista dell'utente dopo che l'operazione è stata completata. Se viene creato un nuovo file e viene eliminato il file originale, l'utente visualizza un'operazione di spostamento e il valore dei dati del formato è impostato su DROPEFFECT_MOVE. Se il file originale è ancora presente, l'utente visualizza un'operazione di copia e il valore dei dati del formato è impostato su DROPEFFECT_COPY. Se è stato creato un collegamento, il valore dei dati del formato verrà DROPEFFECT_LINK.

### <a name="cfstr_pastesucceeded"></a>CFSTR_PASTESUCCEEDED

Questo identificatore di formato viene usato dalla destinazione per informare l'oggetto dati, tramite il metodo [**IDataObject:: SetData**](/windows/win32/api/objidl/nf-objidl-idataobject-setdata) , che un'operazione Delete-on-paste ha avuto esito positivo. I dati sono una struttura [**STGMEDIUM**](/windows/win32/api/objidl/ns-objidl-ustgmedium-r1) che contiene un oggetto memoria globale. Il membro **hGlobal** della struttura punta a un valore **DWORD** contenente un valore [**DropEffect**](../com/dropeffect-constants.md) . Questo formato viene utilizzato per notificare all'oggetto dati che deve completare l'operazione di taglio ed eliminare i dati originali, se necessario. Per altre informazioni, vedere [operazioni delete-on-paste](datascenarios.md).

### <a name="cfstr_performeddropeffect"></a>CFSTR_PERFORMEDDROPEFFECT

Questo identificatore di formato viene usato dalla destinazione per informare l'oggetto dati tramite il metodo [**IDataObject:: SetData**](/windows/win32/api/objidl/nf-objidl-idataobject-setdata) del risultato di un trasferimento dei dati. I dati sono una struttura [**STGMEDIUM**](/windows/win32/api/objidl/ns-objidl-ustgmedium-r1) che contiene un oggetto memoria globale. Il membro **hGlobal** della struttura punta a un valore **DWORD** impostato sul valore [**DROPEFFECT**](../com/dropeffect-constants.md) appropriato, in genere DROPEFFECT_MOVE o DROPEFFECT_COPY.

Questo formato viene in genere usato quando il risultato di un'operazione può essere uno spostamento o una copia, ad esempio in un'operazione di spostamento o eliminazione su Incolla [ottimizzata](datascenarios.md) . Fornisce un modo affidabile per la destinazione per indicare all'oggetto dati cosa si è effettivamente verificato. È stata introdotta perché il valore di *pdwEffect* restituito da [**DoDragDrop**](/windows/win32/api/ole2/nf-ole2-dodragdrop) non indica in modo affidabile quale operazione è avvenuta. Il formato [CFSTR_PERFORMEDDROPEFFECT](#cfstr_performeddropeffect) è il modo affidabile per indicare che si è verificato uno spostamento non ottimizzato.

### <a name="cfstr_preferreddropeffect"></a>CFSTR_PREFERREDDROPEFFECT

Questo identificatore di formato viene usato dall'origine per specificare se il metodo preferito per il trasferimento dei dati è lo spostamento o la copia. Un obiettivo di rilascio richiede questo formato chiamando il metodo [**IDataObject:: GetData**](/windows/win32/api/objidl/nf-objidl-idataobject-getdata) dell'oggetto dati. I dati sono una struttura [**STGMEDIUM**](/windows/win32/api/objidl/ns-objidl-ustgmedium-r1) che contiene un oggetto memoria globale. Il membro **hGlobal** della struttura punta a un valore **DWORD** . Questo valore è impostato su DROPEFFECT_MOVE se un'operazione di spostamento è preferibile o DROPEFFECT_COPY se è preferibile un'operazione di copia.

Questa funzionalità viene utilizzata quando un'origine può supportare un'operazione di spostamento o copia. Usa il formato [CFSTR_PREFERREDDROPEFFECT](#cfstr_preferreddropeffect) per comunicare la propria preferenza alla destinazione. Poiché la destinazione non è obbligata a rispettare la richiesta, la destinazione deve chiamare il metodo [**IDataObject:: SetData**](/windows/win32/api/objidl/nf-objidl-idataobject-setdata) dell'origine con un formato [CFSTR_PERFORMEDDROPEFFECT](#cfstr_performeddropeffect) per indicare all'oggetto dati l'operazione effettivamente eseguita.

Con un'operazione [Delete-on-paste](datascenarios.md) , il formato CFSTR_PREFERREDDROPFORMAT viene usato per indicare alla destinazione se l'origine ha fatto un taglio o una copia. Con un'operazione di trascinamento della selezione, è possibile usare CFSTR_PREFERREDDROPFORMAT per specificare l'azione della shell. Se questo formato non è presente, la shell esegue un'azione predefinita, in base al contesto. Ad esempio, se un utente trascina un file da un volume e lo rilascia in un altro volume, l'azione predefinita della Shell consiste nel copiare il file. Includendo un formato CFSTR_PREFERREDDROPFORMAT nell'oggetto dati, è possibile eseguire l'override dell'azione predefinita e indicare in modo esplicito alla shell di copiare, spostare o collegare il file. Se l'utente sceglie di trascinare con il pulsante destro, CFSTR_PREFERREDDROPFORMAT specifica il comando predefinito nel menu di scelta rapida del [trascinamento della selezione](context-menu-handlers.md) . L'utente è ancora libero di scegliere altri comandi nel menu.

Prima di Microsoft Internet Explorer 4,0, un'applicazione indicava che era in corso il trasferimento dei tipi di file di collegamento impostando FD_LINKUI nel membro **dwFlags** della struttura [**FileDescriptor**](/windows/win32/api/shlobj_core/ns-shlobj_core-filedescriptora) . Le destinazioni hanno quindi dovuto usare una chiamata potenzialmente dispendiosa in termini di tempo a [**IDataObject:: GetData**](/windows/win32/api/objidl/nf-objidl-idataobject-getdata) per verificare se è stato impostato il flag di FD_LINKUI. A questo punto, il modo migliore per indicare che i collegamenti vengono trasferiti consiste nell'usare il formato CFSTR_PREFERREDDROPEFFECT impostato su DROPEFFECT_LINK. Per la compatibilità con le versioni precedenti, tuttavia, le origini devono comunque impostare il flag di FD_LINKUI.

### <a name="cfstr_targetclsid"></a>CFSTR_TARGETCLSID

Questo identificatore di formato viene utilizzato da una destinazione per fornire il relativo CLSID all'origine. I dati sono una struttura [**STGMEDIUM**](/windows/win32/api/objidl/ns-objidl-ustgmedium-r1) che contiene un oggetto memoria globale. Il membro **hGlobal** della struttura punta al GUID CLSID dell'obiettivo di rilascio.

Questo formato viene usato principalmente per consentire l'eliminazione degli oggetti trascinandoli nel Cestino. Quando un oggetto viene eliminato nel Cestino, viene chiamato il metodo [**IDataObject:: SetData**](/windows/win32/api/objidl/nf-objidl-idataobject-setdata) dell'origine con un formato di CFSTR_TARGETCLSID impostato sul CLSID del cestino (CLSID_RecycleBin). L'origine può quindi eliminare l'oggetto originale.

### <a name="cfstr_untrusteddragdrop"></a>CFSTR_UNTRUSTEDDRAGDROP

Questo identificatore di formato viene utilizzato da Windows Internet Explorer e dalla shell di Windows per fornire un meccanismo tramite il quale bloccare o richiedere operazioni di trascinamento della selezione provenienti da Internet Explorer insieme al flag di [**URLACTION_SHELL_ENHANCED_DRAGDROP_SECURITY**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms537178(v=vs.85)) .

**CFSTR_UNTRUSTEDDRAGDROP** viene aggiunto dall'origine di un'operazione di trascinamento della selezione per specificare che l'oggetto dati potrebbe contenere dati non attendibili. I dati sono rappresentati da una struttura [**STGMEDIUM**](/windows/win32/api/objidl/ns-objidl-ustgmedium-r1) che contiene un oggetto memoria globale. Il membro **hGlobal** della struttura punta a un **valore DWORD** impostato su un flag di [**azione URL**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms537178(v=vs.85)) appropriato per fare in modo che un criterio controlli tramite il metodo [**IInternetSecurityManager::P rocessurlaction**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms537136(v=vs.85)) , usando il flag di [**PUAF_ENFORCERESTRICTED**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms537171(v=vs.85)) .

### <a name="dragwindow"></a>DragWindow

Questo formato viene usato in un'operazione di trascinamento della selezione per identificare l'immagine di trascinamento di un oggetto (finestra), in modo che le informazioni visive possano essere aggiornate dinamicamente. Quando un oggetto viene trascinato su un obiettivo di rilascio, un'applicazione aggiorna la struttura [**DROPDESCRIPTION**](/windows/desktop/api/shlobj_core/ns-shlobj_core-dropdescription) in risposta al metodo [**IDropTarget::D ragover**](/windows/win32/api/oleidl/nf-oleidl-idroptarget-dragover) o [**IDropSource:: GiveFeedback**](/windows/win32/api/oleidl/nf-oleidl-idropsource-givefeedback) . **DROPDESCRIPTION** viene aggiornato con un nuovo valore [**DROPIMAGETYPE**](/windows/desktop/api/shlobj_core/ne-shlobj_core-dropimagetype) che indica la decorazione da applicare all'oggetto visivo della finestra di trascinamento. ad esempio, un'indicazione che indica che il file viene copiato anziché spostato o che l'oggetto non può essere eliminato in tale posizione. Tuttavia, finché l'oggetto non riceve un messaggio di [**DDWM_UPDATEWINDOW**](ddwm-updatewindow.md) , gli oggetti visivi non vengono aggiornati. Questo formato fornisce l' **HWND** della finestra di trascinamento del destinatario al mittente del messaggio di **DDWM_UPDATEWINDOW** .

I dati degli Appunti sono di tipo [**TYMED_HGLOBAL**](/windows/win32/api/objidl/ne-objidl-tymed). Si tratta di una rappresentazione **DWORD** di un **HWND**. I dati possono essere passati alla funzione **ULongToHandle** , definita in Basetsd. h, per fornire un **HWND** a 64 bit da usare in Windows a 64 bit.

Questo formato non richiede l'inclusione di Shlobj. h.

 

 
