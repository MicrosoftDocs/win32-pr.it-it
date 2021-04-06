---
title: Nascondi IAgentCharacter
description: Nascondi IAgentCharacter
ms.assetid: a8128fe8-9a3b-41a3-bfe3-82ace1baff6f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9bcd0ef91eb4d2738f19fb594ac1ab186efaec6e
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "104046667"
---
# <a name="iagentcharacterhide"></a><span data-ttu-id="f9ec1-103">IAgentCharacter:: Hide</span><span class="sxs-lookup"><span data-stu-id="f9ec1-103">IAgentCharacter::Hide</span></span>

<span data-ttu-id="f9ec1-104">\[Microsoft Agent è stato deprecato a partire da Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="f9ec1-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT Hide(
   long bFast,      // play Hiding state animation flag
   long * pdwReqID  // address of request ID
);
```

<span data-ttu-id="f9ec1-105">Nasconde il carattere.</span><span class="sxs-lookup"><span data-stu-id="f9ec1-105">Hides the character.</span></span>

-   <span data-ttu-id="f9ec1-106">Restituisce \_ OK per indicare che l'operazione è stata completata.</span><span class="sxs-lookup"><span data-stu-id="f9ec1-106">Returns S\_OK to indicate the operation was successful.</span></span> <span data-ttu-id="f9ec1-107">Quando la funzione restituisce, *pdwReqID* contiene l'ID della richiesta.</span><span class="sxs-lookup"><span data-stu-id="f9ec1-107">When the function returns, *pdwReqID* contains the ID of the request.</span></span>

<dl> <dt>

<span data-ttu-id="f9ec1-108"><span id="bFast"></span><span id="bfast"></span><span id="BFAST"></span>*bFast*</span><span class="sxs-lookup"><span data-stu-id="f9ec1-108"><span id="bFast"></span><span id="bfast"></span><span id="BFAST"></span>*bFast*</span></span>
</dt> <dd>

<span data-ttu-id="f9ec1-109">Flag animazione stato **nascosto** .</span><span class="sxs-lookup"><span data-stu-id="f9ec1-109">**Hiding** state animation flag.</span></span> <span data-ttu-id="f9ec1-110">Se questo parametro è **true**, l'animazione **nascosta** non viene riprodotto prima che il frame di caratteri sia nascosto; Se **false**, l'animazione viene riprodotta.</span><span class="sxs-lookup"><span data-stu-id="f9ec1-110">If this parameter is **True**, the **Hiding** animation does not play before the character frame is hidden; if **False**, the animation plays.</span></span>

</dd> <dt>

<span data-ttu-id="f9ec1-111"><span id="pdwReqID"></span><span id="pdwreqid"></span><span id="PDWREQID"></span>*pdwReqID*</span><span class="sxs-lookup"><span data-stu-id="f9ec1-111"><span id="pdwReqID"></span><span id="pdwreqid"></span><span id="PDWREQID"></span>*pdwReqID*</span></span>
</dt> <dd>

<span data-ttu-id="f9ec1-112">Indirizzo di una variabile che riceve l'ID richiesta **Hide** .</span><span class="sxs-lookup"><span data-stu-id="f9ec1-112">Address of a variable that receives the **Hide** request ID.</span></span>

</dd> </dl>

<span data-ttu-id="f9ec1-113">Il server accoda l'animazione associata al metodo **Hide** nella coda del carattere.</span><span class="sxs-lookup"><span data-stu-id="f9ec1-113">The server queues the animation associated with the **Hide** method in the character's queue.</span></span> <span data-ttu-id="f9ec1-114">In questo modo è possibile usarlo per nascondere il carattere dopo una sequenza di altre animazioni.</span><span class="sxs-lookup"><span data-stu-id="f9ec1-114">This allows you to use it to hide the character after a sequence of other animations.</span></span> <span data-ttu-id="f9ec1-115">È possibile riprodurre l'azione immediatamente usando il metodo [**Stop**](iagentcharacter--stop.md) prima di chiamare il metodo **Hide** .</span><span class="sxs-lookup"><span data-stu-id="f9ec1-115">You can play the action immediately by using the [**Stop**](iagentcharacter--stop.md) method before calling the **Hide** method.</span></span>

<span data-ttu-id="f9ec1-116">Quando si utilizza il protocollo HTTP per accedere ai dati di tipo carattere e animazione, utilizzare il metodo [**Prepare**](/windows/desktop/lwef/iagentcharacter--prepare) per garantire la disponibilità dell'animazione dello stato di **occultamento** prima di chiamare questo metodo.</span><span class="sxs-lookup"><span data-stu-id="f9ec1-116">When using the HTTP protocol to access character and animation data, use the [**Prepare**](/windows/desktop/lwef/iagentcharacter--prepare) method to ensure the availability of the **Hiding** state animation before calling this method.</span></span>

<span data-ttu-id="f9ec1-117">Nascondere un carattere può anche causare l'attivazione dell'evento [**IAgentNotifySink:: ActivateInputState**](iagentnotifysink--activateinputstate.md) di un altro carattere visibile.</span><span class="sxs-lookup"><span data-stu-id="f9ec1-117">Hiding a character can also result in triggering the [**IAgentNotifySink::ActivateInputState**](iagentnotifysink--activateinputstate.md) event of another visible character.</span></span>

<span data-ttu-id="f9ec1-118">I caratteri nascosti non possono accedere al canale audio.</span><span class="sxs-lookup"><span data-stu-id="f9ec1-118">Hidden characters cannot access the audio channel.</span></span> <span data-ttu-id="f9ec1-119">Il server restituirà uno stato di errore nell'evento [**RequestComplete**](iagentnotifysink--requestcomplete.md) se si genera una richiesta di animazione e il carattere è nascosto.</span><span class="sxs-lookup"><span data-stu-id="f9ec1-119">The server will pass back a failure status in the [**RequestComplete**](iagentnotifysink--requestcomplete.md) event if you generate an animation request and the character is hidden.</span></span>

## <a name="see-also"></a><span data-ttu-id="f9ec1-120">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="f9ec1-120">See Also</span></span>

[<span data-ttu-id="f9ec1-121">**IAgentCharacter:: Show**</span><span class="sxs-lookup"><span data-stu-id="f9ec1-121">**IAgentCharacter::Show**</span></span>](iagentcharacter--show.md)


 

 