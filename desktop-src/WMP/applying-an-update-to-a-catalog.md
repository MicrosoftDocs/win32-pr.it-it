---
title: Applicazione di un aggiornamento a un catalogo
description: Applicazione di un aggiornamento a un catalogo
ms.assetid: 4aedb0d6-36c7-425c-b6d3-e16161cf6828
keywords:
- Windows Media Player Online Stores, applicazione degli aggiornamenti ai cataloghi
- negozi online, applicazione di aggiornamenti ai cataloghi
- digitare 1 negozi online, applicazione di aggiornamenti ai cataloghi
- Windows Media Player Online Stores, aggiornamento di cataloghi
- archivi online, aggiornamento di cataloghi
- digitare 1 negozi online, aggiornamento di cataloghi
- Windows Media Player Online Stores, aggiornamenti del catalogo
- archivi online, aggiornamenti del catalogo
- digitare 1 negozi online, aggiornamenti del catalogo
- aggiornamenti del catalogo
- aggiornamento di cataloghi
- applicazione degli aggiornamenti ai cataloghi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d468edb7d09b8804fa924f7c31fc1be45d27c8fe
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106298931"
---
# <a name="applying-an-update-to-a-catalog"></a><span data-ttu-id="d2683-115">Applicazione di un aggiornamento a un catalogo</span><span class="sxs-lookup"><span data-stu-id="d2683-115">Applying an Update To a Catalog</span></span>

> [!Note]  
> <span data-ttu-id="d2683-116">Questa operazione non viene in genere eseguita ad eccezione degli scopi di diagnostica, ad esempio per verificare che un file di differenza sia valido.</span><span class="sxs-lookup"><span data-stu-id="d2683-116">This is not normally done except for diagnostic purposes—for instance, to help verify that a difference file is valid.</span></span> <span data-ttu-id="d2683-117">Il catalogo generato in questo modo non è in formato compresso e non deve essere passato a Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="d2683-117">The catalog generated in this way is not in compressed form and should not be passed to Windows Media Player.</span></span>

 

<span data-ttu-id="d2683-118">È possibile creare un nuovo file di catalogo usando la sintassi seguente, dove *inputcatalog* è il percorso del catalogo originale e *inputdiff* è il percorso del file di differenza da applicare.</span><span class="sxs-lookup"><span data-stu-id="d2683-118">A new catalog file can be created by using the syntax below, where *inputcatalog* is the location of the original catalog, and *inputdiff* is the location of the difference file to apply.</span></span> <span data-ttu-id="d2683-119">I file di catalogo devono essere in formato non compresso.</span><span class="sxs-lookup"><span data-stu-id="d2683-119">The catalog files must be in uncompressed form.</span></span>


```C++
catcomp applydiff <inputcatalog> <inputdiff>
```



<span data-ttu-id="d2683-120">Ad esempio, di seguito viene creato un nuovo catalogo da C: \\ Catalog210 \\ Catalog. WMDB e c: \\ Catalog210 \\ Catalog. diff.</span><span class="sxs-lookup"><span data-stu-id="d2683-120">For example, the following creates a new catalog from C:\\Catalog210\\catalog.wmdb and C:\\Catalog210\\catalog.diff.</span></span>


```C++
catcomp applydiff C:\Catalog210\catalog.wmdb C:\Catalog210\catalog.diff
```



<span data-ttu-id="d2683-121">Se la compilazione ha esito positivo, catcomp.exe crea i file di output seguenti.</span><span class="sxs-lookup"><span data-stu-id="d2683-121">If compilation is successful, catcomp.exe creates the follow output files.</span></span>



| <span data-ttu-id="d2683-122">Nome file</span><span class="sxs-lookup"><span data-stu-id="d2683-122">File name</span></span>        | <span data-ttu-id="d2683-123">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d2683-123">Description</span></span>       |
|------------------|-------------------|
| <span data-ttu-id="d2683-124">Catalog. WMDB. New</span><span class="sxs-lookup"><span data-stu-id="d2683-124">catalog.wmdb.new</span></span> | <span data-ttu-id="d2683-125">Nuovo file di catalogo.</span><span class="sxs-lookup"><span data-stu-id="d2683-125">New catalog file.</span></span> |



 

 

 




