---
description: 'Il registro eventi contiene i log standard seguenti, nonché i log personalizzati:'
ms.assetid: 87d860e3-2495-4e15-bb42-341e92935e55
title: Chiave EventLog
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6965c850dd31ab722786cf4da41c7d3a67f5d980
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103755658"
---
# <a name="eventlog-key"></a>Chiave EventLog

Il registro eventi contiene i log standard seguenti, nonché i log personalizzati:



| Registro             | Descrizione                                                                                                                                                                                                                                  |
|-----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Applicazione** | Contiene gli eventi registrati dalle applicazioni. Ad esempio, un'applicazione di database potrebbe registrare un errore di file. Lo sviluppatore di applicazioni decide gli eventi da registrare.                                                                             |
| **Sicurezza**    | Contiene eventi quali i tentativi di accesso validi e non validi, nonché gli eventi correlati all'utilizzo delle risorse, ad esempio la creazione, l'apertura o l'eliminazione di file o altri oggetti. Un amministratore può avviare il controllo per registrare gli eventi nel registro di sicurezza. |
| **Sistema**      | Contiene gli eventi registrati dai componenti di sistema, ad esempio l'errore di un driver o di un altro componente di sistema da caricare durante l'avvio.                                                                                                               |
| *CustomLog*     | Contiene eventi registrati da applicazioni che creano un log personalizzato. L'utilizzo di un log personalizzato consente a un'applicazione di controllare le dimensioni del log o di alleghi ACL per motivi di sicurezza senza influire sulle altre applicazioni.                         |



 

Il servizio di registrazione eventi utilizza le informazioni archiviate nella chiave del registro di sistema **EventLog** . La chiave **EventLog** contiene diverse sottochiavi, denominate *log*. Ogni log contiene informazioni utilizzate dal servizio di registrazione eventi per individuare le risorse quando un'applicazione scrive e legge dal registro eventi.

La struttura della chiave **EventLog** è la seguente:

```
HKEY_LOCAL_MACHINE
   SYSTEM
      CurrentControlSet
         Services
            Eventlog
               Application
               Security
               System
               CustomLog
```

Si noti che i controller di dominio registrano gli eventi nei log del **servizio directory** e del **servizio Replica file** e i server DNS registrano gli eventi nel **server DNS**.

