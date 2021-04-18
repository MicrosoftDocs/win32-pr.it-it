---
description: Le operazioni di backup e ripristino in genere copiano i file da un determinato percorso predefinito sul disco a un supporto di backup e quindi il ripristino da tale supporto nello stesso percorso predefinito sul disco.
ms.assetid: 7609c392-d5f8-48c2-8e7e-f35f56cf94f8
title: Percorsi di backup e ripristino non predefiniti
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c809b886886c1d84de1cc3960163a7cc94179cb7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106310694"
---
# <a name="non-default-backup-and-restore-locations"></a><span data-ttu-id="f201a-103">Percorsi di backup e ripristino non predefiniti</span><span class="sxs-lookup"><span data-stu-id="f201a-103">Non-Default Backup and Restore Locations</span></span>

<span data-ttu-id="f201a-104">Le operazioni di backup e ripristino in genere copiano i file da un determinato percorso predefinito sul disco a un supporto di backup e quindi il ripristino da tale supporto nello stesso percorso predefinito sul disco.</span><span class="sxs-lookup"><span data-stu-id="f201a-104">Backup and restore operations typically copy files from a given, default location on disk to backup media and then restore from that media to the same default location on disk.</span></span>

<span data-ttu-id="f201a-105">Esistono diversi motivi, in particolare quando si gestiscono i processi in esecuzione, senza seguire questo semplice modello.</span><span class="sxs-lookup"><span data-stu-id="f201a-105">There are many reasons, particularly when dealing with running processes, not to follow this simple model.</span></span> <span data-ttu-id="f201a-106">VSS supporta l'utilizzo di origini non standard per il backup e destinazioni alternative per il ripristino e include meccanismi che consentono di utilizzare subset di file e di modificare il mapping dei file.</span><span class="sxs-lookup"><span data-stu-id="f201a-106">VSS supports using nonstandard sources for backup and alternate destinations for restore, and includes mechanisms to work with subsets of files and to remap files.</span></span>

-   [<span data-ttu-id="f201a-107">Utilizzo di percorsi alternativi durante il backup</span><span class="sxs-lookup"><span data-stu-id="f201a-107">Working with Alternate Paths during Backup</span></span>](working-with-alternate-paths-during-backup.md)
-   [<span data-ttu-id="f201a-108">Utilizzo di percorsi alternativi durante il ripristino</span><span class="sxs-lookup"><span data-stu-id="f201a-108">Working with Alternate Locations during Restore</span></span>](working-with-alternate-locations-during-restore.md)
-   [<span data-ttu-id="f201a-109">Utilizzo di nuove destinazioni durante il ripristino</span><span class="sxs-lookup"><span data-stu-id="f201a-109">Working with New Targets during Restore</span></span>](working-with-new-targets-during-restore.md)
-   [<span data-ttu-id="f201a-110">Utilizzo di file parziali</span><span class="sxs-lookup"><span data-stu-id="f201a-110">Working with Partial Files</span></span>](working-with-partial-files.md)
-   [<span data-ttu-id="f201a-111">Utilizzo di destinazioni dirette</span><span class="sxs-lookup"><span data-stu-id="f201a-111">Working with Directed Targets</span></span>](working-with-directed-targets.md)

 

 



