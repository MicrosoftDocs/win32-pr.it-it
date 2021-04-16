---
description: La tabella CompLocator contiene le informazioni necessarie per trovare un file o una directory che usa i dati di configurazione del programma di installazione.
ms.assetid: 8b527307-51bf-47b3-a0b2-3421cc5278b7
title: Tabella CompLocator
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5e9fcb4a3c4f2e2c6f3ca3c92f6dc7466326bd11
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104530240"
---
# <a name="complocator-table"></a><span data-ttu-id="6751a-103">Tabella CompLocator</span><span class="sxs-lookup"><span data-stu-id="6751a-103">CompLocator Table</span></span>

<span data-ttu-id="6751a-104">La tabella CompLocator contiene le informazioni necessarie per trovare un file o una directory che usa i dati di configurazione del programma di installazione.</span><span class="sxs-lookup"><span data-stu-id="6751a-104">The CompLocator Table contains the information needed to find a file or directory that is using the installer configuration data.</span></span>

<span data-ttu-id="6751a-105">La tabella CompLocator contiene le informazioni seguenti.</span><span class="sxs-lookup"><span data-stu-id="6751a-105">The CompLocator table contains the following information.</span></span>



| <span data-ttu-id="6751a-106">Colonna</span><span class="sxs-lookup"><span data-stu-id="6751a-106">Column</span></span>      | <span data-ttu-id="6751a-107">Tipo</span><span class="sxs-lookup"><span data-stu-id="6751a-107">Type</span></span>                         | <span data-ttu-id="6751a-108">Chiave</span><span class="sxs-lookup"><span data-stu-id="6751a-108">Key</span></span> | <span data-ttu-id="6751a-109">Nullable</span><span class="sxs-lookup"><span data-stu-id="6751a-109">Nullable</span></span> |
|-------------|------------------------------|-----|----------|
| <span data-ttu-id="6751a-110">Firma\_</span><span class="sxs-lookup"><span data-stu-id="6751a-110">Signature\_</span></span> | [<span data-ttu-id="6751a-111">Identificatore</span><span class="sxs-lookup"><span data-stu-id="6751a-111">Identifier</span></span>](identifier.md) | <span data-ttu-id="6751a-112">S</span><span class="sxs-lookup"><span data-stu-id="6751a-112">Y</span></span>   | <span data-ttu-id="6751a-113">N</span><span class="sxs-lookup"><span data-stu-id="6751a-113">N</span></span>        |
| <span data-ttu-id="6751a-114">ComponentId</span><span class="sxs-lookup"><span data-stu-id="6751a-114">ComponentId</span></span> | [<span data-ttu-id="6751a-115">GUID</span><span class="sxs-lookup"><span data-stu-id="6751a-115">GUID</span></span>](guid.md)             | <span data-ttu-id="6751a-116">N</span><span class="sxs-lookup"><span data-stu-id="6751a-116">N</span></span>   | <span data-ttu-id="6751a-117">N</span><span class="sxs-lookup"><span data-stu-id="6751a-117">N</span></span>        |
| <span data-ttu-id="6751a-118">Tipo</span><span class="sxs-lookup"><span data-stu-id="6751a-118">Type</span></span>        | [<span data-ttu-id="6751a-119">Integer</span><span class="sxs-lookup"><span data-stu-id="6751a-119">Integer</span></span>](integer.md)       | <span data-ttu-id="6751a-120">N</span><span class="sxs-lookup"><span data-stu-id="6751a-120">N</span></span>   | <span data-ttu-id="6751a-121">S</span><span class="sxs-lookup"><span data-stu-id="6751a-121">Y</span></span>        |



 

## <a name="column-information"></a><span data-ttu-id="6751a-122">Informazioni sulle colonne</span><span class="sxs-lookup"><span data-stu-id="6751a-122">Column Information</span></span>

<dl> <dt>

<span data-ttu-id="6751a-123"><span id="Signature_"></span><span id="signature_"></span><span id="SIGNATURE_"></span>Firma\_</span><span class="sxs-lookup"><span data-stu-id="6751a-123"><span id="Signature_"></span><span id="signature_"></span><span id="SIGNATURE_"></span>Signature\_</span></span>
</dt> <dd>

