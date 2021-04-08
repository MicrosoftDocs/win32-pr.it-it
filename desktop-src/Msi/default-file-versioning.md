---
description: I diagrammi di flusso nelle sezioni seguenti illustrano le regole predefinite di controllo delle versioni dei file usate quando il file di chiave di un componente installato ha lo stesso nome di un file già installato nel percorso di destinazione.
ms.assetid: a09e091c-ee82-4951-b129-d1d4c8948883
title: Controllo delle versioni dei file predefinito
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fad33a7af49c28b560d9d558abbc86b220c4cb42
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103883005"
---
# <a name="default-file-versioning"></a><span data-ttu-id="2a7cc-103">Controllo delle versioni dei file predefinito</span><span class="sxs-lookup"><span data-stu-id="2a7cc-103">Default File Versioning</span></span>

<span data-ttu-id="2a7cc-104">I diagrammi di flusso nelle sezioni seguenti illustrano le regole predefinite di controllo delle versioni dei file usate quando il file di chiave di un componente installato ha lo stesso nome di un file già installato nel percorso di destinazione.</span><span class="sxs-lookup"><span data-stu-id="2a7cc-104">The flow diagrams in the following sections illustrate the default file versioning rules used when the key file of a component being installed has the same name as a file already installed in the target location.</span></span> <span data-ttu-id="2a7cc-105">Il controllo delle versioni dei file predefinito è illustrato anche in [sostituzione dei file esistenti](replacing-existing-files.md).</span><span class="sxs-lookup"><span data-stu-id="2a7cc-105">Default file versioning is also illustrated in [Replacing Existing Files](replacing-existing-files.md).</span></span>

<span data-ttu-id="2a7cc-106">Si noti che con Windows Installer, l'hashing dei file è disponibile per ottimizzare la copia di file.</span><span class="sxs-lookup"><span data-stu-id="2a7cc-106">Note that with Windows Installer, file hashing is available to optimize the copying of files.</span></span> <span data-ttu-id="2a7cc-107">Per informazioni dettagliate, vedere [**MsiGetFileHash**](/windows/desktop/api/Msi/nf-msi-msigetfilehasha) e la [tabella MsiFileHash](msifilehash-table.md).</span><span class="sxs-lookup"><span data-stu-id="2a7cc-107">For details, see [**MsiGetFileHash**](/windows/desktop/api/Msi/nf-msi-msigetfilehasha) and the [MsiFileHash table](msifilehash-table.md).</span></span> <span data-ttu-id="2a7cc-108">La tabella MsiFileHash può essere utilizzata solo con file senza versione.</span><span class="sxs-lookup"><span data-stu-id="2a7cc-108">The MsiFileHash table can only be used with unversioned files.</span></span>

-   [<span data-ttu-id="2a7cc-109">Entrambi i file hanno una versione</span><span class="sxs-lookup"><span data-stu-id="2a7cc-109">Both Files Have a Version</span></span>](both-files-have-a-version.md)
-   [<span data-ttu-id="2a7cc-110">Nessun file ha una versione</span><span class="sxs-lookup"><span data-stu-id="2a7cc-110">Neither File Has a Version</span></span>](neither-file-has-a-version.md)
-   [<span data-ttu-id="2a7cc-111">Nessun file ha una versione con controllo hash file</span><span class="sxs-lookup"><span data-stu-id="2a7cc-111">Neither File Has a Version with File Hash Check</span></span>](neither-file-has-a-version-with-file-hash-check.md)
-   [<span data-ttu-id="2a7cc-112">Un file ha una versione</span><span class="sxs-lookup"><span data-stu-id="2a7cc-112">One File Has a Version</span></span>](one-file-has-a-version.md)

 

 



