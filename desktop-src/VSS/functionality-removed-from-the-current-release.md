---
description: 'La versione di VSS di Windows Server 2003 non supporta più quanto segue:'
ms.assetid: 01993cae-433e-4d01-b805-f97592369575
title: Funzionalità rimosse da Windows Server 2003
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 181d053420f0fc947ebad024c0eaf2bbaf32f3e6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106310715"
---
# <a name="functionality-removed-from-windows-server-2003"></a>Funzionalità rimosse da Windows Server 2003

La versione di VSS di Windows Server 2003 non supporta più quanto segue:

-   I writer non possono specificare nuove destinazioni di ripristino di file ([*nuovi percorsi di destinazione*](vssgloss-n.md)) durante le operazioni di ripristino.
-   Il rimontaggio di una copia shadow esposta come volume scrivibile non è più supportato. Il metodo **IVssBackupComponents:: RemountReadWrite** non è più disponibile.
-   I writer non possono specificare i file inclusi in modo esplicito (usando [**IVssCreateWriterMetadata:: AddIncludeFiles**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-addincludefiles)). I file possono essere aggiunti a un componente solo come parte di un set di file tramite [**IVssCreateWriterMetadata:: AddFilesToFileGroup**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-addfilestofilegroup), [**IVssCreateWriterMetadata:: AddDatabaseFiles**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-adddatabasefiles)o [**IVssCreateWriterMetadata:: AddDatabaseLogFiles**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-adddatabaselogfiles).

    I file possono comunque essere esclusi in modo esplicito da un componente usando [**IVssCreateWriterMetadata:: AddExcludeFiles**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-addexcludefiles).

 

 



