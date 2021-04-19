---
title: PLAYLIST. Columns
description: L'attributo Columns definisce le colonne visualizzate nell'elemento PLAYLIST.
ms.assetid: a805ee06-cf73-4eab-bcda-c374e55cd11a
keywords:
- PLAYLIST. Columns Media Player Windows
topic_type:
- apiref
api_name:
- PLAYLIST.columns
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fcc5f8ef5dc76428ca892d079b60692e6949a5ca
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325998"
---
# <a name="playlistcolumns"></a><span data-ttu-id="20bd3-104">PLAYLIST. Columns</span><span class="sxs-lookup"><span data-stu-id="20bd3-104">PLAYLIST.columns</span></span>

<span data-ttu-id="20bd3-105">L'attributo **Columns** definisce le colonne visualizzate nell'elemento **playlist** .</span><span class="sxs-lookup"><span data-stu-id="20bd3-105">The **columns** attribute defines the columns that appear in the **PLAYLIST** element.</span></span>

``` syntax
        elementID.columns
```

## <a name="possible-values"></a><span data-ttu-id="20bd3-106">Valori possibili</span><span class="sxs-lookup"><span data-stu-id="20bd3-106">Possible Values</span></span>

<span data-ttu-id="20bd3-107">Questo attributo è una **stringa** di lettura/scrittura nel formato seguente:</span><span class="sxs-lookup"><span data-stu-id="20bd3-107">This attribute is a read/write **String** in the following format:</span></span>

<span data-ttu-id="20bd3-108">\_nome database = nome DEscrittivo \_ ; \_ nome database = nome descrittivo \_ ;</span><span class="sxs-lookup"><span data-stu-id="20bd3-108">DB\_NAME=FRIENDLY\_NAME;DB\_NAME=FRIENDLY\_NAME;</span></span>

<span data-ttu-id="20bd3-109">Nome descrittivo \_ è il valore visualizzato nell'intestazione di colonna dell'elemento playlist e il \_ nome del database è un valore della tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="20bd3-109">FRIENDLY\_NAME is the value shown in the column header of the PLAYLIST element, and DB\_NAME is a value from the following table.</span></span> <span data-ttu-id="20bd3-110">Si noti che un elemento della playlist può essere un elemento multimediale dalla libreria o da un CD oppure può essere un'altra **playlist** creata dall'utente o ricavata da un CD.</span><span class="sxs-lookup"><span data-stu-id="20bd3-110">Note that a Playlist item might be a media item from the library or from a CD, or it might be another **Playlist** that is either user-created or taken from a CD.</span></span> <span data-ttu-id="20bd3-111">Alcune colonne sono valide solo con determinati elementi della playlist come indicato nella colonna Descrizione.</span><span class="sxs-lookup"><span data-stu-id="20bd3-111">Some columns are valid only with certain Playlist items as indicated in the Description column.</span></span>



