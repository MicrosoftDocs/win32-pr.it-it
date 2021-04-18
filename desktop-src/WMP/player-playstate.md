---
title: Player. riproduzione
description: La proprietà riproduzione recupera un valore che indica lo stato dell'operazione Windows Media Player.
ms.assetid: 8ed1ee1f-8731-402a-aff5-5ae513a35eea
keywords:
- Player. riproduzione Windows Media Player
topic_type:
- apiref
api_name:
- Player.playState
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7c442b1be9e1ea15b8a54c2dafc264edf8aeb479
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327704"
---
# <a name="playerplaystate"></a><span data-ttu-id="af73f-104">Player. riproduzione</span><span class="sxs-lookup"><span data-stu-id="af73f-104">Player.playState</span></span>

<span data-ttu-id="af73f-105">La proprietà **riproduzione** recupera un valore che indica lo stato dell'operazione Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="af73f-105">The **playState** property retrieves a value indicating the state of the Windows Media Player operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="af73f-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="af73f-106">Syntax</span></span>

<span data-ttu-id="af73f-107">*Player* . **riproduzione**</span><span class="sxs-lookup"><span data-stu-id="af73f-107">*player* .**playState**</span></span>

## <a name="possible-values"></a><span data-ttu-id="af73f-108">Valori possibili</span><span class="sxs-lookup"><span data-stu-id="af73f-108">Possible Values</span></span>

<span data-ttu-id="af73f-109">Questa proprietà è un **numero** di sola lettura (**Long**).</span><span class="sxs-lookup"><span data-stu-id="af73f-109">This property is a read-only **Number** (**long**).</span></span> <span data-ttu-id="af73f-110">La costante di enumerazione di tipo C può essere derivata anteponendo il valore di stato con "wmpps".</span><span class="sxs-lookup"><span data-stu-id="af73f-110">The C-style enumeration constant can be derived by prefixing the state value with "wmpps".</span></span> <span data-ttu-id="af73f-111">La costante per lo stato di riproduzione, ad esempio, è **wmppsPlaying**.</span><span class="sxs-lookup"><span data-stu-id="af73f-111">For example, the constant for the Playing state is **wmppsPlaying**.</span></span>



