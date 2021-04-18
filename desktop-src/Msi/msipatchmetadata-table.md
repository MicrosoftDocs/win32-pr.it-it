---
description: La tabella MsiPatchMetadata contiene informazioni su una patch Windows Installer necessaria per rimuovere la patch e utilizzata da installazione applicazioni.
ms.assetid: b1c30e16-6c91-451a-8b75-7ddbcefcc092
title: Tabella MsiPatchMetadata
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2642661a8f9dc067086926f8e993fc32c95a4a85
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106319007"
---
# <a name="msipatchmetadata-table"></a><span data-ttu-id="3bb9c-103">Tabella MsiPatchMetadata</span><span class="sxs-lookup"><span data-stu-id="3bb9c-103">MsiPatchMetadata Table</span></span>

<span data-ttu-id="3bb9c-104">La tabella MsiPatchMetadata contiene informazioni su una patch Windows Installer necessaria per rimuovere la patch e utilizzata da **Installazione applicazioni**.</span><span class="sxs-lookup"><span data-stu-id="3bb9c-104">The MsiPatchMetadata Table contains information about a Windows Installer patch that is required to remove the patch and that is used by **Add/Remove Programs**.</span></span>

<span data-ttu-id="3bb9c-105">Non è possibile rimuovere le patch installate senza la tabella presente nel database della patch (file con estensione msp) e non sono disponibili alcune informazioni da **Installazione applicazioni**.</span><span class="sxs-lookup"><span data-stu-id="3bb9c-105">Patches installed without this table present in the patch database (.msp file) cannot be removed, and are missing some information from **Add/Remove Programs**.</span></span> <span data-ttu-id="3bb9c-106">La tabella deve trovarsi nel database del file di correzione e non in una trasformazione della patch.</span><span class="sxs-lookup"><span data-stu-id="3bb9c-106">The table must be in the database of the patch file and not in a transform in the patch.</span></span>

<span data-ttu-id="3bb9c-107">La tabella MsiPatchMetadata include le colonne seguenti.</span><span class="sxs-lookup"><span data-stu-id="3bb9c-107">The MsiPatchMetadata Table has the following columns.</span></span>



| <span data-ttu-id="3bb9c-108">Colonna</span><span class="sxs-lookup"><span data-stu-id="3bb9c-108">Column</span></span>   | <span data-ttu-id="3bb9c-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="3bb9c-109">Type</span></span>                         | <span data-ttu-id="3bb9c-110">Chiave</span><span class="sxs-lookup"><span data-stu-id="3bb9c-110">Key</span></span> | <span data-ttu-id="3bb9c-111">Nullable</span><span class="sxs-lookup"><span data-stu-id="3bb9c-111">Nullable</span></span> |
|----------|------------------------------|-----|----------|
| <span data-ttu-id="3bb9c-112">Company</span><span class="sxs-lookup"><span data-stu-id="3bb9c-112">Company</span></span>  | [<span data-ttu-id="3bb9c-113">Identificatore</span><span class="sxs-lookup"><span data-stu-id="3bb9c-113">Identifier</span></span>](identifier.md) | <span data-ttu-id="3bb9c-114">S</span><span class="sxs-lookup"><span data-stu-id="3bb9c-114">Y</span></span>   | <span data-ttu-id="3bb9c-115">S</span><span class="sxs-lookup"><span data-stu-id="3bb9c-115">Y</span></span>        |
| <span data-ttu-id="3bb9c-116">Proprietà</span><span class="sxs-lookup"><span data-stu-id="3bb9c-116">Property</span></span> | [<span data-ttu-id="3bb9c-117">Identificatore</span><span class="sxs-lookup"><span data-stu-id="3bb9c-117">Identifier</span></span>](identifier.md) | <span data-ttu-id="3bb9c-118">S</span><span class="sxs-lookup"><span data-stu-id="3bb9c-118">Y</span></span>   | <span data-ttu-id="3bb9c-119">N</span><span class="sxs-lookup"><span data-stu-id="3bb9c-119">N</span></span>        |
| <span data-ttu-id="3bb9c-120">Valore</span><span class="sxs-lookup"><span data-stu-id="3bb9c-120">Value</span></span>    | [<span data-ttu-id="3bb9c-121">Text</span><span class="sxs-lookup"><span data-stu-id="3bb9c-121">Text</span></span>](text.md)             | <span data-ttu-id="3bb9c-122">N</span><span class="sxs-lookup"><span data-stu-id="3bb9c-122">N</span></span>   | <span data-ttu-id="3bb9c-123">N</span><span class="sxs-lookup"><span data-stu-id="3bb9c-123">N</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="3bb9c-124">Colonne</span><span class="sxs-lookup"><span data-stu-id="3bb9c-124">Columns</span></span>

