---
title: Compilazione di un aggiornamento del catalogo da cataloghi completi
description: Compilazione di un aggiornamento del catalogo da cataloghi completi
ms.assetid: 046c0a01-0ad7-41b6-bad5-dcab953a3980
keywords:
- Windows Media Player Online Stores, compilazione di cataloghi
- archivi online, compilazione di cataloghi
- digitare 1 negozi online, compilazione di cataloghi
- Windows Media Player Online Stores, aggiornamenti del catalogo
- archivi online, aggiornamenti del catalogo
- digitare 1 negozi online, aggiornamenti del catalogo
- Windows Media Player Online Stores, cataloghi completi
- archivi online, cataloghi completi
- digitare 1 Online Stores, cataloghi completi
- compilazione di cataloghi
- aggiornamenti del catalogo
- cataloghi completi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: abaa6d1bc0d3dbc4fefaffe1498be03259716a5e
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/19/2020
ms.locfileid: "104336249"
---
# <a name="compiling-a-catalog-update-from-full-catalogs"></a><span data-ttu-id="36046-115">Compilazione di un aggiornamento del catalogo da cataloghi completi</span><span class="sxs-lookup"><span data-stu-id="36046-115">Compiling a Catalog Update from Full Catalogs</span></span>

<span data-ttu-id="36046-116">Un aggiornamento del catalogo contenente le modifiche tra due versioni di un catalogo compilato può essere creato usando la sintassi seguente, dove *path1* è la directory che contiene il primo catalogo, *path2* è la directory che contiene il secondo catalogo e il debug può essere incluso facoltativamente per visualizzare informazioni dettagliate sull'errore sullo schermo.</span><span class="sxs-lookup"><span data-stu-id="36046-116">A catalog update containing the changes between two versions of a compiled catalog can be created by using the syntax below, where *path1* is the directory containing the first catalog, *path2* is the directory containing the second catalog, and debug can be optionally included to display detailed error information on the screen.</span></span> <span data-ttu-id="36046-117">I file di catalogo devono essere in formato non compresso. il nome file del catalogo compilato sarà Catalog. WMDB, anziché Catalog. WMDB. LZ.</span><span class="sxs-lookup"><span data-stu-id="36046-117">The catalog files must be in uncompressed form—the file name of the compiled catalog would be catalog.wmdb, rather than catalog.wmdb.lz.</span></span>


```C++
catcomp diff <path1> <path2> [debug]
```



<span data-ttu-id="36046-118">Se, ad esempio, la directory C: \\ Catalog210 \\ contiene la versione 210 di un catalogo compilato completo e C: \\ Catalog211 \\ contiene la versione 211, il comando seguente crea un file di differenze che contiene le modifiche tra le due versioni:</span><span class="sxs-lookup"><span data-stu-id="36046-118">For example, if the C:\\Catalog210\\ directory contains version 210 of a full compiled catalog and C:\\Catalog211\\ contains version 211, the following command creates a difference file that contains the changes between the two versions:</span></span>


```C++
catcomp diff C:\Catalog210\ C:\Catalog211\
```



<span data-ttu-id="36046-119">Per visualizzare informazioni dettagliate sull'errore, è possibile aggiungere il parametro di debug facoltativo come indicato di seguito:</span><span class="sxs-lookup"><span data-stu-id="36046-119">To display detailed error information, you can add the optional debug parameter as follows:</span></span>


```C++
catcomp diff C:\Catalog210\ C:\Catalog211\ debug
```



<span data-ttu-id="36046-120">Se la compilazione ha esito positivo, catcomp.exe crea i file di output elencati di seguito e li salva nella directory che contiene il primo catalogo.</span><span class="sxs-lookup"><span data-stu-id="36046-120">If compilation is successful, catcomp.exe creates the output files listed below and saves them in the directory that contains the first catalog.</span></span>



| <span data-ttu-id="36046-121">Nome file</span><span class="sxs-lookup"><span data-stu-id="36046-121">File name</span></span>             | <span data-ttu-id="36046-122">Descrizione</span><span class="sxs-lookup"><span data-stu-id="36046-122">Description</span></span>                                                                                                                                                                                      |
|-----------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="36046-123">Catalog. diff</span><span class="sxs-lookup"><span data-stu-id="36046-123">catalog.diff</span></span>          | <span data-ttu-id="36046-124">File delle differenze compilate non compresso.</span><span class="sxs-lookup"><span data-stu-id="36046-124">Uncompressed compiled difference file.</span></span>                                                                                                                                                           |
| <span data-ttu-id="36046-125">Catalog. diff. LZ</span><span class="sxs-lookup"><span data-stu-id="36046-125">catalog.diff.lz</span></span>       | <span data-ttu-id="36046-126">Versione compressa del file di aggiornamento del catalogo.</span><span class="sxs-lookup"><span data-stu-id="36046-126">Compressed version of catalog update file.</span></span> <span data-ttu-id="36046-127">Il plug-in può assegnare il percorso di questo file a Windows Media Player in [IWMPContentPartner:: GetCatalogURL](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-getcatalogurl).</span><span class="sxs-lookup"><span data-stu-id="36046-127">Your plug-in can give the location of this file to Windows Media Player in [IWMPContentPartner::GetCatalogURL](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-getcatalogurl).</span></span> |
| <span data-ttu-id="36046-128">Catalog. WMDB. Delta</span><span class="sxs-lookup"><span data-stu-id="36046-128">catalog.wmdb.delta</span></span>    | <span data-ttu-id="36046-129">File di output intermedio.</span><span class="sxs-lookup"><span data-stu-id="36046-129">Intermediate output file.</span></span> <span data-ttu-id="36046-130">Non utilizzato da Windows Media Player</span><span class="sxs-lookup"><span data-stu-id="36046-130">Not used by Windows Media Player</span></span>                                                                                                                                       |
| <span data-ttu-id="36046-131">Catalog. WMDB. Modified</span><span class="sxs-lookup"><span data-stu-id="36046-131">catalog.wmdb.modified</span></span> | <span data-ttu-id="36046-132">File di output intermedio.</span><span class="sxs-lookup"><span data-stu-id="36046-132">Intermediate output file.</span></span> <span data-ttu-id="36046-133">Non utilizzato da Windows Media Player</span><span class="sxs-lookup"><span data-stu-id="36046-133">Not used by Windows Media Player</span></span>                                                                                                                                       |



 

 

 




