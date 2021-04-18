---
title: Player. openState
description: La proprietà openState recupera un valore che indica lo stato dell'origine del contenuto.
ms.assetid: d38eadad-d0f0-40a9-92c6-1c745a0d4f1b
keywords:
- Player. openState Windows Media Player
topic_type:
- apiref
api_name:
- Player.openState
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b87ad682a0c9ea6420ec291cbe66a7f81c9062e4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324530"
---
# <a name="playeropenstate"></a><span data-ttu-id="ac374-104">Player. openState</span><span class="sxs-lookup"><span data-stu-id="ac374-104">Player.openState</span></span>

<span data-ttu-id="ac374-105">La proprietà **openState** recupera un valore che indica lo stato dell'origine del contenuto.</span><span class="sxs-lookup"><span data-stu-id="ac374-105">The **openState** property retrieves a value indicating the state of the content source.</span></span>

## <a name="syntax"></a><span data-ttu-id="ac374-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="ac374-106">Syntax</span></span>

<span data-ttu-id="ac374-107">*Player* . **openState**</span><span class="sxs-lookup"><span data-stu-id="ac374-107">*player* .**openState**</span></span>

## <a name="possible-values"></a><span data-ttu-id="ac374-108">Valori possibili</span><span class="sxs-lookup"><span data-stu-id="ac374-108">Possible Values</span></span>

<span data-ttu-id="ac374-109">Questa proprietà è un **numero** di sola lettura (**Long**).</span><span class="sxs-lookup"><span data-stu-id="ac374-109">This property is a read only **Number** (**long**).</span></span> <span data-ttu-id="ac374-110">La costante di enumerazione di tipo C può essere derivata anteponendo il valore di stato con "wmpos".</span><span class="sxs-lookup"><span data-stu-id="ac374-110">The C-style enumeration constant can be derived by prefixing the state value with "wmpos".</span></span> <span data-ttu-id="ac374-111">Ad esempio, la costante per lo stato PlaylistOpening è **wmposPlaylistOpening**.</span><span class="sxs-lookup"><span data-stu-id="ac374-111">For example, the constant for the PlaylistOpening state is **wmposPlaylistOpening**.</span></span>



