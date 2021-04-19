---
title: IAgentAudioOutputPropertiesEx GetStatus
description: IAgentAudioOutputPropertiesEx GetStatus
ms.assetid: 29bf1379-eebe-4b8b-b8d0-b86d2da78b64
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f851c8fc73e9f427bd725d7ef647b84a68be13e4
ms.sourcegitcommit: 59ec383331366f8a62c94bb88468ca03e95c43f8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/13/2021
ms.locfileid: "107380745"
---
# <a name="iagentaudiooutputpropertiesexgetstatus"></a><span data-ttu-id="cf9fa-103">IAgentAudioOutputPropertiesEx::GetStatus</span><span class="sxs-lookup"><span data-stu-id="cf9fa-103">IAgentAudioOutputPropertiesEx::GetStatus</span></span>

<span data-ttu-id="cf9fa-104">\[Microsoft Agent è deprecato a livello di Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="cf9fa-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT GetStatus(
   long * plStatus,  // address of audio channel status
);
```

<span data-ttu-id="cf9fa-105">Recupera lo stato del canale audio.</span><span class="sxs-lookup"><span data-stu-id="cf9fa-105">Retrieves the status of the audio channel.</span></span>

-   <span data-ttu-id="cf9fa-106">Restituisce S \_ OK per indicare che l'operazione è riuscita.</span><span class="sxs-lookup"><span data-stu-id="cf9fa-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="cf9fa-107"><span id="plStatus"></span><span id="plstatus"></span><span id="PLSTATUS"></span>*plStatus*</span><span class="sxs-lookup"><span data-stu-id="cf9fa-107"><span id="plStatus"></span><span id="plstatus"></span><span id="PLSTATUS"></span>*plStatus*</span></span>
</dt> <dd>

<span data-ttu-id="cf9fa-108">Stato del canale di output audio, che può essere uno dei valori seguenti:</span><span class="sxs-lookup"><span data-stu-id="cf9fa-108">Status of the audio output channel, which may be one of the following values:</span></span>



| <span data-ttu-id="cf9fa-109">Valore</span><span class="sxs-lookup"><span data-stu-id="cf9fa-109">Value</span></span>                                                                         | <span data-ttu-id="cf9fa-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="cf9fa-110">Description</span></span>                                                                                                    |
|-------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cf9fa-111">**const unsigned short** **AUDIO STATUS AVAILABLE = \_ \_ 0;**</span><span class="sxs-lookup"><span data-stu-id="cf9fa-111">**const unsigned short** **AUDIO\_STATUS\_AVAILABLE = 0;**</span></span><br/>         | <span data-ttu-id="cf9fa-112">Il canale di output audio è disponibile (non occupato).</span><span class="sxs-lookup"><span data-stu-id="cf9fa-112">The audio output channel is available (not busy).</span></span>                                                              |
| <span data-ttu-id="cf9fa-113">**const unsigned short** **AUDIO STATUS \_ \_ NOAUDIO = 1;**</span><span class="sxs-lookup"><span data-stu-id="cf9fa-113">**const unsigned short** **AUDIO\_STATUS\_NOAUDIO = 1;**</span></span><br/>           | <span data-ttu-id="cf9fa-114">Non è disponibile alcun supporto per l'output audio. ad esempio, poiché non è presente alcuna scheda audio.</span><span class="sxs-lookup"><span data-stu-id="cf9fa-114">There is no support for audio output; for example, because there is no sound card.</span></span>                             |
| <span data-ttu-id="cf9fa-115">**const unsigned short** **AUDIO STATUS \_ \_ CANTOPENAUDIO = 2;**</span><span class="sxs-lookup"><span data-stu-id="cf9fa-115">**const unsigned short** **AUDIO\_STATUS\_CANTOPENAUDIO = 2;**</span></span><br/>     | <span data-ttu-id="cf9fa-116">Il canale di output audio non può essere aperto (è occupato). ad esempio perché un'altra applicazione sta riproducendo l'audio.</span><span class="sxs-lookup"><span data-stu-id="cf9fa-116">The audio output channel can't be opened (is busy); for example, because another application is playing audio.</span></span> |
| <span data-ttu-id="cf9fa-117">**const unsigned short** **AUDIO STATUS \_ \_ USERSPEAKING = 3;**</span><span class="sxs-lookup"><span data-stu-id="cf9fa-117">**const unsigned short** **AUDIO\_STATUS\_USERSPEAKING = 3;**</span></span><br/>      | <span data-ttu-id="cf9fa-118">Il canale di output audio è occupato perché il server sta elaborando l'input vocale dell'utente</span><span class="sxs-lookup"><span data-stu-id="cf9fa-118">The audio output channel is busy because the server is processing user speech input</span></span>                            |
| <span data-ttu-id="cf9fa-119">**const unsigned short** **AUDIO STATUS \_ \_ CHARACTERSPEAKING = 4;**</span><span class="sxs-lookup"><span data-stu-id="cf9fa-119">**const unsigned short** **AUDIO\_STATUS\_CHARACTERSPEAKING = 4;**</span></span><br/> | <span data-ttu-id="cf9fa-120">Il canale di output audio è occupato perché un carattere sta parlando.</span><span class="sxs-lookup"><span data-stu-id="cf9fa-120">The audio output channel is busy because a character is currently speaking.</span></span>                                    |
| <span data-ttu-id="cf9fa-121">**const unsigned short** **AUDIO STATUS \_ \_ SROVERRIDEABLE = 5;**</span><span class="sxs-lookup"><span data-stu-id="cf9fa-121">**const unsigned short** **AUDIO\_STATUS\_SROVERRIDEABLE = 5;**</span></span><br/>    | <span data-ttu-id="cf9fa-122">Il canale di output audio non è occupato, ma è in attesa dell'input vocale dell'utente.</span><span class="sxs-lookup"><span data-stu-id="cf9fa-122">The audio output channel is not busy, but it is waiting for user speech input.</span></span>                                 |
| <span data-ttu-id="cf9fa-123">**const unsigned short** **AUDIO STATUS ERROR = \_ \_ 6;**</span><span class="sxs-lookup"><span data-stu-id="cf9fa-123">**const unsigned short** **AUDIO\_STATUS\_ERROR = 6;**</span></span><br/>             | <span data-ttu-id="cf9fa-124">Si è verificato un altro problema (sconosciuto) durante il tentativo di accesso al canale di output audio.</span><span class="sxs-lookup"><span data-stu-id="cf9fa-124">There was some other (unknown) problem in attempting to access the audio output channel.</span></span>                       |



 

</dd> </dl>

<span data-ttu-id="cf9fa-125">Questa impostazione consente all'applicazione client di eseguire query sullo stato del canale di output audio.</span><span class="sxs-lookup"><span data-stu-id="cf9fa-125">This setting enables your client application to query the state of the audio output channel.</span></span> <span data-ttu-id="cf9fa-126">È possibile usarlo per determinare se il tuo carattere deve parlare o se provare ad attivare la modalità di ascolto **(usando IAgentCharacterEx::Listen).**</span><span class="sxs-lookup"><span data-stu-id="cf9fa-126">You can use this to determine whether to have your character speak or to try to turn on Listening mode (using **IAgentCharacterEx::Listen**).</span></span>

 

 





