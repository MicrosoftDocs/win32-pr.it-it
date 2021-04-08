---
description: Se entrambi i file hanno un numero di versione, il Windows Installer usa la logica illustrata nel diagramma di flusso seguente per determinare se sostituire tutti i file installati appartenenti al componente.
ms.assetid: c4c8a23b-e1c2-4c96-b708-7cbcbcab4cd4
title: Entrambi i file hanno una versione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ddb52c7333e5455d40475c9f845643535b271d0b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103881073"
---
# <a name="both-files-have-a-version"></a><span data-ttu-id="a9ada-103">Entrambi i file hanno una versione</span><span class="sxs-lookup"><span data-stu-id="a9ada-103">Both Files Have a Version</span></span>

<span data-ttu-id="a9ada-104">Se il file di chiave di un componente da installare (Copy-A) ha lo stesso nome di un file già installato nel percorso di destinazione (Copy-B), il programma di installazione confronta il numero di versione e la lingua dei due file.</span><span class="sxs-lookup"><span data-stu-id="a9ada-104">If the key file of a component being installed (copy-A) has the same name as a file already installed in the target location (copy-B), the installer compares the version number and language of the two files.</span></span>

<span data-ttu-id="a9ada-105">Se entrambi i file hanno un numero di versione, il programma di installazione usa la logica illustrata nel diagramma di flusso seguente per determinare se sostituire tutti i file installati appartenenti al componente.</span><span class="sxs-lookup"><span data-stu-id="a9ada-105">If both files have a version number, the installer uses the logic illustrated by the following flow diagram to determine whether to replace all of the installed files belonging to the component.</span></span> <span data-ttu-id="a9ada-106">Poiché il programma di installazione installa solo interi componenti, se il file di chiave installato viene sostituito, vengono sostituiti tutti i file del componente.</span><span class="sxs-lookup"><span data-stu-id="a9ada-106">Because the installer only installs entire components, if the installed key file is replaced then all of the component's files are replaced.</span></span>

<span data-ttu-id="a9ada-107">Si noti che questo diagramma illustra le regole predefinite di [controllo delle versioni dei file](file-versioning-rules.md), che possono essere sostituite impostando la proprietà [**REINSTALLMODE**](reinstallmode.md) .</span><span class="sxs-lookup"><span data-stu-id="a9ada-107">Note that this diagram illustrates the default [File Versioning Rules](file-versioning-rules.md), which can be overridden by setting the [**REINSTALLMODE**](reinstallmode.md) property.</span></span> <span data-ttu-id="a9ada-108">Il valore predefinito della proprietà **REINSTALLMODE** è "omus".</span><span class="sxs-lookup"><span data-stu-id="a9ada-108">The default value of the **REINSTALLMODE** property is "omus".</span></span>

![regole di controllo delle versioni dei file predefinite quando entrambi i file hanno lo stesso nome o numero di versione](images/waiflow1.png)

<span data-ttu-id="a9ada-110">Il diagramma precedente può essere usato anche con i file senza lingua specificata.</span><span class="sxs-lookup"><span data-stu-id="a9ada-110">The previous diagram can also be used with files with no language specified.</span></span> <span data-ttu-id="a9ada-111">Se Copy-A ha una lingua specificata e copy-B non ha un linguaggio specificato, Copy-B viene sostituito con Copy-A.</span><span class="sxs-lookup"><span data-stu-id="a9ada-111">If copy-A has a specified language and copy-B has no specified language, copy-B is replaced with copy-A.</span></span> <span data-ttu-id="a9ada-112">Se per Copy-A e copy-B non è specificato alcun linguaggio, Copy-B non viene sostituito.</span><span class="sxs-lookup"><span data-stu-id="a9ada-112">If copy-A and copy-B both have no language specified, then copy-B is not replaced.</span></span>

<span data-ttu-id="a9ada-113">Per la [sostituzione dei file esistenti](replacing-existing-files.md), vedere esempi di controllo delle versioni dei file predefiniti.</span><span class="sxs-lookup"><span data-stu-id="a9ada-113">See examples of default file versioning in [Replacing Existing Files](replacing-existing-files.md).</span></span>

-   [<span data-ttu-id="a9ada-114">Nessun file ha una versione</span><span class="sxs-lookup"><span data-stu-id="a9ada-114">Neither File Has a Version</span></span>](neither-file-has-a-version.md)
-   [<span data-ttu-id="a9ada-115">Nessun file ha una versione con controllo hash file</span><span class="sxs-lookup"><span data-stu-id="a9ada-115">Neither File Has a Version with File Hash Check</span></span>](neither-file-has-a-version-with-file-hash-check.md)
-   [<span data-ttu-id="a9ada-116">Un file ha una versione</span><span class="sxs-lookup"><span data-stu-id="a9ada-116">One File Has a Version</span></span>](one-file-has-a-version.md)

 

 



