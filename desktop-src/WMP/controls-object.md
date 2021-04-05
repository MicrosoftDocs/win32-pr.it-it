---
title: Oggetto Controls
description: L'oggetto Controls consente di modificare la riproduzione dei supporti usando le proprietà e i metodi seguenti.
ms.assetid: bcc1e768-4fa6-4c82-a12f-52c9bfb4c10c
keywords:
- Controlla le finestre degli oggetti Media Player
topic_type:
- apiref
api_name:
- Controls Object
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 7bac91c522c95c1b45565ca013a000022c73bcc4
ms.sourcegitcommit: 4f5016b1fbfd703dbf769c508db464c2518c0fa5
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/06/2019
ms.locfileid: "103718949"
---
# <a name="controls-object"></a><span data-ttu-id="ee220-104">Oggetto Controls</span><span class="sxs-lookup"><span data-stu-id="ee220-104">Controls Object</span></span>

<span data-ttu-id="ee220-105">L'oggetto **Controls** consente di modificare la riproduzione dei supporti usando le proprietà e i metodi seguenti.</span><span class="sxs-lookup"><span data-stu-id="ee220-105">The **Controls** object provides a way to manipulate the playback of media using the following properties and methods.</span></span>

<span data-ttu-id="ee220-106">L'oggetto **Controls** supporta le proprietà seguenti.</span><span class="sxs-lookup"><span data-stu-id="ee220-106">The **Controls** object supports the following properties.</span></span>



| <span data-ttu-id="ee220-107">Proprietà</span><span class="sxs-lookup"><span data-stu-id="ee220-107">Property</span></span>                                                            | <span data-ttu-id="ee220-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ee220-108">Description</span></span>                                                                                                                                       |
|---------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="ee220-109">audioLanguageCount</span><span class="sxs-lookup"><span data-stu-id="ee220-109">audioLanguageCount</span></span>](controls-audiolanguagecount.md)               | <span data-ttu-id="ee220-110">Recupera il numero di lingue audio supportate.</span><span class="sxs-lookup"><span data-stu-id="ee220-110">Retrieves the number of supported audio languages.</span></span>                                                                                                |
| [<span data-ttu-id="ee220-111">currentAudioLanguage</span><span class="sxs-lookup"><span data-stu-id="ee220-111">currentAudioLanguage</span></span>](controls-currentaudiolanguage.md)           | <span data-ttu-id="ee220-112">Specifica o recupera l'identificatore delle impostazioni locali (LCID) della lingua audio per la riproduzione</span><span class="sxs-lookup"><span data-stu-id="ee220-112">Specifies or retrieves the locale identifier (LCID) of the audio language for playback</span></span>                                                            |
| [<span data-ttu-id="ee220-113">currentAudioLanguageIndex</span><span class="sxs-lookup"><span data-stu-id="ee220-113">currentAudioLanguageIndex</span></span>](controls-currentaudiolanguageindex.md) | <span data-ttu-id="ee220-114">Specifica o recupera l'indice in base uno che corrisponde alla lingua audio per la riproduzione.</span><span class="sxs-lookup"><span data-stu-id="ee220-114">Specifies or retrieves the one-based index that corresponds to the audio language for playback.</span></span>                                                   |
| [<span data-ttu-id="ee220-115">currentItem</span><span class="sxs-lookup"><span data-stu-id="ee220-115">currentItem</span></span>](controls-currentitem.md)                             | <span data-ttu-id="ee220-116">Specifica o recupera l'elemento multimediale corrente.</span><span class="sxs-lookup"><span data-stu-id="ee220-116">Specifies or retrieves the current media item.</span></span>                                                                                                    |
| [<span data-ttu-id="ee220-117">currentMarker</span><span class="sxs-lookup"><span data-stu-id="ee220-117">currentMarker</span></span>](controls-currentmarker.md)                         | <span data-ttu-id="ee220-118">Specifica o Recupera il numero di marcatore corrente.</span><span class="sxs-lookup"><span data-stu-id="ee220-118">Specifies or retrieves the current marker number.</span></span>                                                                                                 |
| [<span data-ttu-id="ee220-119">currentPosition</span><span class="sxs-lookup"><span data-stu-id="ee220-119">currentPosition</span></span>](controls-currentposition.md)                     | <span data-ttu-id="ee220-120">Specifica o recupera la posizione corrente nell'elemento multimediale in secondi dall'inizio.</span><span class="sxs-lookup"><span data-stu-id="ee220-120">Specifies or retrieves the current position in the media item in seconds from the beginning.</span></span>                                                      |
| [<span data-ttu-id="ee220-121">currentPositionString</span><span class="sxs-lookup"><span data-stu-id="ee220-121">currentPositionString</span></span>](controls-currentpositionstring.md)         | <span data-ttu-id="ee220-122">Recupera la posizione corrente nell'elemento multimediale sotto forma di **stringa**.</span><span class="sxs-lookup"><span data-stu-id="ee220-122">Retrieves the current position in the media item as a **String**.</span></span>                                                                                 |
| [<span data-ttu-id="ee220-123">currentPositionTimecode</span><span class="sxs-lookup"><span data-stu-id="ee220-123">currentPositionTimecode</span></span>](controls-currentpositiontimecode.md)     | <span data-ttu-id="ee220-124">Specifica o recupera la posizione corrente nell'elemento multimediale corrente usando un formato di codice temporale.</span><span class="sxs-lookup"><span data-stu-id="ee220-124">Specifies or retrieves the current position in the current media item using a time code format.</span></span> <span data-ttu-id="ee220-125">Questa proprietà attualmente supporta il codice ora SMPTE.</span><span class="sxs-lookup"><span data-stu-id="ee220-125">This property currently supports SMPTE time code.</span></span> |
| [<span data-ttu-id="ee220-126">isAvailable</span><span class="sxs-lookup"><span data-stu-id="ee220-126">isAvailable</span></span>](controls-isavailable.md)                             | <span data-ttu-id="ee220-127">Recupera un valore che indica se un tipo specificato di informazioni è disponibile o se è possibile eseguire una determinata azione.</span><span class="sxs-lookup"><span data-stu-id="ee220-127">Retrieves whether a specified type of information is available or a given action can be performed.</span></span>                                                |



 

