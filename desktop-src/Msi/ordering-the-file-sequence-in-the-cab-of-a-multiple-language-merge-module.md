---
description: È necessario creare moduli di Unione a più lingue, trasformazioni di linguaggio e file CAB in modo tale che l'ordine dei file corrisponda all'ordine specificato nella tabella file.
ms.assetid: c6ddf5fc-a7c5-49c1-899b-ff9fdff9c028
title: Ordinamento della sequenza di file nel file CAB di un modulo di Unione a più lingue
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 01bdd00d8b09c0605b7ddcf656d87d41e3f53776
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104234033"
---
# <a name="ordering-the-file-sequence-in-the-cab-of-a-multiple-language-merge-module"></a><span data-ttu-id="d25b5-103">Ordinamento della sequenza di file nel file CAB di un modulo di Unione a più lingue</span><span class="sxs-lookup"><span data-stu-id="d25b5-103">Ordering the File Sequence in the CAB of a Multiple Language Merge Module</span></span>

<span data-ttu-id="d25b5-104">È necessario creare moduli di Unione a più lingue, trasformazioni di linguaggio e file CAB in modo tale che l'ordine dei file nel file CAB corrisponda all'ordine di installazione dei file specificati nella [tabella dei file](file-table.md), anche dopo l'applicazione della trasformazione del linguaggio.</span><span class="sxs-lookup"><span data-stu-id="d25b5-104">Multiple-language merge modules, language transforms, and cabinet files must be authored such that the order of the files in the .cab matches the installation order of files specified in the [File Table](file-table.md), even after the application of the language transform.</span></span> <span data-ttu-id="d25b5-105">Se l'ordine nel modulo e nel file CAB non corrispondono, non è possibile usare il modulo merge.</span><span class="sxs-lookup"><span data-stu-id="d25b5-105">If the order in the module and in the .cab do not match, the merge module cannot be used.</span></span>

<span data-ttu-id="d25b5-106">Assegnare a ogni file nel modulo, un numero di sequenza univoco indipendente dalla lingua e quindi usare sempre il numero di sequenza per il file.</span><span class="sxs-lookup"><span data-stu-id="d25b5-106">Assign to each file in the module, a unique sequence number that is independent of its language, and then always use that sequence number for the file.</span></span> <span data-ttu-id="d25b5-107">Utilizzare la stessa sequenza quando si compila il file CAB e si crea una trasformazione di linguaggio.</span><span class="sxs-lookup"><span data-stu-id="d25b5-107">Use the same sequence when building the cabinet file and authoring a language transform.</span></span>

<span data-ttu-id="d25b5-108">Poiché il programma di installazione installa solo i file elencati nella [tabella file](file-table.md), l'utilizzo di una sequenza di file globale nel file CAB, nella [tabella file](file-table.md)e nella trasformazione lingua consente allo strumento di merge di ignorare eventuali file aggiuntivi archiviati nel file CAB che non sono elencati nella [tabella file](file-table.md).</span><span class="sxs-lookup"><span data-stu-id="d25b5-108">Because the Installer only installs the files listed in the [File Table](file-table.md), the use of a global file sequence in the cabinet, [File Table](file-table.md), and language transform enables the merge tool to skip any extra files stored in the cabinet that are not listed in the [File Table](file-table.md).</span></span> <span data-ttu-id="d25b5-109">Nel file CAB possono esistere altri file, ma non devono essere elencati nella [tabella file](file-table.md).</span><span class="sxs-lookup"><span data-stu-id="d25b5-109">Other files may exist in the cabinet, but they must not be listed in the [File Table](file-table.md).</span></span> <span data-ttu-id="d25b5-110">Ad esempio, un modulo che installa Code.dll, English. dat, German. dat e French. dat può utilizzare l'ordine di sequenza dei file globale seguente.</span><span class="sxs-lookup"><span data-stu-id="d25b5-110">For example, a module installing Code.dll, English.dat, German.dat, and French.dat can use the following global file sequence order.</span></span>



| <span data-ttu-id="d25b5-111">File</span><span class="sxs-lookup"><span data-stu-id="d25b5-111">File</span></span>        | <span data-ttu-id="d25b5-112">Sequenza</span><span class="sxs-lookup"><span data-stu-id="d25b5-112">Sequence</span></span> |
|-------------|----------|
| <span data-ttu-id="d25b5-113">Code.Dll</span><span class="sxs-lookup"><span data-stu-id="d25b5-113">Code.Dll</span></span>    | <span data-ttu-id="d25b5-114">1</span><span class="sxs-lookup"><span data-stu-id="d25b5-114">1</span></span>        |
| <span data-ttu-id="d25b5-115">Inglese. dat</span><span class="sxs-lookup"><span data-stu-id="d25b5-115">English.Dat</span></span> | <span data-ttu-id="d25b5-116">2</span><span class="sxs-lookup"><span data-stu-id="d25b5-116">2</span></span>        |
| <span data-ttu-id="d25b5-117">Tedesco. dat</span><span class="sxs-lookup"><span data-stu-id="d25b5-117">German.Dat</span></span>  | <span data-ttu-id="d25b5-118">3</span><span class="sxs-lookup"><span data-stu-id="d25b5-118">3</span></span>        |
| <span data-ttu-id="d25b5-119">Francese. dat</span><span class="sxs-lookup"><span data-stu-id="d25b5-119">French.Dat</span></span>  | <span data-ttu-id="d25b5-120">4</span><span class="sxs-lookup"><span data-stu-id="d25b5-120">4</span></span>        |



 

