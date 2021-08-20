---
description: 'Il registro eventi contiene i log standard e i log personalizzati seguenti:'
ms.assetid: 87d860e3-2495-4e15-bb42-341e92935e55
title: Chiave del registro eventi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8b60a2a935267ddeed52a82602c1192ff23d7005
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2021
ms.locfileid: "122477807"
---
# <a name="eventlog-key"></a>Chiave del registro eventi

Il registro eventi contiene i log standard e i log personalizzati seguenti:



| Registro             | Descrizione                                                                                                                                                                                                                                  |
|-----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Applicazione** | Contiene gli eventi registrati dalle applicazioni. Ad esempio, un'applicazione di database potrebbe registrare un errore di file. Lo sviluppatore dell'applicazione decide quali eventi registrare.                                                                             |
| **Sicurezza**    | Contiene eventi quali tentativi di accesso validi e non validi, nonché eventi correlati all'uso delle risorse, ad esempio la creazione, l'apertura o l'eliminazione di file o altri oggetti. Un amministratore può avviare il controllo per registrare gli eventi nel registro di sicurezza. |
| **Sistema**      | Contiene gli eventi registrati dai componenti di sistema, ad esempio l'errore di caricamento di un driver o di un altro componente di sistema durante l'avvio.                                                                                                               |
| *CustomLog*     | Contiene gli eventi registrati dalle applicazioni che creano un log personalizzato. L'uso di un log personalizzato consente a un'applicazione di controllare le dimensioni del log o collegare gli ACL per motivi di sicurezza senza influire sulle altre applicazioni.                         |



 

Il servizio di registrazione eventi usa le informazioni archiviate nella **chiave del Registro di sistema Eventlog.** La **chiave eventlog** contiene diverse sottochiavi, denominate *log*. Ogni log contiene informazioni utilizzate dal servizio di registrazione eventi per individuare le risorse quando un'applicazione scrive e legge dal registro eventi.

La struttura della **chiave eventlog** è la seguente:

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

Si noti che i controller di dominio registrano gli eventi nel servizio **Directory** e nei log del servizio Replica **file** e nei server DNS registrano gli eventi nel **server DNS**.

Ogni log può contenere i valori del Registro di sistema seguenti.