<dl> <dt>

<span data-ttu-id="3bb9c-125"><span id="Company"></span><span id="company"></span><span id="COMPANY"></span>Azienda</span><span class="sxs-lookup"><span data-stu-id="3bb9c-125"><span id="Company"></span><span id="company"></span><span id="COMPANY"></span>Company</span></span>
</dt> <dd>

<span data-ttu-id="3bb9c-126">Nome della società.</span><span class="sxs-lookup"><span data-stu-id="3bb9c-126">The name of the company.</span></span> <span data-ttu-id="3bb9c-127">Un campo vuoto (un valore null) indica che la riga contiene una delle proprietà dei metadati standard del Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="3bb9c-127">An empty field (a Null value) indicates that the row contains one of the standard metadata properties of the Windows Installer.</span></span> <span data-ttu-id="3bb9c-128">Per ulteriori informazioni, vedere la sezione Osservazioni di questo argomento.</span><span class="sxs-lookup"><span data-stu-id="3bb9c-128">For more information, see the Remarks section of this topic.</span></span>

<span data-ttu-id="3bb9c-129">Aggiungendo una riga alla tabella e immettendo il nome di una società in questo campo, è possibile aggiungere qualsiasi azienda per estendere il set di proprietà.</span><span class="sxs-lookup"><span data-stu-id="3bb9c-129">By adding a row to the table and entering a company name in this field, you can add any company to extend the property set.</span></span>

</dd> <dt>

<span data-ttu-id="3bb9c-130"><span id="Property"></span><span id="property"></span><span id="PROPERTY"></span>Proprietà</span><span class="sxs-lookup"><span data-stu-id="3bb9c-130"><span id="Property"></span><span id="property"></span><span id="PROPERTY"></span>Property</span></span>
</dt> <dd>

<span data-ttu-id="3bb9c-131">Nome di una proprietà dei metadati.</span><span class="sxs-lookup"><span data-stu-id="3bb9c-131">The name of a metadata property.</span></span>

</dd> <dt>

<span data-ttu-id="3bb9c-132"><span id="Value"></span><span id="value"></span><span id="VALUE"></span>Valore</span><span class="sxs-lookup"><span data-stu-id="3bb9c-132"><span id="Value"></span><span id="value"></span><span id="VALUE"></span>Value</span></span>
</dt> <dd>

<span data-ttu-id="3bb9c-133">Valore della proprietà dei metadati.</span><span class="sxs-lookup"><span data-stu-id="3bb9c-133">The value of the metadata property.</span></span> <span data-ttu-id="3bb9c-134">Non può mai essere null o una stringa vuota.</span><span class="sxs-lookup"><span data-stu-id="3bb9c-134">This can never be Null or an empty string.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="3bb9c-135">Commenti</span><span class="sxs-lookup"><span data-stu-id="3bb9c-135">Remarks</span></span>

<span data-ttu-id="3bb9c-136">Disponibile in Windows Installer 3,0 e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="3bb9c-136">Available in Windows Installer 3.0 and later.</span></span>

