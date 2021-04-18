---
description: ICE42 verifica che i server inproc non siano collegati ai file EXE nella tabella della classe. Viene inoltre convalidato che solo le classi LocalServer e LocalServer32 dispongono di argomenti e valori DefInProc.
ms.assetid: 14976772-c873-46d8-8687-dcdad2420d83
title: ICE42
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ebe2ea09431870ac7b52ccd69d0ae16c646286ad
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106314214"
---
# <a name="ice42"></a><span data-ttu-id="61170-104">ICE42</span><span class="sxs-lookup"><span data-stu-id="61170-104">ICE42</span></span>

<span data-ttu-id="61170-105">ICE42 verifica che i server inproc non siano collegati ai file EXE nella [tabella della classe](class-table.md).</span><span class="sxs-lookup"><span data-stu-id="61170-105">ICE42 validates that InProc servers are not linked to EXE files in the [Class table](class-table.md).</span></span> <span data-ttu-id="61170-106">Viene inoltre convalidato che solo le classi LocalServer e LocalServer32 dispongono di argomenti e valori DefInProc.</span><span class="sxs-lookup"><span data-stu-id="61170-106">It also validates that only LocalServer and LocalServer32 classes have arguments and DefInProc values.</span></span>

## <a name="result"></a><span data-ttu-id="61170-107">Risultato</span><span class="sxs-lookup"><span data-stu-id="61170-107">Result</span></span>

<span data-ttu-id="61170-108">ICE42 Invia un errore se sono presenti server inproc collegati ai file EXE nella tabella della classe.</span><span class="sxs-lookup"><span data-stu-id="61170-108">ICE42 posts an error if there are InProc servers linked to EXE files in the Class table.</span></span>

## <a name="example"></a><span data-ttu-id="61170-109">Esempio</span><span class="sxs-lookup"><span data-stu-id="61170-109">Example</span></span>

<span data-ttu-id="61170-110">ICE42 segnala gli errori seguenti per l'esempio illustrato.</span><span class="sxs-lookup"><span data-stu-id="61170-110">ICE42 would report the following errors for the example shown.</span></span>



| <span data-ttu-id="61170-111">Errore ICE42</span><span class="sxs-lookup"><span data-stu-id="61170-111">ICE42 error</span></span>                                                                                                                             | <span data-ttu-id="61170-112">Descrizione</span><span class="sxs-lookup"><span data-stu-id="61170-112">Description</span></span>                                                                                                                                                                                                               |
|-----------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="61170-113">Il CLSID ' {GUID1}' è un server inproc, ma il componente di implementazione ' Component1' ha un file con estensione EXE (' test.exe') come file di base.</span><span class="sxs-lookup"><span data-stu-id="61170-113">CLSID '{GUID1}' is an InProc server, but the implementing component 'Component1' has an EXE ('test.exe') as its KeyFile.</span></span>                | <span data-ttu-id="61170-114">È presente un file eseguibile specificato come server inproc.</span><span class="sxs-lookup"><span data-stu-id="61170-114">There is an executable file specified as an InProc server.</span></span> <span data-ttu-id="61170-115">I file EXE non possono essere server inproc.</span><span class="sxs-lookup"><span data-stu-id="61170-115">EXE files cannot be InProc servers.</span></span>                                                                                                                            |
| <span data-ttu-id="61170-116">Il CLSID ' {GUID1}' nel contesto ' InProcServer32' contiene un argomento.</span><span class="sxs-lookup"><span data-stu-id="61170-116">CLSID '{GUID1}' in context 'InProcServer32' has an argument.</span></span> <span data-ttu-id="61170-117">Solo i contesti LocalServer possono avere argomenti.</span><span class="sxs-lookup"><span data-stu-id="61170-117">Only LocalServer contexts can have arguments.</span></span>                              | <span data-ttu-id="61170-118">Per correggere l'errore, rimuovere l'argomento.</span><span class="sxs-lookup"><span data-stu-id="61170-118">To fix this error, remove the argument.</span></span>                                                                                                                                                                                   |
| <span data-ttu-id="61170-119">Il CLSID ' {GUID1}' nel contesto ' InProcServer32' specifica un valore InProc predefinito.</span><span class="sxs-lookup"><span data-stu-id="61170-119">CLSID '{GUID1}' in context 'InProcServer32' specifies a default InProc value.</span></span> <span data-ttu-id="61170-120">Solo i contesti LocalServer possono avere valori InProc predefiniti.</span><span class="sxs-lookup"><span data-stu-id="61170-120">Only LocalServer contexts can have default InProc values.</span></span> | <span data-ttu-id="61170-121">È presente un oggetto con un valore InProc predefinito che non è un oggetto che opera nei contesti LocalServer o LocalServer32.</span><span class="sxs-lookup"><span data-stu-id="61170-121">There is an object with a default InProc value that is not an object operating in the LocalServer or LocalServer32 contexts.</span></span> <span data-ttu-id="61170-122">Per correggere l'errore, rimuovere il valore DeflnProc o modificare il contesto della classe.</span><span class="sxs-lookup"><span data-stu-id="61170-122">To fix this error, remove the DeflnProc value or change the context of the class.</span></span><br/> |



 

