---
description: Considerazioni per la creazione o l'apertura di un file tramite la funzione CreateFile.
ms.assetid: 094cac29-c66d-409e-8928-878dc693d393
title: Creazione e apertura di file
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1430675862b10f9e9221d968242481525dc7632f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106316787"
---
# <a name="creating-and-opening-files"></a>Creazione e apertura di file

La funzione [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) può creare un nuovo file o aprire un file esistente. È necessario specificare il nome del file, le istruzioni per la creazione e altri attributi. Quando un'applicazione crea un nuovo file, il sistema operativo lo aggiunge alla directory specificata.

Il sistema operativo assegna un identificatore univoco, denominato *handle*, a ogni file aperto o creato mediante [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea). Un'applicazione può utilizzare questo handle con funzioni che leggono, scrivono e descrivono il file. È valido fino a quando non vengono chiusi tutti i riferimenti a tale handle. Quando un'applicazione viene avviata, eredita tutti gli handle aperti dal processo che lo ha avviato se gli handle sono stati creati come ereditabili.

Un'applicazione deve controllare il valore dell'handle restituito da [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) prima di provare a utilizzare l'handle per accedere al file. Se si verifica un errore, il valore dell'handle sarà un **\_ \_ valore di handle non valido** e l'applicazione potrà utilizzare la funzione [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) per ottenere informazioni estese sull'errore.

Quando in un'applicazione viene utilizzato [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea), è necessario utilizzare il parametro *dwDesiredAccess* per specificare se si intende leggere il file, scrivere nel file, sia in lettura che in scrittura o nessuno dei due. Questa operazione è nota come richiesta di una *modalità di accesso*. L'applicazione deve anche usare il parametro *dwCreationDisposition* per specificare l'azione da eseguire se il file esiste già, noto come la *disposizione di creazione*. Ad esempio, un'applicazione può chiamare **CreateFile** con *DwCreationDisposition* impostato su **Crea \_ sempre** per creare sempre un nuovo file, anche se esiste già un file con lo stesso nome, sovrascrivendo così il file esistente. L'esito positivo o negativo dipende da fattori quali gli attributi e le impostazioni di sicurezza del file precedente. per ulteriori informazioni, vedere le sezioni seguenti.

In un'applicazione viene inoltre utilizzato [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) per specificare se si desidera condividere il file per la lettura, la scrittura, entrambi o nessuno dei due. Questa operazione è nota come *modalità di condivisione*. Un file aperto che non è condiviso (*dwShareMode* impostato su zero) non può essere aperto nuovamente, dall'applicazione che lo ha aperto o da un'altra applicazione, finché il relativo handle non è stato chiuso. Questa operazione è detta anche accesso esclusivo.

Quando un processo utilizza [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) per tentare di aprire un file già aperto in modalità di condivisione (*dwShareMode* impostato su un valore diverso da zero valido), il sistema confronta le modalità di accesso e condivisione richieste con quelle specificate al momento dell'apertura del file. Se si specifica una modalità di accesso o condivisione che è in conflitto con le modalità specificate nella chiamata precedente, **CreateFile** ha esito negativo.

