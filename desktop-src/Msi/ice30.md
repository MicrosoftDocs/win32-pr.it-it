---
description: ICE30 verifica che l'installazione dei componenti contenenti lo stesso file non installi mai il file più di una volta nella stessa directory.
ms.assetid: 74cb455b-a53e-4c6b-98ff-08cf0858f11f
title: ICE30
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 78fa96899231015d864e5a0912b8ff73cedbbe75
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106314225"
---
# <a name="ice30"></a><span data-ttu-id="b1d91-103">ICE30</span><span class="sxs-lookup"><span data-stu-id="b1d91-103">ICE30</span></span>

<span data-ttu-id="b1d91-104">ICE30 verifica che l'installazione dei componenti contenenti lo stesso file non installi mai il file più di una volta nella stessa directory.</span><span class="sxs-lookup"><span data-stu-id="b1d91-104">ICE30 validates that the installation of components containing the same file never installs the file more than once in the same directory.</span></span>

<span data-ttu-id="b1d91-105">ICE30 passa a tutti i componenti della [tabella dei componenti](component-table.md) e quindi determina la directory di destinazione del componente dalla [tabella di directory](directory-table.md).</span><span class="sxs-lookup"><span data-stu-id="b1d91-105">ICE30 goes to every component in the [Component table](component-table.md) and then determines the component's target directory from the [Directory table](directory-table.md).</span></span> <span data-ttu-id="b1d91-106">Verifica quindi quale di questi componenti viene installato nella stessa directory di destinazione.</span><span class="sxs-lookup"><span data-stu-id="b1d91-106">It then checks to see which of these components install to the same target directory.</span></span> <span data-ttu-id="b1d91-107">Infine, utilizza la [tabella file](file-table.md) per verificare che nessuno dei file presenti in questi componenti abbia lo stesso nome.</span><span class="sxs-lookup"><span data-stu-id="b1d91-107">Finally, it uses the [File table](file-table.md) to verify that none of the files in these components have the same name.</span></span>

<span data-ttu-id="b1d91-108">ICE30 controlla i nomi di file lunghi (LFN) e i nomi di file brevi (SFN).</span><span class="sxs-lookup"><span data-stu-id="b1d91-108">ICE30 checks both long file names (LFN) and short file names (SFN).</span></span>

<span data-ttu-id="b1d91-109">ICE30 non valuta le proprietà nella risoluzione delle directory perché queste proprietà possono cambiare in fase di esecuzione e modificare lo schema di risoluzione della directory.</span><span class="sxs-lookup"><span data-stu-id="b1d91-109">ICE30 does not evaluate properties in the resolution of directories because these properties can change at runtime and alter the directory resolution scheme.</span></span> <span data-ttu-id="b1d91-110">Ciò significa che ICE30 è in grado di rilevare conflitti di file a causa di directory con la stessa proprietà nei percorsi, ma non rileva conflitti che risultano da due proprietà con lo stesso valore.</span><span class="sxs-lookup"><span data-stu-id="b1d91-110">This means ICE30 can detect file collisions due to directories with the same property in their paths, but does not detect collisions resulting from two properties having the same value.</span></span>

## <a name="result"></a><span data-ttu-id="b1d91-111">Risultato</span><span class="sxs-lookup"><span data-stu-id="b1d91-111">Result</span></span>

<span data-ttu-id="b1d91-112">ICE30 Invia un messaggio di errore per ogni coppia di componenti che installa lo stesso file nella stessa directory.</span><span class="sxs-lookup"><span data-stu-id="b1d91-112">ICE30 posts an error message for each pair of components that installs the same file to the same directory.</span></span>

## <a name="example"></a><span data-ttu-id="b1d91-113">Esempio</span><span class="sxs-lookup"><span data-stu-id="b1d91-113">Example</span></span>

<span data-ttu-id="b1d91-114">L'esempio illustrato restituisce due volte gli errori seguenti.</span><span class="sxs-lookup"><span data-stu-id="b1d91-114">The example shown returns each of the following errors twice.</span></span>



