---
description: Poiché i file sono oggetti a protezione diretta, l'accesso a essi è regolamentato dal modello di controllo di accesso che regola l'accesso a tutti gli altri oggetti a protezione diretta in Windows.
ms.assetid: 991d7d94-fae7-406f-b2e3-dee811279366
title: Sicurezza dei file e diritti di accesso
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4c2f33df8117debef1d7f8349ae2fb479974e59ec582d7be758a753726706b9b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119696251"
---
# <a name="file-security-and-access-rights"></a>Sicurezza dei file e diritti di accesso

Poiché i file [sono oggetti a](/windows/desktop/SecAuthZ/securable-objects)protezione diretta, l'accesso a essi è regolamentato dal modello di controllo di accesso che regola l'accesso a tutti gli altri oggetti a protezione diretta in Windows. Per una spiegazione dettagliata di questo modello, vedere Controllo [di accesso](/windows/desktop/SecAuthZ/access-control).

È possibile specificare un [descrittore di sicurezza](/windows/desktop/api/winnt/ns-winnt-security_descriptor) per un file o una directory quando si chiama la [**funzione CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea), [**CreateDirectory**](/windows/desktop/api/FileAPI/nf-fileapi-createdirectorya)o [**CreateDirectoryEx.**](/windows/desktop/api/WinBase/nf-winbase-createdirectoryexa) Se si specifica **NULL** per il *parametro lpSecurityAttributes,* il file o la directory ottiene un descrittore di sicurezza predefinito. Gli elenchi di controllo di accesso (ACL) nel descrittore di sicurezza predefinito per un file o una directory vengono ereditati dalla directory padre. Si noti che un descrittore di sicurezza predefinito viene assegnato solo quando un file o una directory viene appena creato e non quando viene rinominato o spostato.

Per recuperare il descrittore di sicurezza di un oggetto file o directory, chiamare la [**funzione GetNamedSecurityInfo**](/windows/desktop/api/aclapi/nf-aclapi-getnamedsecurityinfoa) [**o GetSecurityInfo.**](/windows/desktop/api/aclapi/nf-aclapi-getsecurityinfo) Per modificare il descrittore di sicurezza di un oggetto file o directory, chiamare la [**funzione SetNamedSecurityInfo**](/windows/desktop/api/aclapi/nf-aclapi-setnamedsecurityinfoa) [**o SetSecurityInfo.**](/windows/desktop/api/aclapi/nf-aclapi-setsecurityinfo)

I diritti di accesso validi per file e directory includono i diritti di accesso [standard](/windows/desktop/SecAuthZ/standard-access-rights) **DELETE**, **READ \_ CONTROL**, **WRITE \_ DAC**, **WRITE \_ OWNER** e **SYNCHRONIZE** . La tabella in [**Costanti dei diritti di accesso**](file-access-rights-constants.md) ai file elenca i diritti di accesso specifici per file e directory.

Anche se il diritto di accesso **SYNCHRONIZE** è definito nell'elenco dei diritti di accesso [standard](/windows/desktop/SecAuthZ/standard-access-rights) come diritto per specificare un handle di file in una delle funzioni di attesa, quando si usano operazioni di I/O di file asincrone è necessario attendere l'handle di evento contenuto in una struttura [**OVERLAPPED**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) configurata correttamente anziché usare l'handle di file con il diritto di accesso **SYNCHRONIZE** per la sincronizzazione.

Di seguito sono riportati i [diritti di accesso generici](/windows/desktop/SecAuthZ/generic-access-rights) per file e directory.



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
<strong>Sincronizzare</strong><br />
</dl></td>
</tr>
<tr class="even">
<td><strong>FILE_GENERIC_READ</strong></td>
<td><dl> <strong>FILE_READ_ATTRIBUTES</strong><br />
<strong>FILE_READ_DATA</strong><br />
<strong>FILE_READ_EA</strong><br />
<strong>STANDARD_RIGHTS_READ</strong><br />
<strong>Sincronizzare</strong><br />
</dl></td>
</tr>
<tr class="odd">
<td><strong>FILE_GENERIC_WRITE</strong></td>
<td><dl> <strong>FILE_APPEND_DATA</strong><br />
<strong>FILE_WRITE_ATTRIBUTES</strong><br />
<strong>FILE_WRITE_DATA</strong><br />
<strong>FILE_WRITE_EA</strong><br />
<strong>STANDARD_RIGHTS_WRITE</strong><br />
<strong>Sincronizzare</strong><br />
</dl></td>
</tr>
</tbody>
</table>



 

