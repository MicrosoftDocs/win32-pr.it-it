---
description: ICE35 convalida che i componenti contenenti file compressi archiviati in un file CAB non siano impostati per l'esecuzione dall'origine. Con Windows Installer 2,0 o versione successiva, questa restrizione è stata rimossa.
ms.assetid: b4df27e2-9790-4b18-a173-25fa8b0ecd4d
title: ICE35
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cea6a98079d3c57e0c796332cf0cd5f11045a07b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103967790"
---
# <a name="ice35"></a><span data-ttu-id="0881a-104">ICE35</span><span class="sxs-lookup"><span data-stu-id="0881a-104">ICE35</span></span>

<span data-ttu-id="0881a-105">ICE35 convalida che i componenti contenenti file compressi archiviati in un [file CAB](cabinet-files.md) non siano impostati per l'esecuzione dall'origine.</span><span class="sxs-lookup"><span data-stu-id="0881a-105">ICE35 validates that components containing compressed files stored in a [cabinet file](cabinet-files.md) are not set to run from source.</span></span> <span data-ttu-id="0881a-106">Con Windows Installer 2,0 o versione successiva, questa restrizione è stata rimossa.</span><span class="sxs-lookup"><span data-stu-id="0881a-106">With Windows Installer 2.0 or later, this restriction has been removed.</span></span>

<span data-ttu-id="0881a-107">ICE35 esegue una query sulla colonna CAB della [tabella dei supporti](media-table.md) per determinare quali file vengono compressi e archiviati in un file CAB.</span><span class="sxs-lookup"><span data-stu-id="0881a-107">ICE35 queries the Cabinet column of the [Media table](media-table.md) to determine which files are compressed and stored in a cabinet file.</span></span> <span data-ttu-id="0881a-108">Viene eseguita una query sulla [tabella file](file-table.md) per determinare quali componenti contengono questi file.</span><span class="sxs-lookup"><span data-stu-id="0881a-108">It queries the [File table](file-table.md) to determine which components contain these files.</span></span> <span data-ttu-id="0881a-109">Infine, viene controllata la [tabella dei componenti](component-table.md) per determinare se i bit dell'esecuzione dall'origine sono impostati nella colonna attributi.</span><span class="sxs-lookup"><span data-stu-id="0881a-109">Finally, it checks the [Component table](component-table.md) to determine whether the run-from-source bits are set in the Attributes column.</span></span>

## <a name="result"></a><span data-ttu-id="0881a-110">Risultato</span><span class="sxs-lookup"><span data-stu-id="0881a-110">Result</span></span>

<span data-ttu-id="0881a-111">ICE35 Invia un messaggio di errore se è presente un file compresso archiviato in un file CAB appartenente a un componente con il bit msidbComponentAttributesSourceOnly impostato nella colonna attributi della [tabella dei componenti](component-table.md).</span><span class="sxs-lookup"><span data-stu-id="0881a-111">ICE35 posts an error message if there is a compressed file stored in a cabinet file belonging to a component with the msidbComponentAttributesSourceOnly bit set in the Attributes column of the [Component table](component-table.md).</span></span> <span data-ttu-id="0881a-112">Con Windows Installer 2,0 o versioni successive, questo valore viene modificato da un errore in un messaggio di avviso.</span><span class="sxs-lookup"><span data-stu-id="0881a-112">With Windows Installer 2.0 or later, this is changed from an error to a warning message.</span></span> <span data-ttu-id="0881a-113">Un pacchetto che supporta solo Windows Installer 2,0 e versioni successive presenta la \_ Proprietà PID PageCount del flusso di informazioni di riepilogo impostato su un valore pari ad almeno 200.</span><span class="sxs-lookup"><span data-stu-id="0881a-113">A package that supports only Windows Installer 2.0 and later has the PID\_PAGECOUNT property of the Summary Information Stream set to a value of at least 200.</span></span>

