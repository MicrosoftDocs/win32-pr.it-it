---
title: Attivazione di IAgentCharacter
description: Attivazione di IAgentCharacter
ms.assetid: a81eb62d-709b-46b4-9ff2-c9017f7f853e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c1e86d2c094da484f528750d433e0fb6608790e4
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104516123"
---
# <a name="iagentcharacteractivate"></a>IAgentCharacter:: Activate

\[Microsoft Agent è stato deprecato a partire da Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]

``` syntax
HRESULT Activate(
   short sState, // topmost character or client setting
);
```

Imposta un valore che indica se un client è attivo o un carattere è in primo piano.

-   Restituisce \_ OK per indicare che l'operazione è stata completata.
-   Restituisce \_ false per indicare che l'operazione non è riuscita.

<dl> <dt>

<span id="sState"></span><span id="sstate"></span><span id="SSTATE"></span>*sState*
</dt> <dd>

Per questo parametro è possibile specificare i valori seguenti:



| Valore | Descrizione                   |
|-------|-------------------------------|
| 0     | Imposta come non client attivo. |
| 1     | Imposta come client attivo.     |
| 2     | Creare il carattere di primo livello.   |



 

</dd> </dl>

Quando sono visibili più caratteri, solo uno dei caratteri riceve l'input vocale alla volta. Analogamente, quando più applicazioni client condividono lo stesso carattere, solo uno dei client riceve l'input del mouse, ad esempio gli eventi di clic o di trascinamento del controllo agente Microsoft alla volta. Il set di caratteri per ricevere input da mouse e vocale è il carattere superiore e il client che riceve l'input è il client attivo del carattere. La finestra del carattere superiore viene visualizzata anche nella parte superiore dell'ordine z della finestra dei caratteri. In genere, l'utente determina quale carattere è in primo piano selezionandola in modo esplicito. Tuttavia, l'attivazione in primo piano cambia anche quando un carattere viene visualizzato o nascosto (il carattere diventa o non è più in primo piano, rispettivamente).

È anche possibile usare questo metodo per gestire in modo esplicito quando il client riceve l'input indirizzato al carattere, ad esempio quando l'applicazione stessa diventa attiva. Se, ad esempio, si imposta **lo stato** su 2, il carattere è in primo piano e il client riceve tutti gli eventi di input del mouse e vocale generati dall'interazione dell'utente con il carattere. Quindi, rende il client anche il client di input-attivo del carattere. Tuttavia, è anche possibile impostare il client attivo per un carattere senza rendere il carattere superiore, impostando **lo stato** su 1. Ciò consente al client di ricevere input indirizzato a tale carattere quando il carattere diventa più in alto. Analogamente, è possibile impostare il client in modo che non sia il client attivo (per non ricevere input) quando il carattere diventa superiore, impostando **stato** su 0. È possibile determinare se un carattere dispone di altri client correnti utilizzando [**IAgentCharacter:: HasOtherClients**](iagentcharacter--hasotherclients.md).

Evitare di chiamare questo metodo direttamente dopo un metodo [**show**](iagentcharacter--show.md) . **Mostra** imposta automaticamente il client attivo di input. Quando il carattere è nascosto, la chiamata di **attivazione** potrebbe non riuscire se viene elaborata prima del completamento del metodo **show** .

Il tentativo di chiamare questo metodo con il parametro **state** impostato su 2 (quando il carattere specificato è nascosto) avrà esito negativo. Analogamente, se si imposta **lo stato** su 0 e l'applicazione è l'unico client, la chiamata avrà esito negativo. Un carattere deve sempre avere un client in primo piano.

> [!Note]  
> La chiamata a questo metodo con **lo stato** impostato su 1 non genera in genere un evento [**AgentNotifySink:: ActivateInputState**](https://www.bing.com/search?q=**AgentNotifySink::ActivateInputState**) a meno che non ci siano altri caratteri caricati o che l'applicazione sia già di input-Active.

 

## <a name="see-also"></a>Vedere anche

[**IAgentCharacter::HasOtherClients**](iagentcharacter--hasotherclients.md)


 

 