<span data-ttu-id="ee220-128">L'oggetto **Controls** supporta i metodi seguenti:</span><span class="sxs-lookup"><span data-stu-id="ee220-128">The **Controls** object supports the following methods.</span></span>



| <span data-ttu-id="ee220-129">Metodo</span><span class="sxs-lookup"><span data-stu-id="ee220-129">Method</span></span>                                                                  | <span data-ttu-id="ee220-130">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ee220-130">Description</span></span>                                                                                      |
|-------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="ee220-131">fastForward</span><span class="sxs-lookup"><span data-stu-id="ee220-131">fastForward</span></span>](controls-fastforward.md)                                 | <span data-ttu-id="ee220-132">Avvia la riproduzione veloce dell'elemento multimediale nella direzione in avanti.</span><span class="sxs-lookup"><span data-stu-id="ee220-132">Starts fast play of the media item in the forward direction.</span></span>                                     |
| [<span data-ttu-id="ee220-133">fastReverse</span><span class="sxs-lookup"><span data-stu-id="ee220-133">fastReverse</span></span>](controls-fastreverse.md)                                 | <span data-ttu-id="ee220-134">Avvia la riproduzione veloce dell'elemento multimediale nella direzione inversa.</span><span class="sxs-lookup"><span data-stu-id="ee220-134">Starts fast play of the media item in the reverse direction.</span></span>                                     |
| [<span data-ttu-id="ee220-135">getAudioLanguageDescription</span><span class="sxs-lookup"><span data-stu-id="ee220-135">getAudioLanguageDescription</span></span>](controls-getaudiolanguagedescription.md) | <span data-ttu-id="ee220-136">Recupera la descrizione della lingua audio corrispondente all'indice in base 1 specificato.</span><span class="sxs-lookup"><span data-stu-id="ee220-136">Retrieves the description for the audio language corresponding to the specified one-based index.</span></span> |
| [<span data-ttu-id="ee220-137">getAudioLanguageID</span><span class="sxs-lookup"><span data-stu-id="ee220-137">getAudioLanguageID</span></span>](controls-getaudiolanguageid.md)                   | <span data-ttu-id="ee220-138">Recupera l'LCID per un indice di lingua audio specificato.</span><span class="sxs-lookup"><span data-stu-id="ee220-138">Retrieves the LCID for a specified audio language index.</span></span>                                         |
| [<span data-ttu-id="ee220-139">getLanguageName</span><span class="sxs-lookup"><span data-stu-id="ee220-139">getLanguageName</span></span>](controls-getlanguagename.md)                         | <span data-ttu-id="ee220-140">Recupera il nome della lingua audio con l'LCID specificato.</span><span class="sxs-lookup"><span data-stu-id="ee220-140">Retrieves the name of the audio language with the specified LCID.</span></span>                                |
| [<span data-ttu-id="ee220-141">avanti</span><span class="sxs-lookup"><span data-stu-id="ee220-141">next</span></span>](controls-next.md)                                               | <span data-ttu-id="ee220-142">Imposta l'elemento corrente sull'elemento successivo nella playlist.</span><span class="sxs-lookup"><span data-stu-id="ee220-142">Sets the current item to the next item in the playlist.</span></span>                                          |
| [<span data-ttu-id="ee220-143">pause</span><span class="sxs-lookup"><span data-stu-id="ee220-143">pause</span></span>](controls-pause.md)                                             | <span data-ttu-id="ee220-144">Sospende la riproduzione dell'elemento multimediale.</span><span class="sxs-lookup"><span data-stu-id="ee220-144">Pauses the playing of the media item.</span></span>                                                            |
| [<span data-ttu-id="ee220-145">Play</span><span class="sxs-lookup"><span data-stu-id="ee220-145">play</span></span>](controls-play.md)                                               | <span data-ttu-id="ee220-146">Determina l'avvio della riproduzione dell'elemento multimediale.</span><span class="sxs-lookup"><span data-stu-id="ee220-146">Causes the media item to start playing.</span></span>                                                          |
| [<span data-ttu-id="ee220-147">playItem</span><span class="sxs-lookup"><span data-stu-id="ee220-147">playItem</span></span>](controls-playitem.md)                                       | <span data-ttu-id="ee220-148">Determina la riproduzione dell'elemento multimediale corrente o riprende la riproduzione di un elemento sospeso.</span><span class="sxs-lookup"><span data-stu-id="ee220-148">Causes the current media item to start playing, or resumes play of a paused item.</span></span>                |
| [<span data-ttu-id="ee220-149">previous</span><span class="sxs-lookup"><span data-stu-id="ee220-149">previous</span></span>](controls-previous.md)                                       | <span data-ttu-id="ee220-150">Imposta l'elemento corrente sull'elemento precedente nella playlist.</span><span class="sxs-lookup"><span data-stu-id="ee220-150">Sets the current item to the previous item in the playlist.</span></span>                                      |
| [<span data-ttu-id="ee220-151">passo</span><span class="sxs-lookup"><span data-stu-id="ee220-151">step</span></span>](controls-step.md)                                               | <span data-ttu-id="ee220-152">Fa in modo che l'elemento multimediale del video corrente blocchi la riproduzione nel frame successivo.</span><span class="sxs-lookup"><span data-stu-id="ee220-152">Causes the current video media item to freeze playback on the next frame.</span></span>                        |
| [<span data-ttu-id="ee220-153">stop</span><span class="sxs-lookup"><span data-stu-id="ee220-153">stop</span></span>](controls-stop.md)                                               | <span data-ttu-id="ee220-154">Interrompe la riproduzione dell'elemento multimediale.</span><span class="sxs-lookup"><span data-stu-id="ee220-154">Stops the playing of the media item.</span></span>                                                             |



 

