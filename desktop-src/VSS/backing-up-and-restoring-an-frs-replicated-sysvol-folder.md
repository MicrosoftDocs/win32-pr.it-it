---
description: In questo argomento viene illustrato come determinare se una cartella SYSVOL viene replicata da DFSR o FSR e viene illustrato come eseguire il backup e il ripristino di una cartella SYSVOL replicata con FRS.
ms.assetid: 32d8a5bd-eeb4-4db6-8129-b5cd3508a7e5
title: Backup e ripristino di una cartella FRS-Replicated SYSVOL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ea83ccbc156182a4a3b84c758cb22153f4f7110f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104347226"
---
# <a name="backing-up-and-restoring-an-frs-replicated-sysvol-folder"></a>Backup e ripristino di una cartella FRS-Replicated SYSVOL

La cartella volume di sistema (SYSVOL) fornisce una posizione standard per archiviare gli elementi importanti di [criteri di gruppo](/previous-versions/windows/it-pro/windows-server-2003/cc779838(v=ws.10)) oggetti e script. Una copia della cartella SYSVOL esiste in ogni controller di dominio in un dominio. La cartella SYSVOL viene replicata da [file System distribuito replica (DFSR)](/windows-server/storage/dfs-replication/migrate-sysvol-to-dfsr) o dal [servizio Replica file (FRS)](/previous-versions/windows/it-pro/windows-server-2003/cc781582(v=ws.10)). In questo argomento viene illustrato come determinare se una cartella SYSVOL viene replicata da DFSR o FSR e viene illustrato come eseguire il backup e il ripristino di una cartella SYSVOL replicata con FRS.

Il servizio Replica file può copiare il contenuto di SYSVOL in altri controller di dominio all'interno del dominio. FRS monitora la cartella SYSVOL e, se si verifica una modifica in qualsiasi file archiviato nella cartella SYSVOL, FRS replica automaticamente il file modificato nelle cartelle SYSVOL degli altri controller di dominio del dominio.

> [!Note]  
> Solo il modello di Criteri di gruppo viene replicato replicando il contenuto della cartella SYSVOL. Il contenitore Criteri di gruppo viene replicato tramite Active Directory replica. Per il corretto funzionamento di Criteri di gruppo, è necessario che il modello di Criteri di gruppo e il contenitore Criteri di gruppo siano disponibili in un controller di dominio.

 

In questo argomento vengono illustrati gli argomenti seguenti:

