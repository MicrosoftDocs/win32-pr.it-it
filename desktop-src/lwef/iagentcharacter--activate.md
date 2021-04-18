---
title: Attivazione di IAgentCharacter
description: Attivazione di IAgentCharacter
ms.assetid: a81eb62d-709b-46b4-9ff2-c9017f7f853e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c1e86d2c094da484f528750d433e0fb6608790e4
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104516123"
---
# <a name="iagentcharacteractivate"></a><span data-ttu-id="86a58-103">IAgentCharacter:: Activate</span><span class="sxs-lookup"><span data-stu-id="86a58-103">IAgentCharacter::Activate</span></span>

<span data-ttu-id="86a58-104">\[Microsoft Agent è stato deprecato a partire da Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="86a58-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT Activate(
   short sState, // topmost character or client setting
);
```

<span data-ttu-id="86a58-105">Imposta un valore che indica se un client è attivo o un carattere è in primo piano.</span><span class="sxs-lookup"><span data-stu-id="86a58-105">Sets whether a client is active or a character is topmost.</span></span>

-   <span data-ttu-id="86a58-106">Restituisce \_ OK per indicare che l'operazione è stata completata.</span><span class="sxs-lookup"><span data-stu-id="86a58-106">Returns S\_OK to indicate the operation was successful.</span></span>
-   <span data-ttu-id="86a58-107">Restituisce \_ false per indicare che l'operazione non è riuscita.</span><span class="sxs-lookup"><span data-stu-id="86a58-107">Returns S\_FALSE to indicate the operation was not successful.</span></span>

<dl> <dt>

<span data-ttu-id="86a58-108"><span id="sState"></span><span id="sstate"></span><span id="SSTATE"></span>*sState*</span><span class="sxs-lookup"><span data-stu-id="86a58-108"><span id="sState"></span><span id="sstate"></span><span id="SSTATE"></span>*sState*</span></span>
</dt> <dd>

<span data-ttu-id="86a58-109">Per questo parametro è possibile specificare i valori seguenti:</span><span class="sxs-lookup"><span data-stu-id="86a58-109">You can specify the following values for this parameter:</span></span>



| <span data-ttu-id="86a58-110">Valore</span><span class="sxs-lookup"><span data-stu-id="86a58-110">Value</span></span> | <span data-ttu-id="86a58-111">Descrizione</span><span class="sxs-lookup"><span data-stu-id="86a58-111">Description</span></span>                   |
|-------|-------------------------------|
| <span data-ttu-id="86a58-112">0</span><span class="sxs-lookup"><span data-stu-id="86a58-112">0</span></span>     | <span data-ttu-id="86a58-113">Imposta come non client attivo.</span><span class="sxs-lookup"><span data-stu-id="86a58-113">Set as not the active client.</span></span> |
| <span data-ttu-id="86a58-114">1</span><span class="sxs-lookup"><span data-stu-id="86a58-114">1</span></span>     | <span data-ttu-id="86a58-115">Imposta come client attivo.</span><span class="sxs-lookup"><span data-stu-id="86a58-115">Set as the active client.</span></span>     |
| <span data-ttu-id="86a58-116">2</span><span class="sxs-lookup"><span data-stu-id="86a58-116">2</span></span>     | <span data-ttu-id="86a58-117">Creare il carattere di primo livello.</span><span class="sxs-lookup"><span data-stu-id="86a58-117">Make the topmost character.</span></span>   |



 

</dd> </dl>

<span data-ttu-id="86a58-118">Quando sono visibili più caratteri, solo uno dei caratteri riceve l'input vocale alla volta.</span><span class="sxs-lookup"><span data-stu-id="86a58-118">When multiple characters are visible, only one of the characters receives speech input at a time.</span></span> <span data-ttu-id="86a58-119">Analogamente, quando più applicazioni client condividono lo stesso carattere, solo uno dei client riceve l'input del mouse, ad esempio gli eventi di clic o di trascinamento del controllo agente Microsoft alla volta.</span><span class="sxs-lookup"><span data-stu-id="86a58-119">Similarly, when multiple client applications share the same character, only one of the clients receives mouse input (for example, Microsoft Agent control click or drag events) at a time.</span></span> <span data-ttu-id="86a58-120">Il set di caratteri per ricevere input da mouse e vocale è il carattere superiore e il client che riceve l'input è il client attivo del carattere.</span><span class="sxs-lookup"><span data-stu-id="86a58-120">The character set to receive mouse and speech input is the topmost character and the client that receives input is the character's active client.</span></span> <span data-ttu-id="86a58-121">La finestra del carattere superiore viene visualizzata anche nella parte superiore dell'ordine z della finestra dei caratteri. In genere, l'utente determina quale carattere è in primo piano selezionandola in modo esplicito.</span><span class="sxs-lookup"><span data-stu-id="86a58-121">(The topmost character's window also appears at the top of the character window's z-order.) Typically, the user determines which character is topmost by explicitly selecting it.</span></span> <span data-ttu-id="86a58-122">Tuttavia, l'attivazione in primo piano cambia anche quando un carattere viene visualizzato o nascosto (il carattere diventa o non è più in primo piano, rispettivamente).</span><span class="sxs-lookup"><span data-stu-id="86a58-122">However, topmost activation also changes when a character is shown or hidden (the character becomes or is no longer topmost, respectively.)</span></span>

<span data-ttu-id="86a58-123">È anche possibile usare questo metodo per gestire in modo esplicito quando il client riceve l'input indirizzato al carattere, ad esempio quando l'applicazione stessa diventa attiva.</span><span class="sxs-lookup"><span data-stu-id="86a58-123">You can also use this method to explicitly manage when your client receives input directed to the character, such as when your application itself becomes active.</span></span> <span data-ttu-id="86a58-124">Se, ad esempio, si imposta **lo stato** su 2, il carattere è in primo piano e il client riceve tutti gli eventi di input del mouse e vocale generati dall'interazione dell'utente con il carattere.</span><span class="sxs-lookup"><span data-stu-id="86a58-124">For example, setting **State** to 2 makes the character topmost, and your client receives all mouse and speech input events generated from user interaction with the character.</span></span> <span data-ttu-id="86a58-125">Quindi, rende il client anche il client di input-attivo del carattere.</span><span class="sxs-lookup"><span data-stu-id="86a58-125">Therefore, it also makes your client the input-active client of the character.</span></span> <span data-ttu-id="86a58-126">Tuttavia, è anche possibile impostare il client attivo per un carattere senza rendere il carattere superiore, impostando **lo stato** su 1.</span><span class="sxs-lookup"><span data-stu-id="86a58-126">However, you can also set the active client for a character without making the character topmost, by setting **State** to 1.</span></span> <span data-ttu-id="86a58-127">Ciò consente al client di ricevere input indirizzato a tale carattere quando il carattere diventa più in alto.</span><span class="sxs-lookup"><span data-stu-id="86a58-127">This enables your client to receive input directed to that character when the character becomes topmost.</span></span> <span data-ttu-id="86a58-128">Analogamente, è possibile impostare il client in modo che non sia il client attivo (per non ricevere input) quando il carattere diventa superiore, impostando **stato** su 0.</span><span class="sxs-lookup"><span data-stu-id="86a58-128">Similarly, you can set your client to not be the active client (to not receive input) when the character becomes topmost, by setting **State** to 0.</span></span> <span data-ttu-id="86a58-129">È possibile determinare se un carattere dispone di altri client correnti utilizzando [**IAgentCharacter:: HasOtherClients**](iagentcharacter--hasotherclients.md).</span><span class="sxs-lookup"><span data-stu-id="86a58-129">You can determine if a character has other current clients using [**IAgentCharacter::HasOtherClients**](iagentcharacter--hasotherclients.md).</span></span>

<span data-ttu-id="86a58-130">Evitare di chiamare questo metodo direttamente dopo un metodo [**show**](iagentcharacter--show.md) .</span><span class="sxs-lookup"><span data-stu-id="86a58-130">Avoid calling this method directly after a [**Show**](iagentcharacter--show.md) method.</span></span> <span data-ttu-id="86a58-131">**Mostra** imposta automaticamente il client attivo di input.</span><span class="sxs-lookup"><span data-stu-id="86a58-131">**Show** automatically sets the input-active client.</span></span> <span data-ttu-id="86a58-132">Quando il carattere è nascosto, la chiamata di **attivazione** potrebbe non riuscire se viene elaborata prima del completamento del metodo **show** .</span><span class="sxs-lookup"><span data-stu-id="86a58-132">When the character is hidden, the **Activate** call may fail, if it gets processed before the **Show** method completes.</span></span>

<span data-ttu-id="86a58-133">Il tentativo di chiamare questo metodo con il parametro **state** impostato su 2 (quando il carattere specificato è nascosto) avrà esito negativo.</span><span class="sxs-lookup"><span data-stu-id="86a58-133">Attempting to call this method with the **State** parameter set to 2 (when the specified character is hidden) will fail.</span></span> <span data-ttu-id="86a58-134">Analogamente, se si imposta **lo stato** su 0 e l'applicazione è l'unico client, la chiamata avrà esito negativo.</span><span class="sxs-lookup"><span data-stu-id="86a58-134">Similarly, if you set **State** to 0, and your application is the only client, this call fails.</span></span> <span data-ttu-id="86a58-135">Un carattere deve sempre avere un client in primo piano.</span><span class="sxs-lookup"><span data-stu-id="86a58-135">A character must always have a topmost client.</span></span>

> [!Note]  
> <span data-ttu-id="86a58-136">La chiamata a questo metodo con **lo stato** impostato su 1 non genera in genere un evento [**AgentNotifySink:: ActivateInputState**](https://www.bing.com/search?q=**AgentNotifySink::ActivateInputState**) a meno che non ci siano altri caratteri caricati o che l'applicazione sia già di input-Active.</span><span class="sxs-lookup"><span data-stu-id="86a58-136">Calling this method with **State** set to 1 does not typically generate an [**AgentNotifySink::ActivateInputState**](https://www.bing.com/search?q=**AgentNotifySink::ActivateInputState**) event unless there are no other characters loaded or your application is already input-active.</span></span>

 

## <a name="see-also"></a><span data-ttu-id="86a58-137">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="86a58-137">See Also</span></span>

[<span data-ttu-id="86a58-138">**IAgentCharacter::HasOtherClients**</span><span class="sxs-lookup"><span data-stu-id="86a58-138">**IAgentCharacter::HasOtherClients**</span></span>](iagentcharacter--hasotherclients.md)


 

 




