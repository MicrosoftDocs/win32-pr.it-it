---
description: I formati degli Appunti della shell vengono usati per identificare il tipo di dati della shell trasferiti tramite gli Appunti.
ms.assetid: fb8ce5d3-3215-4e05-a916-4d4a803464d2
title: Formati degli Appunti della shell
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9fccd73f5b364c247454d874f5b9bb7586e3187150ebce28620cc6dc01f8298d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119351391"
---
# <a name="shell-clipboard-formats"></a>Formati degli Appunti della shell

I formati degli Appunti della shell vengono usati per identificare il tipo di dati della shell trasferiti tramite gli Appunti. La maggior parte dei formati degli Appunti della shell identifica un tipo di dati, ad esempio un elenco di nomi di file o puntatori a elenchi di identificatori di elemento (PID). Tuttavia, alcuni formati vengono usati per la comunicazione tra origine e destinazione. Possono accelerare il processo di trasferimento dei [](datascenarios.md) dati supportando le operazioni della shell, ad esempio lo spostamento ottimizzato [e delete_on_paste](datascenarios.md). I dati della shell sono sempre contenuti in un oggetto [dati](dataobject.md) che usa [**una struttura FORMATETC**](/windows/win32/api/objidl/ns-objidl-formatetc) come modo più generale per caratterizzare i dati. Il membro **cfFormat della** struttura è impostato sul formato degli Appunti per l'elemento specifico dei dati. Gli altri membri forniscono informazioni aggiuntive, ad esempio il meccanismo di trasferimento dei dati. I dati sono contenuti in una struttura [**STGMEDIUM**](/windows/win32/api/objidl/ns-objidl-ustgmedium-r1) di associazione.

