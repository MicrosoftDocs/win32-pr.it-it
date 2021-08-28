---
title: IAgentCharacter GetSoundEffectsOn
description: IAgentCharacter GetSoundEffectsOn
ms.assetid: 11bc074e-7654-4a78-920e-acd56db52c98
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7f7133e41e4c291200feaf8fdb8ab3919cdb622ca927c155fc0941202fd555a6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119848641"
---
# <a name="iagentcharactergetsoundeffectson"></a>IAgentCharacter::GetSoundEffectsOn

\[Microsoft Agent è deprecato a Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]

``` syntax
HRESULT GetSoundEffectsOn(
   long * pbOn  // address of variable for sound effects setting 
);
```

Recupera un valore che indica se l'impostazione degli effetti audio del carattere è abilitata.

-   Restituisce S \_ OK per indicare che l'operazione è riuscita.

<dl> <dt>

<span id="pbOn"></span><span id="pbon"></span><span id="PBON"></span>*pbOn*
</dt> <dd>

Indirizzo di una variabile che riceve **True se** l'impostazione degli effetti sonori del carattere è abilitata, **False** se disabilitata.

</dd> </dl>

L'impostazione degli effetti audio del carattere determina se gli effetti audio compilati come parte del carattere vengono riprodotti quando si riproduce un'animazione associata. L'impostazione è soggetta all'impostazione degli effetti audio globali dell'utente in [**IAgentAudioOutputProperties::GetUsingSoundEffects**](iagentaudiooutputproperties--getusingsoundeffects.md).

## <a name="see-also"></a>Vedere anche

[**IAgentCharacter::SetSoundEffectsOn**](iagentcharacter--setsoundeffectson.md), [ **IAgentAudioOutputProperties::GetUsingSoundEffects**](iagentaudiooutputproperties--getusingsoundeffects.md)


 

 