<span data-ttu-id="d25b5-121">Le trasformazioni della lingua possono quindi essere create per modificare la [tabella dei file](file-table.md) del modulo per la lingua inglese, tedesca o francese.</span><span class="sxs-lookup"><span data-stu-id="d25b5-121">Language transforms can then be authored to modify the [File Table](file-table.md) of the module for English, German, or French.</span></span>

<span data-ttu-id="d25b5-122">[Tabella file](file-table.md) (parziale per l'inglese)</span><span class="sxs-lookup"><span data-stu-id="d25b5-122">[File Table](file-table.md) (partial for English)</span></span>



| <span data-ttu-id="d25b5-123">File</span><span class="sxs-lookup"><span data-stu-id="d25b5-123">File</span></span>        | <span data-ttu-id="d25b5-124">Sequenza</span><span class="sxs-lookup"><span data-stu-id="d25b5-124">Sequence</span></span> |
|-------------|----------|
| <span data-ttu-id="d25b5-125">Code.Dll</span><span class="sxs-lookup"><span data-stu-id="d25b5-125">Code.Dll</span></span>    | <span data-ttu-id="d25b5-126">1</span><span class="sxs-lookup"><span data-stu-id="d25b5-126">1</span></span>        |
| <span data-ttu-id="d25b5-127">Inglese. dat</span><span class="sxs-lookup"><span data-stu-id="d25b5-127">English.Dat</span></span> | <span data-ttu-id="d25b5-128">2</span><span class="sxs-lookup"><span data-stu-id="d25b5-128">2</span></span>        |



 

<span data-ttu-id="d25b5-129">[Tabella file](file-table.md) (parziale per il tedesco)</span><span class="sxs-lookup"><span data-stu-id="d25b5-129">[File Table](file-table.md) (partial for German)</span></span>



| <span data-ttu-id="d25b5-130">File</span><span class="sxs-lookup"><span data-stu-id="d25b5-130">File</span></span>       | <span data-ttu-id="d25b5-131">Sequenza</span><span class="sxs-lookup"><span data-stu-id="d25b5-131">Sequence</span></span> |
|------------|----------|
| <span data-ttu-id="d25b5-132">Code.Dll</span><span class="sxs-lookup"><span data-stu-id="d25b5-132">Code.Dll</span></span>   | <span data-ttu-id="d25b5-133">1</span><span class="sxs-lookup"><span data-stu-id="d25b5-133">1</span></span>        |
| <span data-ttu-id="d25b5-134">Tedesco. dat</span><span class="sxs-lookup"><span data-stu-id="d25b5-134">German.Dat</span></span> | <span data-ttu-id="d25b5-135">3</span><span class="sxs-lookup"><span data-stu-id="d25b5-135">3</span></span>        |



 

<span data-ttu-id="d25b5-136">[Tabella file](file-table.md) (parziale per il francese)</span><span class="sxs-lookup"><span data-stu-id="d25b5-136">[File Table](file-table.md) (partial for French)</span></span>



| <span data-ttu-id="d25b5-137">File</span><span class="sxs-lookup"><span data-stu-id="d25b5-137">File</span></span>       | <span data-ttu-id="d25b5-138">Sequenza</span><span class="sxs-lookup"><span data-stu-id="d25b5-138">Sequence</span></span> |
|------------|----------|
| <span data-ttu-id="d25b5-139">Code.Dll</span><span class="sxs-lookup"><span data-stu-id="d25b5-139">Code.Dll</span></span>   | <span data-ttu-id="d25b5-140">1</span><span class="sxs-lookup"><span data-stu-id="d25b5-140">1</span></span>        |
| <span data-ttu-id="d25b5-141">Francese. dat</span><span class="sxs-lookup"><span data-stu-id="d25b5-141">French.Dat</span></span> | <span data-ttu-id="d25b5-142">4</span><span class="sxs-lookup"><span data-stu-id="d25b5-142">4</span></span>        |



 

<span data-ttu-id="d25b5-143">Per ulteriori informazioni, vedere [creazione di una trasformazione di linguaggio per un modulo di merge a più lingue](authoring-a-language-transform-for-a-multiple-language-merge-module.md) e [creazione di tabelle di file di moduli merge](authoring-merge-module-file-tables.md).</span><span class="sxs-lookup"><span data-stu-id="d25b5-143">For more information, see [Authoring a Language Transform for a Multiple Language Merge Module](authoring-a-language-transform-for-a-multiple-language-merge-module.md) and [Authoring Merge Module File Tables](authoring-merge-module-file-tables.md).</span></span>

 

 