| <span data-ttu-id="20bd3-112">Valore</span><span class="sxs-lookup"><span data-stu-id="20bd3-112">Value</span></span>             | <span data-ttu-id="20bd3-113">Descrizione</span><span class="sxs-lookup"><span data-stu-id="20bd3-113">Description</span></span>                                                                                                             |
|-------------------|-------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="20bd3-114">Album</span><span class="sxs-lookup"><span data-stu-id="20bd3-114">Album</span></span>             | <span data-ttu-id="20bd3-115">Nome dell'album.</span><span class="sxs-lookup"><span data-stu-id="20bd3-115">The name of the album.</span></span> <span data-ttu-id="20bd3-116">Utilizzato solo con elementi multimediali.</span><span class="sxs-lookup"><span data-stu-id="20bd3-116">Used with media items only.</span></span>                                                                      |
| <span data-ttu-id="20bd3-117">Artista</span><span class="sxs-lookup"><span data-stu-id="20bd3-117">Artist</span></span>            | <span data-ttu-id="20bd3-118">Nome dell'artista.</span><span class="sxs-lookup"><span data-stu-id="20bd3-118">The name of the artist.</span></span> <span data-ttu-id="20bd3-119">Non usato con le playlist create dall'utente.</span><span class="sxs-lookup"><span data-stu-id="20bd3-119">Not used with user-created playlists.</span></span>                                                           |
| <span data-ttu-id="20bd3-120">Autore</span><span class="sxs-lookup"><span data-stu-id="20bd3-120">Author</span></span>            | <span data-ttu-id="20bd3-121">Nome dell'artista.</span><span class="sxs-lookup"><span data-stu-id="20bd3-121">The name of the artist.</span></span>                                                                                                 |
| <span data-ttu-id="20bd3-122">Bitrate</span><span class="sxs-lookup"><span data-stu-id="20bd3-122">Bitrate</span></span>           | <span data-ttu-id="20bd3-123">Velocità in bit del contenuto.</span><span class="sxs-lookup"><span data-stu-id="20bd3-123">The bit rate of the content.</span></span> <span data-ttu-id="20bd3-124">Utilizzato solo con gli elementi multimediali della libreria.</span><span class="sxs-lookup"><span data-stu-id="20bd3-124">Used only with media items from the library.</span></span>                                               |
| <span data-ttu-id="20bd3-125">CDTrackEnabled</span><span class="sxs-lookup"><span data-stu-id="20bd3-125">CDTrackEnabled</span></span>    | <span data-ttu-id="20bd3-126">Indica se la traccia del CD è abilitata.</span><span class="sxs-lookup"><span data-stu-id="20bd3-126">Indicates whether the CD track is enabled.</span></span> <span data-ttu-id="20bd3-127">Utilizzato solo con gli elementi multimediali CD.</span><span class="sxs-lookup"><span data-stu-id="20bd3-127">Used only with CD media items.</span></span>                                               |
| <span data-ttu-id="20bd3-128">Selezionata</span><span class="sxs-lookup"><span data-stu-id="20bd3-128">Checked</span></span>           | <span data-ttu-id="20bd3-129">Riservato per utilizzi futuri.</span><span class="sxs-lookup"><span data-stu-id="20bd3-129">Reserved for future use.</span></span>                                                                                                |
| <span data-ttu-id="20bd3-130">Copyright</span><span class="sxs-lookup"><span data-stu-id="20bd3-130">Copyright</span></span>         | <span data-ttu-id="20bd3-131">Copyright della playlist.</span><span class="sxs-lookup"><span data-stu-id="20bd3-131">The copyright of the playlist.</span></span> <span data-ttu-id="20bd3-132">Non usato con playlist CD o elementi multimediali.</span><span class="sxs-lookup"><span data-stu-id="20bd3-132">Not used with CD playlists or media items.</span></span>                                               |
| <span data-ttu-id="20bd3-133">CreationDate</span><span class="sxs-lookup"><span data-stu-id="20bd3-133">CreationDate</span></span>      | <span data-ttu-id="20bd3-134">Data e ora di creazione della voce nella libreria.</span><span class="sxs-lookup"><span data-stu-id="20bd3-134">The date and time that the entry in the library was created.</span></span> <span data-ttu-id="20bd3-135">Utilizzato solo con gli elementi della libreria.</span><span class="sxs-lookup"><span data-stu-id="20bd3-135">Used only with items from the library.</span></span>                     |
| <span data-ttu-id="20bd3-136">DigitallySecure</span><span class="sxs-lookup"><span data-stu-id="20bd3-136">DigitallySecure</span></span>   | <span data-ttu-id="20bd3-137">Indica se l'elemento è protetto con Windows Media Rights Manager.</span><span class="sxs-lookup"><span data-stu-id="20bd3-137">Indicates whether the item is protected with Windows Media Rights Manager.</span></span> <span data-ttu-id="20bd3-138">Utilizzato solo con gli elementi multimediali della libreria.</span><span class="sxs-lookup"><span data-stu-id="20bd3-138">Used only with media items from the library.</span></span> |
| <span data-ttu-id="20bd3-139">Duration</span><span class="sxs-lookup"><span data-stu-id="20bd3-139">Duration</span></span>          | <span data-ttu-id="20bd3-140">Durata dell'elemento multimediale.</span><span class="sxs-lookup"><span data-stu-id="20bd3-140">The duration of the media item.</span></span>                                                                                         |
| <span data-ttu-id="20bd3-141">FileType</span><span class="sxs-lookup"><span data-stu-id="20bd3-141">FileType</span></span>          | <span data-ttu-id="20bd3-142">Riservato per utilizzi futuri.</span><span class="sxs-lookup"><span data-stu-id="20bd3-142">Reserved for future use.</span></span>                                                                                                |
| <span data-ttu-id="20bd3-143">Genre</span><span class="sxs-lookup"><span data-stu-id="20bd3-143">Genre</span></span>             | <span data-ttu-id="20bd3-144">Genere della playlist.</span><span class="sxs-lookup"><span data-stu-id="20bd3-144">The genre of the playlist.</span></span> <span data-ttu-id="20bd3-145">Non usato con playlist da CDs.</span><span class="sxs-lookup"><span data-stu-id="20bd3-145">Not used with playlists from CDs.</span></span>                                                            |
| <span data-ttu-id="20bd3-146">MediaAttribute</span><span class="sxs-lookup"><span data-stu-id="20bd3-146">MediaAttribute</span></span>    | <span data-ttu-id="20bd3-147">Riservato per utilizzi futuri.</span><span class="sxs-lookup"><span data-stu-id="20bd3-147">Reserved for future use.</span></span>                                                                                                |
| <span data-ttu-id="20bd3-148">MediaType</span><span class="sxs-lookup"><span data-stu-id="20bd3-148">MediaType</span></span>         | <span data-ttu-id="20bd3-149">Tipo di elemento multimediale (audio o video).</span><span class="sxs-lookup"><span data-stu-id="20bd3-149">The type of the media item (audio or video).</span></span>                                                                            |
| <span data-ttu-id="20bd3-150">Metadatasource</span><span class="sxs-lookup"><span data-stu-id="20bd3-150">MetadataSource</span></span>    | <span data-ttu-id="20bd3-151">Origine dei metadati per questa traccia CD (AMG, WindowsMedia.com e così via).</span><span class="sxs-lookup"><span data-stu-id="20bd3-151">The source of the metadata for this CD track (AMG, WindowsMedia.com, and so on).</span></span> <span data-ttu-id="20bd3-152">Utilizzato solo con gli elementi multimediali CD.</span><span class="sxs-lookup"><span data-stu-id="20bd3-152">Used only with CD media items.</span></span>         |
| <span data-ttu-id="20bd3-153">ModifiedBy</span><span class="sxs-lookup"><span data-stu-id="20bd3-153">ModifiedBy</span></span>        | <span data-ttu-id="20bd3-154">Riservato per utilizzi futuri.</span><span class="sxs-lookup"><span data-stu-id="20bd3-154">Reserved for future use.</span></span>                                                                                                |
| <span data-ttu-id="20bd3-155">Nome</span><span class="sxs-lookup"><span data-stu-id="20bd3-155">Name</span></span>              | <span data-ttu-id="20bd3-156">Nome della playlist.</span><span class="sxs-lookup"><span data-stu-id="20bd3-156">The name of the playlist.</span></span>                                                                                               |
| <span data-ttu-id="20bd3-157">OriginalIndex</span><span class="sxs-lookup"><span data-stu-id="20bd3-157">OriginalIndex</span></span>     | <span data-ttu-id="20bd3-158">Se applicabile, l'identificatore di traccia CD corrispondente.</span><span class="sxs-lookup"><span data-stu-id="20bd3-158">If applicable, the corresponding CD track identifier.</span></span> <span data-ttu-id="20bd3-159">Utilizzato solo con gli elementi multimediali CD.</span><span class="sxs-lookup"><span data-stu-id="20bd3-159">Used only with CD media items.</span></span>                                    |
| <span data-ttu-id="20bd3-160">PlayCount</span><span class="sxs-lookup"><span data-stu-id="20bd3-160">PlayCount</span></span>         | <span data-ttu-id="20bd3-161">Il numero di volte in cui il contenuto è stato riprodotto fino alla fine.</span><span class="sxs-lookup"><span data-stu-id="20bd3-161">The number of times the content has been played through to the end.</span></span> <span data-ttu-id="20bd3-162">Utilizzato solo con gli elementi multimediali della libreria.</span><span class="sxs-lookup"><span data-stu-id="20bd3-162">Used only with media items from the library.</span></span>        |
| <span data-ttu-id="20bd3-163">PlaylistAttribute</span><span class="sxs-lookup"><span data-stu-id="20bd3-163">PlaylistAttribute</span></span> | <span data-ttu-id="20bd3-164">Riservato per utilizzi futuri.</span><span class="sxs-lookup"><span data-stu-id="20bd3-164">Reserved for future use.</span></span>                                                                                                |
| <span data-ttu-id="20bd3-165">Classificazione</span><span class="sxs-lookup"><span data-stu-id="20bd3-165">Rating</span></span>            | <span data-ttu-id="20bd3-166">Riservato per utilizzi futuri.</span><span class="sxs-lookup"><span data-stu-id="20bd3-166">Reserved for future use.</span></span>                                                                                                |
| <span data-ttu-id="20bd3-167">SourceURL</span><span class="sxs-lookup"><span data-stu-id="20bd3-167">SourceURL</span></span>         | <span data-ttu-id="20bd3-168">Percorso o URL del contenuto.</span><span class="sxs-lookup"><span data-stu-id="20bd3-168">The path or URL to the content.</span></span> <span data-ttu-id="20bd3-169">Utilizzato solo con gli elementi multimediali della libreria.</span><span class="sxs-lookup"><span data-stu-id="20bd3-169">Used only with media items from the library.</span></span>                                            |
| <span data-ttu-id="20bd3-170">Stato</span><span class="sxs-lookup"><span data-stu-id="20bd3-170">Status</span></span>            | <span data-ttu-id="20bd3-171">Stato di copia di una traccia CD da copiare.</span><span class="sxs-lookup"><span data-stu-id="20bd3-171">The copying status of a CD track being copied.</span></span> <span data-ttu-id="20bd3-172">Utilizzato solo con gli elementi multimediali CD.</span><span class="sxs-lookup"><span data-stu-id="20bd3-172">Used only with CD media items.</span></span>                                           |
| <span data-ttu-id="20bd3-173">Stile</span><span class="sxs-lookup"><span data-stu-id="20bd3-173">Style</span></span>             | <span data-ttu-id="20bd3-174">Riservato per utilizzi futuri.</span><span class="sxs-lookup"><span data-stu-id="20bd3-174">Reserved for future use.</span></span>                                                                                                |
| <span data-ttu-id="20bd3-175">Sommario</span><span class="sxs-lookup"><span data-stu-id="20bd3-175">TOC</span></span>               | <span data-ttu-id="20bd3-176">Se applicabile, l'identificatore della tabella di contenuti CD corrispondente.</span><span class="sxs-lookup"><span data-stu-id="20bd3-176">If applicable, the corresponding CD Table of Contents Identifier.</span></span> <span data-ttu-id="20bd3-177">Non usato con le playlist create dall'utente.</span><span class="sxs-lookup"><span data-stu-id="20bd3-177">Not used with user-created playlists.</span></span>                 |



 

