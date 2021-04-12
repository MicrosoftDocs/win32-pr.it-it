---
title: Chiavi e valori del registro di sistema per il backup e il ripristino
ms.assetid: 83449f78-cca1-449b-8c5f-3c8a91c8b3e7
description: 'Altre informazioni su: chiavi e valori del registro di sistema per il backup e il ripristino'
keywords:
- backup backup, chiavi del registro di sistema
- Backup delle chiavi del registro di sistema
- Backup CustomPerformanceSettings
- Backup DisableMonitoring
- Backup FilesNotToBackup
- Backup FilesNotToSnapshot
- Backup KeysNotToRestore
- Backup LastInstance
- Backup LastRestoreId
- Backup MaxShadowCopies
- Backup MinDiffAreaFileSize
- Backup OverallPerformanceSetting
- Backup SYSVOL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ef9796ff96efbc20ac90de6d26a0c1bac7b17633
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104127659"
---
# <a name="registry-keys-and-values-for-backup-and-restore"></a>Chiavi e valori del registro di sistema per il backup e il ripristino

Le applicazioni che richiedono o eseguono operazioni di backup e ripristino devono usare le chiavi e i valori del registro di sistema seguenti per comunicare tra loro o con funzionalità quali il [servizio Copia Shadow del volume (VSS)](/windows/desktop/VSS/volume-shadow-copy-service-portal) e Windows backup:

-   [CustomPerformanceSettings](#customperformancesettings)
-   [DisableMonitoring](#disablemonitoring)
-   [FilesNotToBackup](#filesnottobackup)
-   [FilesNotToSnapshot](#filesnottosnapshot)
-   [IdleTimeout](#idletimeout)
-   [KeysNotToRestore](#keysnottorestore)
-   [LastInstance](#lastinstance)
-   [LastRestoreId](#lastrestoreid)
-   [MaxShadowCopies](#maxshadowcopies)
-   [MinDiffAreaFileSize](#mindiffareafilesize)
-   [OverallPerformanceSetting e CustomPerformanceSettings](#overallperformancesetting-and-customperformancesettings)
-   [SYSVOL](#sysvol)

## <a name="customperformancesettings"></a>CustomPerformanceSettings

Vedere [OverallPerformanceSetting e CustomPerformanceSettings](#overallperformancesetting-and-customperformancesettings).

## <a name="disablemonitoring"></a>DisableMonitoring

Nelle piattaforme client Windows a partire da Windows 7, agli utenti viene automaticamente richiesto di configurare la funzionalità di backup di Windows, se non è già stata eseguita. Queste notifiche vengono visualizzate in fase di avvio del computer, a partire da sette giorni dopo l'installazione del sistema operativo. Vengono visualizzate anche quando l'utente si connette a un'unità disco rigido; in questo caso, le notifiche vengono visualizzate immediatamente.

Gli OEM e gli sviluppatori di applicazioni di backup di terze parti possono usare il valore del registro di sistema **DisableMonitoring** per disattivare queste notifiche automatiche.

Questo valore non esiste per impostazione predefinita, pertanto deve essere creato nella seguente chiave del registro di sistema:

**HKEY \_ \_Computer locale** \\ **software** \\ **Microsoft** \\ **Windows** \\ **CurrentVersion** \\ **WindowsBackup**

Il valore del registro di sistema **DisableMonitoring** ha il tipo di dati reg \_ DWORD ed è interpretato nel modo seguente:

-   Se i dati del valore sono impostati su 1 e se gli utenti non hanno già configurato la funzionalità Windows backup, le notifiche automatiche sono disattivate. Se una notifica automatica è già presente nel centro operativo, impostando questo valore del registro di sistema la notifica verrà rimossa alle 10:00 del mattino successivo.
-   Se il valore non esiste, se i dati non sono impostati o se i dati sono impostati su zero, le notifiche automatiche non vengono disattivate.

**Windows Vista e Windows XP:** Il valore del registro di sistema non è supportato.

## <a name="filesnottobackup"></a>FilesNotToBackup

La chiave del registro di sistema **FilesNotToBackup** specifica i nomi dei file e delle directory per cui le applicazioni di backup non devono eseguire il backup o il ripristino. Ognuna delle voci in questa chiave è una stringa REG \_ \_ multisz nel formato seguente:

\[*Unità di* \] \[  \] Percorso \\ *Nome file* \[ /s\]

-   *Unità* consente di specificare l'unità ed è facoltativa. Ad esempio, c:. Per specificare tutte le unità, utilizzare una barra rovesciata ( \) ; non è necessaria alcuna lettera di unità.
-   *Path* specifica il percorso ed è facoltativo. Non può contenere caratteri jolly.
-   *Filename* specifica il file o la directory ed è obbligatorio. Può contenere caratteri jolly.
-   /s indica che devono essere incluse tutte le sottodirectory del percorso specificato.
-   Le variabili di ambiente come% SystemRoot% possono essere sostituite per tutta o parte dell'intera stringa.

Nella tabella seguente vengono illustrate alcune voci tipiche.

| Nome voce                             | Valore predefinito                                                                             |
|----------------------------------------|-------------------------------------------------------------------------------------------|
| Internet Explorer                      | File temporanei                                                                           |
| File di paging della memoria                       | \\Pagefile.sys                                                                            |
| Distributed Transaction Coordinator MS | C: \\ Windows \\ system32 MSDTC MSDTC \\ \\ . LOG C: \\ Windows \\ system32 \\ MSDtc \\ trace \\ dtctrace. log |
| Cache File offline                    | % SystemRoot% \\ csc \\ \* /s                                                                  |
| Risparmio energia                       | \\hiberfil.sys                                                                            |
| Single Instance Storage (SIS)                | \\Archivio comune SIS \\ \* . \* /s                                                              |
| File temporanei                        | % TEMP% \\ \* /s                                                                             |



 

> [!Note]  
> Per le applicazioni che eseguono backup a livello di volume in genere, copiando l'intero volume a livello di blocco, non è possibile rispettare la chiave del registro di sistema **FilesNotToBackup** in fase di backup. Ma restano in attesa fino al momento del ripristino per eliminare i file di cui non è stato eseguito il backup. Nella maggior parte dei casi, si tratta di una strategia ragionevole. Tuttavia, nel caso di file di archiviazione a istanza singola, i file di archivio comuni SIS non devono essere eliminati in fase di ripristino.

 

Per i backup del volume a livello di blocco, Windows Server Backup e l'utilità Windows Wbadmin rispettano la chiave del registro di sistema **FilesNotToBackup** eliminando i file appropriati in fase di ripristino. Il ripristino del sistema e il backup dello stato del sistema non rispettano la chiave del registro di sistema **FilesNotToBackup** .

**Windows XP:** Ripristino configurazione di sistema rispetta la chiave del registro di sistema **FilesNotToBackup** .

## <a name="filesnottosnapshot"></a>FilesNotToSnapshot

VSS supporta la chiave del registro di sistema **FilesNotToSnapshot** . Le applicazioni e i servizi possono usare questa chiave per specificare i file da eliminare dalle copie shadow appena create. Per altre informazioni, vedere [esclusione di file dalle copie shadow](/windows/desktop/VSS/excluding-files-from-shadow-copies).

**Windows Server 2003 e Windows XP:** Questa chiave del registro di sistema non è supportata.

Per i backup del volume a livello di blocco, Windows Server Backup rispetta la chiave del registro di sistema **FilesNotToSnapshot** eliminando i file appropriati in fase di ripristino.

## <a name="idletimeout"></a>IdleTimeout

Il valore del registro di sistema **IdleTimeout** specifica la quantità di tempo, in secondi, in cui il servizio VSS resterà in attesa quando è inattivo. Se questo valore di timeout viene raggiunto e non è necessario eseguire alcuna attività, il servizio VSS verrà arrestato.

Questo valore del registro di sistema si trova nella seguente chiave del registro di sistema:

**HKEY \_ \_** \\  \\  \\  \\  \\ **Impostazioni** VSS dei servizi CurrentControlSet di sistema del computer locale

Se il valore del registro di sistema non esiste:

-   Per impostazione predefinita, il valore di timeout effettivo usato è 180 secondi (3 minuti).
-   È possibile creare un valore con il nome **IdleTimeout** e il tipo DWORD e impostarlo sul valore desiderato.

Se il valore del registro di sistema è impostato su 0 secondi:

-   Il valore di timeout effettivo utilizzato è 180 secondi (3 minuti).

Se si imposta questo valore del registro di sistema:

-   VSS utilizza il valore di timeout impostato.
-   È possibile specificare qualsiasi valore compreso tra 1 e FFFFFFFF secondi. Tuttavia, si consiglia di scegliere un valore compreso tra 1 e 180 secondi.

**Windows Server 2003 e Windows XP:** Questa chiave del registro di sistema non è supportata.

## <a name="keysnottorestore"></a>KeysNotToRestore

La chiave del registro di sistema **KeysNotToRestore** specifica i nomi delle sottochiavi del registro di sistema e i valori che non devono essere ripristinati dalle applicazioni di backup. Per ulteriori informazioni, vedere [KeysNotToRestore](/previous-versions/windows/it-pro/windows-server-2003/cc737538(v=ws.10)). Non è necessario rispettare la chiave del registro di sistema **KeysNotToRestore** .

**Windows Server 2003 e Windows XP:** È necessario rispettare la chiave del registro di sistema **KeysNotToRestore** .

Per i backup del volume a livello di blocco, Windows Server Backup rispetta la chiave del registro di sistema **KeysNotToRestore** eliminando i file appropriati in fase di ripristino.

Il backup dello stato del sistema rispetta la chiave del registro di sistema **KeysNotToRestore** .

## <a name="lastinstance"></a>LastInstance

Il valore del registro di sistema **LastInstance** indica che è stata eseguita un'operazione di ripristino bare metal e che i volumi sono stati sovrascritti ma non formattati. Per ulteriori informazioni, vedere [utilizzo del ripristino automatico del sistema VSS per il ripristino di emergenza](/windows/desktop/VSS/using-vss-automated-system-recovery-for-disaster-recovery).

**Windows Server 2003 e Windows XP:** Il valore del registro di sistema non è supportato.

## <a name="lastrestoreid"></a>LastRestoreId

Quando un'applicazione di backup esegue un ripristino dello stato del sistema, deve indicare che l'operazione è stata eseguita impostando il valore del registro di sistema **LastRestoreId** . "Ripristino dello stato del sistema" in questo caso si riferisce a qualsiasi ripristino che ripristini in modo selettivo i driver e i binari del sistema operativo.

Se l'intero volume di avvio e di sistema viene ripristinato a livello di volume, questo valore non deve essere impostato.

Se il valore del registro di sistema **LastRestoreId** non esiste, l'applicazione di backup deve crearla con la chiave del registro di sistema seguente:

**HKEY \_ \_Computer locale** \\ **System** \\ **CurrentControlSet** \\ **Control** \\ **backuprestore** \\ **SystemStateRestore**

Creare un valore con il nome **LastRestoreId** e digitare reg \_ SZ. Il valore deve essere un valore opaco univoco, ad esempio un GUID.

Ogni volta che viene eseguito un nuovo ripristino dello stato del sistema, l'applicazione di backup deve modificare i dati del valore **LastRestoreId** .

Altre applicazioni che devono monitorare i ripristini dello stato del sistema devono archiviare i dati di questo valore del registro di sistema. Questi dati possono essere confrontati con i dati correnti del valore del registro di sistema **LastRestoreId** per determinare se è stato eseguito un nuovo ripristino dello stato del sistema.

**Windows Vista, Windows Server 2003 e Windows XP:** Questo valore del registro di sistema non è supportato fino a Windows Vista con Service Pack 1 (SP1) e Windows Server 2008.

## <a name="maxshadowcopies"></a>MaxShadowCopies

Il valore del registro di sistema **MaxShadowCopies** specifica il numero massimo di [*copie shadow accessibili dal client*](/windows/desktop/VSS/vssgloss-c) che possono essere archiviate in ogni volume del computer. Una copia shadow accessibile dal client è una copia shadow creata usando il valore **accessibile del \_ \_ client \_ VSS CTX** dell'enumerazione del [**\_ \_ \_ contesto dello snapshot VSS**](/windows/desktop/api/vss/ne-vss-vss_snapshot_context) . Le copie shadow accessibili dal client vengono usate da Copie shadow di cartelle condivise. Per ulteriori informazioni sulle copie shadow, vedere la documentazione di [VSS](/windows/desktop/VSS/volume-shadow-copy-service-portal) .

Se il valore del registro di sistema **MaxShadowCopies** non esiste, l'applicazione di backup può crearla con la chiave del registro di sistema seguente:

**HKEY \_ \_** \\  \\  \\  \\  \\ **Impostazioni** VSS dei servizi CurrentControlSet di sistema del computer locale

Creare un valore con il nome **MaxShadowCopies** e digitare DWORD. I dati predefiniti per questo valore sono 64. Il valore minimo è 1. Il valore massimo è 512.

> [!Note]  
> Per altri tipi di copie shadow, non esiste alcun valore del registro di sistema corrispondente a **MaxShadowCopies**. Il numero massimo di copie shadow è 512 per volume.

 

**Nota**  L'impostazione **MaxShadowCopies** è supportata in Windows Server 2003 o versioni successive.

**Windows Server 2003:** Nei server del cluster è possibile che i dati del valore del registro di sistema **MaxShadowCopies** debbano essere impostati su un numero inferiore. Per ulteriori informazioni, vedere "quando si utilizza il Servizio Copia Shadow del volume nei computer basati su Windows Server 2003 che eseguono molte operazioni di I/O, i volumi del disco impiegano più tempo per l'esecuzione online" nella Knowledge base e supporto tecnico all'indirizzo [https://support.microsoft.com/kb/945058](https://support.microsoft.com/kb/945058) .

**Windows XP:** Il valore del registro di sistema non è supportato.

## <a name="mindiffareafilesize"></a>MinDiffAreaFileSize

[VSS](/windows/desktop/VSS/volume-shadow-copy-service-portal) alloca un'area di archiviazione copia shadow (o "area diff") per archiviare i dati per le copie shadow. La dimensione minima dell'area di archiviazione copia shadow è un'impostazione per computer che può essere specificata usando il valore del registro di sistema **MinDiffAreaFileSize** .

Se il valore del registro di sistema **MinDiffAreaFileSize** non è impostato, le dimensioni minime dell'area di archiviazione della copia shadow sono pari a 32 MB per i volumi inferiori a 500 mb e 320 MB per volumi di dimensioni superiori a 500 MB.

**Windows server 2008, Windows server 2003 con SP1 e Windows Vista:** Se il valore del registro di sistema **MinDiffAreaFileSize** non è impostato, le dimensioni minime dell'area di archiviazione della copia shadow sono pari a 300 MB. Se viene impostato il valore del registro di sistema **MinDiffAreaFileSize** , i dati devono essere compresi tra 300 mb e 3000 MB (3 GB) e devono essere un multiplo di 300 MB.

**Windows Server 2003:** Se il valore del registro di sistema **MinDiffAreaFileSize** non è impostato, le dimensioni minime dell'area di archiviazione della copia shadow sono 100 MB.

**Windows XP:** Il valore del registro di sistema non è supportato.

Se il valore del registro di sistema **MinDiffAreaFileSize** non esiste, l'applicazione di backup può crearla con la chiave del registro di sistema seguente:

**HKEY \_ \_Computer locale** \\ **System** \\ **CurrentControlSet** \\ **Services** \\ **VolSnap**

Creare un valore con il nome **MinDiffAreaFileSize** e digitare reg \_ DWORD. I dati per questa chiave sono specificati in megabyte. 320 è uguale a 320 MB e 3200 è uguale a 3,2 GB. È necessario specificare un numero che corrisponde a un multiplo di 32. Se si specifica un valore che non è un multiplo di 32, verrà usato il multiplo successivo di 32.

Le copie shadow potrebbero non funzionare correttamente se il valore del registro di sistema **MinDiffAreaFileSize** specifica una dimensione minima maggiore delle dimensioni massime dell'area di archiviazione della copia shadow. Per specificare le dimensioni massime dell'area di archiviazione copia shadow, usare il comando [vssadmin](/previous-versions/windows/it-pro/windows-server-2012-R2-and-2012/cc754968(v=ws.11)) add shadowstorage o vssadmin resize shadowstorage. Per visualizzare le dimensioni massime correnti, usare il comando [vssadmin list shadowstorage](/previous-versions/windows/it-pro/windows-server-2012-R2-and-2012/cc754968(v=ws.11)) . Se non è stata impostata una dimensione massima, non esiste alcun limite alla quantità di spazio che è possibile usare.

## <a name="overallperformancesetting-and-customperformancesettings"></a>OverallPerformanceSetting e CustomPerformanceSettings

I valori del registro di sistema **OverallPerformanceSetting** e **CustomPerformanceSettings** vengono usati per specificare le impostazioni delle prestazioni per Windows Server backup. Questi valori del registro di sistema sono supportati solo nei sistemi operativi Windows Server.

**Windows Server 2003:** Questi valori del registro di sistema non sono supportati.

Se questi valori del registro di sistema non esistono, l'applicazione di backup può crearli con la seguente chiave del registro di sistema:

**HKEY \_ \_Computer locale** \\ **software** \\ **Microsoft** \\ **Windows** \\ **CurrentVersion** \\ **Windows block level backup**

Per specificare le impostazioni delle prestazioni per tutti i volumi, creare un valore con il nome **OverallPerformanceSetting** e digitare reg \_ DWORD. I dati del valore devono essere impostati su uno dei valori seguenti.

| Valore | Significato                                                                                                                                                                                                                                   |
|-------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 1     | Normali prestazioni di backup (tramite backup completi). Questa impostazione corrisponde alla normale impostazione delle prestazioni di backup descritta in [ottimizzazione delle prestazioni di backup e server](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/dd759145(v=ws.11)).            |
| 2     | Prestazioni di backup più veloci (usando i backup incrementali). Questa impostazione corrisponde all'impostazione delle prestazioni di backup più veloce descritta in [ottimizzazione delle prestazioni di backup e server](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/dd759145(v=ws.11)).     |
| 3     | Prestazioni di backup personalizzate (specificando un'impostazione delle prestazioni per ogni volume). Questa impostazione corrisponde all'impostazione personalizzata descritta in [ottimizzazione delle prestazioni di backup e server](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/dd759145(v=ws.11)). |



 

Se si imposta **OverallPerformanceSetting** su 3, è necessario specificare anche le impostazioni relative alle prestazioni per ogni volume singolarmente. A tale scopo, creare un valore con il nome **CustomPerformanceSettings** e digitare reg \_ \_ multisz. I dati di questo valore devono essere impostati come segue:

-   Ogni stringa nella sequenza REG \_ \_ multisz di stringhe contiene l'impostazione per un volume.
-   Ogni stringa è costituita da un GUID del volume, seguito da una virgola, seguita da un valore DWORD.
-   Ognuno dei valori DWORD è 1 (backup completo) o 2 (backup incrementale).

Si supponga, ad esempio, che il computer disponga di due volumi come segue:

-   I due volumi sono C: \\ e D: \\ .
-   Il GUID per il volume C: \\ è 07c473ca4-2df8-11de-9d80-806e6f6e6963 e il GUID per il volume D: \\ è 0ac22ea6c-712f-11de-ADB0-00215a67606e.
-   Si desidera specificare perfornance di backup normali per il volume C: \\ e prestazioni di backup più veloci per il volume D: \\ .

A tale scopo, impostare **OverallPerformanceSetting** su 3 e **CustomPerformanceSettings** su "07c473ca4-2df8-11de-9d80-806e6f6e6963, 1 \\ 00ac22ea6c-712f-11de-ADB0-00215a67606e, 2".

Se si imposta **OverallPerformanceSetting** su 1 o 2, i dati nel valore **CustomPerformanceSettings** vengono ignorati.

## <a name="sysvol"></a>SYSVOL

Il valore del registro di sistema **SYSVOL** è un modo per notificare al servizio file System distribuito Replication (DFSR) che è stata avviata un'operazione di ripristino dello stato del sistema. Qualsiasi applicazione di backup che esegue il ripristino dello stato del sistema di SYSVOL deve usare questo valore per indicare se l'operazione di ripristino è autorevole o non autorevole. Questo valore viene letto dal servizio DFSR. Se questo valore non è impostato, per impostazione predefinita il ripristino di SYSVOL viene eseguito in un caso non autorevole.

Se il valore del registro di sistema **SYSVOL** non esiste, l'applicazione di backup deve crearla con la seguente chiave del registro di sistema:

**HKEY \_ \_** \\  \\  \\  \\  \\ **Ripristino** DFSR dei servizi CurrentControlSet del computer locale

Creare un valore con il nome **SYSVOL** e digitare reg \_ SZ. I dati del valore devono essere impostati su "autorevole" o "non autorevole" in base alla richiesta dell'amministratore di sistema.

**Windows Vista, Windows Server 2003 e Windows XP:** Il valore del registro di sistema non è supportato.

 

 