<span data-ttu-id="6751a-124">Questa colonna rappresenta una firma del file univoca ed è anche la chiave esterna nella [tabella della firma](signature-table.md).</span><span class="sxs-lookup"><span data-stu-id="6751a-124">This column represents a unique file signature and is also the external key into the [Signature Table](signature-table.md).</span></span> <span data-ttu-id="6751a-125">Se la chiave è assente dalla tabella di firma, si presuppone che la ricerca sia per la presenza di una directory a cui punta la tabella CompLocator.</span><span class="sxs-lookup"><span data-stu-id="6751a-125">If the key is absent from the Signature Table, the search is assumed to be for the presence of a directory pointed to by the CompLocator Table.</span></span>

</dd> <dt>

<span data-ttu-id="6751a-126"><span id="ComponentId"></span><span id="componentid"></span><span id="COMPONENTID"></span>ComponentId</span><span class="sxs-lookup"><span data-stu-id="6751a-126"><span id="ComponentId"></span><span id="componentid"></span><span id="COMPONENTID"></span>ComponentId</span></span>
</dt> <dd>

<span data-ttu-id="6751a-127">ID del componente il cui percorso della chiave deve essere utilizzato per la ricerca.</span><span class="sxs-lookup"><span data-stu-id="6751a-127">The component ID of the component whose key path is to be used for the search.</span></span> <span data-ttu-id="6751a-128">Deve corrispondere al GUID di un componente visualizzato nel campo ComponentId della [tabella Component](component-table.md).</span><span class="sxs-lookup"><span data-stu-id="6751a-128">This should be the GUID of a component that appears in the ComponentId field of the [Component Table](component-table.md).</span></span> <span data-ttu-id="6751a-129">Potrebbe trattarsi dell'ID componente di un componente che appartiene a un altro prodotto installato nel computer.</span><span class="sxs-lookup"><span data-stu-id="6751a-129">It may be the component ID of a component belonging to another product installed on the computer.</span></span> <span data-ttu-id="6751a-130">Non deve essere il GUID di un componente Pubblicato visualizzato nel campo ComponentId della [tabella PublishComponent](publishcomponent-table.md).</span><span class="sxs-lookup"><span data-stu-id="6751a-130">It should not be the GUID of a published component appearing in the ComponentId field of the [PublishComponent Table](publishcomponent-table.md).</span></span>

<span data-ttu-id="6751a-131">Per trovare il valore GUID ID componente per un file installato da un altro prodotto, passare al pacchetto di installazione del prodotto.</span><span class="sxs-lookup"><span data-stu-id="6751a-131">To find the component ID GUID value for a file installed by another product, go to the installation package of the product.</span></span> <span data-ttu-id="6751a-132">Passare alla [tabella file](file-table.md) e individuare la riga che contiene l'identificatore del file.</span><span class="sxs-lookup"><span data-stu-id="6751a-132">Go to the [File Table](file-table.md) and find the row that contains the file identifier for the file.</span></span> <span data-ttu-id="6751a-133">La \_ colonna Component di questa riga contiene l'identificatore del componente per il componente che controlla il file.</span><span class="sxs-lookup"><span data-stu-id="6751a-133">The Component\_ column of this row contains the component identifier for the component that controls the file.</span></span> <span data-ttu-id="6751a-134">Passare alla [tabella dei componenti](component-table.md) e trovare la riga che contiene l'identificatore del componente nella colonna componente.</span><span class="sxs-lookup"><span data-stu-id="6751a-134">Go to the [Component table](component-table.md) and find the row that contains this component identifier in the Component column.</span></span> <span data-ttu-id="6751a-135">La colonna ComponentId di questa riga contiene il GUID ID componente.</span><span class="sxs-lookup"><span data-stu-id="6751a-135">The ComponentId column of this row contains the component ID GUID.</span></span>

</dd> <dt>

<span data-ttu-id="6751a-136"><span id="Type"></span><span id="type"></span><span id="TYPE"></span>Tipo</span><span class="sxs-lookup"><span data-stu-id="6751a-136"><span id="Type"></span><span id="type"></span><span id="TYPE"></span>Type</span></span>
</dt> <dd>

<span data-ttu-id="6751a-137">Valore booleano che determina se il percorso della chiave del componente è un nome file o un percorso di directory.</span><span class="sxs-lookup"><span data-stu-id="6751a-137">A Boolean value that determines if the key path of the component is a file name or a directory location.</span></span>