## <a name="remarks"></a><span data-ttu-id="20bd3-178">Commenti</span><span class="sxs-lookup"><span data-stu-id="20bd3-178">Remarks</span></span>

<span data-ttu-id="20bd3-179">Se una delle colonne non esiste nella libreria, viene lasciata vuota.</span><span class="sxs-lookup"><span data-stu-id="20bd3-179">If one of the columns does not exist in the library, it is left blank.</span></span>

<span data-ttu-id="20bd3-180">È possibile specificare un massimo di 31 colonne.</span><span class="sxs-lookup"><span data-stu-id="20bd3-180">A maximum of 31 columns may be specified.</span></span>

<span data-ttu-id="20bd3-181">Se si specifica una colonna duplicata, i dati nella prima colonna verranno allineati a sinistra, ma tutte le altre colonne duplicate verranno allineate a destra.</span><span class="sxs-lookup"><span data-stu-id="20bd3-181">If you specify a duplicate column, the data in the first column will be left-aligned but all other duplicate columns will be right-aligned.</span></span> <span data-ttu-id="20bd3-182">Se, ad esempio, sono presenti due colonne Duration, i dati verranno allineati a sinistra nel primo e allineati a destra nel secondo.</span><span class="sxs-lookup"><span data-stu-id="20bd3-182">For example, if you have two duration columns, the data will be left-aligned in the first and right-aligned in the second.</span></span>

