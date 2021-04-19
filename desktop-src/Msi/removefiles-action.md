---
description: L'azione RemoveFiles rimuove i file precedentemente installati dall'azione InstallFiles.
ms.assetid: 1079be89-515c-443e-8927-46ddf7891a59
title: Azione RemoveFiles
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 174e477d512401c8ff6f1ff091b7c67f26e86f16
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106314780"
---
# <a name="removefiles-action"></a><span data-ttu-id="b5eb6-103">Azione RemoveFiles</span><span class="sxs-lookup"><span data-stu-id="b5eb6-103">RemoveFiles Action</span></span>

<span data-ttu-id="b5eb6-104">L'azione RemoveFiles rimuove i file precedentemente installati dall'azione [InstallFiles](installfiles-action.md) .</span><span class="sxs-lookup"><span data-stu-id="b5eb6-104">The RemoveFiles action removes files previously installed by the [InstallFiles](installfiles-action.md) action.</span></span> <span data-ttu-id="b5eb6-105">Ognuno di questi file è gestito da un collegamento a una voce nella tabella dei [componenti](component-table.md) .</span><span class="sxs-lookup"><span data-stu-id="b5eb6-105">Each of these files is gated by a link to an entry in the [Component](component-table.md) table.</span></span> <span data-ttu-id="b5eb6-106">Solo i file con componenti risolti nello stato *msiInstallStateAbsent* o *msiInstallStateLocal* se il componente è installato localmente, vengono rimossi.</span><span class="sxs-lookup"><span data-stu-id="b5eb6-106">Only those files with components resolved to either the *msiInstallStateAbsent* state or the *msiInstallStateLocal* state if the component is installed locally, are removed.</span></span>

## <a name="sequence-restrictions"></a><span data-ttu-id="b5eb6-107">Restrizioni sequenza</span><span class="sxs-lookup"><span data-stu-id="b5eb6-107">Sequence Restrictions</span></span>

<span data-ttu-id="b5eb6-108">L'azione [InstallValidate](installvalidate-action.md) deve essere chiamata prima di chiamare RemoveFiles.</span><span class="sxs-lookup"><span data-stu-id="b5eb6-108">The [InstallValidate](installvalidate-action.md) action must be called before calling RemoveFiles.</span></span> <span data-ttu-id="b5eb6-109">Se viene usata un'azione [InstallFiles](installfiles-action.md) , deve essere visualizzata dopo RemoveFiles.</span><span class="sxs-lookup"><span data-stu-id="b5eb6-109">If an [InstallFiles](installfiles-action.md) action is used, it must appear after RemoveFiles.</span></span>

## <a name="actiondata-messages"></a><span data-ttu-id="b5eb6-110">Messaggi ActionData</span><span class="sxs-lookup"><span data-stu-id="b5eb6-110">ActionData Messages</span></span>



| <span data-ttu-id="b5eb6-111">Campo</span><span class="sxs-lookup"><span data-stu-id="b5eb6-111">Field</span></span> | <span data-ttu-id="b5eb6-112">Descrizione dei dati dell'azione</span><span class="sxs-lookup"><span data-stu-id="b5eb6-112">Description of action data</span></span>                    |
|-------|-----------------------------------------------|
| <span data-ttu-id="b5eb6-113">\[1\]</span><span class="sxs-lookup"><span data-stu-id="b5eb6-113">\[1\]</span></span> | <span data-ttu-id="b5eb6-114">Identificatore del file rimosso.</span><span class="sxs-lookup"><span data-stu-id="b5eb6-114">Identifier of removed file.</span></span>                   |
| <span data-ttu-id="b5eb6-115">\[9\]</span><span class="sxs-lookup"><span data-stu-id="b5eb6-115">\[9\]</span></span> | <span data-ttu-id="b5eb6-116">Identificatore della directory che contiene il file rimosso.</span><span class="sxs-lookup"><span data-stu-id="b5eb6-116">Identifier of directory holding removed file.</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="b5eb6-117">Commenti</span><span class="sxs-lookup"><span data-stu-id="b5eb6-117">Remarks</span></span>

