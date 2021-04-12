---
title: IAgentBalloon GetEnabled
description: IAgentBalloon GetEnabled
ms.assetid: 1a5ea6c0-6150-459f-95eb-a9c7598c1d94
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cfd78245534b942e7972066ec90179172f7b556c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104332468"
---
# <a name="iagentballoongetenabled"></a>IAgentBalloon:: GetEnabled

\[Microsoft Agent è stato deprecato a partire da Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]

``` syntax
HRESULT GetEnabled(
  long * pbEnabled  // address of variable for Enabled setting 
);                  // for word balloon
```

Recupera il valore della proprietà [**Enabled**](enabled-property.md) per un fumetto di Word.

-   Restituisce \_ OK per indicare che l'operazione è stata completata.

<dl> <dt>

<span id="pbEnabled"></span><span id="pbenabled"></span><span id="PBENABLED"></span>*pbEnabled*
</dt> <dd>

Indirizzo di una variabile che riceve **true** quando il Word Balloon è abilitato e **false** quando è disabilitato.

</dd> </dl>

Il server Microsoft Agent Visualizza automaticamente la parola fumetto per l'output parlato, a meno che non sia disabilitato. La parola Balloon può essere disabilitata per un carattere nell'editor dei caratteri di Microsoft Agent oppure (dall'utente) per tutti i caratteri nella finestra delle proprietà di Microsoft Agent. Se l'utente disabilita la parola Balloon, il client non potrà ripristinarla.

 

 




