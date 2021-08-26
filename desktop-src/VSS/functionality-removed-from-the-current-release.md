---
description: 'La Windows Server 2003 di VSS non supporta più quanto segue:'
ms.assetid: 01993cae-433e-4d01-b805-f97592369575
title: Funzionalità rimosse da Windows Server 2003
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bb7cd2cbfce24717bdd0bf0c36db1c5d8ff7faddebd5b7795cff6640b74df3c1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120006361"
---
# <a name="functionality-removed-from-windows-server-2003"></a>Funzionalità rimosse da Windows Server 2003

La Windows Server 2003 di VSS non supporta più quanto segue:

-   I writer non possono specificare nuove destinazioni di ripristino file ([*nuovi percorsi di destinazione*](vssgloss-n.md)) durante le operazioni di ripristino.
-   Il rimontaggio di una copia shadow esposta come volume scrivibile non è più supportato. Il **metodo IVssBackupComponents::RemountReadWrite** non è più disponibile.
-   I writer non possono specificare file inclusi in modo esplicito [**(usando IVssCreateWriterMetadata::AddIncludeFiles**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-addincludefiles)). I file possono essere aggiunti a un componente solo come parte di un set di file usando [**IVssCreateWriterMetadata::AddFilesToFileGroup**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-addfilestofilegroup), [**IVssCreateWriterMetadata::AddDatabaseFiles**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-adddatabasefiles)o [**IVssCreateWriterMetadata::AddDatabaseLogFiles**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-adddatabaselogfiles).

    I file possono comunque essere esclusi in modo esplicito da un componente usando [**IVssCreateWriterMetadata::AddExcludeFiles**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-addexcludefiles).

 

 



