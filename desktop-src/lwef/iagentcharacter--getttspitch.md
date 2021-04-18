---
title: IAgentCharacter GetTTSPitch
description: IAgentCharacter GetTTSPitch
ms.assetid: b21ae1f1-daf6-42e5-9c52-f28722180021
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2dff1bb7999795cf27e29a7d064dd500b47bb419
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106298977"
---
# <a name="iagentcharactergetttspitch"></a><span data-ttu-id="5d5fa-103">IAgentCharacter::GetTTSPitch</span><span class="sxs-lookup"><span data-stu-id="5d5fa-103">IAgentCharacter::GetTTSPitch</span></span>

<span data-ttu-id="5d5fa-104">\[Microsoft Agent è stato deprecato a partire da Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="5d5fa-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT GetTTSPitch(
   long * pdwPitch  // address of variable for character TTS pitch
);
```

<span data-ttu-id="5d5fa-105">Recupera l'impostazione del pitch di output TTS del carattere.</span><span class="sxs-lookup"><span data-stu-id="5d5fa-105">Retrieves the character's TTS output pitch setting.</span></span>

-   <span data-ttu-id="5d5fa-106">Restituisce \_ OK per indicare che l'operazione è stata completata.</span><span class="sxs-lookup"><span data-stu-id="5d5fa-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="5d5fa-107"><span id="pdwPitch"></span><span id="pdwpitch"></span><span id="PDWPITCH"></span>*pdwPitch*</span><span class="sxs-lookup"><span data-stu-id="5d5fa-107"><span id="pdwPitch"></span><span id="pdwpitch"></span><span id="PDWPITCH"></span>*pdwPitch*</span></span>
</dt> <dd>

<span data-ttu-id="5d5fa-108">Indirizzo di una variabile che riceve l'impostazione del pitch TTS corrente del carattere in Hertz.</span><span class="sxs-lookup"><span data-stu-id="5d5fa-108">Address of a variable that receives the character's current TTS pitch setting in Hertz.</span></span>

</dd> </dl>

<span data-ttu-id="5d5fa-109">Anche se l'applicazione non è in grado di scrivere questo valore, è possibile includere tag pitch nel testo di output che aumenterà temporaneamente il pitch per una determinata espressione.</span><span class="sxs-lookup"><span data-stu-id="5d5fa-109">Although your application cannot write this value, you can include pitch tags in your output text that will temporarily increase the pitch for a particular utterance.</span></span> <span data-ttu-id="5d5fa-110">Questo metodo si applica solo ai caratteri configurati per l'output TTS.</span><span class="sxs-lookup"><span data-stu-id="5d5fa-110">This method applies only to characters configured for TTS output.</span></span> <span data-ttu-id="5d5fa-111">Se il motore di sintesi vocale (TTS) non è abilitato (o installato) o il carattere non supporta l'output TTS, questo metodo restituisce zero (0).</span><span class="sxs-lookup"><span data-stu-id="5d5fa-111">If the speech synthesis (TTS) engine is not enabled (or installed) or the character does not support TTS output, this method returns zero (0).</span></span>

 

 




