---
description: ICE94 controlla la tabella dei collegamenti, la tabella delle funzionalità e la tabella MsiAssembly e invia un avviso se sono presenti collegamenti non pubblicizzati che puntano a un file di assembly nel Global Assembly Cache.
ms.assetid: 9b1b25b5-b190-47c2-8d43-fa3964e87a6f
title: ICE94
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d8ce52e88a31e246eb4d69defba77b64c2955eb8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104233155"
---
# <a name="ice94"></a><span data-ttu-id="b29e0-103">ICE94</span><span class="sxs-lookup"><span data-stu-id="b29e0-103">ICE94</span></span>

<span data-ttu-id="b29e0-104">ICE94 [Controlla la tabella dei collegamenti,](shortcut-table.md)la tabella delle [funzionalità](feature-table.md)e la [tabella MsiAssembly](msiassembly-table.md) e invia un avviso se sono presenti collegamenti non pubblicizzati che puntano a un file di assembly nel Global assembly cache.</span><span class="sxs-lookup"><span data-stu-id="b29e0-104">ICE94 checks the [Shortcut table](shortcut-table.md), [Feature table](feature-table.md), and [MsiAssembly table](msiassembly-table.md) and posts a warning if there are any unadvertised shortcuts pointing to an assembly file in the global assembly cache.</span></span> <span data-ttu-id="b29e0-105">Se la voce nel campo di destinazione della tabella dei collegamenti non è una funzionalità della tabella delle funzionalità, il collegamento non verrà annunciato.</span><span class="sxs-lookup"><span data-stu-id="b29e0-105">If the entry in the Target field of the Shortcut table is not a feature in the Feature table, the shortcut is unadvertised.</span></span> <span data-ttu-id="b29e0-106">Se la voce nel campo componente \_ della tabella dei collegamenti è elencata anche nella tabella MsiAssembly, il collegamento punta a un file di assembly.</span><span class="sxs-lookup"><span data-stu-id="b29e0-106">If the entry in the Component\_ field of the Shortcut table is also listed in the MsiAssembly table, the shortcut points to an assembly file.</span></span> <span data-ttu-id="b29e0-107">Se la voce nel \_ campo applicazione file nella tabella MsiAssembly è vuota, il file di assembly si trova nel Global assembly cache.</span><span class="sxs-lookup"><span data-stu-id="b29e0-107">If the entry in the File\_Application field in the MsiAssembly table is empty, the assembly file is in the global assembly cache.</span></span>

## <a name="result"></a><span data-ttu-id="b29e0-108">Risultato</span><span class="sxs-lookup"><span data-stu-id="b29e0-108">Result</span></span>

<span data-ttu-id="b29e0-109">ICE94 invia il seguente avviso.</span><span class="sxs-lookup"><span data-stu-id="b29e0-109">ICE94 posts the following warning.</span></span>



| <span data-ttu-id="b29e0-110">Avviso di ICE94</span><span class="sxs-lookup"><span data-stu-id="b29e0-110">ICE94 warning</span></span>                                                                                | <span data-ttu-id="b29e0-111">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b29e0-111">Description</span></span>                                                                            |
|----------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="b29e0-112">Il collegamento non annunciato ' \[ 2 \] ' punta a un file di assembly nel Global assembly cache.</span><span class="sxs-lookup"><span data-stu-id="b29e0-112">The non-advertised shortcut '\[2\]' points to an assembly file in the global assembly cache.</span></span> | <span data-ttu-id="b29e0-113">Un collegamento non annunciato sta puntando a un file di assembly nel Global Assembly Cache.</span><span class="sxs-lookup"><span data-stu-id="b29e0-113">An unadvertised shortcut is pointing to an assembly file in the global assembly cache.</span></span> |



 

## <a name="example"></a><span data-ttu-id="b29e0-114">Esempio</span><span class="sxs-lookup"><span data-stu-id="b29e0-114">Example</span></span>

<span data-ttu-id="b29e0-115">ICE94 segnala l'errore seguente per l'esempio:</span><span class="sxs-lookup"><span data-stu-id="b29e0-115">ICE94 reports the following error for the example:</span></span>

``` syntax
The non-advertised shortcut 'shortcut1' points to an assembly file in the global assembly cache.
```