<span data-ttu-id="3bb9c-137">Le righe della tabella MsiPatchMetadata che contengono un valore null nel campo CompanyName si riferiscono a una delle seguenti proprietà standard dei metadati del Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="3bb9c-137">Rows in the MsiPatchMetadata Table that contain a Null value in the CompanyName field refer to one of the following standard Windows Installer metadata properties.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="3bb9c-138">Proprietà</span><span class="sxs-lookup"><span data-stu-id="3bb9c-138">Property</span></span></th>
<th><span data-ttu-id="3bb9c-139">Descrizione</span><span class="sxs-lookup"><span data-stu-id="3bb9c-139">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="3bb9c-140">AllowRemoval</span><span class="sxs-lookup"><span data-stu-id="3bb9c-140">AllowRemoval</span></span></td>
<td><span data-ttu-id="3bb9c-141">Indica se la patch è una patch non <a href="uninstallable-patches.md">installabile</a>.</span><span class="sxs-lookup"><span data-stu-id="3bb9c-141">Indicates whether or not the patch is an <a href="uninstallable-patches.md">Uninstallable Patch</a>.</span></span> <span data-ttu-id="3bb9c-142">Se il campo del valore contiene 0 (zero), la patch non può essere rimossa.</span><span class="sxs-lookup"><span data-stu-id="3bb9c-142">If the value field contains 0 (zero), the patch cannot be removed.</span></span> <span data-ttu-id="3bb9c-143">Se il campo del valore contiene uno (1), la patch è una patch non installabile. questa proprietà è registrata e il relativo valore può essere ottenuto tramite la funzione <a href="/windows/desktop/api/Msi/nf-msi-msigetpatchinfoexa"><strong>MsiGetPatchInfoEx</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="3bb9c-143">If the value field contains one (1), the patch is an Uninstallable Patch.This property is registered and its value can be obtain by using the <a href="/windows/desktop/api/Msi/nf-msi-msigetpatchinfoexa"><strong>MsiGetPatchInfoEx</strong></a> function.</span></span> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3bb9c-144">ManufacturerName</span><span class="sxs-lookup"><span data-stu-id="3bb9c-144">ManufacturerName</span></span></td>
<td><span data-ttu-id="3bb9c-145">Nome del produttore dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="3bb9c-145">Name of the manufacturer of the application.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3bb9c-146">MinorUpdateTargetRTM</span><span class="sxs-lookup"><span data-stu-id="3bb9c-146">MinorUpdateTargetRTM</span></span></td>
<td><span data-ttu-id="3bb9c-147">Indica che la patch è destinata alla versione RTM del prodotto o alla patch di aggiornamento principale più recente.</span><span class="sxs-lookup"><span data-stu-id="3bb9c-147">Indicates that the patch targets the RTM version of the product or the most recent major upgrade patch.</span></span> <span data-ttu-id="3bb9c-148">Creare questa proprietà facoltativa in patch di aggiornamento secondarie che contengono informazioni di sequenziazione per indicare che la patch rimuove tutte le patch fino alla versione RTM del prodotto o fino alla patch di aggiornamento principale più recente.</span><span class="sxs-lookup"><span data-stu-id="3bb9c-148">Author this optional property in minor upgrade patches that contain sequencing information to indicate that the patch removes of all patches up to the RTM version of the product, or up to the most recent major upgrade patch.</span></span> <span data-ttu-id="3bb9c-149">Questa proprietà è disponibile in Windows Installer 3,1 e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="3bb9c-149">This property is available in Windows Installer 3.1 and later.</span></span> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3bb9c-150">TargetProductName</span><span class="sxs-lookup"><span data-stu-id="3bb9c-150">TargetProductName</span></span></td>
<td><span data-ttu-id="3bb9c-151">Nome dell'applicazione o del gruppo di applicazioni di destinazione.</span><span class="sxs-lookup"><span data-stu-id="3bb9c-151">Name of the application or target application suite.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3bb9c-152">MoreInfoURL</span><span class="sxs-lookup"><span data-stu-id="3bb9c-152">MoreInfoURL</span></span></td>
<td><span data-ttu-id="3bb9c-153">URL che fornisce informazioni specifiche per questa patch.</span><span class="sxs-lookup"><span data-stu-id="3bb9c-153">A URL that provides information specific to this patch.</span></span> <span data-ttu-id="3bb9c-154">Questa proprietà è registrata e il relativo valore può essere ottenuto tramite la funzione <a href="/windows/desktop/api/Msi/nf-msi-msigetpatchinfoexa"><strong>MsiGetPatchInfoEx</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="3bb9c-154">This property is registered and its value can be obtained by using the <a href="/windows/desktop/api/Msi/nf-msi-msigetpatchinfoexa"><strong>MsiGetPatchInfoEx</strong></a> function.</span></span> <span data-ttu-id="3bb9c-155">A partire da Windows XP con Service Pack 2 (SP2), questo valore può essere il collegamento di supporto per la patch visualizzata in <strong>Installazione applicazioni</strong>.</span><span class="sxs-lookup"><span data-stu-id="3bb9c-155">Beginning with Windows XP with Service Pack 2 (SP2), this value can be the support link for the patch displayed in <strong>Add/Remove Programs</strong>.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3bb9c-156">CreationTimeUTC</span><span class="sxs-lookup"><span data-stu-id="3bb9c-156">CreationTimeUTC</span></span></td>
<td><span data-ttu-id="3bb9c-157">Ora di creazione del file con estensione msp nel formato mm-DD-YY HH: MM (mese-giorno-anno ora: minuto).</span><span class="sxs-lookup"><span data-stu-id="3bb9c-157">Creation time of the .msp file in the form of mm-dd-yy HH:MM (month-day-year hour:minute).</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3bb9c-158">DisplayName</span><span class="sxs-lookup"><span data-stu-id="3bb9c-158">DisplayName</span></span></td>
<td><span data-ttu-id="3bb9c-159">Titolo per la patch che è corretto per la visualizzazione pubblica.</span><span class="sxs-lookup"><span data-stu-id="3bb9c-159">A title for the patch that is okay for public display.</span></span> <span data-ttu-id="3bb9c-160">Questa proprietà è registrata e il relativo valore può essere ottenuto tramite la funzione <a href="/windows/desktop/api/Msi/nf-msi-msigetpatchinfoexa"><strong>MsiGetPatchInfoEx</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="3bb9c-160">This property is registered, and its value can be obtained by using the <a href="/windows/desktop/api/Msi/nf-msi-msigetpatchinfoexa"><strong>MsiGetPatchInfoEx</strong></a> function.</span></span> <span data-ttu-id="3bb9c-161">A partire da Windows XP con SP2, questo valore corrisponde al nome della patch visualizzata in <strong>Installazione applicazioni</strong>.</span><span class="sxs-lookup"><span data-stu-id="3bb9c-161">Beginning with Windows XP with SP2, this value is the name of the patch that is displayed in <strong>Add/Remove Programs</strong>.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3bb9c-162">Descrizione</span><span class="sxs-lookup"><span data-stu-id="3bb9c-162">Description</span></span></td>
<td><span data-ttu-id="3bb9c-163">Breve descrizione della patch.</span><span class="sxs-lookup"><span data-stu-id="3bb9c-163">Brief description of the patch.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3bb9c-164">Classificazione</span><span class="sxs-lookup"><span data-stu-id="3bb9c-164">Classification</span></span></td>
<td><span data-ttu-id="3bb9c-165">Valore stringa che contiene la categoria arbitraria di aggiornamenti come definito dall'autore della patch.</span><span class="sxs-lookup"><span data-stu-id="3bb9c-165">A string value that contains the arbitrary category of updates as defined by the author of the patch.</span></span> <span data-ttu-id="3bb9c-166">Gli autori delle patch possono ad esempio specificare che ogni patch deve essere classificata come hotfix, rollup della sicurezza, aggiornamento critico, aggiornamento, Service Pack o aggiornamento cumulativo.</span><span class="sxs-lookup"><span data-stu-id="3bb9c-166">For example, patch authors can specify that each patch be classified as a Hotfix, Security Rollup, Critical Update, Update, Service Pack, or Update Rollup.</span></span> <span data-ttu-id="3bb9c-167">Questa proprietà è obbligatoria.</span><span class="sxs-lookup"><span data-stu-id="3bb9c-167">This property is required.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3bb9c-168">OptimizeCA</span><span class="sxs-lookup"><span data-stu-id="3bb9c-168">OptimizeCA</span></span></td>
<td><span data-ttu-id="3bb9c-169">Indica se il Windows Installer deve ignorare le azioni personalizzate durante l'applicazione della patch.</span><span class="sxs-lookup"><span data-stu-id="3bb9c-169">Indicates whether the Windows Installer should skip custom actions when applying the patch.</span></span> <span data-ttu-id="3bb9c-170">In questo modo è possibile ridurre il tempo necessario per applicare la patch.</span><span class="sxs-lookup"><span data-stu-id="3bb9c-170">This can reduce the time required to apply the patch.</span></span> <span data-ttu-id="3bb9c-171">Il valore della proprietà OptimizeCA può essere uno dei seguenti:</span><span class="sxs-lookup"><span data-stu-id="3bb9c-171">The OptimizeCA property can have one of the following values:</span></span><br/>
<ul>
<li><span data-ttu-id="3bb9c-172">0: non viene ignorata alcuna azione personalizzata.</span><span class="sxs-lookup"><span data-stu-id="3bb9c-172">0 - Do not skip any custom actions.</span></span></li>
<li><span data-ttu-id="3bb9c-173">1-ignorare le azioni personalizzate di assegnazione di proprietà e directory.</span><span class="sxs-lookup"><span data-stu-id="3bb9c-173">1 - Skip property and directory assignment custom actions.</span></span> <span data-ttu-id="3bb9c-174">Il <a href="custom-action-type-35.md">tipo di azione personalizzata 35</a> e il <a href="custom-action-type-51.md">tipo di azione personalizzato 51</a> possono essere azioni personalizzate di assegnazione di proprietà e directory.</span><span class="sxs-lookup"><span data-stu-id="3bb9c-174"><a href="custom-action-type-35.md">Custom Action Type 35</a> and <a href="custom-action-type-51.md">Custom Action Type 51</a> can be property and directory assignment custom actions.</span></span></li>
<li><span data-ttu-id="3bb9c-175">2-ignorare le azioni personalizzate immediate che non rientrano nelle assegnazioni di proprietà o directory.</span><span class="sxs-lookup"><span data-stu-id="3bb9c-175">2 - Skip immediate custom actions that do not fall into the property or directory assignments.</span></span> <span data-ttu-id="3bb9c-176">Le azioni personalizzate immediate non includono l'opzione msidbCustomActionTypeInScript nella colonna Type della <a href="customaction-table.md">tabella CustomAction</a>.</span><span class="sxs-lookup"><span data-stu-id="3bb9c-176">The immediate custom actions do not include msidbCustomActionTypeInScript option in the Type column of the <a href="customaction-table.md">CustomAction Table</a>.</span></span></li>
<li><span data-ttu-id="3bb9c-177">4-ignorare le azioni personalizzate eseguite all'interno dello script.</span><span class="sxs-lookup"><span data-stu-id="3bb9c-177">4 - Skip custom actions that run within the script.</span></span></li>
</ul>
<span data-ttu-id="3bb9c-178">Il valore di OptimizeCA deve essere lo stesso per tutte le patch installate o non viene ignorata alcuna azione personalizzata.</span><span class="sxs-lookup"><span data-stu-id="3bb9c-178">The value of OptimizeCA must be the same for all patches that are being installed or no custom actions are skipped.</span></span> <span data-ttu-id="3bb9c-179">Se, ad esempio, vengono installate due patch e OptimizeCA è impostato rispettivamente sui valori 1 e 2, nessuna azione personalizzata verrà ignorata.</span><span class="sxs-lookup"><span data-stu-id="3bb9c-179">For example, if two patches are being installed, and OptimizeCA is set to the values 1 and 2 respectively, no custom actions are skipped.</span></span> <br/> <span data-ttu-id="3bb9c-180">I valori di OptimizeCA possono essere combinati quando si elaborano più nuove patch.</span><span class="sxs-lookup"><span data-stu-id="3bb9c-180">The values of OptimizeCA can be combined when processing multiple new patches.</span></span> <span data-ttu-id="3bb9c-181">Se tutte le patch hanno un 1 (uno) incluso nei valori, tutte le azioni personalizzate di assegnazione di proprietà e directory vengono ignorate.</span><span class="sxs-lookup"><span data-stu-id="3bb9c-181">If all patches have a 1 (one) included in the values, then all property and directory assignment custom actions are skipped.</span></span> <span data-ttu-id="3bb9c-182">Se una patch ha il valore 3 (tre) per la proprietà e una patch ha il valore 1 (uno) per la proprietà, le azioni personalizzate di assegnazione di directory e proprietà vengono ignorate.</span><span class="sxs-lookup"><span data-stu-id="3bb9c-182">If one patch has the value 3 (three)for the property, and one patch has the value 1 (one) for the property, the property and directory assignment custom actions are skipped.</span></span> <span data-ttu-id="3bb9c-183">Tuttavia, l'altra azione personalizzata immediata viene eseguita, perché non tutte le patch richieste vengono ignorate.</span><span class="sxs-lookup"><span data-stu-id="3bb9c-183">However, the other immediate custom actions run, because not all of the patches requested are skipped.</span></span> <br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3bb9c-184">OptimizedInstallMode</span><span class="sxs-lookup"><span data-stu-id="3bb9c-184">OptimizedInstallMode</span></span></td>
<td><span data-ttu-id="3bb9c-185">Se questa proprietà è impostata su 1 (una) in tutte le patch da applicare in una transazione, un'applicazione della patch viene ottimizzata, se possibile.</span><span class="sxs-lookup"><span data-stu-id="3bb9c-185">If this property is set to 1 (one) in all the patches to be applied in a transaction, an application of the patch is optimized if possible.</span></span> <span data-ttu-id="3bb9c-186">Per altre informazioni, vedere <a href="patch-optimization.md">ottimizzazione della patch</a>.</span><span class="sxs-lookup"><span data-stu-id="3bb9c-186">For more information, see <a href="patch-optimization.md">Patch Optimization</a>.</span></span> <span data-ttu-id="3bb9c-187">Disponibile a partire da Windows Installer 3,1.</span><span class="sxs-lookup"><span data-stu-id="3bb9c-187">Available beginning with Windows Installer 3.1.</span></span></td>
</tr>
</tbody>
</table>



 

## <a name="validation"></a><span data-ttu-id="3bb9c-188">Convalida</span><span class="sxs-lookup"><span data-stu-id="3bb9c-188">Validation</span></span>

<dl>

[<span data-ttu-id="3bb9c-189">ICE03</span><span class="sxs-lookup"><span data-stu-id="3bb9c-189">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="3bb9c-190">ICE06</span><span class="sxs-lookup"><span data-stu-id="3bb9c-190">ICE06</span></span>](ice06.md)  
</dl>

## <a name="related-topics"></a><span data-ttu-id="3bb9c-191">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="3bb9c-191">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3bb9c-192">Non supportato in Windows Installer 2,0 e versioni precedenti</span><span class="sxs-lookup"><span data-stu-id="3bb9c-192">Not Supported in Windows Installer 2.0 and earlier</span></span>](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 