> [!Note]  
> Gli identificatori di formato degli Appunti standard hanno il formato CF_ *XXX*. Un esempio comune è CF_TEXT, che viene usato per il trasferimento di dati di testo ANSI. Questi identificatori hanno valori predefiniti e possono essere usati direttamente con [**strutture FORMATETC.**](/windows/win32/api/objidl/ns-objidl-formatetc) Ad eccezione di [CF_HDROP](#cf_hdrop), gli identificatori di formato della shell non sono predefiniti. Ad eccezione di DragWindow, hanno il formato CFSTR_ *XXX*. Per differenziare questi valori dai formati predefiniti, vengono spesso definiti semplicemente *formati*. Tuttavia, a differenza dei formati predefiniti, devono essere registrati sia dall'origine che dalla destinazione prima di poter essere usati per trasferire i dati. Per registrare un formato shell, includere il file di intestazione Shlobj.h e passare l'identificatore CFSTR_ *formato XXX* a [RegisterClipboardFormat.](/windows/win32/api/winuser/nf-winuser-registerclipboardformata) Questa funzione restituisce un valore di formato degli Appunti valido, che può quindi essere usato come membro **cfFormat** di una **struttura FORMATETC.**

 

I formati degli Appunti della shell sono organizzati in tre gruppi, in base al modo in cui vengono usati.

-   [Formati per il trasferimento di oggetti del file system](#formats-for-transferring-file-system-objects)
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
-   [Formati per la comunicazione tra origine e destinazione](#formats-for-communication-between-source-and-target)
    -   [CFSTR_INDRAGLOOP](#cfstr_indragloop)
    -   [CFSTR_LOGICALPERFORMEDDROPEFFECT](#cfstr_logicalperformeddropeffect)
    -   [CFSTR_PASTESUCCEEDED](#cfstr_pastesucceeded)
    -   [CFSTR_PERFORMEDDROPEFFECT](#cfstr_performeddropeffect)
    -   [CFSTR_PREFERREDDROPEFFECT](#cfstr_preferreddropeffect)
    -   [CFSTR_TARGETCLSID](#cfstr_targetclsid)
    -   [CFSTR_UNTRUSTEDDRAGDROP](#cfstr_untrusteddragdrop)
    -   [Finestra di trascinamento](#dragwindow)

## <a name="formats-for-transferring-file-system-objects"></a>Formati per il trasferimento di oggetti del file system

Questi formati vengono usati per trasferire uno o più file o altri oggetti shell.

-   [CF_HDROP](#cf_hdrop)
-   [CFSTR_FILECONTENTS](#cfstr_filecontents)
-   [CFSTR_FILEDESCRIPTOR](#cfstr_filedescriptor)
-   [CFSTR_FILENAME](#cfstr_filename)
-   [CFSTR_FILENAMEMAP](#cfstr_filenamemap)
-   [CFSTR_MOUNTEDVOLUME](#cfstr_mountedvolume)
-   [CFSTR_SHELLIDLIST](#cfstr_shellidlist)
-   [CFSTR_SHELLIDLISTOFFSET](#cfstr_shellidlistoffset)

### <a name="cf_hdrop"></a>CF_HDROP

Questo formato degli Appunti viene usato durante il trasferimento dei percorsi di un gruppo di file esistenti. A differenza degli altri formati shell, è predefinito, quindi non è necessario chiamare [RegisterClipboardFormat.](/windows/win32/api/winuser/nf-winuser-registerclipboardformata) I dati sono costituiti da [**una struttura STGMEDIUM**](/windows/win32/api/objidl/ns-objidl-ustgmedium-r1) che contiene un oggetto memoria globale. Il membro **hGlobal della** struttura punta a una [**struttura DROPFILES**](/windows/desktop/api/shlobj_core/ns-shlobj_core-dropfiles) come **membro hGlobal.**

Il **membro pFiles** della struttura [**DROPFILES**](/windows/desktop/api/shlobj_core/ns-shlobj_core-dropfiles) contiene un offset per una matrice di caratteri con terminazione **Null** doppia che contiene i nomi di file. Se si estrae un CF_HDROP da un oggetto dati, è possibile usare [**DragQueryFile**](/windows/desktop/api/Shellapi/nf-shellapi-dragqueryfilea) per estrarre singoli nomi di file dall'oggetto memoria globale. Se si sta creando un CF_HDROP da inserire in un oggetto dati, sarà necessario costruire la matrice di nomi file.

La matrice di nomi file è costituita da una serie di stringhe, ognuna delle quali contiene il percorso completo di un file, incluso il carattere **NULL di** terminazione. Un carattere **Null** aggiuntivo viene aggiunto alla stringa finale per terminare la matrice. Ad esempio, se i file c:temp1.txt e c:temp2.txt vengono trasferiti, la matrice di caratteri \\ \\ sarà simile alla seguente:


```CMD
c:\temp1.txt'\0'c:\temp2.txt'\0''\0'
```

> [!Note]  
> In questo esempio viene usato \\ '0' per rappresentare il carattere **Null,** non i caratteri letterali da includere.


Se l'oggetto è stato copiato negli Appunti come parte di un'operazione di trascinamento della selezione, il membro **pt** della struttura [**DROPFILES**](/windows/desktop/api/shlobj_core/ns-shlobj_core-dropfiles) contiene le coordinate del punto in cui è stato rilasciato l'oggetto. È possibile usare [**DragQueryPoint per**](/windows/desktop/api/Shellapi/nf-shellapi-dragquerypoint) estrarre le coordinate del cursore.

Se questo formato è presente in un oggetto dati, un ciclo di trascinamento OLE simula WM_DROPFILES [**funzionalità**](wm-dropfiles.md) con destinazioni di rilascio non OLE. Questo è importante se l'applicazione è l'origine di un'operazione di trascinamento della selezione in un sistema Windows 3.1.

### <a name="cfstr_filecontents"></a>CFSTR_FILECONTENTS

Questo identificatore di formato viene usato con [il formato CFSTR_FILEDESCRIPTOR](#cfstr_filedescriptor) per trasferire i dati come se fosse un file, indipendentemente dal modo in cui vengono effettivamente archiviati. I dati sono costituiti da [**una struttura STGMEDIUM**](/windows/win32/api/objidl/ns-objidl-ustgmedium-r1) che rappresenta il contenuto di un file. Il file viene in genere rappresentato come oggetto flusso, evitando così di dover inserire il contenuto del file in memoria. In tal caso, il **membro tymed** della struttura **STGMEDIUM** è impostato su TYMED_ISTREAM e il file è rappresentato da [**un'interfaccia IStream.**](/windows/win32/api/objidl/nn-objidl-istream) Il file può anche essere un oggetto di archiviazione o di memoria globale (TYMED_ISTORAGE o TYMED_HGLOBAL). Il formato CFSTR_FILEDESCRIPTOR contiene una [**struttura FILEDESCRIPTOR**](/windows/win32/api/shlobj_core/ns-shlobj_core-filedescriptora) per ogni file che specifica il nome e gli attributi del file.

La destinazione considera i dati associati a un CFSTR_FILECONTENTS formato come se fosse un file. Quando la destinazione chiama [**IDataObject::GetData**](/windows/win32/api/objidl/nf-objidl-idataobject-getdata) per estrarre i dati, specifica un particolare file impostando il membro **lindex** della struttura [**FORMATETC**](/windows/win32/api/objidl/ns-objidl-formatetc) sull'indice in base zero della struttura [**FILEDESCRIPTOR**](/windows/win32/api/shlobj_core/ns-shlobj_core-filedescriptora) del file nel formato [CFSTR_FILEDESCRIPTOR](#cfstr_filedescriptor) associato. La destinazione usa quindi il puntatore di interfaccia restituito o l'handle di memoria globale per estrarre i dati.

### <a name="cfstr_filedescriptor"></a>CFSTR_FILEDESCRIPTOR

Questo identificatore di formato viene usato con il [CFSTR_FILECONTENTS](#cfstr_filecontents) per trasferire i dati come gruppo di file. Questi due formati sono il modo migliore per trasferire gli oggetti della shell che non vengono archiviati come file del file system. Ad esempio, questi formati possono essere usati per trasferire un gruppo di messaggi di posta elettronica come singoli file, anche se ogni messaggio di posta elettronica viene effettivamente archiviato come blocco di dati in un database. I dati sono costituiti da [**una struttura STGMEDIUM**](/windows/win32/api/objidl/ns-objidl-ustgmedium-r1) che contiene un oggetto memoria globale. Il membro **hGlobal** della struttura punta a una struttura [**FILEGROUPDESCRIPTOR**](/windows/win32/api/shlobj_core/ns-shlobj_core-filegroupdescriptora) seguita da una matrice contenente una [**struttura FILEDESCRIPTOR**](/windows/win32/api/shlobj_core/ns-shlobj_core-filedescriptora) per ogni file nel gruppo. Per ogni **struttura FILEDESCRIPTOR** esiste un formato CFSTR_FILECONTENTS che contiene il contenuto del file. Per identificare il formato di CFSTR_FILECONTENTS di un determinato file, impostare il valore **lIndex** della struttura [**FORMATETC**](/windows/win32/api/objidl/ns-objidl-formatetc) sull'indice in base zero della struttura **FILEDESCRIPTOR del** file.

Il CFSTR_FILEDESCRIPTOR viene comunemente usato per trasferire i dati come se fossero un gruppo di file, indipendentemente dal modo in cui vengono effettivamente archiviati. Dal punto di vista della destinazione, ogni CFSTR_FILECONTENTS rappresenta un singolo file e viene trattato di conseguenza. Tuttavia, l'origine può archiviare i dati nel modo scelto. Anche se CSFTR_FILECONTENTS formato può corrispondere a un singolo file, può anche rappresentare, ad esempio, i dati estratti dall'origine da un database o da un documento di testo.

### <a name="cfstr_filename"></a>CFSTR_FILENAME

Questo identificatore di formato viene usato per trasferire un singolo file. I dati sono costituiti da [**una struttura STGMEDIUM**](/windows/win32/api/objidl/ns-objidl-ustgmedium-r1) che contiene un oggetto memoria globale. Il membro **hGlobal** della struttura punta a una singola stringa con terminazione **Null** contenente il percorso completo del file. Questo formato è stato sostituito da [CF_HDROP](#cf_hdrop), ma è supportato per la compatibilità con le Windows 3.1.

### <a name="cfstr_filenamemap"></a>CFSTR_FILENAMEMAP

Questo identificatore di formato viene usato quando un gruppo di file in [CF_HDROP](#cf_hdrop) viene rinominato e trasferito. I dati sono costituiti da [**una struttura STGMEDIUM**](/windows/win32/api/objidl/ns-objidl-ustgmedium-r1) che contiene un oggetto memoria globale. Il membro **hGlobal della struttura** punta a una matrice di caratteri con terminazione **Null** doppia. Questa matrice contiene un nuovo nome per ogni file, nello stesso ordine in cui i file sono elencati nel formato CF_HDROP. Il formato della matrice di caratteri è lo stesso usato da CF_HDROP per elencare i file trasferiti.

### <a name="cfstr_mountedvolume"></a>CFSTR_MOUNTEDVOLUME

Questo identificatore di formato viene usato per trasferire un percorso in un volume montato. È simile a [CF_HDROP](#cf_hdrop), ma contiene un solo percorso e può gestire le stringhe di percorso più lunghe che potrebbero essere necessarie per rappresentare un percorso quando il volume viene montato in una cartella. I dati sono costituiti da [**una struttura STGMEDIUM**](/windows/win32/api/objidl/ns-objidl-ustgmedium-r1) che contiene un oggetto memoria globale. Il membro **hGlobal** della struttura punta a una singola **stringa con** terminazione Null contenente il percorso completo del file. La stringa di percorso deve terminare con un \\ carattere ' ', seguito dal carattere NULL di **terminazione.**

Prima di Windows 2000, i volumi potevano essere montati solo su lettere di unità. Per Windows 2000 e versioni successive con un'unità formattata NTFS, è anche possibile montare volumi in cartelle vuote. Questa funzionalità consente di montare un volume senza richiedere una lettera di unità. Il volume montato può usare qualsiasi formato attualmente supportato, tra cui FAT, FAT32, NTFS e CDFS.

È possibile aggiungere pagine a una finestra delle proprietà Proprietà unità implementando un gestore [della finestra delle proprietà](propsheet-handlers.md). Se il volume viene montato in una lettera di unità, la shell passa le informazioni sul percorso al gestore con il [CF_HDROP](#cf_hdrop) specificato. Con Windows 2000 e versioni successive, il formato CF_HDROP viene usato quando un volume viene montato in una lettera di unità, come con i sistemi precedenti. Tuttavia, se un volume viene montato in una cartella, viene usato [CFSTR_MOUNTEDVOLUME](#cfstr_mountedvolume) identificatore di formato anziché CF_HDROP.

Se per montare i volumi verranno [](#cf_hdrop) usate solo lettere di unità, CF_HDROP e i gestori della finestra delle proprietà esistenti funzioneranno come con i sistemi precedenti. Tuttavia, se si vuole che il gestore possa visualizzare una pagina per i volumi montati in cartelle e lettere di unità, il gestore deve essere in grado di comprendere i formati CSFTR_MOUNTEDVOLUME e CF_HDROP.

### <a name="cfstr_shellidlist"></a>CFSTR_SHELLIDLIST

Questo identificatore di formato viene utilizzato durante il trasferimento delle posizioni di uno o più oggetti spazio dei nomi esistenti. Viene usato in modo molto identico a CF_HDROP [,](#cf_hdrop)ma contiene PID anziché file system percorsi. L'uso di PID consente al CFSTR_SHELLIDLIST di gestire gli oggetti virtuali e di file system virtuali. I dati sono una [**struttura STGMEDIUM**](/windows/win32/api/objidl/ns-objidl-ustgmedium-r1) che contiene un oggetto memoria globale. Il membro **hGlobal della** struttura punta a una [**struttura CIDA.**](/windows/win32/api/shlobj_core/ns-shlobj_core-cida)

Il **membro aoffset** della [**struttura CIDA**](/windows/win32/api/shlobj_core/ns-shlobj_core-cida) è una matrice contenente offset all'inizio della struttura [**ITEMIDLIST**](/windows/desktop/api/Shtypes/ns-shtypes-itemidlist) per ogni PIDL da trasferire. Per estrarre un particolare PIDL, determinare innanzitutto il relativo indice. Aggiungere quindi il **valore aoffset** che corrisponde all'indice all'indirizzo della **struttura CIDA.**

Il primo elemento di **aoffset** contiene un offset per il PIDL completo di una cartella padre. Se questo PIDL è vuoto, la cartella padre è il desktop. Ognuno degli elementi rimanenti della matrice contiene un offset per uno degli PID da trasferire. Tutti questi PID sono relativi al PIDL della cartella padre.

Le due macro seguenti possono essere usate per recuperare gli PID da una [**struttura CIDA.**](/windows/win32/api/shlobj_core/ns-shlobj_core-cida) Il primo accetta un puntatore alla struttura e recupera il file PIDL della cartella padre. Il secondo accetta un puntatore alla struttura e recupera uno degli altri PID, identificati dal relativo indice in base zero.


```C++
#define GetPIDLFolder(pida) (LPCITEMIDLIST)(((LPBYTE)pida)+(pida)->aoffset[0])

#define GetPIDLItem(pida, i) (LPCITEMIDLIST)(((LPBYTE)pida)+(pida)->aoffset[i+1])
```

> [!Note]  
> Il valore restituito da queste macro è un puntatore alla struttura [**ITEMIDLIST**](/windows/desktop/api/Shtypes/ns-shtypes-itemidlist) di PIDL. Poiché queste strutture variano di lunghezza, è necessario determinare la fine della struttura passando attraverso ognuna delle strutture [**SHITEMID**](/windows/desktop/api/Shtypes/ns-shtypes-shitemid) della struttura **ITEMIDLIST** fino a raggiungere il valore **NULL** a due byte che contrassegna la fine.

### <a name="cfstr_shellidlistoffset"></a>CFSTR_SHELLIDLISTOFFSET

Questo identificatore di formato viene usato con formati quali [CF_HDROP](#cf_hdrop), [CFSTR_SHELLIDLIST](#cfstr_shellidlist)e [CFSTR_FILECONTENTS](#cfstr_filecontents) per specificare la posizione di un gruppo di oggetti dopo un trasferimento. I dati sono costituiti da [**una struttura STGMEDIUM**](/windows/win32/api/objidl/ns-objidl-ustgmedium-r1) che contiene un oggetto memoria globale. Il membro **hGlobal della** struttura punta a una matrice di [**strutture POINT.**](/previous-versions//dd162805(v=vs.85)) La prima struttura specifica le coordinate dello schermo, in pixel, dell'angolo superiore sinistro del rettangolo che racchiude il gruppo. Il resto delle strutture specifica le posizioni dei singoli oggetti rispetto alla posizione del gruppo. Devono essere nello stesso ordine usato per elencare gli oggetti nel formato associato.

## <a name="formats-for-transferring-virtual-objects"></a>Formati per il trasferimento di oggetti virtuali

Il CFSTR_SHELLIDLIST può essere usato per trasferire sia gli file system virtuali che gli oggetti virtuali. Esistono tuttavia anche diversi formati specializzati per il trasferimento di tipi specifici di oggetti virtuali.

-   [CFSTR_NETRESOURCES](#cfstr_netresources)
-   [CFSTR_PRINTERGROUP](#cfstr_printergroup)
-   [CFSTR_INETURL](#cfstr_ineturl)
-   [CFSTR_SHELLURL (deprecato)](#cfstr_shellurl-deprecated)

### <a name="cfstr_netresources"></a>CFSTR_NETRESOURCES

Questo identificatore di formato viene usato durante il trasferimento di risorse di rete, ad esempio un dominio o un server. I dati sono una [**struttura STGMEDIUM**](/windows/win32/api/objidl/ns-objidl-ustgmedium-r1) che contiene un oggetto memoria globale. Il membro **hGlobal della** struttura punta a una [**struttura NRESARRAY.**](/windows/desktop/api/shlobj_core/ns-shlobj_core-nresarray) Il **membro nr** di tale struttura indica una struttura [**NETRESOURCE**](/windows/win32/api/rrascfg/nn-rrascfg-ieapproviderconfig) il cui membro **lpRemoteName** contiene una stringa con terminazione **Null** che identifica la risorsa di rete. L'obiettivo di rilascio può quindi usare i dati con qualsiasi funzione API [di rete Windows (WNet),](../wnet/windows-networking-wnet-.md) ad esempio [**WNetAddConnection,**](/windows/win32/api/winnetwk/nf-winnetwk-wnetaddconnectiona)per eseguire operazioni di rete sull'oggetto.

### <a name="cfstr_printergroup"></a>CFSTR_PRINTERGROUP

Questo identificatore di formato viene utilizzato durante il trasferimento dei nomi descrittivi delle stampanti. I dati sono una [**struttura STGMEDIUM**](/windows/win32/api/objidl/ns-objidl-ustgmedium-r1) che contiene un oggetto memoria globale. Il membro **hGlobal** della struttura punta a una stringa nello stesso formato usato con [CF_HDROP](#cf_hdrop). Tuttavia, il **membro pFiles** della struttura [**DROPFILES**](/windows/desktop/api/shlobj_core/ns-shlobj_core-dropfiles) contiene uno o più nomi descrittivi di stampanti anziché percorsi di file.

### <a name="cfstr_ineturl"></a>CFSTR_INETURL

Questo identificatore di formato [sostituisce CFSTR_SHELLURL (deprecato).](#cfstr_shellurl-deprecated) Se si vuole che l'applicazione manipoli gli URL degli Appunti, usare CFSTR_INETURL anziché CFSTR_SHELLURL (deprecato). Questo formato offre la migliore rappresentazione degli Appunti di un singolo URL. Se unicode non è definito, l'applicazione recupera la CF_TEXT/CFSTR_SHELLURL dell'URL. Se unicode è definito, l'applicazione recupera la CF_UNICODE dell'URL.

### <a name="cfstr_shellurl-deprecated"></a>CFSTR_SHELLURL (deprecato)

> [!Note]  
> Questo identificatore di formato è stato deprecato. Usare CFSTR_INETURL in alternativa.

 

## <a name="formats-for-communication-between-source-and-target"></a>Formati per la comunicazione tra origine e destinazione

Questi identificatori di formato consentono la comunicazione tra origine e destinazione. I formati accompagnano i dati e offrono alle applicazioni un maggiore livello di controllo sulle operazioni di spostamento, copia e incolla o trascinamento della selezione che coinvolgono gli oggetti shell.

-   [CFSTR_INDRAGLOOP](#cfstr_indragloop)
-   [CFSTR_LOGICALPERFORMEDDROPEFFECT](#cfstr_logicalperformeddropeffect)
-   [CFSTR_PASTESUCCEEDED](#cfstr_pastesucceeded)
-   [CFSTR_PERFORMEDDROPEFFECT](#cfstr_performeddropeffect)
-   [CFSTR_PREFERREDDROPEFFECT](#cfstr_preferreddropeffect)
-   [CFSTR_TARGETCLSID](#cfstr_targetclsid)
-   [CFSTR_UNTRUSTEDDRAGDROP](#cfstr_untrusteddragdrop)
-   [Finestra di trascinamento](#dragwindow)

### <a name="cfstr_indragloop"></a>CFSTR_INDRAGLOOP

Questo identificatore di formato viene utilizzato da un oggetto dati per indicare se si trova in un ciclo di trascinamento della selezione. I dati sono una [**struttura STGMEDIUM**](/windows/win32/api/objidl/ns-objidl-ustgmedium-r1) che contiene un oggetto memoria globale. Il membro **hGlobal della** struttura punta a un **valore DWORD.** Se il **valore DWORD** è diverso da zero, l'oggetto dati si trova all'interno di un ciclo di trascinamento della selezione. Se il valore è impostato su zero, l'oggetto dati non si trova all'interno di un ciclo di trascinamento della selezione.

Alcune destinazioni di rilascio potrebbero [**chiamare IDataObject::GetData**](/windows/win32/api/objidl/nf-objidl-idataobject-getdata) e tentare di estrarre i dati mentre l'oggetto è ancora all'interno del ciclo di trascinamento della selezione. Il rendering completo dell'oggetto per ogni occorrenza di questo tipo potrebbe causare il blocco del cursore di trascinamento. Se l'oggetto dati supporta CFSTR_INDRAGLOOP , la destinazione può usare tale formato per controllare lo stato del ciclo di trascinamento della selezione ed evitare il rendering a elevato utilizzo di memoria dell'oggetto fino [a](#cfstr_indragloop)quando non viene effettivamente eliminato. I formati che richiedono un utilizzo elevato di memoria per il rendering devono essere comunque inclusi nell'enumeratore [**FORMATETC**](/windows/win32/api/objidl/ns-objidl-formatetc) e nelle chiamate a [**IDataObject::QueryGetData.**](/windows/win32/api/objidl/nf-objidl-idataobject-querygetdata) Se l'oggetto dati non CFSTR_INDRAGLOOP, deve agire come se il valore fosse impostato su zero.

### <a name="cfstr_logicalperformeddropeffect"></a>CFSTR_LOGICALPERFORMEDDROPEFFECT

[Versione 5.0.](versions.md) Questo identificatore di formato consente a un'origine di rilascio di chiamare il metodo [**IDataObject::GetData**](/windows/win32/api/objidl/nf-objidl-idataobject-getdata) dell'oggetto dati per determinare il risultato di un trasferimento dei dati della shell. I dati sono una [**struttura STGMEDIUM**](/windows/win32/api/objidl/ns-objidl-ustgmedium-r1) che contiene un oggetto memoria globale. Il membro **hGlobal** della struttura punta a un valore DWORD contenente un [**valore DROPEFFECT.**](../com/dropeffect-constants.md)

L CFSTR_PERFORMEDDROPEFFECT idato di formato personalizzato era progettato per consentire alla destinazione di indicare all'oggetto dati quale operazione è stata effettivamente eseguita. [](#cfstr_performeddropeffect) Tuttavia, la shell usa [spostamenti ottimizzati per file system](datascenarios.md) oggetti quando possibile. In tal caso, la shell imposta in genere il valore CFSTR_PERFORMEDDROPEFFECT su DROPEFFECT_NONE, per indicare all'oggetto dati che i dati originali sono stati eliminati. Di conseguenza, l'origine non può usare CFSTR_PERFORMEDDROPEFFECT valore per determinare quale operazione è stata eseguita. Sebbene la maggior parte delle origini non necessiti di queste informazioni, esistono alcune eccezioni. Ad esempio, anche se gli spostamenti ottimizzati eliminano la necessità che un'origine elimini i dati, potrebbe comunque essere necessario aggiornare un database correlato per indicare che i file sono stati spostati o copiati.

Se un'origine deve sapere quale operazione è stata eseguita, può chiamare il metodo [**IDataObject::GetData**](/windows/win32/api/objidl/nf-objidl-idataobject-getdata) dell'oggetto dati e richiedere il formato CFSTR_LOGICALPERFORMEDDROPEFFECT dati. Questo formato riflette essenzialmente ciò che accade dal punto di vista dell'utente dopo il completamento dell'operazione. Se viene creato un nuovo file e il file originale viene eliminato, l'utente visualizza un'operazione di spostamento e il valore dei dati del formato viene impostato su DROPEFFECT_MOVE. Se il file originale è ancora presente, l'utente visualizza un'operazione di copia e il valore dei dati del formato è impostato su DROPEFFECT_COPY. Se è stato creato un collegamento, il valore dei dati del formato verrà DROPEFFECT_LINK.

### <a name="cfstr_pastesucceeded"></a>CFSTR_PASTESUCCEEDED

Questo identificatore di formato viene usato dalla destinazione per informare l'oggetto dati, tramite il relativo metodo [**IDataObject::SetData,**](/windows/win32/api/objidl/nf-objidl-idataobject-setdata) che un'operazione di eliminazione su incolla è riuscita. I dati sono una [**struttura STGMEDIUM**](/windows/win32/api/objidl/ns-objidl-ustgmedium-r1) che contiene un oggetto memoria globale. Il membro **hGlobal della struttura** punta a un **valore DWORD** contenente un [**valore DROPEFFECT.**](../com/dropeffect-constants.md) Questo formato viene utilizzato per notificare all'oggetto dati che deve completare l'operazione di taglio ed eliminare i dati originali, se necessario. Per altre informazioni, vedere [Operazioni Delete-on-Paste](datascenarios.md).

### <a name="cfstr_performeddropeffect"></a>CFSTR_PERFORMEDDROPEFFECT

Questo identificatore di formato viene usato dalla destinazione per informare l'oggetto dati tramite il relativo metodo [**IDataObject::SetData**](/windows/win32/api/objidl/nf-objidl-idataobject-setdata) del risultato di un trasferimento dei dati. I dati sono una [**struttura STGMEDIUM**](/windows/win32/api/objidl/ns-objidl-ustgmedium-r1) che contiene un oggetto memoria globale. Il membro **hGlobal** della struttura punta a un **valore DWORD** impostato sul valore [**DROPEFFECT**](../com/dropeffect-constants.md) appropriato, in genere DROPEFFECT_MOVE o DROPEFFECT_COPY.

Questo formato viene in genere usato quando il risultato di un'operazione può essere lo spostamento o la copia, ad esempio in un'operazione di spostamento ottimizzata o di eliminazione su incolla. [](datascenarios.md) Fornisce un modo affidabile per la destinazione per indicare all'oggetto dati cosa è effettivamente accaduto. È stato introdotto perché il valore *di pdwEffect* restituito da [**DoDragDrop**](/windows/win32/api/ole2/nf-ole2-dodragdrop) non indica in modo affidabile quale operazione è stata eseguita. Il [CFSTR_PERFORMEDDROPEFFECT](#cfstr_performeddropeffect) è il modo affidabile per indicare che è stato effettuato uno spostamento non corretto.

### <a name="cfstr_preferreddropeffect"></a>CFSTR_PREFERREDDROPEFFECT

Questo identificatore di formato viene utilizzato dall'origine per specificare se il metodo di trasferimento dei dati preferito è lo spostamento o la copia. Un obiettivo di rilascio richiede questo formato chiamando il metodo [**IDataObject::GetData dell'oggetto**](/windows/win32/api/objidl/nf-objidl-idataobject-getdata) dati. I dati sono una [**struttura STGMEDIUM**](/windows/win32/api/objidl/ns-objidl-ustgmedium-r1) che contiene un oggetto memoria globale. Il membro **hGlobal della** struttura punta a un **valore DWORD.** Questo valore è impostato su DROPEFFECT_MOVE se un'operazione di spostamento è preferibile o DROPEFFECT_COPY se è preferibile un'operazione di copia.

Questa funzionalità viene usata quando un'origine può supportare un'operazione di spostamento o copia. Usa il formato [CFSTR_PREFERREDDROPEFFECT](#cfstr_preferreddropeffect) per comunicare la propria preferenza alla destinazione. Poiché la destinazione non è obbligata a rispettare la richiesta, la destinazione deve chiamare il metodo [**IDataObject::SetData**](/windows/win32/api/objidl/nf-objidl-idataobject-setdata) dell'origine con un formato [CFSTR_PERFORMEDDROPEFFECT](#cfstr_performeddropeffect) per indicare all'oggetto dati quale operazione è stata effettivamente eseguita.

Con [un'operazione delete-on-paste,](datascenarios.md) il formato CFSTR_PREFERREDDROPFORMAT viene usato per indicare alla destinazione se l'origine ha fatto un'operazione taglia o copia. Con un'operazione di trascinamento della selezione, è possibile usare CFSTR_PREFERREDDROPFORMAT per specificare l'azione della shell. Se questo formato non è presente, la shell esegue un'azione predefinita, in base al contesto. Ad esempio, se un utente trascina un file da un volume e lo rilascia in un altro volume, l'azione predefinita della shell è copiare il file. Includendo un formato CFSTR_PREFERREDDROPFORMAT nell'oggetto dati, è possibile eseguire l'override dell'azione predefinita e indicare in modo esplicito alla shell di copiare, spostare o collegare il file. Se l'utente sceglie di trascinare con il pulsante destro, CFSTR_PREFERREDDROPFORMAT specifica il comando predefinito nel menu di scelta rapida [di](context-menu-handlers.md) trascinamento della selezione. L'utente è comunque libero di scegliere altri comandi nel menu.

Prima di Microsoft Internet Explorer 4.0, un'applicazione indicava il trasferimento dei tipi di file di collegamento impostando FD_LINKUI nel membro **dwFlags** della struttura [**FILEDESCRIPTOR.**](/windows/win32/api/shlobj_core/ns-shlobj_core-filedescriptora) Le destinazioni dovevano quindi usare una chiamata potenzialmente dispendiosa in termini di tempo a [**IDataObject::GetData**](/windows/win32/api/objidl/nf-objidl-idataobject-getdata) per determinare se il flag FD_LINKUI è stato impostato. A questo punto, il modo migliore per indicare che i collegamenti vengono trasferiti è usare il formato CFSTR_PREFERREDDROPEFFECT impostato su DROPEFFECT_LINK. Tuttavia, per garantire la compatibilità con le versioni precedenti dei sistemi precedenti, le origini devono comunque impostare il flag FD_LINKUI precedente.

### <a name="cfstr_targetclsid"></a>CFSTR_TARGETCLSID

Questo identificatore di formato viene usato da una destinazione per fornire il CLSID all'origine. I dati sono una [**struttura STGMEDIUM**](/windows/win32/api/objidl/ns-objidl-ustgmedium-r1) che contiene un oggetto memoria globale. Il membro **hGlobal della struttura** punta al GUID CLSID dell'obiettivo di rilascio.

Questo formato viene utilizzato principalmente per consentire l'eliminazione degli oggetti trascinandoli nella Cestino. Quando un oggetto viene rilasciato nel Cestino, il metodo [**IDataObject::SetData**](/windows/win32/api/objidl/nf-objidl-idataobject-setdata) dell'origine viene chiamato con un formato CFSTR_TARGETCLSID impostato sul CLSID (CLSID_RecycleBin) del Cestino. L'origine può quindi eliminare l'oggetto originale.

### <a name="cfstr_untrusteddragdrop"></a>CFSTR_UNTRUSTEDDRAGDROP

Questo identificatore di formato viene usato da Windows Internet Explorer e dalla shell di Windows per fornire un meccanismo tramite il quale bloccare o richiedere operazioni di trascinamento della selezione provenienti da Internet Explorer insieme al [**flag**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms537178(v=vs.85)) URLACTION_SHELL_ENHANCED_DRAGDROP_SECURITY.

**CFSTR_UNTRUSTEDDRAGDROP** viene aggiunto dall'origine di un'operazione di trascinamento della selezione per specificare che l'oggetto dati potrebbe contenere dati non attendibili. I dati sono rappresentati da una [**struttura STGMEDIUM**](/windows/win32/api/objidl/ns-objidl-ustgmedium-r1) che contiene un oggetto memoria globale. Il membro **hGlobal** della struttura punta a un **valore DWORD** impostato su un flag action [**URL**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms537178(v=vs.85)) appropriato per generare un controllo dei criteri tramite il metodo [**IInternetSecurityManager::P rocessUrlAction,**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms537136(v=vs.85)) usando il flag [**PUAF_ENFORCERESTRICTED.**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms537171(v=vs.85))

### <a name="dragwindow"></a>Finestra di trascinamento

Questo formato viene usato in un'operazione di trascinamento della selezione per identificare l'immagine di trascinamento di un oggetto (finestra) in modo che le informazioni visive possano essere aggiornate dinamicamente. Quando un oggetto viene trascinato su un obiettivo di rilascio, un'applicazione aggiorna la struttura [**DROPDESCRIPTION**](/windows/desktop/api/shlobj_core/ns-shlobj_core-dropdescription) in risposta al metodo [**IDropTarget::D ragOver**](/windows/win32/api/oleidl/nf-oleidl-idroptarget-dragover) o [**IDropSource::GiveFeedback.**](/windows/win32/api/oleidl/nf-oleidl-idropsource-givefeedback) DROPDESCRIPTION **viene** aggiornato con un nuovo valore [**DROPIMAGETYPE**](/windows/desktop/api/shlobj_core/ne-shlobj_core-dropimagetype) che indica la decorazione da applicare all'oggetto visivo della finestra di trascinamento. ad esempio un'indicazione che il file viene copiato anziché spostato o che l'oggetto non può essere rilasciato in tale percorso. Tuttavia, finché l'oggetto non riceve [**DDWM_UPDATEWINDOW**](ddwm-updatewindow.md) messaggio, gli oggetti visivi non vengono aggiornati. Questo formato fornisce **l'oggetto HWND** della finestra di trascinamento del destinatario al mittente **del DDWM_UPDATEWINDOW** messaggio.

I dati degli Appunti sono di [**tipo TYMED_HGLOBAL**](/windows/win32/api/objidl/ne-objidl-tymed). È una **rappresentazione DWORD** di **un oggetto HWND.** I dati possono essere passati alla funzione **ULongToHandle,** definita in Basetsd.h, per fornire un **HWND** a 64 bit da usare in un Windows a 64 bit.

Questo formato non richiede l'inclusione di Shlobj.h.

 

 
