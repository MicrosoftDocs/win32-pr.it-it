---
title: subgenre.csv
description: subgenre.csv
ms.assetid: 3ba51cda-0c29-4ce9-9237-8444225349c8
keywords:
- Windows Media Player Online Stores, subgenre.csv
- archivi online, subgenre.csv
- digitare 1 Store online, subgenre.csv
- subgenre.csv
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 98f004eb8cecaaae64a5cc95348ac93e8a7db230
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106298744"
---
# <a name="subgenrecsv"></a><span data-ttu-id="be8a4-107">subgenre.csv</span><span class="sxs-lookup"><span data-stu-id="be8a4-107">subgenre.csv</span></span>

<span data-ttu-id="be8a4-108">Questo file contiene una voce per ogni sottogenere rappresentato nel catalogo.</span><span class="sxs-lookup"><span data-stu-id="be8a4-108">This file contains an entry for each subgenre represented in the catalog.</span></span> <span data-ttu-id="be8a4-109">Ogni voce è una riga costituita dai campi delimitati da tabulazioni descritti nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="be8a4-109">Each entry is a row composed of the tab-delimited fields described in the table below.</span></span> <span data-ttu-id="be8a4-110">I campi devono essere visualizzati nell'ordine elencato.</span><span class="sxs-lookup"><span data-stu-id="be8a4-110">Fields must appear in the order listed.</span></span>

<span data-ttu-id="be8a4-111">La colonna Format nella tabella seguente descrive la modalità di formattazione di ogni campo di testo Unicode.</span><span class="sxs-lookup"><span data-stu-id="be8a4-111">The Format column in the table below describes the way each Unicode text field is formatted.</span></span> <span data-ttu-id="be8a4-112">Non si riferisce al tipo di dati del contenuto.</span><span class="sxs-lookup"><span data-stu-id="be8a4-112">It does not refer to the data type of the contents.</span></span> <span data-ttu-id="be8a4-113">Se, ad esempio, nella colonna formato è indicato Integer, significa che il campo contiene una stringa Unicode che rappresenta un valore integrale, anziché un numero intero effettivo.</span><span class="sxs-lookup"><span data-stu-id="be8a4-113">For example, if Integer is indicated in the Format column, it means that the field contains a Unicode string representing an integral value, rather than an actual integer.</span></span>



