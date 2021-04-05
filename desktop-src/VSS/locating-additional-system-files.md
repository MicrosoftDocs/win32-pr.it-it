---
description: Quando si esegue un backup o un ripristino VSS, lo stato del sistema Windows viene definito come una raccolta di diversi elementi chiave del sistema operativo e dei relativi file. Questi elementi devono essere sempre considerati come un'unità dalle operazioni di backup e ripristino.
ms.assetid: 48721358-8450-462f-8f99-23e207311041
title: Backup e ripristino dello stato del sistema
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ed61c3ccad51ebd8cd632fab292160c795741c9b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103755543"
---
# <a name="backing-up-and-restoring-system-state"></a>Backup e ripristino dello stato del sistema

> [!Note]  
> Questo argomento si applica a Windows Vista, Windows Server 2008 e versioni successive. Per informazioni su Windows Server 2003, vedere [backup e ripristino dello stato del sistema in Windows server 2003 R2 e Windows server 2003 SP1](backing-up-and-restoring-system-state-under-vss.md)

 

Quando si esegue un backup o un ripristino VSS, lo stato del sistema Windows viene definito come una raccolta di diversi elementi chiave del sistema operativo e dei relativi file. Questi elementi devono essere sempre considerati come un'unità dalle operazioni di backup e ripristino.

> [!Note]  
> Microsoft non fornisce supporto tecnico per sviluppatori o professionisti IT per l'implementazione di ripristini dello stato del sistema online in Windows (tutte le versioni).

 

Quando si esegue il backup e il ripristino dello stato del sistema, la strategia consigliata consiste nel eseguire il backup e il ripristino dei volumi di sistema e di avvio oltre ai file enumerati dai writer dello stato del sistema. I writer dello stato del sistema sono writer per i quali l'attributo del [**\_ \_ tipo di utilizzo VSS**](/windows/desktop/api/VsWriter/ne-vswriter-vss_usage_type) è impostato su VSS \_ ut \_ BOOTABLESYSTEMSTATE o VSS \_ ut \_ SYSTEMSERVICE.

> [!IMPORTANT]
> Se un writer VSS è identificato dal relativo [**\_ \_ tipo di utilizzo VSS**](/windows/desktop/api/VsWriter/ne-vswriter-vss_usage_type) come writer dello stato del sistema, deve essere incluso in un backup dello stato del sistema anche se è selezionabile.

 

Oltre al sistema operativo enumerato e ai file binari del driver enumerati dai writer dello stato del sistema, è necessario eseguire il backup di alcuni file come parte dello stato del sistema.

Tutti i componenti restituiti da un writer dello stato del sistema VSS fanno parte dello stato del sistema, ad eccezione di quelli per cui \_ \_ è impostato il flag VSS CF Not \_ System \_ state.

Anche i programmi di backup devono impostare la chiave del registro di sistema **LastRestoreId** . Per ulteriori informazioni, vedere [chiavi e valori del registro di sistema per il backup e il ripristino](../backup/registry-keys-for-backup-and-restore.md).

> [!Note]  
> In Windows Vista, Windows Server 2008 e versioni successive, i nomi e le posizioni di alcuni file di sistema sono stati modificati come indicato di seguito.

 

## <a name="system-state"></a>Stato del sistema

Per Windows Server 2012 e versioni successive, oltre ai file segnalati dai vari writer di stato del sistema VSS, è necessario includere in modo esplicito solo i file di licenza seguenti e i file DRM seguenti devono essere esclusi in modo esplicito.

## <a name="windows-media-digital-rights-management-files"></a>File di Rights Management digitali di Windows Media

In Windows Server 2008 e versioni successive, i file seguenti, incluse tutte le sottodirectory nel percorso seguente, sono esclusi dallo stato del sistema e non devono essere sottoposti a backup:

-   % ProgramData% \\ Microsoft \\ Windows \\ DRM\\

Questa operazione sostituisce le informazioni contenute nella sezione Windows Media Digital Rights Management di [utilizzo delle funzionalità di sicurezza e del file System](working-with-file-system-and-security-features.md).

## <a name="performance-counter-configuration-files"></a>File di configurazione dei contatori delle prestazioni

I file di configurazione del contatore delle prestazioni si trovano nella directory% SystemRoot% \\ system32 \\ e hanno i nomi seguenti:

<dl> Prestazioni? 00?. dat  
??. Perfc0 dat  
??. Perfd0 dat  
??. Perfh0 dat  
??. Perfi0 dat  
???. Prfc0 dat  
???. Prfd0 dat  
???. Prfh0 dat  
???. Prfi0 dat  
</dl>

Questi file vengono modificati solo durante l'installazione dell'applicazione ed è necessario eseguirne il backup e il ripristino durante i backup e i ripristini dello stato del sistema.

## <a name="iis-configuration-files"></a>File di configurazione di IIS

> [!Note]  
> In Windows Vista con Service Pack 1 (SP1) e versioni successive, non è consigliabile eseguire il backup di questi file. Usare invece il writer di configurazione di IIS in-box. Per ulteriori informazioni su questo writer, vedere la pagina relativa ai [writer VSS](in-box-vss-writers.md).

 

Di seguito sono elencati i file di configurazione IIS pertinenti e i relativi percorsi:

-   Il file di machine.config .NET FX si trova nella directory della versione del Framework.
-   Il file di web.config radice ASP.NET si trova nella directory della versione del Framework.
    > [!Note]  
    > I file di configurazione per .NET FX e ASP.NET si trovano nella directory della versione del Framework. Se nel computer sono installate più versioni del Framework, questa directory conterrà un file di configurazione per ogni versione installata.

     

-   Il file di configurazione centrale di IIS applicationHost.config si trova nella directory% windir% \\ system32 \\ inetsrv \\ config. Poiché il server è in grado di comprendere questo file di configurazione, sono presenti file di schema che ne determinano la grammatica e la struttura. Questi file si trovano nella directory% windir% \\ system32 \\ inetsrv \\ config \\ schema.

Il percorso della directory della versione del Framework è archiviato nella chiave del registro di sistema seguente:

**HKEY \_ \_ computer locale \\ software \\ Microsoft \\ . \\InstallRoot NETFramework**

Inoltre, è necessario eseguire il backup delle chiavi di crittografia seguenti:<dl> % ProgramData% \\ Microsoft \\ Crypto \\ RSA \\ MachineKeys\\\*  
% SystemRoot% \\ system32 \\ Microsoft \\ Protect\\\*  
</dl>

## <a name="framework-files"></a>File di Framework

È necessario eseguire il backup di tutte le versioni di .NET Framework. I file si trovano in una o in entrambe le directory seguenti:

<dl> % WINDIR% \\ Microsoft.NET \\ Framework  
% WINDIR% \\ Microsoft.NET \\ Framework64  
</dl>

Inoltre, è necessario eseguire il backup dei file di assembly. Questi file sono disponibili nella directory seguente:<dl> assembly% windir% \\  
</dl>

## <a name="task-scheduler-task-files"></a>File Utilità di pianificazione attività

È necessario eseguire il backup dei file delle attività dell'utilità di pianificazione. I file si trovano in una o in entrambe le posizioni seguenti:

<dl> % WINDIR% \\ system32 \\ attività e qualsiasi sottodirectory (in modo ricorsivo)  
% WINDIR% \\ attività (nessuna sottodirectory)  
</dl>

 

 
