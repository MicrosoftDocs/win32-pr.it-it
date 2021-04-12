---
description: La \_ tabella UpgradedFile OptionalData contiene informazioni su file specifici in un'immagine aggiornata. Questa tabella è facoltativa nel database di creazione della patch (file con estensione PCP) e viene usata dalla funzione UiCreatePatchPackageEx.
ms.assetid: 8b96a83a-2bfa-47b7-bde0-896bdcc97d29
title: Tabella UpgradedFiles_OptionalData (Patchwiz.dll)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a2a648623e2a0cde11af34a3b948b4f2ac6fba59
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104233706"
---
# <a name="upgradedfiles_optionaldata-table-patchwizdll"></a><span data-ttu-id="b3277-104">\_Tabella UpgradedFiles OptionalData (Patchwiz.dll)</span><span class="sxs-lookup"><span data-stu-id="b3277-104">UpgradedFiles\_OptionalData Table (Patchwiz.dll)</span></span>

<span data-ttu-id="b3277-105">La \_ tabella UpgradedFile OptionalData contiene informazioni su file specifici in un'immagine aggiornata.</span><span class="sxs-lookup"><span data-stu-id="b3277-105">The UpgradedFile\_OptionalData table contains information about specific files in an upgraded image.</span></span> <span data-ttu-id="b3277-106">Questa tabella è facoltativa nel database di creazione della patch (file con estensione PCP) e viene usata dalla funzione [UiCreatePatchPackageEx](uicreatepatchpackageex--patchwiz-dll-.md) .</span><span class="sxs-lookup"><span data-stu-id="b3277-106">This table is optional in the patch creation database (.pcp file) and is used by the [UiCreatePatchPackageEx](uicreatepatchpackageex--patchwiz-dll-.md) function.</span></span>

<span data-ttu-id="b3277-107">La \_ tabella OptionalData di UpgradedFile include le colonne seguenti.</span><span class="sxs-lookup"><span data-stu-id="b3277-107">The UpgradedFile\_OptionalData table has the following columns.</span></span>



| <span data-ttu-id="b3277-108">Colonna</span><span class="sxs-lookup"><span data-stu-id="b3277-108">Column</span></span>                  | <span data-ttu-id="b3277-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="b3277-109">Type</span></span>    | <span data-ttu-id="b3277-110">Chiave</span><span class="sxs-lookup"><span data-stu-id="b3277-110">Key</span></span> | <span data-ttu-id="b3277-111">Nullable</span><span class="sxs-lookup"><span data-stu-id="b3277-111">Nullable</span></span> |
|-------------------------|---------|-----|----------|
| <span data-ttu-id="b3277-112">Aggiornato</span><span class="sxs-lookup"><span data-stu-id="b3277-112">Upgraded</span></span>                | <span data-ttu-id="b3277-113">text</span><span class="sxs-lookup"><span data-stu-id="b3277-113">text</span></span>    | <span data-ttu-id="b3277-114">S</span><span class="sxs-lookup"><span data-stu-id="b3277-114">Y</span></span>   | <span data-ttu-id="b3277-115">N</span><span class="sxs-lookup"><span data-stu-id="b3277-115">N</span></span>        |
| <span data-ttu-id="b3277-116">FTK</span><span class="sxs-lookup"><span data-stu-id="b3277-116">FTK</span></span>                     | <span data-ttu-id="b3277-117">text</span><span class="sxs-lookup"><span data-stu-id="b3277-117">text</span></span>    | <span data-ttu-id="b3277-118">S</span><span class="sxs-lookup"><span data-stu-id="b3277-118">Y</span></span>   | <span data-ttu-id="b3277-119">N</span><span class="sxs-lookup"><span data-stu-id="b3277-119">N</span></span>        |
| <span data-ttu-id="b3277-120">SymbolPaths</span><span class="sxs-lookup"><span data-stu-id="b3277-120">SymbolPaths</span></span>             | <span data-ttu-id="b3277-121">text</span><span class="sxs-lookup"><span data-stu-id="b3277-121">text</span></span>    |     | <span data-ttu-id="b3277-122">S</span><span class="sxs-lookup"><span data-stu-id="b3277-122">Y</span></span>        |
| <span data-ttu-id="b3277-123">AllowIgnoreOnPatchError</span><span class="sxs-lookup"><span data-stu-id="b3277-123">AllowIgnoreOnPatchError</span></span> | <span data-ttu-id="b3277-124">numero intero</span><span class="sxs-lookup"><span data-stu-id="b3277-124">integer</span></span> |     | <span data-ttu-id="b3277-125">S</span><span class="sxs-lookup"><span data-stu-id="b3277-125">Y</span></span>        |
| <span data-ttu-id="b3277-126">IncludeWholeFile</span><span class="sxs-lookup"><span data-stu-id="b3277-126">IncludeWholeFile</span></span>        | <span data-ttu-id="b3277-127">numero intero</span><span class="sxs-lookup"><span data-stu-id="b3277-127">integer</span></span> |     | <span data-ttu-id="b3277-128">S</span><span class="sxs-lookup"><span data-stu-id="b3277-128">Y</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="b3277-129">Colonne</span><span class="sxs-lookup"><span data-stu-id="b3277-129">Columns</span></span>

<dl> <dt>

<span data-ttu-id="b3277-130"><span id="Upgraded"></span><span id="upgraded"></span><span id="UPGRADED"></span>Aggiornato</span><span class="sxs-lookup"><span data-stu-id="b3277-130"><span id="Upgraded"></span><span id="upgraded"></span><span id="UPGRADED"></span>Upgraded</span></span>
</dt> <dd>

