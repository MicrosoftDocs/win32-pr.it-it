---
title: track.csv
description: track.csv
ms.assetid: 5ce782b7-5fb8-4e6e-80cb-fa1dd7c47716
keywords:
- Windows Media Player Online Stores, track.csv
- archivi online, track.csv
- digitare 1 Store online, track.csv
- track.csv
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9826dbcc7b553caba89b2288057b643cdb0712bf
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104330660"
---
# <a name="trackcsv"></a><span data-ttu-id="5c93b-107">track.csv</span><span class="sxs-lookup"><span data-stu-id="5c93b-107">track.csv</span></span>

<span data-ttu-id="5c93b-108">Questo file contiene una voce per ogni traccia nel catalogo.</span><span class="sxs-lookup"><span data-stu-id="5c93b-108">This file contains an entry for each track in the catalog.</span></span> <span data-ttu-id="5c93b-109">Ogni voce è una riga costituita dai campi delimitati da tabulazioni descritti nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="5c93b-109">Each entry is a row composed of the tab-delimited fields described in the table below.</span></span> <span data-ttu-id="5c93b-110">I campi devono essere visualizzati nell'ordine elencato.</span><span class="sxs-lookup"><span data-stu-id="5c93b-110">Fields must appear in the order listed.</span></span>

<span data-ttu-id="5c93b-111">La colonna Format nella tabella seguente descrive la modalità di formattazione di ogni campo di testo Unicode.</span><span class="sxs-lookup"><span data-stu-id="5c93b-111">The Format column in the table below describes the way each Unicode text field is formatted.</span></span> <span data-ttu-id="5c93b-112">Non si riferisce al tipo di dati del contenuto.</span><span class="sxs-lookup"><span data-stu-id="5c93b-112">It does not refer to the data type of the contents.</span></span> <span data-ttu-id="5c93b-113">Se, ad esempio, nella colonna formato è indicato Integer, significa che il campo contiene una stringa Unicode che rappresenta un valore integrale, anziché un numero intero effettivo.</span><span class="sxs-lookup"><span data-stu-id="5c93b-113">For example, if Integer is indicated in the Format column, it means that the field contains a Unicode string representing an integral value, rather than an actual integer.</span></span>



