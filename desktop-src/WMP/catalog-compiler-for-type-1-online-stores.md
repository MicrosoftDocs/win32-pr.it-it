---
title: Compilatore del catalogo per i negozi di tipo 1 online
description: Compilatore del catalogo per i negozi di tipo 1 online
ms.assetid: 49c03d3b-3381-4663-83c8-5bc8fa70f7c3
keywords:
- Windows Media Player Online Stores, compilatore catalog
- archivi online, compilatore di cataloghi
- digitare 1 negozi online, compilatore di cataloghi
- Windows Media Player Online Stores, catcomp.exe
- archivi online, catcomp.exe
- digitare 1 Store online, catcomp.exe
- compilatore Catalogo
- catcomp.exe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a4c54ffd054c5e72b04ddd32eef12c7fe6b6cc89
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/19/2020
ms.locfileid: "106299372"
---
# <a name="catalog-compiler-for-type-1-online-stores"></a><span data-ttu-id="0f41b-111">Compilatore del catalogo per i negozi di tipo 1 online</span><span class="sxs-lookup"><span data-stu-id="0f41b-111">Catalog Compiler for Type 1 Online Stores</span></span>

<span data-ttu-id="0f41b-112">Il compilatore del catalogo (catcomp.exe) è uno strumento da riga di comando utilizzato dagli archivi online di tipo 1 per compilare il set di file con valori delimitati da tabulazioni (TSV) contenenti i dati del catalogo del negozio online in un catalogo compresso che può essere scaricato da Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="0f41b-112">The catalog compiler (catcomp.exe) is a command-line tool used by Type 1 online stores to compile the set of tab-separated-value (TSV) files containing the online store's catalog data into a compressed catalog that can be downloaded by Windows Media Player.</span></span> <span data-ttu-id="0f41b-113">Il compilatore del catalogo compila inoltre i file di aggiornamento del catalogo contenenti solo le informazioni del catalogo modificate dopo l'ultimo aggiornamento del catalogo.</span><span class="sxs-lookup"><span data-stu-id="0f41b-113">The catalog compiler also compiles catalog update files containing only the catalog information that has changed since the last catalog update.</span></span>

<span data-ttu-id="0f41b-114">I file di catalogo compressi o i file di aggiornamento del catalogo devono essere forniti a Windows Media Player per il download nell'implementazione del plug-in Online Store di [IWMPContentPartner:: GetCatalogURL](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-getcatalogurl).</span><span class="sxs-lookup"><span data-stu-id="0f41b-114">The compressed catalog files or catalog update files should be provided to Windows Media Player for download in the online store plug-in's implementation of [IWMPContentPartner::GetCatalogURL](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-getcatalogurl).</span></span>

<span data-ttu-id="0f41b-115">Attività comuni</span><span class="sxs-lookup"><span data-stu-id="0f41b-115">Common Tasks</span></span>

-   [<span data-ttu-id="0f41b-116">Compilazione di un catalogo completo da file TSV</span><span class="sxs-lookup"><span data-stu-id="0f41b-116">Compiling a Full Catalog from TSV Files</span></span>](compiling-a-full-catalog-from-tsv-files.md)
-   [<span data-ttu-id="0f41b-117">Compilazione di un aggiornamento del catalogo da cataloghi completi</span><span class="sxs-lookup"><span data-stu-id="0f41b-117">Compiling a Catalog Update from Full Catalogs</span></span>](compiling-a-catalog-update-from-full-catalogs.md)

<span data-ttu-id="0f41b-118">Attività diagnostiche</span><span class="sxs-lookup"><span data-stu-id="0f41b-118">Diagnostic Tasks</span></span>

-   [<span data-ttu-id="0f41b-119">Visualizzazione della Guida</span><span class="sxs-lookup"><span data-stu-id="0f41b-119">Displaying Help</span></span>](displaying-help.md)
-   [<span data-ttu-id="0f41b-120">Recupero delle informazioni del catalogo</span><span class="sxs-lookup"><span data-stu-id="0f41b-120">Retrieving Catalog Information</span></span>](retrieving-catalog-information.md)
-   [<span data-ttu-id="0f41b-121">Applicazione di un aggiornamento a un catalogo</span><span class="sxs-lookup"><span data-stu-id="0f41b-121">Applying an Update To a Catalog</span></span>](applying-an-update-to-a-catalog.md)

 

 