<span data-ttu-id="b29e0-116">[Tabella collegamenti](shortcut-table.md) (parziale)</span><span class="sxs-lookup"><span data-stu-id="b29e0-116">[Shortcut Table](shortcut-table.md) (partial)</span></span>



| <span data-ttu-id="b29e0-117">Tasto di scelta rapida</span><span class="sxs-lookup"><span data-stu-id="b29e0-117">Shortcut</span></span>  | <span data-ttu-id="b29e0-118">Componente\_</span><span class="sxs-lookup"><span data-stu-id="b29e0-118">Component\_</span></span> | <span data-ttu-id="b29e0-119">Destinazione</span><span class="sxs-lookup"><span data-stu-id="b29e0-119">Target</span></span>    |
|-----------|-------------|-----------|
| <span data-ttu-id="b29e0-120">shortcut1</span><span class="sxs-lookup"><span data-stu-id="b29e0-120">shortcut1</span></span> | <span data-ttu-id="b29e0-121">c1</span><span class="sxs-lookup"><span data-stu-id="b29e0-121">c1</span></span>          | <span data-ttu-id="b29e0-122">\[file1\]</span><span class="sxs-lookup"><span data-stu-id="b29e0-122">\[file1\]</span></span> |
| <span data-ttu-id="b29e0-123">shortcut2</span><span class="sxs-lookup"><span data-stu-id="b29e0-123">shortcut2</span></span> | <span data-ttu-id="b29e0-124">c2</span><span class="sxs-lookup"><span data-stu-id="b29e0-124">c2</span></span>          | <span data-ttu-id="b29e0-125">Feature1</span><span class="sxs-lookup"><span data-stu-id="b29e0-125">feature1</span></span>  |
| <span data-ttu-id="b29e0-126">shortcut3</span><span class="sxs-lookup"><span data-stu-id="b29e0-126">shortcut3</span></span> | <span data-ttu-id="b29e0-127">c3</span><span class="sxs-lookup"><span data-stu-id="b29e0-127">c3</span></span>          | <span data-ttu-id="b29e0-128">\[file2\]</span><span class="sxs-lookup"><span data-stu-id="b29e0-128">\[file2\]</span></span> |



 

<span data-ttu-id="b29e0-129">[Tabella delle funzionalità](feature-table.md) (parziale)</span><span class="sxs-lookup"><span data-stu-id="b29e0-129">[Feature Table](feature-table.md) (partial)</span></span>



| <span data-ttu-id="b29e0-130">Funzionalità</span><span class="sxs-lookup"><span data-stu-id="b29e0-130">Feature</span></span>  |
|----------|
| <span data-ttu-id="b29e0-131">Feature1</span><span class="sxs-lookup"><span data-stu-id="b29e0-131">feature1</span></span> |



 

<span data-ttu-id="b29e0-132">[Tabella MsiAssembly](msiassembly-table.md) (parziale)</span><span class="sxs-lookup"><span data-stu-id="b29e0-132">[MsiAssembly Table](msiassembly-table.md) (partial)</span></span>



| <span data-ttu-id="b29e0-133">Componente\_</span><span class="sxs-lookup"><span data-stu-id="b29e0-133">Component\_</span></span> | <span data-ttu-id="b29e0-134">\_Applicazione file</span><span class="sxs-lookup"><span data-stu-id="b29e0-134">File\_Application</span></span> |
|-------------|-------------------|
| <span data-ttu-id="b29e0-135">c1</span><span class="sxs-lookup"><span data-stu-id="b29e0-135">c1</span></span>          |                   |
| <span data-ttu-id="b29e0-136">c2</span><span class="sxs-lookup"><span data-stu-id="b29e0-136">c2</span></span>          |                   |
| <span data-ttu-id="b29e0-137">c3</span><span class="sxs-lookup"><span data-stu-id="b29e0-137">c3</span></span>          | <span data-ttu-id="b29e0-138">FA1</span><span class="sxs-lookup"><span data-stu-id="b29e0-138">fa1</span></span>               |



 

## <a name="related-topics"></a><span data-ttu-id="b29e0-139">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="b29e0-139">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b29e0-140">Riferimento ghiaccio</span><span class="sxs-lookup"><span data-stu-id="b29e0-140">ICE Reference</span></span>](ice-reference.md)
</dt> </dl>

 

 



