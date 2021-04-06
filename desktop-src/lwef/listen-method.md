---
title: Listen (metodo)
description: Listen (metodo)
ms.assetid: ceb3b62f-2a33-4a13-b608-4cfa800be38a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6813fb155074c4cc47a51ec7241eddd332edbcc3
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "104046615"
---
# <a name="listen-method"></a><span data-ttu-id="11b0f-103">Listen (metodo)</span><span class="sxs-lookup"><span data-stu-id="11b0f-103">Listen Method</span></span>

<span data-ttu-id="11b0f-104">\[Microsoft Agent è stato deprecato a partire da Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="11b0f-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="11b0f-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descrizione**</span><span class="sxs-lookup"><span data-stu-id="11b0f-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="11b0f-106">Attiva la modalità di ascolto (riconoscimento vocale) per un periodo di tempo.</span><span class="sxs-lookup"><span data-stu-id="11b0f-106">Turns on Listening mode (speech recognition) for a timed period.</span></span>

</dd> <dt>

<span data-ttu-id="11b0f-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintassi**</span><span class="sxs-lookup"><span data-stu-id="11b0f-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="11b0f-108">\*agente. ***Caratteri \* \* \* \* ("*** CharacterID \* \* *").* \*  *Stato* ascolto</span><span class="sxs-lookup"><span data-stu-id="11b0f-108">*agent.\*\*\*Characters\*\*\*\*("*\*\* CharacterID\***").Listen** *State*</span></span>



| <span data-ttu-id="11b0f-109">Parte</span><span class="sxs-lookup"><span data-stu-id="11b0f-109">Part</span></span>    | <span data-ttu-id="11b0f-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="11b0f-110">Description</span></span>                                                                                                                                                                      |
|---------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="11b0f-111">*State*</span><span class="sxs-lookup"><span data-stu-id="11b0f-111">*State*</span></span> | <span data-ttu-id="11b0f-112">Obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="11b0f-112">Required.</span></span> <span data-ttu-id="11b0f-113">Valore booleano che determina se attivare o disattivare la modalità di ascolto.</span><span class="sxs-lookup"><span data-stu-id="11b0f-113">A Boolean value that determines whether to turn Listening mode on or off.</span></span> <span data-ttu-id="11b0f-114">Valore **true** Attiva la modalità di ascolto.</span><span class="sxs-lookup"><span data-stu-id="11b0f-114">**True** Turns Listening mode on.</span></span> <br/> <span data-ttu-id="11b0f-115">**False** Disattiva la modalità di ascolto.</span><span class="sxs-lookup"><span data-stu-id="11b0f-115">**False** Turns Listening mode off.</span></span><br/> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="11b0f-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="11b0f-116">Remarks</span></span>

<span data-ttu-id="11b0f-117">L'impostazione di questo metodo su **true** Abilita la modalità di ascolto (attiva il riconoscimento vocale) per un periodo di tempo fisso (10 secondi).</span><span class="sxs-lookup"><span data-stu-id="11b0f-117">Setting this method to **True** enables Listening mode (turns on speech recognition) for a fixed period of time (10 seconds).</span></span> <span data-ttu-id="11b0f-118">Anche se non è possibile impostare il valore del timeout, è possibile disattivare la modalità di ascolto prima della scadenza del timeout.</span><span class="sxs-lookup"><span data-stu-id="11b0f-118">While you cannot set the value of the time-out, you can turn off Listening mode before the time-out expires.</span></span> <span data-ttu-id="11b0f-119">Se un utente (o un altro client) ha impostato correttamente la modalità di ascolto e si tenta di impostare questa proprietà su **true** prima della scadenza del timeout, il metodo ha esito positivo e reimposta il timeout. Tuttavia, se la modalità di ascolto è attiva perché l'utente preme il tasto ascolto, il metodo ha esito positivo, ma il timeout viene ignorato e la modalità di ascolto termina in base all'interazione dell'utente con la chiave di ascolto.</span><span class="sxs-lookup"><span data-stu-id="11b0f-119">If you (or another client) successfully set Listening mode on and you attempt to set this property to **True** before the time-out expires, the method succeeds and resets the time-out. However, if the Listening mode is on because the user is pressing the Listening key, the method succeeds, but the time-out is ignored and the Listening mode ends based on the user's interaction with the Listening key.</span></span>

<span data-ttu-id="11b0f-120">Questo metodo ha esito positivo solo quando viene chiamato dal client di input-attivo e se i servizi di riconoscimento vocale sono stati avviati.</span><span class="sxs-lookup"><span data-stu-id="11b0f-120">This method succeeds only when called by the input-active client and if speech services have been started.</span></span> <span data-ttu-id="11b0f-121">Per assicurarsi che i servizi di riconoscimento vocale siano stati avviati, eseguire una query o impostare il [**SRModeID**](srmodeid-property.md) o impostare l'impostazione [**Voice**](voice-property.md) per un [**comando**](/windows/desktop/lwef/the-command-object) prima di chiamare **Listen** altrimenti il metodo avrà esito negativo.</span><span class="sxs-lookup"><span data-stu-id="11b0f-121">To ensure that speech services have been started, query or set the [**SRModeID**](srmodeid-property.md) or set the [**Voice**](voice-property.md) setting for a [**Command**](/windows/desktop/lwef/the-command-object) before you call **Listen** otherwise the method will fail.</span></span> <span data-ttu-id="11b0f-122">Per rilevare l'esito positivo di questo metodo, chiamarlo come funzione e restituirà un valore booleano che indica se il metodo ha avuto esito positivo.</span><span class="sxs-lookup"><span data-stu-id="11b0f-122">To detect the success of this method, call it as a function and it will return a Boolean value indicating whether the method succeeded.</span></span>


```
   If Genie.Listen(True) Then
      'The method succeeded

   Else
      ' The method failed

   End If
```



<span data-ttu-id="11b0f-123">Il metodo ha esito negativo anche se l'utente preme il tasto di attesa e si tenta di impostare **Listen** su **false**.</span><span class="sxs-lookup"><span data-stu-id="11b0f-123">The method also fails if the user is pressing the Listening key and you attempt to set **Listen** to **False**.</span></span> <span data-ttu-id="11b0f-124">Tuttavia, se l'utente ha rilasciato il tasto ascolto e la modalità di ascolto non è scaduta, l'operazione avrà esito positivo.</span><span class="sxs-lookup"><span data-stu-id="11b0f-124">However, if the user has released the Listening key and Listening mode has not timed out, it will succeed.</span></span>

<span data-ttu-id="11b0f-125">**Listen** ha esito negativo anche se non è disponibile un motore vocale compatibile che corrisponda all'impostazione [**LanguageID**](languageid-property.md) del carattere, l'utente ha disabilitato l'input vocale usando la finestra delle proprietà di Microsoft Agent oppure il dispositivo audio è occupato.</span><span class="sxs-lookup"><span data-stu-id="11b0f-125">**Listen** also fails if there is no compatible speech engine available that matches the character's [**LanguageID**](languageid-property.md) setting, the user has disabled speech input using the Microsoft Agent property sheet, or the audio device is busy.</span></span>

<span data-ttu-id="11b0f-126">Quando si imposta correttamente questo metodo su **true**, il server attiva l'evento [**ListenStart**](listenstart-event.md) .</span><span class="sxs-lookup"><span data-stu-id="11b0f-126">When you successfully set this method to **True**, the server triggers the [**ListenStart**](listenstart-event.md) event.</span></span> <span data-ttu-id="11b0f-127">Il server invia [**ListenComplete**](listencomplete-event.md) quando il timeout della modalità di ascolto viene completato o quando si imposta **Listen** su **false**.</span><span class="sxs-lookup"><span data-stu-id="11b0f-127">The server sends [**ListenComplete**](listencomplete-event.md) when the Listening mode time-out completes or when you set **Listen** to **False**.</span></span>

<span data-ttu-id="11b0f-128">Questo metodo non chiama automaticamente [**Interrompi**](stop-method.md) e riproduce un'animazione dello stato di ascolto come il server quando viene premuto il tasto di attesa.</span><span class="sxs-lookup"><span data-stu-id="11b0f-128">This method does not automatically call [**Stop**](stop-method.md) and play a Listening state animation as the server does when the Listening key is pressed.</span></span> <span data-ttu-id="11b0f-129">Questo consente di determinare se interrompere l'animazione corrente usando l'animazione [**ListenStart**](listenstart-event.md) chiamando **Interrompi** e riproducendo un'animazione appropriata.</span><span class="sxs-lookup"><span data-stu-id="11b0f-129">This enables you to determine whether to interrupt the current animation using the [**ListenStart**](listenstart-event.md) animation by calling **Stop** and playing your own appropriate animation.</span></span> <span data-ttu-id="11b0f-130">Tuttavia, il server chiama **Stop** e riproduce un'animazione dello stato di udito quando viene rilevata un'espressione utente.</span><span class="sxs-lookup"><span data-stu-id="11b0f-130">However, the server does call **Stop** and plays a Hearing state animation when a user utterance is detected.</span></span>

## <a name="see-also"></a><span data-ttu-id="11b0f-131">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="11b0f-131">See Also</span></span>

<span data-ttu-id="11b0f-132">[**Proprietà LanguageID**](languageid-property.md), [**evento ListenComplete**](listencomplete-event.md), [**evento ListenStart**](listenstart-event.md)</span><span class="sxs-lookup"><span data-stu-id="11b0f-132">[**LanguageID property**](languageid-property.md), [**ListenComplete event**](listencomplete-event.md), [**ListenStart event**](listenstart-event.md)</span></span>


 

