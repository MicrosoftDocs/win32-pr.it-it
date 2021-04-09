---
title: list.csv
description: list.csv
ms.assetid: 020b213c-826c-430c-8ce7-92b819581de8
keywords:
- Windows Media Player Online Stores, list.csv
- archivi online, list.csv
- digitare 1 Store online, list.csv
- list.csv
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1f41ed237c5f4a185f01feace8f09b4615e4922b
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/19/2020
ms.locfileid: "104117347"
---
# <a name="listcsv"></a><span data-ttu-id="3ba26-107">list.csv</span><span class="sxs-lookup"><span data-stu-id="3ba26-107">list.csv</span></span>

<span data-ttu-id="3ba26-108">Questo file contiene una voce per ogni elenco contenente il catalogo.</span><span class="sxs-lookup"><span data-stu-id="3ba26-108">This file contains an entry for each of the lists the catalog contains.</span></span> <span data-ttu-id="3ba26-109">Gli elenchi possono essere elenchi di tracce, album, artisti, generi, sottogeneri o feed radiofonici; oppure possono essere elenchi di altri elenchi.</span><span class="sxs-lookup"><span data-stu-id="3ba26-109">Lists can be lists of tracks, albums, artists, genres, subgenres, or radio feeds; or they can be lists of other lists.</span></span> <span data-ttu-id="3ba26-110">Ogni voce di elenco è una riga costituita dai campi delimitati da tabulazioni descritti nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="3ba26-110">Each list entry is a row composed of the tab-delimited fields described in the table below.</span></span> <span data-ttu-id="3ba26-111">I campi devono essere visualizzati nell'ordine elencato.</span><span class="sxs-lookup"><span data-stu-id="3ba26-111">Fields must appear in the order listed.</span></span>

<span data-ttu-id="3ba26-112">La colonna Format nella tabella seguente descrive la modalità di formattazione di ogni campo di testo Unicode.</span><span class="sxs-lookup"><span data-stu-id="3ba26-112">The Format column in the table below describes the way each Unicode text field is formatted.</span></span> <span data-ttu-id="3ba26-113">Non si riferisce al tipo di dati del contenuto.</span><span class="sxs-lookup"><span data-stu-id="3ba26-113">It does not refer to the data type of the contents.</span></span> <span data-ttu-id="3ba26-114">Se, ad esempio, nella colonna formato è indicato Integer, significa che il campo contiene una stringa Unicode che rappresenta un valore integrale, anziché un numero intero effettivo.</span><span class="sxs-lookup"><span data-stu-id="3ba26-114">For example, if Integer is indicated in the Format column, it means that the field contains a Unicode string representing an integral value, rather than an actual integer.</span></span>