La tabella seguente illustra le combinazioni valide di due chiamate a [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) usando varie modalità di accesso e modalità di condivisione (*dwDesiredAccess*, *dwShareMode* rispettivamente). Non è importante l'ordine con cui vengono effettuate le chiamate **CreateFile** . Tuttavia, le successive operazioni di I/O dei file in ogni handle di file saranno comunque vincolate dalle modalità di accesso e condivisione correnti associate a tale handle di file specifico.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Prima chiamata a <a href="/windows/desktop/api/FileAPI/nf-fileapi-createfilea"> <strong>CreateFile</strong></a></th>
<th>Seconde valide chiamate a <a href="/windows/desktop/api/FileAPI/nf-fileapi-createfilea"> <strong>CreateFile</strong></a></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><strong>GENERIC_READ</strong>, <strong>FILE_SHARE_READ</strong><br/></td>
<td><ul>
<li><strong>GENERIC_READ</strong>, <strong>FILE_SHARE_READ</strong></li>
<li><strong>GENERIC_READ</strong>, <strong>FILE_SHARE_READ</strong>  |  <strong>FILE_SHARE_WRITE</strong></li>
</ul></td>
</tr>
<tr class="even">
<td><strong>GENERIC_READ</strong>, <strong>FILE_SHARE_WRITE</strong><br/></td>
<td><ul>
<li><strong>GENERIC_WRITE</strong>, <strong>FILE_SHARE_READ</strong></li>
<li><strong>GENERIC_WRITE</strong>, <strong>FILE_SHARE_READ</strong>  |  <strong>FILE_SHARE_WRITE</strong></li>
</ul></td>
</tr>
<tr class="odd">
<td><strong>GENERIC_READ</strong>, <strong>FILE_SHARE_READ</strong>  |  <strong>FILE_SHARE_WRITE</strong><br/></td>
<td><ul>
<li><strong>GENERIC_READ</strong>, <strong>FILE_SHARE_READ</strong></li>
<li><strong>GENERIC_READ</strong>, <strong>FILE_SHARE_READ</strong>  |  <strong>FILE_SHARE_WRITE</strong></li>
<li><strong>GENERIC_WRITE</strong>, <strong>FILE_SHARE_READ</strong></li>
<li><strong>GENERIC_WRITE</strong>, <strong>FILE_SHARE_READ</strong>  |  <strong>FILE_SHARE_WRITE</strong></li>
<li><strong>GENERIC_READ</strong>  |  <strong>GENERIC_WRITE</strong>, <strong>FILE_SHARE_READ</strong></li>
<li><strong>GENERIC_READ</strong>  |  <strong>GENERIC_WRITE</strong>, <strong>FILE_SHARE_READ</strong>  |  <strong>FILE_SHARE_WRITE</strong></li>
</ul></td>
</tr>
<tr class="even">
<td><strong>GENERIC_WRITE</strong>, <strong>FILE_SHARE_READ</strong><br/></td>
<td><ul>
<li><strong>GENERIC_READ</strong>, <strong>FILE_SHARE_WRITE</strong></li>
<li><strong>GENERIC_READ</strong>, <strong>FILE_SHARE_READ</strong>  |  <strong>FILE_SHARE_WRITE</strong></li>
</ul></td>
</tr>
<tr class="odd">
<td><strong>GENERIC_WRITE</strong>, <strong>FILE_SHARE_WRITE</strong><br/></td>
<td><ul>
<li><strong>GENERIC_WRITE</strong>, <strong>FILE_SHARE_WRITE</strong></li>
<li><strong>GENERIC_WRITE</strong>, <strong>FILE_SHARE_READ</strong>  |  <strong>FILE_SHARE_WRITE</strong></li>
</ul></td>
</tr>
<tr class="even">
<td><strong>GENERIC_WRITE</strong>, <strong>FILE_SHARE_READ</strong>  |  <strong>FILE_SHARE_WRITE</strong><br/></td>
<td><ul>
<li><strong>GENERIC_READ</strong>, <strong>FILE_SHARE_WRITE</strong></li>
<li><strong>GENERIC_READ</strong>, <strong>FILE_SHARE_READ</strong>  |  <strong>FILE_SHARE_WRITE</strong></li>
<li><strong>GENERIC_WRITE</strong>, <strong>FILE_SHARE_WRITE</strong></li>
<li><strong>GENERIC_WRITE</strong>, <strong>FILE_SHARE_READ</strong>  |  <strong>FILE_SHARE_WRITE</strong></li>
<li><strong>GENERIC_READ</strong>  |  <strong>GENERIC_WRITE</strong>, <strong>FILE_SHARE_WRITE</strong></li>
<li><strong>GENERIC_READ</strong>  |  <strong>GENERIC_WRITE</strong>, <strong>FILE_SHARE_READ</strong>  |  <strong>FILE_SHARE_WRITE</strong></li>
</ul></td>
</tr>
<tr class="odd">
<td><strong>GENERIC_READ</strong>  |  <strong>GENERIC_WRITE</strong>, <strong>FILE_SHARE_READ</strong><br/></td>
<td><ul>
<li><strong>GENERIC_READ</strong>, <strong>FILE_SHARE_READ</strong>  |  <strong>FILE_SHARE_WRITE</strong></li>
</ul></td>
</tr>
<tr class="even">
<td><strong>GENERIC_READ</strong>  |  <strong>GENERIC_WRITE</strong>, <strong>FILE_SHARE_WRITE</strong><br/></td>
<td><ul>
<li><strong>GENERIC_WRITE</strong>, <strong>FILE_SHARE_READ</strong>  |  <strong>FILE_SHARE_WRITE</strong></li>
</ul></td>
</tr>
<tr class="odd">
<td><strong>GENERIC_READ</strong>  |  <strong>GENERIC_WRITE</strong>, <strong>FILE_SHARE_READ</strong>  |  <strong>FILE_SHARE_WRITE</strong><br/></td>
<td><ul>
<li><strong>GENERIC_READ</strong>, <strong>FILE_SHARE_READ</strong>  |  <strong>FILE_SHARE_WRITE</strong></li>
<li><strong>GENERIC_WRITE</strong>, <strong>FILE_SHARE_READ</strong>  |  <strong>FILE_SHARE_WRITE</strong></li>
<li><strong>GENERIC_READ</strong>  |  <strong>GENERIC_WRITE</strong>, <strong>FILE_SHARE_READ</strong>  |  <strong>FILE_SHARE_WRITE</strong></li>
</ul></td>
</tr>
</tbody>
</table>



 

