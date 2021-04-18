---
description: La tabella UpgradedFilesToIgnore impedisce l'aggiornamento di file specifici che sono in effetti modificati nell'immagine aggiornata rispetto alle immagini di destinazione.
ms.assetid: 3b5f4360-887a-4a21-8f16-faa84da34328
title: Tabella UpgradedFilesToIgnore (Patchwiz.dll)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8f4a235759251ac3dadbe01b030c0d984d1f66b9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106318272"
---
# <a name="upgradedfilestoignore-table-patchwizdll"></a><span data-ttu-id="3a95a-103">Tabella UpgradedFilesToIgnore (Patchwiz.dll)</span><span class="sxs-lookup"><span data-stu-id="3a95a-103">UpgradedFilesToIgnore Table (Patchwiz.dll)</span></span>

<span data-ttu-id="3a95a-104">La tabella UpgradedFilesToIgnore impedisce l'aggiornamento di file specifici che sono in effetti modificati nell'immagine aggiornata rispetto alle immagini di destinazione.</span><span class="sxs-lookup"><span data-stu-id="3a95a-104">The UpgradedFilesToIgnore table prevents the updating of specific files that are in fact changed in the upgraded image relative to the target images.</span></span> <span data-ttu-id="3a95a-105">In alcuni casi può essere utile eseguire questa operazione.</span><span class="sxs-lookup"><span data-stu-id="3a95a-105">It may be useful to do this in certain cases.</span></span> <span data-ttu-id="3a95a-106">Ad esempio, un pacchetto di patch progettato solo per l'utilizzo con installazioni non amministrative non deve includere file di patch che fanno parte solo di immagini amministrative.</span><span class="sxs-lookup"><span data-stu-id="3a95a-106">For example, a patch package intended only for use with non-administrative installations does not need to include patching files that are only part of administrative images.</span></span> <span data-ttu-id="3a95a-107">Escludendo tali file utilizzati solo nelle immagini amministrative è possibile ridurre le dimensioni del pacchetto di patch. Tuttavia, gli amministratori devono essere informati su come aggiornare i file separatamente.</span><span class="sxs-lookup"><span data-stu-id="3a95a-107">Excluding such files used only in administrative images can reduce the size of the patch package; however, administrators should be informed on how to update these files separately.</span></span> <span data-ttu-id="3a95a-108">Questa tabella è facoltativa nel database di creazione della patch (file con estensione PCP) e viene usata dalla funzione [UiCreatePatchPackageEx](uicreatepatchpackageex--patchwiz-dll-.md) .</span><span class="sxs-lookup"><span data-stu-id="3a95a-108">This table is optional in the patch creation database (.pcp file) and is used by the [UiCreatePatchPackageEx](uicreatepatchpackageex--patchwiz-dll-.md) function.</span></span>

<span data-ttu-id="3a95a-109">La tabella UpgradedFilesToIgnore include le colonne seguenti.</span><span class="sxs-lookup"><span data-stu-id="3a95a-109">The UpgradedFilesToIgnore table has the following columns.</span></span>



