---
description: Windows Server 2008.
ms.assetid: 2f7b62f8-ba1e-42d2-8872-38d4475e4a2a
title: Novità di VSS in Windows Server 2008 e Windows Vista SP1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2f053e327a7a54a9597bc06836b37c00effc62f9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104129278"
---
# <a name="whats-new-in-vss-in-windows-server-2008-and-windows-vista-sp1"></a>Novità di VSS in Windows Server 2008 e Windows Vista SP1

Windows Server 2008 e Windows Vista con Service Pack 1 (SP1) introducono le seguenti modifiche al Servizio Copia Shadow del volume.

> [!Note]  
> Tutte le modifiche per Windows Vista si applicano a Windows Server 2008 e Windows Vista con SP1. Per informazioni dettagliate su tali modifiche, vedere Novità di [VSS in Windows Vista](what-s-new-in-vss-in-windows-vista.md).

 

-   [Nuove interfacce VSS](#new-vss-interfaces)
-   [Nuove enumerazioni VSS](#new-vss-enumerations)
-   [Nuove strutture VSS](#new-vss-structures)
-   [Modifiche dell'enumerazione VSS esistenti](#existing-vss-enumeration-modifications)
-   [Modifiche all'interfaccia VSS esistente](#existing-vss-interface-modifications)
-   [Nuovi writer VSS](#new-vss-writers)

## <a name="new-vss-interfaces"></a>Nuove interfacce VSS

<dl>

[**IVssDifferentialSoftwareSnapshotMgmt3**](/windows/desktop/api/VsMgmt/nn-vsmgmt-ivssdifferentialsoftwaresnapshotmgmt3)  
[**IVssHardwareSnapshotProviderEx**](/windows/desktop/api/VsProv/nn-vsprov-ivsshardwaresnapshotproviderex)  
</dl>

## <a name="new-vss-enumerations"></a>Nuove enumerazioni VSS

<dl>

[**\_\_Opzioni hardware \_ VSS**](/windows/desktop/api/Vss/ne-vss-vss_hardware_options)  
[**\_errore di protezione VSS \_**](/windows/desktop/api/VsMgmt/ne-vsmgmt-vss_protection_fault)  
[**\_livello di protezione VSS \_**](/windows/desktop/api/VsMgmt/ne-vsmgmt-vss_protection_level)  
</dl>

## <a name="new-vss-structures"></a>Nuove strutture VSS

<dl>

[**\_informazioni sulla \_ protezione del volume VSS \_**](/windows/desktop/api/VsMgmt/ns-vsmgmt-vss_volume_protection_info)  
</dl>

## <a name="existing-vss-enumeration-modifications"></a>Modifiche dell'enumerazione VSS esistenti

<dl> <dt>

<span id="VSS_BACKUP_SCHEMA_enumeration"></span><span id="vss_backup_schema_enumeration"></span><span id="VSS_BACKUP_SCHEMA_ENUMERATION"></span>Servizio Copia [**shadow \_ del volume Enumerazione \_ dello schema di backup**](/windows/desktop/api/Vss/ne-vss-vss_backup_schema)
</dt> <dd>

<dl> <dt>

<span id="Added_value_"></span><span id="added_value_"></span><span id="ADDED_VALUE_"></span>Valore aggiunto:
</dt> <dd>

VSS \_ BS \_ writer \_ supporta \_ i \_ ripristini paralleli

</dd> </dl> </dd> </dl>

<dl> <dt>

<span id="_VSS_VOLUME_SNAPSHOT_ATTRIBUTES_enumeration"></span><span id="_vss_volume_snapshot_attributes_enumeration"></span><span id="_VSS_VOLUME_SNAPSHOT_ATTRIBUTES_ENUMERATION"></span>Enumerazione [**\_ \_ \_ \_ attributi snapshot del volume VSS**](/windows/desktop/api/Vss/ne-vss-vss_volume_snapshot_attributes)
</dt> <dd>

<dl> <dt>

<span id="Added_values_"></span><span id="added_values_"></span><span id="ADDED_VALUES_"></span>Valori aggiunti:
</dt> <dd>

\_ \_ \_ snapshot posticipato VolSnap attr di VSS \_

VSS \_ VolSnap \_ attr \_ TXF \_ Recovery

</dd> </dl> </dd> </dl>

## <a name="existing-vss-interface-modifications"></a>Modifiche all'interfaccia VSS esistente

<dl> <dt>

<span id="IVssBackupComponentsEx2_interface"></span><span id="ivssbackupcomponentsex2_interface"></span><span id="IVSSBACKUPCOMPONENTSEX2_INTERFACE"></span>Interfaccia [**IVssBackupComponentsEx2**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssbackupcomponentsex2)
</dt> <dd>

<dl> <dt>

<span id="Added_method_"></span><span id="added_method_"></span><span id="ADDED_METHOD_"></span>Metodo aggiunto:
</dt> <dd>

[**BreakSnapshotSetEx**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponentsex2-breaksnapshotsetex)

</dd> </dl> </dd> </dl>

## <a name="new-vss-writers"></a>Nuovi writer VSS

In Windows Server 2008 e Windows Vista con SP1 sono stati introdotti i writer VSS seguenti:

-   Writer di configurazione IIS
-   Writer metabase IIS
-   Writer VSS server dei criteri di servizio
-   Writer VSS del gateway Servizi Desktop remoto (Servizi terminal)
-   Writer VSS di gestione licenze Servizi Desktop remoto (Servizi terminal)

Questi writer sono documentati in [writer VSS in-box](in-box-vss-writers.md).

 

 