| <span data-ttu-id="af73f-112">Valore</span><span class="sxs-lookup"><span data-stu-id="af73f-112">Value</span></span> | <span data-ttu-id="af73f-113">State</span><span class="sxs-lookup"><span data-stu-id="af73f-113">State</span></span>         | <span data-ttu-id="af73f-114">Descrizione</span><span class="sxs-lookup"><span data-stu-id="af73f-114">Description</span></span>                                                                                                                 |
|-------|---------------|-----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="af73f-115">0</span><span class="sxs-lookup"><span data-stu-id="af73f-115">0</span></span>     | <span data-ttu-id="af73f-116">Non definito</span><span class="sxs-lookup"><span data-stu-id="af73f-116">Undefined</span></span>     | <span data-ttu-id="af73f-117">Windows Media Player è in uno stato non definito.</span><span class="sxs-lookup"><span data-stu-id="af73f-117">Windows Media Player is in an undefined state.</span></span>                                                                              |
| <span data-ttu-id="af73f-118">1</span><span class="sxs-lookup"><span data-stu-id="af73f-118">1</span></span>     | <span data-ttu-id="af73f-119">Arrestato</span><span class="sxs-lookup"><span data-stu-id="af73f-119">Stopped</span></span>       | <span data-ttu-id="af73f-120">La riproduzione dell'elemento multimediale corrente è stata arrestata.</span><span class="sxs-lookup"><span data-stu-id="af73f-120">Playback of the current media item is stopped.</span></span>                                                                              |
| <span data-ttu-id="af73f-121">2</span><span class="sxs-lookup"><span data-stu-id="af73f-121">2</span></span>     | <span data-ttu-id="af73f-122">Paused</span><span class="sxs-lookup"><span data-stu-id="af73f-122">Paused</span></span>        | <span data-ttu-id="af73f-123">La riproduzione dell'elemento multimediale corrente è sospesa.</span><span class="sxs-lookup"><span data-stu-id="af73f-123">Playback of the current media item is paused.</span></span> <span data-ttu-id="af73f-124">Quando un elemento multimediale viene sospeso, la ripresa della riproduzione inizia dalla stessa posizione.</span><span class="sxs-lookup"><span data-stu-id="af73f-124">When a media item is paused, resuming playback begins from the same location.</span></span> |
| <span data-ttu-id="af73f-125">3</span><span class="sxs-lookup"><span data-stu-id="af73f-125">3</span></span>     | <span data-ttu-id="af73f-126">Playing</span><span class="sxs-lookup"><span data-stu-id="af73f-126">Playing</span></span>       | <span data-ttu-id="af73f-127">L'elemento multimediale corrente sta eseguendo la riproduzione.</span><span class="sxs-lookup"><span data-stu-id="af73f-127">The current media item is playing.</span></span>                                                                                          |
| <span data-ttu-id="af73f-128">4</span><span class="sxs-lookup"><span data-stu-id="af73f-128">4</span></span>     | <span data-ttu-id="af73f-129">ScanForward</span><span class="sxs-lookup"><span data-stu-id="af73f-129">ScanForward</span></span>   | <span data-ttu-id="af73f-130">L'elemento multimediale corrente è l'avanzamento rapido.</span><span class="sxs-lookup"><span data-stu-id="af73f-130">The current media item is fast forwarding.</span></span>                                                                                  |
| <span data-ttu-id="af73f-131">5</span><span class="sxs-lookup"><span data-stu-id="af73f-131">5</span></span>     | <span data-ttu-id="af73f-132">ScanReverse</span><span class="sxs-lookup"><span data-stu-id="af73f-132">ScanReverse</span></span>   | <span data-ttu-id="af73f-133">L'elemento multimediale corrente è un riavvolgimento rapido.</span><span class="sxs-lookup"><span data-stu-id="af73f-133">The current media item is fast rewinding.</span></span>                                                                                   |
| <span data-ttu-id="af73f-134">6</span><span class="sxs-lookup"><span data-stu-id="af73f-134">6</span></span>     | <span data-ttu-id="af73f-135">responseBuffering</span><span class="sxs-lookup"><span data-stu-id="af73f-135">Buffering</span></span>     | <span data-ttu-id="af73f-136">L'elemento multimediale corrente sta ottenendo dati aggiuntivi dal server.</span><span class="sxs-lookup"><span data-stu-id="af73f-136">The current media item is getting additional data from the server.</span></span>                                                          |
| <span data-ttu-id="af73f-137">7</span><span class="sxs-lookup"><span data-stu-id="af73f-137">7</span></span>     | <span data-ttu-id="af73f-138">Attesa</span><span class="sxs-lookup"><span data-stu-id="af73f-138">Waiting</span></span>       | <span data-ttu-id="af73f-139">Viene stabilita la connessione, ma il server non invia dati.</span><span class="sxs-lookup"><span data-stu-id="af73f-139">Connection is established, but the server is not sending data.</span></span> <span data-ttu-id="af73f-140">In attesa dell'inizio della sessione.</span><span class="sxs-lookup"><span data-stu-id="af73f-140">Waiting for session to begin.</span></span>                                |
| <span data-ttu-id="af73f-141">8</span><span class="sxs-lookup"><span data-stu-id="af73f-141">8</span></span>     | <span data-ttu-id="af73f-142">MediaEnded</span><span class="sxs-lookup"><span data-stu-id="af73f-142">MediaEnded</span></span>    | <span data-ttu-id="af73f-143">La riproduzione dell'elemento multimediale è stata completata.</span><span class="sxs-lookup"><span data-stu-id="af73f-143">Media item has completed playback.</span></span>                                                                                          |
| <span data-ttu-id="af73f-144">9</span><span class="sxs-lookup"><span data-stu-id="af73f-144">9</span></span>     | <span data-ttu-id="af73f-145">Transizione</span><span class="sxs-lookup"><span data-stu-id="af73f-145">Transitioning</span></span> | <span data-ttu-id="af73f-146">Preparazione di un nuovo elemento multimediale.</span><span class="sxs-lookup"><span data-stu-id="af73f-146">Preparing new media item.</span></span>                                                                                                   |
| <span data-ttu-id="af73f-147">10</span><span class="sxs-lookup"><span data-stu-id="af73f-147">10</span></span>    | <span data-ttu-id="af73f-148">Ready</span><span class="sxs-lookup"><span data-stu-id="af73f-148">Ready</span></span>         | <span data-ttu-id="af73f-149">Pronto per iniziare la riproduzione.</span><span class="sxs-lookup"><span data-stu-id="af73f-149">Ready to begin playing.</span></span>                                                                                                     |
| <span data-ttu-id="af73f-150">11</span><span class="sxs-lookup"><span data-stu-id="af73f-150">11</span></span>    | <span data-ttu-id="af73f-151">Riconnessione</span><span class="sxs-lookup"><span data-stu-id="af73f-151">Reconnecting</span></span>  | <span data-ttu-id="af73f-152">Riconnessione al flusso.</span><span class="sxs-lookup"><span data-stu-id="af73f-152">Reconnecting to stream.</span></span>                                                                                                     |



 

