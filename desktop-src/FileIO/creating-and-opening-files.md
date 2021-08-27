---
description: Considerazioni per la creazione o l'apertura di un file tramite la funzione CreateFile.
ms.assetid: 094cac29-c66d-409e-8928-878dc693d393
title: Creazione e apertura di file
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e80449942fbceb39c37604bf6d8b5410d171d195
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2021
ms.locfileid: "122469928"
---
# <a name="creating-and-opening-files"></a>Creazione e apertura di file

La [**funzione CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) può creare un nuovo file o aprire un file esistente. È necessario specificare il nome del file, le istruzioni di creazione e altri attributi. Quando un'applicazione crea un nuovo file, il sistema operativo lo aggiunge alla directory specificata.

Il sistema operativo assegna un identificatore univoco, denominato *handle*, a ogni file aperto o creato tramite [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea). Un'applicazione può usare questo handle con funzioni che leggono, scrivono e descrivono il file. È valido fino alla chiusura di tutti i riferimenti all'handle. All'avvio di un'applicazione, eredita tutti gli handle aperti dal processo che l'ha avviata se gli handle sono stati creati come ereditabili.

Un'applicazione deve controllare il valore dell'handle restituito da [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) prima di tentare di usare l'handle per accedere al file. Se si verifica un errore, il valore dell'handle sarà **INVALID \_ HANDLE \_ VALUE** e l'applicazione può usare la [**funzione GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) per informazioni sull'errore estese.

Quando un'applicazione usa [**CreateFile,**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea)deve usare il *parametro dwDesiredAccess* per specificare se intende leggere dal file, scrivere nel file, sia in lettura che in scrittura o in nessuno dei due. Questa operazione è nota come richiesta di una *modalità di accesso*. L'applicazione deve anche usare il *parametro dwCreationDisposition* per specificare l'azione da eseguire se il file esiste già, noto come *disposizione di creazione.* Ad esempio, un'applicazione può chiamare **CreateFile** con *dwCreationDisposition* impostato su **CREATE \_ ALWAYS** per creare sempre un nuovo file, anche se esiste già un file con lo stesso nome (sovrascrivendo quindi il file esistente). La riuscita o meno di questa operazione dipende da fattori quali gli attributi e le impostazioni di sicurezza del file precedente . Per altre informazioni, vedere le sezioni seguenti.

Un'applicazione usa anche [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) per specificare se vuole condividere il file per la lettura, la scrittura, entrambi o nessuno dei due. Questa operazione è nota come modalità *di condivisione*. Un file aperto non condiviso *(dwShareMode* impostato su zero) non può essere aperto di nuovo dall'applicazione che lo ha aperto o da un'altra applicazione, fino a quando l'handle non è stato chiuso. Questa operazione viene definita anche accesso esclusivo.

Quando un processo usa [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) per tentare di aprire un file già aperto in modalità di condivisione *(dwShareMode* impostato su un valore valido diverso da zero), il sistema confronta le modalità di accesso e condivisione richieste con quelle specificate all'apertura del file. Se si specifica una modalità di accesso o di condivisione in conflitto con le modalità specificate nella chiamata precedente, **CreateFile ha** esito negativo.

La tabella seguente illustra le combinazioni valide di due chiamate a [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) usando diverse modalità di accesso e modalità di condivisione (*dwDesiredAccess*, *dwShareMode* rispettivamente). Non è importante l'ordine in cui vengono effettuate le chiamate **CreateFile.** Tuttavia, tutte le operazioni di I/O di file successive su ogni handle di file saranno comunque vincolate dalle modalità di accesso e condivisione correnti associate a tale handle di file specifico.




