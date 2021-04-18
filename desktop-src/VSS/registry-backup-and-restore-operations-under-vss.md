---
description: Il servizio Registro di sistema di Windows supporta un VSS writer, denominato writer del registro di sistema, che consente ai richiedenti di eseguire il backup di un registro di sistema usando i dati archiviati in un volume copiato da un'ombreggiatura.
ms.assetid: 94a45b04-0bdc-4211-bed0-caeabba774af
title: Operazioni di backup e ripristino del registro di sistema in VSS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: db1a3022ec2fb08b07bcff8b28455ae7154e4c40
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106310677"
---
# <a name="registry-backup-and-restore-operations-under-vss"></a>Operazioni di backup e ripristino del registro di sistema in VSS

Il servizio Registro di sistema di Windows supporta un VSS writer, denominato writer del registro di sistema, che consente ai richiedenti di eseguire il backup di un registro di sistema usando i dati archiviati in un volume copiato da un'ombreggiatura. Per ulteriori informazioni sul writer del registro di sistema, vedere la pagina relativa ai [writer VSS](in-box-vss-writers.md).

Il writer del registro di sistema esegue backup sul posto e ripristini del registro di sistema. Inoltre, il writer del registro di sistema segnala solo hive di sistema; non segnala gli hive degli utenti.

**Windows Server 2003:** Il writer del registro di sistema utilizza un file di repository intermedio (noto anche come file spit) per archiviare i dati del registro di sistema. Inoltre, il writer del registro di sistema segnala hive di sistema e hive utente.

L'ID del writer per il writer del registro di sistema è AFBAB4A2-367D-4D15-A586-71DBB18F8485.

**Windows XP:** Nessun writer del registro di sistema. I dati del registro di sistema vengono segnalati dal writer dello stato di avvio, il cui ID writer è F2436E37-09F5-41AF-9B2A-4CA2435DBFD5.

