---
description: La tabella MsiPatchOldAssemblyFile correla un file nella tabella file con un nome di assembly nella tabella MsiPatchOldAssemblyName. È possibile associare più nomi di assembly precedenti a un singolo file.
ms.assetid: a3c1e7fb-5f97-41db-bdc8-bd3ddb695c42
title: Tabella MsiPatchOldAssemblyFile
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c995e4f6d6622dd3d7d1c96c9ef1297a787b66d6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106319006"
---
# <a name="msipatcholdassemblyfile-table"></a><span data-ttu-id="a458b-104">Tabella MsiPatchOldAssemblyFile</span><span class="sxs-lookup"><span data-stu-id="a458b-104">MsiPatchOldAssemblyFile Table</span></span>

<span data-ttu-id="a458b-105">La tabella MsiPatchOldAssemblyFile correla un file nella tabella [file](file-table.md) con un nome di assembly nella [tabella MsiPatchOldAssemblyName](msipatcholdassemblyname-table.md).</span><span class="sxs-lookup"><span data-stu-id="a458b-105">The MsiPatchOldAssemblyFile table relates a file in the [File table](file-table.md) to an assembly name in the [MsiPatchOldAssemblyName table](msipatcholdassemblyname-table.md).</span></span> <span data-ttu-id="a458b-106">È possibile associare più nomi di assembly precedenti a un singolo file.</span><span class="sxs-lookup"><span data-stu-id="a458b-106">Multiple old assembly names can be associated with a single file.</span></span>

<span data-ttu-id="a458b-107">La tabella MsiPatchOldAssemblyFile include le colonne seguenti.</span><span class="sxs-lookup"><span data-stu-id="a458b-107">The MsiPatchOldAssemblyFile table has the following columns.</span></span>



| <span data-ttu-id="a458b-108">Colonna</span><span class="sxs-lookup"><span data-stu-id="a458b-108">Column</span></span>     | <span data-ttu-id="a458b-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="a458b-109">Type</span></span>                         | <span data-ttu-id="a458b-110">Chiave</span><span class="sxs-lookup"><span data-stu-id="a458b-110">Key</span></span> | <span data-ttu-id="a458b-111">Nullable</span><span class="sxs-lookup"><span data-stu-id="a458b-111">Nullable</span></span> |
|------------|------------------------------|-----|----------|
| <span data-ttu-id="a458b-112">file\_</span><span class="sxs-lookup"><span data-stu-id="a458b-112">File\_</span></span>     | [<span data-ttu-id="a458b-113">Identificatore</span><span class="sxs-lookup"><span data-stu-id="a458b-113">Identifier</span></span>](identifier.md) | <span data-ttu-id="a458b-114">S</span><span class="sxs-lookup"><span data-stu-id="a458b-114">Y</span></span>   | <span data-ttu-id="a458b-115">N</span><span class="sxs-lookup"><span data-stu-id="a458b-115">N</span></span>        |
| <span data-ttu-id="a458b-116">Assembly\_</span><span class="sxs-lookup"><span data-stu-id="a458b-116">Assembly\_</span></span> | [<span data-ttu-id="a458b-117">Identificatore</span><span class="sxs-lookup"><span data-stu-id="a458b-117">Identifier</span></span>](identifier.md) | <span data-ttu-id="a458b-118">S</span><span class="sxs-lookup"><span data-stu-id="a458b-118">Y</span></span>   | <span data-ttu-id="a458b-119">N</span><span class="sxs-lookup"><span data-stu-id="a458b-119">N</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="a458b-120">Colonne</span><span class="sxs-lookup"><span data-stu-id="a458b-120">Columns</span></span>

<dl> <dt>

<span data-ttu-id="a458b-121"><span id="File_"></span><span id="file_"></span><span id="FILE_"></span>File\_</span><span class="sxs-lookup"><span data-stu-id="a458b-121"><span id="File_"></span><span id="file_"></span><span id="FILE_"></span>File\_</span></span>
</dt> <dd>

<span data-ttu-id="a458b-122">Chiave esterna per la [tabella file](file-table.md) che specifica l'assembly di cui applicare la patch.</span><span class="sxs-lookup"><span data-stu-id="a458b-122">Foreign key to the [File table](file-table.md) that specifies the assembly to be patched.</span></span> <span data-ttu-id="a458b-123">Questa colonna fa parte della chiave primaria.</span><span class="sxs-lookup"><span data-stu-id="a458b-123">This column is part of the primary key.</span></span>

</dd> <dt>

