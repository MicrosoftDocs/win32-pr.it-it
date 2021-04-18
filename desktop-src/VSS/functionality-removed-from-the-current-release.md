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
# <a name="functionality-removed-from-windows-server-2003"></a><span data-ttu-id="d5bff-103">Funzionalità rimosse da Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="d5bff-103">Functionality Removed From Windows Server 2003</span></span>

<span data-ttu-id="d5bff-104">La versione di VSS di Windows Server 2003 non supporta più quanto segue:</span><span class="sxs-lookup"><span data-stu-id="d5bff-104">The Windows Server 2003 release of VSS no longer supports the following:</span></span>

-   <span data-ttu-id="d5bff-105">I writer non possono specificare nuove destinazioni di ripristino di file ([*nuovi percorsi di destinazione*](vssgloss-n.md)) durante le operazioni di ripristino.</span><span class="sxs-lookup"><span data-stu-id="d5bff-105">Writers cannot specify new file restore destinations ([*new target locations*](vssgloss-n.md)) at restore operations.</span></span>
-   <span data-ttu-id="d5bff-106">Il rimontaggio di una copia shadow esposta come volume scrivibile non è più supportato.</span><span class="sxs-lookup"><span data-stu-id="d5bff-106">Remounting an exposed shadow copy as a writable volume is no longer supported.</span></span> <span data-ttu-id="d5bff-107">Il metodo **IVssBackupComponents:: RemountReadWrite** non è più disponibile.</span><span class="sxs-lookup"><span data-stu-id="d5bff-107">The **IVssBackupComponents::RemountReadWrite** method is no longer available.</span></span>
-   <span data-ttu-id="d5bff-108">I writer non possono specificare i file inclusi in modo esplicito (usando [**IVssCreateWriterMetadata:: AddIncludeFiles**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-addincludefiles)).</span><span class="sxs-lookup"><span data-stu-id="d5bff-108">Writers cannot specify explicitly included files (using [**IVssCreateWriterMetadata::AddIncludeFiles**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-addincludefiles)).</span></span> <span data-ttu-id="d5bff-109">I file possono essere aggiunti a un componente solo come parte di un set di file tramite [**IVssCreateWriterMetadata:: AddFilesToFileGroup**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-addfilestofilegroup), [**IVssCreateWriterMetadata:: AddDatabaseFiles**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-adddatabasefiles)o [**IVssCreateWriterMetadata:: AddDatabaseLogFiles**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-adddatabaselogfiles).</span><span class="sxs-lookup"><span data-stu-id="d5bff-109">Files can be added to a component only as part of a file set by using [**IVssCreateWriterMetadata::AddFilesToFileGroup**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-addfilestofilegroup), [**IVssCreateWriterMetadata::AddDatabaseFiles**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-adddatabasefiles), or [**IVssCreateWriterMetadata::AddDatabaseLogFiles**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-adddatabaselogfiles).</span></span>

    <span data-ttu-id="d5bff-110">I file possono comunque essere esclusi in modo esplicito da un componente usando [**IVssCreateWriterMetadata:: AddExcludeFiles**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-addexcludefiles).</span><span class="sxs-lookup"><span data-stu-id="d5bff-110">Files can still be explicitly excluded from a component by using [**IVssCreateWriterMetadata::AddExcludeFiles**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-addexcludefiles).</span></span>

 

 