<span data-ttu-id="61170-123">[Tabella classi](class-table.md) (parziale)</span><span class="sxs-lookup"><span data-stu-id="61170-123">[Class Table](class-table.md) (partial)</span></span>



| <span data-ttu-id="61170-124">CLSID</span><span class="sxs-lookup"><span data-stu-id="61170-124">CLSID</span></span>   | <span data-ttu-id="61170-125">Context</span><span class="sxs-lookup"><span data-stu-id="61170-125">Context</span></span>        | <span data-ttu-id="61170-126">Componente\_</span><span class="sxs-lookup"><span data-stu-id="61170-126">Component\_</span></span> | <span data-ttu-id="61170-127">DefInProcHandler</span><span class="sxs-lookup"><span data-stu-id="61170-127">DefInProcHandler</span></span> | <span data-ttu-id="61170-128">Argomento</span><span class="sxs-lookup"><span data-stu-id="61170-128">Argument</span></span> |
|---------|----------------|-------------|------------------|----------|
| <span data-ttu-id="61170-129">Guid1</span><span class="sxs-lookup"><span data-stu-id="61170-129">{GUID1}</span></span> | <span data-ttu-id="61170-130">InProcServer32</span><span class="sxs-lookup"><span data-stu-id="61170-130">InProcServer32</span></span> | <span data-ttu-id="61170-131">Component1</span><span class="sxs-lookup"><span data-stu-id="61170-131">Component1</span></span>  | <span data-ttu-id="61170-132">InProcServer</span><span class="sxs-lookup"><span data-stu-id="61170-132">InProcServer</span></span>     | <span data-ttu-id="61170-133">ARG</span><span class="sxs-lookup"><span data-stu-id="61170-133">Arg</span></span>      |



 

<span data-ttu-id="61170-134">[Tabella componenti](component-table.md) (parziale)</span><span class="sxs-lookup"><span data-stu-id="61170-134">[Component Table](component-table.md) (partial)</span></span>



| <span data-ttu-id="61170-135">Componente</span><span class="sxs-lookup"><span data-stu-id="61170-135">Component</span></span>  | <span data-ttu-id="61170-136">KeyPath</span><span class="sxs-lookup"><span data-stu-id="61170-136">KeyPath</span></span> |
|------------|---------|
| <span data-ttu-id="61170-137">Component1</span><span class="sxs-lookup"><span data-stu-id="61170-137">Component1</span></span> | <span data-ttu-id="61170-138">File1</span><span class="sxs-lookup"><span data-stu-id="61170-138">File1</span></span>   |



 

<span data-ttu-id="61170-139">[Tabella file](file-table.md) (parziale)</span><span class="sxs-lookup"><span data-stu-id="61170-139">[File Table](file-table.md) (partial)</span></span>



| <span data-ttu-id="61170-140">File</span><span class="sxs-lookup"><span data-stu-id="61170-140">File</span></span>  | <span data-ttu-id="61170-141">Nome file</span><span class="sxs-lookup"><span data-stu-id="61170-141">Filename</span></span> |
|-------|----------|
| <span data-ttu-id="61170-142">File1</span><span class="sxs-lookup"><span data-stu-id="61170-142">File1</span></span> | <span data-ttu-id="61170-143">test.exe</span><span class="sxs-lookup"><span data-stu-id="61170-143">test.exe</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="61170-144">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="61170-144">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="61170-145">Riferimento ghiaccio</span><span class="sxs-lookup"><span data-stu-id="61170-145">ICE Reference</span></span>](ice-reference.md)
</dt> </dl>

 

 




