---
title: IAgentCharacter GestureAt
description: IAgentCharacter GestureAt
ms.assetid: ece84652-383e-4397-a6d9-f0209dd80767
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 266dc2d5e797ec0c7b30f7f827a094cd01c04195
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104396995"
---
# <a name="iagentcharactergestureat"></a>IAgentCharacter::GestureAt

\[Microsoft Agent è stato deprecato a partire da Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]

``` syntax
HRESULT GestureAt(
   short x,         // x-coordinate of specified location
   short y,         // y-coordinate of specified location
   long * pdwReqID  // address of a request ID
);
```

Riproduce l'animazione dello stato **gestuale** associato in base alla posizione specificata.

-   Restituisce \_ OK per indicare che l'operazione è stata completata. Quando la funzione restituisce, *pdwReqID* contiene l'ID della richiesta.

<dl> <dt>

<span id="x"></span><span id="X"></span>*x*
</dt> <dd>

Coordinata x della posizione specificata, espressa in pixel, rispetto all'origine dello schermo (in alto a sinistra).

</dd> <dt>

<span id="y"></span><span id="Y"></span>*y*
</dt> <dd>

Coordinata y della posizione specificata, espressa in pixel, rispetto all'origine dello schermo (in alto a sinistra).

</dd> <dt>

<span id="pdwReqID"></span><span id="pdwreqid"></span><span id="PDWREQID"></span>*pdwReqID*
</dt> <dd>

Indirizzo di una variabile che riceve l'ID richiesta **GestureAt** .

</dd> </dl>

Il server determina automaticamente e riproduce l'animazione gestuale appropriata in base alla posizione corrente del carattere e alla posizione specificata. Quando si usa il protocollo HTTP per accedere ai dati di tipo carattere e animazione, usare il metodo [**Prepare**](iagentcharacter--prepare.md) per assicurarsi che le animazioni siano disponibili prima di chiamare questo metodo.

 

 




