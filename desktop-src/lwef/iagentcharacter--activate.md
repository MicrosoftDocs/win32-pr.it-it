---
title: IAgentCharacter Activate
description: IAgentCharacter Activate
ms.assetid: a81eb62d-709b-46b4-9ff2-c9017f7f853e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7256b1d155b051985c72120283e60896026218ea81d8b2b9c37dc94fb52bb63a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118750997"
---
# <a name="iagentcharacteractivate"></a>IAgentCharacter::Activate

\[Microsoft Agent è deprecato a Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]

``` syntax
HRESULT Activate(
   short sState, // topmost character or client setting
);
```

Imposta se un client è attivo o se un carattere è in primo piano.

-   Restituisce S \_ OK per indicare che l'operazione è riuscita.
-   Restituisce S \_ FALSE per indicare che l'operazione non è riuscita.

<dl> <dt>

<span id="sState"></span><span id="sstate"></span><span id="SSTATE"></span>*sState*
</dt> <dd>

È possibile specificare i valori seguenti per questo parametro:



| Valore | Descrizione                   |
|-------|-------------------------------|
| 0     | Impostare come non il client attivo. |
| 1     | Impostare come client attivo.     |
| 2     | Creare il carattere più in alto.   |



 

</dd> </dl>

Quando sono visibili più caratteri, solo uno dei caratteri riceve l'input vocale alla volta. Analogamente, quando più applicazioni client condividono lo stesso carattere, solo uno dei client riceve l'input del mouse (ad esempio, eventi clic o trascinamento del controllo di Microsoft Agent) alla volta. Il set di caratteri per ricevere l'input tramite mouse e voce è il carattere più in alto e il client che riceve l'input è il client attivo del carattere. La finestra del carattere più in alto viene visualizzata anche nella parte superiore dell'ordine z della finestra dei caratteri. In genere, l'utente determina il carattere in primo piano selezionandolo in modo esplicito. Tuttavia, l'attivazione in primo piano cambia anche quando un carattere viene visualizzato o nascosto (il carattere diventa o non è più in primo piano, rispettivamente).

È anche possibile usare questo metodo per gestire in modo esplicito quando il client riceve input indirizzato al carattere, ad esempio quando l'applicazione stessa diventa attiva. Ad esempio, se si imposta **Stato** su 2, il carattere viene visualizzato in primo piano e il client riceve tutti gli eventi di input del mouse e del riconoscimento vocale generati dall'interazione dell'utente con il carattere. Pertanto, rende anche il client il client attivo di input del carattere. Tuttavia, è anche possibile impostare il client attivo per un carattere senza rendere il carattere in primo piano, impostando **Stato** su 1. In questo modo il client può ricevere l'input indirizzato a tale carattere quando il carattere diventa in primo piano. Analogamente, è possibile impostare il client in modo che non sia il client attivo (per non ricevere input) quando il carattere diventa in primo piano, impostando **Stato** su 0. È possibile determinare se un carattere ha altri client correnti [**usando IAgentCharacter::HasOtherClients**](iagentcharacter--hasotherclients.md).

Evitare di chiamare questo metodo direttamente dopo un [**metodo Show.**](iagentcharacter--show.md) **Mostra** imposta automaticamente il client attivo di input. Quando il carattere è nascosto, la **chiamata Activate** potrebbe non riuscire, se viene elaborata prima del **completamento del** metodo Show.

Il tentativo di chiamare questo metodo con **il parametro State** impostato su 2 (quando il carattere specificato è nascosto) avrà esito negativo. Analogamente, se si imposta **State** su 0 e l'applicazione è l'unico client, questa chiamata ha esito negativo. Un carattere deve sempre avere un client in primo piano.

> [!Note]  
> La chiamata di questo metodo con **State** impostato su 1 in genere non genera un evento [**AgentNotifySink::ActivateInputState**](https://www.bing.com/search?q=**AgentNotifySink::ActivateInputState**) a meno che non siano stati caricati altri caratteri o che l'applicazione non sia già attiva per l'input.

 

## <a name="see-also"></a>Vedere anche

[**IAgentCharacter::HasOtherClients**](iagentcharacter--hasotherclients.md)


 

 




