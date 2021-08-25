---
description: 'La combinazione di percorso, specifica di file e flag di ricorsione (rispettivamente wszPath, wszFileSpec e bRecursive) deve corrispondere a quella di uno dei set di file aggiunti a uno dei componenti del writer usando IVssCreateWriterMetadata::AddFilesToFileGroup, IVssCreateWriterMetadata::AddDatabaseFiles o IVssCreateWriterMetadata::AddDatabaseLogFiles quando:'
ms.assetid: debf181a-1579-46f2-86ef-a1d2a850e99e
title: Modifiche semantiche Windows Server 2003
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8319259dc27c981822bb242d20243264ca9025d959693aafcb3836976fd7754d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119866261"
---
# <a name="semantic-changes-to-windows-server-2003"></a>Modifiche semantiche Windows Server 2003

La combinazione di percorso, specifica di file e flag di ricorsione (*rispettivamente wszPath*, *wszFileSpec* e *bRecursive)* deve corrispondere a quella di uno dei set di file aggiunti a uno dei componenti del writer usando [**IVssCreateWriterMetadata::AddFilesToFileGroup**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-addfilestofilegroup), [**IVssCreateWriterMetadata::AddDatabaseFiles**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-adddatabasefiles)o [**IVssCreateWriterMetadata::AddDatabaseLogFiles**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-adddatabaselogfiles) quando:

-   Un richiedente aggiunge una nuova destinazione [**usando IVssBackupComponents::AddNewTarget.**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addnewtarget)
-   Un writer aggiunge un mapping di percorso alternativo [**usando IVssCreateWriterMetadata::AddAlternateLocationMapping**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-addalternatelocationmapping).
-   I file esistenti vengono aggiunti come file differenze [**usando IVssComponent::AddDifferencedFilesByLastModifyTime**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-adddifferencedfilesbylastmodifytime).
-   Un richiedente indica che è stato usato un mapping del percorso alternativo per ripristinare un set di file [**usando IVssBackupComponents::AddAlternativeLocationMapping**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addalternativelocationmapping).

 

 



