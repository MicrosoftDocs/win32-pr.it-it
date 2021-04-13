---
description: La tabella UpgradedImages contiene informazioni sulle immagini aggiornate del prodotto.
ms.assetid: f4ee2cc8-8a49-4e4a-b8cf-b4ae2bc7e753
title: Tabella UpgradedImages (Patchwiz.dll)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 48dcecc94786cbe783f21e6e005b645586f2e894
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104348956"
---
# <a name="upgradedimages-table-patchwizdll"></a><span data-ttu-id="6c83b-103">Tabella UpgradedImages (Patchwiz.dll)</span><span class="sxs-lookup"><span data-stu-id="6c83b-103">UpgradedImages Table (Patchwiz.dll)</span></span>

<span data-ttu-id="6c83b-104">La tabella UpgradedImages contiene informazioni sulle immagini aggiornate del prodotto.</span><span class="sxs-lookup"><span data-stu-id="6c83b-104">The UpgradedImages table contains information about the upgraded images of the product.</span></span> <span data-ttu-id="6c83b-105">L'immagine aggiornata deve essere un'immagine di configurazione completamente non compressa della versione più recente del prodotto, ad esempio un'immagine amministrativa o un'immagine di configurazione non compressa da un CD-ROM.</span><span class="sxs-lookup"><span data-stu-id="6c83b-105">The upgraded image should be a fully uncompressed setup image of the latest version of the product, for example, an administrative image or an uncompressed setup image from a CD-ROM.</span></span> <span data-ttu-id="6c83b-106">Un pacchetto Windows Installer patch aggiorna un'immagine di destinazione in un'immagine aggiornata.</span><span class="sxs-lookup"><span data-stu-id="6c83b-106">A Windows Installer patch package updates a target image into an upgraded image.</span></span> <span data-ttu-id="6c83b-107">La tabella UpgradedImages è obbligatoria nel database di creazione della patch (file con estensione PCP) e viene usata da [UiCreatePatchPackageEx](uicreatepatchpackageex--patchwiz-dll-.md).</span><span class="sxs-lookup"><span data-stu-id="6c83b-107">The UpgradedImages table is required in the patch creation database (.pcp file) and is used by [UiCreatePatchPackageEx](uicreatepatchpackageex--patchwiz-dll-.md).</span></span>

<span data-ttu-id="6c83b-108">Una tabella UpgradedImages contenente almeno un record è obbligatoria in ogni database di creazione della patch (file con estensione PCP).</span><span class="sxs-lookup"><span data-stu-id="6c83b-108">An UpgradedImages table containing at least one record is required in every patch creation database (.pcp file).</span></span> <span data-ttu-id="6c83b-109">Questa tabella viene utilizzata da [UiCreatePatchPackageEx](uicreatepatchpackageex--patchwiz-dll-.md).</span><span class="sxs-lookup"><span data-stu-id="6c83b-109">This table is used by [UiCreatePatchPackageEx](uicreatepatchpackageex--patchwiz-dll-.md).</span></span>

<span data-ttu-id="6c83b-110">La tabella UpgradedImages include le colonne seguenti.</span><span class="sxs-lookup"><span data-stu-id="6c83b-110">The UpgradedImages table has the following columns.</span></span>