| <span data-ttu-id="3a95a-110">Colonna</span><span class="sxs-lookup"><span data-stu-id="3a95a-110">Column</span></span>   | <span data-ttu-id="3a95a-111">Tipo</span><span class="sxs-lookup"><span data-stu-id="3a95a-111">Type</span></span> | <span data-ttu-id="3a95a-112">Chiave</span><span class="sxs-lookup"><span data-stu-id="3a95a-112">Key</span></span> | <span data-ttu-id="3a95a-113">Nullable</span><span class="sxs-lookup"><span data-stu-id="3a95a-113">Nullable</span></span> |
|----------|------|-----|----------|
| <span data-ttu-id="3a95a-114">Aggiornato</span><span class="sxs-lookup"><span data-stu-id="3a95a-114">Upgraded</span></span> | <span data-ttu-id="3a95a-115">text</span><span class="sxs-lookup"><span data-stu-id="3a95a-115">text</span></span> | <span data-ttu-id="3a95a-116">S</span><span class="sxs-lookup"><span data-stu-id="3a95a-116">Y</span></span>   | <span data-ttu-id="3a95a-117">N</span><span class="sxs-lookup"><span data-stu-id="3a95a-117">N</span></span>        |
| <span data-ttu-id="3a95a-118">FTK</span><span class="sxs-lookup"><span data-stu-id="3a95a-118">FTK</span></span>      | <span data-ttu-id="3a95a-119">text</span><span class="sxs-lookup"><span data-stu-id="3a95a-119">text</span></span> | <span data-ttu-id="3a95a-120">S</span><span class="sxs-lookup"><span data-stu-id="3a95a-120">Y</span></span>   | <span data-ttu-id="3a95a-121">N</span><span class="sxs-lookup"><span data-stu-id="3a95a-121">N</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="3a95a-122">Colonne</span><span class="sxs-lookup"><span data-stu-id="3a95a-122">Columns</span></span>

<dl> <dt>

<span data-ttu-id="3a95a-123"><span id="Upgraded"></span><span id="upgraded"></span><span id="UPGRADED"></span>Aggiornato</span><span class="sxs-lookup"><span data-stu-id="3a95a-123"><span id="Upgraded"></span><span id="upgraded"></span><span id="UPGRADED"></span>Upgraded</span></span>
</dt> <dd>

<span data-ttu-id="3a95a-124">Chiave esterna per la colonna aggiornata della [tabella UpgradedImages (Patchwiz.dll)](upgradedimages-table-patchwiz-dll-.md).</span><span class="sxs-lookup"><span data-stu-id="3a95a-124">Foreign key to the Upgraded column of the [UpgradedImages Table (Patchwiz.dll)](upgradedimages-table-patchwiz-dll-.md).</span></span> <span data-ttu-id="3a95a-125">Lo strumento di creazione della patch esclude l'aggiornamento del file specificato nella colonna FTK della tabella UpgradedFilesToIgnore durante l'aggiornamento di una destinazione all'immagine specificata nel campo aggiornato.</span><span class="sxs-lookup"><span data-stu-id="3a95a-125">The patch creation tool excludes updating the file specified in the FTK column of the UpgradedFilesToIgnore table when upgrading a target to the image specified in the Upgraded field.</span></span> <span data-ttu-id="3a95a-126">Immettere il valore " \* " nel campo aggiornato per escludere l'aggiornamento del file per tutte le immagini aggiornate.</span><span class="sxs-lookup"><span data-stu-id="3a95a-126">Enter a value of "\*" in the Upgraded field to exclude updating the file for all upgraded images.</span></span>

</dd> <dt>

<span data-ttu-id="3a95a-127"><span id="FTK"></span><span id="ftk"></span>FTK</span><span class="sxs-lookup"><span data-stu-id="3a95a-127"><span id="FTK"></span><span id="ftk"></span>FTK</span></span>
</dt> <dd>

<span data-ttu-id="3a95a-128">Chiave esterna nella [tabella file](file-table.md) dell'immagine aggiornata.</span><span class="sxs-lookup"><span data-stu-id="3a95a-128">Foreign key into the [File table](file-table.md) of the upgraded image.</span></span> <span data-ttu-id="3a95a-129">Un valore nel formato " <prefix> \* " corrisponde a tutte le chiavi della tabella file nella tabella file che iniziano con tale prefisso.</span><span class="sxs-lookup"><span data-stu-id="3a95a-129">A value of the form "<prefix>\*" matches all file table keys in the File table that begin with that prefix.</span></span> <span data-ttu-id="3a95a-130">Nessun testo può seguire l'asterisco.</span><span class="sxs-lookup"><span data-stu-id="3a95a-130">No text can follow the asterisk.</span></span>

</dd> </dl>

 

 



