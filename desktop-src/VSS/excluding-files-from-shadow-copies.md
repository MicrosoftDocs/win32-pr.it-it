---
description: In Windows Vista e Windows Server 2008 e versioni successive, lo sviluppatore di un VSS writer o di un'applicazione può scegliere di escludere determinati file dalle copie shadow.
ms.assetid: 4fe1ae94-7b2f-421a-9009-3a7e88822458
title: Esclusione di file da copie shadow
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c39acf8c92d44bcf8786a880b6ae5eb6a88786809f5af1609dee1b342cd2fb65
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118122108"
---
# <a name="excluding-files-from-shadow-copies"></a>Esclusione di file da copie shadow

In Windows Vista e Windows Server 2008 e versioni successive, lo sviluppatore di un VSS writer o di un'applicazione può scegliere di escludere determinati file dalle copie shadow.

L'impatto sulle prestazioni e l'utilizzo dell'area di archiviazione della copia shadow (detta anche "area diff") di un file in una copia shadow sono direttamente correlati alla quantità di modifiche nel contenuto del file dopo la creazione della copia shadow. Inoltre, l'esclusione di file dalle copie shadow può rallentare la creazione della copia shadow.

Per questi motivi, un file deve essere escluso dalle copie shadow solo se è di grandi dimensioni, subisce modifiche significative tra una copia shadow e la successiva e non è necessario eseguire il backup.

È consigliabile escludere solo i file che appartengono all'applicazione.

Se il \_ flag VSS VOLSNAP \_ ATTR \_ NO AUTORECOVERY è impostato nel contesto della copia shadow, significa che il ripristino automatico è disabilitato e nessun file può essere escluso dalla \_ copia shadow. Per altre informazioni, vedere l'enumerazione [**\_ VSS \_ VOLUME \_ SNAPSHOT \_ ATTRIBUTES.**](/windows/desktop/api/Vss/ne-vss-vss_volume_snapshot_attributes)

## <a name="using-the-addexcludefilesfromsnapshot-method"></a>Uso del metodo AddExcludeFilesFromSnapshot

Un VSS writer può escludere file da una copia shadow come indicato di seguito:

1.  Chiamare il [**metodo IVssCreateWriterMetadataEx::AddExcludeFilesFromSnapshot**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadataex-addexcludefilesfromsnapshot) per segnalare i file da escludere.
2.  Nel metodo [**CVssWriter::OnPostSnapshot**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onpostsnapshot) del writer eliminare i file dalla copia shadow.

## <a name="using-the-filesnottosnapshot-registry-key"></a>Uso della chiave del Registro di sistema FilesNotToSnapshot

> [!Note]  
> La chiave del Registro di sistema **FilesNotToSnapshot** deve essere usata solo dalle applicazioni. Gli utenti che tentano di usarla incontreranno limitazioni come le seguenti:
>
> -   Non è possibile eliminare file da una copia shadow creata in un server Windows usando la funzionalità Versioni precedenti.
> -   Non è possibile eliminare file dalle copie shadow per cartelle condivise.
> -   Può eliminare file da una copia shadow creata tramite l'utilità [DiskShadow,](/previous-versions/windows/it-pro/windows-server-2012-R2-and-2012/cc772172(v=ws.11)) ma non da una copia shadow creata tramite l'utilità [Vssadmin.](/previous-versions/windows/it-pro/windows-server-2012-R2-and-2012/cc754968(v=ws.11))
> -   I file vengono eliminati da una copia shadow in base al massimo sforzo. Ciò significa che non è garantito che vengano eliminati.

 

Un'applicazione VSS può eliminare file da una copia shadow durante la creazione della copia shadow usando la chiave del Registro di sistema seguente:

**HKEY \_ LOCAL \_ MACHINE \\ System \\ CurrentControlSet \\ Control \\ BackupRestore \\ FilesNotToSnapshot**

Questa chiave del Registro di sistema ha valori REG \_ MULTI \_ SZ per ogni applicazione i cui file possono essere esclusi. I file vengono specificati da percorsi completi, che possono contenere il \* carattere jolly.

In tutti i casi, la voce viene ignorata se non sono presenti file che corrispondono alla stringa di percorso.

Dopo essere stato aggiunto al valore della chiave del Registro di sistema appropriato, un file viene eliminato dalla copia shadow durante la creazione dal writer di ottimizzazione della copia shadow nel modo più appropriato.

Se non è possibile specificare un percorso completo, un percorso può essere implicito anche usando la variabile $UserProfile$ o $AllVolumes$. Esempio:

-   $UserProfile$ Directory \\ \\ Subdirectory \\ FileName.\*
-   $AllVolumes$ \\ TemporaryFiles \\ \* .\*

Per rendere ricorsivo il percorso, aggiungere " /s" alla fine. Esempio:

-   $UserProfile$ Directory \\ \\ Subdirectory \\ FileName. \* /s
-   $AllVolumes$ \\ TemporaryFiles \\ \* . \* /s

La $UserProfile$ fa sì che la stringa di percorso sia applicata a tutti i profili utente nel computer. I profili utente vengono enumerati esaminando la chiave del Registro di sistema seguente:

**HKEY \_ LOCAL MACHINE Software Microsoft Windows NT \_ \\ \\ \\ \\ CurrentVersion \\ ProfileList**

La $AllVolumes$ fa sì che la stringa di percorso sia applicata a tutte le copie shadow nel computer. Si supponga, ad esempio, che il percorso sia "$AllVolumes$ \\ TemporaryFiles \\ \* . \* /s" e il computer ha tre volumi: C:, D: ed E:. Se C: ed E: contengono il percorso " TemporaryFiles " e il volume D: contiene solo il percorso D: Data , l'albero di directory C: TemporaryFiles viene eliminato dalle copie shadow di C: e l'albero di \\ \\ directory \\ \\ \\ \\ E: TemporaryFiles viene \\ eliminato dalle \\ copie shadow di E:.

Gli amministratori possono disabilitare l'espansione della $UserProfile$ usando la chiave del Registro di sistema seguente:

**HKEY \_ LOCAL MACHINE System \_ \\ \\ CurrentControlSet \\ Services \\ Vss \\ Impostazioni**

In questa chiave del Registro di sistema specificare DisableUserProfileExpansion per il nome del valore, REG DWORD per il tipo di valore e un valore diverso da zero per i \_ dati del valore.

## <a name="about-the-filesnottobackup-registry-key"></a>Informazioni sulla chiave del Registro di sistema FilesNotToBackup

La chiave del Registro di sistema **FilesNotToBackup** può essere usata per specificare i nomi dei file e delle directory di cui le applicazioni di backup non devono eseguire il backup o il ripristino. Tuttavia, non esclude tali file dalle copie shadow. Per altre informazioni su questa chiave del Registro di sistema, vedere Chiavi e valori del Registro [di sistema per il backup e il ripristino.](../backup/registry-keys-for-backup-and-restore.md)

 

 
