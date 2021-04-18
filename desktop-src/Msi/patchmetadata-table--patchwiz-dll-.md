---
description: La tabella PatchMetadata contiene informazioni su una patch Windows Installer necessaria per rimuovere una patch e utilizzata da installazione applicazioni.
ms.assetid: 09a06de4-0713-4e92-ab29-f34f6c94b677
title: Tabella PatchMetadata (PATCHWIZ.DLL)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7e2521684714b91d8d172f8eb56bab984ffea87d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106318996"
---
# <a name="patchmetadata-table-patchwizdll"></a><span data-ttu-id="3f704-103">Tabella PatchMetadata (PATCHWIZ.DLL)</span><span class="sxs-lookup"><span data-stu-id="3f704-103">PatchMetadata Table (PATCHWIZ.DLL)</span></span>

<span data-ttu-id="3f704-104">La tabella PatchMetadata contiene informazioni su una patch Windows Installer necessaria per rimuovere una patch e utilizzata da installazione applicazioni.</span><span class="sxs-lookup"><span data-stu-id="3f704-104">The PatchMetadata Table contains information about a Windows Installer patch that is required to remove a patch and that is used by Add/Remove Programs.</span></span> <span data-ttu-id="3f704-105">Tutte le proprietà nella tabella PatchMetadata vengono aggiunte alla [tabella MsiPatchMetadata](msipatchmetadata-table.md) del file con estensione msp per una patch.</span><span class="sxs-lookup"><span data-stu-id="3f704-105">All the properties in the PatchMetadata Table are added to the [MsiPatchMetadata Table](msipatchmetadata-table.md) of the .msp file for a patch.</span></span>

<span data-ttu-id="3f704-106">La tabella PatchMetadata è obbligatoria nei file delle proprietà di creazione della patch (file con estensione PCP) con MinimumRequiredMsiVersion uguale a 300 nella [tabella Properties](properties-table-patchwiz-dll-.md).</span><span class="sxs-lookup"><span data-stu-id="3f704-106">The PatchMetadata Table is required in patch creation properties files (.pcp files) that have a MinimumRequiredMsiVersion equal to 300 in the [Properties Table](properties-table-patchwiz-dll-.md).</span></span> <span data-ttu-id="3f704-107">La tabella è facoltativa se MinimumRequiredMsiVersion non è uguale a 300.</span><span class="sxs-lookup"><span data-stu-id="3f704-107">The table is optional if MinimumRequiredMsiVersion is not equal to 300.</span></span>

<span data-ttu-id="3f704-108">La tabella PatchMetadata include le colonne seguenti.</span><span class="sxs-lookup"><span data-stu-id="3f704-108">The PatchMetadata Table has the following columns.</span></span>



| <span data-ttu-id="3f704-109">Colonna</span><span class="sxs-lookup"><span data-stu-id="3f704-109">Column</span></span>   | <span data-ttu-id="3f704-110">Tipo</span><span class="sxs-lookup"><span data-stu-id="3f704-110">Type</span></span> | <span data-ttu-id="3f704-111">Chiave</span><span class="sxs-lookup"><span data-stu-id="3f704-111">Key</span></span> | <span data-ttu-id="3f704-112">Nullable</span><span class="sxs-lookup"><span data-stu-id="3f704-112">Nullable</span></span> |
|----------|------|-----|----------|
| <span data-ttu-id="3f704-113">Company</span><span class="sxs-lookup"><span data-stu-id="3f704-113">Company</span></span>  | <span data-ttu-id="3f704-114">text</span><span class="sxs-lookup"><span data-stu-id="3f704-114">text</span></span> | <span data-ttu-id="3f704-115">S</span><span class="sxs-lookup"><span data-stu-id="3f704-115">Y</span></span>   | <span data-ttu-id="3f704-116">S</span><span class="sxs-lookup"><span data-stu-id="3f704-116">Y</span></span>        |
| <span data-ttu-id="3f704-117">Proprietà</span><span class="sxs-lookup"><span data-stu-id="3f704-117">Property</span></span> | <span data-ttu-id="3f704-118">text</span><span class="sxs-lookup"><span data-stu-id="3f704-118">text</span></span> | <span data-ttu-id="3f704-119">S</span><span class="sxs-lookup"><span data-stu-id="3f704-119">Y</span></span>   | <span data-ttu-id="3f704-120">N</span><span class="sxs-lookup"><span data-stu-id="3f704-120">N</span></span>        |
| <span data-ttu-id="3f704-121">Valore</span><span class="sxs-lookup"><span data-stu-id="3f704-121">Value</span></span>    | <span data-ttu-id="3f704-122">text</span><span class="sxs-lookup"><span data-stu-id="3f704-122">text</span></span> |     | <span data-ttu-id="3f704-123">S</span><span class="sxs-lookup"><span data-stu-id="3f704-123">Y</span></span>        |



 