## <a name="requirements"></a><span data-ttu-id="20bd3-183">Requisiti</span><span class="sxs-lookup"><span data-stu-id="20bd3-183">Requirements</span></span>



| <span data-ttu-id="20bd3-184">Requisito</span><span class="sxs-lookup"><span data-stu-id="20bd3-184">Requirement</span></span> | <span data-ttu-id="20bd3-185">Valore</span><span class="sxs-lookup"><span data-stu-id="20bd3-185">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="20bd3-186">Versione</span><span class="sxs-lookup"><span data-stu-id="20bd3-186">Version</span></span><br/> | <span data-ttu-id="20bd3-187">Windows Media Player versione 7,0 o successiva</span><span class="sxs-lookup"><span data-stu-id="20bd3-187">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="20bd3-188">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="20bd3-188">See also</span></span>

<dl> <dt>

[<span data-ttu-id="20bd3-189">**PLAYLIST (elemento)**</span><span class="sxs-lookup"><span data-stu-id="20bd3-189">**PLAYLIST Element**</span></span>](playlist-element.md)
</dt> <dt>

[<span data-ttu-id="20bd3-190">**PLAYLIST. columnsVisible**</span><span class="sxs-lookup"><span data-stu-id="20bd3-190">**PLAYLIST.columnsVisible**</span></span>](playlist-columnsvisible.md)
</dt> </dl>

 

 