<span data-ttu-id="0881a-114">ICE35 Invia un messaggio di avviso se è presente un file compresso archiviato in un file CAB appartenente a un componente con il bit msidbComponentAttributesOptional impostato nella colonna attributi della [tabella dei componenti](component-table.md).</span><span class="sxs-lookup"><span data-stu-id="0881a-114">ICE35 posts warning message if there is a compressed file stored in a cabinet file belonging to a component with the msidbComponentAttributesOptional bit set in the Attributes column of the [Component table](component-table.md).</span></span> <span data-ttu-id="0881a-115">Questo messaggio di avviso è stato rimosso con Windows Installer 2,0 e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="0881a-115">This warning message has been removed with Windows Installer 2.0 and later.</span></span>

<span data-ttu-id="0881a-116">Se più file in un componente si trovano in un file CAB, ICE35 segnala gli errori per ogni file con l'esecuzione dal set di bit di origine.</span><span class="sxs-lookup"><span data-stu-id="0881a-116">If multiple files in a component are in a cabinet file, ICE35 reports errors for each file that has the run from source bit set.</span></span>

## <a name="example"></a><span data-ttu-id="0881a-117">Esempio</span><span class="sxs-lookup"><span data-stu-id="0881a-117">Example</span></span>

<span data-ttu-id="0881a-118">ICE35 segnala gli errori e gli avvisi seguenti per l'esempio illustrato con una versione precedente alla Windows Installer versione 2,0.</span><span class="sxs-lookup"><span data-stu-id="0881a-118">ICE35 reports the following errors and warnings for the example shown using a version earlier than Windows Installer version 2.0.</span></span>



| <span data-ttu-id="0881a-119">Errore ICE35</span><span class="sxs-lookup"><span data-stu-id="0881a-119">ICE35 Error</span></span>                                                                                                | <span data-ttu-id="0881a-120">Descrizione</span><span class="sxs-lookup"><span data-stu-id="0881a-120">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
|------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0881a-121">ERRORE: il componente Component3 non può essere eseguito solo dall'origine perché il file membro ' file3' è compresso.</span><span class="sxs-lookup"><span data-stu-id="0881a-121">ERROR: Component Component3 cannot be Run From Source only, because its member file 'File3' is compressed.</span></span> | <span data-ttu-id="0881a-122">È presente un file compresso archiviato in un file CAB e questo file appartiene a un componente con il bit SourceOnly impostato nella colonna attributi della tabella dei [componenti](component-table.md).</span><span class="sxs-lookup"><span data-stu-id="0881a-122">There is a compressed file stored in a cabinet file and this file belongs to a component with the SourceOnly bit set in the Attributes column of the [Component table](component-table.md).</span></span> <span data-ttu-id="0881a-123">Per correggere questo errore, modificare i 2 bit inferiori del valore degli attributi Component2's in "00", vale a dire solo locale, oppure rimuovere file4 dal file CAB.</span><span class="sxs-lookup"><span data-stu-id="0881a-123">To fix this error change the lower 2 bits of Component2's Attributes value to "00", meaning Local only, or remove File4 from the CAB file.</span></span><br/>                                                                                                                                                                         |
| <span data-ttu-id="0881a-124">ERRORE: il componente Component3 non può essere eseguito solo dall'origine perché il file membro ' file3' è compresso.</span><span class="sxs-lookup"><span data-stu-id="0881a-124">ERROR: Component Component3 cannot be Run From Source only, because its member file 'File3' is compressed.</span></span> | <span data-ttu-id="0881a-125">È presente un file compresso archiviato in un file CAB e questo file appartiene a un componente con il bit SourceOnly impostato nella colonna attributi della tabella dei [componenti](component-table.md).</span><span class="sxs-lookup"><span data-stu-id="0881a-125">There is a compressed file stored in a cabinet file and this file belongs to a component with the SourceOnly bit set in the Attributes column of the [Component table](component-table.md).</span></span> <span data-ttu-id="0881a-126">Poiché i file in un componente non devono essere tutti originati dallo stesso supporto, ICE35 segnala gli errori per ogni file nel componente che si trova in un file CAB.</span><span class="sxs-lookup"><span data-stu-id="0881a-126">Because the files in a component do not all have to originate from the same media, ICE35 reports errors for each file in the component that is in a cabinet.</span></span><br/> <span data-ttu-id="0881a-127">Per correggere questo errore, modificare i 2 bit inferiori del valore degli attributi Component2's in "00", vale a dire solo locale, oppure rimuovere file4 dal file CAB.</span><span class="sxs-lookup"><span data-stu-id="0881a-127">To fix this error change the lower 2 bits of Component2's Attributes value to "00", meaning Local only, or remove File4 from the CAB file.</span></span><br/> |



 