<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="3ba26-115">Campo</span><span class="sxs-lookup"><span data-stu-id="3ba26-115">Field</span></span></th>
<th><span data-ttu-id="3ba26-116">Necessario</span><span class="sxs-lookup"><span data-stu-id="3ba26-116">Required</span></span></th>
<th><span data-ttu-id="3ba26-117">Formato</span><span class="sxs-lookup"><span data-stu-id="3ba26-117">Format</span></span></th>
<th><span data-ttu-id="3ba26-118">Descrizione</span><span class="sxs-lookup"><span data-stu-id="3ba26-118">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="3ba26-119">ListID</span><span class="sxs-lookup"><span data-stu-id="3ba26-119">ListID</span></span></td>
<td><span data-ttu-id="3ba26-120">Sì</span><span class="sxs-lookup"><span data-stu-id="3ba26-120">Yes</span></span></td>
<td><span data-ttu-id="3ba26-121">Integer non negativo.</span><span class="sxs-lookup"><span data-stu-id="3ba26-121">Non-negative integer.</span></span></td>
<td><span data-ttu-id="3ba26-122">Identificatore dell'elenco, univoco all'interno list.csv.</span><span class="sxs-lookup"><span data-stu-id="3ba26-122">List identifier, unique within list.csv.</span></span> <span data-ttu-id="3ba26-123">Deve essere non negativo e minore di 2 ^ 32. <strong>Visualizzazione di un nodo elenco nel controllo di visualizzazione albero:</strong> Se ListID è 0, 1, 2, 3, 4, 5, 6 o 7, l'elenco verrà visualizzato come nodo personalizzato nel nodo di primo livello del negozio online nel controllo di visualizzazione albero del lettore.</span><span class="sxs-lookup"><span data-stu-id="3ba26-123">Must be non-negative and less than 2^32.<strong>Displaying a list node in tree view control:</strong> If the ListID is 0, 1, 2, 3, 4, 5, 6, or 7, the list will appear as a custom node under your online store's top-level node in the Player's tree view control.</span></span> <span data-ttu-id="3ba26-124">I nodi personalizzati vengono visualizzati prima dei nodi standard nel nodo di primo livello del negozio online e sono posizionati in ordine crescente in base a ListID.</span><span class="sxs-lookup"><span data-stu-id="3ba26-124">Custom nodes appear before the standard nodes under the online store's top-level node, and they are positioned in ascending order by ListID.</span></span> <span data-ttu-id="3ba26-125">Se ad esempio sono presenti tre nodi personalizzati, con ListId di 1, 3 e 5, verranno visualizzati prima, secondo e terzo nel nodo di primo livello del negozio online.</span><span class="sxs-lookup"><span data-stu-id="3ba26-125">For example, if there are three custom nodes, with ListIDs of 1, 3, and 5, they will be displayed first, second, and third under the online store's top level node.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3ba26-126">Titoloelenco</span><span class="sxs-lookup"><span data-stu-id="3ba26-126">ListTitle</span></span></td>
<td><span data-ttu-id="3ba26-127">No</span><span class="sxs-lookup"><span data-stu-id="3ba26-127">No</span></span></td>
<td><span data-ttu-id="3ba26-128">Stringa Unicode. Esempio: primi dieci riscontri</span><span class="sxs-lookup"><span data-stu-id="3ba26-128">Unicode string.Example: Top Ten Hits</span></span><br/></td>
<td><span data-ttu-id="3ba26-129">Titolo dell'elenco.</span><span class="sxs-lookup"><span data-stu-id="3ba26-129">List title.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3ba26-130">ListSubtitle</span><span class="sxs-lookup"><span data-stu-id="3ba26-130">ListSubtitle</span></span></td>
<td><span data-ttu-id="3ba26-131">No</span><span class="sxs-lookup"><span data-stu-id="3ba26-131">No</span></span></td>
<td><span data-ttu-id="3ba26-132">Stringa Unicode</span><span class="sxs-lookup"><span data-stu-id="3ba26-132">Unicode string</span></span></td>
<td><span data-ttu-id="3ba26-133">Elenca il titolo alternativo, visualizzato nella seconda riga della visualizzazione affiancata.</span><span class="sxs-lookup"><span data-stu-id="3ba26-133">List alternate title, displayed in the second line of the Tile view.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3ba26-134">ListDescription</span><span class="sxs-lookup"><span data-stu-id="3ba26-134">ListDescription</span></span></td>
<td><span data-ttu-id="3ba26-135">Sì</span><span class="sxs-lookup"><span data-stu-id="3ba26-135">Yes</span></span></td>
<td><span data-ttu-id="3ba26-136">Stringa Unicode</span><span class="sxs-lookup"><span data-stu-id="3ba26-136">Unicode string</span></span></td>
<td><span data-ttu-id="3ba26-137">Elenca il testo visualizzato descrittivo (visualizzato nelle pagine delle proprietà).</span><span class="sxs-lookup"><span data-stu-id="3ba26-137">List friendly display text (displayed in property pages).</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3ba26-138">Linked_ItemType</span><span class="sxs-lookup"><span data-stu-id="3ba26-138">Linked_ItemType</span></span></td>
<td><span data-ttu-id="3ba26-139">Sì</span><span class="sxs-lookup"><span data-stu-id="3ba26-139">Yes</span></span></td>
<td><span data-ttu-id="3ba26-140">Stringa Unicode. Formato: [T | P | A | L | G | S | R</span><span class="sxs-lookup"><span data-stu-id="3ba26-140">Unicode string.Format: [T|P|A|L|G|S|R]</span></span><br/> <span data-ttu-id="3ba26-141">Esempio: T</span><span class="sxs-lookup"><span data-stu-id="3ba26-141">Example: T</span></span><br/></td>
<td><span data-ttu-id="3ba26-142">Indica il tipo degli elementi collegati.</span><span class="sxs-lookup"><span data-stu-id="3ba26-142">Indicates the type of the linked items.</span></span>
<ul>
<li><span data-ttu-id="3ba26-143">T = Track</span><span class="sxs-lookup"><span data-stu-id="3ba26-143">T= Track</span></span></li>
<li><span data-ttu-id="3ba26-144">P = esecutore</span><span class="sxs-lookup"><span data-stu-id="3ba26-144">P = Performer</span></span></li>
<li><span data-ttu-id="3ba26-145">A = album</span><span class="sxs-lookup"><span data-stu-id="3ba26-145">A = Album</span></span></li>
<li><span data-ttu-id="3ba26-146">L = elenco</span><span class="sxs-lookup"><span data-stu-id="3ba26-146">L = List</span></span></li>
<li><span data-ttu-id="3ba26-147">G = genere</span><span class="sxs-lookup"><span data-stu-id="3ba26-147">G = Genre</span></span></li>
<li><span data-ttu-id="3ba26-148">S = sottogenere</span><span class="sxs-lookup"><span data-stu-id="3ba26-148">S = Subgenre</span></span></li>
<li><span data-ttu-id="3ba26-149">R = radio</span><span class="sxs-lookup"><span data-stu-id="3ba26-149">R = Radio</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3ba26-150">ListPrice</span><span class="sxs-lookup"><span data-stu-id="3ba26-150">ListPrice</span></span></td>
<td><span data-ttu-id="3ba26-151">Sì</span><span class="sxs-lookup"><span data-stu-id="3ba26-151">Yes</span></span></td>
<td><span data-ttu-id="3ba26-152">Stringa Unicode. Esempio: $9,99</span><span class="sxs-lookup"><span data-stu-id="3ba26-152">Unicode string.Example: $9.99</span></span><br/></td>
<td><span data-ttu-id="3ba26-153">Prezzo dell'elenco.</span><span class="sxs-lookup"><span data-stu-id="3ba26-153">Price of the list.</span></span> <span data-ttu-id="3ba26-154">È necessario includere il simbolo di valuta. Zero indica che l'elenco è gratuito.</span><span class="sxs-lookup"><span data-stu-id="3ba26-154">The currency symbol should be included.A zero means the list is free.</span></span> <span data-ttu-id="3ba26-155">Nessun valore indica che il prezzo è sconosciuto.</span><span class="sxs-lookup"><span data-stu-id="3ba26-155">No value means the price is unknown.</span></span> <span data-ttu-id="3ba26-156">Un trattino indica che non è possibile acquistare l'elenco.</span><span class="sxs-lookup"><span data-stu-id="3ba26-156">A hyphen means the list cannot be purchased.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3ba26-157">Popolarità</span><span class="sxs-lookup"><span data-stu-id="3ba26-157">Popularity</span></span></td>
<td><span data-ttu-id="3ba26-158">Sì</span><span class="sxs-lookup"><span data-stu-id="3ba26-158">Yes</span></span></td>
<td><span data-ttu-id="3ba26-159">Integer o valore decimale. Esempio: 1259,3</span><span class="sxs-lookup"><span data-stu-id="3ba26-159">Integer or decimal value.Example: 1259.3</span></span><br/></td>
<td><span data-ttu-id="3ba26-160">Indica la classificazione della popolarità quando questo elenco viene visualizzato in altri elenchi.</span><span class="sxs-lookup"><span data-stu-id="3ba26-160">Indicates the popularity ranking when this list appears in other lists.</span></span> <span data-ttu-id="3ba26-161">Può essere zero se non è applicabile.</span><span class="sxs-lookup"><span data-stu-id="3ba26-161">Can be zero if not applicable..</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3ba26-162">IsRecentlyAdded</span><span class="sxs-lookup"><span data-stu-id="3ba26-162">IsRecentlyAdded</span></span></td>
<td><span data-ttu-id="3ba26-163">Sì</span><span class="sxs-lookup"><span data-stu-id="3ba26-163">Yes</span></span></td>
<td><span data-ttu-id="3ba26-164">Boolean. Format: [0 | 1]</span><span class="sxs-lookup"><span data-stu-id="3ba26-164">Boolean.Format: [0|1]</span></span><br/> <span data-ttu-id="3ba26-165">Esempio: 0</span><span class="sxs-lookup"><span data-stu-id="3ba26-165">Example: 0</span></span><br/></td>
<td><span data-ttu-id="3ba26-166">Indica se l'elenco è stato aggiunto di recente.</span><span class="sxs-lookup"><span data-stu-id="3ba26-166">Indicates whether the list was recently added.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3ba26-167">Funzionalità di</span><span class="sxs-lookup"><span data-stu-id="3ba26-167">IsFeatured</span></span></td>
<td><span data-ttu-id="3ba26-168">Sì</span><span class="sxs-lookup"><span data-stu-id="3ba26-168">Yes</span></span></td>
<td><span data-ttu-id="3ba26-169">Boolean. Format: [0 | 1]</span><span class="sxs-lookup"><span data-stu-id="3ba26-169">Boolean.Format: [0|1]</span></span><br/> <span data-ttu-id="3ba26-170">Esempio: 0</span><span class="sxs-lookup"><span data-stu-id="3ba26-170">Example: 0</span></span><br/></td>
<td><span data-ttu-id="3ba26-171">Indica se l'elenco è in primo piano.</span><span class="sxs-lookup"><span data-stu-id="3ba26-171">Indicates whether the list is featured.</span></span> <span data-ttu-id="3ba26-172">Può essere utilizzato per determinare l'ordinamento.</span><span class="sxs-lookup"><span data-stu-id="3ba26-172">Can be used in determining sort order.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3ba26-173">EditorialGlyph</span><span class="sxs-lookup"><span data-stu-id="3ba26-173">EditorialGlyph</span></span></td>
<td><span data-ttu-id="3ba26-174">Sì</span><span class="sxs-lookup"><span data-stu-id="3ba26-174">Yes</span></span></td>
<td><span data-ttu-id="3ba26-175">Integer non negativo.</span><span class="sxs-lookup"><span data-stu-id="3ba26-175">Non-negative integer.</span></span> <span data-ttu-id="3ba26-176">Deve essere 0.</span><span class="sxs-lookup"><span data-stu-id="3ba26-176">Should be 0.</span></span></td>
<td><span data-ttu-id="3ba26-177">Non utilizzato in questa versione.</span><span class="sxs-lookup"><span data-stu-id="3ba26-177">Not used in this release.</span></span> <span data-ttu-id="3ba26-178">Deve essere 0.</span><span class="sxs-lookup"><span data-stu-id="3ba26-178">Should be 0.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3ba26-179">ViewType</span><span class="sxs-lookup"><span data-stu-id="3ba26-179">ViewType</span></span></td>
<td><span data-ttu-id="3ba26-180">Sì</span><span class="sxs-lookup"><span data-stu-id="3ba26-180">Yes</span></span></td>
<td><span data-ttu-id="3ba26-181">Stringa Unicode.</span><span class="sxs-lookup"><span data-stu-id="3ba26-181">Unicode string.</span></span> <span data-ttu-id="3ba26-182">Formato: [I | T | R | L | O] esempio: T</span><span class="sxs-lookup"><span data-stu-id="3ba26-182">Format: [I|T|R|L|O]Example: T</span></span><br/></td>
<td><span data-ttu-id="3ba26-183">Indica il tipo di visualizzazione da utilizzare per l'elenco.</span><span class="sxs-lookup"><span data-stu-id="3ba26-183">Indicates the view type to use for the list.</span></span>
<ul>
<li><span data-ttu-id="3ba26-184">I = icona</span><span class="sxs-lookup"><span data-stu-id="3ba26-184">I = Icon</span></span></li>
<li><span data-ttu-id="3ba26-185">T = riquadro</span><span class="sxs-lookup"><span data-stu-id="3ba26-185">T = Tile</span></span></li>
<li><span data-ttu-id="3ba26-186">R = report</span><span class="sxs-lookup"><span data-stu-id="3ba26-186">R = Report</span></span></li>
<li><span data-ttu-id="3ba26-187">L = elenco</span><span class="sxs-lookup"><span data-stu-id="3ba26-187">L = List</span></span></li>
<li><span data-ttu-id="3ba26-188">O = elenco ordinato</span><span class="sxs-lookup"><span data-stu-id="3ba26-188">O = Ordered List</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3ba26-189">ViewImageSize</span><span class="sxs-lookup"><span data-stu-id="3ba26-189">ViewImageSize</span></span></td>
<td><span data-ttu-id="3ba26-190">Sì</span><span class="sxs-lookup"><span data-stu-id="3ba26-190">Yes</span></span></td>
<td><span data-ttu-id="3ba26-191">Integer non negativo. Esempio: 180</span><span class="sxs-lookup"><span data-stu-id="3ba26-191">Non-negative integer.Example: 180</span></span><br/></td>
<td><span data-ttu-id="3ba26-192">Dimensione in corrispondenza della quale viene visualizzata l'immagine dell'elenco.</span><span class="sxs-lookup"><span data-stu-id="3ba26-192">The size at which the list image is displayed.</span></span> <span data-ttu-id="3ba26-193">Se è 0, la dimensione viene determinata automaticamente.</span><span class="sxs-lookup"><span data-stu-id="3ba26-193">If 0, size is determined automatically.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3ba26-194">GroupBy</span><span class="sxs-lookup"><span data-stu-id="3ba26-194">GroupBy</span></span></td>
<td><span data-ttu-id="3ba26-195">Sì</span><span class="sxs-lookup"><span data-stu-id="3ba26-195">Yes</span></span></td>
<td><span data-ttu-id="3ba26-196">Stringa Unicode. Formato: [-| P | A | C | R | D</span><span class="sxs-lookup"><span data-stu-id="3ba26-196">Unicode string.Format: [-|P|A|C|R|D]</span></span><br/> <span data-ttu-id="3ba26-197">Esempio: P</span><span class="sxs-lookup"><span data-stu-id="3ba26-197">Example: P</span></span><br/></td>
<td><span data-ttu-id="3ba26-198">Indica il campo utilizzato per raggruppare gli elementi nell'elenco.</span><span class="sxs-lookup"><span data-stu-id="3ba26-198">Indicates what field is used to group the items in the list.</span></span>
<ul>
<li><span data-ttu-id="3ba26-199">- = Automatico</span><span class="sxs-lookup"><span data-stu-id="3ba26-199">- = Automatic</span></span></li>
<li><span data-ttu-id="3ba26-200">P = esecutore</span><span class="sxs-lookup"><span data-stu-id="3ba26-200">P = Performer</span></span></li>
<li><span data-ttu-id="3ba26-201">A = album</span><span class="sxs-lookup"><span data-stu-id="3ba26-201">A = Album</span></span></li>
<li><span data-ttu-id="3ba26-202">C = Composer</span><span class="sxs-lookup"><span data-stu-id="3ba26-202">C = Composer</span></span></li>
<li><span data-ttu-id="3ba26-203">R = classificazione</span><span class="sxs-lookup"><span data-stu-id="3ba26-203">R = Rating</span></span></li>
<li><span data-ttu-id="3ba26-204">D = Data</span><span class="sxs-lookup"><span data-stu-id="3ba26-204">D = Date</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3ba26-205">ListItemsAreDynamic</span><span class="sxs-lookup"><span data-stu-id="3ba26-205">ListItemsAreDynamic</span></span></td>
<td><span data-ttu-id="3ba26-206">Sì</span><span class="sxs-lookup"><span data-stu-id="3ba26-206">Yes</span></span></td>
<td><span data-ttu-id="3ba26-207">Proprietà di tipo Boolean.</span><span class="sxs-lookup"><span data-stu-id="3ba26-207">Boolean.</span></span> <span data-ttu-id="3ba26-208">Può essere 0 o 1.</span><span class="sxs-lookup"><span data-stu-id="3ba26-208">Can be 0 or 1.</span></span></td>
<td><span data-ttu-id="3ba26-209">Indica se l'elenco viene generato dinamicamente.</span><span class="sxs-lookup"><span data-stu-id="3ba26-209">Indicates whether the list is generated dynamically.</span></span> <span data-ttu-id="3ba26-210">Gli elenchi dinamici non contengono elementi in listitem.csv.</span><span class="sxs-lookup"><span data-stu-id="3ba26-210">Dynamic lists do not have items in listitem.csv.</span></span> <span data-ttu-id="3ba26-211">Se un elenco è contrassegnato come dinamico, i relativi elementi vengono forniti da <a href="/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-getlistcontents">IWMPContentPartner:: GetListContents</a></span><span class="sxs-lookup"><span data-stu-id="3ba26-211">If a list is marked as dynamic, its items are provided by <a href="/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-getlistcontents">IWMPContentPartner::GetListContents</a></span></span></td>
</tr>
</tbody>
</table>



 

 

 