| Prima chiamata a <a href="/windows/desktop/api/FileAPI/nf-fileapi-createfilea"> <strong>CreateFile</strong></a> | Second calls to CreateFile (Second calls to <a href="/windows/desktop/api/FileAPI/nf-fileapi-createfilea"> <strong>CreateFile) valide</strong></a> | 
|-------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <strong>GENERIC_READ</strong>, <strong>FILE_SHARE_READ</strong><br /> | <ul><li><strong>GENERIC_READ</strong>, <strong>FILE_SHARE_READ</strong></li><li><strong>GENERIC_READ</strong>, <strong>FILE_SHARE_READ</strong> | <strong>FILE_SHARE_WRITE</strong></li></ul> | 
| <strong>GENERIC_READ</strong>, <strong>FILE_SHARE_WRITE</strong><br /> | <ul><li><strong>GENERIC_WRITE</strong>, <strong>FILE_SHARE_READ</strong></li><li><strong>GENERIC_WRITE</strong>, <strong>FILE_SHARE_READ</strong> | <strong>FILE_SHARE_WRITE</strong></li></ul> | 
| <strong>GENERIC_READ</strong>, <strong>FILE_SHARE_READ</strong> | <strong>FILE_SHARE_WRITE</strong><br /> | <ul><li><strong>GENERIC_READ</strong>, <strong>FILE_SHARE_READ</strong></li><li><strong>GENERIC_READ</strong>, <strong>FILE_SHARE_READ</strong> | <strong>FILE_SHARE_WRITE</strong></li><li><strong>GENERIC_WRITE</strong>, <strong>FILE_SHARE_READ</strong></li><li><strong>GENERIC_WRITE</strong>, <strong>FILE_SHARE_READ</strong> | <strong>FILE_SHARE_WRITE</strong></li><li><strong>GENERIC_READ</strong> | <strong>GENERIC_WRITE</strong>, <strong>FILE_SHARE_READ</strong></li><li><strong>GENERIC_READ</strong> | <strong>GENERIC_WRITE</strong>, <strong>FILE_SHARE_READ</strong> | <strong>FILE_SHARE_WRITE</strong></li></ul> | 
| <strong>GENERIC_WRITE</strong>, <strong>FILE_SHARE_READ</strong><br /> | <ul><li><strong>GENERIC_READ</strong>, <strong>FILE_SHARE_WRITE</strong></li><li><strong>GENERIC_READ</strong>, <strong>FILE_SHARE_READ</strong> | <strong>FILE_SHARE_WRITE</strong></li></ul> | 
| <strong>GENERIC_WRITE</strong>, <strong>FILE_SHARE_WRITE</strong><br /> | <ul><li><strong>GENERIC_WRITE</strong>, <strong>FILE_SHARE_WRITE</strong></li><li><strong>GENERIC_WRITE</strong>, <strong>FILE_SHARE_READ</strong> | <strong>FILE_SHARE_WRITE</strong></li></ul> | 
| <strong>GENERIC_WRITE</strong>, <strong>FILE_SHARE_READ</strong> | <strong>FILE_SHARE_WRITE</strong><br /> | <ul><li><strong>GENERIC_READ</strong>, <strong>FILE_SHARE_WRITE</strong></li><li><strong>GENERIC_READ</strong>, <strong>FILE_SHARE_READ</strong> | <strong>FILE_SHARE_WRITE</strong></li><li><strong>GENERIC_WRITE</strong>, <strong>FILE_SHARE_WRITE</strong></li><li><strong>GENERIC_WRITE</strong>, <strong>FILE_SHARE_READ</strong> | <strong>FILE_SHARE_WRITE</strong></li><li><strong>GENERIC_READ</strong> | <strong>GENERIC_WRITE</strong>, <strong>FILE_SHARE_WRITE</strong></li><li><strong>GENERIC_READ</strong> | <strong>GENERIC_WRITE</strong>, <strong>FILE_SHARE_READ</strong> | <strong>FILE_SHARE_WRITE</strong></li></ul> | 
| <strong>GENERIC_READ</strong> | <strong>GENERIC_WRITE</strong>, <strong>FILE_SHARE_READ</strong><br /> | <ul><li><strong>GENERIC_READ</strong>, <strong>FILE_SHARE_READ</strong> | <strong>FILE_SHARE_WRITE</strong></li></ul> | 
| <strong>GENERIC_READ</strong> | <strong>GENERIC_WRITE</strong>, <strong>FILE_SHARE_WRITE</strong><br /> | <ul><li><strong>GENERIC_WRITE</strong>, <strong>FILE_SHARE_READ</strong> | <strong>FILE_SHARE_WRITE</strong></li></ul> | 
| <strong>GENERIC_READ</strong> | <strong>GENERIC_WRITE</strong>, <strong>FILE_SHARE_READ</strong> | <strong>FILE_SHARE_WRITE</strong><br /> | <ul><li><strong>GENERIC_READ</strong>, <strong>FILE_SHARE_READ</strong> | <strong>FILE_SHARE_WRITE</strong></li><li><strong>GENERIC_WRITE</strong>, <strong>FILE_SHARE_READ</strong> | <strong>FILE_SHARE_WRITE</strong></li><li><strong>GENERIC_READ</strong> | <strong>GENERIC_WRITE</strong>, <strong>FILE_SHARE_READ</strong> | <strong>FILE_SHARE_WRITE</strong></li></ul> | 




 

