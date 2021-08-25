---
title: IAgentCharacter MoveTo
description: IAgentCharacter MoveTo
ms.assetid: 4e24d2f8-1df2-47ca-a1e9-b9d29708207d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 00ea5a0e288e4b7d9782f1b463fdbcccf01b0da9314894be1a60c556392e25e8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119848541"
---
# <a name="iagentcharactermoveto"></a>IAgentCharacter::MoveTo

\[Microsoft Agent è deprecato a Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]

``` syntax
HRESULT MoveTo(
   short x,         // x-coordinate of new location
   short y,         // y-coordinate of new location
   long lSpeed,     // speed to move the character
   long * pdwReqID  // address of request ID
);
```

Riproduce **l'animazione dello** stato Di spostamento associata e sposta il fotogramma carattere nella posizione specificata.

-   Restituisce S \_ OK per indicare che l'operazione è riuscita. Quando la funzione viene restituita, questa variabile contiene l'ID della richiesta.

<dl> <dt>

<span id="x"></span><span id="X"></span>*X*
</dt> <dd>

Coordinata x della nuova posizione in pixel, rispetto all'origine dello schermo (in alto a sinistra). La posizione di un carattere si basa sull'angolo superiore sinistro del frame di animazione.

</dd> <dt>

<span id="y"></span><span id="Y"></span>*Y*
</dt> <dd>

Coordinata y della nuova posizione in pixel, rispetto all'origine dello schermo (in alto a sinistra). La posizione di un carattere si basa sull'angolo superiore sinistro del frame di animazione.

</dd> <dt>

<span id="lSpeed"></span><span id="lspeed"></span><span id="LSPEED"></span>*lSpeed*
</dt> <dd>

Parametro che specifica in millisecondi la velocità di spostamento del frame del carattere. Il valore consigliato è 1000. Se si specifica zero (0), il frame viene spostato senza riprodurre un'animazione.

</dd> <dt>

<span id="pdwReqID"></span><span id="pdwreqid"></span><span id="PDWREQID"></span>*pdwReqID*
</dt> <dd>

Indirizzo di una variabile che riceve l'ID [**richiesta MoveTo.**](https://www.bing.com/search?q=**MoveTo**)

</dd> </dl>

Quando si usa il protocollo HTTP per accedere ai dati di animazione e caratteri, usare il metodo [**Prepare**](/windows/desktop/lwef/iagentcharacter--prepare) per garantire la disponibilità delle animazioni di stato **Moving** prima di chiamare questo metodo. Anche se l'animazione non è caricata, il server sposta comunque il frame.

## <a name="see-also"></a>Vedere anche

[**IAgentCharacter::SetPosition**](iagentcharacter--setposition.md)


 

 