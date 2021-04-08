---
title: IAgentCharacter MoveTo
description: IAgentCharacter MoveTo
ms.assetid: 4e24d2f8-1df2-47ca-a1e9-b9d29708207d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 86d1ba423dc637895216ff03e2adec2862bbf27d
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "104046619"
---
# <a name="iagentcharactermoveto"></a>IAgentCharacter:: MoveTo

\[Microsoft Agent è stato deprecato a partire da Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]

``` syntax
HRESULT MoveTo(
   short x,         // x-coordinate of new location
   short y,         // y-coordinate of new location
   long lSpeed,     // speed to move the character
   long * pdwReqID  // address of request ID
);
```

Riproduce l'animazione dello stato di **spostamento** associato e sposta il frame di caratteri nella posizione specificata.

-   Restituisce \_ OK per indicare che l'operazione è stata completata. Quando la funzione restituisce, questa variabile contiene l'ID della richiesta.

<dl> <dt>

<span id="x"></span><span id="X"></span>*x*
</dt> <dd>

Coordinata x della nuova posizione, espressa in pixel, rispetto all'origine dello schermo (in alto a sinistra). La posizione di un carattere è basata sull'angolo superiore sinistro del frame di animazione.

</dd> <dt>

<span id="y"></span><span id="Y"></span>*y*
</dt> <dd>

Coordinata y della nuova posizione, espressa in pixel, rispetto all'origine dello schermo (in alto a sinistra). La posizione di un carattere è basata sull'angolo superiore sinistro del frame di animazione.

</dd> <dt>

<span id="lSpeed"></span><span id="lspeed"></span><span id="LSPEED"></span>*lSpeed*
</dt> <dd>

Parametro che specifica in millisecondi la velocità con cui viene spostato il frame del carattere. Il valore consigliato è 1000. Se si specifica zero (0), il frame viene spostato senza riprodurre un'animazione.

</dd> <dt>

<span id="pdwReqID"></span><span id="pdwreqid"></span><span id="PDWREQID"></span>*pdwReqID*
</dt> <dd>

Indirizzo di una variabile che riceve l'ID della richiesta [**MoveTo**](https://www.bing.com/search?q=**MoveTo**) .

</dd> </dl>

Quando si utilizza il protocollo HTTP per accedere ai dati di tipo carattere e animazione, utilizzare il metodo [**Prepare**](/windows/desktop/lwef/iagentcharacter--prepare) per garantire la disponibilità delle animazioni dello stato di **trasferimento** prima di chiamare questo metodo. Anche se l'animazione non è caricata, il server sposta ancora il frame.

## <a name="see-also"></a>Vedere anche

[**IAgentCharacter:: seposition**](iagentcharacter--setposition.md)


 

 