Oltre agli attributi di file standard, è anche possibile specificare gli attributi di sicurezza includendo un puntatore a una struttura [**SECURITY \_ ATTRIBUTES**](/previous-versions/windows/desktop/legacy/aa379560(v=vs.85)) come quarto parametro di [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea). Tuttavia, il file system sottostante deve supportare la sicurezza per avere alcun effetto (ad esempio, il file system NTFS lo supporta, ma i vari file system FAT non lo supportano). Per altre informazioni sugli attributi di sicurezza, vedere [Controllo di accesso](/windows/desktop/SecAuthZ/access-control).

Un'applicazione che crea un nuovo file può fornire un handle facoltativo a un file modello, da cui [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) accetta attributi di file e attributi estesi per la creazione del nuovo file.

## <a name="createfile-scenarios"></a>Scenari CreateFile

Esistono diversi scenari fondamentali per avviare l'accesso a un file usando la [**funzione CreateFile.**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) Questi sono riepilogati come segue:

-   Creazione di un nuovo file quando non esiste già un file con tale nome.
-   Creazione di un nuovo file anche se esiste già un file con lo stesso nome, cancellando i dati e iniziando da vuoto.
-   Apertura di un file esistente solo se esistente e solo intatto.
-   Apertura di un file esistente solo se esistente, troncamento in modo che sia vuoto.
-   Apertura di un file sempre: così come è se esiste, ne viene creato uno nuovo se non esiste.

Questi scenari sono controllati dall'uso corretto del *parametro dwCreationDisposition.* Di seguito è riportata una suddivisione del mapping di questi scenari ai valori per questo parametro e di cosa accade quando vengono usati.

Quando si crea o si apre un nuovo file quando non esiste già un file con tale nome (*dwCreationDisposition* impostato su **CREATE \_ NEW,** **CREATE \_ ALWAYS** o **OPEN \_ ALWAYS),** la funzione [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) esegue le azioni seguenti:

-   Combina gli attributi di file e i flag specificati da *dwFlagsAndAttributes con* **FILE ATTRIBUTE \_ \_ ARCHIVE**.
-   Imposta la lunghezza del file su zero.
-   Copia gli attributi estesi forniti dal file modello nel nuovo file se viene specificato il parametro *hTemplateFile* ( esegue l'override di tutti i flag **FILE \_ ATTRIBUTE \_ \*** specificati in precedenza).
-   Imposta il flag inherit specificato dal **membro bInheritHandle** e il descrittore di sicurezza specificato dal membro **lpSecurityDescriptor** del parametro *lpSecurityAttributes* (struttura [**SECURITY \_ ATTRIBUTES),**](/previous-versions/windows/desktop/legacy/aa379560(v=vs.85)) se specificato.

Quando si crea un nuovo file anche se esiste già un file con lo stesso nome (*dwCreationDisposition* impostato su **CREATE \_ ALWAYS**), la funzione [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) esegue le azioni seguenti:

-   Controlla gli attributi di file correnti e le impostazioni di sicurezza per l'accesso in scrittura, con esito negativo se negato.
-   Combina gli attributi di file e i flag specificati da *dwFlagsAndAttributes* con **FILE ATTRIBUTE \_ \_ ARCHIVE** e gli attributi di file esistenti.
-   Imposta la lunghezza del file su zero, ovvero tutti i dati presenti nel file non sono più disponibili e il file è vuoto.
-   Copia gli attributi estesi forniti dal file modello nel nuovo file se viene specificato il parametro *hTemplateFile* ( esegue l'override di tutti i flag **FILE \_ ATTRIBUTE \_ \*** specificati in precedenza).
-   Imposta il flag inherit specificato dal membro **bInheritHandle** del parametro *lpSecurityAttributes* (struttura [**SECURITY \_ ATTRIBUTES),**](/previous-versions/windows/desktop/legacy/aa379560(v=vs.85)) se specificato, ma ignora il membro **lpSecurityDescriptor** della struttura **SECURITY \_ ATTRIBUTES.**
-   In caso contrario, [**createFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) restituisce un handle valido, chiamando [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) verrà restituito il codice **ERROR ALREADY \_ \_ EXISTS,** anche se per questo particolare caso d'uso non si tratta effettivamente di un errore come tale (se si intende creare un file "nuovo" (vuoto) al posto di quello esistente.

Quando si apre un file esistente (*dwCreationDisposition* impostato su **OPEN \_ EXISTING,** **OPEN \_ ALWAYS** o **TRUNCATE \_ EXISTING**), la [**funzione CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) esegue le azioni seguenti:

-   Controlla gli attributi di file correnti e le impostazioni di sicurezza per l'accesso richiesto, senza esito negativo se negato.
-   Combina i flag di file (**FILE \_ FLAG \_ \** _) specificati da _dwFlagsAndAttributes* con gli attributi \_ \_ \** di file esistenti e ignora gli attributi di file (**FILE ATTRIBUTE _) specificati da _dwFlagsAndAttributes*.
-   Imposta la lunghezza del file su zero solo se *dwCreationDisposition* è impostato su **TRUNCATE \_ EXISTING,** in caso contrario la lunghezza corrente del file viene mantenuta e il file viene aperto così come è.
-   Ignora il *parametro hTemplateFile.*
-   Imposta il flag inherit specificato dal membro **bInheritHandle** del parametro *lpSecurityAttributes* (struttura [**SECURITY \_ ATTRIBUTES),**](/previous-versions/windows/desktop/legacy/aa379560(v=vs.85)) se specificato, ma ignora il membro **lpSecurityDescriptor** della struttura **SECURITY \_ ATTRIBUTES.**

## <a name="file-attributes-and-directories"></a>Attributi e directory dei file

Gli attributi di file fanno parte dei metadati associati a un file o a una directory, ognuno con il proprio scopo e regole su come può essere impostato e modificato. Alcuni di questi attributi si applicano solo ai file e altri solo alle directory. Ad esempio, l'attributo **FILE \_ ATTRIBUTE \_ DIRECTORY** si applica solo alle directory: viene usato dal file system per determinare se un oggetto su disco è una directory, ma non può essere modificato per un oggetto file system esistente.

Alcuni attributi di file possono essere impostati per una directory, ma hanno significato solo per i file creati in tale directory, fungendo da attributi predefiniti. Ad esempio, **FILE \_ ATTRIBUTE \_ COMPRESSED** può essere impostato su un oggetto directory, ma poiché l'oggetto directory stesso non contiene dati effettivi, non viene effettivamente compresso. Tuttavia, le directory contrassegnate con questo attributo indicano al file system di comprimere i nuovi file aggiunti a tale directory. Qualsiasi attributo di file che può essere impostato in una directory e verrà impostato anche per i nuovi file aggiunti a tale directory viene definito *attributo ereditato.*

La [**funzione CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) fornisce un parametro per l'impostazione di determinati attributi di file quando viene creato un file. In generale, questi attributi sono i più comuni da usare per un'applicazione in fase di creazione del file, ma non tutti gli attributi di file possibili sono disponibili per **CreateFile**. Alcuni attributi di file richiedono l'uso di altre funzioni, ad esempio [**SetFileAttributes,**](/windows/desktop/api/FileAPI/nf-fileapi-setfileattributesa) [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol)o [**DecryptFile**](/windows/desktop/api/WinBase/nf-winbase-decryptfilea) dopo che il file esiste già. Nel caso di **FILE \_ ATTRIBUTE \_ DIRECTORY,** la [**funzione CreateDirectory**](/windows/desktop/api/FileAPI/nf-fileapi-createdirectorya) è necessaria in fase di creazione perché **CreateFile** non è in grado di creare directory. Gli altri attributi di file che richiedono una gestione speciale sono **FILE \_ ATTRIBUTE \_ REPARSE \_ POINT** e **FILE ATTRIBUTE \_ \_ SPARSE \_ FILE**, che richiedono **DeviceIoControl**. Per altre informazioni, vedere [**SetFileAttributes**](/windows/desktop/api/FileAPI/nf-fileapi-setfileattributesa).

Come indicato in precedenza, l'ereditarietà degli attributi di file si verifica quando viene creato un file con attributi di file letti dagli attributi della directory in cui si trova il file. Nella tabella seguente vengono riepilogati questi attributi ereditati e la loro relazione con [**le funzionalità CreateFile.**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea)



| Stato dell'attributo della directory                                      | [**Funzionalità di override**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) dell'ereditarietà CreateFile per i nuovi file      |
|----------------------------------------------------------------|-------------------------------------------------------------------------------------|
| **FILE \_ SET \_ DI ATTRIBUTI COMPRESSI.**<br/>                | Nessun controllo. Usare [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) per cancellare.<br/>    |
| **FILE \_ ATTRIBUTO \_ COMPRESSED** non impostato.<br/>            | Nessun controllo. Usare [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) per impostare .<br/>      |
| **FILE \_ SET \_ DI ATTRIBUTI CRITTOGRAFATI.**<br/>                 | Nessun controllo. Usare [**DecryptFile**](/windows/desktop/api/WinBase/nf-winbase-decryptfilea).<br/>                      |
| **FILE \_ ATTRIBUTO \_ ENCRYPTED** non impostato.<br/>             | Può essere impostato usando [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea).<br/>                       |
| **FILE \_ ATTRIBUTE \_ NOT \_ CONTENT \_ INDEXED** set.<br/>     | Nessun controllo. Usare [**SetFileAttributes**](/windows/desktop/api/FileAPI/nf-fileapi-setfileattributesa) per cancellare.<br/> |
| **FILE \_ ATTRIBUTE \_ NOT \_ CONTENT \_ INDEXED** non impostato.<br/> | Nessun controllo. Usare [**SetFileAttributes**](/windows/desktop/api/FileAPI/nf-fileapi-setfileattributesa) per impostare .<br/>   |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Controllo di accesso](/windows/desktop/SecAuthZ/access-control)
</dt> <dt>

[**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea)
</dt> <dt>

[**Deviceiocontrol**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol)
</dt> <dt>

[**Costanti degli attributi di file**](file-attribute-constants.md)
</dt> <dt>

[Compressione e decompressione dei file](file-compression-and-decompression.md)
</dt> <dt>

[Crittografia file](file-encryption.md)
</dt> <dt>

[Funzioni di gestione file](file-management-functions.md)
</dt> <dt>

[Handle e oggetti](/windows/desktop/SysInfo/handles-and-objects)
</dt> <dt>

[Gestire l'ereditarietà](/windows/desktop/SysInfo/handle-inheritance)
</dt> <dt>

[Apertura di un file per la lettura o la scrittura](opening-a-file-for-reading-or-writing.md)
</dt> <dt>

[**SetFileAttributes**](/windows/desktop/api/FileAPI/nf-fileapi-setfileattributesa)
</dt> </dl>

 

