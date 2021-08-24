---
title: Chiavi e valori del Registro di sistema per il backup e il ripristino
ms.assetid: 83449f78-cca1-449b-8c5f-3c8a91c8b3e7
description: 'Altre informazioni su: Chiavi e valori del Registro di sistema per il backup e il ripristino'
keywords:
- backup, chiavi del Registro di sistema
- Backup delle chiavi del Registro di sistema
- CustomPerformanceSettings Backup
- DisableMonitoring Backup
- FilesNotToBackup Backup
- FilesNotToSnapshot Backup
- KeysNotToRestore Backup
- LastInstance Backup
- LastRestoreId Backup
- MaxShadowCopies Backup
- MinDiffAreaFileSize Backup
- OverallPerformanceSetting Backup
- SYSVOL Backup
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6d825c6588242dccd5df16778de9c590e51b7cdbf6696be4f1a5e40ff2d967c4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119702191"
---
# <a name="registry-keys-and-values-for-backup-and-restore"></a>Chiavi e valori del Registro di sistema per il backup e il ripristino

Le applicazioni che richiedono o eseguono operazioni di backup e ripristino devono usare le chiavi e i valori del Registro di sistema seguenti per comunicare tra loro o con funzionalità quali [Servizio Copia Shadow del volume (VSS)](/windows/desktop/VSS/volume-shadow-copy-service-portal) e Windows Backup:

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

