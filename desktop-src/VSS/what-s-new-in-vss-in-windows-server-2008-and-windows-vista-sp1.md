---
description: Windows Server 2008.
ms.assetid: 2f7b62f8-ba1e-42d2-8872-38d4475e4a2a
title: Novità di VSS in Windows Server 2008 e Windows Vista SP1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 83ee109eec31c084dc43fb9e0cc6341f443a16e6aa06ac989a7f328d9bb3011f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120006121"
---
# <a name="whats-new-in-vss-in-windows-server-2008-and-windows-vista-sp1"></a>Novità di VSS in Windows Server 2008 e Windows Vista SP1

Windows Server 2008 e Windows Vista con Service Pack 1 (SP1) introducono le modifiche seguenti al Servizio Copia Shadow del volume.

> [!Note]  
> Tutte le modifiche per Windows Vista si applicano Windows Server 2008 e Windows Vista con SP1. Per informazioni dettagliate su queste modifiche, vedere [Novità di VSS in Windows Vista.](what-s-new-in-vss-in-windows-vista.md)

 

-   [Nuove interfacce vss](#new-vss-interfaces)
-   [Nuove enumerazioni vss](#new-vss-enumerations)
-   [Nuove strutture vss](#new-vss-structures)
-   [Modifiche dell'enumerazione VSS esistenti](#existing-vss-enumeration-modifications)
-   [Modifiche dell'interfaccia VSS esistenti](#existing-vss-interface-modifications)
-   [Nuovi vss writer](#new-vss-writers)

## <a name="new-vss-interfaces"></a>Nuove interfacce vss

<dl>

[**IVssDifferentialSoftwareSnapshotMgmt3**](/windows/desktop/api/VsMgmt/nn-vsmgmt-ivssdifferentialsoftwaresnapshotmgmt3)  
[**IVssHardwareSnapshotProviderEx**](/windows/desktop/api/VsProv/nn-vsprov-ivsshardwaresnapshotproviderex)  
</dl>

## <a name="new-vss-enumerations"></a>Nuove enumerazioni vss

<dl>

[**\_OPZIONI HARDWARE DI VSS \_ \_**](/windows/desktop/api/Vss/ne-vss-vss_hardware_options)  
[**ERRORE DI \_ PROTEZIONE VSS \_**](/windows/desktop/api/VsMgmt/ne-vsmgmt-vss_protection_fault)  
[**LIVELLO DI \_ PROTEZIONE VSS \_**](/windows/desktop/api/VsMgmt/ne-vsmgmt-vss_protection_level)  
</dl>

## <a name="new-vss-structures"></a>Nuove strutture VSS

<dl>

[**INFORMAZIONI SULLA PROTEZIONE \_ DEI VOLUMI \_ DI VSS \_**](/windows/desktop/api/VsMgmt/ns-vsmgmt-vss_volume_protection_info)  
</dl>

## <a name="existing-vss-enumeration-modifications"></a>Modifiche dell'enumerazione VSS esistenti

<dl> <dt>

<span id="VSS_BACKUP_SCHEMA_enumeration"></span><span id="vss_backup_schema_enumeration"></span><span id="VSS_BACKUP_SCHEMA_ENUMERATION"></span>[**VSS \_ Enumerazione \_ BACKUP SCHEMA**](/windows/desktop/api/Vss/ne-vss-vss_backup_schema)
</dt> <dd>

<dl> <dt>

<span id="Added_value_"></span><span id="added_value_"></span><span id="ADDED_VALUE_"></span>Valore aggiunto:
</dt> <dd>

VSS \_ BS \_ WRITER SUPPORTA \_ \_ RIPRISTINI \_ PARALLELI

</dd> </dl> </dd> </dl>

<dl> <dt>

<span id="_VSS_VOLUME_SNAPSHOT_ATTRIBUTES_enumeration"></span><span id="_vss_volume_snapshot_attributes_enumeration"></span><span id="_VSS_VOLUME_SNAPSHOT_ATTRIBUTES_ENUMERATION"></span>[**\_ Enumerazione VSS \_ VOLUME SNAPSHOT \_ \_ ATTRIBUTES**](/windows/desktop/api/Vss/ne-vss-vss_volume_snapshot_attributes)
</dt> <dd>

<dl> <dt>

<span id="Added_values_"></span><span id="added_values_"></span><span id="ADDED_VALUES_"></span>Valori aggiunti:
</dt> <dd>

VSS \_ VOLSNAP \_ ATTR \_ DELAYED \_ POSTSNAPSHOT

RIPRISTINO DI VSS \_ VOLSNAP \_ ATTR \_ TXF \_

</dd> </dl> </dd> </dl>

## <a name="existing-vss-interface-modifications"></a>Modifiche dell'interfaccia VSS esistenti

<dl> <dt>

<span id="IVssBackupComponentsEx2_interface"></span><span id="ivssbackupcomponentsex2_interface"></span><span id="IVSSBACKUPCOMPONENTSEX2_INTERFACE"></span>[**Interfaccia IVssBackupComponentsEx2**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssbackupcomponentsex2)
</dt> <dd>

<dl> <dt>

<span id="Added_method_"></span><span id="added_method_"></span><span id="ADDED_METHOD_"></span>Aggiunta del metodo:
</dt> <dd>

[**BreakSnapshotSetEx**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponentsex2-breaksnapshotsetex)

</dd> </dl> </dd> </dl>

## <a name="new-vss-writers"></a>Nuovi vss writer

Windows Server 2008 e Windows Vista con SP1 introducono i writer VSS seguenti:

-   Writer di configurazione IIS
-   IIS Metabase Writer
-   Vss Writer di Server dei criteri di rete
-   vss writer del gateway di Servizi Desktop remoto (Servizi terminal)
-   Servizi Desktop remoto (Servizi terminal) Licensing VSS Writer

Questi writer sono documentati in [VSS Writer in -Box](in-box-vss-writers.md).

 

 



