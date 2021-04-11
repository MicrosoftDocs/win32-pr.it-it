---
description: 'La combinazione di percorso, specifica file e flag di ricorsione (rispettivamente wszPath, wszFileSpec e bRecursive) deve corrispondere a quella di uno dei set di file aggiunti a uno dei componenti del writer usando IVssCreateWriterMetadata:: AddFilesToFileGroup, IVssCreateWriterMetadata:: AddDatabaseFiles o IVssCreateWriterMetadata:: AddDatabaseLogFiles quando:'
ms.assetid: debf181a-1579-46f2-86ef-a1d2a850e99e
title: Modifiche semantiche di Windows Server 2003
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 53b9d2edc56f215f554b497eebff9f76a1da53dd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104227036"
---
# <a name="semantic-changes-to-windows-server-2003"></a>Modifiche semantiche di Windows Server 2003

La combinazione di percorso, specifica file e flag di ricorsione (rispettivamente *wszPath*, *wszFileSpec* e *bRecursive*) deve corrispondere a quella di uno dei set di file aggiunti a uno dei componenti del writer usando [**IVssCreateWriterMetadata:: AddFilesToFileGroup**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-addfilestofilegroup), [**IVssCreateWriterMetadata:: AddDatabaseFiles**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-adddatabasefiles)o [**IVssCreateWriterMetadata:: AddDatabaseLogFiles**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-adddatabaselogfiles) quando:

-   Un richiedente aggiunge una nuova destinazione usando [**IVssBackupComponents:: AddNewTarget**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addnewtarget).
-   Un writer aggiunge un mapping del percorso alternativo usando [**IVssCreateWriterMetadata:: AddAlternateLocationMapping**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-addalternatelocationmapping).
-   I file esistenti vengono aggiunti come file differenziati con [**IVssComponent:: AddDifferencedFilesByLastModifyTime**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-adddifferencedfilesbylastmodifytime).
-   Un richiedente indica che è stato usato un mapping del percorso alternativo per ripristinare un set di file con [**IVssBackupComponents:: AddAlternativeLocationMapping**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addalternativelocationmapping).

 

 



