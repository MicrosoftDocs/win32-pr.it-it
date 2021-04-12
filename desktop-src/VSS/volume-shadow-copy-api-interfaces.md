---
description: L'API Servizio Copia Shadow del volume (VSS) fornisce le interfacce COM e C++ per supportare la creazione di richiedenti e writer.
ms.assetid: 3a0c60df-666c-4e33-a54c-7fa5ddbfde13
title: Interfacce API copia shadow del volume
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bc1291f0e63b18530f92d99f9d526202df078fc8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104129303"
---
# <a name="volume-shadow-copy-api-interfaces"></a>Interfacce API copia shadow del volume

L'API Servizio Copia Shadow del volume (VSS) fornisce le interfacce COM e C++ per supportare la creazione di richiedenti e writer.

## <a name="vss-requester-specific-interfaces"></a>Interfacce Requester-Specific VSS

-   [**IVssBackupComponents**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssbackupcomponents)
-   [**IVssBackupComponentsEx**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssbackupcomponentsex)
-   [**IVssBackupComponentsEx2**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssbackupcomponentsex2)
-   [**IVssBackupComponentsEx3**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssbackupcomponentsex3)
-   [**IVssExamineWriterMetadata**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssexaminewritermetadata)
-   [**IVssExamineWriterMetadataEx**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssexaminewritermetadataex)
-   [**IVssExamineWriterMetadataEx2**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssexaminewritermetadataex2)
-   [**IVssWMComponent**](/windows/desktop/api/VsBackup/nl-vsbackup-ivsswmcomponent)
-   [**IVssWriterComponentsExt**](/windows/win32/api/vsbackup/nl-vsbackup-ivsswritercomponentsext)

## <a name="vss-writer-specific-interfaces"></a>Interfacce Writer-Specific VSS

-   [**IVssCreateExpressWriterMetadata**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscreateexpresswritermetadata)
-   [**IVssCreateWriterMetadata**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscreatewritermetadata)
-   [**IVssCreateWriterMetadataEx**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscreatewritermetadataex)
-   [**IVssExpressWriter**](/windows/desktop/api/VsWriter/nl-vswriter-ivssexpresswriter)
-   [**IVssWriterComponents**](/windows/desktop/api/VsWriter/nl-vswriter-ivsswritercomponents)

## <a name="vss-hardware-provider-specific-interfaces"></a>Interfacce di Provider-Specific hardware VSS

-   [**IVssAdmin**](/windows/desktop/api/VsAdmin/nn-vsadmin-ivssadmin)
-   [**IVssHardwareSnapshotProvider**](/windows/desktop/api/VsProv/nn-vsprov-ivsshardwaresnapshotprovider)
-   [**IVssHardwareSnapshotProviderEx**](/windows/desktop/api/VsProv/nn-vsprov-ivsshardwaresnapshotproviderex)
-   [**IVssProviderCreateSnapshotSet**](/windows/desktop/api/VsProv/nn-vsprov-ivssprovidercreatesnapshotset)
-   [**IVssProviderNotifications**](/windows/desktop/api/VsProv/nn-vsprov-ivssprovidernotifications)

## <a name="vss-software-provider-specific-interfaces"></a>Interfacce di Provider-Specific software VSS

-   [**IVssSoftwareSnapshotProvider**](/windows/desktop/api/VsProv/nn-vsprov-ivsssoftwaresnapshotprovider)

## <a name="vss-shared-interfaces"></a>Interfacce condivise VSS

-   [**IVssAsync**](/windows/desktop/api/Vss/nn-vss-ivssasync)
-   [**IVssComponent**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponent)
-   [**IVssComponentEx**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponentex)
-   [**IVssComponentEx2**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponentex2)
-   [**IVssEnumObject**](/windows/desktop/api/Vss/nn-vss-ivssenumobject)
-   [**IVssWMDependency**](/windows/desktop/api/VsWriter/nl-vswriter-ivsswmdependency)
-   [**IVssWMFiledesc**](/windows/desktop/api/VsWriter/nl-vswriter-ivsswmfiledesc)

## <a name="vss-management-interfaces"></a>Interfacce di gestione VSS

-   [**IVssDifferentialSoftwareSnapshotMgmt**](/windows/desktop/api/VsMgmt/nn-vsmgmt-ivssdifferentialsoftwaresnapshotmgmt)
-   [**IVssDifferentialSoftwareSnapshotMgmt2**](/windows/desktop/api/VsMgmt/nn-vsmgmt-ivssdifferentialsoftwaresnapshotmgmt2)
-   [**IVssDifferentialSoftwareSnapshotMgmt3**](/windows/desktop/api/VsMgmt/nn-vsmgmt-ivssdifferentialsoftwaresnapshotmgmt3)
-   [**IVssEnumMgmtObject**](/windows/desktop/api/VsMgmt/nn-vsmgmt-ivssenummgmtobject)
-   [**IVssSnapshotMgmt**](/windows/desktop/api/VsMgmt/nn-vsmgmt-ivsssnapshotmgmt)
-   [**IVssSnapshotMgmt2**](/windows/desktop/api/VsMgmt/nn-vsmgmt-ivsssnapshotmgmt2)

 

 