<span data-ttu-id="a458b-124"><span id="Assembly_"></span><span id="assembly_"></span><span id="ASSEMBLY_"></span>Assembly\_</span><span class="sxs-lookup"><span data-stu-id="a458b-124"><span id="Assembly_"></span><span id="assembly_"></span><span id="ASSEMBLY_"></span>Assembly\_</span></span>
</dt> <dd>

<span data-ttu-id="a458b-125">Chiave esterna per la [tabella MsiPatchOldAssemblyName](msipatcholdassemblyname-table.md) che identifica uno dei nomi degli assembly precedenti per l'assembly.</span><span class="sxs-lookup"><span data-stu-id="a458b-125">Foreign key to the [MsiPatchOldAssemblyName table](msipatcholdassemblyname-table.md) that identifies one of the old assembly names for the assembly.</span></span> <span data-ttu-id="a458b-126">Questa colonna fa parte della chiave primaria.</span><span class="sxs-lookup"><span data-stu-id="a458b-126">This column is part of the primary key.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="a458b-127">Commenti</span><span class="sxs-lookup"><span data-stu-id="a458b-127">Remarks</span></span>

<span data-ttu-id="a458b-128">Windows Installer utilizza la tabella MsiPatchOldAssemblyFile e la [tabella MsiPatchOldAssemblyName](msipatcholdassemblyname-table.md) durante l'applicazione di patch agli assembly installati nella global assembly cache (GAC).</span><span class="sxs-lookup"><span data-stu-id="a458b-128">Windows Installer uses the MsiPatchOldAssemblyFile table and [MsiPatchOldAssemblyName table](msipatcholdassemblyname-table.md) when patching assemblies installed to the Global Assembly Cache (GAC).</span></span> <span data-ttu-id="a458b-129">Quando si rilascia una versione più recente di un assembly, il nome sicuro dell'assembly viene modificato.</span><span class="sxs-lookup"><span data-stu-id="a458b-129">When releasing a newer version of an assembly, the strong name of the assembly is changed.</span></span> <span data-ttu-id="a458b-130">Le due tabelle identificano il nome dell'assembly precedente per un assembly aggiornato.</span><span class="sxs-lookup"><span data-stu-id="a458b-130">The two tables together identify the old assembly name for an updated assembly.</span></span> <span data-ttu-id="a458b-131">Ciò consente al programma di installazione di utilizzare il nome dell'assembly precedente per trovare il file originale nella GAC e applicare una patch binaria.</span><span class="sxs-lookup"><span data-stu-id="a458b-131">This allows the Installer to use the old assembly name to find the original file in the GAC and apply a binary patch.</span></span> <span data-ttu-id="a458b-132">Senza queste informazioni, il programma di installazione potrebbe dover accedere all'origine di installazione originale per applicare la patch a un assembly installato nella GAC.</span><span class="sxs-lookup"><span data-stu-id="a458b-132">Without this information, the installer may have to access the original installation source in order to patch an assembly installed in the GAC.</span></span>

<span data-ttu-id="a458b-133">La tabella MsiPatchOldAssemblyFile e la [tabella MsiPatchOldAssemblyName](msipatcholdassemblyname-table.md) non vengono generate automaticamente da [Patchwiz](patchwiz-dll.md).</span><span class="sxs-lookup"><span data-stu-id="a458b-133">The MsiPatchOldAssemblyFile table and [MsiPatchOldAssemblyName table](msipatcholdassemblyname-table.md) are not generated automatically by [PatchWiz](patchwiz-dll.md).</span></span> <span data-ttu-id="a458b-134">Il pacchetto di aggiornamento specificato nella [tabella UpgradedImages](upgradedimages-table-patchwiz-dll-.md) deve contenere le tabelle per la patch in modo che dispongano di queste informazioni.</span><span class="sxs-lookup"><span data-stu-id="a458b-134">The update package specified in the [UpgradedImages table](upgradedimages-table-patchwiz-dll-.md) is required to contain these tables for the patch to have this information.</span></span>

## <a name="validation"></a><span data-ttu-id="a458b-135">Convalida</span><span class="sxs-lookup"><span data-stu-id="a458b-135">Validation</span></span>

<dl>

[<span data-ttu-id="a458b-136">ICE03</span><span class="sxs-lookup"><span data-stu-id="a458b-136">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="a458b-137">ICE06</span><span class="sxs-lookup"><span data-stu-id="a458b-137">ICE06</span></span>](ice06.md)  
[<span data-ttu-id="a458b-138">ICE32</span><span class="sxs-lookup"><span data-stu-id="a458b-138">ICE32</span></span>](ice32.md)  
</dl>

 

 