Windows confronta i diritti di accesso richiesti e le informazioni nel token di accesso del thread con le informazioni nel descrittore di sicurezza dell'oggetto file o directory. Se il confronto non impedisce la concessione di tutti i diritti di accesso richiesti, viene restituito un handle per l'oggetto al thread e vengono concessi i diritti di accesso. Per altre informazioni su questo processo, vedere [Interazione tra thread e oggetti a protezione diretta](/windows/desktop/SecAuthZ/interaction-between-threads-and-securable-objects).

Per impostazione predefinita, l'autorizzazione per l'accesso a un file o a una directory è controllata esclusivamente dagli ACL nel descrittore di sicurezza associato a tale file o directory. In particolare, il descrittore di sicurezza di una directory padre non viene usato per controllare l'accesso a qualsiasi file o directory figlio. Il **diritto di accesso FILE \_ TRAVERSE** [può](/windows/desktop/SecAuthZ/access-rights-and-access-masks) essere applicato rimuovendo il **privilegio BYPASS \_ TRAVERSE \_ CHECKING** [dagli](/windows/desktop/SecAuthZ/privileges) utenti. Questa operazione non è consigliata in generale, perché molti programmi non gestiscono correttamente gli errori di attraversamento della directory. L'uso principale del diritto di accesso **\_ FILE TRAVERSE** nelle directory è quello di abilitare la conformità a determinati standard IEEE e ISO POSIX quando l'interoperabilità con i sistemi Unix è un requisito.

Il Windows di sicurezza consente a una directory figlio di ereditare o impedire l'ereditarietà di una o più voci ACE nel descrittore di sicurezza della directory padre. Ogni ACE contiene informazioni che determinano come può essere ereditata e se avrà effetto sull'oggetto directory che eredita. Ad esempio, alcune voci di controllo di accesso ereditate controllano l'accesso all'oggetto directory ereditato, chiamate *ACE effettive.* Tutte le altre ACE sono denominate *ACE di sola ereditarietà.*

Il Windows di sicurezza applica anche l'ereditarietà automatica delle voci di controllo di accesso agli oggetti figlio in base alle regole [di ereditarietà ACE.](/windows/desktop/SecAuthZ/ace-inheritance-rules) Questa ereditarietà automatica, insieme alle informazioni sull'ereditarietà in ogni ACE, determina il modo in cui le restrizioni di sicurezza vengono passate nella gerarchia di directory.

Si noti che non è possibile usare una ACE negata dall'accesso per negare solo l'accesso **GENERIC \_ READ** o **GENERIC \_ WRITE** a un file. Questo perché per gli oggetti file, i mapping generici per **GENERIC \_ READ** o **GENERIC \_ WRITE** includono il diritto di accesso **SYNCHRONIZE.** Se una ACE nega l'accesso **\_ GENERIC WRITE** a un trustee il trustee richiede l'accesso GENERIC **\_ READ,** la richiesta avrà esito negativo perché la richiesta include in modo implicito l'accesso **SYNCHRONIZE,** che viene negato in modo implicito dalla ACE e viceversa. Invece di usare le ACE negate di accesso, usare le ACE consentite per consentire in modo esplicito i diritti di accesso consentiti.

Un altro modo per gestire l'accesso agli oggetti di archiviazione è la crittografia. L'implementazione file system crittografia Windows è il file system crittografato o EFS. EFS crittografa solo i file e non le directory. Il vantaggio della crittografia è che offre protezione aggiuntiva ai file applicati ai supporti e non tramite il file system e l'architettura di controllo di accesso Windows standard. Per altre informazioni sulla crittografia dei file, vedere [Crittografia file](file-encryption.md).

