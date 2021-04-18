---
title: Compilazione di un catalogo completo da file TSV
description: Compilazione di un catalogo completo da file TSV
ms.assetid: fba80b32-dc78-4c4a-a351-e8786f9a7131
keywords:
- Windows Media Player Online Stores, compilazione di cataloghi
- archivi online, compilazione di cataloghi
- digitare 1 negozi online, compilazione di cataloghi
- Windows Media Player Online Stores, file TSV
- archivi online, file TSV
- digitare 1 archivi online, file TSV
- Windows Media Player Online Stores, catcomp.exe
- archivi online, catcomp.exe
- digitare 1 Store online, catcomp.exe
- catcomp.exe
- compilazione di cataloghi
- file con valori delimitati da tabulazioni (TSV)
- File TSV (con valori delimitati da tabulazioni)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b68af019a5e2302f52f615d5a1dba2180e27cfe5
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/19/2020
ms.locfileid: "106299379"
---
# <a name="compiling-a-full-catalog-from-tsv-files"></a><span data-ttu-id="de3ab-116">Compilazione di un catalogo completo da file TSV</span><span class="sxs-lookup"><span data-stu-id="de3ab-116">Compiling a Full Catalog from TSV Files</span></span>

<span data-ttu-id="de3ab-117">I nuovi cataloghi vengono creati da un set di file con valori delimitati da tabulazioni (TSV).</span><span class="sxs-lookup"><span data-stu-id="de3ab-117">New catalogs are created from a set of tab-separated-value (TSV) files.</span></span> <span data-ttu-id="de3ab-118">I file devono essere in formato Unicode.</span><span class="sxs-lookup"><span data-stu-id="de3ab-118">The files must be in Unicode format.</span></span> <span data-ttu-id="de3ab-119">Inserire i file TSV richiesti elencati di seguito in una cartella (l'argomento del percorso di input per catcomp.exe) e chiamare catcomp.exe usando la sintassi seguente:</span><span class="sxs-lookup"><span data-stu-id="de3ab-119">Place the required TSV files listed below into a folder (the input path argument to catcomp.exe), and call catcomp.exe using the following syntax:</span></span>


```C++
catcomp <input path> [version number] [locale ID] [debug]
```



<span data-ttu-id="de3ab-120">Se non viene specificato un numero di versione, il numero di versione verrà impostato su 0.</span><span class="sxs-lookup"><span data-stu-id="de3ab-120">If a version number is not provided, the version number will be set to 0.</span></span> <span data-ttu-id="de3ab-121">Se non viene specificato alcun ID delle impostazioni locali, vengono usate le impostazioni locali del sistema.</span><span class="sxs-lookup"><span data-stu-id="de3ab-121">If no locale ID is provided, the system locale is used.</span></span> <span data-ttu-id="de3ab-122">Se viene fornito un solo argomento numerico facoltativo, si presuppone che corrisponda al numero di versione.</span><span class="sxs-lookup"><span data-stu-id="de3ab-122">If only one numeric optional argument is provided, it is assumed to be the version number.</span></span> <span data-ttu-id="de3ab-123">Se viene specificato debug, l'output sullo schermo fornirà informazioni di diagnostica più dettagliate.</span><span class="sxs-lookup"><span data-stu-id="de3ab-123">If debug is specified, the output to the screen will provide more detailed diagnostic information.</span></span>

<span data-ttu-id="de3ab-124">Ad esempio, il codice seguente compila un catalogo dai file in C: \\ CatalogData \\ 210 e assegna al catalogo un numero di versione di 210:</span><span class="sxs-lookup"><span data-stu-id="de3ab-124">For example, the following will compile a catalog from the files in C:\\CatalogData\\210 and give the catalog a version number of 210:</span></span>


```C++
catcomp C:\CatalogData\210 210
```



<span data-ttu-id="de3ab-125">Per visualizzare messaggi di errore più dettagliati, è possibile aggiungere l'argomento facoltativo debug, come indicato di seguito:</span><span class="sxs-lookup"><span data-stu-id="de3ab-125">To display more detailed error messages, the optional debug argument can be added, as follows:</span></span>


```C++
catcomp C:\CatalogData\210 210 debug
```



## <a name="required-tsv-files"></a><span data-ttu-id="de3ab-126">File TSV richiesti</span><span class="sxs-lookup"><span data-stu-id="de3ab-126">Required TSV Files</span></span>

<span data-ttu-id="de3ab-127">Ognuno dei seguenti file deve essere presente, ma è possibile usare un file vuoto se non sono presenti dati per un file.</span><span class="sxs-lookup"><span data-stu-id="de3ab-127">Each of the following files must be present, but an empty file can be used if there is no data for a file.</span></span> <span data-ttu-id="de3ab-128">Ad esempio, se il catalogo non contiene canali radio, radio.csv può essere vuoto.</span><span class="sxs-lookup"><span data-stu-id="de3ab-128">For instance, if your catalog contains no radio channels, radio.csv can be empty.</span></span> <span data-ttu-id="de3ab-129">I file devono essere denominati esattamente come elencato.</span><span class="sxs-lookup"><span data-stu-id="de3ab-129">The files must be named exactly as listed.</span></span>

[<span data-ttu-id="de3ab-130">track.csv</span><span class="sxs-lookup"><span data-stu-id="de3ab-130">track.csv</span></span>](track-csv.md)

[<span data-ttu-id="de3ab-131">album.csv</span><span class="sxs-lookup"><span data-stu-id="de3ab-131">album.csv</span></span>](album-csv.md)

[<span data-ttu-id="de3ab-132">artist.csv</span><span class="sxs-lookup"><span data-stu-id="de3ab-132">artist.csv</span></span>](artist-csv.md)

[<span data-ttu-id="de3ab-133">genre.csv</span><span class="sxs-lookup"><span data-stu-id="de3ab-133">genre.csv</span></span>](genre-csv.md)

[<span data-ttu-id="de3ab-134">subgenre.csv</span><span class="sxs-lookup"><span data-stu-id="de3ab-134">subgenre.csv</span></span>](subgenre-csv.md)

[<span data-ttu-id="de3ab-135">list.csv</span><span class="sxs-lookup"><span data-stu-id="de3ab-135">list.csv</span></span>](list-csv.md)

[<span data-ttu-id="de3ab-136">listitem.csv</span><span class="sxs-lookup"><span data-stu-id="de3ab-136">listitem.csv</span></span>](listitem-csv.md)

[<span data-ttu-id="de3ab-137">radio.csv</span><span class="sxs-lookup"><span data-stu-id="de3ab-137">radio.csv</span></span>](radio-csv.md)

> [!Note]  
> <span data-ttu-id="de3ab-138">Sebbene i nomi file debbano includere estensioni CSV, i file non sono in formato CSV (valori separati da virgola).</span><span class="sxs-lookup"><span data-stu-id="de3ab-138">Although the file names must have .csv extensions, the files are not in Comma Separated Values (CSV) format.</span></span> <span data-ttu-id="de3ab-139">È necessario che i file siano in formato TSV (Tab Separated Values).</span><span class="sxs-lookup"><span data-stu-id="de3ab-139">The files must be in Tab Separated Values (TSV) format.</span></span>

 

<span data-ttu-id="de3ab-140">Se la compilazione ha esito positivo, catcomp.exe crea tre file di output.</span><span class="sxs-lookup"><span data-stu-id="de3ab-140">If compilation is successful, catcomp.exe creates three output files.</span></span>



| <span data-ttu-id="de3ab-141">Nome file</span><span class="sxs-lookup"><span data-stu-id="de3ab-141">File name</span></span>                   | <span data-ttu-id="de3ab-142">Descrizione</span><span class="sxs-lookup"><span data-stu-id="de3ab-142">Description</span></span>                                                                                                                                                                         |
|-----------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="de3ab-143">Catalog. WMDB</span><span class="sxs-lookup"><span data-stu-id="de3ab-143">catalog.wmdb</span></span>                | <span data-ttu-id="de3ab-144">Catalogo compilato non compresso.</span><span class="sxs-lookup"><span data-stu-id="de3ab-144">Uncompressed compiled catalog.</span></span>                                                                                                                                                      |
| <span data-ttu-id="de3ab-145">Catalog. WMDB. LZ</span><span class="sxs-lookup"><span data-stu-id="de3ab-145">catalog.wmdb.lz</span></span>             | <span data-ttu-id="de3ab-146">Catalogo in formato compresso.</span><span class="sxs-lookup"><span data-stu-id="de3ab-146">Catalog in compressed format.</span></span> <span data-ttu-id="de3ab-147">Il plug-in può assegnare il percorso di questo file a Windows Media Player in [IWMPContentPartner:: GetCatalogURL](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-getcatalogurl).</span><span class="sxs-lookup"><span data-stu-id="de3ab-147">Your plug-in can give the location of this file to Windows Media Player in [IWMPContentPartner::GetCatalogURL](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-getcatalogurl).</span></span> |
| <span data-ttu-id="de3ab-148">\_words.txt univoca compilata \_</span><span class="sxs-lookup"><span data-stu-id="de3ab-148">compiled\_unique\_words.txt</span></span> | <span data-ttu-id="de3ab-149">Un file di output intermedio.</span><span class="sxs-lookup"><span data-stu-id="de3ab-149">An intermediate output file.</span></span> <span data-ttu-id="de3ab-150">Non utilizzato da Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="de3ab-150">Not used by Windows Media Player.</span></span>                                                                                                                      |



 

 

 