| <span data-ttu-id="b1d91-115">Errore o avviso ICE30</span><span class="sxs-lookup"><span data-stu-id="b1d91-115">ICE30 error or warning</span></span>                                                                                                                                                                                                                                                                    | <span data-ttu-id="b1d91-116">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b1d91-116">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                    |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b1d91-117">ERRORE: il file di destinazione ' README. 1st ' è installato in ' TARGETDIR \\ Product ' da due componenti diversi in un sistema SFN:' Component1' è Component2'.</span><span class="sxs-lookup"><span data-stu-id="b1d91-117">ERROR: The target file 'README.1st' is installed in 'TARGETDIR\\PRODUCT' by two different components on an SFN system: 'Component1' and 'Component2'.</span></span> <span data-ttu-id="b1d91-118">Il conteggio dei riferimenti del componente viene interrotto.</span><span class="sxs-lookup"><span data-stu-id="b1d91-118">This breaks component reference counting.</span></span>                                                                                           | <span data-ttu-id="b1d91-119">Component1 e Component2 hanno entrambi un file denominato "reademe. 1st".</span><span class="sxs-lookup"><span data-stu-id="b1d91-119">Component1 and Component2 both have a file named 'READEME.1st'.</span></span> <span data-ttu-id="b1d91-120">Quando si usano nomi di file brevi, il programma di installazione installa sia dir1 che dir2 nella stessa directory, TARGETDIR \\ Product.</span><span class="sxs-lookup"><span data-stu-id="b1d91-120">When using short file names, the installer installs both Dir1 and Dir2 to the same directory, TARGETDIR\\PRODUCT.</span></span><br/> <span data-ttu-id="b1d91-121">ICE30 generano due errori, uno per ogni file.</span><span class="sxs-lookup"><span data-stu-id="b1d91-121">ICE30 generate two errors, one for each file.</span></span> <span data-ttu-id="b1d91-122">In un ambiente di creazione che Visualizza i percorsi degli errori, il primo errore si trova nella voce di un file nella [tabella file](file-table.md)e il secondo nella posizione dell'altro file.</span><span class="sxs-lookup"><span data-stu-id="b1d91-122">In an authoring environment that displays error locations, the first error is at one file's entry in the [File Table](file-table.md), and the second at the location of the other file.</span></span><br/> |
| <span data-ttu-id="b1d91-123">ERRORE: l'installazione di un componente condizionale comporterebbe l'installazione del file di destinazione ' README. 1st ' in ' TARGETDIR \\ Common Tools ' da due componenti diversi in un sistema LFN:' Component3' è Component4'.</span><span class="sxs-lookup"><span data-stu-id="b1d91-123">ERROR: Installation of a conditionalized component would cause the target file 'README.1st' to be installed in 'TARGETDIR\\COMMON TOOLS' by two different components on an LFN system: 'Component3' and 'Component4'.</span></span> <span data-ttu-id="b1d91-124">In questo modo si interrompe il conteggio dei riferimenti ai componenti.</span><span class="sxs-lookup"><span data-stu-id="b1d91-124">This would break component reference counting.</span></span>                      | <span data-ttu-id="b1d91-125">Component4 include una voce nella colonna Condition della [tabella Component](component-table.md) e Component3 No.</span><span class="sxs-lookup"><span data-stu-id="b1d91-125">Component4 has an entry in the Condition column of the [Component table](component-table.md) and Component3 does not.</span></span> <span data-ttu-id="b1d91-126">Se [**VersionNT**](versionnt.md) è true, Component4 è installato e si verifica un conflitto con il file Leggimi. 1 sempre installato da Component3.</span><span class="sxs-lookup"><span data-stu-id="b1d91-126">If [**VersionNT**](versionnt.md) is True, Component4 is installed, and there a collision with the Readme.1st always installed by Component3.</span></span><br/> <span data-ttu-id="b1d91-127">ICE30 genera 4 errori, una coppia per SFN, uno per LFN.</span><span class="sxs-lookup"><span data-stu-id="b1d91-127">ICE30 generates 4 errors, one pair for SFN, one for LFN.</span></span><br/>                                                                                            |
| <span data-ttu-id="b1d91-128">AVVISO: il file di destinazione ' README. 1st ' potrebbe essere installato in ' TARGETDIR \\ Common Tools ' da due diversi componenti condizionali in un sistema SFN:' Component4' è Component5'.</span><span class="sxs-lookup"><span data-stu-id="b1d91-128">WARNING: The target file 'README.1st' might be installed in 'TARGETDIR\\COMMON TOOLS' by two different conditionalized components on an SFN system: 'Component4' and 'Component5'.</span></span> <span data-ttu-id="b1d91-129">Se le condizioni non si escludono a vicenda, il sistema di conteggio dei riferimenti ai componenti verrà interrotta.</span><span class="sxs-lookup"><span data-stu-id="b1d91-129">If the conditions are not mutually exclusive, this will break the component reference counting system.</span></span> | <span data-ttu-id="b1d91-130">Poiché Component4 e Component5 contengono entrambe voci nella colonna condizione della tabella dei [componenti](component-table.md) , questo conflitto di file potrebbe non verificarsi.</span><span class="sxs-lookup"><span data-stu-id="b1d91-130">Because Component4 and Component5 both have entries in the Condition column of the [Component table](component-table.md) this file collision may not occur.</span></span> <span data-ttu-id="b1d91-131">ICE30 Invia un avviso solo perché le condizioni devono essere determinate al momento dell'installazione.</span><span class="sxs-lookup"><span data-stu-id="b1d91-131">ICE30 only posts a warning because the conditions must be determined at the time of the installation.</span></span><br/> <span data-ttu-id="b1d91-132">ICE30 genera 4 avvisi, una coppia per SFN, uno per LFN.</span><span class="sxs-lookup"><span data-stu-id="b1d91-132">ICE30 generates 4 warnings, one pair for SFN, one for LFN.</span></span><br/>                                                                                            |



 

