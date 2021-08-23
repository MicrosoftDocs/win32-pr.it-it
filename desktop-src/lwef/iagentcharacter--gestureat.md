---
title: IAgentCharacter GestureAt
description: IAgentCharacter GestureAt
ms.assetid: ece84652-383e-4397-a6d9-f0209dd80767
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9bde86f9e1e60820aa7e1bc3a3f839dc920efda001f5b15e4f1ec7df4fc0cd7c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118976451"
---
# <a name="iagentcharactergestureat"></a>IAgentCharacter::GestureAt

\[Microsoft Agent è deprecato a Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]

``` syntax
HRESULT GestureAt(
   short x,         // x-coordinate of specified location
   short y,         // y-coordinate of specified location
   long * pdwReqID  // address of a request ID
);
```

Riproduce **l'animazione dello stato di inserimento** associata in base alla posizione specificata.

-   Restituisce S \_ OK per indicare che l'operazione è riuscita. Quando la funzione viene restituita, *pdwReqID* contiene l'ID della richiesta.

<dl> <dt>

<span id="x"></span><span id="X"></span>*X*
</dt> <dd>

Coordinata x della posizione specificata in pixel, rispetto all'origine dello schermo (in alto a sinistra).

</dd> <dt>

<span id="y"></span><span id="Y"></span>*Y*
</dt> <dd>

Coordinata y della posizione specificata in pixel, rispetto all'origine dello schermo (in alto a sinistra).

</dd> <dt>

<span id="pdwReqID"></span><span id="pdwreqid"></span><span id="PDWREQID"></span>*pdwReqID*
</dt> <dd>

Indirizzo di una variabile che riceve l'ID **richiesta GestureAt.**

</dd> </dl>

Il server determina e riproduce automaticamente l'animazione di inserimento appropriata in base alla posizione corrente del carattere e alla posizione specificata. Quando si usa il protocollo HTTP per accedere ai dati di animazione e caratteri, usare il metodo [**Prepare**](iagentcharacter--prepare.md) per assicurarsi che le animazioni siano disponibili prima di chiamare questo metodo.

 

 




