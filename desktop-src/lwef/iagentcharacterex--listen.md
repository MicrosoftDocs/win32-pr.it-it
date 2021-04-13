---
title: IAgentCharacterEx ascolto
description: IAgentCharacterEx ascolto
ms.assetid: 8d4cdb6c-04e1-498c-867f-fddbe6e2791a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 12c479936a8d2dc43e2f2da5a680a51705af2885
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104330695"
---
# <a name="iagentcharacterexlisten"></a>IAgentCharacterEx:: Listen

\[Microsoft Agent è stato deprecato a partire da Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]

``` syntax
HRESULT Listen(
   long bListen  // listening mode flag
);
```

Attiva o disattiva la modalità di ascolto (input riconoscimento vocale).

-   Restituisce \_ OK per indicare che l'operazione è stata completata.

<dl> <dt>

<span id="bListen"></span><span id="blisten"></span><span id="BLISTEN"></span>*bListen*
</dt> <dd>

Flag modalità di ascolto. Se questo parametro è **true**, la modalità di ascolto è attivata; Se **false**, la modalità di ascolto è disattivata.

</dd> </dl>

L'impostazione di questo metodo su **true** Abilita la modalità di ascolto (attiva il riconoscimento vocale) per un periodo di tempo fisso. Anche se non è possibile impostare il valore del timeout, è possibile disattivare la modalità di ascolto prima della scadenza del timeout. Inoltre, se la modalità di ascolto è già attiva perché l'utente (o un altro client) ha impostato correttamente il metodo su **true** prima della scadenza del timeout, il metodo ha esito positivo e reimposta il timeout. Tuttavia, se la modalità di ascolto è già attiva perché l'utente preme il tasto ascolto, il metodo ha esito positivo, ma il timeout viene ignorato e la modalità di ascolto termina in base all'interazione dell'utente con la chiave di ascolto.

Questo metodo avrà esito positivo solo quando viene chiamato dal client attivo di input. Pertanto, il metodo avrà esito negativo se il client non è il client attivo del carattere di primo livello. Il metodo avrà esito negativo anche se si tenta di impostare il metodo su **false** e l'utente preme il tasto di attesa. Può inoltre avere esito negativo se non è disponibile un motore vocale compatibile che corrisponda all'impostazione dell'ID lingua del carattere o se l'utente ha disabilitato l'input vocale usando la finestra delle proprietà di Microsoft Agent. Tuttavia, il metodo non avrà esito negativo se il dispositivo audio è occupato.

Quando si imposta correttamente questo metodo su **true**, il server attiva l'evento [**IAgentNotifySinkEx:: ListeningState**](iagentnotifysinkex--listeningstate.md) . Il server invia anche **IAgentNotifySinkEx:: ListeningState** al termine del timeout della modalità di ascolto o quando si imposta [**IAgentCharacterEx:: Listen**](https://www.bing.com/search?q=**IAgentCharacterEx::Listen**) su **false**.

Questo metodo non chiama automaticamente [**IAgentCharacter:: stopAll**](iagentcharacter--stopall.md) e riproduce un'animazione dello stato di ascolto del carattere come si verifica quando l'utente preme il tasto di attesa. Questo consente di usare l'evento [**IAgentNotifySinkEx:: ListeningState**](iagentnotifysinkex--listeningstate.md) per determinare se si vuole arrestare l'animazione corrente e riprodurre un'animazione appropriata. Tuttavia, una volta rilevato un enunciato utente, il server chiama automaticamente **IAgentCharacter:: stopAll** e riproduce un'animazione dello stato di udito.

## <a name="see-also"></a>Vedere anche

[**IAgentNotifySinkEx:: ListeningState**](iagentnotifysinkex--listeningstate.md), [ **IAgentSpeechInputProperties:: GetEnabled**](iagentspeechinputproperties--getenabled.md)


 

 




