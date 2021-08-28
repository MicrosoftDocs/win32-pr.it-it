---
description: Questo argomento illustra come determinare se una cartella SYSVOL viene replicata da DFSR o FSR e illustra come eseguire il backup e il ripristino di una cartella SYSVOL replicata da FRS.
ms.assetid: 32d8a5bd-eeb4-4db6-8129-b5cd3508a7e5
title: Backup e ripristino di una FRS-Replicated sysvol
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6d841f64bab62114824847f91876ba8bbffbb0166db942c0f3cb9d010b72f106
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120124601"
---
# <a name="backing-up-and-restoring-an-frs-replicated-sysvol-folder"></a>Backup e ripristino di una FRS-Replicated sysvol

La cartella Del volume di sistema (SYSVOL) fornisce un percorso standard per archiviare elementi importanti [di](/previous-versions/windows/it-pro/windows-server-2003/cc779838(v=ws.10)) Criteri di gruppo e script. In ogni controller di dominio di un dominio è presente una copia della cartella SYSVOL. La cartella SYSVOL viene replicata da [Replica file system distribuito (DFSR)](/windows-server/storage/dfs-replication/migrate-sysvol-to-dfsr) o dal servizio Replica file [(FRS).](/previous-versions/windows/it-pro/windows-server-2003/cc781582(v=ws.10)) Questo argomento illustra come determinare se una cartella SYSVOL viene replicata da DFSR o FSR e illustra come eseguire il backup e il ripristino di una cartella SYSVOL replicata da FRS.

Il servizio Replica file può copiare il contenuto di SYSVOL in altri controller di dominio all'interno del dominio. FrS monitora la cartella SYSVOL e, se si verifica una modifica a qualsiasi file archiviato nella cartella SYSVOL, frs replica automaticamente il file modificato nelle cartelle SYSVOL negli altri controller di dominio nel dominio.

> [!Note]  
> Solo il Criteri di gruppo viene replicato replicando il contenuto della cartella SYSVOL. Il Criteri di gruppo contenitore viene replicato tramite la replica di Active Directory. Per Criteri di gruppo, il modello di Criteri di gruppo e il contenitore Criteri di gruppo devono essere disponibili in un controller di dominio.

 

In questo argomento vengono trattati gli argomenti seguenti:

-   [Determinazione della replica della cartella SYSVOL di un controller di dominio tramite replica DFS o frs](#determining-whether-a-domain-controllers-sysvol-folder-is-replicated-by-dfsr-or-frs)
-   [Backup di una DFSR-Replicated SYSVOL](#backing-up-a-dfsr-replicated-sysvol-folder)
-   [Backup di una FRS-Replicated SYSVOL in un dominio Windows Server 2008 o Windows Server 2003](#backing-up-an-frs-replicated-sysvol-folder-on-a-windows-server-2008-or-windows-server-2003-domain)
-   [Documento di metadati del writer FRS di esempio](#sample-frs-writer-metadata-document)
-   [Impostazione delle chiavi del Registro di sistema per un ripristino di FRS-Replicated cartella SYSVOL](#setting-registry-keys-for-a-restore-of-an-frs-replicated-sysvol-folder)
-   [Esecuzione di un ripristino non autorevole di una FRS-Replicated sysvol](#performing-a-nonauthoritative-restore-of-an-frs-replicated-sysvol-folder)
-   [Esecuzione di un ripristino autorevole di una FRS-Replicated sysvol](#performing-an-authoritative-restore-of-an-frs-replicated-sysvol-folder)

## <a name="determining-whether-a-domain-controllers-sysvol-folder-is-replicated-by-dfsr-or-frs"></a>Determinazione della replica della cartella SYSVOL di un controller di dominio tramite replica DFS o frs

La tabella seguente riepiloga come determinare se la cartella SYSVOL di un controller di dominio viene replicata da [replica DFS](/windows-server/storage/dfs-replication/migrate-sysvol-to-dfsr) o frs.

| Se il controller di dominio è in esecuzione                                                                                                                  | SYSVOL viene replicato da |
|------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------|
| Windows Server 2008 + livello di funzionalità del dominio di Windows Server 2008 + [MIGRAZIONE SYSVOL completata](https://blogs.technet.com/filecab/archive/2008/02/08/sysvol-migration-series-part-1-introduction-to-the-sysvol-migration-process.aspx) | DFSR                    |
| Windows Server 2008 + livello di funzionalità del dominio inferiore Windows Server 2008                                                                              | Frs                     |
| Windows Server 2003                                                                                                                                  | Frs                     |



 

Se il livello [](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc754918(v=ws.10)) di funzionalità del dominio è Windows Server 2008 e il dominio è stato sottoposto a migrazione [SYSVOL,](https://blogs.technet.com/filecab/archive/2008/02/08/sysvol-migration-series-part-1-introduction-to-the-sysvol-migration-process.aspx) [DFSR](/windows-server/storage/dfs-replication/migrate-sysvol-to-dfsr) verrà usato per replicare la cartella SYSVOL. Se il primo controller di dominio nel dominio è stato alzato [](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc754918(v=ws.10))di livello direttamente al livello di funzionalità di Windows Server 2008, DFSR viene usato automaticamente per la replica SYSVOL. In questi casi, non è necessario eseguire la migrazione della replica SYSVOL dal servizio Replica file a Replica DFS. Se il dominio è stato aggiornato al livello di funzionalità di Windows Server 2008, il servizio Replica file viene usato per la replica SYSVOL fino al completamento del processo di migrazione dal servizio Replica file a Replica DFS. [](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc754918(v=ws.10)) [](https://blogs.technet.com/filecab/archive/2008/02/08/sysvol-migration-series-part-1-introduction-to-the-sysvol-migration-process.aspx)

Per determinare se DFSR o FRS viene usato in un controller di dominio che esegue Windows Server 2008, controllare il valore della sottochiave del Registro di sistema **HKEY \_ LOCAL \_ MACHINE** \\ **System** \\ **CurrentControlSet** \\ **Services** \\ **DFSR** \\ **Parameters** \\ **SysVols** \\ **Migrating Sysvols** \\ **LocalState** . Se questa sottochiave del Registro di sistema esiste e il relativo valore è impostato su 3 (ELIMINATO), viene usata [la replica DFS.](/windows-server/storage/dfs-replication/migrate-sysvol-to-dfsr) Se la sottochiave non esiste o ha un valore diverso, viene usato il servizio Replica file.

## <a name="backing-up-a-dfsr-replicated-sysvol-folder"></a>Backup di una DFSR-Replicated SYSVOL

Se la cartella SYSVOL viene replicata da [DFSR,](/windows-server/storage/dfs-replication/migrate-sysvol-to-dfsr)il VSS writer DFSR può essere usato per eseguire il backup. Per altre informazioni sulla replica DFS VSS writer, vedere Cartelle replicate [DFSR.](/previous-versions/windows/desktop/dfsr/dfsr-replicated-folders)

## <a name="backing-up-an-frs-replicated-sysvol-folder-on-a-windows-server-2008-or-windows-server-2003-domain"></a>Backup di una FRS-Replicated SYSVOL in un dominio Windows Server 2008 o Windows Server 2003

In un controller di dominio che esegue Windows Server 2008 o Windows Server 2003, l'infrastruttura VSS è presente e pertanto il VSS writer frs può essere usato per eseguire il backup della cartella SYSVOL e dei componenti frs.

Il documento di metadati VSS writer del servizio Replica file fornisce informazioni sul percorso della cartella SYSVOL e sugli elenchi di esclusione per il writer. In base a queste informazioni, un'applicazione di backup VSS (richiedente) può eseguire il backup della cartella SYSVOL usando le normali tecniche di backup basate su VSS.

Il documento di metadati del writer contiene informazioni sul writer, sui dati di proprietà del writer e su come ripristinare i dati. Si tratta di un documento di sola lettura che può essere recuperato dall'applicazione di backup prima di eseguire un backup. Lo [strumento DiskShadow](/previous-versions/windows/it-pro/windows-server-2012-R2-and-2012/cc772172(v=ws.11)) può essere usato per visualizzare il VSS writer dei metadati del writer del servizio Replica file. Il [comando DiskShadow list writers](/previous-versions/windows/it-pro/windows-server-2012-R2-and-2012/cc772172(v=ws.11)) fornisce informazioni sui writer presenti nel sistema. Questo elenco contiene informazioni sul writer FRS nei controller di dominio che usano il servizio Replica file per la replica SYSVOL o nei file server che usano il servizio Replica file per la replica delle destinazioni [di collegamento DFS.](/previous-versions/windows/it-pro/windows-server-2003/cc782417(v=ws.10))

La sezione documento di metadati del writer FRS di esempio seguente illustra un documento di metadati del writer FRS di esempio per un controller di dominio con la cartella SYSVOL in D: \\ Windows \\ Sysvol. Il percorso visualizzato nella sezione "File esclusi" sarà uguale a quello ottenuto quando si esegue una query sulla chiave del Registro di sistema **SysVol** del servizio Netlogon:

**HKEY \_ Local \_ MACHINE** \\ **System** \\ **CurrentControlSet** \\ **Services** \\ **NetLogon** \\ **Parameters** \\ **SysVol**

L'unica eccezione a questa regola si verifica quando il controller di dominio si trova nello stato REDIRECTED della [migrazione SYSVOL.](https://blogs.technet.com/filecab/archive/2008/02/08/sysvol-migration-series-part-1-introduction-to-the-sysvol-migration-process.aspx) In questo stato, i writer corrispondenti al servizio Replica file e al servizio [Replica DFS](/windows-server/storage/dfs-replication/migrate-sysvol-to-dfsr) segnalano le rispettive copie della cartella SYSVOL. Tuttavia, la copia della cartella SYSVOL del servizio [DFSR](/windows-server/storage/dfs-replication/migrate-sysvol-to-dfsr) (in genere una cartella denominata SYSVOL DFSR) è quella condivisa dal controller di dominio. Questo percorso è quello a cui fa riferimento la chiave del Registro di \_ **sistema SysVol.**

Il servizio Replica file VSS writer richiede un metodo di ripristino personalizzato. Ciò significa che determinati passaggi personalizzati devono essere eseguiti durante il ripristino dei file replicati dal servizio Replica file. Per altre informazioni, vedere Esecuzione di un ripristino non autorevole di una FRS-Replicated SYSVOL.

> [!Note]  
> I backup dello stato del sistema per i controller di dominio Windows non includono il database FRS che gestisce le informazioni sullo stato per il servizio FrS relative ai file all'interno della cartella SYSVOL e ad altri set di contenuto. Il database FRS, i log di debug, i file dell'area di gestione temporanea e i file nella cartella di dati [preesiste](/previous-versions/windows/it-pro/windows-server-2003/cc758169(v=ws.10)) vengono esclusi da un backup dello stato del sistema. La specifica del writer FRS di esempio seguente contiene l'elenco di esclusione nella sezione "File esclusi".

 

## <a name="sample-frs-writer-metadata-document"></a>Documento di metadati del writer FRS di esempio

Di seguito è riportato un documento di metadati del writer FRS di esempio per un controller di dominio il cui percorso della cartella SYSVOL è D: \\ Windows \\ Sysvol.

``` syntax
* WRITER "FRS Writer"
    - Writer ID   = {d76f5a28-3092-4589-ba48-2958fb88ce29}
    - Writer Instance ID = {07ae58e5-6977-4e34-9dfe-399bbd2cbe40}
    - Supports restore events = FALSE
    - Writer restore conditions = VSS_WRE_NEVER
    - Restore method = VSS_RME_CUSTOM
    - Requires reboot after restore = FALSE

    - Excluded files:
       - Exclude: Path = d:\windows\ntfrs\jet, Filespec = *
       - Exclude: Path = d:\Windows\debug\NtFrs, Filespec = NtFrs*
       - Exclude: Path = d:\windows\sysvol\domain\DO_NOT_REMOVE_NtFrs_PreInstall_Directory, Filespec = *
       - Exclude: Path = d:\windows\sysvol\domain\NtFrs_PreExisting___See_EventLog, Filespec = *
       - Exclude: Path = d:\windows\sysvol\staging\domain, Filespec = NTFRS_*

    - Component "FRS Writer:\SYSVOL\da45368c-b2d3-4cf0-bdc338a2cde15a7b"
       - Name: 'da45368c-b2d3-4cf0-bdc338a2cde15a7b'
       - Logical Path: 'SYSVOL'
       - Full Path: '\SYSVOL\da45368c-b2d3-4cf0-bdc338a2cde15a7b'
       - Caption: ''
       - Type: VSS_CT_FILEGROUP [2]
       - Is Selectable: 'TRUE'
       - Is top level: 'TRUE'
       - Notify on backup complete: 'TRUE'
       - Components:
       - File List: Path = d:\windows\sysvol, Filespec = *
       - Affected paths by this component:
         - d:\windows\sysvol
       - Affected volumes by this component:
         - \\?\Volume{da897ba5-5840-11db-93c1-806e6f6e6963}\ [D:\]
       - Component Dependencies:
```

## <a name="setting-registry-keys-for-a-restore-of-an-frs-replicated-sysvol-folder"></a>Impostazione delle chiavi del Registro di sistema per un ripristino di FRS-Replicated cartella SYSVOL

La chiave del Registro di sistema **BurFlags** viene usata per eseguire ripristini autorevoli o non autorevoli sui membri frs dei set di repliche DFS o SYSVOL. La chiave globale (a livello di computer) del Registro di sistema **BurFlags** contiene i valori DWORD REG e si trova nel \_ percorso seguente nel Registro di sistema:

**HKEY \_ Local \_ MACHINE** \\ **System** \\ **CurrentControlSet** \\ **Services** \\ **NtFrs** \\ **Parameters** \\ **Backup/Restore** \\ **Process at Startup**

I valori più comuni per la **chiave del Registro di sistema BurFlags** sono:

-   D2, noto anche come ripristino in modalità non autorevole.
-   D4, noto anche come ripristino in modalità autorevole.

Sono disponibili chiavi del Registro di sistema **BurFlags** globali e specifiche del set di repliche. L'impostazione della chiave globale del Registro di sistema **BurFlags** reinizializza tutti i set di repliche che il membro contiene. Questa chiave globale deve essere impostata quando il server contiene un solo set di repliche o quando i set di repliche che contiene sono relativamente pochi in numero e di dimensioni ridotte. Ad esempio, se il server è un controller di dominio che non ospita alcun set di contenuto replicato tramite frs diverso dalla cartella SYSVOL, è possibile impostare la chiave globale del Registro di sistema **BurFlags.**

La chiave globale del Registro di sistema **BurFlags** si trova nel percorso seguente nel Registro di sistema:

**HKEY \_ Local \_ MACHINE** \\ **System** \\ **CurrentControlSet** \\ **Services** \\ **NtFrs** \\ **Parameters** \\ **Backup/Restore** \\ **Process at Startup**

A differenza della chiave **globale BurFlags,** la chiave **BurFlags** specifica del set di repliche consente la nuova inizializzazione di singoli set di repliche discreti, consentendo di lasciare intatti i set di replica integri.

Le chiavi del Registro di **sistema BurFlags** specifiche del set di repliche possono essere individuate determinando il GUID per quel particolare set di repliche.

Nella procedura seguente viene descritto come determinare quale GUID corrisponde a un determinato set di repliche e come configurare un ripristino.

**Per determinare quale GUID corrisponde a un determinato set di repliche e per configurare un ripristino**

1.  Arrestare il servizio FrS.
2.  Per determinare il GUID che rappresenta un determinato set di repliche:
    1.  Individuare la chiave seguente nel Registro di sistema.

        **HKEY \_ Local \_ MACHINE System** \\  \\ **CurrentControlSet** Services \\  \\ **NtFrs** \\ **Parameters** \\ **Replica Sets**

    2.  Sotto la **sottochiave Set** di repliche sono presenti una o più sottochiavi identificate da un GUID.
    3.  Il **valore Replica Set Root** per ogni GUID è un file system che indica il set di repliche rappresentato da questo GUID.
    4.  Scorrere questo elenco di GUID fino a quando non viene individuato il set di repliche desiderato. Si noti il GUID corrispondente.

3.  Individuare la sottochiave seguente nel Registro di sistema:

    **HKEY \_ Local \_ MACHINE System** \\  \\ **CurrentControlSet** \\ **Services** \\ **NtFrs** \\ **Parameters** \\ **Cumulative Replica Sets**

4.  Sotto questa sottochiave individuare lo stesso GUID indicato nel passaggio 2. Sotto la sottochiave GUID creare una voce per la **chiave BurFlags.**
5.  Riavviare il servizio FrS.

## <a name="performing-a-nonauthoritative-restore-of-an-frs-replicated-sysvol-folder"></a>Esecuzione di un ripristino non autorevole di una FRS-Replicated SYSVOL

Il ripristino non autorevole è il modo più comune per reinizializzare la replica SYSVOL nei singoli controller di dominio. I controller di dominio ripristinati in modo non autorevole devono avere connessioni in ingresso da altri controller di dominio funzionanti, che partecipano alla replica di Active Directory e frs. In un ambiente di distribuzione di grandi dimensioni costituito da molti controller di dominio, i controller di dominio rimanenti possono essere ripristinati usando un ripristino in modalità non autorevole nelle condizioni seguenti:

-   Deve essere presente almeno un membro di replica noto , ovvero un controller di dominio con una cartella SYSVOL integra.
-   Gli altri controller di dominio devono essere reinizializzato nell'ordine dei partner di replica diretta.

Nella procedura seguente viene descritto come eseguire un ripristino non autorevole.

**Per eseguire un ripristino non autorevole**

1.  Arrestare il servizio FrS.
2.  Ripristinare i dati di cui è stato eseguito il backup nella cartella SYSVOL.
3.  Configurare la chiave del Registro di sistema **BurFlags** impostando il valore della chiave del Registro di sistema seguente sul valore DWORD D2.

    **HKEY \_ Local \_ MACHINE** \\ **System** \\ **CurrentControlSet** \\ **Services** \\ **NtFrs** \\ **Parameters** \\ **Backup/Restore** \\ **Process at Startup** \\ **BurFlags**

4.  Riavviare il servizio FrS.

Quando il servizio Replica file viene riavviato, si verificano le azioni seguenti:

-   Il valore della chiave **del Registro di sistema BurFlags** viene reimpostato su zero.
-   I file nelle cartelle FRS reinizializzata vengono spostati in una cartella preesiste.
-   L'evento 13565 viene registrato nel registro eventi frs per segnalare che è stato avviato un ripristino non autorevole.
    > [!Note]  
    > I codici evento FRS sono documentati in "FrS event log error codes" (Codici di errore del registro eventi FRS) nella guida e supporto Knowledge Base all'indirizzo <https://go.microsoft.com/fwlink/p/?linkid=117779>

     

-   Il database FRS viene ricompilato.
-   Il membro esegue un join iniziale del set di repliche da un  partner upstream o dal computer specificato nella chiave del Registro di sistema padre del set di repliche se è stato specificato un elemento padre per i set di repliche SYSVOL.
-   Il computer reinizializzato esegue una replica completa dei set di repliche interessati all'inizio della pianificazione della replica pertinente.
-   Al termine del processo, viene registrato un evento 13516 per segnalare che il servizio Replica file è operativo. Se l'evento non viene registrato, si è verificato un problema con la configurazione del servizio Replica file.

> [!Note]  
> Il posizionamento dei file nella [cartella preesisttiva](/previous-versions/windows/it-pro/windows-server-2003/cc758169(v=ws.10)) nei membri reinizializzato è una protezione nel servizio Replica file progettata per impedire la perdita accidentale di dati. Tutti i file destinati alla replica che esistono solo nella cartella preesistente locale e sono stati replicati dopo la replica iniziale possono quindi essere copiati nella cartella appropriata. Quando si verifica la replica in uscita, i file nella cartella preesistibile possono essere eliminati per liberare spazio aggiuntivo sull'unità.

 

## <a name="performing-an-authoritative-restore-of-an-frs-replicated-sysvol-folder"></a>Esecuzione di un ripristino autorevole di una FRS-Replicated sysvol

I ripristini autorevoli vengono usati come ultima risorsa in caso di situazioni critiche, ad esempio la divergenza dei dati nel set di contenuto causato da conflitti di directory. Ad esempio, potrebbe essere necessario un ripristino autorevole per ripristinare un set di repliche frs in cui la replica è stata arrestata completamente ed è necessaria una ricompilazione da zero.

Se è necessario eseguire un ripristino autorevole della cartella SYSVOL, tenere presente che si tratta di un processo molto complesso. Le linee guida complete che illustrano in dettaglio le operazioni che devono essere eseguite per un ripristino autorevole del contenuto della cartella SYSVOL sono documentate in "Come ricompilare l'albero SYSVOL e il relativo contenuto in un dominio" in Guida e supporto tecnico Knowledge Base all'indirizzo <https://go.microsoft.com/fwlink/p/?linkid=117780> .

Prima di eseguire un ripristino frs autorevole, è necessario soddisfare i requisiti seguenti:

1.  Il servizio FrS deve essere disabilitato in tutti i partner di replica downstream (diretti e transitivi) per la cartella SYSVOL reinizializzata prima che il ripristino autorevole sia stato configurato per l'esecuzione.
2.  Gli eventi 13553 e 13516 sono stati registrati nel registro eventi frs. Questi eventi indicano che l'appartenenza del set di repliche SYSVOL è stata stabilita nel controller di dominio configurato per il ripristino autorevole.
    > [!Note]  
    > I codici evento FRS sono documentati in "FrS event log error codes" (Codici di errore del registro eventi FRS) nella guida e supporto Knowledge Base all'indirizzo <https://go.microsoft.com/fwlink/p/?linkid=117779>

     

3.  Il controller di dominio configurato per il ripristino autorevole è configurato per essere autorevole per tutti i dati SYSVOL che devono essere replicati nei controller di dominio rimanenti.
4.  Tutti gli altri partner nel set di repliche devono essere reinizializzato con un ripristino non autorevole.

 

 