| <span data-ttu-id="6c83b-111">Colonna</span><span class="sxs-lookup"><span data-stu-id="6c83b-111">Column</span></span>       | <span data-ttu-id="6c83b-112">Tipo</span><span class="sxs-lookup"><span data-stu-id="6c83b-112">Type</span></span> | <span data-ttu-id="6c83b-113">Chiave</span><span class="sxs-lookup"><span data-stu-id="6c83b-113">Key</span></span> | <span data-ttu-id="6c83b-114">Nullable</span><span class="sxs-lookup"><span data-stu-id="6c83b-114">Nullable</span></span> |
|--------------|------|-----|----------|
| <span data-ttu-id="6c83b-115">Aggiornato</span><span class="sxs-lookup"><span data-stu-id="6c83b-115">Upgraded</span></span>     | <span data-ttu-id="6c83b-116">text</span><span class="sxs-lookup"><span data-stu-id="6c83b-116">text</span></span> | <span data-ttu-id="6c83b-117">S</span><span class="sxs-lookup"><span data-stu-id="6c83b-117">Y</span></span>   | <span data-ttu-id="6c83b-118">N</span><span class="sxs-lookup"><span data-stu-id="6c83b-118">N</span></span>        |
| <span data-ttu-id="6c83b-119">PercorsoMSI</span><span class="sxs-lookup"><span data-stu-id="6c83b-119">MsiPath</span></span>      | <span data-ttu-id="6c83b-120">text</span><span class="sxs-lookup"><span data-stu-id="6c83b-120">text</span></span> |     | <span data-ttu-id="6c83b-121">N</span><span class="sxs-lookup"><span data-stu-id="6c83b-121">N</span></span>        |
| <span data-ttu-id="6c83b-122">PatchMsiPath</span><span class="sxs-lookup"><span data-stu-id="6c83b-122">PatchMsiPath</span></span> | <span data-ttu-id="6c83b-123">text</span><span class="sxs-lookup"><span data-stu-id="6c83b-123">text</span></span> |     | <span data-ttu-id="6c83b-124">S</span><span class="sxs-lookup"><span data-stu-id="6c83b-124">Y</span></span>        |
| <span data-ttu-id="6c83b-125">SymbolPaths</span><span class="sxs-lookup"><span data-stu-id="6c83b-125">SymbolPaths</span></span>  | <span data-ttu-id="6c83b-126">text</span><span class="sxs-lookup"><span data-stu-id="6c83b-126">text</span></span> |     | <span data-ttu-id="6c83b-127">S</span><span class="sxs-lookup"><span data-stu-id="6c83b-127">Y</span></span>        |
| <span data-ttu-id="6c83b-128">Famiglia</span><span class="sxs-lookup"><span data-stu-id="6c83b-128">Family</span></span>       | <span data-ttu-id="6c83b-129">text</span><span class="sxs-lookup"><span data-stu-id="6c83b-129">text</span></span> |     | <span data-ttu-id="6c83b-130">N</span><span class="sxs-lookup"><span data-stu-id="6c83b-130">N</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="6c83b-131">Colonne</span><span class="sxs-lookup"><span data-stu-id="6c83b-131">Columns</span></span>

<dl> <dt>

<span data-ttu-id="6c83b-132"><span id="Upgraded"></span><span id="upgraded"></span><span id="UPGRADED"></span>Aggiornato</span><span class="sxs-lookup"><span data-stu-id="6c83b-132"><span id="Upgraded"></span><span id="upgraded"></span><span id="UPGRADED"></span>Upgraded</span></span>
</dt> <dd>

<span data-ttu-id="6c83b-133">Il campo aggiornato è un identificatore arbitrario per connettere le immagini di destinazione a un'immagine aggiornata del prodotto.</span><span class="sxs-lookup"><span data-stu-id="6c83b-133">The Upgraded field is an arbitrary identifier to connect the target images with an upgraded image of the product.</span></span>

</dd> <dt>

<span data-ttu-id="6c83b-134"><span id="MsiPath"></span><span id="msipath"></span><span id="MSIPATH"></span>PercorsoMSI</span><span class="sxs-lookup"><span data-stu-id="6c83b-134"><span id="MsiPath"></span><span id="msipath"></span><span id="MSIPATH"></span>MsiPath</span></span>
</dt> <dd>

<span data-ttu-id="6c83b-135">Questo campo specifica il percorso completo, incluso il nome del file, al percorso del file con estensione msi per l'immagine aggiornata.</span><span class="sxs-lookup"><span data-stu-id="6c83b-135">This field specifies the full path, including the file name, to the location of the .msi file for the upgraded image.</span></span> <span data-ttu-id="6c83b-136">Si tratta del percorso dei file di origine per l'immagine aggiornata.</span><span class="sxs-lookup"><span data-stu-id="6c83b-136">This is the location of the source files for the upgraded image.</span></span>

</dd> <dt>

<span data-ttu-id="6c83b-137"><span id="PatchMsiPath"></span><span id="patchmsipath"></span><span id="PATCHMSIPATH"></span>PatchMsiPath</span><span class="sxs-lookup"><span data-stu-id="6c83b-137"><span id="PatchMsiPath"></span><span id="patchmsipath"></span><span id="PATCHMSIPATH"></span>PatchMsiPath</span></span>
</dt> <dd>

