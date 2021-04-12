---
title: listitem.csv
description: listitem.csv
ms.assetid: d8f4bdb3-e7a5-4080-9ae7-555bf3695e9c
keywords:
- Windows Media Player Online Stores, listitem.csv
- archivi online, listitem.csv
- digitare 1 Store online, listitem.csv
- listitem.csv
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fe080c5b9426d5394a7d05c1bd293bba84014b0e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104395714"
---
# <a name="listitemcsv"></a><span data-ttu-id="01fb7-107">listitem.csv</span><span class="sxs-lookup"><span data-stu-id="01fb7-107">listitem.csv</span></span>

<span data-ttu-id="01fb7-108">Questo file contiene le voci per ogni elemento incluso in un elenco.</span><span class="sxs-lookup"><span data-stu-id="01fb7-108">This file contains entries for each item that is included in a list.</span></span> <span data-ttu-id="01fb7-109">Ogni voce è una riga costituita dai campi delimitati da tabulazioni descritti nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="01fb7-109">Each entry is a row composed of the tab-delimited fields described in the table below.</span></span> <span data-ttu-id="01fb7-110">I campi devono essere visualizzati nell'ordine elencato.</span><span class="sxs-lookup"><span data-stu-id="01fb7-110">Fields must appear in the order listed.</span></span>

<span data-ttu-id="01fb7-111">Tutti i campi sono obbligatori.</span><span class="sxs-lookup"><span data-stu-id="01fb7-111">All fields are required.</span></span>

<span data-ttu-id="01fb7-112">La colonna Format nella tabella seguente descrive la modalità di formattazione di ogni campo di testo Unicode.</span><span class="sxs-lookup"><span data-stu-id="01fb7-112">The Format column in the table below describes the way each Unicode text field is formatted.</span></span> <span data-ttu-id="01fb7-113">Non si riferisce al tipo di dati del contenuto.</span><span class="sxs-lookup"><span data-stu-id="01fb7-113">It does not refer to the data type of the contents.</span></span> <span data-ttu-id="01fb7-114">Se, ad esempio, nella colonna formato è indicato Integer, significa che il campo contiene una stringa Unicode che rappresenta un valore integrale, anziché un numero intero effettivo.</span><span class="sxs-lookup"><span data-stu-id="01fb7-114">For example, if Integer is indicated in the Format column, it means that the field contains a Unicode string representing an integral value, rather than an actual integer.</span></span>



| <span data-ttu-id="01fb7-115">Campo</span><span class="sxs-lookup"><span data-stu-id="01fb7-115">Field</span></span>              | <span data-ttu-id="01fb7-116">Formato</span><span class="sxs-lookup"><span data-stu-id="01fb7-116">Format</span></span>                                          | <span data-ttu-id="01fb7-117">Descrizione</span><span class="sxs-lookup"><span data-stu-id="01fb7-117">Description</span></span>                                                                                                            |
|--------------------|-------------------------------------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="01fb7-118">\_ListId collegato</span><span class="sxs-lookup"><span data-stu-id="01fb7-118">Linked\_ListID</span></span>     | <span data-ttu-id="01fb7-119">Integer non negativo. Esempio: 465</span><span class="sxs-lookup"><span data-stu-id="01fb7-119">Non-negative integer.Example: 465</span></span><br/>    | <span data-ttu-id="01fb7-120">ID dell'elenco di cui fa parte questo elemento.</span><span class="sxs-lookup"><span data-stu-id="01fb7-120">The ID of the list this item is part of.</span></span>                                                                               |
| <span data-ttu-id="01fb7-121">\_ListItem collegato</span><span class="sxs-lookup"><span data-stu-id="01fb7-121">Linked\_ListItem</span></span>   | <span data-ttu-id="01fb7-122">Integer non negativo. Esempio: 684793</span><span class="sxs-lookup"><span data-stu-id="01fb7-122">Non-negative integer.Example: 684793</span></span><br/> | <span data-ttu-id="01fb7-123">ID dell'elemento.</span><span class="sxs-lookup"><span data-stu-id="01fb7-123">The ID of the item.</span></span> <span data-ttu-id="01fb7-124">Può essere l'ID di una traccia, un album, un artista, un genere, un sottogenere, un feed di radio o un altro elenco.</span><span class="sxs-lookup"><span data-stu-id="01fb7-124">Can be the ID of a track, an album, an artist, a genre, a subgenre, a radio feed, or another list.</span></span> |
| <span data-ttu-id="01fb7-125">ItemPositionInList</span><span class="sxs-lookup"><span data-stu-id="01fb7-125">ItemPositionInList</span></span> | <span data-ttu-id="01fb7-126">Integer non negativo. Esempio: 5</span><span class="sxs-lookup"><span data-stu-id="01fb7-126">Non-negative integer.Example: 5</span></span><br/>      | <span data-ttu-id="01fb7-127">Posizione dell'elemento all'interno dell'elenco.</span><span class="sxs-lookup"><span data-stu-id="01fb7-127">The position of the item within its list.</span></span> <span data-ttu-id="01fb7-128">Il primo elemento di un elenco è nella posizione 0.</span><span class="sxs-lookup"><span data-stu-id="01fb7-128">The first item in a list is at position 0.</span></span>                                   |



 

 

 





