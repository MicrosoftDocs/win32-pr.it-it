---
description: La tabella MsiPatchOldAssemblyName specifica il nome precedente di un assembly.
ms.assetid: e9f22ba1-6be4-4382-abe5-5cfdc68c0855
title: Tabella MsiPatchOldAssemblyName
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ee301801efc1618f84794c48172aff47734b38d9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104347346"
---
# <a name="msipatcholdassemblyname-table"></a><span data-ttu-id="85d9d-103">Tabella MsiPatchOldAssemblyName</span><span class="sxs-lookup"><span data-stu-id="85d9d-103">MsiPatchOldAssemblyName Table</span></span>

<span data-ttu-id="85d9d-104">La tabella MsiPatchOldAssemblyName specifica il nome precedente di un assembly.</span><span class="sxs-lookup"><span data-stu-id="85d9d-104">The MsiPatchOldAssemblyName table specifies the old name for an assembly.</span></span>

<span data-ttu-id="85d9d-105">La tabella MsiPatchOldAssemblyName include le colonne seguenti.</span><span class="sxs-lookup"><span data-stu-id="85d9d-105">The MsiPatchOldAssemblyName table has the following columns.</span></span>



| <span data-ttu-id="85d9d-106">Colonna</span><span class="sxs-lookup"><span data-stu-id="85d9d-106">Column</span></span>   | <span data-ttu-id="85d9d-107">Tipo</span><span class="sxs-lookup"><span data-stu-id="85d9d-107">Type</span></span>                         | <span data-ttu-id="85d9d-108">Chiave</span><span class="sxs-lookup"><span data-stu-id="85d9d-108">Key</span></span> | <span data-ttu-id="85d9d-109">Nullable</span><span class="sxs-lookup"><span data-stu-id="85d9d-109">Nullable</span></span> |
|----------|------------------------------|-----|----------|
| <span data-ttu-id="85d9d-110">Assembly</span><span class="sxs-lookup"><span data-stu-id="85d9d-110">Assembly</span></span> | [<span data-ttu-id="85d9d-111">Identificatore</span><span class="sxs-lookup"><span data-stu-id="85d9d-111">Identifier</span></span>](identifier.md) | <span data-ttu-id="85d9d-112">S</span><span class="sxs-lookup"><span data-stu-id="85d9d-112">Y</span></span>   | <span data-ttu-id="85d9d-113">N</span><span class="sxs-lookup"><span data-stu-id="85d9d-113">N</span></span>        |
| <span data-ttu-id="85d9d-114">Nome</span><span class="sxs-lookup"><span data-stu-id="85d9d-114">Name</span></span>     | [<span data-ttu-id="85d9d-115">Text</span><span class="sxs-lookup"><span data-stu-id="85d9d-115">Text</span></span>](text.md)             | <span data-ttu-id="85d9d-116">S</span><span class="sxs-lookup"><span data-stu-id="85d9d-116">Y</span></span>   | <span data-ttu-id="85d9d-117">N</span><span class="sxs-lookup"><span data-stu-id="85d9d-117">N</span></span>        |
| <span data-ttu-id="85d9d-118">Valore</span><span class="sxs-lookup"><span data-stu-id="85d9d-118">Value</span></span>    | [<span data-ttu-id="85d9d-119">Text</span><span class="sxs-lookup"><span data-stu-id="85d9d-119">Text</span></span>](text.md)             | <span data-ttu-id="85d9d-120">N</span><span class="sxs-lookup"><span data-stu-id="85d9d-120">N</span></span>   | <span data-ttu-id="85d9d-121">N</span><span class="sxs-lookup"><span data-stu-id="85d9d-121">N</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="85d9d-122">Colonne</span><span class="sxs-lookup"><span data-stu-id="85d9d-122">Columns</span></span>

<dl> <dt>

<span data-ttu-id="85d9d-123"><span id="Assembly"></span><span id="assembly"></span><span id="ASSEMBLY"></span>Assembly</span><span class="sxs-lookup"><span data-stu-id="85d9d-123"><span id="Assembly"></span><span id="assembly"></span><span id="ASSEMBLY"></span>Assembly</span></span>
</dt> <dd>

<span data-ttu-id="85d9d-124">Identificatore univoco per il vecchio nome dell'assembly.</span><span class="sxs-lookup"><span data-stu-id="85d9d-124">Unique identifier for the old assembly name.</span></span> <span data-ttu-id="85d9d-125">Questa chiave viene utilizzata come mapping tra questa e la [tabella MsiPatchOldAssemblyFile](msipatcholdassemblyfile-table.md).</span><span class="sxs-lookup"><span data-stu-id="85d9d-125">This key is used as a mapping between this and the [MsiPatchOldAssemblyFile table](msipatcholdassemblyfile-table.md).</span></span>

</dd> <dt>

