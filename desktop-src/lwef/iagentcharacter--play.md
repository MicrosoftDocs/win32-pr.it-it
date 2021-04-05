---
title: IAgentCharacter Play
description: IAgentCharacter Play
ms.assetid: a0158693-ff62-4da4-8b68-402e8d5b1c2a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 996929271156254377f08b9fc41da3932aee9da4
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104045402"
---
# <a name="iagentcharacterplay"></a><span data-ttu-id="a3029-103">IAgentCharacter::P lay</span><span class="sxs-lookup"><span data-stu-id="a3029-103">IAgentCharacter::Play</span></span>

<span data-ttu-id="a3029-104">\[Microsoft Agent è stato deprecato a partire da Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="a3029-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT Play(
   BSTR bszAnimation,  // name of an animation
   long * pdwReqID     // address of request ID
);
```

<span data-ttu-id="a3029-105">Riproduce l'animazione specificata.</span><span class="sxs-lookup"><span data-stu-id="a3029-105">Plays the specified animation.</span></span>

-   <span data-ttu-id="a3029-106">Restituisce \_ OK per indicare che l'operazione è stata completata.</span><span class="sxs-lookup"><span data-stu-id="a3029-106">Returns S\_OK to indicate the operation was successful.</span></span> <span data-ttu-id="a3029-107">Quando la funzione restituisce, *pdwReqID* contiene l'ID della richiesta.</span><span class="sxs-lookup"><span data-stu-id="a3029-107">When the function returns, *pdwReqID* contains the ID of the request.</span></span>

<dl> <dt>

<span data-ttu-id="a3029-108"><span id="bszAnimation"></span><span id="bszanimation"></span><span id="BSZANIMATION"></span>*bszAnimation*</span><span class="sxs-lookup"><span data-stu-id="a3029-108"><span id="bszAnimation"></span><span id="bszanimation"></span><span id="BSZANIMATION"></span>*bszAnimation*</span></span>
</dt> <dd>

<span data-ttu-id="a3029-109">Nome di un'animazione.</span><span class="sxs-lookup"><span data-stu-id="a3029-109">The name of an animation.</span></span>

</dd> <dt>

<span data-ttu-id="a3029-110"><span id="pdwReqID"></span><span id="pdwreqid"></span><span id="PDWREQID"></span>*pdwReqID*</span><span class="sxs-lookup"><span data-stu-id="a3029-110"><span id="pdwReqID"></span><span id="pdwreqid"></span><span id="PDWREQID"></span>*pdwReqID*</span></span>
</dt> <dd>

<span data-ttu-id="a3029-111">Indirizzo di una variabile che riceve l'ID richiesta **IAgentCharacter::P Lay** .</span><span class="sxs-lookup"><span data-stu-id="a3029-111">Address of a variable that receives the **IAgentCharacter::Play** request ID.</span></span>

</dd> </dl>

<span data-ttu-id="a3029-112">Il nome di un'animazione viene definito quando il carattere viene compilato con l'editor dei caratteri di Microsoft Agent.</span><span class="sxs-lookup"><span data-stu-id="a3029-112">An animation's name is defined when the character is compiled with the Microsoft Agent Character Editor.</span></span> <span data-ttu-id="a3029-113">Prima di riprodurre l'animazione specificata, il server tenta di riprodurre l'animazione **restituita** per l'animazione precedente (se ne è stata assegnata una).</span><span class="sxs-lookup"><span data-stu-id="a3029-113">Before playing the specified animation, the server attempts to play the **Return** animation for the previous animation (if one has been assigned).</span></span>

<span data-ttu-id="a3029-114">Quando i dati di animazione di un carattere vengono archiviati nel computer locale dell'utente, è possibile usare il metodo **IAgentCharacter::P Lay** e specificare il nome dell'animazione.</span><span class="sxs-lookup"><span data-stu-id="a3029-114">When a character's animation data is stored on the user's local machine, you can use the **IAgentCharacter::Play** method and specify the name of the animation.</span></span> <span data-ttu-id="a3029-115">Quando si utilizza il protocollo HTTP per accedere ai dati di animazione, utilizzare il metodo [**Prepare**](iagentcharacter--prepare.md) per garantire la disponibilità dell'animazione prima di chiamare questo metodo.</span><span class="sxs-lookup"><span data-stu-id="a3029-115">When using the HTTP protocol to access animation data, use the [**Prepare**](iagentcharacter--prepare.md) method to ensure the availability of the animation before calling this method.</span></span>

## <a name="see-also"></a><span data-ttu-id="a3029-116">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="a3029-116">See Also</span></span>

[<span data-ttu-id="a3029-117">**IAgentCharacter::P ripare**</span><span class="sxs-lookup"><span data-stu-id="a3029-117">**IAgentCharacter::Prepare**</span></span>](iagentcharacter--prepare.md)


 

 




