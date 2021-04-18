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
# <a name="iagentcharactergetttspitch"></a>IAgentCharacter::GetTTSPitch

\[Microsoft Agent è stato deprecato a partire da Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]

``` syntax
HRESULT GetTTSPitch(
   long * pdwPitch  // address of variable for character TTS pitch
);
```

Recupera l'impostazione del pitch di output TTS del carattere.

-   Restituisce \_ OK per indicare che l'operazione è stata completata.

<dl> <dt>

<span id="pdwPitch"></span><span id="pdwpitch"></span><span id="PDWPITCH"></span>*pdwPitch*
</dt> <dd>

Indirizzo di una variabile che riceve l'impostazione del pitch TTS corrente del carattere in Hertz.

</dd> </dl>

Anche se l'applicazione non è in grado di scrivere questo valore, è possibile includere tag pitch nel testo di output che aumenterà temporaneamente il pitch per una determinata espressione. Questo metodo si applica solo ai caratteri configurati per l'output TTS. Se il motore di sintesi vocale (TTS) non è abilitato (o installato) o il carattere non supporta l'output TTS, questo metodo restituisce zero (0).

 

 




