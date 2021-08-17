---
title: IAgentCharacter GetTTSSpeed
description: IAgentCharacter GetTTSSpeed
ms.assetid: 25526ef7-581f-489c-a299-bd3b5ac9ea61
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 33e7fbe4cbba7eaed22f49865e1a0f0994c512867fb6f233ef2bbfa01dcaafcf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119609871"
---
# <a name="iagentcharactergetttsspeed"></a>IAgentCharacter::GetTTSSpeed

\[Microsoft Agent è deprecato a Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]

``` syntax
HRESULT GetTTSSpeed(
   long * pdwSpeed  // address of variable for character TTS output speed
);
```

Recupera l'impostazione della velocità di output TTS del carattere.

-   Restituisce S \_ OK per indicare che l'operazione è riuscita.

<dl> <dt>

<span id="pdwSpeed"></span><span id="pdwspeed"></span><span id="PDWSPEED"></span>*pdwSpeed*
</dt> <dd>

Indirizzo di una variabile che riceve la velocità di output del carattere in parole al minuto.

</dd> </dl>

Anche se l'applicazione non può scrivere questo valore, è possibile includere tag di velocità nel testo di output che velocizzano temporaneamente l'output per una determinata espressione.

Questa proprietà restituisce l'impostazione corrente della velocità di output per il carattere. Per i caratteri che usano l'output TTS, la proprietà restituisce l'output TTS effettivo per il carattere. Se TTS non è abilitato o il carattere non supporta l'output TTS, l'impostazione riflette l'impostazione dell'utente per la velocità di output.

 

 