<span data-ttu-id="0881a-128">[Tabella media](media-table.md) (parziale)</span><span class="sxs-lookup"><span data-stu-id="0881a-128">[Media Table](media-table.md) (partial)</span></span>



| <span data-ttu-id="0881a-129">DiskID</span><span class="sxs-lookup"><span data-stu-id="0881a-129">DiskID</span></span> | <span data-ttu-id="0881a-130">LastSequence</span><span class="sxs-lookup"><span data-stu-id="0881a-130">LastSequence</span></span> | <span data-ttu-id="0881a-131">CAB</span><span class="sxs-lookup"><span data-stu-id="0881a-131">Cabinet</span></span>   |
|--------|--------------|-----------|
| <span data-ttu-id="0881a-132">1</span><span class="sxs-lookup"><span data-stu-id="0881a-132">1</span></span>      | <span data-ttu-id="0881a-133">2</span><span class="sxs-lookup"><span data-stu-id="0881a-133">2</span></span>            |           |
| <span data-ttu-id="0881a-134">2</span><span class="sxs-lookup"><span data-stu-id="0881a-134">2</span></span>      | <span data-ttu-id="0881a-135">4</span><span class="sxs-lookup"><span data-stu-id="0881a-135">4</span></span>            | <span data-ttu-id="0881a-136">One.cab</span><span class="sxs-lookup"><span data-stu-id="0881a-136">One.cab</span></span>   |
| <span data-ttu-id="0881a-137">3</span><span class="sxs-lookup"><span data-stu-id="0881a-137">3</span></span>      | <span data-ttu-id="0881a-138">5</span><span class="sxs-lookup"><span data-stu-id="0881a-138">5</span></span>            | <span data-ttu-id="0881a-139">\#Two.cab</span><span class="sxs-lookup"><span data-stu-id="0881a-139">\#Two.cab</span></span> |



 

<span data-ttu-id="0881a-140">[Tabella file](file-table.md) (parziale)</span><span class="sxs-lookup"><span data-stu-id="0881a-140">[File Table](file-table.md) (partial)</span></span>



| <span data-ttu-id="0881a-141">File</span><span class="sxs-lookup"><span data-stu-id="0881a-141">File</span></span>  | <span data-ttu-id="0881a-142">Componente\_</span><span class="sxs-lookup"><span data-stu-id="0881a-142">Component\_</span></span> | <span data-ttu-id="0881a-143">Sequenza</span><span class="sxs-lookup"><span data-stu-id="0881a-143">Sequence</span></span> |
|-------|-------------|----------|
| <span data-ttu-id="0881a-144">File1</span><span class="sxs-lookup"><span data-stu-id="0881a-144">File1</span></span> | <span data-ttu-id="0881a-145">Component1</span><span class="sxs-lookup"><span data-stu-id="0881a-145">Component1</span></span>  | <span data-ttu-id="0881a-146">1</span><span class="sxs-lookup"><span data-stu-id="0881a-146">1</span></span>        |
| <span data-ttu-id="0881a-147">File2</span><span class="sxs-lookup"><span data-stu-id="0881a-147">File2</span></span> | <span data-ttu-id="0881a-148">Component2</span><span class="sxs-lookup"><span data-stu-id="0881a-148">Component2</span></span>  | <span data-ttu-id="0881a-149">2</span><span class="sxs-lookup"><span data-stu-id="0881a-149">2</span></span>        |
| <span data-ttu-id="0881a-150">File3</span><span class="sxs-lookup"><span data-stu-id="0881a-150">File3</span></span> | <span data-ttu-id="0881a-151">Component2</span><span class="sxs-lookup"><span data-stu-id="0881a-151">Component2</span></span>  | <span data-ttu-id="0881a-152">3</span><span class="sxs-lookup"><span data-stu-id="0881a-152">3</span></span>        |
| <span data-ttu-id="0881a-153">File4</span><span class="sxs-lookup"><span data-stu-id="0881a-153">File4</span></span> | <span data-ttu-id="0881a-154">Component3</span><span class="sxs-lookup"><span data-stu-id="0881a-154">Component3</span></span>  | <span data-ttu-id="0881a-155">4</span><span class="sxs-lookup"><span data-stu-id="0881a-155">4</span></span>        |
| <span data-ttu-id="0881a-156">File5</span><span class="sxs-lookup"><span data-stu-id="0881a-156">File5</span></span> | <span data-ttu-id="0881a-157">Component3</span><span class="sxs-lookup"><span data-stu-id="0881a-157">Component3</span></span>  | <span data-ttu-id="0881a-158">5</span><span class="sxs-lookup"><span data-stu-id="0881a-158">5</span></span>        |



 