<span data-ttu-id="b3277-131">Chiave esterna per la colonna aggiornata della [tabella UpgradedImages (Patchwiz.dll)](upgradedimages-table-patchwiz-dll-.md).</span><span class="sxs-lookup"><span data-stu-id="b3277-131">Foreign key to the Upgraded column of the [UpgradedImages Table (Patchwiz.dll)](upgradedimages-table-patchwiz-dll-.md).</span></span>

</dd> <dt>

<span data-ttu-id="b3277-132"><span id="FTK"></span><span id="ftk"></span>FTK</span><span class="sxs-lookup"><span data-stu-id="b3277-132"><span id="FTK"></span><span id="ftk"></span>FTK</span></span>
</dt> <dd>

<span data-ttu-id="b3277-133">Chiave della tabella file.</span><span class="sxs-lookup"><span data-stu-id="b3277-133">File table key.</span></span> <span data-ttu-id="b3277-134">Chiave esterna nella [tabella file](file-table.md) del file con estensione msi dell'immagine aggiornata.</span><span class="sxs-lookup"><span data-stu-id="b3277-134">Foreign key into [File table](file-table.md) of the .msi file of the upgraded image.</span></span> <span data-ttu-id="b3277-135">Se due o più immagini aggiornate all'interno di una famiglia hanno lo stesso valore FTK, il valore deve fare riferimento allo stesso file.</span><span class="sxs-lookup"><span data-stu-id="b3277-135">If two or more upgraded images within a family have the same FTK value, the value must refer to the same file.</span></span> <span data-ttu-id="b3277-136">I file condivisi da più immagini di aggiornamento devono avere lo stesso FTK per ridurre al minimo le dimensioni del file CAB.</span><span class="sxs-lookup"><span data-stu-id="b3277-136">Files shared by multiple upgrade images should have the same FTK to minimize cabinet file size.</span></span>

</dd> <dt>

<span data-ttu-id="b3277-137"><span id="SymbolPaths"></span><span id="symbolpaths"></span><span id="SYMBOLPATHS"></span>SymbolPaths</span><span class="sxs-lookup"><span data-stu-id="b3277-137"><span id="SymbolPaths"></span><span id="symbolpaths"></span><span id="SYMBOLPATHS"></span>SymbolPaths</span></span>
</dt> <dd>

<span data-ttu-id="b3277-138">Il valore in questo campo viene aggiunto all'elenco delimitato da punti e virgola di cartelle nella colonna SymbolPaths della [tabella UpgradedImages (Patchwiz.dll)](upgradedimages-table-patchwiz-dll-.md) durante la generazione della patch e può essere usato per aggiungere i file di simboli per un file specifico.</span><span class="sxs-lookup"><span data-stu-id="b3277-138">The value in this field is added to the semicolon-delimited list of folders in the SymbolPaths column of the [UpgradedImages Table (Patchwiz.dll)](upgradedimages-table-patchwiz-dll-.md) when the patch is generated, and can be used to add symbol files for a specific file.</span></span>

</dd> <dt>

<span data-ttu-id="b3277-139"><span id="AllowIgnoreOnPatchError"></span><span id="allowignoreonpatcherror"></span><span id="ALLOWIGNOREONPATCHERROR"></span>AllowIgnoreOnPatchError</span><span class="sxs-lookup"><span data-stu-id="b3277-139"><span id="AllowIgnoreOnPatchError"></span><span id="allowignoreonpatcherror"></span><span id="ALLOWIGNOREONPATCHERROR"></span>AllowIgnoreOnPatchError</span></span>
</dt> <dd>

<span data-ttu-id="b3277-140">Impostare su 1 per indicare che la patch è non vitale.</span><span class="sxs-lookup"><span data-stu-id="b3277-140">Set to 1 to indicate that the patch is non-vital.</span></span> <span data-ttu-id="b3277-141">Impostare su 0 per indicare che la patch è fondamentale.</span><span class="sxs-lookup"><span data-stu-id="b3277-141">Set to 0 to indicate that the patch is vital.</span></span> <span data-ttu-id="b3277-142">Se Windows Installer rileva un problema quando si applica questa patch al file specificato nella colonna FTK, il valore in questo campo determina se la finestra di messaggio di errore include un pulsante **Ignora** per consentire all'utente di continuare il processo di applicazione di patch.</span><span class="sxs-lookup"><span data-stu-id="b3277-142">If Windows Installer encounters a problem when applying this patch to the file specified in the FTK column, the value in this field determines whether the error message box includes an **Ignore** button to enable the user to continue the patching process.</span></span>

</dd> <dt>

<span data-ttu-id="b3277-143"><span id="IncludeWholeFile"></span><span id="includewholefile"></span><span id="INCLUDEWHOLEFILE"></span>IncludeWholeFile</span><span class="sxs-lookup"><span data-stu-id="b3277-143"><span id="IncludeWholeFile"></span><span id="includewholefile"></span><span id="INCLUDEWHOLEFILE"></span>IncludeWholeFile</span></span>
</dt> <dd>

<span data-ttu-id="b3277-144">Impostare su un valore diverso da zero se è necessario installare l'intero file specificato nella colonna FTK anziché creare una patch binaria.</span><span class="sxs-lookup"><span data-stu-id="b3277-144">Set to a nonzero value if the entire file specified in the FTK column should be installed rather than creating a binary patch.</span></span>

</dd> </dl>

 

 



