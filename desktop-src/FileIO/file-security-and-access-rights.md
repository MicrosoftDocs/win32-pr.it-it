---
description: Poiché i file sono oggetti a protezione diretta, l'accesso viene regolato dal modello di controllo di accesso che regola l'accesso a tutti gli altri oggetti a protezione diretta di Windows.
ms.assetid: 991d7d94-fae7-406f-b2e3-dee811279366
title: Sicurezza file e diritti di accesso
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b161dd78c7585cf6de2781d7339787a22bde95dc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106310023"
---
# <a name="file-security-and-access-rights"></a>Sicurezza file e diritti di accesso

Poiché i file sono [oggetti a protezione diretta](/windows/desktop/SecAuthZ/securable-objects), l'accesso viene regolato dal modello di controllo di accesso che regola l'accesso a tutti gli altri oggetti a protezione diretta di Windows. Per una spiegazione dettagliata di questo modello, vedere [Access Control](/windows/desktop/SecAuthZ/access-control).

È possibile specificare un [descrittore di sicurezza](/windows/desktop/api/winnt/ns-winnt-security_descriptor) per un file o una directory quando si chiama la funzione [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea), [**CreateDirectory**](/windows/desktop/api/FileAPI/nf-fileapi-createdirectorya)o [**CreateDirectoryEx**](/windows/desktop/api/WinBase/nf-winbase-createdirectoryexa) . Se si specifica **null** per il parametro *lpSecurityAttributes* , il file o la directory ottiene un descrittore di sicurezza predefinito. Gli elenchi di controllo di accesso (ACL) nel descrittore di sicurezza predefinito per un file o una directory vengono ereditati dalla relativa directory padre. Si noti che un descrittore di sicurezza predefinito viene assegnato solo quando viene appena creato un file o una directory e non quando viene rinominato o spostato.

Per recuperare il descrittore di sicurezza di un oggetto file o directory, chiamare la funzione [**GetNamedSecurityInfo**](/windows/desktop/api/aclapi/nf-aclapi-getnamedsecurityinfoa) o [**GetSecurityInfo**](/windows/desktop/api/aclapi/nf-aclapi-getsecurityinfo) . Per modificare il descrittore di sicurezza di un oggetto file o directory, chiamare la funzione [**SetNamedSecurityInfo**](/windows/desktop/api/aclapi/nf-aclapi-setnamedsecurityinfoa) o [**SetSecurityInfo**](/windows/desktop/api/aclapi/nf-aclapi-setsecurityinfo) .

I diritti di accesso validi per file e directory includono **l'eliminazione**, il **\_ controllo di lettura**, la scrittura dell' **\_ applicazione livello dati**, la scrittura del **\_ proprietario** e la **sincronizzazione** [dei diritti di accesso standard](/windows/desktop/SecAuthZ/standard-access-rights). La tabella nelle [**costanti dei diritti di accesso ai file**](file-access-rights-constants.md) elenca i diritti di accesso specifici per i file e le directory.

Sebbene il diritto di accesso **sincronizzato** venga definito nell'elenco [dei diritti di accesso standard](/windows/desktop/SecAuthZ/standard-access-rights) come diritto di specificare un handle di file in una delle funzioni di attesa, quando si usano operazioni di I/O di file asincrone è necessario attendere l'handle di evento contenuto in una struttura [**sovrapposta**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) configurata correttamente invece di usare l'handle di file con il diritto di accesso **Synchronize** per la sincronizzazione.

Di seguito sono indicati i [diritti di accesso generici](/windows/desktop/SecAuthZ/generic-access-rights) per file e directory.



<table>
<thead>
<tr class="header">
<th>Diritto di accesso</th>
<th>Descrizione</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><strong>FILE_GENERIC_EXECUTE</strong></td>
<td><dl> <strong>FILE_EXECUTE</strong><br />
<strong>FILE_READ_ATTRIBUTES</strong><br />
<strong>STANDARD_RIGHTS_EXECUTE</strong><br />
<strong>SINCRONIZZARE</strong><br />
</dl></td>
</tr>
<tr class="even">
<td><strong>FILE_GENERIC_READ</strong></td>
<td><dl> <strong>FILE_READ_ATTRIBUTES</strong><br />
<strong>FILE_READ_DATA</strong><br />
<strong>FILE_READ_EA</strong><br />
<strong>STANDARD_RIGHTS_READ</strong><br />
<strong>SINCRONIZZARE</strong><br />
</dl></td>
</tr>
<tr class="odd">
<td><strong>FILE_GENERIC_WRITE</strong></td>
<td><dl> <strong>FILE_APPEND_DATA</strong><br />
<strong>FILE_WRITE_ATTRIBUTES</strong><br />
<strong>FILE_WRITE_DATA</strong><br />
<strong>FILE_WRITE_EA</strong><br />
<strong>STANDARD_RIGHTS_WRITE</strong><br />
<strong>SINCRONIZZARE</strong><br />
</dl></td>
</tr>
</tbody>
</table>



 