### <a name="columns"></a><span data-ttu-id="3f704-124">Colonne</span><span class="sxs-lookup"><span data-stu-id="3f704-124">Columns</span></span>

<dl> <dt>

<span data-ttu-id="3f704-125"><span id="Company"></span><span id="company"></span><span id="COMPANY"></span>Azienda</span><span class="sxs-lookup"><span data-stu-id="3f704-125"><span id="Company"></span><span id="company"></span><span id="COMPANY"></span>Company</span></span>
</dt> <dd>

<span data-ttu-id="3f704-126">Nome della società.</span><span class="sxs-lookup"><span data-stu-id="3f704-126">The name of the company.</span></span> <span data-ttu-id="3f704-127">Un campo vuoto (un valore null) indica che questa riga contiene una delle proprietà dei metadati standard.</span><span class="sxs-lookup"><span data-stu-id="3f704-127">An empty field (a Null value) indicates that this row contains one of the standard metadata properties.</span></span> <span data-ttu-id="3f704-128">Una società può estendere il set di proprietà aggiungendo una riga alla tabella e immettendo il nome di una società in questo campo.</span><span class="sxs-lookup"><span data-stu-id="3f704-128">A company can extend the property set by adding a row to the table, and entering a company name in this field.</span></span>

</dd> <dt>

<span data-ttu-id="3f704-129"><span id="Property"></span><span id="property"></span><span id="PROPERTY"></span>Proprietà</span><span class="sxs-lookup"><span data-stu-id="3f704-129"><span id="Property"></span><span id="property"></span><span id="PROPERTY"></span>Property</span></span>
</dt> <dd>

