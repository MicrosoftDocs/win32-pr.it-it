---
title: artist.csv
description: artist.csv
ms.assetid: 50cf2fbc-28cc-4b13-988e-4c02eb821cfd
keywords:
- Windows Media Player Online Stores, artist.csv
- archivi online, artist.csv
- digitare 1 Store online, artist.csv
- artist.csv
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4f548c419f01d23b76172c44cd6e50263c4e9197
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104332428"
---
# <a name="artistcsv"></a><span data-ttu-id="9a0df-107">artist.csv</span><span class="sxs-lookup"><span data-stu-id="9a0df-107">artist.csv</span></span>

<span data-ttu-id="9a0df-108">Questo file contiene una voce per ogni artista nel catalogo.</span><span class="sxs-lookup"><span data-stu-id="9a0df-108">This file contains an entry for each artist in the catalog.</span></span> <span data-ttu-id="9a0df-109">Ogni voce è una riga costituita dai campi delimitati da tabulazioni descritti nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="9a0df-109">Each entry is a row composed of the tab-delimited fields described in the table below.</span></span> <span data-ttu-id="9a0df-110">I campi devono essere visualizzati nell'ordine elencato.</span><span class="sxs-lookup"><span data-stu-id="9a0df-110">Fields must appear in the order listed.</span></span>

<span data-ttu-id="9a0df-111">Tutti i campi nel artist.csv sono obbligatori.</span><span class="sxs-lookup"><span data-stu-id="9a0df-111">All fields in artist.csv are required.</span></span>

<span data-ttu-id="9a0df-112">La colonna Format nella tabella seguente descrive la modalità di formattazione di ogni campo di testo Unicode.</span><span class="sxs-lookup"><span data-stu-id="9a0df-112">The Format column in the table below describes the way each Unicode text field is formatted.</span></span> <span data-ttu-id="9a0df-113">Non si riferisce al tipo di dati del contenuto.</span><span class="sxs-lookup"><span data-stu-id="9a0df-113">It does not refer to the data type of the contents.</span></span> <span data-ttu-id="9a0df-114">Se, ad esempio, nella colonna formato è indicato Integer, significa che il campo contiene una stringa Unicode che rappresenta un valore integrale, anziché un numero intero effettivo.</span><span class="sxs-lookup"><span data-stu-id="9a0df-114">For example, if Integer is indicated in the Format column, it means that the field contains a Unicode string representing an integral value, rather than an actual integer.</span></span>



