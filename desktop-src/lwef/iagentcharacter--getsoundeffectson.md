---
title: IAgentCharacter GetSoundEffectsOn
description: IAgentCharacter GetSoundEffectsOn
ms.assetid: 11bc074e-7654-4a78-920e-acd56db52c98
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5a40f18a4fb8e7778c116c54391a7dc50e5267af
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106298978"
---
# <a name="iagentcharactergetsoundeffectson"></a><span data-ttu-id="7465a-103">IAgentCharacter::GetSoundEffectsOn</span><span class="sxs-lookup"><span data-stu-id="7465a-103">IAgentCharacter::GetSoundEffectsOn</span></span>

<span data-ttu-id="7465a-104">\[Microsoft Agent è stato deprecato a partire da Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="7465a-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT GetSoundEffectsOn(
   long * pbOn  // address of variable for sound effects setting 
);
```

<span data-ttu-id="7465a-105">Recupera un valore che indica se l'impostazione degli effetti audio del carattere è abilitata.</span><span class="sxs-lookup"><span data-stu-id="7465a-105">Retrieves whether the character's sound effects setting is enabled.</span></span>

-   <span data-ttu-id="7465a-106">Restituisce \_ OK per indicare che l'operazione è stata completata.</span><span class="sxs-lookup"><span data-stu-id="7465a-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="7465a-107"><span id="pbOn"></span><span id="pbon"></span><span id="PBON"></span>*pbOn*</span><span class="sxs-lookup"><span data-stu-id="7465a-107"><span id="pbOn"></span><span id="pbon"></span><span id="PBON"></span>*pbOn*</span></span>
</dt> <dd>

<span data-ttu-id="7465a-108">Indirizzo di una variabile che riceve **true** se l'impostazione degli effetti audio del carattere è abilitata, **false** se è disabilitata.</span><span class="sxs-lookup"><span data-stu-id="7465a-108">Address of a variable that receives **True** if the character's sound effects setting is enabled, **False** if disabled.</span></span>

</dd> </dl>

<span data-ttu-id="7465a-109">L'impostazione effetti acustici del carattere determina se gli effetti audio compilati come parte del carattere vengono riprodotti quando si riproduce un'animazione associata.</span><span class="sxs-lookup"><span data-stu-id="7465a-109">The character's sound effects setting determines whether sound effects compiled as a part of the character are played when you play an associated animation.</span></span> <span data-ttu-id="7465a-110">L'impostazione è soggetta all'impostazione degli effetti acustici globali dell'utente in [**IAgentAudioOutputProperties:: GetUsingSoundEffects**](iagentaudiooutputproperties--getusingsoundeffects.md).</span><span class="sxs-lookup"><span data-stu-id="7465a-110">The setting is subject to the user's global sound effects setting in [**IAgentAudioOutputProperties::GetUsingSoundEffects**](iagentaudiooutputproperties--getusingsoundeffects.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="7465a-111">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="7465a-111">See Also</span></span>

<span data-ttu-id="7465a-112">[**IAgentCharacter:: SetSoundEffectsOn**](iagentcharacter--setsoundeffectson.md), [ **IAgentAudioOutputProperties:: GetUsingSoundEffects**](iagentaudiooutputproperties--getusingsoundeffects.md)</span><span class="sxs-lookup"><span data-stu-id="7465a-112">[**IAgentCharacter::SetSoundEffectsOn**](iagentcharacter--setsoundeffectson.md), [**IAgentAudioOutputProperties::GetUsingSoundEffects**](iagentaudiooutputproperties--getusingsoundeffects.md)</span></span>


 

 