## <a name="remarks"></a><span data-ttu-id="af73f-153">Commenti</span><span class="sxs-lookup"><span data-stu-id="af73f-153">Remarks</span></span>

<span data-ttu-id="af73f-154">Non è garantito che gli Stati di Windows Media Player vengano eseguiti in un ordine particolare.</span><span class="sxs-lookup"><span data-stu-id="af73f-154">Windows Media Player states are not guaranteed to occur in any particular order.</span></span> <span data-ttu-id="af73f-155">Inoltre, non tutti gli Stati si verificano necessariamente durante una sequenza di eventi.</span><span class="sxs-lookup"><span data-stu-id="af73f-155">Furthermore, not every state necessarily occurs during a sequence of events.</span></span> <span data-ttu-id="af73f-156">Non è necessario scrivere codice che si basa sull'ordine di stato.</span><span class="sxs-lookup"><span data-stu-id="af73f-156">You should not write code that relies upon state order.</span></span>

## <a name="examples"></a><span data-ttu-id="af73f-157">Esempio</span><span class="sxs-lookup"><span data-stu-id="af73f-157">Examples</span></span>

<span data-ttu-id="af73f-158">Il codice JScript seguente illustra l'uso del *lettore*. proprietà **riproduzione** .</span><span class="sxs-lookup"><span data-stu-id="af73f-158">The following JScript code shows the use of the *player*.**playState** property.</span></span> <span data-ttu-id="af73f-159">Un elemento di testo HTML, denominato "testo", Visualizza lo stato corrente.</span><span class="sxs-lookup"><span data-stu-id="af73f-159">An HTML text element, named "myText", displays the current status.</span></span> <span data-ttu-id="af73f-160">L'oggetto **Player** è stato creato con ID = "Player".</span><span class="sxs-lookup"><span data-stu-id="af73f-160">The **Player** object was created with ID = "Player".</span></span>


```JScript
// Test whether Windows Media Player is in the playing state.
if (3 == Player.playState)
    myText.value = "Windows Media Player is playing!";
else
    myText.value = "Windows Media Player is NOT playing!";
```



## <a name="requirements"></a><span data-ttu-id="af73f-161">Requisiti</span><span class="sxs-lookup"><span data-stu-id="af73f-161">Requirements</span></span>



| <span data-ttu-id="af73f-162">Requisito</span><span class="sxs-lookup"><span data-stu-id="af73f-162">Requirement</span></span> | <span data-ttu-id="af73f-163">Valore</span><span class="sxs-lookup"><span data-stu-id="af73f-163">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="af73f-164">Versione</span><span class="sxs-lookup"><span data-stu-id="af73f-164">Version</span></span><br/> | <span data-ttu-id="af73f-165">Windows Media Player versione 7,0 o successiva.</span><span class="sxs-lookup"><span data-stu-id="af73f-165">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="af73f-166">DLL</span><span class="sxs-lookup"><span data-stu-id="af73f-166">DLL</span></span><br/>     | <dl> <span data-ttu-id="af73f-167"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="af73f-167"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="af73f-168">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="af73f-168">See also</span></span>

<dl> <dt>

[<span data-ttu-id="af73f-169">**Oggetto Player**</span><span class="sxs-lookup"><span data-stu-id="af73f-169">**Player Object**</span></span>](player-object.md)
</dt> <dt>

[<span data-ttu-id="af73f-170">**Evento Player. PlayStateChange**</span><span class="sxs-lookup"><span data-stu-id="af73f-170">**Player.PlayStateChange Event**</span></span>](player-player-playstatechange.md)
</dt> </dl>

 

 