Oltre agli attributi di file standard, è anche possibile specificare attributi di sicurezza includendo un puntatore a una struttura di [**\_ attributi di sicurezza**](/previous-versions/windows/desktop/legacy/aa379560(v=vs.85)) come quarto parametro di [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea). Tuttavia, il file system sottostante deve supportare la protezione affinché questo abbia effetto (ad esempio, il file system NTFS lo supporta ma i vari file system FAT non). Per ulteriori informazioni sugli attributi di sicurezza, vedere [controllo di accesso](/windows/desktop/SecAuthZ/access-control).

Un'applicazione che crea un nuovo file può fornire un handle facoltativo a un file di modello, da cui [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) accetta attributi di file e attributi estesi per la creazione del nuovo file.

## <a name="createfile-scenarios"></a>Scenari di CreateFile

Esistono diversi scenari fondamentali per l'avvio dell'accesso a un file mediante la funzione [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) . Questi vengono riepilogati come segue:

-   Creazione di un nuovo file quando non esiste già un file con lo stesso nome.
-   Creazione di un nuovo file anche se esiste già un file con lo stesso nome, deselezionando i dati e iniziando vuoti.
-   Apertura di un file esistente solo se esistente e solo intatto.
-   Apertura di un file esistente solo se esistente, troncando il file in modo che sia vuoto.
-   L'apertura di un file è sempre: così com'è, se esiste, crearne una nuova se non esiste.

Questi scenari sono controllati dall'uso corretto del parametro *dwCreationDisposition* . Di seguito è riportata una suddivisione del modo in cui questi scenari eseguono il mapping ai valori per questo parametro e cosa accade quando vengono usati.

Quando si crea o si apre un nuovo file quando non esiste già un file con lo stesso nome (*dwCreationDisposition* impostato **su Crea \_ nuovo**, **Crea \_ sempre** o **Apri \_ sempre**), la funzione [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) esegue le azioni seguenti:

-   Combina gli attributi e i flag di file specificati da *dwFlagsAndAttributes* con l' **Archivio degli \_ attributi \_ di file**.
-   Imposta la lunghezza del file su zero.
-   Copia gli attributi estesi forniti dal file di modello nel nuovo file se è specificato il parametro *hTemplateFile* (esegue l'override di tutti i * flag *\_ attributo \_ \* _ file* specificati in precedenza).
-   Imposta il flag di ereditarietà specificato dal membro _ *bInheritHandle** e il descrittore di sicurezza specificato dal membro **LpSecurityDescriptor** del parametro *lpSecurityAttributes* (struttura degli [**\_ attributi di sicurezza**](/previous-versions/windows/desktop/legacy/aa379560(v=vs.85)) ), se specificato.

Quando si crea un nuovo file anche se esiste già un file con lo stesso nome (*dwCreationDisposition* impostato su **Create \_ Always**), la funzione [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) esegue le azioni seguenti:

-   Controlla gli attributi del file e le impostazioni di sicurezza correnti per l'accesso in scrittura, non riuscita se negato.
-   Combina gli attributi e i flag di file specificati da *dwFlagsAndAttributes* con l' **\_ \_ Archivio** degli attributi di file e gli attributi del file esistenti.
-   Imposta la lunghezza del file su zero (ovvero tutti i dati presenti nel file non sono più disponibili e il file è vuoto).
-   Copia gli attributi estesi forniti dal file di modello nel nuovo file se è specificato il parametro *hTemplateFile* (esegue l'override di tutti i * flag *\_ attributo \_ \* _ file* specificati in precedenza).
-   Imposta il flag di ereditarietà specificato dal membro _ *bInheritHandle** del parametro *lpSecurityAttributes* (struttura [**degli \_ attributi di sicurezza**](/previous-versions/windows/desktop/legacy/aa379560(v=vs.85)) ) se fornito, ma ignora il membro **lpSecurityDescriptor** della struttura **degli \_ attributi di sicurezza** .
-   Se ha esito positivo, ovvero [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) restituisce un handle valido, la chiamata a [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) produrrà l' **errore di codice \_ già \_ esistente**, anche se per questo particolare caso d'uso non si tratta effettivamente di un errore di questo tipo (se si intende creare un file "nuovo" (vuoto) al posto di quello esistente.

Quando si apre un file esistente (*dwCreationDisposition* impostato su **Apri \_ esistente**, **Apri \_ sempre** o **Tronca \_ esistente**), la funzione [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) esegue le azioni seguenti:

-   Verifica le impostazioni di sicurezza e gli attributi del file correnti per l'accesso richiesto, se negato.
-   Combina i flag di file (**\_ flag \_ \* di file* _) specificati da _dwFlagsAndAttributes * con gli attributi di file esistenti e ignora gli attributi di file (* * \_ attributo \_ \* file* _) specificati da _dwFlagsAndAttributes *.
-   Imposta la lunghezza del file su zero solo se *dwCreationDisposition* è impostato su **Truncate \_ esistente**, in caso contrario viene mantenuta la lunghezza del file corrente e il file viene aperto così com'è.
-   Ignora il parametro *hTemplateFile* .
-   Imposta il flag di ereditarietà specificato dal membro **bInheritHandle** del parametro *lpSecurityAttributes* (struttura [**degli \_ attributi di sicurezza**](/previous-versions/windows/desktop/legacy/aa379560(v=vs.85)) ) se fornito, ma ignora il membro **lpSecurityDescriptor** della struttura **degli \_ attributi di sicurezza** .

## <a name="file-attributes-and-directories"></a>Attributi e directory di file

Gli attributi di file fanno parte dei metadati associati a un file o a una directory, ciascuno con il proprio scopo e le relative regole su come può essere impostato e modificato. Alcuni di questi attributi sono validi solo per i file e solo per le directory. Ad esempio, l' **attributo \_ \_ directory attributo file** si applica solo alle directory: viene usato dal file System per determinare se un oggetto su disco è una directory, ma non può essere modificato per un oggetto file System esistente.

Alcuni attributi di file possono essere impostati per una directory, ma hanno un significato solo per i file creati in tale directory, agendo come attributi predefiniti. Ad esempio, **l' \_ attributo file \_ compresso** può essere impostato su un oggetto directory, ma poiché l'oggetto directory stesso non contiene dati effettivi, non è effettivamente compresso. Tuttavia, le directory contrassegnate con questo attributo indicano al file System di comprimere eventuali nuovi file aggiunti a tale directory. Qualsiasi attributo di file che può essere impostato in una directory e verrà impostato anche per i nuovi file aggiunti a tale directory viene definito *attributo ereditato*.

La funzione [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) fornisce un parametro per l'impostazione di determinati attributi di file quando viene creato un file. In generale, questi attributi sono i più comuni per un'applicazione da usare in fase di creazione dei file, ma non tutti i possibili attributi di file sono disponibili per **CreateFile**. Alcuni attributi di file richiedono l'uso di altre funzioni, ad esempio [**SetFileAttributes**](/windows/desktop/api/FileAPI/nf-fileapi-setfileattributesa), [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol)o [**DecryptFile**](/windows/desktop/api/WinBase/nf-winbase-decryptfilea) dopo che il file esiste già. Nel caso della **directory degli \_ attributi \_ di file**, la funzione [**CreateDirectory**](/windows/desktop/api/FileAPI/nf-fileapi-createdirectorya) è obbligatoria al momento della creazione perché **CreateFile** non è in grado di creare directory. Gli altri attributi di file che richiedono una gestione speciale sono i file di **\_ \_ reparse \_ Point** e di file **\_ \_ sparse \_** degli attributi file, che richiedono **DeviceIoControl**. Per ulteriori informazioni, vedere [**SetFileAttributes**](/windows/desktop/api/FileAPI/nf-fileapi-setfileattributesa).

Come indicato in precedenza, l'ereditarietà degli attributi di file si verifica quando viene creato un file con attributi di file letti dagli attributi di directory in cui si trova il file. Nella tabella seguente vengono riepilogati questi attributi ereditati e il modo in cui sono correlati alle funzionalità di [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) .



| Stato dell'attributo della directory                                      | Funzionalità di override dell'ereditarietà di [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) per i nuovi file      |
|----------------------------------------------------------------|-------------------------------------------------------------------------------------|
| **File \_ Set di attributi \_ compresso** .<br/>                | Nessun controllo. Usare [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) per cancellare.<br/>    |
| **File \_ ATTRIBUTO \_ compresso** non impostato.<br/>            | Nessun controllo. Usare [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) per impostare.<br/>      |
| **File \_ Set \_ crittografato con attributi** .<br/>                 | Nessun controllo. Usare [**DecryptFile**](/windows/desktop/api/WinBase/nf-winbase-decryptfilea).<br/>                      |
| **File \_ L'attributo \_ crittografato** non è impostato.<br/>             | Può essere impostato utilizzando [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea).<br/>                       |
| **File \_ ATTRIBUTO \_ non impostato come \_ contenuto \_ indicizzato** .<br/>     | Nessun controllo. Usare [**SetFileAttributes**](/windows/desktop/api/FileAPI/nf-fileapi-setfileattributesa) per cancellare.<br/> |
| **File \_ ATTRIBUTO \_ senza \_ contenuto \_ indicizzato** non impostato.<br/> | Nessun controllo. Usare [**SetFileAttributes**](/windows/desktop/api/FileAPI/nf-fileapi-setfileattributesa) per impostare.<br/>   |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Controllo di accesso](/windows/desktop/SecAuthZ/access-control)
</dt> <dt>

[**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea)
</dt> <dt>

[**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol)
</dt> <dt>

[**Costanti di attributi file**](file-attribute-constants.md)
</dt> <dt>

[Compressione e decompressione dei file](file-compression-and-decompression.md)
</dt> <dt>

[Crittografia file](file-encryption.md)
</dt> <dt>

[Funzioni di gestione file](file-management-functions.md)
</dt> <dt>

[Handle e oggetti](/windows/desktop/SysInfo/handles-and-objects)
</dt> <dt>

[Gestisci ereditarietà](/windows/desktop/SysInfo/handle-inheritance)
</dt> <dt>

[Apertura di un file per la lettura o la scrittura](opening-a-file-for-reading-or-writing.md)
</dt> <dt>

[**SetFileAttributes**](/windows/desktop/api/FileAPI/nf-fileapi-setfileattributesa)
</dt> </dl>

 