<span data-ttu-id="ee220-155">L'accesso all'oggetto **Controls** viene effettuato tramite la proprietà seguente.</span><span class="sxs-lookup"><span data-stu-id="ee220-155">The **Controls** object is accessed through the following property.</span></span>



| <span data-ttu-id="ee220-156">Oggetto</span><span class="sxs-lookup"><span data-stu-id="ee220-156">Object</span></span>                      | <span data-ttu-id="ee220-157">Proprietà</span><span class="sxs-lookup"><span data-stu-id="ee220-157">Property</span></span>                        |
|-----------------------------|---------------------------------|
| [<span data-ttu-id="ee220-158">Player</span><span class="sxs-lookup"><span data-stu-id="ee220-158">Player</span></span>](player-object.md) | [<span data-ttu-id="ee220-159">controlli</span><span class="sxs-lookup"><span data-stu-id="ee220-159">controls</span></span>](player-controls.md) |



 

## <a name="see-also"></a><span data-ttu-id="ee220-160">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="ee220-160">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ee220-161">**Riferimento del modello a oggetti per lo scripting**</span><span class="sxs-lookup"><span data-stu-id="ee220-161">**Object Model Reference for Scripting**</span></span>](object-model-reference-for-scripting.md)
</dt> </dl>

 

 