Nella maggior parte dei casi, la possibilità di leggere e scrivere le impostazioni di sicurezza di un oggetto file o directory è limitata ai processi in modalità kernel. Ovviamente, non si vuole che un processo utente sia in grado di modificare la proprietà o la restrizione di accesso per il file o la directory privata. Tuttavia, un'applicazione di backup non sarebbe in grado di completare il processo di backup del file se le restrizioni di accesso applicate al file o alla directory non consentono al processo in modalità utente dell'applicazione di leggerlo. Le applicazioni di backup devono essere in grado di eseguire l'override delle impostazioni di sicurezza degli oggetti file e directory per garantire un backup completo. Analogamente, se un'applicazione di backup tenta di scrivere una copia di backup del file sulla copia residente su disco e si negano esplicitamente privilegi di scrittura al processo dell'applicazione di backup, l'operazione di ripristino non può essere completata. Anche in questo caso, l'applicazione di backup deve essere in grado di eseguire l'override delle impostazioni di controllo di accesso del file.

I **edizione Standard \_ BACKUP \_ NAME** **e edizione Standard \_ di \_** accesso RESTORE NAME sono stati creati in modo specifico per offrire questa possibilità di eseguire il backup delle applicazioni. Se questi privilegi sono stati concessi e abilitati nel token di accesso del processo dell'applicazione di backup, è possibile chiamare [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) per aprire il file o la directory per il backup, specificando il diritto di accesso **READ \_ CONTROL** standard come valore del *parametro dwDesiredAccess.* Tuttavia, per identificare il processo chiamante come processo di backup, la chiamata a **CreateFile** deve includere il flag **FILE FLAG BACKUP \_ \_ \_ SEMANTICS** nel *parametro dwFlagsAndAttributes.* La sintassi completa della chiamata di funzione è la seguente:


```C++
HANDLE hFile = CreateFile( fileName,                   // lpFileName
                           READ_CONTROL,               // dwDesiredAccess
                           0,                          // dwShareMode
                           NULL,                       // lpSecurityAttributes
                           OPEN_EXISTING,              // dwCreationDisposition
                           FILE_FLAG_BACKUP_SEMANTICS, // dwFlagsAndAttributes
                           NULL );                     // hTemplateFile
```



In questo modo il processo dell'applicazione di backup aprirà il file ed eseguirà l'override del controllo di sicurezza standard. Per ripristinare il file, l'applicazione di backup userebbe la sintassi di [**chiamata CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) seguente quando si apre il file da scrivere.


```C++
HANDLE hFile = CreateFile( fileName,                   // lpFileName
                           WRITE_OWNER | WRITE_DAC,    // dwDesiredAccess
                           0,                          // dwShareMode
                           NULL,                       // lpSecurityAttributes
                           CREATE_ALWAYS,              // dwCreationDisposition
                           FILE_FLAG_BACKUP_SEMANTICS, // dwFlagsAndAttributes
                           NULL );                     // hTemplateFile
```



In alcuni casi un'applicazione di backup deve essere in grado di modificare le impostazioni di controllo di accesso di un file o di una directory. Un esempio è quando le impostazioni di controllo di accesso della copia residente su disco di un file o di una directory sono diverse dalla copia di backup. Ciò si verifica se queste impostazioni sono state modificate dopo il backup del file o della directory o se è stato danneggiato.

Il flag **FILE \_ FLAG BACKUP \_ \_ SEMANTICS** specificato nella chiamata a [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) concede all'applicazione di backup l'autorizzazione per leggere le impostazioni di controllo di accesso del file o della directory. Con questa autorizzazione, il processo dell'applicazione di backup può quindi chiamare [**GetKernelObjectSecurity**](/windows/desktop/api/securitybaseapi/nf-securitybaseapi-getkernelobjectsecurity) e [**SetKernelObjectSecurity**](/windows/desktop/api/securitybaseapi/nf-securitybaseapi-setkernelobjectsecurity) per leggere e reimpostare le impostazioni di controllo di accesso.

Se un'applicazione di backup deve avere accesso alle impostazioni di controllo di accesso a livello di [sistema,](/windows/desktop/SecAuthZ/access-control-lists)è necessario specificare il flag **ACCESS SYSTEM \_ \_ SECURITY** nel valore del parametro *dwDesiredAccess* passato a [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea).

Le applicazioni di [**backup chiamano BackupRead**](/windows/desktop/api/winbase/nf-winbase-backupread) per leggere i file e le directory specificati per l'operazione di ripristino e [**BackupWrite**](/windows/desktop/api/winbase/nf-winbase-backupwrite) per scriverli.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[diritti di accesso standard](/windows/desktop/SecAuthZ/standard-access-rights)
</dt> </dl>

 

 
