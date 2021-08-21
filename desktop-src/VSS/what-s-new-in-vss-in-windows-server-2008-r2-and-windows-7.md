---
description: Windows Server 2008 R2 e Windows 7 introducono le modifiche seguenti al Servizio Copia Shadow del volume.
ms.assetid: 1287f175-29e4-40be-804b-d78542e76efc
title: 'Novità: VSS in Windows Server 2008 R2 & Windows 7'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8eeaaf42a82e13c5766ee3cfa6ba9fe73a36a783824497482ac97fc20d058a51
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118121527"
---
# <a name="whats-new-vss-in-windows-server-2008-r2--windows-7"></a>Novità: VSS in Windows Server 2008 R2 & Windows 7

Windows Server 2008 R2 e Windows 7 introducono le modifiche seguenti al Servizio Copia Shadow del volume.

## <a name="new-vss-interfaces"></a>Nuove interfacce vss

<dl>

[**IVssBackupComponentsEx3**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssbackupcomponentsex3)  
[**IVssComponentEx2**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponentex2)  
[**IVssCreateExpressWriterMetadata**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscreateexpresswritermetadata)  
[**IVssExpressWriter**](/windows/desktop/api/VsWriter/nl-vswriter-ivssexpresswriter)  
</dl>

## <a name="new-vss-classes"></a>Nuove classi VSS

<dl>

[**CVssWriterEx2**](/windows/desktop/api/VsWriter/nl-vswriter-cvsswriterex2)  
</dl>

## <a name="new-vss-enumerations"></a>Nuove enumerazioni vss

<dl>

[**OPZIONI DI RIPRISTINO DI VSS \_ \_**](/windows/desktop/api/Vss/ne-vss-vss_recovery_options)  
</dl>

## <a name="new-vss-functions"></a>Nuove funzioni vss

<dl>

[**CreateVssExpressWriter**](/windows/desktop/api/VsWriter/nf-vswriter-createvssexpresswriter)  
</dl>

## <a name="existing-vss-interface-modifications"></a>Modifiche dell'interfaccia VSS esistenti

<dl>

[**Interfaccia IVssHardwareSnapshotProviderEx**](/windows/desktop/api/VsProv/nn-vsprov-ivsshardwaresnapshotproviderex)<dl> Aggiunta del metodo: [ **ResyncLuns**](/windows/desktop/api/VsProv/nf-vsprov-ivsshardwaresnapshotproviderex-resyncluns)  
</dl> </dd> </dl>

## <a name="vss-event-tracing-and-logging"></a>Traccia e registrazione degli eventi di VSS

A partire da Windows Server 2008 R2 e Windows 7, è possibile usare lo strumento VssTrace, lo strumento Logman o lo strumento Tracelog per raccogliere informazioni di traccia per l'infrastruttura vsstrace. Per altre informazioni, vedere [Uso degli strumenti di traccia con VSS.](using-tracing-tools-with-vss.md)

## <a name="lun-resynchronization"></a>Risincronizzazione LUN

In Windows Server 2008 R2 e Windows 7 i richiedenti VSS possono usare una funzionalità del provider di copie shadow hardware denominata "risincronizzazione LUN". Si tratta di uno schema di ripristino rapido che consente a un amministratore dell'applicazione di ripristinare i dati da una copia shadow al numero di unità logica (LUN) originale o a un nuovo LUN. La copia shadow può essere un clone completo oppure una copia shadow differenziale. In entrambi i casi, al termine dell'operazione di risincronizzazione, il LUN di destinazione avrà lo stesso contenuto del LUN della copia shadow. Durante l'operazione di risincronizzazione, l'array esegue una copia a livello di blocco dalla copia shadow al LUN di destinazione. Per altre informazioni, vedere gli argomenti seguenti:

-   [Lun Resync : scenario di ripristino rapido in Server 2008 R2](https://blogs.technet.com/filecab/archive/2009/04/11/lun-resync-a-fast-recovery-scenario-in-server-2008-r2.aspx)
-   "Come vengono usate le copie shadow" in [Servizio Copia Shadow del volume](/windows-server/storage/file-server/volume-shadow-copy-service)
-   [Gotcha di risincronizzazione LUN comuni](https://blogs.msdn.com/gregd/archive/2009/07/27/common-lun-resync-gotchas.aspx)

## <a name="express-writers"></a>Autori di express writer

In Windows Server 2008 R2 e Windows 7, l'interfaccia rapida vss consente a un'applicazione di registrare il percorso dei file di dati senza implementare un VSS writer. Per altre informazioni, vedere [Servizio Copia Shadow del volume (VSS) Express Writers](https://blogs.technet.com/filecab/archive/2009/06/17/volume-shadow-copy-service-vss-express-writers.aspx).

## <a name="new-vss-writers"></a>Nuovi vss writer

Windows Server 2008 R2 e Windows 7 introducono i writer VSS seguenti:

-   Writer dei contatori delle prestazioni
-   Utilità di pianificazione Writer
-   Writer dell'archivio dei metadati vss

Questi nuovi writer sono documentati in [VsS Writer in -Box](in-box-vss-writers.md).

 

 
