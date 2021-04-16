---
description: Se nessuno dei due file ha un numero di versione, il Windows Installer usa la logica illustrata nel diagramma di flusso seguente per determinare se sostituire tutti i file installati appartenenti al componente.
ms.assetid: 82cb0d96-f49f-408e-a8c6-a0d1ee9af8c7
title: Nessun file ha una versione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5360bb7b6b4deda54156006073f353ab65ab2b2e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104559928"
---
# <a name="neither-file-has-a-version"></a><span data-ttu-id="c50a9-103">Nessun file ha una versione</span><span class="sxs-lookup"><span data-stu-id="c50a9-103">Neither File Has a Version</span></span>

<span data-ttu-id="c50a9-104">Se il file di chiave di un componente da installare (Copy-A) ha lo stesso nome di un file già installato nel percorso di destinazione (Copy-B), il programma di installazione confronta il numero di versione, la data e la lingua dei due file.</span><span class="sxs-lookup"><span data-stu-id="c50a9-104">If the key file of a component being installed (copy-A) has the same name as a file already installed in the target location (copy-B), the installer compares the version number, date, and language of the two files.</span></span>

<span data-ttu-id="c50a9-105">Se nessuno dei due file ha un numero di versione, il programma di installazione usa la logica illustrata nel diagramma di flusso seguente per determinare se sostituire tutti i file installati appartenenti al componente.</span><span class="sxs-lookup"><span data-stu-id="c50a9-105">If neither file has a version number, the installer uses the logic illustrated by the following flow diagram to determine whether to replace all of the installed files belonging to the component.</span></span> <span data-ttu-id="c50a9-106">Poiché il programma di installazione installa solo interi componenti, se il file di chiave installato viene sostituito, vengono sostituiti tutti i file del componente.</span><span class="sxs-lookup"><span data-stu-id="c50a9-106">Because the installer only installs entire components, if the installed key file is replaced, then all of the component's files are replaced.</span></span>

<span data-ttu-id="c50a9-107">Si noti che questo diagramma illustra le regole predefinite di [controllo delle versioni dei file](file-versioning-rules.md), che possono essere sostituite impostando la proprietà [**REINSTALLMODE**](reinstallmode.md) .</span><span class="sxs-lookup"><span data-stu-id="c50a9-107">Note that this diagram illustrates the default [File Versioning Rules](file-versioning-rules.md), which can be overridden by setting the [**REINSTALLMODE**](reinstallmode.md) property.</span></span> <span data-ttu-id="c50a9-108">Il valore predefinito della proprietà **REINSTALLMODE** è "omus".</span><span class="sxs-lookup"><span data-stu-id="c50a9-108">The default value of the **REINSTALLMODE** property is "omus".</span></span>

![regole di controllo delle versioni dei file predefinite quando nessuno dei due file ha un numero di versione](images/waiflow2.png)

<span data-ttu-id="c50a9-110">Vedere gli esempi di controllo delle versioni dei file predefiniti per la [sostituzione dei file esistenti](replacing-existing-files.md).</span><span class="sxs-lookup"><span data-stu-id="c50a9-110">See the examples of default file versioning in [Replacing Existing Files](replacing-existing-files.md).</span></span>

-   [<span data-ttu-id="c50a9-111">Entrambi i file hanno una versione</span><span class="sxs-lookup"><span data-stu-id="c50a9-111">Both Files Have a Version</span></span>](both-files-have-a-version.md)
-   [<span data-ttu-id="c50a9-112">Nessun file ha una versione con controllo hash file</span><span class="sxs-lookup"><span data-stu-id="c50a9-112">Neither File Has a Version with File Hash Check</span></span>](neither-file-has-a-version-with-file-hash-check.md)
-   [<span data-ttu-id="c50a9-113">Un file ha una versione</span><span class="sxs-lookup"><span data-stu-id="c50a9-113">One File Has a Version</span></span>](one-file-has-a-version.md)

 

 