| <span data-ttu-id="9a0df-115">Campo</span><span class="sxs-lookup"><span data-stu-id="9a0df-115">Field</span></span>                  | <span data-ttu-id="9a0df-116">Formato</span><span class="sxs-lookup"><span data-stu-id="9a0df-116">Format</span></span>                                            | <span data-ttu-id="9a0df-117">Descrizione</span><span class="sxs-lookup"><span data-stu-id="9a0df-117">Description</span></span>                                                                                                |
|------------------------|---------------------------------------------------|------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9a0df-118">ArtistID</span><span class="sxs-lookup"><span data-stu-id="9a0df-118">ArtistID</span></span>               | <span data-ttu-id="9a0df-119">Integer non negativo.</span><span class="sxs-lookup"><span data-stu-id="9a0df-119">Non-negative integer.</span></span> <span data-ttu-id="9a0df-120">Esempio: 65832</span><span class="sxs-lookup"><span data-stu-id="9a0df-120">Example: 65832</span></span>              | <span data-ttu-id="9a0df-121">Identificatore univoco per l'artista, univoco all'interno artist.csv.</span><span class="sxs-lookup"><span data-stu-id="9a0df-121">Unique identifier for the artist, unique within artist.csv.</span></span> <span data-ttu-id="9a0df-122">Deve essere minore di 2 ^ 32.</span><span class="sxs-lookup"><span data-stu-id="9a0df-122">Must be less than 2^32.</span></span>                        |
| <span data-ttu-id="9a0df-123">ArtistName</span><span class="sxs-lookup"><span data-stu-id="9a0df-123">ArtistName</span></span>             | <span data-ttu-id="9a0df-124">Stringa Unicode. Esempio: Don Funk</span><span class="sxs-lookup"><span data-stu-id="9a0df-124">Unicode string.Example: Don Funk</span></span><br/>       | <span data-ttu-id="9a0df-125">Nome visualizzato per l'artista.</span><span class="sxs-lookup"><span data-stu-id="9a0df-125">Display name for the artist.</span></span>                                                                               |
| <span data-ttu-id="9a0df-126">LinkedGenreID</span><span class="sxs-lookup"><span data-stu-id="9a0df-126">LinkedGenreID</span></span>          | <span data-ttu-id="9a0df-127">Integer non negativo. Esempio: 313</span><span class="sxs-lookup"><span data-stu-id="9a0df-127">Non-negative integer.Example: 313</span></span><br/>      | <span data-ttu-id="9a0df-128">GenreID del genere principale dell'artista.</span><span class="sxs-lookup"><span data-stu-id="9a0df-128">GenreID of the artist's primary genre.</span></span> <span data-ttu-id="9a0df-129">Deve essere un genere principale e non un sottogenere.</span><span class="sxs-lookup"><span data-stu-id="9a0df-129">Must be a main genre and not a subgenre.</span></span> <span data-ttu-id="9a0df-130">È consentito un solo valore.</span><span class="sxs-lookup"><span data-stu-id="9a0df-130">Only one value is allowed.</span></span> |
| <span data-ttu-id="9a0df-131">LinkedSimilarArtistIDs</span><span class="sxs-lookup"><span data-stu-id="9a0df-131">LinkedSimilarArtistIDs</span></span> | <span data-ttu-id="9a0df-132">N/D</span><span class="sxs-lookup"><span data-stu-id="9a0df-132">N/A</span></span>                                               | <span data-ttu-id="9a0df-133">Non utilizzato in questa versione.</span><span class="sxs-lookup"><span data-stu-id="9a0df-133">Not used in this release.</span></span> <span data-ttu-id="9a0df-134">Deve essere vuoto.</span><span class="sxs-lookup"><span data-stu-id="9a0df-134">Should be empty.</span></span>                                                                 |
| <span data-ttu-id="9a0df-135">Popolarità</span><span class="sxs-lookup"><span data-stu-id="9a0df-135">Popularity</span></span>             | <span data-ttu-id="9a0df-136">Può essere un valore intero o decimale.</span><span class="sxs-lookup"><span data-stu-id="9a0df-136">Can be integer or decimal value.</span></span> <span data-ttu-id="9a0df-137">Esempio: 1252,25</span><span class="sxs-lookup"><span data-stu-id="9a0df-137">Example: 1252.25</span></span> | <span data-ttu-id="9a0df-138">Classificazione della popolarità.</span><span class="sxs-lookup"><span data-stu-id="9a0df-138">Popularity ranking.</span></span> <span data-ttu-id="9a0df-139">Può essere la posizione nell'elenco quando è ordinata in base alla popolarità.</span><span class="sxs-lookup"><span data-stu-id="9a0df-139">Can be the position in the list when sorted by popularity.</span></span>                             |
| <span data-ttu-id="9a0df-140">FeedsAvailable</span><span class="sxs-lookup"><span data-stu-id="9a0df-140">FeedsAvailable</span></span>         | <span data-ttu-id="9a0df-141">Proprietà di tipo Boolean.</span><span class="sxs-lookup"><span data-stu-id="9a0df-141">Boolean.</span></span> <span data-ttu-id="9a0df-142">Formato: \[ 0 \| 1 \] esempio: 0</span><span class="sxs-lookup"><span data-stu-id="9a0df-142">Format: \[0\|1\]Example: 0</span></span><br/>    | <span data-ttu-id="9a0df-143">Non utilizzato in questa versione.</span><span class="sxs-lookup"><span data-stu-id="9a0df-143">Not used in this release.</span></span> <span data-ttu-id="9a0df-144">Deve essere vuoto.</span><span class="sxs-lookup"><span data-stu-id="9a0df-144">Should be empty.</span></span>                                                                 |



 

 

 





