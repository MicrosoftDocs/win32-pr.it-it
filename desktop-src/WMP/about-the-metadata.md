---
title: Informazioni sui metadati
description: Informazioni sui metadati
ms.assetid: bdb35606-7861-4f97-aae5-4f7f3ed48106
keywords:
- Media Player di Windows, metadati
- metadati, informazioni
- metadati, attributi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3a1c2e9782b52adc274a5b3dbaf16c48ed1a892e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104328519"
---
# <a name="about-the-metadata"></a><span data-ttu-id="0def8-106">Informazioni sui metadati</span><span class="sxs-lookup"><span data-stu-id="0def8-106">About the Metadata</span></span>

<span data-ttu-id="0def8-107">Windows Media Player 10 o versioni successive tenta di sincronizzare i seguenti attributi di metadati.</span><span class="sxs-lookup"><span data-stu-id="0def8-107">Windows Media Player 10 or later attempts to synchronize the following metadata attributes.</span></span>



| <span data-ttu-id="0def8-108">Attributo Player</span><span class="sxs-lookup"><span data-stu-id="0def8-108">Player attribute</span></span> | <span data-ttu-id="0def8-109">Costante globale WMDM</span><span class="sxs-lookup"><span data-stu-id="0def8-109">WMDM global constant</span></span>  | <span data-ttu-id="0def8-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="0def8-110">Description</span></span>                                                                                                 | <span data-ttu-id="0def8-111">Versione necessaria</span><span class="sxs-lookup"><span data-stu-id="0def8-111">Required version</span></span>                  |
|------------------|-----------------------|-------------------------------------------------------------------------------------------------------------|-----------------------------------|
| <span data-ttu-id="0def8-112">AlbumArtist</span><span class="sxs-lookup"><span data-stu-id="0def8-112">AlbumArtist</span></span>      | <span data-ttu-id="0def8-113">g \_ wszWMDMAlbumArtist</span><span class="sxs-lookup"><span data-stu-id="0def8-113">g\_wszWMDMAlbumArtist</span></span> | <span data-ttu-id="0def8-114">**Stringa** con terminazione null che contiene il nome dell'artista principale per l'album.</span><span class="sxs-lookup"><span data-stu-id="0def8-114">Null-terminated **string** containing the name of the primary artist for the album.</span></span>                         | <span data-ttu-id="0def8-115">Windows Media Player 11 o versione successiva.</span><span class="sxs-lookup"><span data-stu-id="0def8-115">Windows Media Player 11 or later.</span></span> |
| <span data-ttu-id="0def8-116">Album</span><span class="sxs-lookup"><span data-stu-id="0def8-116">Album</span></span>            | <span data-ttu-id="0def8-117">g \_ wszWMDMAlbumTitle</span><span class="sxs-lookup"><span data-stu-id="0def8-117">g\_wszWMDMAlbumTitle</span></span>  | <span data-ttu-id="0def8-118">**Stringa** con terminazione null contenente il titolo dell'album in cui è stato rilasciato originariamente il contenuto.</span><span class="sxs-lookup"><span data-stu-id="0def8-118">Null-terminated **string** containing the title of the album on which the content was originally released.</span></span>  | <span data-ttu-id="0def8-119">Windows Media Player 11 o versione successiva.</span><span class="sxs-lookup"><span data-stu-id="0def8-119">Windows Media Player 11 or later.</span></span> |
| <span data-ttu-id="0def8-120">Autore</span><span class="sxs-lookup"><span data-stu-id="0def8-120">Author</span></span>           | <span data-ttu-id="0def8-121">g \_ wszWMDMAuthor</span><span class="sxs-lookup"><span data-stu-id="0def8-121">g\_wszWMDMAuthor</span></span>      | <span data-ttu-id="0def8-122">**Stringa** con terminazione null che contiene il nome dell'autore o dell'attore multimediale associato al contenuto.</span><span class="sxs-lookup"><span data-stu-id="0def8-122">Null-terminated **string** containing the name of the media artist or actor associated with the content.</span></span>    | <span data-ttu-id="0def8-123">Windows Media Player 11 o versione successiva.</span><span class="sxs-lookup"><span data-stu-id="0def8-123">Windows Media Player 11 or later.</span></span> |
| <span data-ttu-id="0def8-124">CompraOra</span><span class="sxs-lookup"><span data-stu-id="0def8-124">BuyNow</span></span>           | <span data-ttu-id="0def8-125">g \_ wszWMDMBuyNow</span><span class="sxs-lookup"><span data-stu-id="0def8-125">g\_wszWMDMBuyNow</span></span>      | <span data-ttu-id="0def8-126">**Valore booleano** che indica se l'utente ha scelto di acquistare il contenuto.</span><span class="sxs-lookup"><span data-stu-id="0def8-126">**Boolean** indicating whether the user has chosen to purchase the content.</span></span>                                 | <span data-ttu-id="0def8-127">Windows Media Player 10 o versione successiva.</span><span class="sxs-lookup"><span data-stu-id="0def8-127">Windows Media Player 10 or later.</span></span> |
| <span data-ttu-id="0def8-128">WM/genre</span><span class="sxs-lookup"><span data-stu-id="0def8-128">WM/Genre</span></span>         | <span data-ttu-id="0def8-129">g \_ wszWMDMGenre</span><span class="sxs-lookup"><span data-stu-id="0def8-129">g\_wszWMDMGenre</span></span>       | <span data-ttu-id="0def8-130">**Stringa** con terminazione null contenente il genere del contenuto.</span><span class="sxs-lookup"><span data-stu-id="0def8-130">Null-terminated **string** containing the genre of the content.</span></span>                                             | <span data-ttu-id="0def8-131">Windows Media Player 11 o versione successiva.</span><span class="sxs-lookup"><span data-stu-id="0def8-131">Windows Media Player 11 or later.</span></span> |
| <span data-ttu-id="0def8-132">UserPlayCount</span><span class="sxs-lookup"><span data-stu-id="0def8-132">UserPlayCount</span></span>    | <span data-ttu-id="0def8-133">g \_ wszWMDMPlayCount</span><span class="sxs-lookup"><span data-stu-id="0def8-133">g\_wszWMDMPlayCount</span></span>   | <span data-ttu-id="0def8-134">**DWORD** contenente il numero di volte in cui l'utente ha eseguito il file multimediale digitale.</span><span class="sxs-lookup"><span data-stu-id="0def8-134">**DWORD** containing the number of times the user has played the digital media file.</span></span>                        | <span data-ttu-id="0def8-135">Windows Media Player 10 o versione successiva.</span><span class="sxs-lookup"><span data-stu-id="0def8-135">Windows Media Player 10 or later.</span></span> |
| <span data-ttu-id="0def8-136">ReleaseDate</span><span class="sxs-lookup"><span data-stu-id="0def8-136">ReleaseDate</span></span>      | <span data-ttu-id="0def8-137">g \_ wszWMDMYear</span><span class="sxs-lookup"><span data-stu-id="0def8-137">g\_wszWMDMYear</span></span>        | <span data-ttu-id="0def8-138">Data della versione originale dell'elemento.</span><span class="sxs-lookup"><span data-stu-id="0def8-138">The date of the original release of the item.</span></span>                                                               | <span data-ttu-id="0def8-139">Windows Media Player 11 o versione successiva.</span><span class="sxs-lookup"><span data-stu-id="0def8-139">Windows Media Player 11 or later.</span></span> |
| <span data-ttu-id="0def8-140">Titolo</span><span class="sxs-lookup"><span data-stu-id="0def8-140">Title</span></span>            | <span data-ttu-id="0def8-141">g \_ wszWMDMTitle</span><span class="sxs-lookup"><span data-stu-id="0def8-141">g\_wszWMDMTitle</span></span>       | <span data-ttu-id="0def8-142">**Stringa** con terminazione null che contiene il titolo.</span><span class="sxs-lookup"><span data-stu-id="0def8-142">Null-terminated **string** containing the title.</span></span>                                                            | <span data-ttu-id="0def8-143">Windows Media Player 11 o versione successiva.</span><span class="sxs-lookup"><span data-stu-id="0def8-143">Windows Media Player 11 or later.</span></span> |
| <span data-ttu-id="0def8-144">WM/numero</span><span class="sxs-lookup"><span data-stu-id="0def8-144">WM/TrackNumber</span></span>   | <span data-ttu-id="0def8-145">g \_ wszWMDMTrack</span><span class="sxs-lookup"><span data-stu-id="0def8-145">g\_wszWMDMTrack</span></span>       | <span data-ttu-id="0def8-146">**DWORD** contenente il numero di traccia dell'elemento sull'album in cui è stato rilasciato originariamente.</span><span class="sxs-lookup"><span data-stu-id="0def8-146">**DWORD** containing the track number of the item on the album on which it was originally released.</span></span>         | <span data-ttu-id="0def8-147">Windows Media Player 11 o versione successiva.</span><span class="sxs-lookup"><span data-stu-id="0def8-147">Windows Media Player 11 or later.</span></span> |
| <span data-ttu-id="0def8-148">UserRating</span><span class="sxs-lookup"><span data-stu-id="0def8-148">UserRating</span></span>       | <span data-ttu-id="0def8-149">g \_ wszWMDMUserRating</span><span class="sxs-lookup"><span data-stu-id="0def8-149">g\_wszWMDMUserRating</span></span>  | <span data-ttu-id="0def8-150">**DWORD** contenente un valore che rappresenta la classificazione a stelle specificata dall'utente per il file multimediale digitale.</span><span class="sxs-lookup"><span data-stu-id="0def8-150">**DWORD** containing a value that represents the star rating the user specified for the digital media file.</span></span> | <span data-ttu-id="0def8-151">Windows Media Player 10 o versione successiva.</span><span class="sxs-lookup"><span data-stu-id="0def8-151">Windows Media Player 10 or later.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="0def8-152">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="0def8-152">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0def8-153">**Estensioni del dispositivo per il trasferimento di metadati accelerati**</span><span class="sxs-lookup"><span data-stu-id="0def8-153">**Device Extensions for Accelerated Metadata Transfer**</span></span>](device-extensions-for-accelerated-metadata-transfer.md)
</dt> </dl>

 

 




