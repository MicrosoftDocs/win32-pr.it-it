---
title: IAgentCharacterEx ascolto
description: IAgentCharacterEx ascolto
ms.assetid: 8d4cdb6c-04e1-498c-867f-fddbe6e2791a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 12c479936a8d2dc43e2f2da5a680a51705af2885
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104330695"
---
# <a name="iagentcharacterexlisten"></a><span data-ttu-id="39b7a-103">IAgentCharacterEx:: Listen</span><span class="sxs-lookup"><span data-stu-id="39b7a-103">IAgentCharacterEx::Listen</span></span>

<span data-ttu-id="39b7a-104">\[Microsoft Agent è stato deprecato a partire da Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="39b7a-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT Listen(
   long bListen  // listening mode flag
);
```

<span data-ttu-id="39b7a-105">Attiva o disattiva la modalità di ascolto (input riconoscimento vocale).</span><span class="sxs-lookup"><span data-stu-id="39b7a-105">Turns Listening mode (speech recognition input) on or off.</span></span>

-   <span data-ttu-id="39b7a-106">Restituisce \_ OK per indicare che l'operazione è stata completata.</span><span class="sxs-lookup"><span data-stu-id="39b7a-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="39b7a-107"><span id="bListen"></span><span id="blisten"></span><span id="BLISTEN"></span>*bListen*</span><span class="sxs-lookup"><span data-stu-id="39b7a-107"><span id="bListen"></span><span id="blisten"></span><span id="BLISTEN"></span>*bListen*</span></span>
</dt> <dd>

<span data-ttu-id="39b7a-108">Flag modalità di ascolto.</span><span class="sxs-lookup"><span data-stu-id="39b7a-108">Listening mode flag.</span></span> <span data-ttu-id="39b7a-109">Se questo parametro è **true**, la modalità di ascolto è attivata; Se **false**, la modalità di ascolto è disattivata.</span><span class="sxs-lookup"><span data-stu-id="39b7a-109">If this parameter is **True**, the Listening mode is turned on; if **False**, Listening mode is turned off.</span></span>

</dd> </dl>

<span data-ttu-id="39b7a-110">L'impostazione di questo metodo su **true** Abilita la modalità di ascolto (attiva il riconoscimento vocale) per un periodo di tempo fisso.</span><span class="sxs-lookup"><span data-stu-id="39b7a-110">Setting this method to **True** enables the Listening mode (turns on speech recognition) for a fixed period of time.</span></span> <span data-ttu-id="39b7a-111">Anche se non è possibile impostare il valore del timeout, è possibile disattivare la modalità di ascolto prima della scadenza del timeout.</span><span class="sxs-lookup"><span data-stu-id="39b7a-111">While you cannot set the value of the time-out, you can turn off Listening mode before the time-out expires.</span></span> <span data-ttu-id="39b7a-112">Inoltre, se la modalità di ascolto è già attiva perché l'utente (o un altro client) ha impostato correttamente il metodo su **true** prima della scadenza del timeout, il metodo ha esito positivo e reimposta il timeout. Tuttavia, se la modalità di ascolto è già attiva perché l'utente preme il tasto ascolto, il metodo ha esito positivo, ma il timeout viene ignorato e la modalità di ascolto termina in base all'interazione dell'utente con la chiave di ascolto.</span><span class="sxs-lookup"><span data-stu-id="39b7a-112">In addition, if the Listening mode is already on because you (or another client) successfully set the method to **True** before the time-out expires, the method succeeds and resets the time-out. However, if Listening mode is already on because the user is pressing the Listening key, the method succeeds, but the time-out is ignored and the Listening mode ends based on the user's interaction with the Listening key.</span></span>

<span data-ttu-id="39b7a-113">Questo metodo avrà esito positivo solo quando viene chiamato dal client attivo di input.</span><span class="sxs-lookup"><span data-stu-id="39b7a-113">This method will succeed only when called by the input-active client.</span></span> <span data-ttu-id="39b7a-114">Pertanto, il metodo avrà esito negativo se il client non è il client attivo del carattere di primo livello.</span><span class="sxs-lookup"><span data-stu-id="39b7a-114">Therefore, the method will fail if your client is not the active client of the topmost character.</span></span> <span data-ttu-id="39b7a-115">Il metodo avrà esito negativo anche se si tenta di impostare il metodo su **false** e l'utente preme il tasto di attesa.</span><span class="sxs-lookup"><span data-stu-id="39b7a-115">The method will also fail if you attempt to set the method to **False** and the user is pressing the Listening key.</span></span> <span data-ttu-id="39b7a-116">Può inoltre avere esito negativo se non è disponibile un motore vocale compatibile che corrisponda all'impostazione dell'ID lingua del carattere o se l'utente ha disabilitato l'input vocale usando la finestra delle proprietà di Microsoft Agent.</span><span class="sxs-lookup"><span data-stu-id="39b7a-116">It can also fail if there is no compatible speech engine available that matches the character's language ID setting or the user has disabled speech input using the Microsoft Agent property sheet.</span></span> <span data-ttu-id="39b7a-117">Tuttavia, il metodo non avrà esito negativo se il dispositivo audio è occupato.</span><span class="sxs-lookup"><span data-stu-id="39b7a-117">However, the method will not fail if the audio device is busy.</span></span>

<span data-ttu-id="39b7a-118">Quando si imposta correttamente questo metodo su **true**, il server attiva l'evento [**IAgentNotifySinkEx:: ListeningState**](iagentnotifysinkex--listeningstate.md) .</span><span class="sxs-lookup"><span data-stu-id="39b7a-118">When you successfully set this method to **True**, the server triggers the [**IAgentNotifySinkEx::ListeningState**](iagentnotifysinkex--listeningstate.md) event.</span></span> <span data-ttu-id="39b7a-119">Il server invia anche **IAgentNotifySinkEx:: ListeningState** al termine del timeout della modalità di ascolto o quando si imposta [**IAgentCharacterEx:: Listen**](https://www.bing.com/search?q=**IAgentCharacterEx::Listen**) su **false**.</span><span class="sxs-lookup"><span data-stu-id="39b7a-119">The server also sends **IAgentNotifySinkEx::ListeningState** when the Listening mode time-out completes or when you set [**IAgentCharacterEx::Listen**](https://www.bing.com/search?q=**IAgentCharacterEx::Listen**) to **False**.</span></span>

<span data-ttu-id="39b7a-120">Questo metodo non chiama automaticamente [**IAgentCharacter:: stopAll**](iagentcharacter--stopall.md) e riproduce un'animazione dello stato di ascolto del carattere come si verifica quando l'utente preme il tasto di attesa.</span><span class="sxs-lookup"><span data-stu-id="39b7a-120">This method does not automatically call [**IAgentCharacter::StopAll**](iagentcharacter--stopall.md) and play a Listening state animation of the character as occurs when the user presses the Listening key.</span></span> <span data-ttu-id="39b7a-121">Questo consente di usare l'evento [**IAgentNotifySinkEx:: ListeningState**](iagentnotifysinkex--listeningstate.md) per determinare se si vuole arrestare l'animazione corrente e riprodurre un'animazione appropriata.</span><span class="sxs-lookup"><span data-stu-id="39b7a-121">This enables you to use the [**IAgentNotifySinkEx::ListeningState**](iagentnotifysinkex--listeningstate.md) event to determine whether you wish to stop the current animation and play your own appropriate animation.</span></span> <span data-ttu-id="39b7a-122">Tuttavia, una volta rilevato un enunciato utente, il server chiama automaticamente **IAgentCharacter:: stopAll** e riproduce un'animazione dello stato di udito.</span><span class="sxs-lookup"><span data-stu-id="39b7a-122">However, once a user utterance is detected, the server automatically calls **IAgentCharacter::StopAll** and plays a Hearing state animation.</span></span>

## <a name="see-also"></a><span data-ttu-id="39b7a-123">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="39b7a-123">See Also</span></span>

<span data-ttu-id="39b7a-124">[**IAgentNotifySinkEx:: ListeningState**](iagentnotifysinkex--listeningstate.md), [ **IAgentSpeechInputProperties:: GetEnabled**](iagentspeechinputproperties--getenabled.md)</span><span class="sxs-lookup"><span data-stu-id="39b7a-124">[**IAgentNotifySinkEx::ListeningState**](iagentnotifysinkex--listeningstate.md), [**IAgentSpeechInputProperties::GetEnabled**](iagentspeechinputproperties--getenabled.md)</span></span>


 

 