| <span data-ttu-id="be8a4-114">Campo</span><span class="sxs-lookup"><span data-stu-id="be8a4-114">Field</span></span>             | <span data-ttu-id="be8a4-115">Necessario</span><span class="sxs-lookup"><span data-stu-id="be8a4-115">Required</span></span> | <span data-ttu-id="be8a4-116">Formato</span><span class="sxs-lookup"><span data-stu-id="be8a4-116">Format</span></span>                                                                                            | <span data-ttu-id="be8a4-117">Descrizione</span><span class="sxs-lookup"><span data-stu-id="be8a4-117">Description</span></span>                                                                                                                                               |
|-------------------|----------|---------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="be8a4-118">SubGenreID</span><span class="sxs-lookup"><span data-stu-id="be8a4-118">SubGenreID</span></span>        | <span data-ttu-id="be8a4-119">Sì</span><span class="sxs-lookup"><span data-stu-id="be8a4-119">Yes</span></span>      | <span data-ttu-id="be8a4-120">Integer non negativo.</span><span class="sxs-lookup"><span data-stu-id="be8a4-120">Non-negative integer.</span></span>                                                                             | <span data-ttu-id="be8a4-121">Identificatore (ID) del sottogenere, univoco all'interno subgenre.csv.</span><span class="sxs-lookup"><span data-stu-id="be8a4-121">Subgenre identifier (ID), unique within subgenre.csv.</span></span> <span data-ttu-id="be8a4-122">Sono consentiti fino a 1024 sottogeneri.</span><span class="sxs-lookup"><span data-stu-id="be8a4-122">Up to 1024 subgenres are allowed.</span></span>                                                                   |
| <span data-ttu-id="be8a4-123">SubGenreTitle</span><span class="sxs-lookup"><span data-stu-id="be8a4-123">SubGenreTitle</span></span>     | <span data-ttu-id="be8a4-124">Sì</span><span class="sxs-lookup"><span data-stu-id="be8a4-124">Yes</span></span>      | <span data-ttu-id="be8a4-125">Stringa Unicode. Esempio: Intelligent Dance Music (IDM)</span><span class="sxs-lookup"><span data-stu-id="be8a4-125">Unicode string.Example: Intelligent Dance Music (IDM)</span></span><br/>                                  | <span data-ttu-id="be8a4-126">Nome visualizzato del sottogenere.</span><span class="sxs-lookup"><span data-stu-id="be8a4-126">Subgenre display name.</span></span>                                                                                                                                    |
| <span data-ttu-id="be8a4-127">SubGenreSubtitle</span><span class="sxs-lookup"><span data-stu-id="be8a4-127">SubGenreSubtitle</span></span>  | <span data-ttu-id="be8a4-128">No</span><span class="sxs-lookup"><span data-stu-id="be8a4-128">No</span></span>       | <span data-ttu-id="be8a4-129">Stringa Unicode. Esempio: nuovo, musica elettronica a percussione che non è un techno puro.</span><span class="sxs-lookup"><span data-stu-id="be8a4-129">Unicode string.Example: New, percussive electronic music that's not quite pure techno.</span></span><br/> | <span data-ttu-id="be8a4-130">Descrive il significato del nome visualizzato del sottogenere.</span><span class="sxs-lookup"><span data-stu-id="be8a4-130">Describe the meaning of the subgenre display name.</span></span> <span data-ttu-id="be8a4-131">Deve essere minore di 64 caratteri.</span><span class="sxs-lookup"><span data-stu-id="be8a4-131">Should be less than 64 characters.</span></span>                                                                     |
| <span data-ttu-id="be8a4-132">FeedsAreAvailable</span><span class="sxs-lookup"><span data-stu-id="be8a4-132">FeedsAreAvailable</span></span> | <span data-ttu-id="be8a4-133">Sì</span><span class="sxs-lookup"><span data-stu-id="be8a4-133">Yes</span></span>      | <span data-ttu-id="be8a4-134">Boolean. Format: \[ 0 \| 1\]</span><span class="sxs-lookup"><span data-stu-id="be8a4-134">Boolean.Format: \[0\|1\]</span></span><br/> <span data-ttu-id="be8a4-135">Esempio: 0</span><span class="sxs-lookup"><span data-stu-id="be8a4-135">Example: 0</span></span><br/>                                         | <span data-ttu-id="be8a4-136">Indica se è possibile eseguire la radioriproduzione eseguendo il passaggio a un feed.</span><span class="sxs-lookup"><span data-stu-id="be8a4-136">Indicates whether "radio play" is possible by jumping to a feed.</span></span>                                                                                          |
| <span data-ttu-id="be8a4-137">\_GenreID collegato</span><span class="sxs-lookup"><span data-stu-id="be8a4-137">Linked\_GenreID</span></span>   | <span data-ttu-id="be8a4-138">Sì</span><span class="sxs-lookup"><span data-stu-id="be8a4-138">Yes</span></span>      | <span data-ttu-id="be8a4-139">Integer non negativo (GenreID). Esempio: 12</span><span class="sxs-lookup"><span data-stu-id="be8a4-139">Non-negative integer (GenreID).Example: 12</span></span><br/>                                             | <span data-ttu-id="be8a4-140">GenreID del genere padre.</span><span class="sxs-lookup"><span data-stu-id="be8a4-140">The GenreID of the parent genre.</span></span> <span data-ttu-id="be8a4-141">È consentito un solo elemento padre.</span><span class="sxs-lookup"><span data-stu-id="be8a4-141">Only one parent is allowed.</span></span>                                                                                              |
| <span data-ttu-id="be8a4-142">SortOrderRank</span><span class="sxs-lookup"><span data-stu-id="be8a4-142">SortOrderRank</span></span>     | <span data-ttu-id="be8a4-143">Sì</span><span class="sxs-lookup"><span data-stu-id="be8a4-143">Yes</span></span>      | <span data-ttu-id="be8a4-144">Integer non negativo. Esempio: 23</span><span class="sxs-lookup"><span data-stu-id="be8a4-144">Non-negative integer.Example: 23</span></span><br/>                                                       | <span data-ttu-id="be8a4-145">Classificazione, idealmente univoca, utilizzata per l'ordinamento dei sottogeneri nell'interfaccia utente.</span><span class="sxs-lookup"><span data-stu-id="be8a4-145">A ranking, ideally unique, used for sorting subgenres in the user interface.</span></span> <span data-ttu-id="be8a4-146">Se il genere padre ha 10 sottogeneri, potrebbe trattarsi di un numero intero compreso tra 1 e 10.</span><span class="sxs-lookup"><span data-stu-id="be8a4-146">If the parent genre has 10 subgenres, this might be an integer from 1 to 10.</span></span> |



 

 

 





