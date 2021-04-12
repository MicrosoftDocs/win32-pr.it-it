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
# <a name="iagentcharactergetttsspeed"></a>IAgentCharacter::GetTTSSpeed

\[Microsoft Agent è stato deprecato a partire da Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]

``` syntax
HRESULT GetTTSSpeed(
   long * pdwSpeed  // address of variable for character TTS output speed
);
```

Recupera l'impostazione della velocità di output TTS del carattere.

-   Restituisce \_ OK per indicare che l'operazione è stata completata.

<dl> <dt>

<span id="pdwSpeed"></span><span id="pdwspeed"></span><span id="PDWSPEED"></span>*pdwSpeed*
</dt> <dd>

Indirizzo di una variabile che riceve la velocità di output del carattere in parole al minuto.

</dd> </dl>

Anche se l'applicazione non è in grado di scrivere questo valore, è possibile includere tag di velocità nel testo di output che accelererà temporaneamente l'output per una determinata espressione.

Questa proprietà restituisce l'impostazione della velocità di output in lettura corrente per il carattere. Per i caratteri che usano l'output TTS, la proprietà restituisce l'output TTS effettivo per il carattere. Se TTS non è abilitato o il carattere non supporta l'output TTS, l'impostazione riflette l'impostazione utente per la velocità di output.

 

 




