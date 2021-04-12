---
title: IAgentCharacter GetTTSSpeed
description: IAgentCharacter GetTTSSpeed
ms.assetid: 25526ef7-581f-489c-a299-bd3b5ac9ea61
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 551074e1647cffc88e0b5f9f530cea931cd21ff9
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104396986"
---
# <a name="iagentcharactergetttsspeed"></a><span data-ttu-id="b2fed-103">IAgentCharacter::GetTTSSpeed</span><span class="sxs-lookup"><span data-stu-id="b2fed-103">IAgentCharacter::GetTTSSpeed</span></span>

<span data-ttu-id="b2fed-104">\[Microsoft Agent è stato deprecato a partire da Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="b2fed-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT GetTTSSpeed(
   long * pdwSpeed  // address of variable for character TTS output speed
);
```

<span data-ttu-id="b2fed-105">Recupera l'impostazione della velocità di output TTS del carattere.</span><span class="sxs-lookup"><span data-stu-id="b2fed-105">Retrieves the character's TTS output speed setting.</span></span>

-   <span data-ttu-id="b2fed-106">Restituisce \_ OK per indicare che l'operazione è stata completata.</span><span class="sxs-lookup"><span data-stu-id="b2fed-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="b2fed-107"><span id="pdwSpeed"></span><span id="pdwspeed"></span><span id="PDWSPEED"></span>*pdwSpeed*</span><span class="sxs-lookup"><span data-stu-id="b2fed-107"><span id="pdwSpeed"></span><span id="pdwspeed"></span><span id="PDWSPEED"></span>*pdwSpeed*</span></span>
</dt> <dd>

<span data-ttu-id="b2fed-108">Indirizzo di una variabile che riceve la velocità di output del carattere in parole al minuto.</span><span class="sxs-lookup"><span data-stu-id="b2fed-108">Address of a variable that receives the output speed of the character in words per minute.</span></span>

</dd> </dl>

<span data-ttu-id="b2fed-109">Anche se l'applicazione non è in grado di scrivere questo valore, è possibile includere tag di velocità nel testo di output che accelererà temporaneamente l'output per una determinata espressione.</span><span class="sxs-lookup"><span data-stu-id="b2fed-109">Although your application cannot write this value, you can include speed tags in your output text that will temporarily speed up the output for a particular utterance.</span></span>

<span data-ttu-id="b2fed-110">Questa proprietà restituisce l'impostazione della velocità di output in lettura corrente per il carattere.</span><span class="sxs-lookup"><span data-stu-id="b2fed-110">This property returns the current speaking output speed setting for the character.</span></span> <span data-ttu-id="b2fed-111">Per i caratteri che usano l'output TTS, la proprietà restituisce l'output TTS effettivo per il carattere.</span><span class="sxs-lookup"><span data-stu-id="b2fed-111">For characters using TTS output, the property returns the actual TTS output for the character.</span></span> <span data-ttu-id="b2fed-112">Se TTS non è abilitato o il carattere non supporta l'output TTS, l'impostazione riflette l'impostazione utente per la velocità di output.</span><span class="sxs-lookup"><span data-stu-id="b2fed-112">If TTS is not enabled or the character does not support TTS output, the setting reflects the user setting for output speed.</span></span>

 

 




