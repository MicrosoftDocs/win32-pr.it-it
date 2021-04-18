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
# <a name="iagentcharactersetsoundeffectson"></a>IAgentCharacter::SetSoundEffectsOn

\[Microsoft Agent è stato deprecato a partire da Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]

``` syntax
HRESULT SetSoundEffectsOn(
   long bOn  // character sound effects setting 
);
```

Determina se vengono riprodotti gli effetti audio del carattere.

-   Restituisce \_ OK per indicare che l'operazione è stata completata.

<dl> <dt>

<span id="bOn"></span><span id="bon"></span><span id="BON"></span>*bOn*
</dt> <dd>

Impostazione effetti audio. Se questo parametro è **true**, gli effetti audio per le animazioni vengono riprodotti quando viene riprodotta l'animazione; Se **false**, gli effetti audio non vengono riprodotti.

</dd> </dl>

Questa impostazione determina se gli effetti audio compilati come parte del carattere vengono riprodotti quando si riproduce un'animazione associata. L'impostazione di questa proprietà si applica a tutti i client del carattere. L'impostazione è inoltre soggetta all'impostazione degli effetti audio globali dell'utente in [**IAgentAudioOutputProperties:: GetUsingSoundEffects**](iagentaudiooutputproperties--getusingsoundeffects.md).

## <a name="see-also"></a>Vedere anche

[**IAgentCharacter:: GetSoundEffectsOn**](iagentcharacter--getsoundeffectson.md), [ **IAgentAudioOutputProperties:: GetUsingSoundEffects**](iagentaudiooutputproperties--getusingsoundeffects.md)


 

 