<span data-ttu-id="0881a-159">[Tabella componenti](component-table.md) (parziale)</span><span class="sxs-lookup"><span data-stu-id="0881a-159">[Component Table](component-table.md) (partial)</span></span>



| <span data-ttu-id="0881a-160">Componente</span><span class="sxs-lookup"><span data-stu-id="0881a-160">Component</span></span>  | <span data-ttu-id="0881a-161">Attributi</span><span class="sxs-lookup"><span data-stu-id="0881a-161">Attributes</span></span> |
|------------|------------|
| <span data-ttu-id="0881a-162">Component1</span><span class="sxs-lookup"><span data-stu-id="0881a-162">Component1</span></span> | <span data-ttu-id="0881a-163">0</span><span class="sxs-lookup"><span data-stu-id="0881a-163">0</span></span>          |
| <span data-ttu-id="0881a-164">Component2</span><span class="sxs-lookup"><span data-stu-id="0881a-164">Component2</span></span> | <span data-ttu-id="0881a-165">2</span><span class="sxs-lookup"><span data-stu-id="0881a-165">2</span></span>          |
| <span data-ttu-id="0881a-166">Component3</span><span class="sxs-lookup"><span data-stu-id="0881a-166">Component3</span></span> | <span data-ttu-id="0881a-167">1</span><span class="sxs-lookup"><span data-stu-id="0881a-167">1</span></span>          |



 

<span data-ttu-id="0881a-168">[Tabella collegamenti](shortcut-table.md) (parziale)</span><span class="sxs-lookup"><span data-stu-id="0881a-168">[Shortcut Table](shortcut-table.md) (partial)</span></span>



| <span data-ttu-id="0881a-169">Tasto di scelta rapida</span><span class="sxs-lookup"><span data-stu-id="0881a-169">Shortcut</span></span>  | <span data-ttu-id="0881a-170">Icona\_</span><span class="sxs-lookup"><span data-stu-id="0881a-170">Icon\_</span></span> |
|-----------|--------|
| <span data-ttu-id="0881a-171">Shortcut1</span><span class="sxs-lookup"><span data-stu-id="0881a-171">Shortcut1</span></span> | <span data-ttu-id="0881a-172">Icon2</span><span class="sxs-lookup"><span data-stu-id="0881a-172">Icon2</span></span>  |



 

<span data-ttu-id="0881a-173">Si noti che i file possono anche essere contrassegnati come compressi usando la proprietà di [**Riepilogo di Word Count**](word-count-summary.md) del [flusso di informazioni di riepilogo](summary-information-stream.md).</span><span class="sxs-lookup"><span data-stu-id="0881a-173">Note that files can also be marked as compressed using the [**Word Count Summary**](word-count-summary.md) Property of the [Summary Information stream](summary-information-stream.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="0881a-174">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="0881a-174">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0881a-175">Riferimento ghiaccio</span><span class="sxs-lookup"><span data-stu-id="0881a-175">ICE Reference</span></span>](ice-reference.md)
</dt> </dl>

 

 




