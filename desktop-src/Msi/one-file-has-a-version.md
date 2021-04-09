---
description: Se solo uno dei file ha un numero di versione, il Windows Installer usa la logica illustrata nel diagramma di flusso seguente per determinare se sostituire tutti i file installati appartenenti al componente.
ms.assetid: 1eda5521-6e23-49b8-9870-f5370def487e
title: Un file ha una versione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 417060119f8b13b1545161faa80552c79e8ca9aa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104130283"
---
# <a name="one-file-has-a-version"></a><span data-ttu-id="4cd45-103">Un file ha una versione</span><span class="sxs-lookup"><span data-stu-id="4cd45-103">One File Has a Version</span></span>

<span data-ttu-id="4cd45-104">Se il file di chiave di un componente da installare (Copy-A) ha lo stesso nome di un file già installato nel percorso di destinazione (Copy-B), il programma di installazione confronta il numero di versione, la data e la lingua dei due file.</span><span class="sxs-lookup"><span data-stu-id="4cd45-104">If the key file of a component being installed (copy-A) has the same name as a file already installed in the target location (copy-B), the installer compares the version number, date, and language of the two files.</span></span>

<span data-ttu-id="4cd45-105">Se solo uno dei file ha un numero di versione, il programma di installazione usa la logica illustrata nel diagramma di flusso seguente per determinare se sostituire tutti i file installati appartenenti al componente.</span><span class="sxs-lookup"><span data-stu-id="4cd45-105">If only one of the files has a version number, the installer uses the logic illustrated by the following flow diagram to determine whether to replace all of the installed files belonging to the component.</span></span> <span data-ttu-id="4cd45-106">Poiché il programma di installazione installa solo interi componenti, se il file di chiave installato viene sostituito, vengono sostituiti tutti i file del componente.</span><span class="sxs-lookup"><span data-stu-id="4cd45-106">Because the installer only installs entire components, if the installed key file is replaced, then all of the component's files are replaced.</span></span>

<span data-ttu-id="4cd45-107">Si noti che questo diagramma illustra le regole predefinite di [controllo delle versioni dei file](file-versioning-rules.md), che possono essere sostituite impostando la proprietà [**REINSTALLMODE**](reinstallmode.md) .</span><span class="sxs-lookup"><span data-stu-id="4cd45-107">Note that this diagram illustrates the default [File Versioning Rules](file-versioning-rules.md), which can be overridden by setting the [**REINSTALLMODE**](reinstallmode.md) property.</span></span> <span data-ttu-id="4cd45-108">Il valore predefinito della proprietà **REINSTALLMODE** è "omus".</span><span class="sxs-lookup"><span data-stu-id="4cd45-108">The default value of the **REINSTALLMODE** property is "omus".</span></span>

![regole di controllo delle versioni dei file predefinite quando un solo file ha un numero di versione](images/waiflow3.png)

<span data-ttu-id="4cd45-110">Vedere gli esempi di controllo delle versioni dei file predefiniti per la [sostituzione dei file esistenti](replacing-existing-files.md).</span><span class="sxs-lookup"><span data-stu-id="4cd45-110">See the examples of default file versioning in [Replacing Existing Files](replacing-existing-files.md).</span></span>

-   [<span data-ttu-id="4cd45-111">Entrambi i file hanno una versione</span><span class="sxs-lookup"><span data-stu-id="4cd45-111">Both Files Have a Version</span></span>](both-files-have-a-version.md)
-   [<span data-ttu-id="4cd45-112">Nessun file ha una versione</span><span class="sxs-lookup"><span data-stu-id="4cd45-112">Neither File Has a Version</span></span>](neither-file-has-a-version.md)
-   [<span data-ttu-id="4cd45-113">Nessun file ha una versione con controllo hash file</span><span class="sxs-lookup"><span data-stu-id="4cd45-113">Neither File Has a Version with File Hash Check</span></span>](neither-file-has-a-version-with-file-hash-check.md)

 

 