<span data-ttu-id="85d9d-126"><span id="Name"></span><span id="name"></span><span id="NAME"></span>Nome</span><span class="sxs-lookup"><span data-stu-id="85d9d-126"><span id="Name"></span><span id="name"></span><span id="NAME"></span>Name</span></span>
</dt> <dd>

<span data-ttu-id="85d9d-127">Nome dell'attributo associato al valore specificato nella colonna valore.</span><span class="sxs-lookup"><span data-stu-id="85d9d-127">Name of the attribute associated with the value specified in the Value column.</span></span>

</dd> <dt>

<span data-ttu-id="85d9d-128"><span id="Value"></span><span id="value"></span><span id="VALUE"></span>Valore</span><span class="sxs-lookup"><span data-stu-id="85d9d-128"><span id="Value"></span><span id="value"></span><span id="VALUE"></span>Value</span></span>
</dt> <dd>

<span data-ttu-id="85d9d-129">Valore associato al nome specificato nella colonna Name.</span><span class="sxs-lookup"><span data-stu-id="85d9d-129">Value associated with the name specified in the Name column.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="85d9d-130">Commenti</span><span class="sxs-lookup"><span data-stu-id="85d9d-130">Remarks</span></span>

<span data-ttu-id="85d9d-131">Windows Installer utilizza la tabella [MsiPatchOldAssemblyFile](msipatcholdassemblyfile-table.md) e la tabella MsiPatchOldAssemblyName durante l'applicazione di patch agli assembly installati nella global assembly cache (GAC).</span><span class="sxs-lookup"><span data-stu-id="85d9d-131">Windows Installer uses the [MsiPatchOldAssemblyFile table](msipatcholdassemblyfile-table.md) and MsiPatchOldAssemblyName table when patching assemblies installed to the Global Assembly Cache (GAC).</span></span> <span data-ttu-id="85d9d-132">Quando si rilascia una versione più recente di un assembly, il nome sicuro dell'assembly viene modificato.</span><span class="sxs-lookup"><span data-stu-id="85d9d-132">When releasing a newer version of an assembly, the strong name of the assembly is changed.</span></span> <span data-ttu-id="85d9d-133">Le due tabelle identificano il nome dell'assembly precedente per un assembly aggiornato.</span><span class="sxs-lookup"><span data-stu-id="85d9d-133">The two tables together identify the old assembly name for an updated assembly.</span></span> <span data-ttu-id="85d9d-134">Ciò consente al programma di installazione di utilizzare il nome dell'assembly precedente per trovare il file originale nella GAC e applicare una patch binaria.</span><span class="sxs-lookup"><span data-stu-id="85d9d-134">This allows the Installer to use the old assembly name to find the original file in the GAC and apply a binary patch.</span></span> <span data-ttu-id="85d9d-135">Senza queste informazioni, il programma di installazione potrebbe dover accedere all'origine di installazione originale per applicare la patch a un assembly installato nella GAC.</span><span class="sxs-lookup"><span data-stu-id="85d9d-135">Without this information, the installer may have to access the original installation source in order to patch an assembly installed in the GAC.</span></span>

<span data-ttu-id="85d9d-136">La [tabella MsiPatchOldAssemblyFile](msipatcholdassemblyfile-table.md) e la tabella MsiPatchOldAssemblyName non vengono generate automaticamente da [Patchwiz](patchwiz-dll.md).</span><span class="sxs-lookup"><span data-stu-id="85d9d-136">The [MsiPatchOldAssemblyFile table](msipatcholdassemblyfile-table.md) and MsiPatchOldAssemblyName table are not generated automatically by [PatchWiz](patchwiz-dll.md).</span></span> <span data-ttu-id="85d9d-137">Il pacchetto di aggiornamento specificato nella [tabella UpgradedImages](upgradedimages-table-patchwiz-dll-.md) deve contenere le tabelle per la patch in modo che dispongano di queste informazioni.</span><span class="sxs-lookup"><span data-stu-id="85d9d-137">The update package specified in the [UpgradedImages table](upgradedimages-table-patchwiz-dll-.md) is required to contain these tables for the patch to have this information.</span></span>

## <a name="validation"></a><span data-ttu-id="85d9d-138">Convalida</span><span class="sxs-lookup"><span data-stu-id="85d9d-138">Validation</span></span>

<dl>

[<span data-ttu-id="85d9d-139">ICE03</span><span class="sxs-lookup"><span data-stu-id="85d9d-139">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="85d9d-140">ICE06</span><span class="sxs-lookup"><span data-stu-id="85d9d-140">ICE06</span></span>](ice06.md)  
[<span data-ttu-id="85d9d-141">ICE32</span><span class="sxs-lookup"><span data-stu-id="85d9d-141">ICE32</span></span>](ice32.md)  
</dl>

 

 



