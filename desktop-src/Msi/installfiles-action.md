---
description: L'azione InstallFiles copia i file specificati nella tabella file dalla directory di origine alla directory di destinazione.
ms.assetid: 187ad82f-13f5-4ea3-913c-2ae7561a6ee6
title: Azione InstallFiles
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5c2a0206ec5a64974f27375e175f25ce1888b430
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106308685"
---
# <a name="installfiles-action"></a><span data-ttu-id="f9744-103">Azione InstallFiles</span><span class="sxs-lookup"><span data-stu-id="f9744-103">InstallFiles Action</span></span>

<span data-ttu-id="f9744-104">L'azione InstallFiles copia i file specificati nella tabella file dalla directory di origine alla directory di destinazione.</span><span class="sxs-lookup"><span data-stu-id="f9744-104">The InstallFiles action copies files specified in the File table from the source directory to the destination directory.</span></span>

## <a name="sequence-restrictions"></a><span data-ttu-id="f9744-105">Restrizioni sequenza</span><span class="sxs-lookup"><span data-stu-id="f9744-105">Sequence Restrictions</span></span>

<span data-ttu-id="f9744-106">L'azione InstallFiles deve essere successiva all'azione [InstallValidate](installvalidate-action.md) e prima di qualsiasi azione dipendente dal file.</span><span class="sxs-lookup"><span data-stu-id="f9744-106">The InstallFiles action must come after the [InstallValidate](installvalidate-action.md) action and before any file-dependent actions.</span></span>

## <a name="actiondata-messages"></a><span data-ttu-id="f9744-107">Messaggi ActionData</span><span class="sxs-lookup"><span data-stu-id="f9744-107">ActionData Messages</span></span>



| <span data-ttu-id="f9744-108">Campo</span><span class="sxs-lookup"><span data-stu-id="f9744-108">Field</span></span> | <span data-ttu-id="f9744-109">Descrizione dei dati dell'azione</span><span class="sxs-lookup"><span data-stu-id="f9744-109">Description of action data</span></span>                      |
|-------|-------------------------------------------------|
| <span data-ttu-id="f9744-110">\[1\]</span><span class="sxs-lookup"><span data-stu-id="f9744-110">\[1\]</span></span> | <span data-ttu-id="f9744-111">Identificatore del file installato.</span><span class="sxs-lookup"><span data-stu-id="f9744-111">Identifier of installed file.</span></span>                   |
| <span data-ttu-id="f9744-112">\[6\]</span><span class="sxs-lookup"><span data-stu-id="f9744-112">\[6\]</span></span> | <span data-ttu-id="f9744-113">Dimensioni del file installato in byte.</span><span class="sxs-lookup"><span data-stu-id="f9744-113">Size of installed file in bytes.</span></span>                |
| <span data-ttu-id="f9744-114">\[9\]</span><span class="sxs-lookup"><span data-stu-id="f9744-114">\[9\]</span></span> | <span data-ttu-id="f9744-115">Identificatore della directory che contiene il file installato.</span><span class="sxs-lookup"><span data-stu-id="f9744-115">Identifier of directory holding installed file.</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="f9744-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="f9744-116">Remarks</span></span>

<span data-ttu-id="f9744-117">L'azione InstallFiles opera sui file specificati nella [tabella file](file-table.md).</span><span class="sxs-lookup"><span data-stu-id="f9744-117">The InstallFiles action operates on files specified in the [File table](file-table.md).</span></span> <span data-ttu-id="f9744-118">Ogni file viene installato in base allo stato di installazione del componente associato del file nella [tabella dei componenti](component-table.md).</span><span class="sxs-lookup"><span data-stu-id="f9744-118">Each file is installed based on the installation state of the file's associated component in the [Component table](component-table.md).</span></span> <span data-ttu-id="f9744-119">Solo i file i cui componenti vengono risolti nello stato **msiInstallStatelocal** sono idonei per la copia.</span><span class="sxs-lookup"><span data-stu-id="f9744-119">Only those files whose components are resolved to the **msiInstallStatelocal** state are eligible for copying.</span></span>

