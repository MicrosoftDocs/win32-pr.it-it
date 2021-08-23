---
description: Il sistema operativo Windows include un set di VSS writer responsabili dell'enumerazione dei dati necessari alle varie funzionalità Windows. Questi sono definiti writer &\# 0034;in-box&\# 0034; writer.
ms.assetid: e20a303d-9440-42be-b383-85f6fad89157
title: VSS writer inclusi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0e34591cb046a8cc702d32452c159e5b8877f2e66603cbd1b048a0841a04e3bc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119767801"
---
# <a name="in-box-vss-writers"></a>VSS writer inclusi

Il sistema operativo Windows include un set di VSS writer responsabili dell'enumerazione dei dati necessari alle varie funzionalità Windows. Questi sono definiti writer "in box".

> [!Note]  
> Il writer di msde in-box non è disponibile in Windows Vista, Windows Server 2008 e versioni successive. È invece necessario usare SQL Writer per eseguire il backup SQL Server database. Solo SQL Server 2005 SP2 e versioni successive sono supportati in Windows Vista, Windows Server 2008 e versioni successive.

 

-   [Active Directory Domain Services (NTDS) VSS Writer](#active-directory-domain-services-ntds-vss-writer)
-   [Active Directory Federation Services Writer](#active-directory-federation-services-writer)
-   [Active Directory Lightweight Directory Services (LDS) VSS Writer](#active-directory-lightweight-directory-services-lds-vss-writer)
-   [Active Directory Rights Management Services (AD RMS) Writer](#active-directory-rights-management-services-ad-rms-writer)
-   [Writer Ripristino di sistema (ASR)](#automated-system-recovery-asr-writer)
-   [Servizio trasferimento intelligente in background writer (BITS)](#background-intelligent-transfer-service-bits-writer)
-   [Writer autorità di certificazione](#certificate-authority-writer)
-   [Writer del servizio cluster](#cluster-service-writer)
-   [Volume condiviso cluster (CSV) VSS Writer](#cluster-shared-volume-csv-vss-writer)
-   [Writer del database di registrazione classi COM+](#com-class-registration-database-writer)
-   [Writer di deduplicazione dati](#data-deduplication-writer)
-   [Replica DFS (Distributed File System)](#distributed-file-system-replication-dfsr)
-   [Dynamic Host Configuration Protocol (DHCP) Writer](#dynamic-host-configuration-protocol-dhcp-writer)
-   [Servizio Replica file](#file-replication-service-frs)
-   [File Server Resource Manager (FSRM) Writer](#file-server-resource-manager-fsrm-writer)
-   [Hyper-V Writer](#hyper-v-writer)
-   [Writer di configurazione IIS](#iis-configuration-writer)
-   [IIS Metabase Writer](#iis-metabase-writer)
-   [Microsoft Message Queuing (MSMQ) Writer](#microsoft-message-queuing-msmq-writer)
-   [Writer del servizio MSSearch](#mssearch-service-writer)
-   [Vss Writer di Server dei criteri di rete](#nps-vss-writer)
-   [Writer dei contatori delle prestazioni](#performance-counters-writer)
-   [Writer del Registro di sistema](#registry-writer)
-   [vss writer del gateway di Servizi Desktop remoto (Servizi terminal)](#remote-desktop-services-terminal-services-gateway-vss-writer)
-   [Servizi Desktop remoto (Servizi terminal) Licensing VSS Writer](#remote-desktop-services-terminal-services-licensing-vss-writer)
-   [Writer di ottimizzazione copia shadow](#shadow-copy-optimization-writer)
-   [Writer del servizio di condivisione di sincronizzazione](#sync-share-service-writer)
-   [Writer di sistema](#system-writer)
-   [Utilità di pianificazione Writer](#task-scheduler-writer)
-   [Writer dell'archivio dei metadati vss](#vss-metadata-store-writer)
-   [Windows Writer di Servizi di distribuzione (WDS)](#windows-deployment-services-wds-writer)
-   [Database interno di Windows writer (WID)](#windows-internal-database-wid-writer)
-   [Windows Writer WINS (Internet Name Service)](#windows-internet-name-service-wins-writer)
-   [WMI Writer](#wmi-writer)

## <a name="active-directory-domain-services-ntds-vss-writer"></a>Active Directory Domain Services (NTDS) VSS Writer

Questo writer segnala il file di database NTDS (ntds.dit) e i file di log associati. Questi file sono necessari per ripristinare correttamente Active Directory.

Esiste un solo file ntds.dit per ogni controller di dominio e viene segnalato nei metadati del writer come nell'esempio seguente:

``` syntax
    <DATABASE_FILES path="C:\Windows\NTDS" 
                     filespec="ntds.dit" 
                     filespecBackupType="3855"/>
```

Di seguito è riportato un esempio che illustra come elencare i componenti nei metadati del writer:

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

In fase di backup, il writer imposta l'ora di scadenza del backup nei metadati di backup del writer. I richiedenti devono recuperare questi metadati usando [**IVssComponent::GetBackupMetadata**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getbackupmetadata) per determinare se il database è scaduto. I database scaduti non possono essere ripristinati.

Se il computer che contiene il database NTDS è un controller di dominio, l'applicazione di backup deve sempre eseguire un backup dello stato del sistema in tutti i volumi contenenti informazioni critiche sullo stato del sistema. In fase di ripristino, l'applicazione deve prima riavviare il computer in modalità ripristino servizi directory e quindi eseguire un ripristino dello stato del sistema.

La stringa del nome del writer per questo writer è "NTDS".

L'ID writer per questo writer è B2014C9E-8711-4C5C-A5A9-3CF384484757.

## <a name="active-directory-federation-services-writer"></a>Active Directory Federation Services Writer

Questo writer segnala i file Active Directory Federation Services (ADFS).

**Windows Server 2008 R2, Windows 7, Windows Server 2008, Windows Vista, Windows Server 2003 e Windows XP:** Questo writer non è supportato.

La stringa del nome del writer per questo writer è "ADFS VSS Writer".

L'ID writer per questo writer è 772C45F8-AE01-4F94-940C-94961864ACAD.

## <a name="active-directory-lightweight-directory-services-lds-vss-writer"></a>Active Directory Lightweight Directory Services (LDS) VSS Writer

Questo writer segnala il file di database ADAM (adamntds.dit) e i file di log associati per ogni istanza in %program files% Microsoft ADAM instance N data, dove N è il numero di istanza \\ \\  \\ ADAM.  Questi file di log del database sono necessari per ripristinare le istanze di ADAM.

**Windows XP:** Questo writer non è supportato.

Di seguito è riportato un esempio che illustra come elencare i componenti nei metadati del writer:

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

In fase di backup, il writer imposta l'ora di scadenza del backup nei metadati di backup. Le applicazioni di backup devono recuperare questi metadati usando il [**metodo IVssComponent::GetBackupMetadata**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getbackupmetadata) per determinare se il database è scaduto. I database scaduti non possono essere ripristinati.

La stringa del nome del writer per questo writer è "ADAM (istanza *N*) Writer", dove *N* è il numero di istanza ADAM, ad esempio "ADAM (istanza1) Writer", "ADAM (istanza2) Writer" e così via.

L'ID writer per questo writer è DD846AAA-A1B6-42A8-AAF8-03DCB6114BFD. Questo ID writer è lo stesso per tutte le istanze.

## <a name="active-directory-rights-management-services-ad-rms-writer"></a>Active Directory Rights Management Services (AD RMS) Writer

Questo writer segnala i file di dati Active Directory Rights Management Service (AD RMS).

**Windows Server 2008 R2, Windows 7, Windows Server 2008, Windows Vista, Windows Server 2003 e Windows XP:** Questo writer non è supportato.

La stringa del nome del writer per questo writer è "AD RMS Writer".

L'ID writer per questo writer è 886C43B1-D455-4428-A37F-4D6B9E43F50F.

## <a name="automated-system-recovery-asr-writer"></a>Writer Ripristino di sistema (ASR)

Il writer asr archivia la configurazione dei dischi nel sistema. Questo writer segnala il database di configurazione di avvio (BCD) ed è anche responsabile dello smontaggio dell'hive del Registro di sistema che rappresenta il database di configurazione di avvio durante la creazione della copia shadow. Il writer asr deve essere incluso in tutti i backup necessari per il ripristino bare metal. Per altre informazioni sul ripristino di emergenza, vedere [Using VSS Automated Ripristino di sistema for Disaster Recovery](using-vss-automated-system-recovery-for-disaster-recovery.md).

**Windows Server 2003 e Windows XP:** Questo writer non è supportato.

La stringa del nome del writer per questo writer è "ASR Writer".

L'ID writer per il writer ASR è BE000CBE-11FE-4426-9C58-531AA6355FC4.

## <a name="background-intelligent-transfer-service-bits-writer"></a>Servizio trasferimento intelligente in background writer (BITS)

Il writer BITS usa la **chiave del Registro di sistema FilesNotToBackup** per escludere i file dalla cartella della cache BITS. Il percorso predefinito della cache è %AllUsersProfile% \\ Microsoft \\ Network \\ Downloader \\ Cache.

**Windows Server 2003 e Windows XP:** Questo writer non è supportato.

Il writer BITS esclude inoltre i file seguenti dal backup: i file di stato BITS (qmgr0.dat e qmgr1.dat), il file di log di debug BITS e i file parzialmente scaricati da BITS.

Se il file di destinazione del download BITS è un file SMB, l'account client deve avere una relazione di trust con il server oppure i backup potrebbero non riuscire.

La stringa del nome del writer per questo writer è "BITS Writer".

L'ID writer per il writer BITS è 4969D978-BE47-48B0-B100-F328F07AC1E0.

## <a name="certificate-authority-writer"></a>Writer autorità di certificazione

Questo writer è responsabile dell'enumerazione dei file di dati per il server dei certificati.

La stringa del nome del writer per questo writer è "Autorità di certificazione".

**Windows XP:** La stringa del nome del writer per questo writer è "Certificate Server Writer".

L'ID writer per il writer è 6F5B15B5-DA24-4D88-B737-63063E3A1F86.

## <a name="cluster-service-writer"></a>Writer del servizio cluster

Il servizio cluster VSS writer è documentato nella documentazione dell'API [del Servizio](/previous-versions/windows/desktop/mscs/backing-up-and-restoring-the-failover-cluster-configuration-using-vss) cluster.

**Windows Vista, Windows Server 2003 e Windows XP:** Questo writer non è supportato fino Windows Vista con Service Pack 1 (SP1) e Windows Server 2008.

## <a name="cluster-shared-volume-csv-vss-writer"></a>Volume condiviso cluster (CSV) VSS Writer

Questo writer segnala i Volume condiviso cluster file di dati (CSV). Questo writer è un writer in-box per le Windows del sistema operativo Server; non viene spedito in Windows Client.

**Windows Server 2008 R2, Windows Server 2008 e Windows Server 2003:** Questo writer non è supportato.

La stringa del nome del writer per questo writer è "Volume condiviso cluster VSS Writer".

L'ID writer per il writer è 1072AE1C-E5A7-4EA1-9E4A-6F7964656570.

## <a name="com-class-registration-database-writer"></a>Writer del database di registrazione classi COM+

Questo writer è responsabile del contenuto della directory %SystemRoot% \\ Registration. Il catalogo COM+ è un file in %SystemRoot% Registration con un nome che segue il modello \\ R *xxxxxxxxxxxxxx*.clb, dove *xxxxxxxxxxxx è* un numero esadecimale di 12 cifre. Possono essere presenti potenzialmente più file di questo tipo se nel computer sono state configurate applicazioni COM+. Il file che contiene il catalogo COM+ corrente è il file con il valore più grande *xxxxxxxxxxxx*.

**Windows Server 2003 e Windows XP:** Questo writer non è supportato.

Il database di registrazione della classe COM+ dipende da una chiave del Registro di sistema di cui viene eseguito il backup e quindi deve essere eseguito il backup e il ripristino insieme al Registro di sistema.

Per ripristinare il database di registrazione COM+, un'applicazione di backup (richiedente) deve chiamare il [**metodo ICOMAdminCatalog::RestoreREGDB.**](/windows/win32/api/comadmin/nf-comadmin-icomadmincatalog-restoreregdb)

La stringa del nome del writer per questo writer è "COM+ REGDB Writer".

L'ID writer per il writer del database di registrazione della classe COM+ è 542DA469-D3E1-473C-9F4F-7847F01FC64F.

## <a name="data-deduplication-writer"></a>Writer di deduplicazione dati

Il VSS writer deduplicazione dati è documentato nella documentazione dell'API [Deduplicazione](/previous-versions/windows/desktop/dedup/backup-and-restore-of-data-deduplication-enabled-volumes) dati. Questo writer è un writer in-box per le Windows del sistema operativo Server; non viene spedito in Windows Client.

**Windows Server 2008 R2, Windows Server 2008 e Windows Server 2003:** Questo writer non è supportato.

## <a name="distributed-file-system-replication-dfsr"></a>Replica DFS (Distributed File System)

Il componente seguente include un VSS writer: [replica file system distribuito (DFSR)](/previous-versions/windows/desktop/dfsr/dfsr-replicated-folders)

**Windows Vista, Windows Server 2003 e Windows XP:** Questo writer non è supportato fino Windows Vista con SP1 e Windows Server 2008.

## <a name="dynamic-host-configuration-protocol-dhcp-writer"></a>Dynamic Host Configuration Protocol (DHCP) Writer

Questo writer è responsabile dell'enumerazione dei file necessari per il ruolo del server DHCP. Questo writer è un writer in-box per le Windows del sistema operativo Server; non viene spedito in Windows Client.

La stringa del nome del writer per questo writer è "Dhcp Jet Writer".

L'ID writer per questo writer è BE9AC81E-3619-421F-920F-4C6FEA9E93AD.

## <a name="file-replication-service-frs"></a>Servizio Replica file

Il writer del servizio Replica file è documentato in Backup e ripristino di una FRS-Replicated [SYSVOL](backing-up-and-restoring-an-frs-replicated-sysvol-folder.md).

**Windows Vista, Windows Server 2003 e Windows XP:** Questo writer non è supportato fino Windows Vista con SP1 e Windows Server 2008.

## <a name="file-server-resource-manager-fsrm-writer"></a>File Server Resource Manager (FSRM) Writer

Questo writer enumera i file di configurazione fsrm usati per il backup dello stato del sistema. Durante le operazioni di ripristino, impedisce le modifiche nella configurazione di GESTIONE FS E interrompe temporaneamente l'applicazione di quote e screening dei file. Al termine del ripristino, il writer aggiorna FSRM con la configurazione ripristinata. Questo writer è presente solo quando FSRM (parte del ruolo Servizi file) è installato e in esecuzione. Questo writer è un writer in-box per le Windows del sistema operativo Server; non viene spedito in Windows Client.

**Windows Server 2003:** Questo writer non è supportato fino a Windows Server 2003 R2.

La stringa del nome del writer per questo writer è "FSRM Writer".

L'ID writer per questo writer è 12CE4370-5BB7-4C58-A76A-E5D5097E3674.

## <a name="hyper-v-writer"></a>Hyper-V Writer

Il VSS writer Hyper-V è documentato nella documentazione [dell'API Hyper-V.](/previous-versions/windows/desktop/virtual/backing-up-and-restoring-virtual-machines) Questo writer è un writer in-box per le Windows del sistema operativo Server; non viene spedito in Windows Client.

**Windows Server 2003:** Questo writer non è supportato fino a Windows Server 2008.

## <a name="iis-configuration-writer"></a>Writer di configurazione IIS

Il writer di configurazione IIS è responsabile dell'enumerazione dei file di configurazione di IIS.

**Windows Vista, Windows Server 2003 e Windows XP:** Questo writer non è supportato fino Windows Vista con SP1 e Windows Server 2008. I richiedenti devono eseguire il backup dei file di configurazione di IIS, incluso il file fx machine.config .NET o il file ASP.NET radice web.config file.

Questo writer non esegue il backup del file fx machine.config .NET o del file web.config radice ASP.NET perché questi file vengono enumerati dal writer di sistema.

Questo writer esegue il backup di tutti i file presenti nello schema di configurazione %windir% \\ system32 \\ inetsrv \\ \\ e %windir% \\ system32 \\ inetsrv \\ config directory, ad eccezione dei file enumerati dal writer di sistema.

L'ID writer per il writer di configurazione IIS è 2A40FD15-DFCA-4aa8-A654-1F8C654603F6.

## <a name="iis-metabase-writer"></a>IIS Metabase Writer

Il writer della metabase di Internet Information Server (IIS) è responsabile dell'enumerazione del file della metabase IIS.

**Windows Vista, Windows Server 2003 e Windows XP:** Questo writer non è supportato fino Windows Vista con SP1 e Windows Server 2008. I richiedenti devono eseguire il backup del file della metabase IIS.

L'ID writer per il writer della metabase IIS è 59B1f0CF-90EF-465F-9609-6CA8B2938366.

## <a name="microsoft-message-queuing-msmq-writer"></a>Microsoft Message Queuing (MSMQ) Writer

Questo writer segnala i Microsoft Message Queuing (MSMQ).

**Windows Server 2008 R2, Windows 7, Windows Server 2008, Windows Vista, Windows Server 2003 e Windows XP:** Questo writer non è supportato.

La stringa del nome del writer per questo writer è "MSMQ Writer (*SvcName*)", dove *SvcName* è il nome del servizio MSMQ a cui è associato il writer. Per l'installazione predefinita, il nome del servizio è "MSMQ". Per le istanze del cluster, il nome del servizio è MSMQ$*ResourceName*, dove *ResourceName* è il nome della risorsa MSMQ in cluster.

L'ID writer per questo writer è 7E47B561-971A-46E6-96B9-696EEEAA53B2A.

## <a name="mssearch-service-writer"></a>Writer del servizio MSSearch

Questo writer esiste per eliminare i file di indice di ricerca dalle copie shadow dopo la creazione. Questa operazione viene eseguita per ridurre al minimo l'impatto dell'I/O di copia su scrittura durante le normali operazioni di I/O su questi file sul volume copiato shadow.

**Windows Server 2003:** Questo writer non è supportato.

Per installare questo writer nel server, è necessario installare il ruolo Servizi file e abilitare il Windows Di ricerca.

La stringa del nome del writer per questo writer è "MSSearch Service Writer".

L'ID writer per il writer del servizio MSSearch è CD3F2362-8BEF-46C7-9181-D62844CDC0B2.

## <a name="nps-vss-writer"></a>Vss Writer di Server dei criteri di rete

Il writer del server dei criteri di rete è responsabile dell'enumerazione dei file di configurazione del server dei criteri di rete per i server in cui sono installati i criteri di rete e il ruolo Access Services rete.

**Windows Vista, Windows Server 2003 e Windows XP:** Questo writer non è supportato fino Windows Vista con SP1 e Windows Server 2008.

La stringa del nome del writer per questo writer è "NPS VSS Writer".

L'ID writer per il VSS writer NPS è 0x35E81631-13E1-48DB-97FC-D5BC721BB18A.

## <a name="performance-counters-writer"></a>Writer dei contatori delle prestazioni

Questo writer segnala i file di configurazione del contatore delle prestazioni. Questi file vengono modificati solo durante l'installazione dell'applicazione e devono essere sottoposti a backup e ripristino durante i backup e i ripristini dello stato del sistema.

**Windows Server 2008, Windows Vista, Windows Server 2003 e Windows XP:** Questo writer non è supportato. I richiedenti devono eseguire manualmente il backup di questi file. Vedere [Backup e ripristino dello stato del sistema.](locating-additional-system-files.md)

La stringa del nome del writer per questo writer è "Performance Counters Writer".

L'ID writer per il writer dei contatori delle prestazioni è 0BADA1DE-01A9-4625-8278-69E735F39DD2.

## <a name="registry-writer"></a>Writer del Registro di sistema

Il writer del Registro di sistema segnala Windows file del Registro di sistema per abilitare i backup e i ripristini sul posto del Registro di sistema. Non segnala gli hive utente.

**Windows Server 2003:** In Windows Server 2003, questo writer usa un file di repository intermedio (talvolta denominato "file di sput") per archiviare i dati del Registro di sistema. Vedere Operazioni [di backup e ripristino del Registro di sistema in VSS.](registry-backup-and-restore-operations-under-vss.md)

**Windows XP:** Questo writer non è supportato. Vedere Operazioni [di backup e ripristino del Registro di sistema in VSS.](registry-backup-and-restore-operations-under-vss.md)

La stringa del nome del writer per questo writer è "Registry Writer".

L'ID writer per il writer del Registro di sistema è AFBAB4A2-367D-4D15-A586-71DBB18F8485.

## <a name="remote-desktop-services-terminal-services-gateway-vss-writer"></a>vss writer del gateway di Servizi Desktop remoto (Servizi terminal)

Questo writer è responsabile dell'enumerazione dei file del gateway Servizi Desktop remoto (Servizi terminal) per i server in cui è installato Desktop remoto Gateway, un sottoruolo di Servizi Desktop remoto ruolo.

**Windows Server 2003:** Questo writer non è supportato.

Questo writer è un writer in-box per le Windows del sistema operativo Server; non viene spedito in Windows Client.

Il Servizi Desktop remoto gateway dipende da diverse chiavi del Registro di sistema di cui viene eseguito il backup e pertanto deve essere eseguito il backup e il ripristino insieme al Registro di sistema.

La stringa del nome del writer per questo writer è "TS Gateway Writer".

L'ID writer per questo writer è 368753EC-572E-4FC7-B4B9-CCD9BDC624CB.

## <a name="remote-desktop-services-terminal-services-licensing-vss-writer"></a>Servizi Desktop remoto (Servizi terminal) Licensing VSS Writer

Questo writer è responsabile dell'enumerazione dei file delle licenze Servizi Desktop remoto (Licenze Desktop remoto) o licenze Servizi terminal per i server in cui è installato Desktop remoto Licensing, un sottoruolo di Servizi Desktop remoto.

**Windows Server 2003:** Questo writer non è supportato.

Questo writer è un writer in-box per le Windows del sistema operativo Server; non è disponibile in Windows Client.

Servizi Desktop remoto licenze dipende da diverse chiavi del Registro di sistema di cui viene eseguito il backup e pertanto deve essere eseguito il backup e il ripristino insieme al Registro di sistema.

La stringa del nome del writer per questo writer è "TermServLicensing".

L'ID writer per questo writer è 5382579C-98DF-47A7-AC6C-98A6D7106E09.

## <a name="shadow-copy-optimization-writer"></a>Writer di ottimizzazione copia shadow

Questo writer elimina determinati file dalle copie shadow del volume. Questa operazione viene eseguita per ridurre al minimo l'impatto dell'I/O di copia su scrittura durante le normali operazioni di I/O su questi file sul volume copiato shadow. I file eliminati sono in genere file temporanei o file che non contengono lo stato utente o di sistema.

**Windows Server 2003 e Windows XP:** Questo writer non è supportato.

La stringa del nome del writer per questo writer è "Shadow Copy Optimization Writer".

L'ID writer per il writer di ottimizzazione della copia shadow è 4DC3BDD4-AB48-4D07-ADB0-3BEE2926FD7F.

## <a name="sync-share-service-writer"></a>Writer del servizio di condivisione di sincronizzazione

**Windows Server 2012 R2:** Questo writer è incluso in Windows Server 2012 R2 e versioni più recenti del server. Non è compatibile con le versioni desktop.

Questo writer è responsabile dell'enumerazione delle condivisioni di sincronizzazione nei server in cui è installato il servizio di condivisione di sincronizzazione e di garantire che i metadati e i dati rimangano coerenti durante il backup e il ripristino.

Questo writer è presente solo quando il servizio di condivisione di sincronizzazione è installato e in esecuzione.

Sarà presente un componente VSS writer per ogni condivisione di sincronizzazione. Sono inclusi i metadati e i percorsi dei dati. È necessario eseguire il backup insieme per garantire la coerenza.

La stringa del nome del writer è "Sync Share Service VSS writer".

L'ID writer è D46BF321-FDBA-4A35-8EC3-454DF03BC86A.

## <a name="system-writer"></a>Writer di sistema

Il writer di sistema enumera tutti i file binari del sistema operativo e dei driver ed è necessario per un backup dello stato del sistema.

**Windows Server 2003 e Windows XP:** Questo writer non è supportato.

Questo writer viene eseguito come parte del servizio Cryptographic Services (CryptSvc). Il writer di sistema genera un elenco di file che contiene i file seguenti:

-   Tutti i file statici installati. Un file statico è un file elencato nel manifesto del componente con l'attributo del file **writeableType** impostato su "static" o "". I file statici includono tutti i file protetti da Windows Resource Protection (WRP). Tuttavia, non tutti i file statici sono file protetti da WRP. Ad esempio, i file di gioco sono statici ma non protetti da WRP in modo che gli amministratori possano modificare le impostazioni di Controllo genitori.
-   Contenuto della directory Windows side-by-side (WinSxS), inclusi tutti i manifesti, i componenti facoltativi e i file Win32 di terze parti.
    > [!Note]  
    > Molti dei file nella directory %windir% system32 sono collegamenti rigidi ai \\ file nella directory WinSxS.

     

-   Tutti i file PnP per i driver installati (di proprietà di PnP).
-   Tutti i servizi in modalità utente e i driver non PnP.
-   Tutti i cataloghi di proprietà di CryptSvc.

L'applicazione di ripristino è responsabile del layout dei file e del Registro di sistema e dell'impostazione degli ACL in modo che corrispondano alla copia shadow del sistema. Per un ripristino dello stato del sistema, è necessario creare anche i collegamenti rigidi appropriati.

La stringa del nome del writer per questo writer è "System Writer".

L'ID writer per il writer di sistema è E8132975-6F93-4464-A53E-1050253AE220.

## <a name="task-scheduler-writer"></a>Utilità di pianificazione Writer

Questo writer segnala i file di attività dell'utilità di pianificazione.

**Windows Server 2008, Windows Vista, Windows Server 2003 e Windows XP:** Questo writer non è supportato. I richiedenti devono eseguire manualmente il backup di questi file. Vedere [Backup e ripristino dello stato del sistema.](locating-additional-system-files.md)

La stringa del nome del writer per questo writer è "Utilità di pianificazione Writer".

L'ID writer per il writer è D61D61C8-D73A-4EEE-8CDD-F6F9786B7124.

## <a name="vss-metadata-store-writer"></a>Writer dell'archivio dei metadati vss

Questo writer segnala i file di metadati del writer per tutti gli express writer vss.

**Windows Server 2008, Windows Vista, Windows Server 2003 e Windows XP:** Questo writer non è supportato.

La stringa del nome del writer per questo writer è "VSS Express Writer Metadata Store Writer".

L'ID writer per il writer è 75DFB225-E2E4-4D39-9AC9-FFAFF65DDF06.

## <a name="windows-deployment-services-wds-writer"></a>Windows Writer di Servizi di distribuzione (WDS)

Questo writer segnala i Windows di dati di Servizi di distribuzione windows (WDS).

**Windows Server 2008, Windows Vista, Windows Server 2003 e Windows XP:** Questo writer non è supportato.

La stringa del nome del writer per questo writer è "WDS VSS Writer".

L'ID writer per questo writer è 82CB5521-68DB-4626-83A4-7FC6F88853E9.

## <a name="windows-internal-database-wid-writer"></a>Database interno di Windows writer (WID)

Questo writer segnala i Database interno di Windows (WID).

**Windows Server 2008 R2, Windows 7, Windows Server 2008, Windows Vista, Windows Server 2003 e Windows XP:** Questo writer non è supportato.

La stringa del nome del writer per questo writer è "WIDWriter".

L'ID writer per questo writer è 8D5194E1-E455-434A-B2E5-51296CCE67DF.

## <a name="windows-internet-name-service-wins-writer"></a>Windows Writer WINS (Internet Name Service)

Questo writer è responsabile dell'enumerazione dei file necessari per WINS.

**Windows XP:** Questo writer non è supportato.

La stringa del nome del writer per questo writer è "WINS Jet Writer".

L'ID writer per questo writer è F08C1483-8407-4A26-8C26-6C267A629741.

## <a name="wmi-writer"></a>WMI Writer

Questo writer viene usato per identificare lo stato e i dati specifici di WMI durante le operazioni di backup. I dati includono i file del repository WBEM.

**Windows Server 2003 e Windows XP:** Questo writer non è supportato.

La stringa del nome del writer per questo writer è "WMI Writer".

L'ID writer per questo writer è A6AD56C2-B509-4E6C-BB19-49D8F43532F0.

 

 
