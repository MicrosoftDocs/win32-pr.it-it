---
description: Quando si sviluppa un'applicazione VSS personalizzata, è necessario osservare le linee guida e le restrizioni seguenti.
ms.assetid: d4edc16c-f768-4095-9b2a-b706f19f9e61
title: Compatibilità delle applicazioni VSS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5b9cc19b6a6d88365a67569bc4729855077c9da9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104343581"
---
# <a name="vss-application-compatibility"></a>Compatibilità delle applicazioni VSS

Quando si sviluppa un'applicazione VSS personalizzata, è necessario osservare le linee guida e le restrizioni seguenti. Può essere utile fare riferimento al codice di esempio per i richiedenti VSS, i provider e i writer forniti in Microsoft Windows Software Development Kit (SDK).

> [!Note]  
> Il Windows SDK può essere utilizzato per sviluppare applicazioni VSS solo per Windows Vista e versioni successive del sistema operativo Windows. Non può essere utilizzato per sviluppare richiedenti VSS, provider o writer per Windows Server 2003 R2, Windows Server 2003 o Windows XP.

 

**Windows server 2003 R2, Windows server 2003 e Windows XP:** VSS è disponibile nel Servizio Copia Shadow del volume 7,2 SDK, che è possibile scaricare da [https://www.microsoft.com/download/details.aspx?id=23490](https://www.microsoft.com/download/details.aspx?id=23490) . Si noti che i file vssapi. lib a 64 bit nelle directory sotto la \\ directory Win2003 obj possono essere usati per le versioni a 64 bit di Windows server 2003 R2, Windows server 2003 e Windows XP. Questo SDK fornisce anche codice di esempio per i richiedenti VSS, i provider e i writer.

## <a name="compiling-vss-applications"></a>Compilazione di applicazioni VSS

Quando si sviluppa un richiedente, ad esempio un'applicazione di backup:

-   Includere le intestazioni seguenti: <dl> VSS. h  
    VsWriter. h  
    VsBackup. h  
    </dl>
-   Link the following library: <dl> VssApi. lib  
    </dl>

Quando si sviluppa un writer:

-   Includere le intestazioni seguenti: <dl> VSS. h  
    VsWriter. h  
    </dl>
-   Link the following library: <dl> VssApi. lib  
    </dl>

## <a name="supported-configurations-and-restrictions"></a>Configurazioni e restrizioni supportate

Nell'elenco seguente vengono descritte le configurazioni e le restrizioni supportate:

-   VSS viene fornito e supportato nelle versioni del sistema operativo Windows a partire da Windows XP.
-   Nella tabella seguente sono riepilogate le informazioni sulla compatibilità tra le versioni di Windows. Si noti che se un'applicazione VSS viene "compilata per" una versione di Windows specificata, significa che l'applicazione è stata compilata utilizzando i file di intestazione e le librerie specifiche di tale versione.

    > [!Note]  
    > I provider hardware vengono eseguiti solo nelle versioni del sistema operativo Windows Server. Non verranno eseguite nelle versioni del sistema operativo client Windows.

     

    > [!Note]  
    > Nelle tabelle seguenti, Windows Server 2008 con Service Pack 2 (SP2) deve essere considerato uguale a quello di Windows Server 2008. Per ulteriori informazioni su Windows Server 2008 con SP2, vedere <https://go.microsoft.com/fwlink/p/?linkid=178730> . Windows Server 2003 R2 deve essere considerato uguale a quello di Windows Server 2003.

     

    > [!Note]  
    > Se un'applicazione VSS viene compilata per Windows Server 2003 o versione successiva, verrà eseguita anche nelle versioni successive di Windows.

     

    

    <table>
    <colgroup>
    <col style="width: 50%" />
    <col style="width: 50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th>Richiedenti VSS, writer e provider compilati per</th>
    <th>Viene eseguito in</th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td>Windows Server 2008 R2 (64 bit), Windows 7 (64 bit), Windows Server 2008 (64 bit) e Windows Vista (64 bit)</td>
    <td>Windows Server 2008 R2 (64 bit), Windows 7 (64 bit), Windows Server 2008 (64 bit) e Windows Vista (64 bit)</td>
    </tr>
    <tr class="even">
    <td>Windows Server 2008 R2 (32 bit), Windows 7 (32 bit), Windows Server 2008 (32 bit) e Windows Vista (32 bit)</td>
    <td>Windows Server 2008 R2 (32 bit), Windows 7 (32 bit), Windows Server 2008 (32 bit) e Windows Vista (32 bit)</td>
    </tr>
    <tr class="odd">
    <td>Windows Server 2003 (64 bit)</td>
    <td>Windows Server 2008 R2 (64 bit), Windows 7 (64 bit), Windows Server 2008 (64 bit), Windows Vista (64 bit) e Windows Server 2003 (64 bit)</td>
    </tr>
    <tr class="even">
    <td>Windows Server 2003 (32 bit)</td>
    <td>Windows Server 2008 R2 (32 bit), Windows 7 (32 bit), Windows Server 2008 (32 bit), Windows Vista (32 bit) e Windows Server 2003 (32 bit) <blockquote>
    [!Note]<br />
I richiedenti vengono eseguiti anche in Windows Server 2003 (64 bit).
    </blockquote>
    <br/></td>
    </tr>
    <tr class="odd">
    <td>Windows XP 64-bit Edition</td>
    <td>Windows Server 2003 (64-bit) e Windows XP 64-bit Edition</td>
    </tr>
    <tr class="even">
    <td>Windows XP (32 bit)</td>
    <td>Windows XP (32 bit)</td>
    </tr>
    </tbody>
    </table>

    

     

    

    | Per compilare un richiedente VSS, un writer o un provider per        | Uso                                                                                                                                       |
    |------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------|
    | Windows Server 2008 R2 o Windows 7                        | Windows SDK per Windows 7, disponibile nell' [area download di Windows](https://www.microsoft.com/download/details.aspx?id=8279).                |
    | Windows Server 2008 o Windows Vista                       | Windows SDK per Windows Server 2008 (disponibile da [Windows SDK Developer Center](https://msdn.microsoft.com/windows/bb980924.aspx)). |
    | Windows Server 2003 R2, Windows Server 2003 o Windows XP | [SDK Servizio Copia Shadow del volume 7,2](https://www.microsoft.com/download/details.aspx?id=23490)                                                      |

    

     

-   Tutte le applicazioni VSS a 32 bit, ovvero i richiedenti, i provider e i writer, devono essere eseguite come applicazioni native a 32 bit o 64 bit. L'esecuzione in WOW64 non è supportata.

    **Windows Server 2003 e Windows XP:** L'esecuzione di richiedenti VSS a 32 bit in WOW64 è supportata, ma non per i backup dello stato del sistema. L'esecuzione di provider e writer VSS a 32 bit in WOW64 non è supportata. Il supporto per l'esecuzione di richiedenti a 32 bit in WOW64 è stato rimosso in Windows Vista e nelle versioni successive.

-   Non è possibile usare una copia shadow creata in Windows Server 2003 R2 o Windows Server 2003 in un computer che esegue Windows Server 2008 R2 o Windows Server 2008. Non è possibile usare una copia shadow creata in Windows Server 2008 R2 o Windows Server 2008 in un computer che esegue Windows Server 2003. Tuttavia, una copia shadow creata in Windows Server 2008 può essere usata in un computer che esegue Windows Server 2008 R2 e viceversa.
-   Per supportare le copie shadow, un sistema che esegue VSS deve avere almeno un file system NTFS. In questo file system verrà ospitata l'"area diff" della copia shadow. Per ulteriori informazioni, vedere [provider di sistema](providers.md).
-   Data la presenza di un file system NTFS e data la scelta appropriata del contesto (vedere [configurazioni del contesto di copia shadow](shadow-copy-context-configurations.md)), qualsiasi file system locale supportato può essere replicata.
-   È possibile creare copie shadow solo per i file system montati localmente. Le condivisioni remote e altri file System Cross-mounted non possono essere replicati dal sistema che li monta. Questi file System possono essere replicati solo dai sistemi che gestiscono i file System.
-   I writer e i richiedenti devono specificare solo le risorse locali. Le risorse locali sono set di file il cui percorso assoluto inizia con una lettera di unità e la lettera di unità non può essere associata a una cartella montata in una condivisione remota.
-   Il numero massimo di copie shadow software per ogni volume è 512. Tuttavia, per impostazione predefinita, puoi gestire solo 64 copie shadow usate dalla funzionalità Copie shadow di cartelle condivise. Per modificare il limite per le copie shadow della funzionalità cartelle condivise, usare la chiave del registro di sistema [MaxShadowCopies](../backup/registry-keys-for-backup-and-restore.md) .
-   L'infrastruttura dei componenti di backup non supporta il backup delle risorse cluster come componenti del writer. Per eseguire il backup delle risorse cluster, le applicazioni devono presupporre che il percorso sia locale a un determinato nodo del cluster.
-   [!Note]  
    > Microsoft non fornisce supporto tecnico per sviluppatori o professionisti IT per l'implementazione di ripristini dello stato del sistema online in Windows (tutte le versioni).

     

    Quando si esegue il backup e il ripristino dello stato del sistema, la strategia consigliata consiste nel eseguire il backup e il ripristino dei volumi di sistema e di avvio oltre ai file enumerati dai writer dello stato del sistema.

    > [!Note]  
    > I writer dello stato del sistema sono writer per i quali l'attributo del [**\_ \_ tipo di utilizzo VSS**](/windows/win32/api/VsWriter/ne-vswriter-vss_usage_type) è impostato su VSS \_ ut \_ BOOTABLESYSTEMSTATE o VSS \_ ut \_ SYSTEMSERVICE.

     

 

 