> [!Note]  
> Microsoft non fornisce supporto tecnico per sviluppatori o professionisti IT per l'implementazione di ripristini dello stato del sistema online in Windows (tutte le versioni). Per informazioni sull'uso di API e procedure fornite da Microsoft per implementare il ripristino dello stato del sistema online, vedere le risorse della community disponibili in [MSDN Community Center](https://msdn.microsoft.com/community/default.aspx).

 

> [!Note]  
> Le informazioni seguenti si applicano solo a Windows Server 2003 e Windows XP.

 

## <a name="registry-backup-using-vss"></a>Backup del registro di sistema con VSS

Il writer del registro di sistema esporterà e salverà i file del registro di sistema attivi nei percorsi definiti dalla chiave **HKEY \_ Local \_ Machine** \\ **System** \\ **CurrentControlSet** \\ **Control** \\ **hive**.

I nomi dei valori in questa voce del registro di sistema identificano l'hive del registro di sistema da salvare e i dati del valore forniscono il file che contiene il file (il file hive). I file hive vengono specificati con il formato seguente: \\ Device \\ *HarddiskVolumeX* \\ *path* \\ *filename*.

Ad esempio, in **HKEY \_ Local \_ Machine** \\ **System** \\ **CurrentControlSet** \\ **Control** \\ **hive**, è possibile vedere il registro di sistema **\\ del dispositivo \\ \\ software**  =  \\ Device \\ HarddiskVolume1 \\ Windows \\ system32 \\ config \\ software.

Il writer del registro di sistema garantisce che i file hive vengano salvati su disco prima della relativa copia shadow.

Quando si esegue il backup degli hive del registro di sistema, un richiedente sostituisce il \\ dispositivo \\ *HarddiskVolumeX* con la stringa dell' [*oggetto dispositivo*](vssgloss-d.md) della copia shadow del volume.

> [!Note]  
> È possibile convertire il \\ percorso \\ *HarddiskVolumeX* del dispositivo in un percorso Win32 equivalente usando la funzione [**QueryDosDevice**](/windows/win32/api/fileapi/nf-fileapi-querydosdevicew) . Per ulteriori informazioni, vedere [ottenere un nome di file da un handle di file](../memory/obtaining-a-file-name-from-a-file-handle.md) o [visualizzare i nomi dei percorsi dei volumi](../fileio/displaying-volume-paths.md).

 

## <a name="registry-restore-using-non-vss-win32-apis"></a>Ripristino del registro di sistema mediante API Win32 non VSS

Per un ripristino in linea (modalità provvisoria o completa), è necessario mantenere le sottochiavi della chiave del registro di sistema **HKEY \_ Local \_ computer** \\ **System** \\ **CurrentControlSet** \\ **Control** \\ **Session Manager** \\ **PendingFileRenameOperations** .

Le funzioni [**MoveFileEx**](/windows/win32/api/winbase/nf-winbase-movefileexa) e [**MoveFileTransacted**](/windows/win32/api/winbase/nf-winbase-movefiletransacteda) usano questa chiave del registro di sistema per archiviare le informazioni sui file che sono stati rinominati usando il ritardo MOVEFILE \_ fino al \_ \_ valore di riavvio nel parametro *dwFlags* .

Per mantenere il contenuto della chiave del registro di sistema **PendingFileRenameOperations** , è necessario che l'applicazione di backup chiami la funzione [**RegLoadKey**](/windows/win32/api/winreg/nf-winreg-regloadkeya) per connettere il file del registro di sistema da ripristinare al registro di sistema attivo. L'applicazione di backup può quindi usare le varie funzioni del registro di sistema per copiare le chiavi e i valori desiderati nell'hive caricato. Al termine della copia, è necessario chiamare le funzioni [**RegFlushKey ha**](/windows/win32/api/winreg/nf-winreg-regflushkey) e [**RegUnLoadKey**](/windows/win32/api/winreg/nf-winreg-regunloadkeya) .

Per un ripristino offline (ambiente ripristino Windows o Windows PE), non è necessario rispettare la chiave del registro di sistema **PendingFileRenameOperations** .

## <a name="registry-restore-using-non-vss-win32-apis-in-windows-server-2003"></a>Ripristino del registro di sistema mediante API Win32 non VSS in Windows Server 2003

> [!Note]  
> Le informazioni seguenti si applicano solo alle operazioni di ripristino correlate al ripristino di emergenza (noto anche come ripristino bare metal) che vengono eseguite in Windows Server 2003.

 

Quando si ripristina il registro di sistema, un'applicazione di backup deve spostare alcune delle sottochiavi dal registro di sistema corrente al registro di sistema da ripristinare.

A tale scopo, un'applicazione di backup può chiamare **RegLoadKey** per connettere il file del registro di sistema da ripristinare al registro di sistema attualmente attivo. Può quindi usare le varie funzioni del registro di sistema per copiare le chiavi e i valori desiderati nell'hive caricato. Al termine della copia, vengono chiamati **RegFlushKey ha** e **RegUnLoadKey** .

È presente una chiave del registro di sistema che indica a un'applicazione di ripristino (richiedente) le chiavi del registro di **sistema in HKEY \_ \_ computer \\ locale** che non devono essere sovrascritte in fase di ripristino:

**HKEY \_ Local \_ computer \\ System \\ CurrentControlSet \\ Control \\ backuprestore \\ KeysNotToRestore**

Parte del processo di ripristino dello stato del sistema comporta il ripristino di un registro di sistema eseguito in precedenza.

Le applicazioni di backup devono prestare particolare attenzione durante il ripristino dell'hive di **\_ \_ \\ sistema del computer locale HKEY** , perché il processo di installazione di una versione temporanea del sistema operativo Windows avrà le chiavi stabilite nell'hive di sistema appena installato i cui valori devono sopravvivere all'operazione di ripristino.

Ad esempio, quando il sistema di sostituzione ha una scheda di interfaccia di rete diversa dal sistema originale, il ripristino delle chiavi originali per la scheda precedente comporterà risultati imprevedibili. Questo è dovuto al fatto che il servizio Plug and Play ha rilevato e inserito nel registro di sistema le voci appropriate del registro di sistema del driver e del servizio. Questi valori devono essere conservati per eseguire correttamente l'avvio dopo il ripristino del sistema.

Questa sezione descrive il modo in cui le applicazioni di backup possono individuare quali chiavi e file devono essere conservati durante l'esecuzione di un ripristino dell'hive di **\_ \_ \\ sistema del computer locale HKEY** . In alcuni casi, questa operazione comporterà la copia a livello di codice delle chiavi dall'hive di installazione appena installato nell'hive da ripristinare. In altri casi, assicurandosi che le chiavi del registro di sistema di un prodotto non vengano sostituite, è sufficiente specificare tali chiavi nel file di configurazione INF del prodotto.

Le chiavi (e i dati chiave) che devono essere mantenute vengono enumerate nell'hive di **\_ \_ \\ sistema del computer locale HKEY** nel

**HKEY \_ Local \_ computer \\ System \\ CurrentControlSet \\ Control \\ backuprestore \\ KeysNotToRestore**

chiave come set di \_ stringhe reg \_ multisz (denominate *stringhe chiave* in questo documento).

Un'applicazione di backup (richiedente) deve esaminare i valori di queste chiavi nel registro di sistema attivo e il registro di sistema appena ripristinato, perché qualsiasi applicazione o servizio può aggiungere valori in qualsiasi momento.

Il modo in cui le stringhe di chiave devono essere interpretate dalle applicazioni di backup è determinato dal carattere terminale:

1.  Le stringhe chiave terminate con una barra rovesciata (' \\ ') vengono interpretate come sottochiavi. Quando viene rilevata una sottostringa di questo tipo, l'applicazione di backup deve conservare tutti i dati e tutte le chiavi subordinate.

    Ad esempio, il codice seguente specifica che tutte le chiavi e i dati subordinati devono essere conservati durante un'operazione di ripristino:

    **HKEY \_ Local \_ computer \\ System \\ CurrentControlSet \\ Services \\ dmio \\ boot info\\**

    A questo scopo, questa chiave e tutte le chiavi e i dati subordinati devono essere copiati dal registro di sistema esistente (ovvero quello creato dall'installazione di Windows) nel registro di sistema appena ripristinato. Questa operazione è detta operazione di *sostituzione della chiave* . Questa operazione sostituisce la chiave corrispondente nel registro di sistema ripristinato.

2.  Le stringhe chiave il cui carattere di terminazione è un asterisco (' \* ') specificano che tutte le sottochiavi devono essere unite. Ad esempio, la stringa chiave:

    **HKEY \_ \_ \\ \\ \\ Servizi \\ CurrentControlSet di sistema del computer locale \** _

    Specifica che la chiave dei servizi nel registro di sistema esistente, ad esempio quelle create dall'installazione di Windows, deve essere unita nel registro di sistema ripristinato. Si tratta di un'operazione di merge * _key e, se è presente una sottochiave nell'hive esistente e nell'hive ripristinato, la chiave nella directory ripristinata viene mantenuta con le eccezioni seguenti:

    -   Se la sottochiave nell'hive esistente contiene un valore denominato "Start" e la sottochiave nel ripristino non lo è.
    -   Se la sottochiave nell'hive esistente e ripristinato contiene un valore denominato "Start" e il relativo valore numerico nell'hive esistente è minore.

    Il valore "Start" nel registro di sistema specifica quando un servizio o un driver si avvierà e può avere un valore numerico compreso tra 0-4. Più basso è il valore, prima nel processo di avvio il servizio inizierà.

    Se questa chiave è presente nella directory esistente e ripristinata, è necessario esaminare il valore della chiave di avvio in ogni hive. Se il valore nell'hive esistente è inferiore al valore della directory ripristinata, è necessario mantenere il valore inferiore.

    Ancora una volta, questa chiave viene usata per determinare se un servizio o un driver deve essere avviato in fase di avvio, in fase di sistema, manualmente, automaticamente o essere disabilitato. Il valore inferiore rappresenta un'ora di inizio precedente. L'ora di inizio precedente deve essere applicata al nuovo registro di sistema per assicurarsi che il servizio o i driver vengano avviati correttamente all'avvio successivo.

3.  Le stringhe chiave il cui carattere di terminazione non è né una barra rovesciata né un asterisco vengono interpretate come valori del registro di sistema da mantenere.

    Ad esempio, la stringa chiave:

    **HKEY \_ Local \_ computer \\ System \\ CurrentControlSet \\ Control \\ Session Manager \\ PendingFileRenameOperations**

    Il meccanismo mediante il quale è possibile mantenere le chiavi a livello di codice comporta l'API del registro di sistema Win32. Un algoritmo, ad esempio, è enumerato di seguito:

    1.  Ripristinare il file hive di sistema di cui è stato eseguito il backup in un file. Per questo esempio, lasciare che il nome sia System. reg.
    2.  Usare **RegLoadKey** per caricare System. reg nel **\_ \_ computer locale HKEY** con un nome temporaneo. Ad esempio, un nome di questo tipo potrebbe essere

        **\_ \_ sistema TMP del computer locale \\ HKEY \_**

    3.  Enumerare i valori nella sottochiave **KeysNotToRestore** da entrambe le copie del registro di sistema e creare un superset degli elenchi. Copia ogni chiave di questo elemento dalla esistente

        **\_sistema del \_ computer \\ locale HKEY**

        chiave in

        **\_ \_ sistema TMP del computer locale \\ HKEY \_**

        chiave in base alla semantica descritta in precedenza.

    4.  Al termine, usare i  &  punti di ingresso **RegUnLoadKey** di RegFlushKey ha per salvare il

        **\_ \_ sistema TMP del computer locale \\ HKEY \_**

        tornare alla chiave System. reg.

    5.  Infine, usare **RegReplaceKey** per specificare che System. reg sostituisce il

        **\_sistema del \_ computer \\ locale HKEY**

        file hive, SYSTEM.

 

 