<span data-ttu-id="3f704-130">Nome di una proprietà dei metadati.</span><span class="sxs-lookup"><span data-stu-id="3f704-130">The name of a metadata property.</span></span> <span data-ttu-id="3f704-131">Le proprietà AllowRemoval, Manufacturer, TargetProductName, MoreInfoURL, DisplayName, Description e Classification sono obbligatorie nella tabella PatchMetadata.</span><span class="sxs-lookup"><span data-stu-id="3f704-131">The AllowRemoval, ManufacturerName, TargetProductName, MoreInfoURL, DisplayName, Description, and Classification properties are required in the PatchMetadata Table .</span></span> <span data-ttu-id="3f704-132">Questo campo deve contenere una delle proprietà di metadati standard seguenti se il campo Company è vuoto (un valore null).</span><span class="sxs-lookup"><span data-stu-id="3f704-132">This field must contain one of the following standard metadata properties if the Company field is empty (a Null value).</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="3f704-133">Proprietà</span><span class="sxs-lookup"><span data-stu-id="3f704-133">Property</span></span></th>
<th><span data-ttu-id="3f704-134">Descrizione</span><span class="sxs-lookup"><span data-stu-id="3f704-134">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="3f704-135">AllowRemoval</span><span class="sxs-lookup"><span data-stu-id="3f704-135">AllowRemoval</span></span></td>
<td><span data-ttu-id="3f704-136">Valore intero che indica se la patch è una <a href="uninstallable-patches.md">patch non installabile</a>.</span><span class="sxs-lookup"><span data-stu-id="3f704-136">An integer value that indicates whether or not the patch is an <a href="uninstallable-patches.md">Uninstallable Patch</a>.</span></span> <span data-ttu-id="3f704-137">Se il campo del valore contiene 0 (zero), la patch non può essere rimossa.</span><span class="sxs-lookup"><span data-stu-id="3f704-137">If the Value field contains a 0 (zero), the patch cannot be removed.</span></span> <span data-ttu-id="3f704-138">Se il campo del valore contiene 1 (uno), la patch è una patch non installabile.</span><span class="sxs-lookup"><span data-stu-id="3f704-138">If the Value field contains 1 (one), the patch is an Uninstallable Patch.</span></span> <span data-ttu-id="3f704-139">Questa proprietà è obbligatoria. Questa proprietà è registrata e il relativo valore può essere ottenuto tramite la funzione <a href="/windows/desktop/api/Msi/nf-msi-msigetpatchinfoexa"><strong>MsiGetPatchInfoEx</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="3f704-139">This property is required.This property is registered and its value can be obtain by using the <a href="/windows/desktop/api/Msi/nf-msi-msigetpatchinfoexa"><strong>MsiGetPatchInfoEx</strong></a> function.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3f704-140">ManufacturerName</span><span class="sxs-lookup"><span data-stu-id="3f704-140">ManufacturerName</span></span></td>
<td><span data-ttu-id="3f704-141">Valore stringa che contiene il nome del produttore dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="3f704-141">A string value that contains the name of the manufacturer of the application.</span></span> <span data-ttu-id="3f704-142">Questa proprietà è obbligatoria.</span><span class="sxs-lookup"><span data-stu-id="3f704-142">This property is required.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3f704-143">MinorUpdateTargetRTM</span><span class="sxs-lookup"><span data-stu-id="3f704-143">MinorUpdateTargetRTM</span></span></td>
<td><span data-ttu-id="3f704-144">Indica che la patch è destinata alla versione RTM del prodotto o alla patch di aggiornamento principale più recente.</span><span class="sxs-lookup"><span data-stu-id="3f704-144">Indicates that the patch targets the RTM version of the product or the most recent major upgrade patch.</span></span> <span data-ttu-id="3f704-145">Creare questa proprietà facoltativa in patch di aggiornamento secondarie che contengono informazioni di sequenziazione per indicare che la patch rimuove tutte le patch fino alla versione RTM del prodotto o fino alla patch di aggiornamento principale più recente.</span><span class="sxs-lookup"><span data-stu-id="3f704-145">Author this optional property in minor upgrade patches that contain sequencing information to indicate that the patch removes of all patches up to the RTM version of the product, or up to the most recent major upgrade patch.</span></span> <span data-ttu-id="3f704-146">Questa proprietà è disponibile a partire da Windows Installer 3,1.</span><span class="sxs-lookup"><span data-stu-id="3f704-146">This property is available beginning with Windows Installer 3.1.</span></span>
<blockquote>
[!Note]<br />
<span data-ttu-id="3f704-147">Per richiedere l'installazione di Windows Installer 3,1 per applicare la patch, impostare la proprietà MinimumRequiredMsiVersion su 310 nella <a href="properties-table-patchwiz-dll-.md">tabella Properties</a> del file con estensione PCP.</span><span class="sxs-lookup"><span data-stu-id="3f704-147">To require that Windows Installer 3.1 be installed to apply the patch, set the MinimumRequiredMsiVersion property to 310 in the <a href="properties-table-patchwiz-dll-.md">Properties Table</a> of the .pcp file.</span></span>
</blockquote>
<br/> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3f704-148">TargetProductName</span><span class="sxs-lookup"><span data-stu-id="3f704-148">TargetProductName</span></span></td>
<td><span data-ttu-id="3f704-149">Valore stringa che contiene il nome dell'applicazione o del gruppo di applicazioni di destinazione.</span><span class="sxs-lookup"><span data-stu-id="3f704-149">A string value that contains the name of the application or target application suite.</span></span> <span data-ttu-id="3f704-150">Questa proprietà è obbligatoria.</span><span class="sxs-lookup"><span data-stu-id="3f704-150">This property is required.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3f704-151">MoreInfoURL</span><span class="sxs-lookup"><span data-stu-id="3f704-151">MoreInfoURL</span></span></td>
<td><span data-ttu-id="3f704-152">Valore stringa che contiene un URL che punta alle informazioni per questa patch.</span><span class="sxs-lookup"><span data-stu-id="3f704-152">A string value that contains a URL pointing to information for this patch.</span></span> <span data-ttu-id="3f704-153">Questa proprietà obbligatoria è registrata e il relativo valore può essere ottenuto tramite la funzione <a href="/windows/desktop/api/Msi/nf-msi-msigetpatchinfoexa"><strong>MsiGetPatchInfoEx</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="3f704-153">This required property is registered and its value can be obtained by using the <a href="/windows/desktop/api/Msi/nf-msi-msigetpatchinfoexa"><strong>MsiGetPatchInfoEx</strong></a> function.</span></span> <span data-ttu-id="3f704-154">A partire da Windows XP con Service Pack 2 (SP2), questo valore può essere il collegamento di supporto per la patch visualizzata in Installazione applicazioni.</span><span class="sxs-lookup"><span data-stu-id="3f704-154">Beginning with Windows XP with Service Pack 2 (SP2), this value can be the support link for the patch displayed in Add/Remove Programs.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3f704-155">CreationTimeUTC</span><span class="sxs-lookup"><span data-stu-id="3f704-155">CreationTimeUTC</span></span></td>
<td><span data-ttu-id="3f704-156">Valore stringa che contiene l'ora di creazione del file con estensione msp nel formato mm-DD-YY HH: MM (mese-giorno-anno ora: minuto).</span><span class="sxs-lookup"><span data-stu-id="3f704-156">A string value that contains the creation time of the .msp file in the form mm-dd-yy HH:MM (month-day-year hour:minute).</span></span> <span data-ttu-id="3f704-157">Questa proprietà è facoltativa.</span><span class="sxs-lookup"><span data-stu-id="3f704-157">This property is optional.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3f704-158">DisplayName</span><span class="sxs-lookup"><span data-stu-id="3f704-158">DisplayName</span></span></td>
<td><span data-ttu-id="3f704-159">Valore stringa che contiene il titolo della patch adatto per la visualizzazione pubblica.</span><span class="sxs-lookup"><span data-stu-id="3f704-159">A string value that contains the title for the patch that is suitable for public display.</span></span> <span data-ttu-id="3f704-160">Questa proprietà è obbligatoria.</span><span class="sxs-lookup"><span data-stu-id="3f704-160">This property is required.</span></span> <span data-ttu-id="3f704-161">Questa proprietà è registrata e il relativo valore può essere ottenuto tramite la funzione <a href="/windows/desktop/api/Msi/nf-msi-msigetpatchinfoexa"><strong>MsiGetPatchInfoEx</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="3f704-161">This property is registered and its value can be obtain by using the <a href="/windows/desktop/api/Msi/nf-msi-msigetpatchinfoexa"><strong>MsiGetPatchInfoEx</strong></a> function.</span></span> <span data-ttu-id="3f704-162">A partire da Windows XP con SP2, questo valore è il nome della patch visualizzata in Installazione applicazioni a partire da Windows XP con SP2.</span><span class="sxs-lookup"><span data-stu-id="3f704-162">Beginning with Windows XP with SP2, this value is the name of the patch displayed in Add/Remove Programs beginning with Windows XP with SP2.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3f704-163">Descrizione</span><span class="sxs-lookup"><span data-stu-id="3f704-163">Description</span></span></td>
<td><span data-ttu-id="3f704-164">Valore stringa che contiene una breve descrizione della patch.</span><span class="sxs-lookup"><span data-stu-id="3f704-164">A string value that contains a brief description of the patch.</span></span> <span data-ttu-id="3f704-165">Questa proprietà è obbligatoria.</span><span class="sxs-lookup"><span data-stu-id="3f704-165">This property is required.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3f704-166">Classificazione</span><span class="sxs-lookup"><span data-stu-id="3f704-166">Classification</span></span></td>
<td><span data-ttu-id="3f704-167">Valore stringa che contiene la categoria arbitraria di aggiornamenti come definito dall'autore della patch.</span><span class="sxs-lookup"><span data-stu-id="3f704-167">A string value that contains the arbitrary category of updates as defined by the author of the patch.</span></span> <span data-ttu-id="3f704-168">Gli autori delle patch possono ad esempio specificare che ogni patch deve essere classificata come hotfix, rollup della sicurezza, aggiornamento critico, aggiornamento, Service Pack o aggiornamento cumulativo.</span><span class="sxs-lookup"><span data-stu-id="3f704-168">For example, patch authors can specify that each patch be classified as a Hotfix, Security Rollup, Critical Update, Update, Service Pack, or Update Rollup.</span></span> <span data-ttu-id="3f704-169">Questa proprietà è obbligatoria.</span><span class="sxs-lookup"><span data-stu-id="3f704-169">This property is required.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3f704-170">OptimizedInstallMode</span><span class="sxs-lookup"><span data-stu-id="3f704-170">OptimizedInstallMode</span></span></td>
<td><span data-ttu-id="3f704-171">Se questa proprietà è impostata su 1 (una) in tutte le patch da applicare in una transazione, l'applicazione della patch viene ottimizzata, se possibile.</span><span class="sxs-lookup"><span data-stu-id="3f704-171">If this property is set to 1 (one) in all the patches to be applied in a transaction, the application of the patch is optimized if possible.</span></span> <span data-ttu-id="3f704-172">Per informazioni, vedere <a href="patch-optimization.md">ottimizzazione della patch</a>.</span><span class="sxs-lookup"><span data-stu-id="3f704-172">For information, see <a href="patch-optimization.md">Patch Optimization</a>.</span></span> <span data-ttu-id="3f704-173">Disponibile a partire da Windows Installer 3,1.</span><span class="sxs-lookup"><span data-stu-id="3f704-173">Available beginning with Windows Installer 3.1.</span></span></td>
</tr>
</tbody>
</table>



 