Windows confronta i diritti di accesso richiesti e le informazioni contenute nel token di accesso del thread con le informazioni contenute nel descrittore di sicurezza dell'oggetto file o directory. Se il confronto non impedisce la concessione di tutti i diritti di accesso richiesti, al thread viene restituito un handle per l'oggetto e vengono concessi i diritti di accesso. Per ulteriori informazioni su questo processo, vedere [interazione tra thread e oggetti a protezione diretta](/windows/desktop/SecAuthZ/interaction-between-threads-and-securable-objects).

Per impostazione predefinita, l'autorizzazione per l'accesso a un file o a una directory viene controllata esclusivamente dagli ACL nel descrittore di sicurezza associato a tale file o directory. In particolare, il descrittore di sicurezza di una directory padre non viene utilizzato per controllare l'accesso a un file o a una directory figlio. Il [diritto di accesso](/windows/desktop/SecAuthZ/access-rights-and-access-masks) all' **\_ attraversamento file** può essere applicato rimuovendo il [privilegio](/windows/desktop/SecAuthZ/privileges) **Ignora \_ \_ controllo incrociato** dagli utenti. Questa operazione non è consigliata nel caso generale, in quanto molti programmi non gestiscono correttamente gli errori di attraversamento delle directory. L'uso principale per l'accesso ai file direttamente nelle directory consiste nell'abilitare la conformità a determinati standard POSIX IEEE e ISO quando l'interoperabilità con i sistemi UNIX è un requisito. **\_**

Il modello di sicurezza di Windows consente a una directory figlio di ereditare o di impedire l'ereditarietà di una o più voci ACE nel descrittore di sicurezza della directory padre. Ogni voce ACE contiene informazioni che determinano come ereditarle e se avranno effetto sull'oggetto directory che eredita. Ad esempio, alcune voci ACE ereditate controllano l'accesso all'oggetto directory ereditato e sono chiamate *voci ACE effettive*. Tutte le altre voci ACE sono denominate *ACE con solo ereditarietà*.

Il modello di sicurezza di Windows applica anche l'ereditarietà automatica delle voci ACE agli oggetti figlio in base alle [regole di ereditarietà Ace](/windows/desktop/SecAuthZ/ace-inheritance-rules). Questa ereditarietà automatica, insieme alle informazioni sull'ereditarietà in ogni voce ACE, determina il modo in cui le restrizioni di sicurezza vengono passate alla gerarchia di directory.

Si noti che non è possibile usare una voce ACE con accesso negato per negare solo l'accesso **generico in \_ lettura** o in **\_ scrittura generico** a un file. Ciò è dovuto al fatto che per gli oggetti file, i mapping generici per la scrittura **generica o \_** **generica \_** includono il diritto di accesso **Synchronize** . Se una voce ACE nega l'accesso in **\_ scrittura generico** a un trustee e il trustee richiede l'accesso in **\_ lettura generico** , la richiesta avrà esito negativo perché la richiesta include in modo implicito l'accesso **Synchronize** , che viene negato in modo implicito dalla voce ACE e viceversa. Invece di usare le voci ACE con accesso negato, usare le voci ACE consentite per consentire esplicitamente i diritti di accesso consentiti.

Un altro mezzo per gestire l'accesso agli oggetti di archiviazione è la crittografia. L'implementazione di file system crittografia in Windows è il file system crittografato o EFS. EFS crittografa solo i file e non le directory. Il vantaggio della crittografia è che fornisce protezione aggiuntiva ai file applicati sui supporti e non tramite il file system e l'architettura standard di controllo di accesso di Windows. Per ulteriori informazioni sulla crittografia dei file, vedere [crittografia dei file](file-encryption.md).

