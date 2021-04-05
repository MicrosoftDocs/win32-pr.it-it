---
description: L'azione RemoveDuplicateFiles Elimina i file installati dall'azione DuplicateFiles.
ms.assetid: 3d8ba4c5-775f-471e-a479-32fa6f7a1bf0
title: Azione RemoveDuplicateFiles
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 555379f3810770abc9f91fd449e71434e9fa6244
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103751122"
---
# <a name="removeduplicatefiles-action"></a><span data-ttu-id="7d00d-103">Azione RemoveDuplicateFiles</span><span class="sxs-lookup"><span data-stu-id="7d00d-103">RemoveDuplicateFiles Action</span></span>

<span data-ttu-id="7d00d-104">L'azione RemoveDuplicateFiles Elimina i file installati dall'azione [DuplicateFiles](duplicatefiles-action.md) .</span><span class="sxs-lookup"><span data-stu-id="7d00d-104">The RemoveDuplicateFiles action deletes files installed by the [DuplicateFiles](duplicatefiles-action.md) action.</span></span>

## <a name="sequence-restrictions"></a><span data-ttu-id="7d00d-105">Restrizioni sequenza</span><span class="sxs-lookup"><span data-stu-id="7d00d-105">Sequence Restrictions</span></span>

<span data-ttu-id="7d00d-106">L'azione RemoveDuplicateFiles deve essere eseguita dopo l'azione [InstallValidate](installvalidate-action.md) e prima dell'azione [InstallFiles](installfiles-action.md) .</span><span class="sxs-lookup"><span data-stu-id="7d00d-106">The RemoveDuplicateFiles action must occur after the [InstallValidate](installvalidate-action.md) action and before the [InstallFiles](installfiles-action.md) action.</span></span>

## <a name="actiondata-messages"></a><span data-ttu-id="7d00d-107">Messaggi ActionData</span><span class="sxs-lookup"><span data-stu-id="7d00d-107">ActionData Messages</span></span>



| <span data-ttu-id="7d00d-108">Campo</span><span class="sxs-lookup"><span data-stu-id="7d00d-108">Field</span></span> | <span data-ttu-id="7d00d-109">Descrizione dei dati dell'azione</span><span class="sxs-lookup"><span data-stu-id="7d00d-109">Description of action data</span></span>                    |
|-------|-----------------------------------------------|
| <span data-ttu-id="7d00d-110">\[1\]</span><span class="sxs-lookup"><span data-stu-id="7d00d-110">\[1\]</span></span> | <span data-ttu-id="7d00d-111">Identificatore del file rimosso.</span><span class="sxs-lookup"><span data-stu-id="7d00d-111">Identifier of removed file.</span></span>                   |
| <span data-ttu-id="7d00d-112">\[9\]</span><span class="sxs-lookup"><span data-stu-id="7d00d-112">\[9\]</span></span> | <span data-ttu-id="7d00d-113">Identificatore della directory che contiene il file rimosso.</span><span class="sxs-lookup"><span data-stu-id="7d00d-113">Identifier of directory holding removed file.</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="7d00d-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="7d00d-114">Remarks</span></span>

<span data-ttu-id="7d00d-115">Per eliminare un file duplicato con l' [azione DuplicateFiles](duplicatefiles-action.md) usando l'azione RemoveDuplicateFiles, è necessario selezionare per la rimozione il componente associato alla voce del file nella tabella DuplicateFile.</span><span class="sxs-lookup"><span data-stu-id="7d00d-115">To delete a file duplicated with the [DuplicateFiles action](duplicatefiles-action.md) using the RemoveDuplicateFiles action, the component associated with the file's entry in the DuplicateFile table must be selected for removal.</span></span>

<span data-ttu-id="7d00d-116">Utilizzare la colonna DestFolder della [tabella DuplicateFile](duplicatefile-table.md) per specificare il nome della proprietà il cui valore identifica la cartella di destinazione.</span><span class="sxs-lookup"><span data-stu-id="7d00d-116">Use the DestFolder column of the [DuplicateFile table](duplicatefile-table.md) to specify the property name whose value identifies the destination folder.</span></span>

 

 



