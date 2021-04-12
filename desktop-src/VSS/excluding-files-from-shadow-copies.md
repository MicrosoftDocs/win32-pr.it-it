---
description: In Windows Vista e Windows Server 2008 e versioni successive lo sviluppatore di un VSS writer o di un'applicazione può scegliere di escludere determinati file dalle copie shadow.
ms.assetid: 4fe1ae94-7b2f-421a-9009-3a7e88822458
title: Esclusione di file dalle copie shadow
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 52546c8ddc6da62433dc610f2bf4fc2c46c5e53f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104233825"
---
# <a name="excluding-files-from-shadow-copies"></a>Esclusione di file dalle copie shadow

In Windows Vista e Windows Server 2008 e versioni successive lo sviluppatore di un VSS writer o di un'applicazione può scegliere di escludere determinati file dalle copie shadow.

L'utilizzo dell'area di archiviazione delle copie shadow e dell'effetto sulle prestazioni (detto anche "area diff") di un file in una copia shadow è direttamente correlato alla quantità di modifiche apportate al contenuto del file dopo la creazione della copia shadow. Inoltre, l'esclusione dei file dalle copie shadow può rallentare la creazione della copia shadow.

Per questi motivi, un file deve essere escluso dalle copie shadow solo se è di grandi dimensioni, subisce una modifica significativa tra una copia shadow e la successiva e non è necessario eseguirne il backup.

È necessario escludere solo i file che appartengono all'applicazione.

Se \_ \_ \_ \_ nel contesto della copia shadow non è impostato il flag VolSnap attr senza recupero automatico, significa che il ripristino automatico è disabilitato e non è possibile escludere alcun file dalla copia shadow. Per ulteriori informazioni, vedere l'enumerazione [**\_ VSS \_ volume \_ snapshot \_ Attributes**](/windows/desktop/api/Vss/ne-vss-vss_volume_snapshot_attributes) .

## <a name="using-the-addexcludefilesfromsnapshot-method"></a>Utilizzo del metodo AddExcludeFilesFromSnapshot

Un VSS writer può escludere i file da una copia shadow come indicato di seguito:

1.  Chiamare il metodo [**IVssCreateWriterMetadataEx:: AddExcludeFilesFromSnapshot**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadataex-addexcludefilesfromsnapshot) per segnalare i file da escludere.
2.  Nel metodo [**CVssWriter:: OnPostSnapshot**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onpostsnapshot) del writer eliminare i file dalla copia shadow.

## <a name="using-the-filesnottosnapshot-registry-key"></a>Uso della chiave del registro di sistema FilesNotToSnapshot

> [!Note]  
> La chiave del Registro di sistema **FilesNotToSnapshot** deve essere usata solo dalle applicazioni. Gli utenti che tentano di usarla incontreranno limitazioni come le seguenti:
>
> -   Non è possibile eliminare file da una copia shadow creata in un server Windows usando la funzionalità Versioni precedenti.
> -   Non è possibile eliminare file dalle copie shadow per cartelle condivise.
> -   Consente di eliminare i file da una copia shadow creata con l'utilità [DiskShadow](/previous-versions/windows/it-pro/windows-server-2012-R2-and-2012/cc772172(v=ws.11)) , ma non di eliminare i file da una copia shadow creata tramite l'utilità [vssadmin](/previous-versions/windows/it-pro/windows-server-2012-R2-and-2012/cc754968(v=ws.11)) .
> -   I file vengono eliminati da una copia shadow in base al massimo sforzo. Ciò significa che non è garantito che vengano eliminati.

 

Un'applicazione VSS può eliminare i file da una copia shadow durante la creazione della copia shadow utilizzando la seguente chiave del registro di sistema:

**HKEY \_ Local \_ computer \\ System \\ CurrentControlSet \\ Control \\ backuprestore \\ FilesNotToSnapshot**

Questa chiave del registro di sistema contiene \_ \_ i valori reg multisz per ogni applicazione i cui file possono essere esclusi. I file vengono specificati da percorsi completi che possono contenere il \* carattere jolly.

In tutti i casi, la voce viene ignorata se non sono presenti file che corrispondono alla stringa di percorso.

Dopo l'aggiunta di un file al valore appropriato della chiave del registro di sistema, questo viene eliminato dalla copia shadow durante la creazione da parte del writer di ottimizzazione della copia shadow nel modo più semplice possibile.

Se non è possibile specificare un percorso completo, è possibile usare anche un percorso usando la variabile $UserProfile $ o $AllVolumes $. Ad esempio:

-   \\ \\ Nome file della sottodirectory $USERPROFILE $ directory \\ .\*
-   $AllVolumes $ \\ TemporaryFiles \\ \* .\*

Per rendere ricorsivo il percorso, aggiungere "/s" alla fine. Ad esempio:

-   $UserProfile $ \\ directory \\ subdirectory \\ filename. \* /s
-   $AllVolumes $ \\ TemporaryFiles \\ \* . \* /s

La variabile $UserProfile $ fa sì che la stringa di percorso venga applicata a tutti i profili utente nel computer. Per enumerare i profili utente, esaminare la seguente chiave del registro di sistema:

**HKEY \_ Local \_ Machine \\ software \\ Microsoft \\ Windows NT \\ CurrentVersion \\ Profiler**

La variabile $AllVolumes $ fa sì che la stringa di percorso venga applicata a tutte le copie shadow nel computer. Si supponga, ad esempio, che il percorso sia "$AllVolumes $ \\ TemporaryFiles \\ \* . \* /s "e il computer dispone di tre volumi: C:, D: e E:. Se C: e e: contengono il percorso " \\ TemporaryFiles \\ " e volume d: contiene solo il percorso D: \\ dati \\ , l'albero di directory C: \\ TemporaryFiles \\ viene eliminato dalle copie shadow di c: e la struttura di directory e: \\ TemporaryFiles \\ viene eliminata dalle copie shadow di E:.

Gli amministratori possono disabilitare l'espansione della variabile $UserProfile $ usando la chiave del registro di sistema seguente:

**\_Impostazioni del \_ servizio Copia Shadow del volume del \\ sistema \\ CurrentControlSet \\ \\ \\ HKEY**

In questa chiave del registro di sistema specificare DisableUserProfileExpansion per il nome del valore, REG \_ DWORD per il tipo di valore e un valore diverso da zero per i dati del valore.

## <a name="about-the-filesnottobackup-registry-key"></a>Informazioni sulla chiave del registro di sistema FilesNotToBackup

La chiave del registro di sistema **FilesNotToBackup** può essere utilizzata per specificare i nomi dei file e delle directory per le quali le applicazioni di backup non devono eseguire il backup o il ripristino. Tuttavia, non esclude tali file dalle copie shadow. Per ulteriori informazioni su questa chiave del registro di sistema, vedere [chiavi e valori del registro di sistema per il backup e il ripristino](../backup/registry-keys-for-backup-and-restore.md).

 

 
