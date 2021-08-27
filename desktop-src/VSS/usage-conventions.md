---
description: Quando si sviluppa un'applicazione VSS, è necessario osservare le linee guida e le restrizioni seguenti.
ms.assetid: d4edc16c-f768-4095-9b2a-b706f19f9e61
title: Compatibilità delle applicazioni VSS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8ca1f6f3013856087e70247aed21d8f35aa4cf09
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2021
ms.locfileid: "122483017"
---
# <a name="vss-application-compatibility"></a>Compatibilità delle applicazioni VSS

Quando si sviluppa un'applicazione VSS, è necessario osservare le linee guida e le restrizioni seguenti. Può essere utile fare riferimento al codice di esempio per i richiedenti, i provider e i writer vss forniti in Microsoft Windows Software Development Kit (SDK).

> [!Note]  
> L Windows SDK può essere usato per sviluppare applicazioni VSS solo per Windows Vista e versioni successive Windows del sistema operativo. Non può essere usato per sviluppare richiedenti, provider o writer VSS per Windows Server 2003 R2, Windows Server 2003 o Windows XP.

 

**Windows Server 2003 R2, Windows Server 2003 e Windows XP:** VSS è disponibile in Servizio Copia Shadow del volume 7.2 SDK, che è possibile scaricare da [https://www.microsoft.com/download/details.aspx?id=23490](https://www.microsoft.com/download/details.aspx?id=23490) . Si noti che i file vssapi.lib a 64 bit nelle directory nella directory Obj win2003 possono essere usati per le versioni \\ a 64 bit di Windows Server 2003 R2, Windows Server 2003 e Windows XP. Questo SDK fornisce anche codice di esempio per i richiedenti, i provider e i writer vss.

## <a name="compiling-vss-applications"></a>Compilazione di applicazioni VSS

Quando si sviluppa un richiedente, ad esempio un'applicazione di backup:

-   Includere le intestazioni seguenti: <dl> Vss.h  
    VsWriter.h  
    VsBackup.h  
    </dl>
-   Link the following library: <dl> VssApi.Lib  
    </dl>

Quando si sviluppa un writer:

-   Includere le intestazioni seguenti: <dl> Vss.h  
    VsWriter.h  
    </dl>
-   Link the following library: <dl> VssApi.lib  
    </dl>

## <a name="supported-configurations-and-restrictions"></a>Configurazioni e restrizioni supportate

L'elenco seguente descrive le configurazioni e le restrizioni supportate:

-   VSS è disponibile e supportato nelle versioni del Windows operativo a partire da Windows XP.
-   La tabella seguente riepiloga le informazioni di compatibilità Windows versioni. Si noti che se un'applicazione VSS viene "compilata per" una versione Windows specificata, significa che l'applicazione è stata compilata usando i file di intestazione e le librerie specifici di tale versione.

    > [!Note]  
    > I provider di hardware verranno eseguiti solo Windows versioni del sistema operativo server. Non verranno eseguiti in Windows del sistema operativo client.

     

    > [!Note]  
    > Nelle tabelle seguenti Windows Server 2008 con Service Pack 2 (SP2) deve essere considerato uguale a Windows Server 2008. Per altre informazioni su Windows Server 2008 con SP2, vedere <https://go.microsoft.com/fwlink/p/?linkid=178730> . Windows Server 2003 R2 deve essere considerato uguale a Windows Server 2003.

     

    > [!Note]  
    > Se un'applicazione VSS viene compilata per Windows Server 2003 o versione successiva, verrà eseguita anche nelle versioni successive di Windows.

     

    

    
| Richiedenti, writer e provider VSS compilati per | Verrà eseguito il | 
|-----------------------------------------------------|-------------|
| Windows Server 2008 R2 (64 bit), Windows 7 (64 bit), Windows Server 2008 (64 bit) e Windows Vista (64 bit) | Windows Server 2008 R2 (64 bit), Windows 7 (64 bit), Windows Server 2008 (64 bit) e Windows Vista (64 bit) | 
| Windows Server 2008 R2 (32 bit), Windows 7 (32 bit), Windows Server 2008 (32 bit) e Windows Vista (32 bit) | Windows Server 2008 R2 (32 bit), Windows 7 (32 bit), Windows Server 2008 (32 bit) e Windows Vista (32 bit) | 
| Windows Server 2003 (64 bit) | Windows Server 2008 R2 (64 bit), Windows 7 (64 bit), Windows Server 2008 (64 bit), Windows Vista (64 bit) e Windows Server 2003 (64 bit) | 
| Windows Server 2003 (32 bit) | Windows Server 2008 R2 (32 bit), Windows 7 (32 bit), Windows Server 2008 (32 bit), Windows Vista (32 bit) e Windows Server 2003 (32 bit)    <blockquote>    [!Note]<br />    I richiedenti verranno eseguiti anche Windows Server 2003 (64 bit).    </blockquote><br /> | 
| Windows XP 64-Bit Edition | Windows Server 2003 (64 bit) e Windows XP 64-Bit Edition | 
| Windows XP (32 bit) | Windows XP (32 bit) | 


    

     

    

    | Per compilare un richiedente, un writer o un provider VSS per        | Uso                                                                                                                                       |
    |------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------|
    | Windows Server 2008 R2 o Windows 7                        | Windows SDK per Windows 7 (disponibile [nell'area Windows download).](https://www.microsoft.com/download/details.aspx?id=8279)                |
    | Windows Server 2008 o Windows Vista                       | Windows SDK per Windows Server 2008 (disponibile in [Windows SDK Developer Center.](https://msdn.microsoft.com/windows/bb980924.aspx) |
    | Windows Server 2003 R2, Windows Server 2003 o Windows XP | [Servizio Copia Shadow del volume 7.2 SDK](https://www.microsoft.com/download/details.aspx?id=23490)                                                      |

    

     

-   Tutte le applicazioni VSS a 32 bit (richiedenti, provider e writer) devono essere eseguite come applicazioni native a 32 bit o a 64 bit. L'esecuzione in WOW64 non è supportata.

    **Windows Server 2003 e Windows XP:** L'esecuzione di richiedenti VSS a 32 bit in WOW64 è supportata, ma non per i backup dello stato del sistema. L'esecuzione di provider e writer VSS a 32 bit in WOW64 non è supportata. Il supporto per l'esecuzione di richiedenti a 32 bit in WOW64 è stato rimosso in Windows Vista e versioni successive.

-   Una copia shadow creata in Windows Server 2003 R2 o Windows Server 2003 non può essere usata in un computer che esegue Windows Server 2008 R2 o Windows Server 2008. Una copia shadow creata in Windows Server 2008 R2 o Windows Server 2008 non può essere usata in un computer che esegue Windows Server 2003. Tuttavia, una copia shadow creata in Windows Server 2008 può essere usata in un computer che esegue Windows Server 2008 R2 e viceversa.
-   Per supportare le copie shadow, un sistema che esegue VSS deve avere almeno un file system NTFS file system. Questa file system ospiterà l'"area diff" della copia shadow. Per altre informazioni, vedere [Provider di sistema](providers.md).
-   Data la presenza di un'file system NTFS e la scelta appropriata del contesto (vedere Configurazioni del contesto della copia [shadow),](shadow-copy-context-configurations.md)qualsiasi file system locale supportato può essere copiato tramite shadow.
-   È possibile creare copie shadow solo per file system montati in locale. Le condivisioni remote e altri file system cross-mounted non possono essere copiati tramite shadow dal sistema che le monta. Questi file system possono essere copiati solo dai sistemi che servono i file system.
-   I writer e i richiedenti devono specificare solo le risorse locali. Le risorse locali sono set di file il cui percorso assoluto inizia con una lettera di unità e la lettera di unità non può essere associata a una cartella montata in una condivisione remota.
-   Il numero massimo è di copie shadow software per ogni volume è 512. Tuttavia, per impostazione predefinita, puoi gestire solo 64 copie shadow usate dalla funzionalità Copie shadow di cartelle condivise. Per modificare il limite per la funzionalità Copie shadow di cartelle condivise, usare la chiave del Registro di sistema [MaxShadowCopies.](../backup/registry-keys-for-backup-and-restore.md)
-   L'infrastruttura dei componenti di backup non supporta il backup delle risorse del cluster come componenti writer. Per eseguire il backup delle risorse del cluster, le applicazioni devono presupporre che il percorso sia locale a un nodo del cluster specifico.
-   [!Note]  
    > Microsoft non fornisce supporto tecnico per sviluppatori o professionisti IT per l'implementazione di ripristini dello stato del sistema online Windows (tutte le versioni).

     

    Quando si esegue il backup e il ripristino dello stato del sistema, la strategia consigliata consiste nel eseguire il backup e il ripristino dei volumi di sistema e di avvio oltre ai file enumerati dai writer dello stato del sistema.

    > [!Note]  
    > I writer di stato del sistema sono writer con l'attributo [**VSS \_ USAGE \_ TYPE**](/windows/win32/api/VsWriter/ne-vswriter-vss_usage_type) impostato su VSS \_ UT \_ BOOTABLESYSTEMSTATE o VSS \_ UT \_ SYSTEMSERVICE.

     

 

 
