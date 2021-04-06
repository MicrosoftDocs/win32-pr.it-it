---
title: IAgentAudioOutputProperties GetEnabled
description: IAgentAudioOutputProperties GetEnabled
ms.assetid: a1e555e1-98f1-4a3d-b6ba-4cd35348db2b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e86b82c720971ae1e14ee294e6d097fd35ca80a5
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104044672"
---
# <a name="iagentaudiooutputpropertiesgetenabled"></a>IAgentAudioOutputProperties:: GetEnabled

\[Microsoft Agent è stato deprecato a partire da Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]

``` syntax
HRESULT GetEnabled(
long * pbEnabled  // address of variable for audio output Enabled setting 
);                      
```

Recupera un valore che indica se l'output del riconoscimento vocale del carattere è abilitato.

-   Restituisce \_ OK per indicare che l'operazione è stata completata.

<dl> <dt>

<span id="pbEnabled"></span><span id="pbenabled"></span><span id="PBENABLED"></span>*pbEnabled*
</dt> <dd>

Indirizzo di una variabile che riceve **true** se l'output vocale è attualmente abilitato e **false** se disabilitato.

</dd> </dl>

Poiché questa impostazione influiscono sull'output parlato (TTS e file audio) per tutti i caratteri, solo l'utente può modificare questa proprietà nella finestra delle proprietà di Microsoft Agent.

 

 