<span data-ttu-id="b1d91-133">[Tabella componenti](component-table.md) (parziale)</span><span class="sxs-lookup"><span data-stu-id="b1d91-133">[Component Table](component-table.md) (partial)</span></span>



| <span data-ttu-id="b1d91-134">Componente</span><span class="sxs-lookup"><span data-stu-id="b1d91-134">Component</span></span>  | <span data-ttu-id="b1d91-135">Directory</span><span class="sxs-lookup"><span data-stu-id="b1d91-135">Directory</span></span> | <span data-ttu-id="b1d91-136">Condizione</span><span class="sxs-lookup"><span data-stu-id="b1d91-136">Condition</span></span> |
|------------|-----------|-----------|
| <span data-ttu-id="b1d91-137">Component1</span><span class="sxs-lookup"><span data-stu-id="b1d91-137">Component1</span></span> | <span data-ttu-id="b1d91-138">Dir1</span><span class="sxs-lookup"><span data-stu-id="b1d91-138">Dir1</span></span>      |           |
| <span data-ttu-id="b1d91-139">Component2</span><span class="sxs-lookup"><span data-stu-id="b1d91-139">Component2</span></span> | <span data-ttu-id="b1d91-140">Dir2</span><span class="sxs-lookup"><span data-stu-id="b1d91-140">Dir2</span></span>      |           |
| <span data-ttu-id="b1d91-141">Component3</span><span class="sxs-lookup"><span data-stu-id="b1d91-141">Component3</span></span> | <span data-ttu-id="b1d91-142">Dir3</span><span class="sxs-lookup"><span data-stu-id="b1d91-142">Dir3</span></span>      |           |
| <span data-ttu-id="b1d91-143">Component4</span><span class="sxs-lookup"><span data-stu-id="b1d91-143">Component4</span></span> | <span data-ttu-id="b1d91-144">Dir3</span><span class="sxs-lookup"><span data-stu-id="b1d91-144">Dir3</span></span>      | <span data-ttu-id="b1d91-145">VersionNT</span><span class="sxs-lookup"><span data-stu-id="b1d91-145">VersionNT</span></span> |
| <span data-ttu-id="b1d91-146">Component5</span><span class="sxs-lookup"><span data-stu-id="b1d91-146">Component5</span></span> | <span data-ttu-id="b1d91-147">Dir3</span><span class="sxs-lookup"><span data-stu-id="b1d91-147">Dir3</span></span>      | <span data-ttu-id="b1d91-148">Version9X</span><span class="sxs-lookup"><span data-stu-id="b1d91-148">Version9X</span></span> |



 

[<span data-ttu-id="b1d91-149">Tabella directory</span><span class="sxs-lookup"><span data-stu-id="b1d91-149">Directory Table</span></span>](directory-table.md)



