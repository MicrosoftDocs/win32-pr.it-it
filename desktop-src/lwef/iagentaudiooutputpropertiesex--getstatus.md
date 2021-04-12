---
title: IAgentAudioOutputPropertiesEx GetStatus
description: IAgentAudioOutputPropertiesEx GetStatus
ms.assetid: 29bf1379-eebe-4b8b-b8d0-b86d2da78b64
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9dd89f4b3d8101ff15b868551626775e6f2e341f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104396310"
---
# <a name="iagentaudiooutputpropertiesexgetstatus"></a><span data-ttu-id="6b929-103">IAgentAudioOutputPropertiesEx:: GetStatus</span><span class="sxs-lookup"><span data-stu-id="6b929-103">IAgentAudioOutputPropertiesEx::GetStatus</span></span>

<span data-ttu-id="6b929-104">\[Microsoft Agent è stato deprecato a partire da Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="6b929-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT GetStatus(
   long * plStatus,  // address of audio channel status
);
```

<span data-ttu-id="6b929-105">Recupera lo stato del canale audio.</span><span class="sxs-lookup"><span data-stu-id="6b929-105">Retrieves the status of the audio channel.</span></span>

-   <span data-ttu-id="6b929-106">Restituisce \_ OK per indicare che l'operazione è stata completata.</span><span class="sxs-lookup"><span data-stu-id="6b929-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="6b929-107"><span id="plStatus"></span><span id="plstatus"></span><span id="PLSTATUS"></span>*plStatus*</span><span class="sxs-lookup"><span data-stu-id="6b929-107"><span id="plStatus"></span><span id="plstatus"></span><span id="PLSTATUS"></span>*plStatus*</span></span>
</dt> <dd>

<span data-ttu-id="6b929-108">Stato del canale di output audio, che può corrispondere a uno dei valori seguenti:</span><span class="sxs-lookup"><span data-stu-id="6b929-108">Status of the audio output channel, which may be one of the following values:</span></span>



| <span data-ttu-id="6b929-109">Valore</span><span class="sxs-lookup"><span data-stu-id="6b929-109">Value</span></span>                                                                         | <span data-ttu-id="6b929-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="6b929-110">Description</span></span>                                                                                                    |
|-------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6b929-111">stato dell'audio **short senza segno const** **\_ \_ disponibile = 0;**</span><span class="sxs-lookup"><span data-stu-id="6b929-111">**const unsigned short** **AUDIO\_STATUS\_AVAILABLE = 0;**</span></span><br/>         | <span data-ttu-id="6b929-112">Il canale di output audio è disponibile (non occupato).</span><span class="sxs-lookup"><span data-stu-id="6b929-112">The audio output channel is available (not busy).</span></span>                                                              |
| <span data-ttu-id="6b929-113">stato audio **breve senza segno const** **\_ \_ = 1;**</span><span class="sxs-lookup"><span data-stu-id="6b929-113">**const unsigned short** **AUDIO\_STATUS\_NOAUDIO = 1;**</span></span><br/>           | <span data-ttu-id="6b929-114">Non è disponibile alcun supporto per l'output audio. ad esempio, perché non è presente alcuna scheda audio.</span><span class="sxs-lookup"><span data-stu-id="6b929-114">There is no support for audio output; for example, because there is no sound card.</span></span>                             |
| <span data-ttu-id="6b929-115">stato dell'audio **breve senza segno const** **\_ \_ CANTOPENAUDIO = 2;**</span><span class="sxs-lookup"><span data-stu-id="6b929-115">**const unsigned short** **AUDIO\_STATUS\_CANTOPENAUDIO = 2;**</span></span><br/>     | <span data-ttu-id="6b929-116">Non è possibile aprire il canale di output audio (è occupato); ad esempio, perché un'altra applicazione sta riproducendo audio.</span><span class="sxs-lookup"><span data-stu-id="6b929-116">The audio output channel can't be opened (is busy); for example, because another application is playing audio.</span></span> |
| <span data-ttu-id="6b929-117">stato dell'audio **breve senza segno const** **\_ \_ USERSPEAKING = 3;**</span><span class="sxs-lookup"><span data-stu-id="6b929-117">**const unsigned short** **AUDIO\_STATUS\_USERSPEAKING = 3;**</span></span><br/>      | <span data-ttu-id="6b929-118">Il canale di output audio è occupato perché il server sta elaborando l'input vocale dell'utente</span><span class="sxs-lookup"><span data-stu-id="6b929-118">The audio output channel is busy because the server is processing user speech input</span></span>                            |
| <span data-ttu-id="6b929-119">stato dell'audio **breve senza segno const** **\_ \_ CHARACTERSPEAKING = 4;**</span><span class="sxs-lookup"><span data-stu-id="6b929-119">**const unsigned short** **AUDIO\_STATUS\_CHARACTERSPEAKING = 4;**</span></span><br/> | <span data-ttu-id="6b929-120">Il canale di output audio è occupato perché è in corso un carattere.</span><span class="sxs-lookup"><span data-stu-id="6b929-120">The audio output channel is busy because a character is currently speaking.</span></span>                                    |
| <span data-ttu-id="6b929-121">stato dell'audio **breve senza segno const** **\_ \_ SROVERRIDEABLE = 5;**</span><span class="sxs-lookup"><span data-stu-id="6b929-121">**const unsigned short** **AUDIO\_STATUS\_SROVERRIDEABLE = 5;**</span></span><br/>    | <span data-ttu-id="6b929-122">Il canale di output audio non è occupato, ma è in attesa dell'input vocale dell'utente.</span><span class="sxs-lookup"><span data-stu-id="6b929-122">The audio output channel is not busy, but it is waiting for user speech input.</span></span>                                 |
| <span data-ttu-id="6b929-123">errore di stato dell'audio **breve const senza segno** **\_ \_ = 6;**</span><span class="sxs-lookup"><span data-stu-id="6b929-123">**const unsigned short** **AUDIO\_STATUS\_ERROR = 6;**</span></span><br/>             | <span data-ttu-id="6b929-124">Si è verificato un altro problema (sconosciuto) durante il tentativo di accedere al canale di output audio.</span><span class="sxs-lookup"><span data-stu-id="6b929-124">There was some other (unknown) problem in attempting to access the audio output channel.</span></span>                       |



 

</dd> </dl>

<span data-ttu-id="6b929-125">Questa impostazione consente all'applicazione client di eseguire query sullo stato del canale di output audio.</span><span class="sxs-lookup"><span data-stu-id="6b929-125">This setting enables your client application to query the state of the audio output channel.</span></span> <span data-ttu-id="6b929-126">È possibile usare questo valore per determinare se il carattere deve parlare o provare ad attivare la modalità di ascolto (usando [**IAgentCharacterEx:: Listen**](lwef.iagentcharacterex::listen_method)).</span><span class="sxs-lookup"><span data-stu-id="6b929-126">You can use this to determine whether to have your character speak or to try to turn on Listening mode (using [**IAgentCharacterEx::Listen**](lwef.iagentcharacterex::listen_method)).</span></span>

 

 





