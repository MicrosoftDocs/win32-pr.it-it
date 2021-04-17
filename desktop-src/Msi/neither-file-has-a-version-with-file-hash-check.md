---
description: L'hashing dei file è disponibile con Windows Installer. Per ulteriori informazioni, vedere MsiGetFileHash e la tabella MsiFileHash. La tabella MsiFileHash può essere utilizzata solo con file senza versione.
ms.assetid: 608859ac-6640-4c28-b4f0-34ab36d804d7
title: Nessun file ha una versione con controllo hash file
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 415019838ac29418b13b513b393a18af2131510f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104528171"
---
# <a name="neither-file-has-a-version-with-file-hash-check"></a><span data-ttu-id="ecaf5-105">Nessun file ha una versione con controllo hash file</span><span class="sxs-lookup"><span data-stu-id="ecaf5-105">Neither File Has a Version with File Hash Check</span></span>

<span data-ttu-id="ecaf5-106">L'hashing dei file è disponibile con Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="ecaf5-106">File hashing is available with Windows Installer.</span></span> <span data-ttu-id="ecaf5-107">Per ulteriori informazioni, vedere [**MsiGetFileHash**](/windows/desktop/api/Msi/nf-msi-msigetfilehasha) e la [tabella MsiFileHash](msifilehash-table.md).</span><span class="sxs-lookup"><span data-stu-id="ecaf5-107">For more information, see [**MsiGetFileHash**](/windows/desktop/api/Msi/nf-msi-msigetfilehasha) and the [MsiFileHash table](msifilehash-table.md).</span></span> <span data-ttu-id="ecaf5-108">La tabella MsiFileHash può essere utilizzata solo con file senza versione.</span><span class="sxs-lookup"><span data-stu-id="ecaf5-108">The MsiFileHash table can only be used with unversioned files.</span></span>

<span data-ttu-id="ecaf5-109">Se il file di chiave di un componente da installare (Copy-A) ha lo stesso nome di un file già installato nel percorso di destinazione (Copy-B), il programma di installazione confronta il numero di versione, la data e la lingua dei due file.</span><span class="sxs-lookup"><span data-stu-id="ecaf5-109">If the key file of a component being installed (copy-A) has the same name as a file already installed in the target location (copy-B), the installer compares the version number, date, and language of the two files.</span></span>

<span data-ttu-id="ecaf5-110">Se nessuno dei due file ha un numero di versione, il programma di installazione usa la logica illustrata nel diagramma di flusso seguente per determinare se sostituire tutti i file installati appartenenti al componente.</span><span class="sxs-lookup"><span data-stu-id="ecaf5-110">If neither file has a version number, the installer uses the logic illustrated by the following flow diagram to determine whether to replace all of the installed files belonging to the component.</span></span> <span data-ttu-id="ecaf5-111">Poiché il programma di installazione installa solo interi componenti, se il file di chiave installato viene sostituito, vengono sostituiti tutti i file del componente.</span><span class="sxs-lookup"><span data-stu-id="ecaf5-111">Because the installer only installs entire components, if the installed key file is replaced then, all of the component's files are replaced.</span></span>

<span data-ttu-id="ecaf5-112">Si noti che questo diagramma illustra le regole predefinite di [controllo delle versioni dei file](file-versioning-rules.md), che possono essere sostituite impostando la proprietà [**REINSTALLMODE**](reinstallmode.md) .</span><span class="sxs-lookup"><span data-stu-id="ecaf5-112">Note that this diagram illustrates the default [File Versioning Rules](file-versioning-rules.md), which can be overridden by setting the [**REINSTALLMODE**](reinstallmode.md) property.</span></span> <span data-ttu-id="ecaf5-113">Il valore predefinito della proprietà **REINSTALLMODE** è "omus".</span><span class="sxs-lookup"><span data-stu-id="ecaf5-113">The default value of the **REINSTALLMODE** property is "omus".</span></span>

![regole predefinite di controllo delle versioni dei file quando ne viene eseguito l'override dall'impostazione della proprietà REINSTALLMODE](images/waiflow2b.png)

<span data-ttu-id="ecaf5-115">Vedere gli esempi di controllo delle versioni dei file predefiniti per la [sostituzione dei file esistenti](replacing-existing-files.md).</span><span class="sxs-lookup"><span data-stu-id="ecaf5-115">See the examples of default file versioning in [Replacing Existing Files](replacing-existing-files.md).</span></span>

-   [<span data-ttu-id="ecaf5-116">Entrambi i file hanno una versione</span><span class="sxs-lookup"><span data-stu-id="ecaf5-116">Both Files Have a Version</span></span>](both-files-have-a-version.md)
-   [<span data-ttu-id="ecaf5-117">Nessun file ha una versione</span><span class="sxs-lookup"><span data-stu-id="ecaf5-117">Neither File Has a Version</span></span>](neither-file-has-a-version.md)
-   [<span data-ttu-id="ecaf5-118">Un file ha una versione</span><span class="sxs-lookup"><span data-stu-id="ecaf5-118">One File Has a Version</span></span>](one-file-has-a-version.md)

 

 