Ogni log può contenere i seguenti valori del registro di sistema.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Valore del Registro di sistema</th>
<th>Descrizione</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><strong>CustomSD</strong></td>
<td>Limita l'accesso al registro eventi. Questo valore è di tipo REG_SZ. Il formato utilizzato è SDDL ( <a href="/windows/desktop/SecAuthZ/security-descriptor-definition-language">Security Descriptor Definition Language</a> ). Costruire un ACL che conceda uno o più dei seguenti diritti:<dl> Cancella (0x0004)<br />
Lettura (0x0001)<br />
Scrittura (0x0002)<br />
</dl> Per essere un SDDL sintatticamente valido, il valore di Dogad deve specificare un proprietario e un proprietario del gruppo (ad esempio, O:BAG: SY), ma il proprietario e il proprietario del gruppo non vengono usati. Se CustomSd è impostato su un valore errato, viene generato un evento nel registro eventi di sistema all'avvio del servizio Registro eventi e il registro eventi ottiene un descrittore di sicurezza predefinito identico al valore originale di CustomS per il registro applicazioni. SACL non supportati.<br/> Per ulteriori informazioni, vedere <a href="event-logging-security.md">sicurezza della registrazione degli eventi</a>.<br/> <strong>Windows Server 2003:</strong> Gli elenchi SACL sono supportati.<br/> <strong>Windows XP/2000:</strong> Questo valore non è supportato.<br/> <br/></td>
</tr>
<tr class="even">
<td><strong>DisplayNameFile</strong></td>
<td>Questo valore non viene utilizzato. <strong>Windows Server 2003 e Windows XP/2000:  </strong> Nome del file in cui è archiviato il nome localizzato del log eventi. Il nome archiviato in questo file viene visualizzato come nome del registro in Visualizzatore eventi. Se questa voce non viene visualizzata nel registro di sistema per un registro eventi, Visualizzatore eventi Visualizza il nome della sottochiave del registro di sistema come nome del registro. Questo valore è di tipo REG_EXPAND_SZ. Il valore predefinito è% SystemRoot% \system32\els.dll.<br/></td>
</tr>
<tr class="odd">
<td><strong>DisplayNameID</strong></td>
<td>Questo valore non viene utilizzato. <strong>Windows Server 2003 e Windows XP/2000:  </strong> Numero di identificazione del messaggio della stringa del nome del log. Questo numero indica il messaggio in cui viene visualizzato il nome visualizzato localizzato. Il messaggio viene archiviato nel file specificato dal valore <strong>DisplayNameFile</strong> . Questo valore è di tipo REG_DWORD.<br/></td>
</tr>
<tr class="even">
<td><strong>File</strong></td>
<td>Percorso completo del file in cui è archiviato ogni registro eventi. Questo consente a Visualizzatore eventi e ad altre applicazioni di trovare i file di log. Questo valore è di tipo REG_SZ o REG_EXPAND_SZ. Questo valore è facoltativo. Se il valore non è specificato, il valore predefinito è%SystemRoot%\system32\winevt\logs\ seguito da un nome di file basato sul nome della chiave del registro di sistema del registro eventi. Il percorso specifico del file di registro eventi deve essere impostato tramite l'utilità della riga di comando wevtutil.exe o tramite la funzione <a href="/windows/desktop/api/winevt/nf-winevt-evtsetchannelconfigproperty"><strong>EvtSetChannelConfigProperty</strong></a> con EvtChannelLoggingConfigLogFilePath passato nel parametro <em>PropertyId</em> .<br/> Se è stato impostato un file specifico, assicurarsi che il servizio Registro eventi disponga di autorizzazioni complete per il file.<br/> Questo valore deve essere un nome file valido per un file che si trova in una directory locale (non un computer remoto, non un dispositivo DOS, non un floppy e non una pipe). Se l'impostazione del file non è corretta, viene generato un evento nel registro eventi di sistema all'avvio del servizio Registro eventi.<br/> Non utilizzare variabili di ambiente, nel percorso del file, che non possono essere espanse nel contesto del servizio Registro eventi.<br/> <strong>Windows Server 2003 e Windows XP/2000:</strong> Per impostazione predefinita, questo valore è%SystemRoot%\system32\config\ seguito da un nome di file basato sul nome della chiave del registro di sistema del registro eventi. Se l'impostazione del file è impostata su un valore non valido, il log non verrà inizializzato correttamente o tutte le richieste passeranno automaticamente al log predefinito (applicazione).<br/></td>
</tr>
<tr class="odd">
<td><strong>MaxSize</strong></td>
<td>Dimensione massima, in byte, del file di log. Questo valore è di tipo REG_DWORD. Il valore deve essere impostato su un multiplo di 64K per un registro di sistema, un'applicazione o una sicurezza. Il valore predefinito è 1 MB. <strong>Windows Server 2003 e Windows XP/2000:</strong> Il valore è limitato a 0xFFFFFFFF e il valore predefinito è 512K.<br/></td>
</tr>
<tr class="even">
<td><strong>PrimaryModule</strong></td>
<td>Questo valore non viene utilizzato. <strong>Windows Server 2003 e Windows XP/2000:</strong> Questo valore è il nome della sottochiave che contiene i valori predefiniti per le voci nella sottochiave per l'origine evento. Questo valore è di tipo REG_SZ.<br/></td>
</tr>
<tr class="odd">
<td><strong>Conservazione</strong></td>
<td>Questo valore è di tipo REG_DWORD. Il valore predefinito è 0. Se questo valore è 0, i record degli eventi vengono sempre sovrascritti. Se questo valore è 0xFFFFFFFF o un valore diverso da zero, i record non vengono mai sovrascritti. Quando il file di log raggiunge le dimensioni massime, è necessario cancellare il registro manualmente; in caso contrario, i nuovi eventi vengono rimossi. Prima di poter modificare le dimensioni, è necessario cancellare anche il log. <strong>Windows Server 2003 e Windows XP/2000:  </strong> Questo valore è l'intervallo di tempo, in secondi, durante il quale i record degli eventi sono protetti da sovrascrivere. Quando il tempo di un evento raggiunge o supera questo valore, può essere sovrascritto.<br/></td>
</tr>
<tr class="even">
<td><strong>recenti</strong></td>
<td>Questo valore non viene utilizzato. <strong>Windows Server 2003 e Windows XP/2000:  </strong> Nomi delle applicazioni, dei servizi o dei gruppi di applicazioni che scrivono gli eventi in questo log. Questo valore deve essere letto e non modificato. Il servizio Registro eventi gestisce l'elenco in base a ogni programma elencato in una sottochiave nel log. Questo valore è di tipo REG_MULTI_SZ.<br/></td>
</tr>
<tr class="odd">
<td><strong>AutoBackupLogFiles</strong></td>
<td>Questo valore è di tipo REG_DWORD e viene utilizzato dal servizio Registro eventi per determinare se un registro eventi deve essere salvato automaticamente. Il valore predefinito è 0, che disabilita il backup automatico. Il servizio eseguirà il backup del file di log solo se il valore di conservazione è-1 (0xFFFFFFFF). Gli altri valori verranno ignorati. <strong>Windows Server 2003:  </strong> Il periodo di memorizzazione può essere impostato su-1 (0xFFFFFFFF) o 1 (0x00000001) per il funzionamento di AutoBackupLogFiles. Gli altri valori verranno ignorati.<br/></td>
</tr>
<tr class="even">
<td><strong>RestrictGuestAccess</strong></td>
<td>Questo valore non viene utilizzato. <strong>Windows XP/2000:  </strong> Questo valore è di tipo REG_DWORD e il valore predefinito è 1. Quando il valore è impostato su 1, limita l'accesso dell'account Guest e anonimo al registro eventi e, quando questo valore è 0, consente all'account Guest di accedere al registro eventi.<br/></td>
</tr>
<tr class="odd">
<td><strong>Isolamento</strong></td>
<td>Definisce le autorizzazioni di accesso predefinite per il log. Questo valore è di tipo REG_SZ. È possibile specificare uno dei valori seguenti:
<ul>
<li><strong>Applicazione</strong></li>
<li><strong>Sistema</strong></li>
<li><strong>Impostazione personalizzata</strong></li>
</ul>
L'isolamento predefinito è <strong>Application</strong>. Le autorizzazioni predefinite per l' <strong>applicazione</strong> sono (visualizzate con SDDL): <br/>
<pre class="syntax" data-space="preserve"><code>            L&quot;O:BAG:SYD:&quot;
            L&quot;(A;;0xf0007;;;SY)&quot;                // local system               (read, write, clear)
            L&quot;(A;;0x7;;;BA)&quot;                    // built-in admins            (read, write, clear)
            L&quot;(A;;0x7;;;SO)&quot;                    // server operators           (read, write, clear)
            L&quot;(A;;0x3;;;IU)&quot;                    // INTERACTIVE LOGON          (read, write)
            L&quot;(A;;0x3;;;SU)&quot;                    // SERVICES LOGON             (read, write)
            L&quot;(A;;0x3;;;S-1-5-3)&quot;               // BATCH LOGON                (read, write)
            L&quot;(A;;0x3;;;S-1-5-33)&quot;              // write restricted service   (read, write)
            L&quot;(A;;0x1;;;S-1-5-32-573)&quot;;         // event log readers          (read) </code></pre>
