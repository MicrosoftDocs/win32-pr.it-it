---
title: genre.csv
description: genre.csv
ms.assetid: e05517f4-a69b-4db7-943d-3490253b92f3
keywords:
- Windows Media Player Online Stores, genre.csv
- archivi online, genre.csv
- digitare 1 Store online, genre.csv
- genre.csv
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3a077cadccc0b2da318e60ca2e0636d96319e5b0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103955680"
---
# <a name="genrecsv"></a><span data-ttu-id="983d7-107">genre.csv</span><span class="sxs-lookup"><span data-stu-id="983d7-107">genre.csv</span></span>

<span data-ttu-id="983d7-108">Questo file contiene una voce per ogni genere rappresentato nel catalogo.</span><span class="sxs-lookup"><span data-stu-id="983d7-108">This file contains an entry for each genre represented in the catalog.</span></span> <span data-ttu-id="983d7-109">Ogni voce è una riga costituita dai campi delimitati da tabulazioni descritti nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="983d7-109">Each entry is a row composed of the tab-delimited fields described in the table below.</span></span> <span data-ttu-id="983d7-110">I campi devono essere visualizzati nell'ordine elencato.</span><span class="sxs-lookup"><span data-stu-id="983d7-110">Fields must appear in the order listed.</span></span>

<span data-ttu-id="983d7-111">Tutti i campi nel genre.csv sono obbligatori.</span><span class="sxs-lookup"><span data-stu-id="983d7-111">All fields in genre.csv are required.</span></span>

<span data-ttu-id="983d7-112">La colonna Format nella tabella seguente descrive la modalità di formattazione di ogni campo di testo Unicode.</span><span class="sxs-lookup"><span data-stu-id="983d7-112">The Format column in the table below describes the way each Unicode text field is formatted.</span></span> <span data-ttu-id="983d7-113">Non si riferisce al tipo di dati del contenuto.</span><span class="sxs-lookup"><span data-stu-id="983d7-113">It does not refer to the data type of the contents.</span></span> <span data-ttu-id="983d7-114">Se, ad esempio, nella colonna formato è indicato Integer, significa che il campo contiene una stringa Unicode che rappresenta un valore integrale, anziché un numero intero effettivo.</span><span class="sxs-lookup"><span data-stu-id="983d7-114">For example, if Integer is indicated in the Format column, it means that the field contains a Unicode string representing an integral value, rather than an actual integer.</span></span>



| <span data-ttu-id="983d7-115">Campo</span><span class="sxs-lookup"><span data-stu-id="983d7-115">Field</span></span>             | <span data-ttu-id="983d7-116">Formato</span><span class="sxs-lookup"><span data-stu-id="983d7-116">Format</span></span>                                                    | <span data-ttu-id="983d7-117">Descrizione</span><span class="sxs-lookup"><span data-stu-id="983d7-117">Description</span></span>                                                                                                                                        |
|-------------------|-----------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="983d7-118">\_ID genere</span><span class="sxs-lookup"><span data-stu-id="983d7-118">Genre\_ID</span></span>         | <span data-ttu-id="983d7-119">Integer non negativo. Esempio: 22</span><span class="sxs-lookup"><span data-stu-id="983d7-119">Non-negative integer.Example: 22</span></span><br/>               | <span data-ttu-id="983d7-120">Identificatore del genere, univoco all'interno genre.csv.</span><span class="sxs-lookup"><span data-stu-id="983d7-120">Genre identifier, unique within genre.csv.</span></span> <span data-ttu-id="983d7-121">Deve essere minore di 2 ^ 32.</span><span class="sxs-lookup"><span data-stu-id="983d7-121">Must be less than 2^32.</span></span> <span data-ttu-id="983d7-122">È possibile ottenere un massimo di 64 generi.</span><span class="sxs-lookup"><span data-stu-id="983d7-122">A maximum of 64 genres is possible.</span></span>                                             |
| <span data-ttu-id="983d7-123">GenreTitle</span><span class="sxs-lookup"><span data-stu-id="983d7-123">GenreTitle</span></span>        | <span data-ttu-id="983d7-124">Stringa Unicode. Esempio: Rock</span><span class="sxs-lookup"><span data-stu-id="983d7-124">Unicode string.Example: Rock</span></span><br/>                   | <span data-ttu-id="983d7-125">Nome visualizzato del genere.</span><span class="sxs-lookup"><span data-stu-id="983d7-125">Genre display name.</span></span>                                                                                                                                |
| <span data-ttu-id="983d7-126">FeedsAreAvailable</span><span class="sxs-lookup"><span data-stu-id="983d7-126">FeedsAreAvailable</span></span> | <span data-ttu-id="983d7-127">Boolean. Format: \[ 0 \| 1\]</span><span class="sxs-lookup"><span data-stu-id="983d7-127">Boolean.Format: \[0\|1\]</span></span><br/> <span data-ttu-id="983d7-128">Esempio: 0</span><span class="sxs-lookup"><span data-stu-id="983d7-128">Example: 0</span></span><br/> | <span data-ttu-id="983d7-129">Indica se è possibile utilizzare il comportamento "Radio Play" passando a un feed.</span><span class="sxs-lookup"><span data-stu-id="983d7-129">Indicates whether "radio play" behavior is possible by jumping to a feed.</span></span>                                                                          |
| <span data-ttu-id="983d7-130">HasComposer</span><span class="sxs-lookup"><span data-stu-id="983d7-130">HasComposer</span></span>       | <span data-ttu-id="983d7-131">Boolean. Format: \[ 0 \| 1\]</span><span class="sxs-lookup"><span data-stu-id="983d7-131">Boolean.Format: \[0\|1\]</span></span><br/> <span data-ttu-id="983d7-132">Esempio: 1</span><span class="sxs-lookup"><span data-stu-id="983d7-132">Example: 1</span></span><br/> | <span data-ttu-id="983d7-133">True se questo genere deve salvare le informazioni del Composer nel catalogo.</span><span class="sxs-lookup"><span data-stu-id="983d7-133">True if this genre should save composer information in the catalog.</span></span> <span data-ttu-id="983d7-134">Se non è impostato, le informazioni del Composer vengono ignorate e non vengono compilate nel catalogo.</span><span class="sxs-lookup"><span data-stu-id="983d7-134">If not set, composer information is ignored and not compiled into the catalog.</span></span> |



 

 

 