Nella maggior parte dei casi, la possibilità di leggere e scrivere le impostazioni di sicurezza di un oggetto file o directory è limitata ai processi in modalità kernel. Ovviamente, non si vuole che un processo utente possa modificare la proprietà o la restrizione di accesso nel file o nella directory privata. Tuttavia, un'applicazione di backup non è in grado di completare il processo di backup del file se le restrizioni di accesso immesse nel file o nella directory non consentono al processo in modalità utente dell'applicazione di leggerlo. Le applicazioni di backup devono essere in grado di eseguire l'override delle impostazioni di sicurezza degli oggetti file e directory per garantire un backup completo. Analogamente, se un'applicazione di backup tenta di scrivere una copia di backup del file tramite la copia del disco residente e si nega in modo esplicito i privilegi di scrittura al processo dell'applicazione di backup, non è possibile completare l'operazione di ripristino. In questo caso, inoltre, l'applicazione di backup deve essere in grado di sostituire le impostazioni di controllo di accesso del file.

Il **\_ \_ nome del backup se** e i privilegi di accesso per il **\_ \_ nome del ripristino** sono stati creati appositamente per offrire la possibilità di eseguire il backup delle applicazioni. Se questi privilegi sono stati concessi e abilitati nel token di accesso del processo dell'applicazione di backup, è possibile chiamare [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) per aprire il file o la directory per il backup, specificando il diritto di accesso al **\_ controllo di lettura** standard come valore del parametro *dwDesiredAccess* . Tuttavia, per identificare il processo chiamante come processo di backup, è necessario che la chiamata a **CreateFile** includa il flag di **\_ \_ \_ semantica di backup del flag file** nel parametro *dwFlagsAndAttributes* . La sintassi completa della chiamata di funzione è la seguente:


```C++
HANDLE hFile = CreateFile( fileName,                   // lpFileName
                           READ_CONTROL,               // dwDesiredAccess
                           0,                          // dwShareMode
                           NULL,                       // lpSecurityAttributes
                           OPEN_EXISTING,              // dwCreationDisposition
                           FILE_FLAG_BACKUP_SEMANTICS, // dwFlagsAndAttributes
                           NULL );                     // hTemplateFile
```



Questo consentirà al processo dell'applicazione di backup di aprire il file ed eseguire l'override del controllo di sicurezza standard. Per ripristinare il file, l'applicazione di backup utilizzerà la sintassi di chiamata [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) seguente all'apertura del file da scrivere.


```C++
HANDLE hFile = CreateFile( fileName,                   // lpFileName
                           WRITE_OWNER | WRITE_DAC,    // dwDesiredAccess
                           0,                          // dwShareMode
                           NULL,                       // lpSecurityAttributes
                           CREATE_ALWAYS,              // dwCreationDisposition
                           FILE_FLAG_BACKUP_SEMANTICS, // dwFlagsAndAttributes
                           NULL );                     // hTemplateFile
```



In alcune situazioni, un'applicazione di backup deve essere in grado di modificare le impostazioni di controllo di accesso di un file o di una directory. Un esempio è quando le impostazioni di controllo di accesso della copia del disco residente di un file o di una directory sono diverse dalla copia di backup. Questo problema si verifica se queste impostazioni sono state modificate dopo il backup del file o della directory o se sono state danneggiate.

Il flag per la **\_ \_ \_ semantica di backup del flag file** specificato nella chiamata a [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) consente all'applicazione di backup di leggere le impostazioni di controllo di accesso del file o della directory. Con questa autorizzazione, il processo dell'applicazione di backup può quindi chiamare [**GetKernelObjectSecurity**](/windows/desktop/api/securitybaseapi/nf-securitybaseapi-getkernelobjectsecurity) e [**SetKernelObjectSecurity**](/windows/desktop/api/securitybaseapi/nf-securitybaseapi-setkernelobjectsecurity) per la lettura e la reimpostazione delle impostazioni di controllo di accesso.

Se un'applicazione di backup deve avere accesso alle [impostazioni di controllo di accesso](/windows/desktop/SecAuthZ/access-control-lists)a livello di sistema, il flag di **\_ \_ sicurezza del sistema di accesso** deve essere specificato nel valore del parametro *dwDesiredAccess* passato a [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea).

Le applicazioni di backup chiamano [**BackupRead**](/windows/desktop/api/winbase/nf-winbase-backupread) per leggere i file e le directory specificati per l'operazione di ripristino e [**BackupWrite**](/windows/desktop/api/winbase/nf-winbase-backupwrite) per scriverli.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[diritti di accesso standard](/windows/desktop/SecAuthZ/standard-access-rights)
</dt> </dl>

 

 