| Valore del Registro di sistema | Descrizione | 
|----------------|-------------|
| <strong>CustomSD</strong> | Limita l'accesso al registro eventi. Questo valore è di tipo REG_SZ. Il formato usato è <a href="/windows/desktop/SecAuthZ/security-descriptor-definition-language">SDDL (Security Descriptor Definition Language).</a> Costruire un elenco di controllo di accesso che concede uno o più dei diritti seguenti:<dl> Cancella (0x0004)<br />Lettura (0x0001)<br />Scrittura (0x0002)<br /></dl> Per essere un SDDL sintatticamente valido, il valore CustomSD deve specificare un proprietario e un proprietario del gruppo (ad esempio, O:BAG:SY), ma il proprietario e il proprietario del gruppo non vengono usati. Se CustomSD è impostato su un valore errato, viene generato un evento nel registro eventi di sistema all'avvio del servizio registro eventi e il registro eventi ottiene un descrittore di sicurezza predefinito identico al valore CustomSD originale per il registro applicazioni. I SACL non sono supportati.<br /> Per altre informazioni, vedere <a href="event-logging-security.md">Sicurezza della registrazione eventi</a>.<br /><strong>Windows Server 2003:</strong> I SACL sono supportati.<br /><strong>Windows XP/2000:</strong> Questo valore non è supportato.<br /><br /> | 
| <strong>DisplayNameFile</strong> | Questo valore non viene utilizzato. <strong>Windows Server 2003 e Windows XP/2000:</strong> Nome del file in cui è archiviato il nome localizzato del registro eventi. Il nome archiviato in questo file viene visualizzato come nome del log in Visualizzatore eventi. Se questa voce non viene visualizzata nel Registro di sistema per un registro eventi, Visualizzatore eventi il nome della sottochiave del Registro di sistema come nome del log. Questo valore è di tipo REG_EXPAND_SZ. Il valore predefinito è %SystemRoot%\system32\els.dll.<br /> | 
| <strong>DisplayNameID</strong> | Questo valore non viene utilizzato. <strong>Windows Server 2003 e Windows XP/2000:</strong> Numero di identificazione del messaggio della stringa del nome del log. Questo numero indica il messaggio in cui viene visualizzato il nome visualizzato localizzato. Il messaggio viene archiviato nel file specificato dal <strong>valore DisplayNameFile.</strong> Questo valore è di tipo REG_DWORD.<br /> | 
| <strong>File</strong> | Percorso completo del file in cui è archiviato ogni log eventi. Ciò consente Visualizzatore eventi e altre applicazioni di trovare i file di log. Questo valore è di tipo REG_SZ o REG_EXPAND_SZ. Questo valore è facoltativo. Se il valore non viene specificato, il valore predefinito è %SystemRoot%\system32\winevt\logs\ seguito da un nome di file basato sul nome della chiave del Registro di sistema del registro eventi. Il percorso del file di log eventi specifico deve essere impostato usando l'utilità della riga di comando wevtutil.exe o usando la funzione <a href="/windows/desktop/api/winevt/nf-winevt-evtsetchannelconfigproperty"><strong>EvtSetChannelConfigProperty</strong></a> con EvtChannelLoggingConfigLogFilePath passato nel <em>parametro PropertyId.</em><br /> Se è impostato un file specifico, assicurarsi che il servizio registro eventi abbia le autorizzazioni complete per il file.<br /> Questo valore deve essere un nome di file valido per un file che si trova in una directory locale (non un computer remoto, non un dispositivo DOS, non un dischetto e non una pipe). Se l'impostazione del file è errata, viene generato un evento nel registro eventi di sistema all'avvio del servizio registro eventi.<br /> Non usare variabili di ambiente, nel percorso del file, che non possono essere espanse nel contesto del servizio registro eventi.<br /><strong>Windows Server 2003 e Windows XP/2000:</strong> Il valore predefinito è %SystemRoot%\system32\config\ seguito da un nome di file basato sul nome della chiave del Registro di sistema del registro eventi. Se l'impostazione File è impostata su un valore non valido, il log non verrà inizializzato correttamente o tutte le richieste verranno automaticamente inviate al log predefinito (applicazione).<br /> | 
| <strong>Maxsize</strong> | Dimensioni massime, in byte, del file di log. Questo valore è di tipo REG_DWORD. Il valore deve essere impostato su un multiplo di 64.000 per un registro di sistema, applicazione o sicurezza. Il valore predefinito è 1 MB. <strong>Windows Server 2003 e Windows XP/2000:</strong> Il valore è limitato a 0xFFFFFFFF e il valore predefinito è 512.000.<br /> | 
| <strong>PrimaryModule</strong> | Questo valore non viene usato. <strong>Windows Server 2003 e Windows XP/2000:</strong> Questo valore è il nome della sottochiave che contiene i valori predefiniti per le voci nella sottochiave per l'origine evento. Questo valore è di tipo REG_SZ.<br /> | 
| <strong>Conservazione</strong> | Questo valore è di tipo REG_DWORD. Il valore predefinito è 0. Se questo valore è 0, i record degli eventi vengono sempre sovrascritti. Se questo valore è 0xFFFFFFFF o qualsiasi valore diverso da zero, i record non vengono mai sovrascritti. Quando il file di log raggiunge le dimensioni massime, è necessario cancellare il log manualmente. In caso contrario, i nuovi eventi vengono eliminati. È anche necessario cancellare il log prima di poterne modificare le dimensioni. <strong>Windows Server 2003 e Windows XP/2000:</strong> Questo valore è l'intervallo di tempo, in secondi, in cui i record degli eventi sono protetti dalla sovrascrittura. Quando l'età di un evento raggiunge o supera questo valore, può essere sovrascritta.<br /> | 
| <strong>recenti</strong> | Questo valore non viene utilizzato. <strong>Windows Server 2003 e Windows XP/2000:</strong> Nomi delle applicazioni, dei servizi o dei gruppi di applicazioni che scrivono eventi in questo log. Questo valore deve essere solo letto e non modificato. Il servizio registro eventi gestisce l'elenco in base a ogni programma elencato in una sottochiave nel log. Questo valore è di tipo REG_MULTI_SZ.<br /> | 
| <strong>AutoBackupLogFiles</strong> | Questo valore è di tipo REG_DWORD e viene usato dal servizio registro eventi per determinare se un log eventi deve essere salvato automaticamente. Il valore predefinito è 0, che disabilita il backup automatico. Il servizio eseguire il backup del file di log solo se il valore di conservazione è -1 (0xFFFFFFFF). Gli altri valori verranno ignorati. <strong>Windows Server 2003:</strong> La conservazione può essere impostata su -1 (0xFFFFFFFF) o 1 (0x00000001) per il funzionamento di AutoBackupLogFiles. Gli altri valori verranno ignorati.<br /> | 
| <strong>RestrictGuestAccess</strong> | Questo valore non viene utilizzato. <strong>Windows XP/2000:</strong> Questo valore è di tipo REG_DWORD e il valore predefinito è 1. Quando il valore è impostato su 1, limita l'accesso degli account guest e anonimi al registro eventi e, quando questo valore è 0, consente l'accesso dell'account Guest al registro eventi.<br /> | 
| <strong>Isolamento</strong> | Definisce le autorizzazioni di accesso predefinite per il log. Questo valore è di tipo REG_SZ. È possibile specificare uno dei valori seguenti:<ul><li><strong>Applicazione</strong></li><li><strong>Sistema</strong></li><li><strong>Impostazione personalizzata</strong></li></ul>L'isolamento predefinito è <strong>Application.</strong> Le autorizzazioni predefinite per <strong>l'applicazione</strong> sono (visualizzate tramite SDDL): <br /><pre class="syntax" data-space="preserve"><code>            L"O:BAG:SYD:"            L"(A;;0xf0007;;;SY)"                // local system               (read, write, clear)            L"(A;;0x7;;;BA)"                    // built-in admins            (read, write, clear)            L"(A;;0x7;;;SO)"                    // server operators           (read, write, clear)            L"(A;;0x3;;;IU)"                    // INTERACTIVE LOGON          (read, write)            L"(A;;0x3;;;SU)"                    // SERVICES LOGON             (read, write)            L"(A;;0x3;;;S-1-5-3)"               // BATCH LOGON                (read, write)            L"(A;;0x3;;;S-1-5-33)"              // write restricted service   (read, write)            L"(A;;0x1;;;S-1-5-32-573)";         // event log readers          (read) </code></pre>Le autorizzazioni predefinite per <strong>System</strong> sono (visualizzate tramite SDDL): <br /><pre class="syntax" data-space="preserve"><code>            L"O:BAG:SYD:"            L"(A;;0xf0007;;;SY)"                // local system             (read, write, clear)            L"(A;;0x7;;;BA)"                    // built-in admins          (read, write, clear)            L"(A;;0x3;;;BO)"                    // backup operators         (read, write)            L"(A;;0x5;;;SO)"                    // server operators         (read, clear)             L"(A;;0x1;;;IU)"                    // INTERACTIVE LOGON        (read)            L"(A;;0x3;;;SU)"                    // SERVICES LOGON           (read, write)            L"(A;;0x1;;;S-1-5-3)"               // BATCH LOGON              (read)            L"(A;;0x2;;;S-1-5-33)"              // write restricted service (write)            L"(A;;0x1;;;S-1-5-32-573)";         // event log readers        (read)</code></pre>Le autorizzazioni predefinite per <strong>Isolamento</strong> personalizzato sono le stesse dell'applicazione.<br /><strong>Windows Server 2003 e Windows XP/2000:</strong> Questo valore non è disponibile.<br /> | 




 

Ogni log contiene anche origini evento. Per altre informazioni, vedere [Origini eventi.](event-sources.md)