-   [Determinare se la cartella SYSVOL di un controller di dominio viene replicata da DFSR o FRS](#determining-whether-a-domain-controllers-sysvol-folder-is-replicated-by-dfsr-or-frs)
-   [Esecuzione del backup di una cartella DFSR-Replicated SYSVOL](#backing-up-a-dfsr-replicated-sysvol-folder)
-   [Backup di una cartella FRS-Replicated SYSVOL in un dominio Windows Server 2008 o Windows Server 2003](#backing-up-an-frs-replicated-sysvol-folder-on-a-windows-server-2008-or-windows-server-2003-domain)
-   [Documento di metadati del writer FRS di esempio](#sample-frs-writer-metadata-document)
-   [Impostazione delle chiavi del registro di sistema per il ripristino di una cartella FRS-Replicated SYSVOL](#setting-registry-keys-for-a-restore-of-an-frs-replicated-sysvol-folder)
-   [Esecuzione di un ripristino non autorevole di una cartella FRS-Replicated SYSVOL](#performing-a-nonauthoritative-restore-of-an-frs-replicated-sysvol-folder)
-   [Esecuzione di un ripristino autorevole di una cartella FRS-Replicated SYSVOL](#performing-an-authoritative-restore-of-an-frs-replicated-sysvol-folder)

## <a name="determining-whether-a-domain-controllers-sysvol-folder-is-replicated-by-dfsr-or-frs"></a>Determinare se la cartella SYSVOL di un controller di dominio viene replicata da DFSR o FRS

Nella tabella seguente viene riepilogato come determinare se la cartella SYSVOL di un controller di dominio viene replicata da [DFSR](/windows-server/storage/dfs-replication/migrate-sysvol-to-dfsr) o FRS.

| Se il controller di dominio è in esecuzione                                                                                                                  | SYSVOL replicato da |
|------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------|
| Windows Server 2008 + livello di funzionalità del dominio di Windows Server 2008 + [migrazione SYSVOL](https://blogs.technet.com/filecab/archive/2008/02/08/sysvol-migration-series-part-1-introduction-to-the-sysvol-migration-process.aspx) completata | DFSR                    |
| Livello di funzionalità del dominio di Windows Server 2008 + sotto Windows Server 2008                                                                              | FRS                     |
| Windows Server 2003                                                                                                                                  | FRS                     |



 

Se il livello di [funzionalità](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc754918(v=ws.10)) del dominio è Windows Server 2008 e il dominio è stato sottoposto a [migrazione SYSVOL](https://blogs.technet.com/filecab/archive/2008/02/08/sysvol-migration-series-part-1-introduction-to-the-sysvol-migration-process.aspx), [DFSR](/windows-server/storage/dfs-replication/migrate-sysvol-to-dfsr) verrà usato per replicare la cartella SYSVOL. Se il primo controller di dominio nel dominio è stato promosso direttamente al livello di [funzionalità](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc754918(v=ws.10))di Windows Server 2008, DFSR viene usato automaticamente per la replica di SYSVOL. In questi casi, non è necessario eseguire la migrazione della replica SYSVOL da FRS a DFSR. Se il dominio è stato aggiornato al livello di [funzionalità](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc754918(v=ws.10))di Windows Server 2008, FRS viene usato per la replica SYSVOL fino al completamento del processo di [migrazione](https://blogs.technet.com/filecab/archive/2008/02/08/sysvol-migration-series-part-1-introduction-to-the-sysvol-migration-process.aspx) da FRS a DFSR.

Per determinare se DFSR o FRS è in uso in un controller di dominio che esegue Windows Server 2008, verificare il valore di **HKEY \_ Local \_ computer** \\ **System** \\ **CurrentControlSet** \\ **Services** \\ **DFSR** \\ **Parameters** \\ **sysvols** \\ **Migrating sysvols** \\ **LocalState** Registry sottochiave. Se questa sottochiave del registro di sistema esiste e il relativo valore è impostato su 3 (eliminato), viene usato [DFSR](/windows-server/storage/dfs-replication/migrate-sysvol-to-dfsr) . Se la sottochiave non esiste o se ha un valore diverso, viene utilizzato FRS.

## <a name="backing-up-a-dfsr-replicated-sysvol-folder"></a>Esecuzione del backup di una cartella DFSR-Replicated SYSVOL

Se la cartella SYSVOL viene replicata da [DFSR](/windows-server/storage/dfs-replication/migrate-sysvol-to-dfsr), è possibile usare la VSS Writer DFSR per eseguire il backup. Per ulteriori informazioni sul VSS writer DFSR, vedere [DFSR Replicated Folders](/previous-versions/windows/desktop/dfsr/dfsr-replicated-folders).

## <a name="backing-up-an-frs-replicated-sysvol-folder-on-a-windows-server-2008-or-windows-server-2003-domain"></a>Backup di una cartella FRS-Replicated SYSVOL in un dominio Windows Server 2008 o Windows Server 2003

In un controller di dominio che esegue Windows Server 2008 o Windows Server 2003, è presente l'infrastruttura VSS e pertanto è possibile utilizzare il VSS writer FRS per eseguire il backup della cartella SYSVOL e dei componenti FRS.

Il documento di metadati del writer del VSS writer FRS fornisce informazioni sul percorso della cartella SYSVOL e sugli elenchi di esclusione per il writer. In base a queste informazioni, un'applicazione di backup VSS (richiedente) può eseguire il backup della cartella SYSVOL usando le normali tecniche di backup basate su VSS.

Il documento di metadati del writer contiene informazioni sul writer, i dati di proprietà del writer e il modo in cui ripristinare i dati. Si tratta di un documento di sola lettura che può essere recuperato dall'applicazione di backup prima di eseguire un backup. Lo strumento [DiskShadow](/previous-versions/windows/it-pro/windows-server-2012-R2-and-2012/cc772172(v=ws.11)) può essere usato per visualizzare il documento di metadati del writer del VSS Writer FRS. Il comando [DiskShadow list writers](/previous-versions/windows/it-pro/windows-server-2012-R2-and-2012/cc772172(v=ws.11)) fornisce informazioni sui Writer presenti nel sistema. Questo elenco contiene informazioni sul writer FRS nei controller di dominio che utilizzano FRS per la replica SYSVOL o sui file server che utilizzano FRS per la replica delle [destinazioni dei collegamenti DFS](/previous-versions/windows/it-pro/windows-server-2003/cc782417(v=ws.10)).

La sezione del documento di metadati del writer FRS di esempio seguente mostra un documento di metadati del writer FRS di esempio per un controller di dominio con la cartella SYSVOL in D: \\ Windows \\ SYSVOL. Il percorso illustrato nella sezione "file esclusi" sarà identico a quello ottenuto quando si esegue una query sulla chiave del registro di sistema **SYSVOL** del servizio Netlogon:

**HKEY \_ \_Computer locale** \\ **sistema** \\ **CurrentControlSet** \\ **Servizi** \\ **Netlogon** \\ **parametri** \\ **SYSVOL**

L'unica eccezione a questa regola si verifica quando il controller di dominio si trova nello stato reindirizzato della [migrazione SYSVOL](https://blogs.technet.com/filecab/archive/2008/02/08/sysvol-migration-series-part-1-introduction-to-the-sysvol-migration-process.aspx). In questo stato, i writer corrispondenti a FRS e al servizio [DFSR](/windows-server/storage/dfs-replication/migrate-sysvol-to-dfsr) segnalano le rispettive copie della cartella SYSVOL. Tuttavia, la copia del servizio [DFSR](/windows-server/storage/dfs-replication/migrate-sysvol-to-dfsr) della cartella SYSVOL (in genere una cartella denominata SYSVOL \_ DFSR) corrisponde a quella condivisa dal controller di dominio. questo percorso è quello a cui fa riferimento la chiave del registro di sistema **SYSVOL** .

Il VSS writer FRS richiede un metodo di ripristino personalizzato. Ciò significa che è necessario eseguire alcuni passaggi personalizzati durante il ripristino dei file replicati da FRS. Per ulteriori informazioni, vedere esecuzione di un ripristino non autorevole di una FRS-Replicated cartella SYSVOL.

> [!Note]  
> I backup dello stato del sistema per i controller di dominio Windows non includono il database FRS che mantiene le informazioni sullo stato per il servizio FRS relativo ai file all'interno della cartella SYSVOL e di altri set di contenuto. Il database FRS, i log di debug, i file dell'area di gestione temporanea e i file nella [cartella dei dati preesistenti](/previous-versions/windows/it-pro/windows-server-2003/cc758169(v=ws.10)) sono esclusi da un backup dello stato del sistema. La specifica del writer FRS di esempio seguente contiene l'elenco di esclusione nella sezione "file esclusi".

 

## <a name="sample-frs-writer-metadata-document"></a>Documento di metadati del writer FRS di esempio

Di seguito è riportato un documento di metadati del writer FRS di esempio per un controller di dominio il cui percorso della cartella SYSVOL è D: \\ Windows \\ SYSVOL.

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

## <a name="setting-registry-keys-for-a-restore-of-an-frs-replicated-sysvol-folder"></a>Impostazione delle chiavi del registro di sistema per il ripristino di una cartella FRS-Replicated SYSVOL

La chiave del registro di sistema **BurFlags** viene utilizzata per eseguire ripristini autorevoli o non autorevoli nei membri FRS dei set di repliche DFS o SYSVOL. La chiave del registro di sistema **BurFlags** globale (a livello di computer) contiene \_ i valori DWORD reg e si trova nel percorso seguente nel registro di sistema:

**HKEY \_ \_Computer locale** \\ **sistema** \\ **CurrentControlSet** \\ **Servizi** \\ **NTFRS** \\ **parametri** \\ processo di **backup/ripristino** \\ **all'avvio**

I valori più comuni per la chiave del registro di sistema **BurFlags** sono:

-   D2, noto anche come ripristino in modalità non autorevole.
-   D4, noto anche come ripristino in modalità autorevole.

Sono disponibili chiavi del registro di sistema **BurFlags** specifiche del set di repliche e globali. L'impostazione della chiave del registro di sistema **BurFlags** globale reinizializza tutti i set di repliche che il membro contiene. Questa chiave globale deve essere impostata quando il server contiene un solo set di repliche o quando la replica che contiene è relativamente limitata a un numero e a dimensioni ridotte. Se, ad esempio, il server è un controller di dominio che non ospita alcun set di contenuto replicato con FRS diverso dalla cartella SYSVOL, è possibile impostare la chiave del registro di sistema **BurFlags** globale.

La chiave del registro di sistema **BurFlags** globale si trova nel seguente percorso del registro di sistema:

**HKEY \_ \_Computer locale** \\ **sistema** \\ **CurrentControlSet** \\ **Servizi** \\ **NTFRS** \\ **parametri** \\ processo di **backup/ripristino** \\ **all'avvio**

A differenza della chiave **BurFlags** globale, la chiave **BurFlags** specifica del set di repliche consente la reinizializzazione dei set di repliche singoli e discreti, consentendo la reimpostazione di set di replica integri.

Le chiavi del registro di sistema **BurFlags** specifiche del set di repliche possono essere individuate determinando il GUID per quel particolare set di repliche.

Nella procedura seguente viene descritto come determinare quale GUID corrisponde a un determinato set di repliche e viene descritto come configurare un ripristino.

**Per determinare quale GUID corrisponde a un determinato set di repliche e configurare un ripristino**

1.  Arrestare il servizio FRS.
2.  Per determinare il GUID che rappresenta un determinato set di repliche:
    1.  Individuare la chiave seguente nel registro di sistema.

        **HKEY \_ \_** Set di \\  \\  \\  \\  \\  \\ **repliche** di parametri NTFRS dei servizi CurrentControlSet del computer locale

    2.  Sotto la sottochiave **set di repliche** sono presenti una o più sottochiavi identificate da un GUID.
    3.  Il valore **radice del set di repliche** per ogni GUID è un file System percorso che indica il set di repliche rappresentato da questo GUID.
    4.  Scorrere l'elenco dei GUID fino a quando non si trova il set di repliche desiderato. Si noti il GUID corrispondente.

3.  Individuare la sottochiave seguente nel registro di sistema:

    **HKEY \_ \_Computer locale** \\ **sistema** \\ **CurrentControlSet** \\ **Servizi** \\ **NTFRS** \\ **parametri** \\ **set di repliche cumulativi**

4.  Sotto questa sottochiave individuare lo stesso GUID indicato nel passaggio 2. Sotto la sottochiave GUID creare una voce per la chiave **BurFlags** .
5.  Riavviare il servizio FRS.

## <a name="performing-a-nonauthoritative-restore-of-an-frs-replicated-sysvol-folder"></a>Esecuzione di un ripristino non autorevole di una cartella FRS-Replicated SYSVOL

Il ripristino non autorevole è il modo più comune per reinizializzare la replica SYSVOL nei singoli controller di dominio. I controller di dominio che vengono ripristinati in modo non autorevole devono disporre di connessioni in ingresso da altri controller di dominio di lavoro, che partecipano alla replica Active Directory e FRS. In un ambiente di distribuzione di grandi dimensioni costituito da molti controller di dominio, è possibile ripristinare i controller di dominio rimanenti utilizzando un ripristino in modalità non autorevole nelle condizioni seguenti:

-   Deve essere presente almeno un membro di replica valido noto (un controller di dominio con una cartella SYSVOL integro).
-   Gli altri controller di dominio devono essere reinizializzati nell'ordine del partner di replica diretta.

Nella procedura riportata di seguito viene descritto come eseguire un ripristino non autorevole.

**Per eseguire un ripristino non autorevole**

1.  Arrestare il servizio FRS.
2.  Ripristinare i dati di cui è stato eseguito il backup nella cartella SYSVOL.
3.  Configurare la chiave del registro di sistema **BurFlags** impostando il valore della seguente chiave del registro di sistema sul valore DWORD D2.

    **HKEY \_ \_Computer locale** \\ **sistema** \\ **CurrentControlSet** \\ **Servizi** \\ **NTFRS** \\ **parametri** \\ processo di **backup/ripristino** \\ **all'avvio** \\ **BurFlags**

4.  Riavviare il servizio FRS.

Quando il servizio FRS viene riavviato, si verificano le azioni seguenti:

-   Il valore della chiave del registro di sistema **BurFlags** viene reimpostato su zero.
-   I file nelle cartelle FRS reinizializzate vengono spostati in una cartella già esistente.
-   L'evento 13565 viene registrato nel registro eventi FRS per segnalare che è stato avviato un ripristino non autorevole.
    > [!Note]  
    > I codici evento FRS sono documentati in "codici di errore del registro eventi FRS" nella Knowledge base della guida e del supporto tecnico all'indirizzo <https://go.microsoft.com/fwlink/p/?linkid=117779>

     

-   Il database FRS viene ricompilato.
-   Il membro esegue un join iniziale del set di repliche da un partner upstream o dal computer specificato nella chiave del registro di sistema **padre del set di repliche** se è stato specificato un elemento padre per i set di repliche SYSVOL.
-   Il computer reinizializzato esegue una replica completa dei set di repliche interessati quando inizia la pianificazione di replica pertinente.
-   Al termine del processo, viene registrato un evento 13516 per segnalare che il servizio Replica file è operativo. Se l'evento non viene registrato, si verifica un problema con la configurazione di FRS.

> [!Note]  
> Il posizionamento dei file nella cartella [preesistente](/previous-versions/windows/it-pro/windows-server-2003/cc758169(v=ws.10)) nei membri reinizializzati è una protezione in FRS progettata per evitare la perdita accidentale di dati. Tutti i file destinati alla replica che esistono solo nella cartella locale preesistente e che sono stati replicati dopo la replica iniziale possono essere copiati nella cartella appropriata. Quando si è verificata la replica in uscita, è possibile eliminare i file nella cartella preesistente per liberare spazio su disco aggiuntivo.

 

## <a name="performing-an-authoritative-restore-of-an-frs-replicated-sysvol-folder"></a>Esecuzione di un ripristino autorevole di una cartella FRS-Replicated SYSVOL

I ripristini autorevoli vengono usati come ultima risorsa in caso di situazioni critiche, ad esempio la divergenza dei dati sul set di contenuti causato da conflitti di directory. Ad esempio, potrebbe essere necessario un ripristino autorevole per ripristinare un set di repliche FRS in cui la replica è stata arrestata completamente ed è richiesta una ricompilazione da zero.

Se è necessario eseguire un ripristino autorevole della cartella SYSVOL, tenere presente che si tratta di un processo molto complesso. Le linee guida complete che illustrano in dettaglio le operazioni che è necessario eseguire per un ripristino autorevole del contenuto della cartella SYSVOL sono documentate in "come ricompilare l'albero SYSVOL e il relativo contenuto in un dominio" nella Knowledge base della guida e supporto tecnico all'indirizzo <https://go.microsoft.com/fwlink/p/?linkid=117780> .

Prima di eseguire un ripristino di FRS autorevole, è necessario soddisfare i requisiti seguenti:

1.  Il servizio FRS deve essere disabilitato in tutti i partner di replica downstream (diretti e transitivi) per la cartella SYSVOL reinizializzata prima che venga configurato il ripristino autorevole.
2.  Gli eventi 13553 e 13516 sono stati registrati nel registro eventi di FRS. Questi eventi indicano che l'appartenenza al set di repliche SYSVOL è stata stabilita sul controller di dominio configurato per il ripristino autorevole.
    > [!Note]  
    > I codici evento FRS sono documentati in "codici di errore del registro eventi FRS" nella Knowledge base della guida e del supporto tecnico all'indirizzo <https://go.microsoft.com/fwlink/p/?linkid=117779>

     

3.  Il controller di dominio configurato per il ripristino autorevole è configurato per essere autorevole per tutti i dati SYSVOL che devono essere replicati nei controller di dominio rimanenti.
4.  Tutti gli altri partner del set di repliche devono essere reinizializzati con un ripristino non autorevole.

 

 
