---
title: IAgentCharacter interrupt
description: IAgentCharacter interrupt
ms.assetid: ae05d317-e2d9-4d11-a6df-f9b25e43467a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 17c9f19f716b15a48ec3cdb064aa4c0fdbbd1774
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "103956360"
---
# <a name="iagentcharacterinterrupt"></a><span data-ttu-id="fc3b7-103">IAgentCharacter:: interrupt</span><span class="sxs-lookup"><span data-stu-id="fc3b7-103">IAgentCharacter::Interrupt</span></span>

<span data-ttu-id="fc3b7-104">\[Microsoft Agent è stato deprecato a partire da Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="fc3b7-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT Interrupt(
   long dwReqID,    // request ID to interrupt
   long * pdwReqID  // address of request ID
);
```

<span data-ttu-id="fc3b7-105">Interrompe l'animazione (richiesta) specificata di un altro carattere.</span><span class="sxs-lookup"><span data-stu-id="fc3b7-105">Interrupts the specified animation (request) of another character.</span></span>

-   <span data-ttu-id="fc3b7-106">Restituisce \_ OK per indicare che l'operazione è stata completata.</span><span class="sxs-lookup"><span data-stu-id="fc3b7-106">Returns S\_OK to indicate the operation was successful.</span></span> <span data-ttu-id="fc3b7-107">Quando la funzione restituisce, *pdwReqID* contiene l'ID della richiesta.</span><span class="sxs-lookup"><span data-stu-id="fc3b7-107">When the function returns, *pdwReqID* contains the ID of the request.</span></span>

<dl> <dt>

<span data-ttu-id="fc3b7-108"><span id="dwReqID"></span><span id="dwreqid"></span><span id="DWREQID"></span>*dwReqID*</span><span class="sxs-lookup"><span data-stu-id="fc3b7-108"><span id="dwReqID"></span><span id="dwreqid"></span><span id="DWREQID"></span>*dwReqID*</span></span>
</dt> <dd>

<span data-ttu-id="fc3b7-109">ID della richiesta da interrompere.</span><span class="sxs-lookup"><span data-stu-id="fc3b7-109">An ID of the request to interrupt.</span></span>

</dd> <dt>

<span data-ttu-id="fc3b7-110"><span id="pdwReqID"></span><span id="pdwreqid"></span><span id="PDWREQID"></span>*pdwReqID*</span><span class="sxs-lookup"><span data-stu-id="fc3b7-110"><span id="pdwReqID"></span><span id="pdwreqid"></span><span id="PDWREQID"></span>*pdwReqID*</span></span>
</dt> <dd>

<span data-ttu-id="fc3b7-111">Indirizzo di una variabile che riceve l'ID della richiesta di **interrupt** .</span><span class="sxs-lookup"><span data-stu-id="fc3b7-111">Address of a variable that receives the **Interrupt** request ID.</span></span>

</dd> </dl>

<span data-ttu-id="fc3b7-112">Se si caricano più caratteri, è possibile usare questo metodo per sincronizzare l'animazione tra i caratteri.</span><span class="sxs-lookup"><span data-stu-id="fc3b7-112">If you load multiple characters, you can use this method to sync up animation between characters.</span></span> <span data-ttu-id="fc3b7-113">Se, ad esempio, un altro carattere si trova in un'animazione di ciclo, questo metodo arresterà l'animazione di ciclo e avvierà l'animazione successiva nella coda del carattere.</span><span class="sxs-lookup"><span data-stu-id="fc3b7-113">For example, if another character is in a looping animation, this method will stop the looping animation and start the next animation in the character's queue.</span></span>

<span data-ttu-id="fc3b7-114">**Interrupt interrompe** l'animazione esistente, ma non Scarica la coda di animazione del carattere.</span><span class="sxs-lookup"><span data-stu-id="fc3b7-114">**Interrupt** halts the existing animation, but does not flush the character's animation queue.</span></span> <span data-ttu-id="fc3b7-115">Viene avviata l'animazione successiva nella coda del carattere.</span><span class="sxs-lookup"><span data-stu-id="fc3b7-115">It starts the next animation in the character's queue.</span></span> <span data-ttu-id="fc3b7-116">Per arrestare e scaricare la coda di un carattere, usare il metodo [**Stop**](/windows/desktop/lwef/iagentcharacter--stop) .</span><span class="sxs-lookup"><span data-stu-id="fc3b7-116">To halt and flush a character's queue, use the [**Stop**](/windows/desktop/lwef/iagentcharacter--stop) method.</span></span>

<span data-ttu-id="fc3b7-117">Non è possibile usare questo metodo per avere un interrupt di tipo carattere, perché il server Microsoft Agent Accoda il metodo **interrupt** nella coda di animazione del carattere.</span><span class="sxs-lookup"><span data-stu-id="fc3b7-117">You cannot use this method to have a character interrupt itself because the Microsoft Agent server queues the **Interrupt** method in the character's animation queue.</span></span> <span data-ttu-id="fc3b7-118">Pertanto, è possibile utilizzare solo **interrupt** per arrestare l'animazione di un altro carattere caricato.</span><span class="sxs-lookup"><span data-stu-id="fc3b7-118">Therefore, you can only use **Interrupt** to halt the animation of another character you have loaded.</span></span>

 

 