</dd> <dt>

<span data-ttu-id="3f704-174"><span id="Value"></span><span id="value"></span><span id="VALUE"></span>Valore</span><span class="sxs-lookup"><span data-stu-id="3f704-174"><span id="Value"></span><span id="value"></span><span id="VALUE"></span>Value</span></span>
</dt> <dd>

<span data-ttu-id="3f704-175">Valore della proprietà dei metadati.</span><span class="sxs-lookup"><span data-stu-id="3f704-175">Value of the metadata property.</span></span> <span data-ttu-id="3f704-176">Non può mai essere null o una stringa vuota.</span><span class="sxs-lookup"><span data-stu-id="3f704-176">This can never be Null or an empty string.</span></span> <span data-ttu-id="3f704-177">Questo valore può essere localizzato.</span><span class="sxs-lookup"><span data-stu-id="3f704-177">This value can be localized.</span></span>

</dd> </dl>

### <a name="remarks"></a><span data-ttu-id="3f704-178">Commenti</span><span class="sxs-lookup"><span data-stu-id="3f704-178">Remarks</span></span>

<span data-ttu-id="3f704-179">Disponibile a partire da Windows Installer 3,0.</span><span class="sxs-lookup"><span data-stu-id="3f704-179">Available beginning in Windows Installer 3.0.</span></span>

<span data-ttu-id="3f704-180">Tutte le proprietà create nella tabella PatchMetadata vengono aggiunte alla tabella MsiPatchMetadata del file msp.</span><span class="sxs-lookup"><span data-stu-id="3f704-180">All properties authored into the PatchMetadata Table are added to the MsiPatchMetadata table of the msp file.</span></span> <span data-ttu-id="3f704-181">Le proprietà AllowRemoval, MoreInfoURL e DisplayName sono registrate e sono accessibili tramite [**MsiGetPatchInfoEx**](/windows/desktop/api/Msi/nf-msi-msigetpatchinfoexa).</span><span class="sxs-lookup"><span data-stu-id="3f704-181">AllowRemoval, MoreInfoURL and DisplayName properties are registered and are accessible through the [**MsiGetPatchInfoEx**](/windows/desktop/api/Msi/nf-msi-msigetpatchinfoexa).</span></span>

 

 




