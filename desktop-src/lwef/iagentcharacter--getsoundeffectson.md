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
# <a name="iagentcharactergetsoundeffectson"></a>IAgentCharacter::GetSoundEffectsOn

\[Microsoft Agent è stato deprecato a partire da Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]

``` syntax
HRESULT GetSoundEffectsOn(
   long * pbOn  // address of variable for sound effects setting 
);
```

Recupera un valore che indica se l'impostazione degli effetti audio del carattere è abilitata.

-   Restituisce \_ OK per indicare che l'operazione è stata completata.

<dl> <dt>

<span id="pbOn"></span><span id="pbon"></span><span id="PBON"></span>*pbOn*
</dt> <dd>

Indirizzo di una variabile che riceve **true** se l'impostazione degli effetti audio del carattere è abilitata, **false** se è disabilitata.

</dd> </dl>

L'impostazione effetti acustici del carattere determina se gli effetti audio compilati come parte del carattere vengono riprodotti quando si riproduce un'animazione associata. L'impostazione è soggetta all'impostazione degli effetti acustici globali dell'utente in [**IAgentAudioOutputProperties:: GetUsingSoundEffects**](iagentaudiooutputproperties--getusingsoundeffects.md).

## <a name="see-also"></a>Vedere anche

[**IAgentCharacter:: SetSoundEffectsOn**](iagentcharacter--setsoundeffectson.md), [ **IAgentAudioOutputProperties:: GetUsingSoundEffects**](iagentaudiooutputproperties--getusingsoundeffects.md)


 

 