| <span data-ttu-id="ac374-112">Valore</span><span class="sxs-lookup"><span data-stu-id="ac374-112">Value</span></span> | <span data-ttu-id="ac374-113">State</span><span class="sxs-lookup"><span data-stu-id="ac374-113">State</span></span>                   | <span data-ttu-id="ac374-114">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ac374-114">Description</span></span>                                                                                                                                            |
|-------|-------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ac374-115">0</span><span class="sxs-lookup"><span data-stu-id="ac374-115">0</span></span>     | <span data-ttu-id="ac374-116">Non definito</span><span class="sxs-lookup"><span data-stu-id="ac374-116">Undefined</span></span>               | <span data-ttu-id="ac374-117">Windows Media Player è in uno stato non definito.</span><span class="sxs-lookup"><span data-stu-id="ac374-117">Windows Media Player is in an undefined state.</span></span>                                                                                                         |
| <span data-ttu-id="ac374-118">1</span><span class="sxs-lookup"><span data-stu-id="ac374-118">1</span></span>     | <span data-ttu-id="ac374-119">PlaylistChanging</span><span class="sxs-lookup"><span data-stu-id="ac374-119">PlaylistChanging</span></span>        | <span data-ttu-id="ac374-120">La nuova playlist sta per essere caricata.</span><span class="sxs-lookup"><span data-stu-id="ac374-120">New playlist is about to be loaded.</span></span>                                                                                                                    |
| <span data-ttu-id="ac374-121">2</span><span class="sxs-lookup"><span data-stu-id="ac374-121">2</span></span>     | <span data-ttu-id="ac374-122">PlaylistLocating</span><span class="sxs-lookup"><span data-stu-id="ac374-122">PlaylistLocating</span></span>        | <span data-ttu-id="ac374-123">Windows Media Player sta tentando di individuare la playlist.</span><span class="sxs-lookup"><span data-stu-id="ac374-123">Windows Media Player is attempting to locate the playlist.</span></span> <span data-ttu-id="ac374-124">La playlist può essere locale (libreria o metafile con estensione del nome di file ASX) o remota.</span><span class="sxs-lookup"><span data-stu-id="ac374-124">The playlist can be local (library or metafile with an .asx file name extension) or remote.</span></span> |
| <span data-ttu-id="ac374-125">3</span><span class="sxs-lookup"><span data-stu-id="ac374-125">3</span></span>     | <span data-ttu-id="ac374-126">PlaylistConnecting</span><span class="sxs-lookup"><span data-stu-id="ac374-126">PlaylistConnecting</span></span>      | <span data-ttu-id="ac374-127">Connessione alla playlist.</span><span class="sxs-lookup"><span data-stu-id="ac374-127">Connecting to the playlist.</span></span>                                                                                                                            |
| <span data-ttu-id="ac374-128">4</span><span class="sxs-lookup"><span data-stu-id="ac374-128">4</span></span>     | <span data-ttu-id="ac374-129">PlaylistLoading</span><span class="sxs-lookup"><span data-stu-id="ac374-129">PlaylistLoading</span></span>         | <span data-ttu-id="ac374-130">La playlist è stata trovata e ora è in fase di recupero.</span><span class="sxs-lookup"><span data-stu-id="ac374-130">Playlist has been found and is now being retrieved.</span></span>                                                                                                    |
| <span data-ttu-id="ac374-131">5</span><span class="sxs-lookup"><span data-stu-id="ac374-131">5</span></span>     | <span data-ttu-id="ac374-132">PlaylistOpening</span><span class="sxs-lookup"><span data-stu-id="ac374-132">PlaylistOpening</span></span>         | <span data-ttu-id="ac374-133">La playlist è stata recuperata e viene ora analizzata e caricata.</span><span class="sxs-lookup"><span data-stu-id="ac374-133">Playlist has been retrieved and is now being parsed and loaded.</span></span>                                                                                        |
| <span data-ttu-id="ac374-134">6</span><span class="sxs-lookup"><span data-stu-id="ac374-134">6</span></span>     | <span data-ttu-id="ac374-135">PlaylistOpenNoMedia</span><span class="sxs-lookup"><span data-stu-id="ac374-135">PlaylistOpenNoMedia</span></span>     | <span data-ttu-id="ac374-136">La playlist è aperta.</span><span class="sxs-lookup"><span data-stu-id="ac374-136">Playlist is open.</span></span>                                                                                                                                      |
| <span data-ttu-id="ac374-137">7</span><span class="sxs-lookup"><span data-stu-id="ac374-137">7</span></span>     | <span data-ttu-id="ac374-138">PlaylistChanged</span><span class="sxs-lookup"><span data-stu-id="ac374-138">PlaylistChanged</span></span>         | <span data-ttu-id="ac374-139">Una nuova playlist è stata assegnata a **currentPlaylist**.</span><span class="sxs-lookup"><span data-stu-id="ac374-139">A new playlist has been assigned to **currentPlaylist**.</span></span>                                                                                               |
| <span data-ttu-id="ac374-140">8</span><span class="sxs-lookup"><span data-stu-id="ac374-140">8</span></span>     | <span data-ttu-id="ac374-141">MediaChanging</span><span class="sxs-lookup"><span data-stu-id="ac374-141">MediaChanging</span></span>           | <span data-ttu-id="ac374-142">Un nuovo elemento multimediale sta per essere caricato.</span><span class="sxs-lookup"><span data-stu-id="ac374-142">A new media item is about to be loaded.</span></span>                                                                                                                |
| <span data-ttu-id="ac374-143">9</span><span class="sxs-lookup"><span data-stu-id="ac374-143">9</span></span>     | <span data-ttu-id="ac374-144">MediaLocating</span><span class="sxs-lookup"><span data-stu-id="ac374-144">MediaLocating</span></span>           | <span data-ttu-id="ac374-145">Windows Media Player individua l'elemento multimediale.</span><span class="sxs-lookup"><span data-stu-id="ac374-145">Windows Media Player is locating the media item.</span></span> <span data-ttu-id="ac374-146">Il file può essere locale o remoto.</span><span class="sxs-lookup"><span data-stu-id="ac374-146">The file can be local or remote.</span></span>                                                                      |
| <span data-ttu-id="ac374-147">10</span><span class="sxs-lookup"><span data-stu-id="ac374-147">10</span></span>    | <span data-ttu-id="ac374-148">MediaConnecting</span><span class="sxs-lookup"><span data-stu-id="ac374-148">MediaConnecting</span></span>         | <span data-ttu-id="ac374-149">Connessione al server che include l'elemento multimediale.</span><span class="sxs-lookup"><span data-stu-id="ac374-149">Connecting to the server that holds the media item.</span></span>                                                                                                    |
| <span data-ttu-id="ac374-150">11</span><span class="sxs-lookup"><span data-stu-id="ac374-150">11</span></span>    | <span data-ttu-id="ac374-151">MediaLoading</span><span class="sxs-lookup"><span data-stu-id="ac374-151">MediaLoading</span></span>            | <span data-ttu-id="ac374-152">L'elemento multimediale è stato individuato e ora viene recuperato.</span><span class="sxs-lookup"><span data-stu-id="ac374-152">Media item has been located and is now being retrieved.</span></span>                                                                                                |
| <span data-ttu-id="ac374-153">12</span><span class="sxs-lookup"><span data-stu-id="ac374-153">12</span></span>    | <span data-ttu-id="ac374-154">MediaOpening</span><span class="sxs-lookup"><span data-stu-id="ac374-154">MediaOpening</span></span>            | <span data-ttu-id="ac374-155">L'elemento multimediale è stato recuperato e ora è in fase di apertura.</span><span class="sxs-lookup"><span data-stu-id="ac374-155">Media item has been retrieved and is now being opened.</span></span>                                                                                                 |
| <span data-ttu-id="ac374-156">13</span><span class="sxs-lookup"><span data-stu-id="ac374-156">13</span></span>    | <span data-ttu-id="ac374-157">MediaOpen</span><span class="sxs-lookup"><span data-stu-id="ac374-157">MediaOpen</span></span>               | <span data-ttu-id="ac374-158">L'elemento multimediale è ora aperto.</span><span class="sxs-lookup"><span data-stu-id="ac374-158">Media item is now open.</span></span>                                                                                                                                |
| <span data-ttu-id="ac374-159">14</span><span class="sxs-lookup"><span data-stu-id="ac374-159">14</span></span>    | <span data-ttu-id="ac374-160">BeginCodecAcquisition</span><span class="sxs-lookup"><span data-stu-id="ac374-160">BeginCodecAcquisition</span></span>   | <span data-ttu-id="ac374-161">Avvio dell'acquisizione del codec.</span><span class="sxs-lookup"><span data-stu-id="ac374-161">Starting codec acquisition.</span></span>                                                                                                                            |
| <span data-ttu-id="ac374-162">15</span><span class="sxs-lookup"><span data-stu-id="ac374-162">15</span></span>    | <span data-ttu-id="ac374-163">EndCodecAcquisition</span><span class="sxs-lookup"><span data-stu-id="ac374-163">EndCodecAcquisition</span></span>     | <span data-ttu-id="ac374-164">L'acquisizione del codec è stata completata.</span><span class="sxs-lookup"><span data-stu-id="ac374-164">Codec acquisition is complete.</span></span>                                                                                                                         |
| <span data-ttu-id="ac374-165">16</span><span class="sxs-lookup"><span data-stu-id="ac374-165">16</span></span>    | <span data-ttu-id="ac374-166">BeginLicenseAcquisition</span><span class="sxs-lookup"><span data-stu-id="ac374-166">BeginLicenseAcquisition</span></span> | <span data-ttu-id="ac374-167">Acquisizione di una licenza per riprodurre contenuti protetti da DRM.</span><span class="sxs-lookup"><span data-stu-id="ac374-167">Acquiring a license to play DRM protected content.</span></span>                                                                                                     |
| <span data-ttu-id="ac374-168">17</span><span class="sxs-lookup"><span data-stu-id="ac374-168">17</span></span>    | <span data-ttu-id="ac374-169">EndLicenseAcquisition</span><span class="sxs-lookup"><span data-stu-id="ac374-169">EndLicenseAcquisition</span></span>   | <span data-ttu-id="ac374-170">È stata acquisita la licenza per la riproduzione di contenuti protetti da DRM.</span><span class="sxs-lookup"><span data-stu-id="ac374-170">License to play DRM protected content has been acquired.</span></span>                                                                                               |
| <span data-ttu-id="ac374-171">18</span><span class="sxs-lookup"><span data-stu-id="ac374-171">18</span></span>    | <span data-ttu-id="ac374-172">BeginIndividualization</span><span class="sxs-lookup"><span data-stu-id="ac374-172">BeginIndividualization</span></span>  | <span data-ttu-id="ac374-173">Inizia l'individualizzazione DRM.</span><span class="sxs-lookup"><span data-stu-id="ac374-173">Begin DRM Individualization.</span></span>                                                                                                                           |
| <span data-ttu-id="ac374-174">19</span><span class="sxs-lookup"><span data-stu-id="ac374-174">19</span></span>    | <span data-ttu-id="ac374-175">EndIndividualization</span><span class="sxs-lookup"><span data-stu-id="ac374-175">EndIndividualization</span></span>    | <span data-ttu-id="ac374-176">L'individualizzazione DRM è stata completata.</span><span class="sxs-lookup"><span data-stu-id="ac374-176">DRM individualization has been completed.</span></span>                                                                                                              |
| <span data-ttu-id="ac374-177">20</span><span class="sxs-lookup"><span data-stu-id="ac374-177">20</span></span>    | <span data-ttu-id="ac374-178">MediaWaiting</span><span class="sxs-lookup"><span data-stu-id="ac374-178">MediaWaiting</span></span>            | <span data-ttu-id="ac374-179">In attesa dell'elemento multimediale.</span><span class="sxs-lookup"><span data-stu-id="ac374-179">Waiting for media item.</span></span>                                                                                                                                |
| <span data-ttu-id="ac374-180">21</span><span class="sxs-lookup"><span data-stu-id="ac374-180">21</span></span>    | <span data-ttu-id="ac374-181">OpeningUnknownURL</span><span class="sxs-lookup"><span data-stu-id="ac374-181">OpeningUnknownURL</span></span>       | <span data-ttu-id="ac374-182">Apertura di un URL con un tipo sconosciuto.</span><span class="sxs-lookup"><span data-stu-id="ac374-182">Opening a URL with an unknown type.</span></span>                                                                                                                    |



 