Vedere [OverallPerformanceSetting e CustomPerformanceSettings.](#overallperformancesetting-and-customperformancesettings)

## <a name="disablemonitoring"></a>DisableMonitoring

Nelle Windows client a partire da Windows 7, agli utenti viene automaticamente richiesto di configurare la funzionalità Windows Backup se non lo hanno già fatto. Queste notifiche vengono visualizzate all'avvio del computer, a partire da sette giorni dopo l'installazione del sistema operativo. Vengono visualizzati anche quando l'utente collega un'unità disco rigido; In questo caso, le notifiche vengono visualizzate immediatamente.

Gli OEM e gli sviluppatori di applicazioni di backup di terze parti possono usare il valore del Registro di sistema **DisableMonitoring** per disattivare queste notifiche automatiche.

Questo valore non esiste per impostazione predefinita, quindi deve essere creato con la chiave del Registro di sistema seguente:

**HKEY \_ LOCAL \_ MACHINE** \\ **SOFTWARE** \\ **Microsoft** \\ **Windows** \\ **CurrentVersion** \\ **WindowsBackup**

Il valore del Registro di sistema **DisableMonitoring** ha il tipo di dati REG \_ DWORD e viene interpretato come segue:

-   Se i dati del valore sono impostati su 1 e se gli utenti non hanno già configurato la funzionalità Windows Backup, le notifiche automatiche vengono disattivate. Se nel Centro notifiche è già presente una notifica automatica, l'impostazione di questo valore del Registro di sistema determina la rimozione della notifica alle 10:00 della mattina seguente.
-   Se il valore non esiste, se i relativi dati non sono impostati o se i relativi dati sono impostati su zero, le notifiche automatiche non vengono disattivate.

**Windows Vista e Windows XP:** Questo valore del Registro di sistema non è supportato.

## <a name="filesnottobackup"></a>FilesNotToBackup

La chiave del Registro di sistema **FilesNotToBackup** specifica i nomi dei file e delle directory di cui le applicazioni di backup non devono eseguire il backup o il ripristino. Ognuna delle voci in questa chiave è una stringa REG \_ MULTI \_ SZ nel formato seguente:

\[ \] Unità \[  \] Percorso \\ *FileName* \[ /s\]

-   *L'unità* specifica l'unità ed è facoltativa. Ad esempio, c:. Per specificare tutte le unità, usare una barra rovesciata ( \\ ); non sono necessarie lettere di unità.
-   *Path* specifica il percorso ed è facoltativo. Non può contenere caratteri jolly.
-   *FileName* specifica il file o la directory ed è obbligatorio. Può contenere caratteri jolly.
-   /s specifica che devono essere incluse tutte le sottodirectory del percorso specificato.
-   Le variabili di ambiente come %Systemroot% possono essere sostituite per tutta o parte dell'intera stringa.

La tabella seguente illustra alcune voci tipiche.

| Nome voce                             | Valore predefinito                                                                             |
|----------------------------------------|-------------------------------------------------------------------------------------------|
| Internet Explorer                      | File temporanei                                                                           |
| File di pagine di memoria                       | \\Pagefile.sys                                                                            |
| MS Distributed Transaction Coordinator | C: \\ Windows \\ \\ msdtc msdtc \\ system32. LOG C: \\ Windows \\ system32 \\ MSDtc \\ trace \\ dtctrace.log |
| File offline cache                    | %Systemroot% \\ CSC \\ \* /s                                                                  |
| Risparmio energia                       | \\hiberfil.sys                                                                            |
| Single Instance Storage (SIS)                | \\Archivio comune SIS \\ \* . \* /s                                                              |
| File temporanei                        | %TEMP% \\ \* /s                                                                             |



 

> [!Note]  
> Le applicazioni che eseguono backup a livello di volume in genere copiano l'intero volume a livello di blocco, quindi non possono rispettare la chiave del Registro di sistema **FilesNotToBackup** in fase di backup. Al contrario, attendono il tempo di ripristino per eliminare i file di cui non è stato eseguito il backup. Nella maggior parte dei casi si tratta di una strategia ragionevole. Tuttavia, nel caso di file di archivio Archiviazione istanza singola, i file di archivio comune SIS non devono essere eliminati in fase di ripristino.

 

Per i backup di volumi a livello di blocco, Windows Server Backup e l'utilità Windows Wbadmin rispettano la chiave del Registro di sistema **FilesNotToBackup** eliminando i file appropriati in fase di ripristino. Ripristino configurazione di sistema e il backup dello stato del sistema non rispettano la chiave del Registro di **sistema FilesNotToBackup.**

**Windows XP:** Ripristino configurazione di sistema rispetta la chiave **del Registro di sistema FilesNotToBackup.**

## <a name="filesnottosnapshot"></a>FilesNotToSnapshot

VSS supporta la chiave **del Registro di sistema FilesNotToSnapshot.** Le applicazioni e i servizi possono usare questa chiave per specificare i file da eliminare dalle nuove copie shadow create. Per altre informazioni, vedere [Esclusione di file da copie shadow.](/windows/desktop/VSS/excluding-files-from-shadow-copies)

**Windows Server 2003 e Windows XP:** Questa chiave del Registro di sistema non è supportata.

Per i backup di volumi a livello di blocco, Windows Server Backup rispetta la chiave del Registro di sistema **FilesNotToSnapshot** eliminando i file appropriati in fase di ripristino.

## <a name="idletimeout"></a>IdleTimeout

Il valore del Registro di sistema **IdleTimeout** specifica la quantità di tempo, in secondi, di attesa del servizio VsS quando è inattivo. Se questo valore di timeout viene raggiunto e non sono presenti attività da eseguire, il servizio VsS verrà arrestato.

Questo valore del Registro di sistema è disponibile nella chiave del Registro di sistema seguente:

**HKEY \_ Local \_ MACHINE** \\ **System** \\ **CurrentControlSet** \\ **Services** \\ **VSS** \\ **Impostazioni**

Se questo valore del Registro di sistema non esiste:

-   Il valore di timeout effettivo usato è 180 secondi (3 minuti) per impostazione predefinita.
-   È possibile creare un valore con il nome **IdleTimeout** e il tipo DWORD e impostarlo sul valore desiderato.

Se questo valore del Registro di sistema è impostato su 0 secondi:

-   Il valore di timeout effettivo usato è 180 secondi (3 minuti).

Se si imposta questo valore del Registro di sistema:

-   VSS usa il valore di timeout impostato.
-   È possibile specificare qualsiasi valore compreso tra 1 e FFFFFFFF secondi. È tuttavia consigliabile scegliere un valore compreso tra 1 e 180 secondi.

**Windows Server 2003 e Windows XP:** Questa chiave del Registro di sistema non è supportata.

## <a name="keysnottorestore"></a>KeysNotToRestore

La chiave del Registro di sistema **KeysNotToRestore** specifica i nomi delle sottochiavi del Registro di sistema e i valori che le applicazioni di backup non devono ripristinare. Per altre informazioni, vedere [KeysNotToRestore](/previous-versions/windows/it-pro/windows-server-2003/cc737538(v=ws.10)). Non è necessario rispettare la chiave **del Registro di sistema KeysNotToRestore.**

**Windows Server 2003 e Windows XP:** È necessario rispettare la chiave **del Registro di sistema KeysNotToRestore.**

Per i backup di volumi a livello di blocco, Windows Backup del server rispetta la chiave del Registro di sistema **KeysNotToRestore** eliminando i file appropriati in fase di ripristino.

Il backup dello stato del sistema rispetta la **chiave del Registro di sistema KeysNotToRestore.**

## <a name="lastinstance"></a>LastInstance

Il valore del Registro di sistema **LastInstance** indica che è stata eseguita un'operazione di ripristino bare metal e che i volumi sono stati sovrascritti ma non formattati. Per altre informazioni, vedere [Using VSS Automated Ripristino di sistema for Disaster Recovery](/windows/desktop/VSS/using-vss-automated-system-recovery-for-disaster-recovery).

**Windows Server 2003 e Windows XP:** Questo valore del Registro di sistema non è supportato.

## <a name="lastrestoreid"></a>LastRestoreId

Quando un'applicazione di backup esegue un ripristino dello stato del sistema, deve indicare che l'operazione è stata eseguita impostando il valore del Registro di sistema **LastRestoreId.** "Ripristino dello stato del sistema" in questo caso si riferisce a qualsiasi ripristino che ripristini in modo selettivo i file binari e i driver del sistema operativo.

Se l'intero volume di avvio e di sistema viene ripristinato a livello di volume, questo valore non deve essere impostato.

Se il valore del Registro di sistema **LastRestoreId** non esiste, l'applicazione di backup deve crearlo nella chiave del Registro di sistema seguente:

**HKEY \_ Controllo \_** \\  \\ **CurrentControlSet del sistema LOCAL** MACHINE \\  \\ **BackupRestore** \\ **SystemStateRestore**

Creare un valore con il nome **LastRestoreId** e digitare REG \_ SZ. Il valore deve essere un valore opaco univoco, ad esempio un GUID.

Ogni volta che viene eseguito un nuovo ripristino dello stato del sistema, l'applicazione di backup deve modificare i dati del **valore LastRestoreId.**

Altre applicazioni che devono monitorare i ripristini dello stato del sistema devono archiviare i dati di questo valore del Registro di sistema. Questi dati possono essere confrontati con i dati correnti del valore del Registro di sistema **LastRestoreId** per determinare se è stato eseguito un nuovo ripristino dello stato del sistema.

**Windows Vista, Windows Server 2003 e Windows XP:** Questo valore del Registro di sistema non è supportato fino Windows Vista con Service Pack 1 (SP1) e Windows Server 2008.

## <a name="maxshadowcopies"></a>MaxShadowCopies

Il valore del Registro di sistema **MaxShadowCopies** specifica il numero massimo di [*copie shadow*](/windows/desktop/VSS/vssgloss-c) accessibili dal client che possono essere archiviate in ogni volume del computer. Una copia shadow accessibile dal client è una copia shadow creata usando il valore **VSS \_ CTX \_ CLIENT \_ ACCESSIBLE** dell'enumerazione [**\_ VSS \_ SNAPSHOT \_ CONTEXT.**](/windows/desktop/api/vss/ne-vss-vss_snapshot_context) Le copie shadow accessibili dal client vengono usate da Copie shadow di cartelle condivise. Per altre informazioni sulle copie shadow, vedere la documentazione [di VSS.](/windows/desktop/VSS/volume-shadow-copy-service-portal)

Se il valore del Registro di sistema **MaxShadowCopies** non esiste, l'applicazione di backup può crearlo nella chiave del Registro di sistema seguente:

**HKEY \_ Local \_ MACHINE** \\ **System** \\ **CurrentControlSet** \\ **Services** \\ **VSS** \\ **Impostazioni**

Creare un valore con il nome **MaxShadowCopies e** digitare DWORD. I dati predefiniti per questo valore sono 64. Il valore minimo è 1. Il valore massimo è 512.

> [!Note]  
> Per altri tipi di copie shadow, non esiste alcun valore del Registro di sistema corrispondente a **MaxShadowCopies**. Il numero massimo di copie shadow è 512 per ogni volume.

 

**Nota:**  **L'impostazione MaxShadowCopies** è supportata Windows Server 2003 o versione successiva.

**Windows Server 2003:** Nei server del cluster, i dati del valore del Registro di sistema **MaxShadowCopies** potrebbero dover essere impostati su un numero inferiore. Per altre informazioni, vedere "Quando si usa Servizio Copia Shadow del volume nei computer basati su Windows Server 2003 che eseguono molte operazioni di I/O, i volumi del disco hanno più tempo per essere online" nella guida e supporto tecnico Knowledge Base all'indirizzo [https://support.microsoft.com/kb/945058](https://support.microsoft.com/kb/945058) .

**Windows XP:** Questo valore del Registro di sistema non è supportato.

## <a name="mindiffareafilesize"></a>MinDiffAreaFileSize

[VSS](/windows/desktop/VSS/volume-shadow-copy-service-portal) alloca un'area di archiviazione delle copie shadow (o "area diff") per archiviare i dati per le copie shadow. La dimensione minima dell'area di archiviazione delle copie shadow è un'impostazione per computer che può essere specificata usando il valore del Registro di sistema **MinDiffAreaFileSize.**

Se il valore del Registro di sistema **MinDiffAreaFileSize** non è impostato, le dimensioni minime dell'area di archiviazione delle copie shadow sono 32 MB per i volumi inferiori a 500 MB e 320 MB per i volumi maggiori di 500 MB.

**Windows Server 2008, Windows Server 2003 con SP1 e Windows Vista:** Se il valore del Registro di sistema **MinDiffAreaFileSize** non è impostato, l'area di archiviazione delle copie shadow ha una dimensione minima di 300 MB. Se il valore del Registro di sistema **MinDiffAreaFileSize** è impostato, i dati devono essere compresi tra 300 MB e 3000 MB (3 GB) e devono essere multipli di 300 MB.

**Windows Server 2003:** Se il valore del Registro di sistema **MinDiffAreaFileSize** non è impostato, le dimensioni minime dell'area di archiviazione delle copie shadow sono pari a 100 MB.

**Windows XP:** Questo valore del Registro di sistema non è supportato.

Se il valore del Registro di sistema **MinDiffAreaFileSize** non esiste, l'applicazione di backup può crearlo nella chiave del Registro di sistema seguente:

**HKEY \_ Local \_ MACHINE** \\ **System** \\ **CurrentControlSet** \\ **Services** \\ **VolSnap**

Creare un valore con il nome **MinDiffAreaFileSize** e digitare REG \_ DWORD. I dati per questa chiave sono specificati in megabyte. 320 è uguale a 320 MB e 3200 è uguale a 3,2 GB. È necessario specificare un numero multiplo di 32. Se si specifica un valore che non è un multiplo di 32, verrà usato il multiplo successivo di 32.

Le copie shadow potrebbero non funzionare correttamente se il valore del Registro di sistema **MinDiffAreaFileSize** specifica una dimensione minima maggiore della dimensione massima dell'area di archiviazione della copia shadow. Per specificare le dimensioni massime dell'area di archiviazione delle copie shadow, usare il comando [Vssadmin](/previous-versions/windows/it-pro/windows-server-2012-R2-and-2012/cc754968(v=ws.11)) add shadowstorage o vssadmin resize shadowstorage. Per visualizzare le dimensioni massime correnti, usare il [comando Vssadmin list shadowstorage.](/previous-versions/windows/it-pro/windows-server-2012-R2-and-2012/cc754968(v=ws.11)) Se non è stata impostata una dimensione massima, non esiste alcun limite alla quantità di spazio che può essere usata.

## <a name="overallperformancesetting-and-customperformancesettings"></a>OverallPerformanceSetting e CustomPerformanceSettings

I valori del Registro di sistema **OverallPerformanceSetting** e **CustomPerformanceSettings** vengono usati per specificare le impostazioni delle prestazioni per Windows Server Backup. Questi valori del Registro di sistema sono supportati solo Windows sistemi operativi server.

**Windows Server 2003:** Questi valori del Registro di sistema non sono supportati.

Se questi valori del Registro di sistema non esistono, l'applicazione di backup può crearli nella chiave del Registro di sistema seguente:

**HKEY \_ LOCAL \_ MACHINE** \\ **SOFTWARE** \\ **Microsoft** \\ **Windows** \\ **CurrentVersion Windows** backup a livello di \\ **blocco**

Per specificare le impostazioni delle prestazioni per tutti i volumi, creare un valore con il nome **OverallPerformanceSetting** e digitare REG \_ DWORD. I dati del valore devono essere impostati su uno dei valori seguenti.

| Valore | Significato                                                                                                                                                                                                                                   |
|-------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 1     | Prestazioni di backup normali (tramite backup completi). Questa impostazione corrisponde all'impostazione Prestazioni di backup normali descritta in [Ottimizzazione delle prestazioni del backup e del server](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/dd759145(v=ws.11)).            |
| 2     | Prestazioni di backup più veloci (tramite backup incrementali). Questa impostazione corrisponde all'impostazione Prestazioni di backup più veloci descritta in [Ottimizzazione delle prestazioni del backup e del server](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/dd759145(v=ws.11)).     |
| 3     | Prestazioni di backup personalizzate (specificando un'impostazione delle prestazioni per ogni volume). Questa impostazione corrisponde all'impostazione Personalizzata descritta in [Ottimizzazione delle prestazioni del backup e del server](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/dd759145(v=ws.11)). |



 

Se si imposta **OverallPerformanceSetting** su 3, è necessario specificare anche le impostazioni delle prestazioni per ogni singolo volume. A tale scopo, creare un valore con il nome **CustomPerformanceSettings** e digitare REG \_ MULTI \_ SZ. I dati di questo valore devono essere impostati come segue:

-   Ogni stringa nella sequenza di stringhe REG \_ MULTI \_ SZ contiene l'impostazione per un volume.
-   Ogni stringa è costituita da un GUID del volume, seguito da una virgola e da un valore DWORD.
-   Ognuno dei valori DWORD è 1 (backup completo) o 2 (backup incrementale).

Si supponga, ad esempio, che il computer abbia due volumi come segue:

-   I due volumi sono C: \\ e D: \\ .
-   Il GUID per il volume C: è \\ 07c473ca4-2df8-11de-9d80-806e6f6e6963 e il GUID per il volume D: \\ è 0ac22ea6c-712f-11de-adb0-00215a67606e.
-   Si vuole specificare una normale perfornance di backup per il volume C: e prestazioni di backup più \\ veloci per il volume D: \\ .

A tale scopo, Si imposta **OverallPerformanceSetting** su 3 e **CustomPerformanceSettings** su "07c473ca4-2df8-11de-9d80-806e6f6e6963,1 \\ 00ac22ea6c-712f-11de-adb0-00215a67606e,2".

Se si imposta **OverallPerformanceSetting** su 1 o 2, i dati nel **valore CustomPerformanceSettings** vengono ignorati.

## <a name="sysvol"></a>SYSVOL

Il valore del Registro di sistema **SYSVOL** consente di notificare al servizio replica file system distribuito (DFSR) che è stata avviata un'operazione di ripristino dello stato del sistema. Qualsiasi applicazione di backup che esegue il ripristino dello stato del sistema di SYSVOL deve usare questo valore per indicare se l'operazione di ripristino è autorevole o non autorevole. Questo valore viene letto dal servizio DFSR. Se questo valore non è impostato, il ripristino SYSVOL viene eseguito in modo non autorevole per impostazione predefinita.

Se il valore del Registro di sistema **SYSVOL** non esiste, l'applicazione di backup deve crearlo nella chiave del Registro di sistema seguente:

**HKEY \_ Ripristino \_** \\  \\ DFSR del sistema **CurrentControlSet** \\ **del** \\ **sistema** \\ **LOCAL MACHINE**

Creare un valore con il nome **SYSVOL** e digitare REG \_ SZ. I dati del valore devono essere impostati su "autorevole" o "non autorevole" in base alla richiesta dell'amministratore di sistema.

**Windows Vista, Windows Server 2003 e Windows XP:** Questo valore del Registro di sistema non è supportato.

 

 
