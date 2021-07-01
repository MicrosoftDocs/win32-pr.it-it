---
title: Preparazione di IAgentCharacter
description: Preparazione di IAgentCharacter
ms.assetid: e016039f-a0b1-4ae9-bff6-7212b02c1ad8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b383bf10330934379990693b75fe2908a432f8d5
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/30/2021
ms.locfileid: "113119876"
---
# <a name="iagentcharacterprepare"></a><span data-ttu-id="30ec1-103">IAgentCharacter::P repare</span><span class="sxs-lookup"><span data-stu-id="30ec1-103">IAgentCharacter::Prepare</span></span>

<span data-ttu-id="30ec1-104">\[Microsoft Agent è deprecato a livello di Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="30ec1-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT Prepare(
   long dwType,     // type of animation data to load
   BSTR bszName,    // name of the animation 
   long bQueue,     // queue the request
   long * pdwReqID  // address of request ID
);
```

<span data-ttu-id="30ec1-105">Recupera i dati di animazione per un carattere.</span><span class="sxs-lookup"><span data-stu-id="30ec1-105">Retrieves animation data for a character.</span></span>

-   <span data-ttu-id="30ec1-106">Restituisce S \_ OK per indicare che l'operazione è riuscita.</span><span class="sxs-lookup"><span data-stu-id="30ec1-106">Returns S\_OK to indicate the operation was successful.</span></span> <span data-ttu-id="30ec1-107">Quando la funzione viene restituita, *pdwReqID* contiene l'ID della richiesta.</span><span class="sxs-lookup"><span data-stu-id="30ec1-107">When the function returns, *pdwReqID* contains the ID of the request.</span></span>

<dl> <dt>

<span data-ttu-id="30ec1-108"><span id="dwType"></span><span id="dwtype"></span><span id="DWTYPE"></span>*dwType*</span><span class="sxs-lookup"><span data-stu-id="30ec1-108"><span id="dwType"></span><span id="dwtype"></span><span id="DWTYPE"></span>*dwType*</span></span>
</dt> <dd>

<span data-ttu-id="30ec1-109">Valore che indica il tipo di dati di animazione da caricare che deve essere uno dei seguenti:</span><span class="sxs-lookup"><span data-stu-id="30ec1-109">A value that indicates the animation data type to load that must be one of the following:</span></span>



| <span data-ttu-id="30ec1-110">Valore</span><span class="sxs-lookup"><span data-stu-id="30ec1-110">Value</span></span>                                                           | <span data-ttu-id="30ec1-111">Descrizione</span><span class="sxs-lookup"><span data-stu-id="30ec1-111">Description</span></span>                                                |
|-----------------------------------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="30ec1-112">**const unsigned short** **PREPARE ANIMATION = \_ 0;**</span><span class="sxs-lookup"><span data-stu-id="30ec1-112">**const unsigned short** **PREPARE\_ANIMATION = 0;**</span></span><br/> | <span data-ttu-id="30ec1-113">Dati di animazione di un carattere.</span><span class="sxs-lookup"><span data-stu-id="30ec1-113">A character's animation data.</span></span>                              |
| <span data-ttu-id="30ec1-114">**const unsigned short** **PREPARE STATE = \_ 1;**</span><span class="sxs-lookup"><span data-stu-id="30ec1-114">**const unsigned short** **PREPARE\_STATE = 1;**</span></span><br/>     | <span data-ttu-id="30ec1-115">Dati sullo stato di un carattere.</span><span class="sxs-lookup"><span data-stu-id="30ec1-115">A character's state data.</span></span>                                  |
| <span data-ttu-id="30ec1-116">**const unsigned short** **PREPARE WAVE = \_ 2**</span><span class="sxs-lookup"><span data-stu-id="30ec1-116">**const unsigned short** **PREPARE\_WAVE = 2**</span></span><br/>       | <span data-ttu-id="30ec1-117">File audio di un carattere (. WAV o . LWV) per l'output parlato.</span><span class="sxs-lookup"><span data-stu-id="30ec1-117">A character's sound file (.WAV or .LWV) for spoken output.</span></span> |



 

</dd> <dt>

<span data-ttu-id="30ec1-118"><span id="bszName"></span><span id="bszname"></span><span id="BSZNAME"></span>*bszName*</span><span class="sxs-lookup"><span data-stu-id="30ec1-118"><span id="bszName"></span><span id="bszname"></span><span id="BSZNAME"></span>*bszName*</span></span>
</dt> <dd>

<span data-ttu-id="30ec1-119">Nome dell'animazione o dello stato.</span><span class="sxs-lookup"><span data-stu-id="30ec1-119">The name of the animation or state.</span></span>

<span data-ttu-id="30ec1-120">Il nome dell'animazione si basa su quello definito per il carattere quando è stato salvato usando l'editor di caratteri di Microsoft Agent.</span><span class="sxs-lookup"><span data-stu-id="30ec1-120">The animation name is based on that defined for the character when it was saved using the Microsoft Agent Character Editor.</span></span>

<span data-ttu-id="30ec1-121">Per gli stati, il valore può essere uno dei seguenti:</span><span class="sxs-lookup"><span data-stu-id="30ec1-121">For states, the value can be one of the following:</span></span>



|                      | <span data-ttu-id="30ec1-122">Descrizione</span><span class="sxs-lookup"><span data-stu-id="30ec1-122">Description</span></span>                                     |
|----------------------|-------------------------------------------------|
| <span data-ttu-id="30ec1-123">**"Gesturing"**</span><span class="sxs-lookup"><span data-stu-id="30ec1-123">**"Gesturing"**</span></span>      | <span data-ttu-id="30ec1-124">Per recuperare tutte **le animazioni dello stato** di gesturing.</span><span class="sxs-lookup"><span data-stu-id="30ec1-124">To retrieve all **Gesturing** state animations.</span></span> |
| <span data-ttu-id="30ec1-125">**"GesturingDown"**</span><span class="sxs-lookup"><span data-stu-id="30ec1-125">**"GesturingDown"**</span></span>  | <span data-ttu-id="30ec1-126">Per recuperare **le animazioni GesturingDown.**</span><span class="sxs-lookup"><span data-stu-id="30ec1-126">To retrieve **GesturingDown** animations.</span></span>       |
| <span data-ttu-id="30ec1-127">**"GesturingLeft"**</span><span class="sxs-lookup"><span data-stu-id="30ec1-127">**"GesturingLeft"**</span></span>  | <span data-ttu-id="30ec1-128">Per recuperare **le animazioni GesturingLeft.**</span><span class="sxs-lookup"><span data-stu-id="30ec1-128">To retrieve **GesturingLeft** animations.</span></span>       |
| <span data-ttu-id="30ec1-129">**"GesturingRight"**</span><span class="sxs-lookup"><span data-stu-id="30ec1-129">**"GesturingRight"**</span></span> | <span data-ttu-id="30ec1-130">Per recuperare **le animazioni GesturingRight.**</span><span class="sxs-lookup"><span data-stu-id="30ec1-130">To retrieve **GesturingRight** animations.</span></span>      |
| <span data-ttu-id="30ec1-131">**"GesturingUp"**</span><span class="sxs-lookup"><span data-stu-id="30ec1-131">**"GesturingUp"**</span></span>    | <span data-ttu-id="30ec1-132">Per recuperare **le animazioni GesturingUp.**</span><span class="sxs-lookup"><span data-stu-id="30ec1-132">To retrieve **GesturingUp** animations.</span></span>         |
| <span data-ttu-id="30ec1-133">**"Nascondi"**</span><span class="sxs-lookup"><span data-stu-id="30ec1-133">**"Hiding"**</span></span>         | <span data-ttu-id="30ec1-134">Per recuperare le animazioni di stato **Nascondi.**</span><span class="sxs-lookup"><span data-stu-id="30ec1-134">To retrieve the **Hiding** state animations.</span></span>    |
| <span data-ttu-id="30ec1-135">**"Ascolto"**</span><span class="sxs-lookup"><span data-stu-id="30ec1-135">**"Hearing"**</span></span>        | <span data-ttu-id="30ec1-136">Per recuperare le animazioni **di stato Hearing.**</span><span class="sxs-lookup"><span data-stu-id="30ec1-136">To retrieve the **Hearing** state animations.</span></span>   |
| <span data-ttu-id="30ec1-137">**"Idling"**</span><span class="sxs-lookup"><span data-stu-id="30ec1-137">**"Idling"**</span></span>         | <span data-ttu-id="30ec1-138">Per recuperare tutte le **animazioni di stato di Idling.**</span><span class="sxs-lookup"><span data-stu-id="30ec1-138">To retrieve all **Idling** state animations.</span></span>    |
| <span data-ttu-id="30ec1-139">**"IdlingLevel1"**</span><span class="sxs-lookup"><span data-stu-id="30ec1-139">**"IdlingLevel1"**</span></span>   | <span data-ttu-id="30ec1-140">Per recuperare tutte **le animazioni IdlingLevel1.**</span><span class="sxs-lookup"><span data-stu-id="30ec1-140">To retrieve all **IdlingLevel1** animations.</span></span>    |
| <span data-ttu-id="30ec1-141">**"IdlingLevel2"**</span><span class="sxs-lookup"><span data-stu-id="30ec1-141">**"IdlingLevel2"**</span></span>   | <span data-ttu-id="30ec1-142">Per recuperare tutte **le animazioni IdlingLevel2.**</span><span class="sxs-lookup"><span data-stu-id="30ec1-142">To retrieve all **IdlingLevel2** animations.</span></span>    |
| <span data-ttu-id="30ec1-143">**"IdlingLevel3"**</span><span class="sxs-lookup"><span data-stu-id="30ec1-143">**"IdlingLevel3"**</span></span>   | <span data-ttu-id="30ec1-144">Per recuperare tutte **le animazioni IdlingLevel3.**</span><span class="sxs-lookup"><span data-stu-id="30ec1-144">To retrieve all **IdlingLevel3** animations.</span></span>    |
| <span data-ttu-id="30ec1-145">**"Ascolto"**</span><span class="sxs-lookup"><span data-stu-id="30ec1-145">**"Listening"**</span></span>      | <span data-ttu-id="30ec1-146">Per recuperare le **animazioni dello stato** di ascolto.</span><span class="sxs-lookup"><span data-stu-id="30ec1-146">To retrieve the **Listening** state animations.</span></span> |
| <span data-ttu-id="30ec1-147">**"Moving"**</span><span class="sxs-lookup"><span data-stu-id="30ec1-147">**"Moving"**</span></span>         | <span data-ttu-id="30ec1-148">Per recuperare tutte le **animazioni di** stato in movimento.</span><span class="sxs-lookup"><span data-stu-id="30ec1-148">To retrieve all **Moving** state animations.</span></span>    |
| <span data-ttu-id="30ec1-149">**"MovingDown"**</span><span class="sxs-lookup"><span data-stu-id="30ec1-149">**"MovingDown"**</span></span>     | <span data-ttu-id="30ec1-150">Per recuperare tutte **le animazioni in** movimento.</span><span class="sxs-lookup"><span data-stu-id="30ec1-150">To retrieve all **Moving** animations.</span></span>          |
| <span data-ttu-id="30ec1-151">**"MovingLeft"**</span><span class="sxs-lookup"><span data-stu-id="30ec1-151">**"MovingLeft"**</span></span>     | <span data-ttu-id="30ec1-152">Per recuperare tutte **le animazioni MovingLeft.**</span><span class="sxs-lookup"><span data-stu-id="30ec1-152">To retrieve all **MovingLeft** animations.</span></span>      |
| <span data-ttu-id="30ec1-153">**"MovingRight"**</span><span class="sxs-lookup"><span data-stu-id="30ec1-153">**"MovingRight"**</span></span>    | <span data-ttu-id="30ec1-154">Per recuperare tutte **le animazioni MovingRight.**</span><span class="sxs-lookup"><span data-stu-id="30ec1-154">To retrieve all **MovingRight** animations.</span></span>     |
| <span data-ttu-id="30ec1-155">**"MovingUp"**</span><span class="sxs-lookup"><span data-stu-id="30ec1-155">**"MovingUp"**</span></span>       | <span data-ttu-id="30ec1-156">Per recuperare tutte **le animazioni MovingUp.**</span><span class="sxs-lookup"><span data-stu-id="30ec1-156">To retrieve all **MovingUp** animations.</span></span>        |
| <span data-ttu-id="30ec1-157">**"Showing"**</span><span class="sxs-lookup"><span data-stu-id="30ec1-157">**"Showing"**</span></span>        | <span data-ttu-id="30ec1-158">Per recuperare le **animazioni dello** stato di visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="30ec1-158">To retrieve the **Showing** state animations.</span></span>   |
| <span data-ttu-id="30ec1-159">**"Speaking"**</span><span class="sxs-lookup"><span data-stu-id="30ec1-159">**"Speaking"**</span></span>       | <span data-ttu-id="30ec1-160">Per recuperare le **animazioni dello stato Speaking.**</span><span class="sxs-lookup"><span data-stu-id="30ec1-160">To retrieve the **Speaking** state animations.</span></span>  |



 

<span data-ttu-id="30ec1-161">Per. File WAV, impostare *bszName* sull'URL o sulla specifica del file per . File WAV.</span><span class="sxs-lookup"><span data-stu-id="30ec1-161">For .WAV files, set *bszName* to the URL or file specification for the .WAV file.</span></span> <span data-ttu-id="30ec1-162">Se la specifica non è completa, viene interpretata come relativa alla specifica usata nel [**metodo Load.**](https://www.bing.com/search?q=**Load**)</span><span class="sxs-lookup"><span data-stu-id="30ec1-162">If the specification is not complete, it is interpreted as being relative to the specification used in the [**Load**](https://www.bing.com/search?q=**Load**) method.</span></span>

</dd> <dt>

<span data-ttu-id="30ec1-163"><span id="bQueue"></span><span id="bqueue"></span><span id="BQUEUE"></span>*bQueue*</span><span class="sxs-lookup"><span data-stu-id="30ec1-163"><span id="bQueue"></span><span id="bqueue"></span><span id="BQUEUE"></span>*bQueue*</span></span>
</dt> <dd>

<span data-ttu-id="30ec1-164">Valore booleano che specifica se il server accoda la [**richiesta Prepare.**](/windows/desktop/lwef/iagentcharacter--prepare)</span><span class="sxs-lookup"><span data-stu-id="30ec1-164">A Boolean specifying whether the server queues the [**Prepare**](/windows/desktop/lwef/iagentcharacter--prepare) request.</span></span> <span data-ttu-id="30ec1-165">**True** accoda la richiesta e fa in modo che tutte le richieste di animazione che la seguono attendano fino al caricamento dei dati di animazione specificati.</span><span class="sxs-lookup"><span data-stu-id="30ec1-165">**True** queues the request and causes any animation request that follows it to wait until the animation data it specifies is loaded.</span></span> <span data-ttu-id="30ec1-166">**False** recupera i dati di animazione in modo asincrono.</span><span class="sxs-lookup"><span data-stu-id="30ec1-166">**False** retrieves the animation data asynchronously.</span></span>

</dd> <dt>

<span data-ttu-id="30ec1-167"><span id="pdwReqID"></span><span id="pdwreqid"></span><span id="PDWREQID"></span>*pdwReqID*</span><span class="sxs-lookup"><span data-stu-id="30ec1-167"><span id="pdwReqID"></span><span id="pdwreqid"></span><span id="PDWREQID"></span>*pdwReqID*</span></span>
</dt> <dd>

<span data-ttu-id="30ec1-168">Indirizzo di una variabile che riceve l'ID [**richiesta di**](/windows/desktop/lwef/iagentcharacter--prepare) preparazione.</span><span class="sxs-lookup"><span data-stu-id="30ec1-168">Address of a variable that receives the [**Prepare**](/windows/desktop/lwef/iagentcharacter--prepare) request ID.</span></span>

</dd> </dl>

<span data-ttu-id="30ec1-169">Se si carica un carattere usando il protocollo HTTP (un oggetto . ACF), è necessario usare il [**metodo Prepare**](/windows/desktop/lwef/iagentcharacter--prepare) per recuperare i dati dell'animazione prima di poter riprodurre l'animazione.</span><span class="sxs-lookup"><span data-stu-id="30ec1-169">If you load a character using the HTTP protocol (an .ACF file), you must use the [**Prepare**](/windows/desktop/lwef/iagentcharacter--prepare) method to retrieve animation data before you can play the animation.</span></span> <span data-ttu-id="30ec1-170">Non è possibile usare questo metodo se il carattere è stato caricato usando il protocollo UNC (un oggetto . file ACS).</span><span class="sxs-lookup"><span data-stu-id="30ec1-170">You cannot use this method if you loaded the character using the UNC protocol (an .ACS file).</span></span> <span data-ttu-id="30ec1-171">Non è inoltre possibile recuperare i dati HTTP per un carattere usando **Prepare** se tale carattere è stato caricato usando il protocollo UNC (. File di caratteri ACS).</span><span class="sxs-lookup"><span data-stu-id="30ec1-171">You also cannot retrieve HTTP data for a character using **Prepare** if you loaded that character using the UNC protocol (.ACS character file).</span></span>

<span data-ttu-id="30ec1-172">I dati di animazione o audio recuperati [**con il metodo Prepare**](/windows/desktop/lwef/iagentcharacter--prepare) vengono archiviati nella cache del browser.</span><span class="sxs-lookup"><span data-stu-id="30ec1-172">Animation or sound data retrieved with the [**Prepare**](/windows/desktop/lwef/iagentcharacter--prepare) method is stored in the browser's cache.</span></span> <span data-ttu-id="30ec1-173">Le chiamate successive controllano la cache e, se i dati dell'animazione sono già presenti, il controllo carica i dati direttamente dalla cache.</span><span class="sxs-lookup"><span data-stu-id="30ec1-173">Subsequent calls will check the cache, and if the animation data is already there, the control loads the data directly from the cache.</span></span> <span data-ttu-id="30ec1-174">Dopo il caricamento, l'animazione o i dati sonori possono essere riprodotti con i [**metodi Play**](/windows/desktop/lwef/iagentcharacter--play) [**o Speak.**](/windows/desktop/lwef/iagentcharacter--speak)</span><span class="sxs-lookup"><span data-stu-id="30ec1-174">Once loaded, the animation or sound data can be played with the [**Play**](/windows/desktop/lwef/iagentcharacter--play) or [**Speak**](/windows/desktop/lwef/iagentcharacter--speak) methods.</span></span>

<span data-ttu-id="30ec1-175">È possibile specificare più animazioni e stati separandoli con virgole.</span><span class="sxs-lookup"><span data-stu-id="30ec1-175">You can specify multiple animations and states by separating them with commas.</span></span> <span data-ttu-id="30ec1-176">Tuttavia, non è possibile combinare tipi nella stessa [**istruzione Prepare.**](/windows/desktop/lwef/iagentcharacter--prepare)</span><span class="sxs-lookup"><span data-stu-id="30ec1-176">However, you cannot mix types in the same [**Prepare**](/windows/desktop/lwef/iagentcharacter--prepare) statement.</span></span>

 

