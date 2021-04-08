---
title: IAgentCharacter preparare
description: IAgentCharacter preparare
ms.assetid: e016039f-a0b1-4ae9-bff6-7212b02c1ad8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3eebee8d2ea99c8782e9506e0e4a812cfb277487
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "104046710"
---
# <a name="iagentcharacterprepare"></a><span data-ttu-id="d1ebb-103">IAgentCharacter::P ripare</span><span class="sxs-lookup"><span data-stu-id="d1ebb-103">IAgentCharacter::Prepare</span></span>

<span data-ttu-id="d1ebb-104">\[Microsoft Agent è stato deprecato a partire da Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="d1ebb-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT Prepare(
   long dwType,     // type of animation data to load
   BSTR bszName,    // name of the animation 
   long bQueue,     // queue the request
   long * pdwReqID  // address of request ID
);
```

<span data-ttu-id="d1ebb-105">Recupera i dati di animazione per un carattere.</span><span class="sxs-lookup"><span data-stu-id="d1ebb-105">Retrieves animation data for a character.</span></span>

-   <span data-ttu-id="d1ebb-106">Restituisce \_ OK per indicare che l'operazione è stata completata.</span><span class="sxs-lookup"><span data-stu-id="d1ebb-106">Returns S\_OK to indicate the operation was successful.</span></span> <span data-ttu-id="d1ebb-107">Quando la funzione restituisce, *pdwReqID* contiene l'ID della richiesta.</span><span class="sxs-lookup"><span data-stu-id="d1ebb-107">When the function returns, *pdwReqID* contains the ID of the request.</span></span>

<dl> <dt>

<span data-ttu-id="d1ebb-108"><span id="dwType"></span><span id="dwtype"></span><span id="DWTYPE"></span>*dwType*</span><span class="sxs-lookup"><span data-stu-id="d1ebb-108"><span id="dwType"></span><span id="dwtype"></span><span id="DWTYPE"></span>*dwType*</span></span>
</dt> <dd>

<span data-ttu-id="d1ebb-109">Valore che indica il tipo di dati di animazione da caricare che deve essere uno dei seguenti:</span><span class="sxs-lookup"><span data-stu-id="d1ebb-109">A value that indicates the animation data type to load that must be one of the following:</span></span>



| <span data-ttu-id="d1ebb-110">Valore</span><span class="sxs-lookup"><span data-stu-id="d1ebb-110">Value</span></span>                                                           | <span data-ttu-id="d1ebb-111">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d1ebb-111">Description</span></span>                                                |
|-----------------------------------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="d1ebb-112">animazione di preparazione **breve const senza segno** **\_ = 0;**</span><span class="sxs-lookup"><span data-stu-id="d1ebb-112">**const unsigned short** **PREPARE\_ANIMATION = 0;**</span></span><br/> | <span data-ttu-id="d1ebb-113">Dati di animazione di un carattere.</span><span class="sxs-lookup"><span data-stu-id="d1ebb-113">A character's animation data.</span></span>                              |
| <span data-ttu-id="d1ebb-114">stato di preparazione **short senza segno const** **\_ = 1;**</span><span class="sxs-lookup"><span data-stu-id="d1ebb-114">**const unsigned short** **PREPARE\_STATE = 1;**</span></span><br/>     | <span data-ttu-id="d1ebb-115">Dati dello stato di un carattere.</span><span class="sxs-lookup"><span data-stu-id="d1ebb-115">A character's state data.</span></span>                                  |
| <span data-ttu-id="d1ebb-116">**const unsigned short** **preparate \_ Wave = 2**</span><span class="sxs-lookup"><span data-stu-id="d1ebb-116">**const unsigned short** **PREPARE\_WAVE = 2**</span></span><br/>       | <span data-ttu-id="d1ebb-117">File audio di un carattere (. WAV o. LWV) per l'output parlato.</span><span class="sxs-lookup"><span data-stu-id="d1ebb-117">A character's sound file (.WAV or .LWV) for spoken output.</span></span> |



 

</dd> <dt>

<span data-ttu-id="d1ebb-118"><span id="bszName"></span><span id="bszname"></span><span id="BSZNAME"></span>*bszName*</span><span class="sxs-lookup"><span data-stu-id="d1ebb-118"><span id="bszName"></span><span id="bszname"></span><span id="BSZNAME"></span>*bszName*</span></span>
</dt> <dd>

<span data-ttu-id="d1ebb-119">Nome dell'animazione o dello stato.</span><span class="sxs-lookup"><span data-stu-id="d1ebb-119">The name of the animation or state.</span></span>

<span data-ttu-id="d1ebb-120">Il nome dell'animazione è basato su quello definito per il carattere quando è stato salvato mediante l'editor dei caratteri di Microsoft Agent.</span><span class="sxs-lookup"><span data-stu-id="d1ebb-120">The animation name is based on that defined for the character when it was saved using the Microsoft Agent Character Editor.</span></span>

<span data-ttu-id="d1ebb-121">Per gli Stati, il valore può essere uno dei seguenti:</span><span class="sxs-lookup"><span data-stu-id="d1ebb-121">For states, the value can be one of the following:</span></span>



|                      |                                                 |
|----------------------|-------------------------------------------------|
| <span data-ttu-id="d1ebb-122">**Gesturing**</span><span class="sxs-lookup"><span data-stu-id="d1ebb-122">**"Gesturing"**</span></span>      | <span data-ttu-id="d1ebb-123">Per recuperare tutte le animazioni dello stato **gestuale** .</span><span class="sxs-lookup"><span data-stu-id="d1ebb-123">To retrieve all **Gesturing** state animations.</span></span> |
| <span data-ttu-id="d1ebb-124">**"GesturingDown"**</span><span class="sxs-lookup"><span data-stu-id="d1ebb-124">**"GesturingDown"**</span></span>  | <span data-ttu-id="d1ebb-125">Per recuperare le animazioni **GesturingDown** .</span><span class="sxs-lookup"><span data-stu-id="d1ebb-125">To retrieve **GesturingDown** animations.</span></span>       |
| <span data-ttu-id="d1ebb-126">**"GesturingLeft"**</span><span class="sxs-lookup"><span data-stu-id="d1ebb-126">**"GesturingLeft"**</span></span>  | <span data-ttu-id="d1ebb-127">Per recuperare le animazioni **GesturingLeft** .</span><span class="sxs-lookup"><span data-stu-id="d1ebb-127">To retrieve **GesturingLeft** animations.</span></span>       |
| <span data-ttu-id="d1ebb-128">**"GesturingRight"**</span><span class="sxs-lookup"><span data-stu-id="d1ebb-128">**"GesturingRight"**</span></span> | <span data-ttu-id="d1ebb-129">Per recuperare le animazioni **GesturingRight** .</span><span class="sxs-lookup"><span data-stu-id="d1ebb-129">To retrieve **GesturingRight** animations.</span></span>      |
| <span data-ttu-id="d1ebb-130">**"GesturingUp"**</span><span class="sxs-lookup"><span data-stu-id="d1ebb-130">**"GesturingUp"**</span></span>    | <span data-ttu-id="d1ebb-131">Per recuperare le animazioni **GesturingUp** .</span><span class="sxs-lookup"><span data-stu-id="d1ebb-131">To retrieve **GesturingUp** animations.</span></span>         |
| <span data-ttu-id="d1ebb-132">**Nascondere**</span><span class="sxs-lookup"><span data-stu-id="d1ebb-132">**"Hiding"**</span></span>         | <span data-ttu-id="d1ebb-133">Per recuperare le animazioni di stato **nascoste** .</span><span class="sxs-lookup"><span data-stu-id="d1ebb-133">To retrieve the **Hiding** state animations.</span></span>    |
| <span data-ttu-id="d1ebb-134">**Udienza**</span><span class="sxs-lookup"><span data-stu-id="d1ebb-134">**"Hearing"**</span></span>        | <span data-ttu-id="d1ebb-135">Per recuperare le animazioni dello stato di **udito** .</span><span class="sxs-lookup"><span data-stu-id="d1ebb-135">To retrieve the **Hearing** state animations.</span></span>   |
| <span data-ttu-id="d1ebb-136">**Inattivi**</span><span class="sxs-lookup"><span data-stu-id="d1ebb-136">**"Idling"**</span></span>         | <span data-ttu-id="d1ebb-137">Per recuperare tutte le animazioni di stato **minimo** .</span><span class="sxs-lookup"><span data-stu-id="d1ebb-137">To retrieve all **Idling** state animations.</span></span>    |
| <span data-ttu-id="d1ebb-138">**"IdlingLevel1"**</span><span class="sxs-lookup"><span data-stu-id="d1ebb-138">**"IdlingLevel1"**</span></span>   | <span data-ttu-id="d1ebb-139">Per recuperare tutte le animazioni **IdlingLevel1** .</span><span class="sxs-lookup"><span data-stu-id="d1ebb-139">To retrieve all **IdlingLevel1** animations.</span></span>    |
| <span data-ttu-id="d1ebb-140">**"IdlingLevel2"**</span><span class="sxs-lookup"><span data-stu-id="d1ebb-140">**"IdlingLevel2"**</span></span>   | <span data-ttu-id="d1ebb-141">Per recuperare tutte le animazioni **IdlingLevel2** .</span><span class="sxs-lookup"><span data-stu-id="d1ebb-141">To retrieve all **IdlingLevel2** animations.</span></span>    |
| <span data-ttu-id="d1ebb-142">**"IdlingLevel3"**</span><span class="sxs-lookup"><span data-stu-id="d1ebb-142">**"IdlingLevel3"**</span></span>   | <span data-ttu-id="d1ebb-143">Per recuperare tutte le animazioni **IdlingLevel3** .</span><span class="sxs-lookup"><span data-stu-id="d1ebb-143">To retrieve all **IdlingLevel3** animations.</span></span>    |
| <span data-ttu-id="d1ebb-144">**In ascolto**</span><span class="sxs-lookup"><span data-stu-id="d1ebb-144">**"Listening"**</span></span>      | <span data-ttu-id="d1ebb-145">Per recuperare le animazioni dello stato di **ascolto** .</span><span class="sxs-lookup"><span data-stu-id="d1ebb-145">To retrieve the **Listening** state animations.</span></span> |
| <span data-ttu-id="d1ebb-146">**Movimento**</span><span class="sxs-lookup"><span data-stu-id="d1ebb-146">**"Moving"**</span></span>         | <span data-ttu-id="d1ebb-147">Per recuperare tutte le animazioni dello stato di **trasferimento** .</span><span class="sxs-lookup"><span data-stu-id="d1ebb-147">To retrieve all **Moving** state animations.</span></span>    |
| <span data-ttu-id="d1ebb-148">**"MovingDown"**</span><span class="sxs-lookup"><span data-stu-id="d1ebb-148">**"MovingDown"**</span></span>     | <span data-ttu-id="d1ebb-149">Per recuperare tutte le animazioni in **evoluzione** .</span><span class="sxs-lookup"><span data-stu-id="d1ebb-149">To retrieve all **Moving** animations.</span></span>          |
| <span data-ttu-id="d1ebb-150">**"MovingLeft"**</span><span class="sxs-lookup"><span data-stu-id="d1ebb-150">**"MovingLeft"**</span></span>     | <span data-ttu-id="d1ebb-151">Per recuperare tutte le animazioni **MovingLeft** .</span><span class="sxs-lookup"><span data-stu-id="d1ebb-151">To retrieve all **MovingLeft** animations.</span></span>      |
| <span data-ttu-id="d1ebb-152">**"MovingRight"**</span><span class="sxs-lookup"><span data-stu-id="d1ebb-152">**"MovingRight"**</span></span>    | <span data-ttu-id="d1ebb-153">Per recuperare tutte le animazioni **MovingRight** .</span><span class="sxs-lookup"><span data-stu-id="d1ebb-153">To retrieve all **MovingRight** animations.</span></span>     |
| <span data-ttu-id="d1ebb-154">**"MovingUp"**</span><span class="sxs-lookup"><span data-stu-id="d1ebb-154">**"MovingUp"**</span></span>       | <span data-ttu-id="d1ebb-155">Per recuperare tutte le animazioni **MovingUp** .</span><span class="sxs-lookup"><span data-stu-id="d1ebb-155">To retrieve all **MovingUp** animations.</span></span>        |
| <span data-ttu-id="d1ebb-156">**Che Mostra**</span><span class="sxs-lookup"><span data-stu-id="d1ebb-156">**"Showing"**</span></span>        | <span data-ttu-id="d1ebb-157">Per **recuperare le animazioni di visualizzazione dello** stato.</span><span class="sxs-lookup"><span data-stu-id="d1ebb-157">To retrieve the **Showing** state animations.</span></span>   |
| <span data-ttu-id="d1ebb-158">**Parlando**</span><span class="sxs-lookup"><span data-stu-id="d1ebb-158">**"Speaking"**</span></span>       | <span data-ttu-id="d1ebb-159">Per recuperare le animazioni dello stato di **pronuncia** .</span><span class="sxs-lookup"><span data-stu-id="d1ebb-159">To retrieve the **Speaking** state animations.</span></span>  |



 

<span data-ttu-id="d1ebb-160">Per. File WAV, impostare *bszName* sull'URL o sulla specifica del file per. File WAV.</span><span class="sxs-lookup"><span data-stu-id="d1ebb-160">For .WAV files, set *bszName* to the URL or file specification for the .WAV file.</span></span> <span data-ttu-id="d1ebb-161">Se la specifica non è completa, viene interpretata come relativa alla specifica utilizzata nel metodo [**Load**](https://www.bing.com/search?q=**Load**) .</span><span class="sxs-lookup"><span data-stu-id="d1ebb-161">If the specification is not complete, it is interpreted as being relative to the specification used in the [**Load**](https://www.bing.com/search?q=**Load**) method.</span></span>

</dd> <dt>

<span data-ttu-id="d1ebb-162"><span id="bQueue"></span><span id="bqueue"></span><span id="BQUEUE"></span>*bQueue*</span><span class="sxs-lookup"><span data-stu-id="d1ebb-162"><span id="bQueue"></span><span id="bqueue"></span><span id="BQUEUE"></span>*bQueue*</span></span>
</dt> <dd>

<span data-ttu-id="d1ebb-163">Valore booleano che specifica se il server accoda la richiesta di [**preparazione**](/windows/desktop/lwef/iagentcharacter--prepare) .</span><span class="sxs-lookup"><span data-stu-id="d1ebb-163">A Boolean specifying whether the server queues the [**Prepare**](/windows/desktop/lwef/iagentcharacter--prepare) request.</span></span> <span data-ttu-id="d1ebb-164">**True** Accoda la richiesta e causa l'attesa di qualsiasi richiesta di animazione che la segua finché non vengono caricati i dati di animazione specificati.</span><span class="sxs-lookup"><span data-stu-id="d1ebb-164">**True** queues the request and causes any animation request that follows it to wait until the animation data it specifies is loaded.</span></span> <span data-ttu-id="d1ebb-165">**False** recupera i dati di animazione in modo asincrono.</span><span class="sxs-lookup"><span data-stu-id="d1ebb-165">**False** retrieves the animation data asynchronously.</span></span>

</dd> <dt>

<span data-ttu-id="d1ebb-166"><span id="pdwReqID"></span><span id="pdwreqid"></span><span id="PDWREQID"></span>*pdwReqID*</span><span class="sxs-lookup"><span data-stu-id="d1ebb-166"><span id="pdwReqID"></span><span id="pdwreqid"></span><span id="PDWREQID"></span>*pdwReqID*</span></span>
</dt> <dd>

<span data-ttu-id="d1ebb-167">Indirizzo di una variabile che riceve l'ID della richiesta di [**preparazione**](/windows/desktop/lwef/iagentcharacter--prepare) .</span><span class="sxs-lookup"><span data-stu-id="d1ebb-167">Address of a variable that receives the [**Prepare**](/windows/desktop/lwef/iagentcharacter--prepare) request ID.</span></span>

</dd> </dl>

<span data-ttu-id="d1ebb-168">Se si carica un carattere usando il protocollo HTTP (un. File ACF), è necessario usare il metodo [**Prepare**](/windows/desktop/lwef/iagentcharacter--prepare) per recuperare i dati di animazione prima di poter riprodurre l'animazione.</span><span class="sxs-lookup"><span data-stu-id="d1ebb-168">If you load a character using the HTTP protocol (an .ACF file), you must use the [**Prepare**](/windows/desktop/lwef/iagentcharacter--prepare) method to retrieve animation data before you can play the animation.</span></span> <span data-ttu-id="d1ebb-169">Non è possibile usare questo metodo se il carattere è stato caricato usando il protocollo UNC (un. File ACS).</span><span class="sxs-lookup"><span data-stu-id="d1ebb-169">You cannot use this method if you loaded the character using the UNC protocol (an .ACS file).</span></span> <span data-ttu-id="d1ebb-170">Non è inoltre possibile recuperare i dati HTTP per un carattere utilizzando **prepara** se è stato caricato il carattere utilizzando il protocollo UNC (. File di caratteri ACS).</span><span class="sxs-lookup"><span data-stu-id="d1ebb-170">You also cannot retrieve HTTP data for a character using **Prepare** if you loaded that character using the UNC protocol (.ACS character file).</span></span>

<span data-ttu-id="d1ebb-171">I dati di animazione o audio recuperati con il metodo [**Prepare**](/windows/desktop/lwef/iagentcharacter--prepare) vengono archiviati nella cache del browser.</span><span class="sxs-lookup"><span data-stu-id="d1ebb-171">Animation or sound data retrieved with the [**Prepare**](/windows/desktop/lwef/iagentcharacter--prepare) method is stored in the browser's cache.</span></span> <span data-ttu-id="d1ebb-172">Le chiamate successive verificheranno la cache e, se i dati di animazione sono già presenti, il controllo caricherà i dati direttamente dalla cache.</span><span class="sxs-lookup"><span data-stu-id="d1ebb-172">Subsequent calls will check the cache, and if the animation data is already there, the control loads the data directly from the cache.</span></span> <span data-ttu-id="d1ebb-173">Una volta caricati, i dati di animazione o audio possono essere riprodotti con i metodi [**Play**](/windows/desktop/lwef/iagentcharacter--play) o [**Speak**](/windows/desktop/lwef/iagentcharacter--speak) .</span><span class="sxs-lookup"><span data-stu-id="d1ebb-173">Once loaded, the animation or sound data can be played with the [**Play**](/windows/desktop/lwef/iagentcharacter--play) or [**Speak**](/windows/desktop/lwef/iagentcharacter--speak) methods.</span></span>

<span data-ttu-id="d1ebb-174">È possibile specificare più animazioni e Stati separandoli con virgole.</span><span class="sxs-lookup"><span data-stu-id="d1ebb-174">You can specify multiple animations and states by separating them with commas.</span></span> <span data-ttu-id="d1ebb-175">Tuttavia, non è possibile combinare tipi nella stessa istruzione [**Prepare**](/windows/desktop/lwef/iagentcharacter--prepare) .</span><span class="sxs-lookup"><span data-stu-id="d1ebb-175">However, you cannot mix types in the same [**Prepare**](/windows/desktop/lwef/iagentcharacter--prepare) statement.</span></span>

 