<span data-ttu-id="6c83b-138">Il patchMsiPath facoltativo punta a una copia modificata del database di installazione aggiornato che contiene la modifica aggiuntiva specifica per il processo di installazione della patch.</span><span class="sxs-lookup"><span data-stu-id="6c83b-138">The optional patchMsiPath points to a modified copy of the upgraded installation database that contains additional authoring specific to the patch installation process.</span></span> <span data-ttu-id="6c83b-139">Ad esempio, finestre di dialogo aggiuntive o azioni personalizzate condizionate nella proprietà [**patch**](patch.md) .</span><span class="sxs-lookup"><span data-stu-id="6c83b-139">For example, additional dialogs or custom actions conditioned on the [**PATCH**](patch.md) property.</span></span>

</dd> <dt>

<span data-ttu-id="6c83b-140"><span id="SymbolPaths"></span><span id="symbolpaths"></span><span id="SYMBOLPATHS"></span>SymbolPaths</span><span class="sxs-lookup"><span data-stu-id="6c83b-140"><span id="SymbolPaths"></span><span id="symbolpaths"></span><span id="SYMBOLPATHS"></span>SymbolPaths</span></span>
</dt> <dd>

<span data-ttu-id="6c83b-141">Elenco delimitato da punti e virgola di cartelle in cui cercare i file di simboli che possono essere usati per ottimizzare la generazione della patch binaria.</span><span class="sxs-lookup"><span data-stu-id="6c83b-141">A semicolon delimited list of folders that are to be searched for symbol files that may be used to optimize the generation of the binary patch.</span></span> <span data-ttu-id="6c83b-142">Si noti che non viene eseguita la ricerca nelle sottodirectory delle cartelle specificate in questo campo.</span><span class="sxs-lookup"><span data-stu-id="6c83b-142">Note that the subdirectories of folders specified in this field are not searched.</span></span> <span data-ttu-id="6c83b-143">Una patch binaria ottimizzata può essere più piccola.</span><span class="sxs-lookup"><span data-stu-id="6c83b-143">An optimized binary patch may be smaller.</span></span> <span data-ttu-id="6c83b-144">Visual C++ deve essere installato nel computer che genera la patch e utilizzato per creare i file di simboli.</span><span class="sxs-lookup"><span data-stu-id="6c83b-144">Visual C++ must be installed on the computer generating the patch and used to create the symbol files.</span></span> <span data-ttu-id="6c83b-145">Questo campo è facoltativo e il programma di installazione crea una patch binaria anche se non è stato specificato alcun file di simboli o se i file di simboli non sono più disponibili per Patchwiz.dll.</span><span class="sxs-lookup"><span data-stu-id="6c83b-145">This field is optional, and the installer creates a binary patch even if no symbol files are specified or if the symbol files become unavailable to Patchwiz.dll.</span></span>

</dd> <dt>

<span data-ttu-id="6c83b-146"><span id="Family"></span><span id="family"></span><span id="FAMILY"></span>Famiglia</span><span class="sxs-lookup"><span data-stu-id="6c83b-146"><span id="Family"></span><span id="family"></span><span id="FAMILY"></span>Family</span></span>
</dt> <dd>

<span data-ttu-id="6c83b-147">Chiave esterna nella [tabella ImageFamilies](imagefamilies-table-patchwiz-dll-.md).</span><span class="sxs-lookup"><span data-stu-id="6c83b-147">Foreign key into the [ImageFamilies table](imagefamilies-table-patchwiz-dll-.md).</span></span> <span data-ttu-id="6c83b-148">Ogni immagine aggiornata deve appartenere a un solo gruppo.</span><span class="sxs-lookup"><span data-stu-id="6c83b-148">Each upgraded image must belong to only one family.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="6c83b-149">Commenti</span><span class="sxs-lookup"><span data-stu-id="6c83b-149">Remarks</span></span>

<span data-ttu-id="6c83b-150">Sebbene ogni immagine aggiornata possa essere raggruppata in una famiglia di immagini distinta, il raggruppamento di immagini aggiornate che condividono i file può rendere più piccolo il file con estensione msp.</span><span class="sxs-lookup"><span data-stu-id="6c83b-150">Although each upgraded image can be grouped into a separate image family, grouping upgraded images that share files together may make the .msp smaller.</span></span>

<span data-ttu-id="6c83b-151">Questa tabella accetta le variabili di ambiente come percorsi che iniziano con la versione 4,0 di Patchwiz.dll.</span><span class="sxs-lookup"><span data-stu-id="6c83b-151">This table accepts environment variables as paths beginning with version 4.0 of Patchwiz.dll.</span></span>

 

 



