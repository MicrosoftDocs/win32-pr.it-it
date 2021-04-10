---
description: L'azione AppSearch usa le firme file per cercare le versioni esistenti dei prodotti.
ms.assetid: 56665876-2c74-476b-aa1a-158c6e86418d
title: Azione AppSearch
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 04187fb146af80839e135c99986dea1902ccb6b9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104227212"
---
# <a name="appsearch-action"></a><span data-ttu-id="6d188-103">Azione AppSearch</span><span class="sxs-lookup"><span data-stu-id="6d188-103">AppSearch Action</span></span>

<span data-ttu-id="6d188-104">L'azione AppSearch usa le firme file per cercare le versioni esistenti dei prodotti.</span><span class="sxs-lookup"><span data-stu-id="6d188-104">The AppSearch action uses file signatures to search for existing versions of products.</span></span> <span data-ttu-id="6d188-105">L'azione AppSearch può utilizzare queste informazioni per determinare la posizione in cui installare gli aggiornamenti.</span><span class="sxs-lookup"><span data-stu-id="6d188-105">The AppSearch action may use this information to determine where upgrades are to be installed.</span></span> <span data-ttu-id="6d188-106">L'azione AppSearch può essere utilizzata anche per impostare una proprietà sul valore esistente di una voce del registro di sistema o di un file ini.</span><span class="sxs-lookup"><span data-stu-id="6d188-106">The AppSearch action can also be used to set a property to the existing value of an registry or .ini file entry.</span></span>

## <a name="sequence-restrictions"></a><span data-ttu-id="6d188-107">Restrizioni sequenza</span><span class="sxs-lookup"><span data-stu-id="6d188-107">Sequence Restrictions</span></span>

<span data-ttu-id="6d188-108">AppSearch deve essere creato nella [tabella InstallUISequence](installuisequence-table.md) e nella [tabella InstallExecuteSequence](installexecutesequence-table.md).</span><span class="sxs-lookup"><span data-stu-id="6d188-108">AppSearch should be authored into the [InstallUISequence table](installuisequence-table.md) and [InstallExecuteSequence table](installexecutesequence-table.md).</span></span> <span data-ttu-id="6d188-109">Il programma di installazione impedisce l'esecuzione dell'azione AppSearch nella sequenza InstallExecuteSequence se l'azione è già stata eseguita nella sequenza InstallUISequence.</span><span class="sxs-lookup"><span data-stu-id="6d188-109">The installer prevents the AppSearch action from running in the InstallExecuteSequence sequence if the action has already run in InstallUISequence sequence.</span></span>

## <a name="actiondata-messages"></a><span data-ttu-id="6d188-110">Messaggi ActionData</span><span class="sxs-lookup"><span data-stu-id="6d188-110">ActionData Messages</span></span>



| <span data-ttu-id="6d188-111">Campo</span><span class="sxs-lookup"><span data-stu-id="6d188-111">Field</span></span> | <span data-ttu-id="6d188-112">Descrizione dei dati dell'azione</span><span class="sxs-lookup"><span data-stu-id="6d188-112">Description of action data</span></span>      |
|-------|---------------------------------|
| <span data-ttu-id="6d188-113">\[1\]</span><span class="sxs-lookup"><span data-stu-id="6d188-113">\[1\]</span></span> | <span data-ttu-id="6d188-114">Proprietà che contiene il percorso del file.</span><span class="sxs-lookup"><span data-stu-id="6d188-114">Property holding file location.</span></span> |
| <span data-ttu-id="6d188-115">\[2\]</span><span class="sxs-lookup"><span data-stu-id="6d188-115">\[2\]</span></span> | <span data-ttu-id="6d188-116">Firma del file.</span><span class="sxs-lookup"><span data-stu-id="6d188-116">File signature.</span></span>                 |



 

## <a name="remarks"></a><span data-ttu-id="6d188-117">Commenti</span><span class="sxs-lookup"><span data-stu-id="6d188-117">Remarks</span></span>

<span data-ttu-id="6d188-118">Per l'azione AppSearch è necessario che la tabella [Signature](signature-table.md) sia presente nel pacchetto di installazione.</span><span class="sxs-lookup"><span data-stu-id="6d188-118">The AppSearch action requires that the [Signature](signature-table.md) table be present in the installation package.</span></span> <span data-ttu-id="6d188-119">Le firme dei file sono elencate nella tabella della firma.</span><span class="sxs-lookup"><span data-stu-id="6d188-119">File signatures are listed in the Signature table.</span></span> <span data-ttu-id="6d188-120">Una firma che non è presente nella tabella delle firme indica una directory e l'azione imposta la proprietà sul percorso di directory per la firma.</span><span class="sxs-lookup"><span data-stu-id="6d188-120">A signature that is not in the Signature table denotes a directory and the action sets the property to the directory path for that signature.</span></span>

<span data-ttu-id="6d188-121">L'azione AppSearch Cerca le firme dei file usando prima la tabella [CompLocator](complocator-table.md) , la tabella [RegLocator](reglocator-table.md) avanti, quindi la tabella [IniLocator](inilocator-table.md) e infine la tabella [DrLocator](drlocator-table.md) .</span><span class="sxs-lookup"><span data-stu-id="6d188-121">The AppSearch action searches for file signatures using the [CompLocator](complocator-table.md) table first, the [RegLocator](reglocator-table.md) table next, then the [IniLocator](inilocator-table.md) table, and finally the [DrLocator](drlocator-table.md) table.</span></span>

## <a name="related-topics"></a><span data-ttu-id="6d188-122">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="6d188-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6d188-123">AppSearch</span><span class="sxs-lookup"><span data-stu-id="6d188-123">AppSearch</span></span>](appsearch-table.md)
</dt> <dt>

[<span data-ttu-id="6d188-124">CompLocator</span><span class="sxs-lookup"><span data-stu-id="6d188-124">CompLocator</span></span>](complocator-table.md)
</dt> <dt>

[<span data-ttu-id="6d188-125">IniLocator</span><span class="sxs-lookup"><span data-stu-id="6d188-125">IniLocator</span></span>](inilocator-table.md)
</dt> <dt>

[<span data-ttu-id="6d188-126">RegLocator</span><span class="sxs-lookup"><span data-stu-id="6d188-126">RegLocator</span></span>](reglocator-table.md)
</dt> <dt>

[<span data-ttu-id="6d188-127">DrLocator</span><span class="sxs-lookup"><span data-stu-id="6d188-127">DrLocator</span></span>](drlocator-table.md)
</dt> </dl>

 

 