## <a name="remarks"></a><span data-ttu-id="ac374-183">Commenti</span><span class="sxs-lookup"><span data-stu-id="ac374-183">Remarks</span></span>

<span data-ttu-id="ac374-184">Non è garantito che gli Stati di Windows Media Player vengano eseguiti in un ordine particolare.</span><span class="sxs-lookup"><span data-stu-id="ac374-184">Windows Media Player states are not guaranteed to occur in any particular order.</span></span> <span data-ttu-id="ac374-185">Inoltre, non tutti gli Stati si verificano necessariamente durante una sequenza di eventi.</span><span class="sxs-lookup"><span data-stu-id="ac374-185">Furthermore, not every state necessarily occurs during a sequence of events.</span></span> <span data-ttu-id="ac374-186">Non è necessario scrivere codice che si basa sull'ordine di stato.</span><span class="sxs-lookup"><span data-stu-id="ac374-186">You should not write code that relies upon state order.</span></span>

## <a name="requirements"></a><span data-ttu-id="ac374-187">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ac374-187">Requirements</span></span>



| <span data-ttu-id="ac374-188">Requisito</span><span class="sxs-lookup"><span data-stu-id="ac374-188">Requirement</span></span> | <span data-ttu-id="ac374-189">Valore</span><span class="sxs-lookup"><span data-stu-id="ac374-189">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="ac374-190">Versione</span><span class="sxs-lookup"><span data-stu-id="ac374-190">Version</span></span><br/> | <span data-ttu-id="ac374-191">Windows Media Player versione 7,0 o successiva.</span><span class="sxs-lookup"><span data-stu-id="ac374-191">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="ac374-192">DLL</span><span class="sxs-lookup"><span data-stu-id="ac374-192">DLL</span></span><br/>     | <dl> <span data-ttu-id="ac374-193"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ac374-193"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ac374-194">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="ac374-194">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ac374-195">**Oggetto Player**</span><span class="sxs-lookup"><span data-stu-id="ac374-195">**Player Object**</span></span>](player-object.md)
</dt> <dt>

[<span data-ttu-id="ac374-196">**Evento Player. OpenStateChange**</span><span class="sxs-lookup"><span data-stu-id="ac374-196">**Player.OpenStateChange Event**</span></span>](player-player-openstatechange.md)
</dt> </dl>

 

 





