---
description: L'azione DuplicateFiles duplica i file installati dall'azione InstallFiles. I file duplicati possono essere copiati nella stessa directory con un nome diverso o in una directory diversa con il nome originale.
ms.assetid: 51cc0b3f-aa01-4f4d-9a4d-add832698061
title: Azione DuplicateFiles
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 711f6bbd4716beb227dea348826bc302e2f4ba2a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106313353"
---
# <a name="duplicatefiles-action"></a><span data-ttu-id="effc9-104">Azione DuplicateFiles</span><span class="sxs-lookup"><span data-stu-id="effc9-104">DuplicateFiles Action</span></span>

<span data-ttu-id="effc9-105">L'azione DuplicateFiles duplica i file installati dall'azione [InstallFiles](installfiles-action.md) .</span><span class="sxs-lookup"><span data-stu-id="effc9-105">The DuplicateFiles action duplicates files installed by the [InstallFiles](installfiles-action.md) action.</span></span> <span data-ttu-id="effc9-106">I file duplicati possono essere copiati nella stessa directory con un nome diverso o in una directory diversa con il nome originale.</span><span class="sxs-lookup"><span data-stu-id="effc9-106">The duplicate files can be copied to the same directory with a different name or to a different directory with the original name.</span></span>

## <a name="sequence-restrictions"></a><span data-ttu-id="effc9-107">Restrizioni sequenza</span><span class="sxs-lookup"><span data-stu-id="effc9-107">Sequence Restrictions</span></span>

<span data-ttu-id="effc9-108">L'azione DuplicateFiles deve essere successiva all' [azione InstallFiles](installfiles-action.md).</span><span class="sxs-lookup"><span data-stu-id="effc9-108">The DuplicateFiles action must come after the [InstallFiles action](installfiles-action.md).</span></span> <span data-ttu-id="effc9-109">L'azione DuplicateFiles deve anche essere successiva all' [azione PatchFiles](patchfiles-action.md) per impedire la duplicazione della versione senza patch del file.</span><span class="sxs-lookup"><span data-stu-id="effc9-109">The DuplicateFiles Action must also come after the [PatchFiles action](patchfiles-action.md) to prevent duplicating the unpatched version of the file.</span></span>

## <a name="actiondata-messages"></a><span data-ttu-id="effc9-110">Messaggi ActionData</span><span class="sxs-lookup"><span data-stu-id="effc9-110">ActionData Messages</span></span>



| <span data-ttu-id="effc9-111">Campo</span><span class="sxs-lookup"><span data-stu-id="effc9-111">Field</span></span> | <span data-ttu-id="effc9-112">Descrizione dei dati dell'azione</span><span class="sxs-lookup"><span data-stu-id="effc9-112">Description of action data</span></span>                       |
|-------|--------------------------------------------------|
| <span data-ttu-id="effc9-113">\[1\]</span><span class="sxs-lookup"><span data-stu-id="effc9-113">\[1\]</span></span> | <span data-ttu-id="effc9-114">Identificatore del file duplicato.</span><span class="sxs-lookup"><span data-stu-id="effc9-114">Identifier of duplicated file.</span></span>                   |
| <span data-ttu-id="effc9-115">\[6\]</span><span class="sxs-lookup"><span data-stu-id="effc9-115">\[6\]</span></span> | <span data-ttu-id="effc9-116">Dimensioni del file duplicato.</span><span class="sxs-lookup"><span data-stu-id="effc9-116">Size of duplicated file.</span></span>                         |
| <span data-ttu-id="effc9-117">\[9\]</span><span class="sxs-lookup"><span data-stu-id="effc9-117">\[9\]</span></span> | <span data-ttu-id="effc9-118">Identificatore della directory che contiene il file duplicato.</span><span class="sxs-lookup"><span data-stu-id="effc9-118">Identifier of directory holding duplicated file.</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="effc9-119">Commenti</span><span class="sxs-lookup"><span data-stu-id="effc9-119">Remarks</span></span>

<span data-ttu-id="effc9-120">L'azione DuplicateFiles elabora una voce di [tabella DuplicateFile](duplicatefile-table.md) solo se il componente collegato a tale voce viene installato localmente.</span><span class="sxs-lookup"><span data-stu-id="effc9-120">The DuplicateFiles action processes a [DuplicateFile table](duplicatefile-table.md) entry only if the component linked to that entry is being installed locally.</span></span> <span data-ttu-id="effc9-121">Per altre informazioni, vedere [tabella dei componenti](component-table.md).</span><span class="sxs-lookup"><span data-stu-id="effc9-121">For more information, see [Component table](component-table.md).</span></span>

<span data-ttu-id="effc9-122">La stringa nel campo DestFolder è un nome di proprietà il cui valore è previsto per la risoluzione in un percorso completo.</span><span class="sxs-lookup"><span data-stu-id="effc9-122">The string in the DestFolder field is a property name whose value is expected to resolve to a fully qualified path.</span></span> <span data-ttu-id="effc9-123">Questa proprietà può essere qualsiasi voce di directory della tabella di [directory](directory-table.md) , qualsiasi proprietà di cartella predefinita ([**CommonFilesFolder**](commonfilesfolder.md), ad esempio) o una proprietà impostata da qualsiasi voce nella tabella [AppSearch](appsearch-table.md) .</span><span class="sxs-lookup"><span data-stu-id="effc9-123">This property can either be any of the directory entries in the [Directory](directory-table.md) table, any pre-defined folder property ([**CommonFilesFolder**](commonfilesfolder.md), for example), or a property set by any entry in the [AppSearch](appsearch-table.md) table.</span></span> <span data-ttu-id="effc9-124">Se la proprietà **DestFolder** non restituisce un percorso valido, l'azione DuplicateFiles non esegue alcuna operazione per tale voce.</span><span class="sxs-lookup"><span data-stu-id="effc9-124">If the **DestFolder** property does not evaluate to a valid path the DuplicateFiles action does nothing for that entry.</span></span>

<span data-ttu-id="effc9-125">Se il nome del file di destinazione nella colonna destName della tabella DuplicateFile viene lasciato vuoto, il nome del file di destinazione sarà uguale al nome del file originale.</span><span class="sxs-lookup"><span data-stu-id="effc9-125">If the name of the destination file in the DestName column of the DuplicateFile table is left blank, the destination file name will be the same as the original file name.</span></span>

<span data-ttu-id="effc9-126">I file installati dall'azione DuplicateFiles vengono rimossi dall'azione [RemoveDuplicateFiles](removeduplicatefiles-action.md) quando appropriato.</span><span class="sxs-lookup"><span data-stu-id="effc9-126">Files installed by the DuplicateFiles action are removed by the [RemoveDuplicateFiles](removeduplicatefiles-action.md) action when appropriate.</span></span>

 

 