<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="5c93b-114">Campo</span><span class="sxs-lookup"><span data-stu-id="5c93b-114">Field</span></span></th>
<th><span data-ttu-id="5c93b-115">Necessario</span><span class="sxs-lookup"><span data-stu-id="5c93b-115">Required</span></span></th>
<th><span data-ttu-id="5c93b-116">Formato</span><span class="sxs-lookup"><span data-stu-id="5c93b-116">Format</span></span></th>
<th><span data-ttu-id="5c93b-117">Descrizione</span><span class="sxs-lookup"><span data-stu-id="5c93b-117">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="5c93b-118">TrackID</span><span class="sxs-lookup"><span data-stu-id="5c93b-118">TrackID</span></span></td>
<td><span data-ttu-id="5c93b-119">Sì</span><span class="sxs-lookup"><span data-stu-id="5c93b-119">Yes</span></span></td>
<td><span data-ttu-id="5c93b-120">Integer non negativo. Esempio: 32789</span><span class="sxs-lookup"><span data-stu-id="5c93b-120">Non-negative integer.Example: 32789</span></span><br/></td>
<td><span data-ttu-id="5c93b-121">Identificatore univoco fornito dal provider di contenuti.</span><span class="sxs-lookup"><span data-stu-id="5c93b-121">Unique identifier provided by the content provider.</span></span> <span data-ttu-id="5c93b-122">Deve essere minore di 2 ^ 32. suggerimento per le prestazioni: se gli ID assegnati alle tracce dello stesso album sono numerati consecutivamente, la compressione del catalogo sarà più efficiente.</span><span class="sxs-lookup"><span data-stu-id="5c93b-122">Must be less than 2^32.Performance tip: If the IDs assigned to tracks from the same album are numbered consecutively, catalog compression will be more efficient.</span></span> <span data-ttu-id="5c93b-123">Tuttavia, la numerazione consecutiva delle tracce di album non è obbligatoria.</span><span class="sxs-lookup"><span data-stu-id="5c93b-123">However, consecutive numbering of album tracks is not required.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5c93b-124">TrackTitle</span><span class="sxs-lookup"><span data-stu-id="5c93b-124">TrackTitle</span></span></td>
<td><span data-ttu-id="5c93b-125">Sì</span><span class="sxs-lookup"><span data-stu-id="5c93b-125">Yes</span></span></td>
<td><span data-ttu-id="5c93b-126">Stringa Unicode.</span><span class="sxs-lookup"><span data-stu-id="5c93b-126">Unicode string.</span></span> <span data-ttu-id="5c93b-127">Esempio: Raygun Robbers ' Blues</span><span class="sxs-lookup"><span data-stu-id="5c93b-127">Example: Raygun Robbers' Blues</span></span></td>
<td><span data-ttu-id="5c93b-128">Nome della traccia.</span><span class="sxs-lookup"><span data-stu-id="5c93b-128">Name of the track.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="5c93b-129">Duration</span><span class="sxs-lookup"><span data-stu-id="5c93b-129">Duration</span></span></td>
<td><span data-ttu-id="5c93b-130">Sì</span><span class="sxs-lookup"><span data-stu-id="5c93b-130">Yes</span></span></td>
<td><span data-ttu-id="5c93b-131">Integer non negativo. Esempio: 543</span><span class="sxs-lookup"><span data-stu-id="5c93b-131">Non-negative integer.Example: 543</span></span><br/></td>
<td><span data-ttu-id="5c93b-132">Durata della traccia in secondi.</span><span class="sxs-lookup"><span data-stu-id="5c93b-132">Duration of the track in seconds.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5c93b-133">Numero</span><span class="sxs-lookup"><span data-stu-id="5c93b-133">TrackNumber</span></span></td>
<td><span data-ttu-id="5c93b-134">Sì</span><span class="sxs-lookup"><span data-stu-id="5c93b-134">Yes</span></span></td>
<td><span data-ttu-id="5c93b-135">Integer non negativo. Esempio: 7</span><span class="sxs-lookup"><span data-stu-id="5c93b-135">Non-negative integer.Example: 7</span></span><br/></td>
<td><span data-ttu-id="5c93b-136">Numero di traccia nell'album della traccia.</span><span class="sxs-lookup"><span data-stu-id="5c93b-136">Track number on the track's album.</span></span> <span data-ttu-id="5c93b-137">I numeri di traccia iniziano da 1 e aumentano tra i set di dischi.</span><span class="sxs-lookup"><span data-stu-id="5c93b-137">Track numbers begin at 1 and increase across disc sets.</span></span> <span data-ttu-id="5c93b-138">Il numero di traccia deve essere minore di 256.</span><span class="sxs-lookup"><span data-stu-id="5c93b-138">The track number must be less than 256.</span></span> <span data-ttu-id="5c93b-139">Un numero di traccia maggiore o uguale a 256 provocherà un comportamento imprevisto in Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="5c93b-139">A track number greater than or equal to 256 will cause unexpected behavior in Windows Media Player.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="5c93b-140">TrackPrice</span><span class="sxs-lookup"><span data-stu-id="5c93b-140">TrackPrice</span></span></td>
<td><span data-ttu-id="5c93b-141">Sì</span><span class="sxs-lookup"><span data-stu-id="5c93b-141">Yes</span></span></td>
<td><span data-ttu-id="5c93b-142">Stringa Unicode.</span><span class="sxs-lookup"><span data-stu-id="5c93b-142">Unicode string.</span></span> <span data-ttu-id="5c93b-143">Esempio: $0,99.</span><span class="sxs-lookup"><span data-stu-id="5c93b-143">Example: $0.99.</span></span></td>
<td><span data-ttu-id="5c93b-144">Tenere traccia del prezzo.</span><span class="sxs-lookup"><span data-stu-id="5c93b-144">Track price.</span></span> <span data-ttu-id="5c93b-145">È necessario includere il simbolo di valuta.</span><span class="sxs-lookup"><span data-stu-id="5c93b-145">The currency symbol should be included.</span></span> <span data-ttu-id="5c93b-146">La stringa vuota, 0 e-hanno un significato speciale.</span><span class="sxs-lookup"><span data-stu-id="5c93b-146">The empty string, 0, and - have special meaning.</span></span> <span data-ttu-id="5c93b-147">Una stringa vuota indica che il prezzo è sconosciuto.</span><span class="sxs-lookup"><span data-stu-id="5c93b-147">An empty string indicates that the price is unknown.</span></span> <span data-ttu-id="5c93b-148">Uno zero in questo campo indica che la traccia è gratuita e un trattino (-) indica che non è possibile acquistare la traccia.</span><span class="sxs-lookup"><span data-stu-id="5c93b-148">A zero in this field means the track is free, and a hyphen (-) indicates that the track cannot be bought.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5c93b-149">CanStream</span><span class="sxs-lookup"><span data-stu-id="5c93b-149">CanStream</span></span></td>
<td><span data-ttu-id="5c93b-150">Sì</span><span class="sxs-lookup"><span data-stu-id="5c93b-150">Yes</span></span></td>
<td><span data-ttu-id="5c93b-151">Proprietà di tipo Boolean.</span><span class="sxs-lookup"><span data-stu-id="5c93b-151">Boolean.</span></span> <span data-ttu-id="5c93b-152">Può essere 0 o 1. esempio: 0</span><span class="sxs-lookup"><span data-stu-id="5c93b-152">Can be 0 or 1.Example: 0</span></span><br/></td>
<td><span data-ttu-id="5c93b-153">Indica se è possibile trasmettere la traccia.</span><span class="sxs-lookup"><span data-stu-id="5c93b-153">Indicates whether the track can be streamed.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="5c93b-154">CanDownload</span><span class="sxs-lookup"><span data-stu-id="5c93b-154">CanDownload</span></span></td>
<td><span data-ttu-id="5c93b-155">Sì</span><span class="sxs-lookup"><span data-stu-id="5c93b-155">Yes</span></span></td>
<td><span data-ttu-id="5c93b-156">Proprietà di tipo Boolean.</span><span class="sxs-lookup"><span data-stu-id="5c93b-156">Boolean.</span></span> <span data-ttu-id="5c93b-157">Può essere 0 o 1. esempio: 0</span><span class="sxs-lookup"><span data-stu-id="5c93b-157">Can be 0 or 1.Example: 0</span></span><br/></td>
<td><span data-ttu-id="5c93b-158">Indica se è possibile scaricare la traccia.</span><span class="sxs-lookup"><span data-stu-id="5c93b-158">Indicates whether the track can be downloaded.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5c93b-159">HasPreviewClip</span><span class="sxs-lookup"><span data-stu-id="5c93b-159">HasPreviewClip</span></span></td>
<td><span data-ttu-id="5c93b-160">Sì</span><span class="sxs-lookup"><span data-stu-id="5c93b-160">Yes</span></span></td>
<td><span data-ttu-id="5c93b-161">Proprietà di tipo Boolean.</span><span class="sxs-lookup"><span data-stu-id="5c93b-161">Boolean.</span></span> <span data-ttu-id="5c93b-162">Può essere 0 o 1. esempio: 0</span><span class="sxs-lookup"><span data-stu-id="5c93b-162">Can be 0 or 1.Example: 0</span></span><br/></td>
<td><span data-ttu-id="5c93b-163">Indica se la traccia include una clip di anteprima.</span><span class="sxs-lookup"><span data-stu-id="5c93b-163">Indicates whether the track has a preview clip.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="5c93b-164">HasVideoClip</span><span class="sxs-lookup"><span data-stu-id="5c93b-164">HasVideoClip</span></span></td>
<td><span data-ttu-id="5c93b-165">Sì</span><span class="sxs-lookup"><span data-stu-id="5c93b-165">Yes</span></span></td>
<td><span data-ttu-id="5c93b-166">Proprietà di tipo Boolean.</span><span class="sxs-lookup"><span data-stu-id="5c93b-166">Boolean.</span></span> <span data-ttu-id="5c93b-167">Può essere 0 o 1. esempio: 0</span><span class="sxs-lookup"><span data-stu-id="5c93b-167">Can be 0 or 1.Example: 0</span></span><br/></td>
<td><span data-ttu-id="5c93b-168">Indica se la traccia contiene un clip video.</span><span class="sxs-lookup"><span data-stu-id="5c93b-168">Indicates whether the track has a video clip.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5c93b-169">ParentalRating</span><span class="sxs-lookup"><span data-stu-id="5c93b-169">ParentalRating</span></span></td>
<td><span data-ttu-id="5c93b-170">Sì</span><span class="sxs-lookup"><span data-stu-id="5c93b-170">Yes</span></span></td>
<td><span data-ttu-id="5c93b-171">Enumerazione.</span><span class="sxs-lookup"><span data-stu-id="5c93b-171">Enumeration.</span></span> <span data-ttu-id="5c93b-172">Può essere N, E o C. esempio: N</span><span class="sxs-lookup"><span data-stu-id="5c93b-172">Can be N, E, or C.Example: N</span></span><br/></td>
<td><span data-ttu-id="5c93b-173">Indica la classificazione consultiva padre.</span><span class="sxs-lookup"><span data-stu-id="5c93b-173">Indicates the Parental Advisory Rating.</span></span> <span data-ttu-id="5c93b-174">I valori N, e e C sono i valori normali, espliciti e puliti.</span><span class="sxs-lookup"><span data-stu-id="5c93b-174">The values N, E, and C stand for Normal, Explicit, and Clean.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="5c93b-175">LinkedAlbumID</span><span class="sxs-lookup"><span data-stu-id="5c93b-175">LinkedAlbumID</span></span></td>
<td><span data-ttu-id="5c93b-176">Sì</span><span class="sxs-lookup"><span data-stu-id="5c93b-176">Yes</span></span></td>
<td><span data-ttu-id="5c93b-177">Integer non negativo.</span><span class="sxs-lookup"><span data-stu-id="5c93b-177">Non-negative integer.</span></span> <span data-ttu-id="5c93b-178">Deve corrispondere all'ID di un album.</span><span class="sxs-lookup"><span data-stu-id="5c93b-178">Must be the ID of an Album.</span></span> <span data-ttu-id="5c93b-179">Esempio: 32423</span><span class="sxs-lookup"><span data-stu-id="5c93b-179">Example: 32423</span></span></td>
<td><span data-ttu-id="5c93b-180">ID dell'album che contiene la traccia.</span><span class="sxs-lookup"><span data-stu-id="5c93b-180">The ID of the album that contains this track.</span></span>
<blockquote>
[!Note]<br />
<span data-ttu-id="5c93b-181">Ogni traccia deve appartenere a un album.</span><span class="sxs-lookup"><span data-stu-id="5c93b-181">Every track must belong to an album.</span></span> <span data-ttu-id="5c93b-182">Ovvero, per ogni traccia, il campo LinkedAlbumID deve essere uguale a uno degli ID album nel file album.csv.</span><span class="sxs-lookup"><span data-stu-id="5c93b-182">That is, for each track, the LinkedAlbumID field must be equal to one of the album IDs in the album.csv file.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5c93b-183">LinkedTrackArtist_ArtistIDs</span><span class="sxs-lookup"><span data-stu-id="5c93b-183">LinkedTrackArtist_ArtistIDs</span></span></td>
<td><span data-ttu-id="5c93b-184">Sì</span><span class="sxs-lookup"><span data-stu-id="5c93b-184">Yes</span></span></td>
<td><span data-ttu-id="5c93b-185">Elenco di numeri interi.</span><span class="sxs-lookup"><span data-stu-id="5c93b-185">List of integers.</span></span> <span data-ttu-id="5c93b-186">L'elenco contiene gli ID degli artisti, separati da punti e virgola.</span><span class="sxs-lookup"><span data-stu-id="5c93b-186">The list contains artist IDs, separated by semicolons.</span></span> <span data-ttu-id="5c93b-187">Esempio: 41322; 12321; 82123;</span><span class="sxs-lookup"><span data-stu-id="5c93b-187">Example: 41322;12321; 82123;</span></span></td>
<td><span data-ttu-id="5c93b-188">Elenco di ID corrispondenti agli artisti che contribuiscono.</span><span class="sxs-lookup"><span data-stu-id="5c93b-188">A list of IDs corresponding to the contributing artists.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="5c93b-189">Composer</span><span class="sxs-lookup"><span data-stu-id="5c93b-189">Composer</span></span></td>
<td><span data-ttu-id="5c93b-190">No</span><span class="sxs-lookup"><span data-stu-id="5c93b-190">No</span></span></td>
<td><span data-ttu-id="5c93b-191">Stringa Unicode.</span><span class="sxs-lookup"><span data-stu-id="5c93b-191">Unicode string.</span></span> <span data-ttu-id="5c93b-192">Esempio: Beethoven</span><span class="sxs-lookup"><span data-stu-id="5c93b-192">Example: Beethoven</span></span></td>
<td><span data-ttu-id="5c93b-193">Compositore della traccia. Se per il genere della traccia non è impostato il campo HasComposer, il valore del campo Composer verrà ignorato.</span><span class="sxs-lookup"><span data-stu-id="5c93b-193">The composer of the track. If the track's genre does not have the HasComposer field set, the value of the Composer field will be ignored.</span></span> <span data-ttu-id="5c93b-194">Usato in genere solo per le tracce jazz o classiche.</span><span class="sxs-lookup"><span data-stu-id="5c93b-194">Typically used only for jazz or classical tracks.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5c93b-195">Popolarità</span><span class="sxs-lookup"><span data-stu-id="5c93b-195">Popularity</span></span></td>
<td><span data-ttu-id="5c93b-196">Sì</span><span class="sxs-lookup"><span data-stu-id="5c93b-196">Yes</span></span></td>
<td><span data-ttu-id="5c93b-197">Intero non negativo o float. esempio: 1252,6</span><span class="sxs-lookup"><span data-stu-id="5c93b-197">Non-negative integer or Float.Example: 1252.6</span></span><br/></td>
<td><span data-ttu-id="5c93b-198">Determina la posizione della traccia nell'elenco quando è ordinata in base alla popolarità.</span><span class="sxs-lookup"><span data-stu-id="5c93b-198">Determines the position of the track in the list when sorted by popularity.</span></span> <span data-ttu-id="5c93b-199">Un numero inferiore indica una maggiore popolarità.</span><span class="sxs-lookup"><span data-stu-id="5c93b-199">A lower number indicates higher popularity.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="5c93b-200">StarRating</span><span class="sxs-lookup"><span data-stu-id="5c93b-200">StarRating</span></span></td>
<td><span data-ttu-id="5c93b-201">No</span><span class="sxs-lookup"><span data-stu-id="5c93b-201">No</span></span></td>
<td><span data-ttu-id="5c93b-202">Float. esempio: 4,21</span><span class="sxs-lookup"><span data-stu-id="5c93b-202">Float.Example: 4.21</span></span><br/></td>
<td><span data-ttu-id="5c93b-203">La classificazione a stelle verrà arrotondata al più vicino a 1/4 stelle da Windows Media Player prima di essere visualizzata nell'interfaccia utente di Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="5c93b-203">The star rating will be rounded to the nearest 1/4 star by Windows Media Player before being displayed in the Windows Media Player user interface.</span></span></td>
</tr>
</tbody>
</table>



 

 

 