<span data-ttu-id="f9744-120">L'azione InstallFiles implementa le colonne seguenti della tabella file.</span><span class="sxs-lookup"><span data-stu-id="f9744-120">The InstallFiles action implements the following columns of the File table.</span></span>

-   <span data-ttu-id="f9744-121">La colonna FileName specifica il nome del file di destinazione.</span><span class="sxs-lookup"><span data-stu-id="f9744-121">The FileName column specifies the target file name.</span></span>
-   <span data-ttu-id="f9744-122">La colonna Version specifica la versione del file.</span><span class="sxs-lookup"><span data-stu-id="f9744-122">The Version column specifies the file version.</span></span>
-   <span data-ttu-id="f9744-123">La colonna attributi specifica i bit del flag dell'attributo di installazione e del file.</span><span class="sxs-lookup"><span data-stu-id="f9744-123">The Attributes column specifies the file and installation attribute flag bits.</span></span>
-   <span data-ttu-id="f9744-124">La colonna file specifica il token del file univoco.</span><span class="sxs-lookup"><span data-stu-id="f9744-124">The File column specifies the unique file token.</span></span>
-   <span data-ttu-id="f9744-125">La colonna Filesize specifica le dimensioni del file non compresso in byte.</span><span class="sxs-lookup"><span data-stu-id="f9744-125">The FileSize column specifies the uncompressed file size in bytes.</span></span>
-   <span data-ttu-id="f9744-126">Nella colonna lingua viene specificato l'identificatore della lingua del file.</span><span class="sxs-lookup"><span data-stu-id="f9744-126">The Language column specifies the file language identifier.</span></span>
-   <span data-ttu-id="f9744-127">Nella colonna sequenza viene specificato il numero di sequenza sui supporti.</span><span class="sxs-lookup"><span data-stu-id="f9744-127">The Sequence column specifies the sequence number on media.</span></span>

<span data-ttu-id="f9744-128">L'azione InstallFiles implementa le colonne seguenti della tabella Component.</span><span class="sxs-lookup"><span data-stu-id="f9744-128">The InstallFiles action implements the following columns of the Component table.</span></span>

-   <span data-ttu-id="f9744-129">Nella \_ colonna directory viene specificato un riferimento a un elemento della [tabella di directory](directory-table.md) .</span><span class="sxs-lookup"><span data-stu-id="f9744-129">The Directory\_ column specifies a reference to a [Directory table](directory-table.md) item.</span></span>
-   <span data-ttu-id="f9744-130">La colonna Component specifica un nome univoco per l'elemento Component.</span><span class="sxs-lookup"><span data-stu-id="f9744-130">The Component column specifies a unique name for the component item.</span></span>

<span data-ttu-id="f9744-131">Il file specificato viene copiato solo se si verifica una delle condizioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="f9744-131">The specified file is copied only if one of the following is true:</span></span>

-   <span data-ttu-id="f9744-132">Il file non è attualmente installato nel computer locale.</span><span class="sxs-lookup"><span data-stu-id="f9744-132">The file is not currently installed on the local computer.</span></span>
-   <span data-ttu-id="f9744-133">Il file si trova nel computer locale, ma ha un numero di versione inferiore a quello del file nella [tabella file](file-table.md).</span><span class="sxs-lookup"><span data-stu-id="f9744-133">The file is on the local computer but has a lower version number than the file in the [File table](file-table.md).</span></span>
-   <span data-ttu-id="f9744-134">Il file si trova nel computer locale, ma non è presente alcun numero di versione associato.</span><span class="sxs-lookup"><span data-stu-id="f9744-134">The file is on the local computer, but there is no associated version number.</span></span>