<span data-ttu-id="b5eb6-118">La tabella [RemoveFile](removefile-table.md) può essere omessa dal database del programma di installazione se non sono presenti file esterni da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="b5eb6-118">The [RemoveFile](removefile-table.md) table can be omitted from the installer database if there are no miscellaneous files to remove.</span></span>

<span data-ttu-id="b5eb6-119">L'azione RemoveFiles può anche rimuovere i file specificati dall'autore che non sono installati dall'azione InstallFiles.</span><span class="sxs-lookup"><span data-stu-id="b5eb6-119">The RemoveFiles action can also remove author-specified files that are not installed by the InstallFiles action.</span></span> <span data-ttu-id="b5eb6-120">Questi file sono specificati nella tabella [RemoveFile](removefile-table.md) .</span><span class="sxs-lookup"><span data-stu-id="b5eb6-120">These files are specified in the [RemoveFile](removefile-table.md) table.</span></span> <span data-ttu-id="b5eb6-121">Ognuno di questi file è gestito da un collegamento a una voce nella tabella dei [componenti](component-table.md) .</span><span class="sxs-lookup"><span data-stu-id="b5eb6-121">Each of these files is gated by a link to an entry in the [Component](component-table.md) table.</span></span> <span data-ttu-id="b5eb6-122">Se il file è presente nella directory specificata, i file i cui componenti vengono risolti in uno stato di azione attivo (ovvero non in stato disattivato o null) vengono rimossi.</span><span class="sxs-lookup"><span data-stu-id="b5eb6-122">Those files whose components are resolved to any active Action state (that is, not in the Off or Null state) are removed if the file exists in the specified directory.</span></span> <span data-ttu-id="b5eb6-123">La rimozione dei file specificati nella tabella RemoveFile viene tentata quando il componente collegato viene installato per la prima volta, durante una reinstallazione e nuovamente quando il componente collegato viene rimosso.</span><span class="sxs-lookup"><span data-stu-id="b5eb6-123">The removal of files specified in the RemoveFile table is attempted when the linked component is first installed, during a reinstall, and again when the linked component is removed.</span></span>

<span data-ttu-id="b5eb6-124">L'azione RemoveFiles consente inoltre di rimuovere le cartelle.</span><span class="sxs-lookup"><span data-stu-id="b5eb6-124">The RemoveFiles action can also remove folders.</span></span> <span data-ttu-id="b5eb6-125">Se il valore nella colonna FileName della tabella RemoveFile è null, viene rimossa una cartella vuota.</span><span class="sxs-lookup"><span data-stu-id="b5eb6-125">An empty folder is removed if the value in the FileName column of the RemoveFile table is null.</span></span>

<span data-ttu-id="b5eb6-126">Quando si rimuovono i file installati in precedenza, l'azione RemoveFiles esegue una query sugli stessi campi nelle stesse tabelle di quelli sottoposti a query dall'azione [InstallFiles](installfiles-action.md) , con l'eccezione che la [tabella supporti](media-table.md) non viene utilizzata dall'azione RemoveFiles.</span><span class="sxs-lookup"><span data-stu-id="b5eb6-126">When removing previously installed files, the RemoveFiles action queries the same fields in the same tables as those queried by the [InstallFiles](installfiles-action.md) action with the exception that the [Media table](media-table.md) is not used by the RemoveFiles action.</span></span>

<span data-ttu-id="b5eb6-127">Il nome del file di destinazione può essere specificato nel testo localizzato nella colonna FileName della tabella RemoveFile.</span><span class="sxs-lookup"><span data-stu-id="b5eb6-127">The target file name can be specified in localized text in the FileName column of the RemoveFile table.</span></span>

 

 