<span data-ttu-id="6751a-138">Nella tabella seguente sono elencati i valori validi.</span><span class="sxs-lookup"><span data-stu-id="6751a-138">The following table lists valid values.</span></span> <span data-ttu-id="6751a-139">Se assente, Type è impostato su 1 (uno).</span><span class="sxs-lookup"><span data-stu-id="6751a-139">If absent, Type is set to be 1 (one).</span></span>



| <span data-ttu-id="6751a-140">Costante</span><span class="sxs-lookup"><span data-stu-id="6751a-140">Constant</span></span>                      | <span data-ttu-id="6751a-141">Valore esadecimale</span><span class="sxs-lookup"><span data-stu-id="6751a-141">Hexadecimal</span></span> | <span data-ttu-id="6751a-142">Decimal</span><span class="sxs-lookup"><span data-stu-id="6751a-142">Decimal</span></span> | <span data-ttu-id="6751a-143">Descrizione</span><span class="sxs-lookup"><span data-stu-id="6751a-143">Description</span></span>              |
|-------------------------------|-------------|---------|--------------------------|
| <span data-ttu-id="6751a-144">**msidbLocatorTypeDirectory**</span><span class="sxs-lookup"><span data-stu-id="6751a-144">**msidbLocatorTypeDirectory**</span></span> | <span data-ttu-id="6751a-145">0x000</span><span class="sxs-lookup"><span data-stu-id="6751a-145">0x000</span></span>       | <span data-ttu-id="6751a-146">0</span><span class="sxs-lookup"><span data-stu-id="6751a-146">0</span></span>       | <span data-ttu-id="6751a-147">Il percorso della chiave è una directory.</span><span class="sxs-lookup"><span data-stu-id="6751a-147">Key path is a directory.</span></span> |
| <span data-ttu-id="6751a-148">**msidbLocatorTypeFileName**</span><span class="sxs-lookup"><span data-stu-id="6751a-148">**msidbLocatorTypeFileName**</span></span>  | <span data-ttu-id="6751a-149">0x001</span><span class="sxs-lookup"><span data-stu-id="6751a-149">0x001</span></span>       | <span data-ttu-id="6751a-150">1</span><span class="sxs-lookup"><span data-stu-id="6751a-150">1</span></span>       | <span data-ttu-id="6751a-151">Il percorso della chiave è un nome di file.</span><span class="sxs-lookup"><span data-stu-id="6751a-151">Key path is a file name.</span></span> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="6751a-152">Commenti</span><span class="sxs-lookup"><span data-stu-id="6751a-152">Remarks</span></span>

<span data-ttu-id="6751a-153">Questa tabella viene utilizzata con la [tabella AppSearch](appsearch-table.md).</span><span class="sxs-lookup"><span data-stu-id="6751a-153">This table is used with the [AppSearch Table](appsearch-table.md).</span></span>

<span data-ttu-id="6751a-154">In genere, le colonne in questa tabella non sono localizzate.</span><span class="sxs-lookup"><span data-stu-id="6751a-154">Typically, the columns in this table are not localized.</span></span> <span data-ttu-id="6751a-155">Se un autore decide di cercare i prodotti in più lingue, è possibile che nella tabella sia inclusa una voce separata per ogni lingua.</span><span class="sxs-lookup"><span data-stu-id="6751a-155">If an author decides to search for products in multiple languages, then there can be a separate entry included in the table for each language.</span></span>

<span data-ttu-id="6751a-156">Per ulteriori informazioni, vedere [ricerca di applicazioni esistenti, file, voci del registro di sistema o voci del file ini](searching-for-existing-applications-files-registry-entries-or--ini-file-entries.md).</span><span class="sxs-lookup"><span data-stu-id="6751a-156">For more information, see [Searching for Existing Applications, Files, Registry Entries or .ini File Entries](searching-for-existing-applications-files-registry-entries-or--ini-file-entries.md).</span></span>

## <a name="validation"></a><span data-ttu-id="6751a-157">Convalida</span><span class="sxs-lookup"><span data-stu-id="6751a-157">Validation</span></span>

<dl>

[<span data-ttu-id="6751a-158">ICE03</span><span class="sxs-lookup"><span data-stu-id="6751a-158">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="6751a-159">ICE06</span><span class="sxs-lookup"><span data-stu-id="6751a-159">ICE06</span></span>](ice06.md)  
</dl>

 

 