Le autorizzazioni predefinite per il <strong>sistema</strong> sono (visualizzate con SDDL): <br/>
<pre class="syntax" data-space="preserve"><code>            L&quot;O:BAG:SYD:&quot;
            L&quot;(A;;0xf0007;;;SY)&quot;                // local system             (read, write, clear)
            L&quot;(A;;0x7;;;BA)&quot;                    // built-in admins          (read, write, clear)
            L&quot;(A;;0x3;;;BO)&quot;                    // backup operators         (read, write)
            L&quot;(A;;0x5;;;SO)&quot;                    // server operators         (read, clear) 
            L&quot;(A;;0x1;;;IU)&quot;                    // INTERACTIVE LOGON        (read)
            L&quot;(A;;0x3;;;SU)&quot;                    // SERVICES LOGON           (read, write)
            L&quot;(A;;0x1;;;S-1-5-3)&quot;               // BATCH LOGON              (read)
            L&quot;(A;;0x2;;;S-1-5-33)&quot;              // write restricted service (write)
            L&quot;(A;;0x1;;;S-1-5-32-573)&quot;;         // event log readers        (read)</code></pre>
Le autorizzazioni predefinite per l'isolamento <strong>personalizzato</strong> sono identiche a quelle dell'applicazione.<br/> <strong>Windows Server 2003 e Windows XP/2000:  </strong> Questo valore non è disponibile.<br/></td>
</tr>
</tbody>
</table>



 

Ogni log contiene anche origini evento. Per ulteriori informazioni, vedere [origini evento](event-sources.md).

