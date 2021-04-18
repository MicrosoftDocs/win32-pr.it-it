---
title: IAgentCharacter SetSoundEffectsOn
description: IAgentCharacter SetSoundEffectsOn
ms.assetid: 141dd9a8-5fd8-42c6-880a-856c61cb8940
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3a454a6ebeecc763cb7e5a964bb1f2897df6c291
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106298647"
---
# <a name="iagentcharactersetsoundeffectson"></a><span data-ttu-id="66ff2-103">IAgentCharacter::SetSoundEffectsOn</span><span class="sxs-lookup"><span data-stu-id="66ff2-103">IAgentCharacter::SetSoundEffectsOn</span></span>

<span data-ttu-id="66ff2-104">\[Microsoft Agent è stato deprecato a partire da Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="66ff2-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT SetSoundEffectsOn(
   long bOn  // character sound effects setting 
);
```

<span data-ttu-id="66ff2-105">Determina se vengono riprodotti gli effetti audio del carattere.</span><span class="sxs-lookup"><span data-stu-id="66ff2-105">Determines whether the character's sound effects are played.</span></span>

-   <span data-ttu-id="66ff2-106">Restituisce \_ OK per indicare che l'operazione è stata completata.</span><span class="sxs-lookup"><span data-stu-id="66ff2-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="66ff2-107"><span id="bOn"></span><span id="bon"></span><span id="BON"></span>*bOn*</span><span class="sxs-lookup"><span data-stu-id="66ff2-107"><span id="bOn"></span><span id="bon"></span><span id="BON"></span>*bOn*</span></span>
</dt> <dd>

<span data-ttu-id="66ff2-108">Impostazione effetti audio.</span><span class="sxs-lookup"><span data-stu-id="66ff2-108">Sound effects setting.</span></span> <span data-ttu-id="66ff2-109">Se questo parametro è **true**, gli effetti audio per le animazioni vengono riprodotti quando viene riprodotta l'animazione; Se **false**, gli effetti audio non vengono riprodotti.</span><span class="sxs-lookup"><span data-stu-id="66ff2-109">If this parameter is **True**, the sound effects for animations are played when the animation plays; if **False**, sound effects are not played.</span></span>

</dd> </dl>

<span data-ttu-id="66ff2-110">Questa impostazione determina se gli effetti audio compilati come parte del carattere vengono riprodotti quando si riproduce un'animazione associata.</span><span class="sxs-lookup"><span data-stu-id="66ff2-110">This setting determines whether sound effects compiled as a part of the character are played when you play an associated animation.</span></span> <span data-ttu-id="66ff2-111">L'impostazione di questa proprietà si applica a tutti i client del carattere.</span><span class="sxs-lookup"><span data-stu-id="66ff2-111">This property's setting applies to all clients of the character.</span></span> <span data-ttu-id="66ff2-112">L'impostazione è inoltre soggetta all'impostazione degli effetti audio globali dell'utente in [**IAgentAudioOutputProperties:: GetUsingSoundEffects**](iagentaudiooutputproperties--getusingsoundeffects.md).</span><span class="sxs-lookup"><span data-stu-id="66ff2-112">The setting is also subject to the user's global sound effects setting in [**IAgentAudioOutputProperties::GetUsingSoundEffects**](iagentaudiooutputproperties--getusingsoundeffects.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="66ff2-113">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="66ff2-113">See Also</span></span>

<span data-ttu-id="66ff2-114">[**IAgentCharacter:: GetSoundEffectsOn**](iagentcharacter--getsoundeffectson.md), [ **IAgentAudioOutputProperties:: GetUsingSoundEffects**](iagentaudiooutputproperties--getusingsoundeffects.md)</span><span class="sxs-lookup"><span data-stu-id="66ff2-114">[**IAgentCharacter::GetSoundEffectsOn**](iagentcharacter--getsoundeffectson.md), [**IAgentAudioOutputProperties::GetUsingSoundEffects**](iagentaudiooutputproperties--getusingsoundeffects.md)</span></span>


 

 




