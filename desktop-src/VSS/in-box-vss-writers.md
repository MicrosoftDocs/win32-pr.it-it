---
description: Il sistema operativo Windows include un set di VSS writer responsabili dell'enumerazione dei dati necessari alle varie funzionalità Windows. Questi vengono definiti &\# 0034,&\# 0034; writer.
ms.assetid: e20a303d-9440-42be-b383-85f6fad89157
title: VSS writer inclusi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ddc256cfe72f3653d4af282148c87c2b45bcac51
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106310705"
---
# <a name="in-box-vss-writers"></a>VSS writer inclusi

Il sistema operativo Windows include un set di VSS writer responsabili dell'enumerazione dei dati necessari alle varie funzionalità Windows. Questi vengono definiti writer "in-box".

> [!Note]  
> Il writer in-box di MSDE non è disponibile in Windows Vista, Windows Server 2008 e versioni successive. Al contrario, il writer SQL deve essere utilizzato per eseguire il backup di SQL Server database. Solo SQL Server 2005 SP2 e versioni successive sono supportati in Windows Vista, Windows Server 2008 e versioni successive.

 

-   [Writer VSS Active Directory Domain Services (NTDS)](#active-directory-domain-services-ntds-vss-writer)
-   [Writer di Active Directory Federation Services](#active-directory-federation-services-writer)
-   [Writer VSS di Active Directory Lightweight Directory Services (LDS)](#active-directory-lightweight-directory-services-lds-vss-writer)
-   [Writer di Active Directory Rights Management Services (AD RMS)](#active-directory-rights-management-services-ad-rms-writer)
-   [Writer ripristino automatico di sistema (ASR)](#automated-system-recovery-asr-writer)
-   [Writer di Servizio trasferimento intelligente in background (BITS)](#background-intelligent-transfer-service-bits-writer)
-   [Writer autorità di certificazione](#certificate-authority-writer)
-   [Writer del servizio cluster](#cluster-service-writer)
-   [Writer VSS Volume condiviso cluster (CSV)](#cluster-shared-volume-csv-vss-writer)
-   [Writer del database di registrazione della classe COM+](#com-class-registration-database-writer)
-   [Writer Deduplicazione dati](#data-deduplication-writer)
-   [Replica DFS (Distributed File System)](#distributed-file-system-replication-dfsr)
-   [Writer di Dynamic Host Configuration Protocol (DHCP)](#dynamic-host-configuration-protocol-dhcp-writer)
-   [Servizio Replica file](#file-replication-service-frs)
-   [Writer di Gestione risorse file server (FSRM)](#file-server-resource-manager-fsrm-writer)
-   [Writer di Hyper-V](#hyper-v-writer)
-   [Writer di configurazione IIS](#iis-configuration-writer)
-   [Writer metabase IIS](#iis-metabase-writer)
-   [Writer di Microsoft Message Queuing (MSMQ)](#microsoft-message-queuing-msmq-writer)
-   [Writer del servizio MSSearch](#mssearch-service-writer)
-   [Writer VSS server dei criteri di servizio](#nps-vss-writer)
-   [Writer dei contatori delle prestazioni](#performance-counters-writer)
-   [Writer del registro di sistema](#registry-writer)
-   [Writer VSS del gateway Servizi Desktop remoto (Servizi terminal)](#remote-desktop-services-terminal-services-gateway-vss-writer)
-   [Writer VSS di gestione licenze Servizi Desktop remoto (Servizi terminal)](#remote-desktop-services-terminal-services-licensing-vss-writer)
-   [Writer di ottimizzazione copia shadow](#shadow-copy-optimization-writer)
-   [Writer del servizio di condivisione di sincronizzazione](#sync-share-service-writer)
-   [Writer di sistema](#system-writer)
-   [Writer di Utilità di pianificazione](#task-scheduler-writer)
-   [Writer archivio metadati VSS](#vss-metadata-store-writer)
-   [Writer di servizi di distribuzione Windows (WDS)](#windows-deployment-services-wds-writer)
-   [Writer database interno di Windows (WID)](#windows-internal-database-wid-writer)
-   [Writer WINS (Windows Internet Name Service)](#windows-internet-name-service-wins-writer)
-   [Writer WMI](#wmi-writer)

## <a name="active-directory-domain-services-ntds-vss-writer"></a>Writer VSS Active Directory Domain Services (NTDS)

Questo writer segnala il file di database NTDS (NTDS. dit) e i file di log associati. Questi file sono necessari per ripristinare correttamente il Active Directory.

È presente un solo file NTDS. dit per controller di dominio e viene segnalato nei metadati del writer come nell'esempio seguente:

``` syntax
    <DATABASE_FILES path="C:\Windows\NTDS" 
                     filespec="ntds.dit" 
                     filespecBackupType="3855"/>
```

Di seguito è riportato un esempio in cui viene illustrato come elencare i componenti nei metadati del writer:

``` syntax
    <BACKUP_LOCATIONS>
        <DATABASE logicalPath="C:_Windows_NTDS" 
                     componentName="ntds" 
                     caption="" restoreMetadata="no" 
                     notifyOnBackupComplete="no" 
                     selectable="no" 
                     selectableForRestore="no" 
                     componentFlags="3">
        <DATABASE_FILES path="C:\Windows\NTDS" 
                     filespec="ntds.dit" 
                     filespecBackupType="3855"/>
        <DATABASE_LOGFILES path="C:\Windows\NTDS" 
                     filespec="edb*.log" 
                     filespecBackupType="3855"/> 
        <DATABASE_LOGFILES path="C:\Windows\NTDS" 
                     filespec="edb.chk" 
                     filespecBackupType="3855"/>
        </DATABASE>
    </BACKUP_LOCATIONS>
```

Al momento del backup, il writer imposta l'ora di scadenza del backup nei metadati di backup del writer. I richiedenti devono recuperare questi metadati usando [**IVssComponent:: GetBackupMetadata**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getbackupmetadata) per determinare se il database è scaduto. Impossibile ripristinare i database scaduti.

Se il computer che contiene il database NTDS è un controller di dominio, l'applicazione di backup deve sempre eseguire un backup dello stato del sistema in tutti i volumi contenenti informazioni critiche sullo stato del sistema. Al momento del ripristino, l'applicazione deve prima riavviare il computer in modalità ripristino servizi directory e quindi eseguire un ripristino dello stato del sistema.

La stringa del nome del writer per questo writer è "NTDS".

L'ID del writer per questo writer è B2014C9E-8711-4C5C-A5A9-3CF384484757.

## <a name="active-directory-federation-services-writer"></a>Writer di Active Directory Federation Services

Questo writer segnala i file di dati di Active Directory Federation Services (ADFS).

**Windows server 2008 R2, Windows 7, Windows server 2008, Windows Vista, Windows server 2003 e Windows XP:** Questo writer non è supportato.

La stringa del nome del writer per questo writer è "ADFS VSS Writer".

L'ID del writer per questo writer è 772C45F8-AE01-4F94-940C-94961864ACAD.

## <a name="active-directory-lightweight-directory-services-lds-vss-writer"></a>Writer VSS di Active Directory Lightweight Directory Services (LDS)

Questo writer segnala il file di database ADAM (Adamntds. dit) e i file di log associati per ogni istanza nei dati% programmi% \\ Microsoft Adam \\ istanza *n* \\ , dove *N* è il numero di istanza di Adam. Questi file di log del database sono necessari per ripristinare le istanze di ADAM.

**Windows XP:** Questo writer non è supportato.

Di seguito è riportato un esempio in cui viene illustrato come elencare i componenti nei metadati del writer:

``` syntax
    <BACKUP_LOCATIONS>
        <DATABASE logicalPath="C:_Program Files_Microsoft ADAM_instance1_data" 
                     componentName="adamntds" 
                     caption="" 
                     restoreMetadata="no" 
                     notifyOnBackupComplete="no" 
                     selectable="no" 
                     selectableForRestore="no" 
                     componentFlags="3">
        <DATABASE_FILES path="C:\Program Files\Microsoft ADAM\instance1\data" 
                     filespec="adamntds.dit" 
                     filespecBackupType="3855"/>
        <DATABASE_LOGFILES path="C:\Program Files\Microsoft ADAM\instance1\data" 
                     filespec="edb*.log" 
                     filespecBackupType="3855"/>
        <DATABASE_LOGFILES path="C:\Program Files\Microsoft ADAM\instance1\data" 
                     filespec="edb.chk" 
                     filespecBackupType="3855"/>
        </DATABASE>
    </BACKUP_LOCATIONS>
```

Al momento del backup, il writer imposta l'ora di scadenza del backup nei metadati di backup. Le applicazioni di backup devono recuperare questi metadati usando il metodo [**IVssComponent:: GetBackupMetadata**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getbackupmetadata) per determinare se il database è scaduto. Impossibile ripristinare i database scaduti.

La stringa del nome del writer per questo writer è "ADAM (instance *N*) writer", dove *N* è il numero di istanza di Adam, ad esempio, "Adam (instance1) writer", "Adam (Instance2) writer" e così via.

L'ID del writer per questo writer è DD846AAA-A1B6-42A8-AAF8-03DCB6114BFD. Questo ID writer è lo stesso per tutte le istanze.

## <a name="active-directory-rights-management-services-ad-rms-writer"></a>Writer di Active Directory Rights Management Services (AD RMS)

Questo writer segnala i file di dati del servizio Active Directory Rights Management (AD RMS).

**Windows server 2008 R2, Windows 7, Windows server 2008, Windows Vista, Windows server 2003 e Windows XP:** Questo writer non è supportato.

La stringa del nome del writer per questo writer è "AD RMS writer".

L'ID del writer per questo writer è 886C43B1-D455-4428-A37F-4D6B9E43F50F.

## <a name="automated-system-recovery-asr-writer"></a>Writer ripristino automatico di sistema (ASR)

Il writer ASR archivia la configurazione dei dischi nel sistema. Questo writer segnala il database di configurazione di avvio (BCD) ed è anche responsabile dello smontaggio dell'hive del registro di sistema che rappresenta il BCD durante la creazione della copia shadow. Il writer di ASR deve essere incluso nei backup necessari per il ripristino bare metal. Per ulteriori informazioni su ASR, vedere [utilizzo del ripristino automatico del sistema VSS per il ripristino di emergenza](using-vss-automated-system-recovery-for-disaster-recovery.md).

**Windows Server 2003 e Windows XP:** Questo writer non è supportato.

La stringa del nome del writer per questo writer è "ASR writer".

L'ID writer per il writer ASR è BE000CBE-11FE-4426-9C58-531AA6355FC4.

## <a name="background-intelligent-transfer-service-bits-writer"></a>Writer di Servizio trasferimento intelligente in background (BITS)

Il writer BITS usa la chiave del registro di sistema **FilesNotToBackup** per escludere i file dalla cartella della cache BITS. Il percorso predefinito della cache è% AllUsersProfile% \\ Microsoft \\ Network \\ Downloader \\ cache.

**Windows Server 2003 e Windows XP:** Questo writer non è supportato.

Inoltre, il writer BITS esclude i file seguenti dal backup: i file di stato BITS (Qmgr0. dat e Qmgr1. dat), il file di log di debug BITS e i file scaricati parzialmente.

Se il file di destinazione per il download BITS è un file SMB, è necessario che l'account client disponga di una relazione di trust con il server. in caso contrario, i backup potrebbero non riuscire.

La stringa del nome del writer per questo writer è "BITS writer".

L'ID del writer per il writer BITS è 4969D978-BE47-48B0-B100-F328F07AC1E0.

## <a name="certificate-authority-writer"></a>Writer autorità di certificazione

Questo writer è responsabile dell'enumerazione dei file di dati per il server dei certificati.

La stringa del nome del writer per questo writer è "autorità di certificazione".

**Windows XP:** La stringa del nome del writer per questo writer è "Certificate Server Writer".

L'ID del writer per il writer è 6F5B15B5-DA24-4D88-B737-63063E3A1F86.

## <a name="cluster-service-writer"></a>Writer del servizio cluster

Il VSS writer del servizio cluster è documentato nella documentazione dell'API del [servizio cluster](/previous-versions/windows/desktop/mscs/backing-up-and-restoring-the-failover-cluster-configuration-using-vss) .

**Windows Vista, Windows Server 2003 e Windows XP:** Questo writer non è supportato fino a Windows Vista con Service Pack 1 (SP1) e Windows Server 2008.

## <a name="cluster-shared-volume-csv-vss-writer"></a>Writer VSS Volume condiviso cluster (CSV)

Questo writer segnala i file di dati di Volume condiviso cluster (CSV). Questo writer è un writer in-box per le versioni del sistema operativo Windows Server. non viene fornito nel client Windows.

**Windows server 2008 R2, Windows server 2008 e Windows server 2003:** Questo writer non è supportato.

La stringa del nome del writer per questo writer è "Volume condiviso cluster VSS Writer".

L'ID del writer per il writer è 1072AE1C-E5A7-4EA1-9E4A-6F7964656570.

## <a name="com-class-registration-database-writer"></a>Writer del database di registrazione della classe COM+

Questo writer è responsabile del contenuto della directory di registrazione% SystemRoot% \\ . Il catalogo COM+ è un file nella registrazione% SystemRoot% \\ con un nome che segue il modello R *xxxxxxxxxxxx*. CLB, dove *xxxxxxxxxxxx* è un numero esadecimale a 12 cifre. Se le applicazioni COM+ sono state configurate nel computer, potrebbero essere presenti più file di questo tipo. Il file che contiene il catalogo COM+ corrente è il file con il valore più grande di *xxxxxxxxxxxx*.

**Windows Server 2003 e Windows XP:** Questo writer non è supportato.

Il database di registrazione della classe COM+ dipende da una chiave del registro di sistema di cui viene eseguito il backup e che pertanto deve essere sottoposta a backup e ripristino insieme al registro di sistema.

Per ripristinare il database di registrazione COM+, un'applicazione di backup (richiedente) deve chiamare il metodo [**ICOMAdminCatalog:: RestoreREGDB**](/windows/win32/api/comadmin/nf-comadmin-icomadmincatalog-restoreregdb) .

La stringa del nome del writer per questo writer è "COM+ REGDB writer".

L'ID del writer per il writer del database di registrazione della classe COM+ è 542DA469-D3E1-473C-9F4F-7847F01FC64F.

## <a name="data-deduplication-writer"></a>Writer Deduplicazione dati

Il VSS writer di deduplicazione dati è documentato nella documentazione dell'API [Deduplicazione dati](/previous-versions/windows/desktop/dedup/backup-and-restore-of-data-deduplication-enabled-volumes) . Questo writer è un writer in-box per le versioni del sistema operativo Windows Server. non viene fornito nel client Windows.

**Windows server 2008 R2, Windows server 2008 e Windows server 2003:** Questo writer non è supportato.

## <a name="distributed-file-system-replication-dfsr"></a>Replica DFS (Distributed File System)

Il componente seguente include un VSS writer: [replica file System distribuito (DFSR)](/previous-versions/windows/desktop/dfsr/dfsr-replicated-folders)

**Windows Vista, Windows Server 2003 e Windows XP:** Questo writer non è supportato fino a Windows Vista con SP1 e Windows Server 2008.

## <a name="dynamic-host-configuration-protocol-dhcp-writer"></a>Writer di Dynamic Host Configuration Protocol (DHCP)

Questo writer è responsabile dell'enumerazione dei file necessari per il ruolo server DHCP. Questo writer è un writer in-box per le versioni del sistema operativo Windows Server. non viene fornito nel client Windows.

La stringa del nome del writer per questo writer è "DHCP Jet writer".

L'ID del writer per questo writer è BE9AC81E-3619-421F-920F-4C6FEA9E93AD.

## <a name="file-replication-service-frs"></a>Servizio Replica file

Il writer del servizio Replica file è documentato per il [backup e il ripristino di una cartella FRS-Replicated SYSVOL](backing-up-and-restoring-an-frs-replicated-sysvol-folder.md).

**Windows Vista, Windows Server 2003 e Windows XP:** Questo writer non è supportato fino a Windows Vista con SP1 e Windows Server 2008.

## <a name="file-server-resource-manager-fsrm-writer"></a>Writer di Gestione risorse file server (FSRM)

Questo writer enumera i file di configurazione FSRM usati per il backup dello stato del sistema. Durante le operazioni di ripristino, impedisce le modifiche nella configurazione di FSRM e interrompe temporaneamente l'applicazione di quote e schermate di file. Al termine del ripristino, il writer Aggiorna FSRM con la configurazione che è stata ripristinata. Questo writer è presente solo quando FSRM (parte del ruolo Servizi file) è installato e in esecuzione. Questo writer è un writer in-box per le versioni del sistema operativo Windows Server. non viene fornito nel client Windows.

**Windows Server 2003:** Questo writer non è supportato fino a Windows Server 2003 R2.

La stringa del nome del writer per questo writer è "FSRM writer".

L'ID del writer per questo writer è 12CE4370-5BB7-4C58-A76A-E5D5097E3674.

## <a name="hyper-v-writer"></a>Writer di Hyper-V

Il VSS writer di Hyper-V è documentato nella documentazione dell'API di [Hyper-v](/previous-versions/windows/desktop/virtual/backing-up-and-restoring-virtual-machines) . Questo writer è un writer in-box per le versioni del sistema operativo Windows Server. non viene fornito nel client Windows.

**Windows Server 2003:** Questo writer non è supportato fino a Windows Server 2008.

## <a name="iis-configuration-writer"></a>Writer di configurazione IIS

Il writer di configurazione di IIS è responsabile dell'enumerazione dei file di configurazione di IIS.

**Windows Vista, Windows Server 2003 e Windows XP:** Questo writer non è supportato fino a Windows Vista con SP1 e Windows Server 2008. I richiedenti sono necessari per eseguire il backup dei file di configurazione di IIS, incluso il file di machine.config .NET FX o il file di web.config radice ASP.NET.

Questo writer non esegue il backup del file di machine.config .NET FX o del file web.config radice di ASP.NET perché questi file sono enumerati dal writer di sistema.

Questo writer esegue il backup di tutti i file presenti nello schema di configurazione% windir% \\ system32 \\ inetsrv \\ e di \\ % windir% \\ system32 \\ inetsrv \\ config directory, ad eccezione dei file enumerati dal writer di sistema.

L'ID writer per il writer di configurazione IIS è 2A40FD15-DFCA-4aa8-A654-1F8C654603F6.

## <a name="iis-metabase-writer"></a>Writer metabase IIS

Il writer della metabase di Internet Information Server (IIS) è responsabile dell'enumerazione del file della metabase di IIS.

**Windows Vista, Windows Server 2003 e Windows XP:** Questo writer non è supportato fino a Windows Vista con SP1 e Windows Server 2008. I richiedenti sono necessari per eseguire il backup del file della metabase di IIS.

L'ID del writer per il writer della metabase di IIS è 59B1f0CF-90EF-465F-9609-6CA8B2938366.

## <a name="microsoft-message-queuing-msmq-writer"></a>Writer di Microsoft Message Queuing (MSMQ)

Questo writer segnala i file di dati di Microsoft Message Queuing (MSMQ).

**Windows server 2008 R2, Windows 7, Windows server 2008, Windows Vista, Windows server 2003 e Windows XP:** Questo writer non è supportato.

La stringa del nome del writer per questo writer è "MSMQ Writer (*SvcName*)", dove *SvcName* è il nome del servizio MSMQ a cui è associato il writer. Per l'installazione predefinita, il nome del servizio è "MSMQ". Per le istanze cluster, il nome del servizio è MSMQ $*resourceName*, dove *resourceName* è il nome della risorsa MSMQ in cluster.

L'ID del writer per questo writer è 7E47B561-971A-46E6-96B9-696EEAA53B2A.

## <a name="mssearch-service-writer"></a>Writer del servizio MSSearch

Questo writer esiste per eliminare i file di indice di ricerca dalle copie shadow dopo la creazione. Questa operazione viene eseguita per ridurre al minimo l'effetto delle operazioni di I/O copy-on-Write durante le operazioni di I/o regolari su questi file nel volume copiato Shadow.

**Windows Server 2003:** Questo writer non è supportato.

Per installare questo writer nel server, è necessario installare il ruolo Servizi file e abilitare Windows servizio di ricerca.

La stringa del nome del writer per questo writer è "MSSearch Service writer".

L'ID writer per il writer del servizio MSSearch è CD3F2362-8BEF-46C7-9181-D62844CDC0B2.

## <a name="nps-vss-writer"></a>Writer VSS server dei criteri di servizio

Il writer NPS è responsabile dell'enumerazione dei file di configurazione del server dei criteri di rete (NPS) per i server in cui è installato il ruolo Servizi di accesso e criteri di rete.

**Windows Vista, Windows Server 2003 e Windows XP:** Questo writer non è supportato fino a Windows Vista con SP1 e Windows Server 2008.

La stringa del nome del writer per questo writer è "NPS VSS Writer".

L'ID del writer per la VSS writer NPS è 0x35E81631-13E1-48DB-97FC-D5BC721BB18A.

## <a name="performance-counters-writer"></a>Writer dei contatori delle prestazioni

Questo writer segnala i file di configurazione del contatore delle prestazioni. Questi file vengono modificati solo durante l'installazione dell'applicazione ed è necessario eseguirne il backup e il ripristino durante i backup e i ripristini dello stato del sistema.

**Windows server 2008, Windows Vista, Windows server 2003 e Windows XP:** Questo writer non è supportato. I richiedenti sono necessari per eseguire manualmente il backup di questi file. (Vedere [backup e ripristino dello stato del sistema](locating-additional-system-files.md)).

La stringa del nome del writer per questo writer è "performance counters writer".

L'ID writer per il writer dei contatori delle prestazioni è 0BADA1DE-01A9-4625-8278-69E735F39DD2.

## <a name="registry-writer"></a>Writer del registro di sistema

Il writer del registro di sistema segnala i file del registro di sistema di Windows per abilitare i backup sul posto e il ripristino del registro di sistema. Non segnala gli hive degli utenti.

**Windows Server 2003:** In Windows Server 2003, questo writer usa un file di repository intermedio (talvolta denominato "file spit") per archiviare i dati del registro di sistema. (Vedere [operazioni di backup e ripristino del registro di sistema in VSS](registry-backup-and-restore-operations-under-vss.md)).

**Windows XP:** Questo writer non è supportato. (Vedere [operazioni di backup e ripristino del registro di sistema in VSS](registry-backup-and-restore-operations-under-vss.md)).

La stringa del nome del writer per questo writer è "Registry writer".

L'ID del writer per il writer del registro di sistema è AFBAB4A2-367D-4D15-A586-71DBB18F8485.

## <a name="remote-desktop-services-terminal-services-gateway-vss-writer"></a>Writer VSS del gateway Servizi Desktop remoto (Servizi terminal)

Questo writer è responsabile dell'enumerazione dei file del gateway Servizi Desktop remoto (Servizi terminal) per i server con Desktop remoto Gateway, un sottoruolo del ruolo Servizi Desktop remoto, installato.

**Windows Server 2003:** Questo writer non è supportato.

Questo writer è un writer in-box per le versioni del sistema operativo Windows Server. non viene fornito nel client Windows.

Il gateway Servizi Desktop remoto dipende da diverse chiavi del registro di sistema di cui viene eseguito il backup e pertanto deve essere eseguito il backup e il ripristino insieme al registro di sistema.

La stringa del nome del writer per questo writer è "TS Gateway writer".

L'ID del writer per questo writer è 368753EC-572E-4FC7-B4B9-CCD9BDC624CB.

## <a name="remote-desktop-services-terminal-services-licensing-vss-writer"></a>Writer VSS di gestione licenze Servizi Desktop remoto (Servizi terminal)

Questo writer è responsabile dell'enumerazione dei file Servizi Desktop remoto Licensing (licenze Desktop remoto) o licenze Servizi terminal (licenze Servizi terminal) per i server che dispongono di licenze Desktop remoto, un sottoruolo del ruolo Servizi Desktop remoto, installato.

**Windows Server 2003:** Questo writer non è supportato.

Questo writer è un writer in-box per le versioni del sistema operativo Windows Server. non viene fornito nel client Windows.

Servizi Desktop remoto le licenze dipendono da diverse chiavi del registro di sistema di cui viene eseguito il backup e pertanto devono essere sottoposte a backup e ripristinate insieme al registro di sistema.

La stringa del nome del writer per questo writer è "TermServLicensing".

L'ID del writer per questo writer è 5382579C-98DF-47A7-AC6C-98A6D7106E09.

## <a name="shadow-copy-optimization-writer"></a>Writer di ottimizzazione copia shadow

Questo writer Elimina alcuni file dalle copie shadow del volume. Questa operazione viene eseguita per ridurre al minimo l'effetto delle operazioni di I/O copy-on-Write durante le operazioni di I/o regolari su questi file nel volume copiato Shadow. I file eliminati sono in genere file temporanei o file che non contengono l'utente o lo stato del sistema.

**Windows Server 2003 e Windows XP:** Questo writer non è supportato.

La stringa del nome del writer per questo writer è "writer di ottimizzazione per la copia shadow".

L'ID del writer per il writer di ottimizzazione della copia shadow è 4DC3BDD4-AB48-4D07-ADB0-3BEE2926FD7F.

## <a name="sync-share-service-writer"></a>Writer del servizio di condivisione di sincronizzazione

**Windows Server 2012 R2:** Questo writer è incluso in Windows Server 2012 R2 e versioni più recenti del server. Non è compatibile con le versioni desktop.

Questo writer è responsabile dell'enumerazione delle condivisioni di sincronizzazione nei server in cui è installato il servizio di condivisione di sincronizzazione e per garantire che i metadati e i dati rimangano coerenti durante il backup e il ripristino.

Questo writer è presente solo quando il servizio di condivisione di sincronizzazione è installato e in esecuzione.

Ci sarà un componente VSS writer per ogni condivisione di sincronizzazione. Sono inclusi i metadati e i percorsi dati. È necessario eseguirne il backup insieme per verificarne la coerenza.

La stringa del nome del writer è "Sync Share service VSS writer".

L'ID del writer è D46BF321-FDBA-4A35-8EC3-454DF03BC86A.

## <a name="system-writer"></a>Writer di sistema

Il writer di sistema enumera tutti i file binari del sistema operativo e dei driver ed è necessario per il backup dello stato del sistema.

**Windows Server 2003 e Windows XP:** Questo writer non è supportato.

Questo writer viene eseguito come parte del servizio servizi di crittografia (CryptSvc). Il writer di sistema genera un elenco di file che contiene i file seguenti:

-   Tutti i file statici installati. Un file statico è un file elencato nel manifesto del componente con l'attributo del file **attributo writeableType** impostato su "static" o "". I file statici includono tutti i file protetti da Protezione risorse di Windows (WRP). Tuttavia, non tutti i file statici sono file protetti con WRP. Ad esempio, i file di gioco sono statici, ma non protetti da WRP, in modo che gli amministratori possano modificare le impostazioni di controllo padre.
-   Il contenuto della directory side-by-side di Windows (WinSxS), inclusi tutti i manifesti, i componenti facoltativi e i file Win32 di terze parti.
    > [!Note]  
    > Molti dei file nella directory% windir% \\ System32 sono collegamenti reali a file nella directory WinSxS.

     

-   Tutti i file PnP per i driver installati (di proprietà di PnP).
-   Tutti i servizi in modalità utente e i driver non PnP.
-   Tutti i cataloghi di proprietà di CryptSvc.

L'applicazione di ripristino è responsabile della disinstallazione dei file e del registro di sistema e dell'impostazione degli ACL in modo che corrispondano alla copia shadow di sistema. Per avere esito positivo, è necessario creare anche i collegamenti reali appropriati per il ripristino dello stato del sistema.

La stringa del nome del writer per questo writer è "System Writer".

L'ID writer per il writer di sistema è E8132975-6F93-4464-A53E-1050253AE220.

## <a name="task-scheduler-writer"></a>Writer di Utilità di pianificazione

Questo writer segnala i file delle attività dell'utilità di pianificazione.

**Windows server 2008, Windows Vista, Windows server 2003 e Windows XP:** Questo writer non è supportato. I richiedenti sono necessari per eseguire manualmente il backup di questi file. (Vedere [backup e ripristino dello stato del sistema](locating-additional-system-files.md)).

La stringa del nome del writer per questo writer è "Utilità di pianificazione writer".

L'ID del writer per il writer è D61D61C8-D73A-4EEE-8CDD-F6F9786B7124.

## <a name="vss-metadata-store-writer"></a>Writer archivio metadati VSS

Questo writer segnala i file di metadati del writer per tutti i writer VSS Express.

**Windows server 2008, Windows Vista, Windows server 2003 e Windows XP:** Questo writer non è supportato.

La stringa del nome del writer per questo writer è "writer dell'archivio di metadati di VSS Express writer".

L'ID del writer per il writer è 75DFB225-E2E4-4D39-9AC9-FFAFF65DDF06.

## <a name="windows-deployment-services-wds-writer"></a>Writer di servizi di distribuzione Windows (WDS)

Questo writer segnala i file di dati di servizi di distribuzione Windows (WDS).

**Windows server 2008, Windows Vista, Windows server 2003 e Windows XP:** Questo writer non è supportato.

La stringa del nome del writer per questo writer è "WDS VSS Writer".

L'ID del writer per questo writer è 82CB5521-68DB-4626-83A4-7FC6F88853E9.

## <a name="windows-internal-database-wid-writer"></a>Writer database interno di Windows (WID)

Questo writer segnala i file di dati del database interno di Windows (WID).

**Windows server 2008 R2, Windows 7, Windows server 2008, Windows Vista, Windows server 2003 e Windows XP:** Questo writer non è supportato.

La stringa del nome del writer per questo writer è "WIDWriter".

L'ID del writer per questo writer è 8D5194E1-E455-434A-B2E5-51296CCE67DF.

## <a name="windows-internet-name-service-wins-writer"></a>Writer WINS (Windows Internet Name Service)

Questo writer è responsabile dell'enumerazione dei file richiesti per WINS.

**Windows XP:** Questo writer non è supportato.

La stringa del nome del writer per questo writer è "WINS Jet writer".

L'ID del writer per questo writer è F08C1483-8407-4A26-8C26-6C267A629741.

## <a name="wmi-writer"></a>Writer WMI

Questo writer viene utilizzato per identificare lo stato e i dati specifici di WMI durante le operazioni di backup. I dati includono i file del repository WBEM.

**Windows Server 2003 e Windows XP:** Questo writer non è supportato.

La stringa del nome del writer per questo writer è "WMI writer".

L'ID del writer per questo writer è A6AD56C2-B509-4E6C-BB19-49D8F43532F0.

 

 