| <span data-ttu-id="b1d91-150">Directory</span><span class="sxs-lookup"><span data-stu-id="b1d91-150">Directory</span></span> | <span data-ttu-id="b1d91-151">\_Directory padre</span><span class="sxs-lookup"><span data-stu-id="b1d91-151">Parent\_Directory</span></span> | <span data-ttu-id="b1d91-152">DefaultDir</span><span class="sxs-lookup"><span data-stu-id="b1d91-152">DefaultDir</span></span>                    |
|-----------|-------------------|-------------------------------|
| <span data-ttu-id="b1d91-153">SOURCEDIR</span><span class="sxs-lookup"><span data-stu-id="b1d91-153">SOURCEDIR</span></span> |                   | <span data-ttu-id="b1d91-154">TARGETDIR</span><span class="sxs-lookup"><span data-stu-id="b1d91-154">TARGETDIR</span></span>                     |
| <span data-ttu-id="b1d91-155">Dir1</span><span class="sxs-lookup"><span data-stu-id="b1d91-155">Dir1</span></span>      | <span data-ttu-id="b1d91-156">SOURCEDIR</span><span class="sxs-lookup"><span data-stu-id="b1d91-156">SOURCEDIR</span></span>         | <span data-ttu-id="b1d91-157">Prodotto \| Component1 prodotto:.</span><span class="sxs-lookup"><span data-stu-id="b1d91-157">Product\|Component1 Product:.</span></span> |
| <span data-ttu-id="b1d91-158">Dir2</span><span class="sxs-lookup"><span data-stu-id="b1d91-158">Dir2</span></span>      | <span data-ttu-id="b1d91-159">SOURCEDIR</span><span class="sxs-lookup"><span data-stu-id="b1d91-159">SOURCEDIR</span></span>         | <span data-ttu-id="b1d91-160">Prodotto:.</span><span class="sxs-lookup"><span data-stu-id="b1d91-160">Product:.</span></span>                     |
| <span data-ttu-id="b1d91-161">Dir3</span><span class="sxs-lookup"><span data-stu-id="b1d91-161">Dir3</span></span>      | <span data-ttu-id="b1d91-162">SOURCEDIR</span><span class="sxs-lookup"><span data-stu-id="b1d91-162">SOURCEDIR</span></span>         | <span data-ttu-id="b1d91-163">\|Strumenti comuni comuni:</span><span class="sxs-lookup"><span data-stu-id="b1d91-163">Common\|Common Tools:</span></span>         |



 

<span data-ttu-id="b1d91-164">[Tabella file](file-table.md) (parziale)</span><span class="sxs-lookup"><span data-stu-id="b1d91-164">[File Table](file-table.md) (partial)</span></span>



| <span data-ttu-id="b1d91-165">File</span><span class="sxs-lookup"><span data-stu-id="b1d91-165">File</span></span>  | <span data-ttu-id="b1d91-166">Componente\_</span><span class="sxs-lookup"><span data-stu-id="b1d91-166">Component\_</span></span> | <span data-ttu-id="b1d91-167">FileName</span><span class="sxs-lookup"><span data-stu-id="b1d91-167">FileName</span></span>   |
|-------|-------------|------------|
| <span data-ttu-id="b1d91-168">File1</span><span class="sxs-lookup"><span data-stu-id="b1d91-168">File1</span></span> | <span data-ttu-id="b1d91-169">Component1</span><span class="sxs-lookup"><span data-stu-id="b1d91-169">Component1</span></span>  | <span data-ttu-id="b1d91-170">FILE Leggimi. 1st</span><span class="sxs-lookup"><span data-stu-id="b1d91-170">README.1st</span></span> |
| <span data-ttu-id="b1d91-171">File2</span><span class="sxs-lookup"><span data-stu-id="b1d91-171">File2</span></span> | <span data-ttu-id="b1d91-172">Component2</span><span class="sxs-lookup"><span data-stu-id="b1d91-172">Component2</span></span>  | <span data-ttu-id="b1d91-173">FILE Leggimi. 1st</span><span class="sxs-lookup"><span data-stu-id="b1d91-173">README.1st</span></span> |
| <span data-ttu-id="b1d91-174">File3</span><span class="sxs-lookup"><span data-stu-id="b1d91-174">File3</span></span> | <span data-ttu-id="b1d91-175">Component3</span><span class="sxs-lookup"><span data-stu-id="b1d91-175">Component3</span></span>  | <span data-ttu-id="b1d91-176">FILE Leggimi. 1st</span><span class="sxs-lookup"><span data-stu-id="b1d91-176">README.1st</span></span> |
| <span data-ttu-id="b1d91-177">File4</span><span class="sxs-lookup"><span data-stu-id="b1d91-177">File4</span></span> | <span data-ttu-id="b1d91-178">Component4</span><span class="sxs-lookup"><span data-stu-id="b1d91-178">Component4</span></span>  | <span data-ttu-id="b1d91-179">FILE Leggimi. 1st</span><span class="sxs-lookup"><span data-stu-id="b1d91-179">README.1st</span></span> |
| <span data-ttu-id="b1d91-180">File5</span><span class="sxs-lookup"><span data-stu-id="b1d91-180">File5</span></span> | <span data-ttu-id="b1d91-181">Component5</span><span class="sxs-lookup"><span data-stu-id="b1d91-181">Component5</span></span>  | <span data-ttu-id="b1d91-182">FILE Leggimi. 1st</span><span class="sxs-lookup"><span data-stu-id="b1d91-182">README.1st</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="b1d91-183">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="b1d91-183">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b1d91-184">Riferimento ghiaccio</span><span class="sxs-lookup"><span data-stu-id="b1d91-184">ICE Reference</span></span>](ice-reference.md)
</dt> </dl>

 

 




