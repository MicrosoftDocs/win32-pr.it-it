---
description: Quando si esegue un backup o un ripristino vss, lo stato Windows sistema viene definito come una raccolta di diversi elementi chiave del sistema operativo e dei relativi file. Questi elementi devono essere sempre considerati come un'unità dalle operazioni di backup e ripristino.
ms.assetid: 48721358-8450-462f-8f99-23e207311041
title: Backup e ripristino dello stato del sistema
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e3b027fa0d1a01f3d4f735494d34d4f2da2d07a0e0d82ecfd189f7a9c7c8537c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119056399"
---
# <a name="backing-up-and-restoring-system-state"></a>Backup e ripristino dello stato del sistema

> [!Note]  
> Questo argomento si applica Windows Vista, Windows Server 2008 e versioni successive. Per informazioni su Windows Server 2003, vedere Backup e ripristino dello stato del sistema [in Windows Server 2003 R2 e Windows Server 2003 SP1](backing-up-and-restoring-system-state-under-vss.md)

 

Quando si esegue un backup o un ripristino vss, lo stato Windows sistema viene definito come una raccolta di diversi elementi chiave del sistema operativo e dei relativi file. Questi elementi devono essere sempre considerati come un'unità dalle operazioni di backup e ripristino.

> [!Note]  
> Microsoft non offre supporto tecnico per sviluppatori o professionisti IT per l'implementazione di ripristini dello stato del sistema online Windows (tutte le versioni).

 

Quando si esegue il backup e il ripristino dello stato del sistema, la strategia consigliata consiste nel eseguire il backup e il ripristino dei volumi di sistema e di avvio oltre ai file enumerati dai writer dello stato del sistema. I writer dello stato del sistema sono writer con l'attributo [**VSS \_ USAGE \_ TYPE**](/windows/desktop/api/VsWriter/ne-vswriter-vss_usage_type) impostato su VSS \_ UT \_ BOOTABLESYSTEMSTATE o VSS \_ UT \_ SYSTEMSERVICE.

> [!IMPORTANT]
> Se un VSS Writer viene identificato dal relativo TIPO DI UTILIZZO [**VSS \_ \_**](/windows/desktop/api/VsWriter/ne-vswriter-vss_usage_type) come writer dello stato del sistema, deve essere incluso in un backup dello stato del sistema anche se è selezionabile.

 

Oltre ai file binari enumerati del sistema operativo e del driver enumerati dai writer dello stato del sistema, è necessario eseguire il backup di alcuni altri file come parte dello stato del sistema.

Tutti i componenti segnalati da un writer di stato del sistema VSS fanno parte dello stato del sistema, ad eccezione di quelli per cui è impostato il flag VSS \_ CF \_ NOT SYSTEM \_ \_ STATE.

I programmi di backup devono anche impostare la chiave del Registro di sistema **LastRestoreId.** Per altre informazioni, vedere Chiavi e [valori del Registro di sistema per il backup e il ripristino.](../backup/registry-keys-for-backup-and-restore.md)

> [!Note]  
> In Windows Vista, Windows Server 2008 e versioni successive, i nomi e i percorsi di alcuni file di sistema sono stati modificati come indicato di seguito.

 

## <a name="system-state"></a>Stato del sistema

Per Windows Server 2012 e versioni successive, oltre ai file segnalati dai vari writer dello stato del sistema vss, è necessario includere in modo esplicito solo i file di licenza seguenti e i file DRM seguenti devono essere esclusi in modo esplicito.

## <a name="windows-media-digital-rights-management-files"></a>Windows File di Rights Management multimediali

In Windows Server 2008 e versioni successive, i file seguenti, incluse tutte le sottodirectory nel percorso seguente, vengono esclusi dallo stato del sistema e non devono essere sottoposti a backup:

-   %ProgramData% \\ Microsoft \\ Windows \\ DRM\\

In questo modo vengono sostituite le informazioni nella sezione Windows Media Digital Rights Management di Working with File System and Security Features ( Uso del file system e [delle funzionalità di sicurezza).](working-with-file-system-and-security-features.md)

## <a name="performance-counter-configuration-files"></a>File di configurazione dei contatori delle prestazioni

I file di configurazione dei contatori delle prestazioni si trovano nella directory %SystemRoot% \\ System32 \\ e hanno i nomi seguenti:

<dl> Perf?00?. Dat  
Perfc0??. Dat  
Perfd0??. Dat  
Perfh0??. Dat  
Perfi0??. Dat  
Prfc0???. Dat  
Prfd0???. Dat  
Prfh0???. Dat  
Prfi0???. Dat  
</dl>

Questi file vengono modificati solo durante l'installazione dell'applicazione e devono essere sottoposti a backup e ripristino durante i backup e i ripristini dello stato del sistema.

## <a name="iis-configuration-files"></a>File di configurazione iis

> [!Note]  
> In Windows Vista con Service Pack 1 (SP1) e versioni successive, non è consigliabile eseguire il backup di questi file. Usare invece il writer di configurazione IIS in uso. Per altre informazioni su questo writer, vedere [VsS Writer in-box.](in-box-vss-writers.md)

 

I file di configurazione IIS pertinenti e i relativi percorsi sono elencati di seguito:

-   Il file di machine.config FX .NET si trova nella directory della versione del framework.
-   Il ASP.NET radice web.config si trova nella directory della versione del framework.
    > [!Note]  
    > I file di configurazione per .NET FX e ASP.NET nella directory della versione del framework. Se nel computer sono installate più versioni del framework, questa directory conterrà un file di configurazione per ogni versione installata.

     

-   Il file applicationHost.config configurazione centrale di IIS si trova nella directory %windir% \\ system32 \\ inetsrv \\ config. Perché il server comprendi questo file di configurazione, sono disponibili file di schema che ne determinano la grammatica e la struttura. Questi file si trovano nella directory %windir% \\ system32 \\ inetsrv \\ config \\ schema.

Il percorso della directory della versione del framework è archiviato nella chiave del Registro di sistema seguente:

**HKEY \_ LOCAL MACHINE SOFTWARE Microsoft \_ \\ \\ \\ . NETFramework \\ InstallRoot**

È inoltre necessario eseguire il backup delle chiavi di crittografia seguenti:<dl> %ProgramData% \\ Microsoft Crypto RSA \\ \\ \\ MachineKeys\\\*  
%SystemRoot% \\ System32 \\ Microsoft \\ Protect\\\*  
</dl>

## <a name="framework-files"></a>File di framework

È necessario eseguire il backup di tutte le versioni di .NET Framework. I file si trovano in una o entrambe le directory seguenti:

<dl> %windir% \\ Microsoft.Net \\ Framework  
%windir% \\ Microsoft.Net \\ Framework64  
</dl>

Inoltre, è necessario eseguire il backup dei file di assembly. Questi file sono disponibili nella directory seguente:<dl> Assembly %windir% \\  
</dl>

## <a name="task-scheduler-task-files"></a>Utilità di pianificazione file dell'attività

È necessario eseguire il backup dei file delle attività dell'utilità di pianificazione. I file si trovano in uno o entrambi i percorsi seguenti:

<dl> %windir% \\ system32 \\ tasks and any subdirectories (recursively) (%windir% system32 tasks and any subdirectories (recursively) (%windir% system32 tasks and any subdirectories (recursively)  
%windir% \\ tasks (nessuna sottodirectory)  
</dl>

 

 
