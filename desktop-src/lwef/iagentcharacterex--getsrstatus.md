---
title: IAgentCharacterEx GetSRStatus
description: IAgentCharacterEx GetSRStatus
ms.assetid: ccb34108-8078-421a-a883-731b51fae179
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4396e325f5afba161046f2a001cebb29033d709b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104044528"
---
# <a name="iagentcharacterexgetsrstatus"></a><span data-ttu-id="d10e4-103">IAgentCharacterEx::GetSRStatus</span><span class="sxs-lookup"><span data-stu-id="d10e4-103">IAgentCharacterEx::GetSRStatus</span></span>

<span data-ttu-id="d10e4-104">\[Microsoft Agent è stato deprecato a partire da Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="d10e4-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT GetSRStatus(
   long * plStatus  // address of the speech input status
);
```

<span data-ttu-id="d10e4-105">Recupera lo stato della condizione necessaria per supportare l'input vocale.</span><span class="sxs-lookup"><span data-stu-id="d10e4-105">Retrieves the status of the condition necessary to support speech input.</span></span>

-   <span data-ttu-id="d10e4-106">Restituisce \_ OK per indicare che l'operazione è stata completata.</span><span class="sxs-lookup"><span data-stu-id="d10e4-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="d10e4-107"><span id="plStatus"></span><span id="plstatus"></span><span id="PLSTATUS"></span>*plStatus*</span><span class="sxs-lookup"><span data-stu-id="d10e4-107"><span id="plStatus"></span><span id="plstatus"></span><span id="PLSTATUS"></span>*plStatus*</span></span>
</dt> <dd>

<span data-ttu-id="d10e4-108">Indirizzo di una variabile che riceve uno dei valori seguenti per l'impostazione dello stato:</span><span class="sxs-lookup"><span data-stu-id="d10e4-108">Address of a variable that receives one of the following values for the state setting:</span></span>



| <span data-ttu-id="d10e4-109">Valore</span><span class="sxs-lookup"><span data-stu-id="d10e4-109">Value</span></span>                                                                               | <span data-ttu-id="d10e4-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d10e4-110">Description</span></span>                                                                                                                                                                                                                               |
|-------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d10e4-111">**const unsigned long** **Listen \_ status \_ CANLISTEN = 0;**</span><span class="sxs-lookup"><span data-stu-id="d10e4-111">**const unsigned long** **LISTEN\_STATUS\_CANLISTEN = 0;**</span></span><br/>               | <span data-ttu-id="d10e4-112">Le condizioni supportano l'input vocale.</span><span class="sxs-lookup"><span data-stu-id="d10e4-112">Conditions support speech input.</span></span>                                                                                                                                                                                                          |
| <span data-ttu-id="d10e4-113">**const unsigned long** **Listen \_ status \_ noaudio = 1;**</span><span class="sxs-lookup"><span data-stu-id="d10e4-113">**const unsigned long** **LISTEN\_STATUS\_NOAUDIO = 1;**</span></span><br/>                 | <span data-ttu-id="d10e4-114">Nessun dispositivo di input audio disponibile nel sistema.</span><span class="sxs-lookup"><span data-stu-id="d10e4-114">There is no audio input device available on this system.</span></span> <span data-ttu-id="d10e4-115">Si noti che questo non rileva se un microfono è installato; può solo rilevare se l'utente dispone di una scheda audio abilitata per l'input correttamente installata con un driver funzionante.</span><span class="sxs-lookup"><span data-stu-id="d10e4-115">(Note that this does not detect whether a microphone is installed; it can only detect whether the user has a properly installed input-enabled sound card with a working driver.)</span></span> |
| <span data-ttu-id="d10e4-116">stato di ascolto **lungo senza segno const** **\_ \_ NOTTOPMOST = 2;**</span><span class="sxs-lookup"><span data-stu-id="d10e4-116">**const unsigned long** **LISTEN\_STATUS\_NOTTOPMOST = 2;**</span></span><br/>              | <span data-ttu-id="d10e4-117">Un altro client è il client attivo di questo carattere oppure il carattere corrente non è in primo piano.</span><span class="sxs-lookup"><span data-stu-id="d10e4-117">Another client is the active client of this character, or the current character is not topmost.</span></span>                                                                                                                                           |
| <span data-ttu-id="d10e4-118">**const unsigned long** **Listen \_ status \_ CANTOPENAUDIO = 3;**</span><span class="sxs-lookup"><span data-stu-id="d10e4-118">**const unsigned long** **LISTEN\_STATUS\_CANTOPENAUDIO = 3;**</span></span><br/>           | <span data-ttu-id="d10e4-119">Il canale di input o di output audio è attualmente occupato, altre applicazioni usano l'audio.</span><span class="sxs-lookup"><span data-stu-id="d10e4-119">The audio input or output channel is currently busy, some other application is using audio.</span></span>                                                                                                                                               |
| <span data-ttu-id="d10e4-120">**const unsigned long** **Listen \_ status \_ COULDNTINITIALIZESPEECH = 4;**</span><span class="sxs-lookup"><span data-stu-id="d10e4-120">**const unsigned long** **LISTEN\_STATUS\_COULDNTINITIALIZESPEECH = 4;**</span></span><br/> | <span data-ttu-id="d10e4-121">Si è verificato un errore non specificato durante il processo di inizializzazione del sottosistema di riconoscimento vocale.</span><span class="sxs-lookup"><span data-stu-id="d10e4-121">An unspecified error occurred in the process of initializing the speech recognition subsystem.</span></span> <span data-ttu-id="d10e4-122">Ciò include la possibilità che non sia disponibile un motore di riconoscimento vocale corrispondente all'impostazione della lingua del carattere.</span><span class="sxs-lookup"><span data-stu-id="d10e4-122">This includes the possibility that there is no speech engine available matching the character's language setting.</span></span>                          |
| <span data-ttu-id="d10e4-123">**const unsigned long** **Listen \_ status \_ SPEECHDISABLED = 5;**</span><span class="sxs-lookup"><span data-stu-id="d10e4-123">**const unsigned long** **LISTEN\_STATUS\_SPEECHDISABLED = 5;**</span></span><br/>          | <span data-ttu-id="d10e4-124">L'utente ha disabilitato l'input vocale nella finestra Opzioni carattere avanzate.</span><span class="sxs-lookup"><span data-stu-id="d10e4-124">The user has disabled speech input in the Advanced Character Options window.</span></span>                                                                                                                                                              |
| <span data-ttu-id="d10e4-125">errore di stato di ascolto **Long senza segno const** **\_ \_ = 6;**</span><span class="sxs-lookup"><span data-stu-id="d10e4-125">**const unsigned long** **LISTEN\_STATUS\_ERROR = 6;**</span></span><br/>                   | <span data-ttu-id="d10e4-126">Si è verificato un errore durante il controllo dello stato dell'audio, ma la cause dell'errore non è stata restituita dal sistema.</span><span class="sxs-lookup"><span data-stu-id="d10e4-126">An error occurred in checking the audio status, but the cause of the error was not returned by the system.</span></span>                                                                                                                                |



 

</dd> </dl>

<span data-ttu-id="d10e4-127">Questa funzione consente di eseguire una query se le condizioni correnti supportano l'input di riconoscimento vocale, incluso lo stato del dispositivo audio.</span><span class="sxs-lookup"><span data-stu-id="d10e4-127">This function enables you to query whether current conditions support speech recognition input, including the status of the audio device.</span></span> <span data-ttu-id="d10e4-128">Se l'applicazione usa il metodo [**IAgentCharacterEx:: Listen**](iagentcharacterex--listen.md) , è possibile usare questa funzione per assicurarsi che la chiamata venga eseguita correttamente.</span><span class="sxs-lookup"><span data-stu-id="d10e4-128">If your application uses the [**IAgentCharacterEx::Listen**](iagentcharacterex--listen.md) method, you can use this function to better ensure that the call will succeed.</span></span> <span data-ttu-id="d10e4-129">La chiamata a questo metodo carica anche il motore vocale se non è già caricato.</span><span class="sxs-lookup"><span data-stu-id="d10e4-129">Calling this method also loads the speech engine if it is not already loaded.</span></span> <span data-ttu-id="d10e4-130">Tuttavia, non attiva la modalità di ascolto.</span><span class="sxs-lookup"><span data-stu-id="d10e4-130">However, it does not turn on Listening mode.</span></span>

<span data-ttu-id="d10e4-131">Quando l'input vocale è abilitato nella finestra delle proprietà dell'agente (Opzioni carattere avanzate), l'esecuzione di query sullo stato caricherà il motore associato (se non è già caricato) e avvierà servizi vocali.</span><span class="sxs-lookup"><span data-stu-id="d10e4-131">When speech input is enabled in the Agent property sheet (Advanced Character Options), querying the status will load the associated engine (if it is not already loaded), and start speech services.</span></span> <span data-ttu-id="d10e4-132">Ovvero, la chiave di ascolto è disponibile e il suggerimento di ascolto è visualizzabile.</span><span class="sxs-lookup"><span data-stu-id="d10e4-132">That is, the Listening key is available, and the Listening Tip is displayable.</span></span> <span data-ttu-id="d10e4-133">(Il tasto di attesa e il suggerimento di ascolto sono abilitati solo se sono abilitati anche nelle opzioni dei caratteri avanzati). Tuttavia, se si esegue una query sulla proprietà quando la voce Speech è disabilitata, il server non avvia i servizi di riconoscimento vocale.</span><span class="sxs-lookup"><span data-stu-id="d10e4-133">(The Listening key and Listening Tip are enabled only if they are also enabled in Advanced Character Options.) However, if you query the property when speech is disabled, the server does not start speech services.</span></span>

<span data-ttu-id="d10e4-134">Questa funzione restituisce solo l'impostazione per l'uso del carattere da parte dell'applicazione client. l'impostazione non riflette altri client del carattere o di altri caratteri dell'applicazione client.</span><span class="sxs-lookup"><span data-stu-id="d10e4-134">This function returns only the setting for your client application's use of the character; the setting does not reflect other clients of the character or other characters of your client application.</span></span>

 

 