<span data-ttu-id="f9744-135">La directory di origine per ogni file da copiare è determinata da sourceMode, che a sua volta dipende dal valore nella colonna CAB della tabella media.</span><span class="sxs-lookup"><span data-stu-id="f9744-135">The source directory for each file to be copied is determined by the sourceMode, which in turn depends on the value in the Cabinet column of the Media table.</span></span> <span data-ttu-id="f9744-136">Per una descrizione completa della modalità di origine, vedere la [tabella media](media-table.md).</span><span class="sxs-lookup"><span data-stu-id="f9744-136">For a full discussion of the source mode, see the [Media table](media-table.md).</span></span>

<span data-ttu-id="f9744-137">Se la directory di origine per un file da copiare si trova su un supporto rimovibile, ad esempio un disco floppy o un CD-ROM, l'azione InstallFiles verifica che il supporto di origine appropriato venga inserito prima di tentare di copiare il file.</span><span class="sxs-lookup"><span data-stu-id="f9744-137">If the source directory for a file to be copied resides on removable media such as a floppy disk or CD-ROM, the InstallFiles action verifies that the proper source media is inserted before attempting to copy the file.</span></span> <span data-ttu-id="f9744-138">InstallFiles Cerca i supporti dello stesso tipo rimovibile con un'etichetta di [*volume*](v-gly.md) che corrisponde al valore specificato nella colonna VolumeLabel della tabella media.</span><span class="sxs-lookup"><span data-stu-id="f9744-138">The InstallFiles searches for media of the same removable type with a [*volume*](v-gly.md) label that matches the value given in the VolumeLabel column of the Media table.</span></span> <span data-ttu-id="f9744-139">Se viene trovato un volume montato corrispondente, il processo di copia dei file continua.</span><span class="sxs-lookup"><span data-stu-id="f9744-139">If a matching mounted volume is found, the file copying process proceeds.</span></span> <span data-ttu-id="f9744-140">Se non viene trovata alcuna corrispondenza, una finestra di dialogo richiede all'utente di inserire i supporti appropriati.</span><span class="sxs-lookup"><span data-stu-id="f9744-140">If no match is found, a dialog box requests that the user to insert the proper media.</span></span> <span data-ttu-id="f9744-141">In questo caso, nella finestra di dialogo viene usato il nome del supporto trovato nella colonna DiskPrompt della tabella dei supporti come parte del prompt.</span><span class="sxs-lookup"><span data-stu-id="f9744-141">In this case, the dialog box uses the media name found in the DiskPrompt column of the Media table as part of the prompt.</span></span>

<span data-ttu-id="f9744-142">È necessario prestare attenzione perché l'azione InstallFiles può eliminare un file originale e non sostituirlo.</span><span class="sxs-lookup"><span data-stu-id="f9744-142">Caution must be exercised because the InstallFiles action can delete an original file and not replace it.</span></span> <span data-ttu-id="f9744-143">Questo errore si verifica quando si verifica un errore nell'azione InstallFiles durante la sostituzione di un file precedente e l'utente sceglie di ignorare l'errore.</span><span class="sxs-lookup"><span data-stu-id="f9744-143">This occurs when the InstallFiles action experiences an error while replacing an older file and the user chooses to ignore the error.</span></span> <span data-ttu-id="f9744-144">Il comportamento predefinito del programma di installazione prevede l'eliminazione di un file obsoleto prima di garantire la copia corretta del nuovo file.</span><span class="sxs-lookup"><span data-stu-id="f9744-144">The default behavior of installer is to delete an old file before ensuring the new file is copied correctly.</span></span>

<span data-ttu-id="f9744-145">Per le regole di controllo delle versioni dei file usate dal programma di installazione, vedere [regole di controllo delle versioni dei file](file-versioning-rules.md).</span><span class="sxs-lookup"><span data-stu-id="f9744-145">For the file versioning rules used by the installer, see [File Versioning Rules](file-versioning-rules.md).</span></span>

 

 



