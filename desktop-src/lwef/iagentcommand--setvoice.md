---
title: IAgentCommand
description: IAgentCommand
ms.assetid: bee06616-26bf-4e1e-89da-6765dd77fb02
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 36bed7e86cb93824fc26c770c1d01336077fda39
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "106299724"
---
# <a name="iagentcommandsetvoice"></a>IAgentCommand:: sevoice

\[Microsoft Agent è stato deprecato a partire da Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]

``` syntax
HRESULT SetVoice(
   BSTR bszVoice  // voice text setting for Command
);
```

Imposta la proprietà [**Voice**](voice-property.md) per un [**comando**](/windows/desktop/lwef/the-command-object).

-   Restituisce \_ OK per indicare che l'operazione è stata completata.

<dl> <dt>

<span id="bszVoice"></span><span id="bszvoice"></span><span id="BSZVOICE"></span>*bszVoice*
</dt> <dd>

BSTR che specifica il testo per la proprietà [**Voice**](voice-property.md) di un [**comando**](/windows/desktop/lwef/the-command-object).

</dd> </dl>

Un [**comando**](/windows/desktop/lwef/the-command-object) deve avere la proprietà [**Voice**](voice-property.md) e la proprietà [**Enabled**](enabled-property.md) impostate per essere accessibile tramite voce. Inoltre, la proprietà [**VoiceCaption**](voicecaption-property.md) deve essere impostata per essere visualizzata nella **finestra dei comandi vocali**. (Per compatibilità con le versioni precedenti, se non esiste alcun **VoiceCaption**, viene utilizzata l'impostazione del [**titolo**](caption-property.md) ).

L'espressione BSTR fornita può includere caratteri di parentesi quadre ( \[ \] ) per indicare parole facoltative e caratteri barra verticale ( \| ) per indicare stringhe alternative. Le alternative devono essere racchiuse tra parentesi. Ad esempio, "(Hello \[ There \] \| HI)" indica al motore di riconoscimento vocale di accettare "Hello", "Hello there" o "Hi" per il comando. Ricordarsi di includere spazi appropriati tra il testo racchiuso tra parentesi quadre o le parentesi e il testo che non è racchiuso tra parentesi quadre.

È possibile usare l'operatore Star ( \* ) per specificare zero o più istanze delle parole incluse nel gruppo o l'operatore più (+) per specificare una o più istanze. Ad esempio, di seguito viene riportata una grammatica che supporta "try this", "try this" e "try this", with Unlimited iteraziones of "Please":

``` syntax
   "please* try this"
```

Il formato di grammatica seguente esclude "try this" perché l'operatore + definisce almeno un'istanza di "Please":

``` syntax
   "please+ try this"
```

Gli operatori di ripetizione seguono le normali regole di precedenza e si applicano all'elemento di testo immediatamente precedente. Ad esempio, la grammatica seguente restituisce "New York" e "New York York", ma non "New York New York":

``` syntax
   "New York+"
```

Pertanto, in genere si desidera utilizzare questi operatori con i caratteri di raggruppamento. Ad esempio, la grammatica seguente include sia "New York" sia "New York New York":

``` syntax
   "(New York)+"
```

Gli operatori di ripetizione sono utili quando si desidera comporre una grammatica che includa una sequenza ripetuta, ad esempio un numero di telefono o una specifica di un elenco di elementi:

``` syntax
   "call (one|two|three|four|five|six|seven|eight|nine|zero|oh)*"
   "I'd like (cheese|pepperoni|pineapple|canadian bacon|mushrooms|and)+"
```

Anche se gli operatori possono essere utilizzati anche con le parentesi quadre (un carattere di raggruppamento facoltativo), in questo modo è possibile ridurre l'efficienza dell'elaborazione della grammatica da parte dell'agente.

È anche possibile usare i puntini di sospensione (...) per supportare l' *individuazione* di parole, ovvero indicare al motore di riconoscimento vocale di ignorare le parole pronunciate in questa posizione nella frase (talvolta denominata *Garbage* Word). Pertanto, il motore di riconoscimento vocale riconosce solo parole specifiche nella stringa, indipendentemente dal fatto che vengano pronunciate parole o frasi adiacenti. Se ad esempio si imposta questa proprietà su " \[ ... \] controllare la posta elettronica \[ ... \] "il motore di riconoscimento vocale corrisponde a frasi come" controllare la posta elettronica "o" selezionare la posta elettronica "per questo comando. I puntini di sospensione possono essere usati in qualsiasi punto all'interno di una stringa. Tuttavia, prestare attenzione utilizzando questa tecnica, perché le impostazioni vocali con ellissi possono aumentare il potenziale di corrispondenze indesiderate.

Quando si definiscono le parole e la grammatica del comando, assicurarsi sempre di includere almeno una parola richiesta. ovvero evitare di fornire solo parole facoltative. Assicurarsi inoltre che la parola includa solo parole e lettere pronunciabili. Per i numeri, è preferibile scrivere la parola anziché usare la rappresentazione numerica. Omettere anche segni di punteggiatura o simboli. Ad esempio, invece di "The \# $1 10 pizza!", usare "The number 1 10 Dollar pizza". L'inclusione di caratteri o simboli non pronunciabili per un comando può causare la mancata compilazione della grammatica da parte del motore vocale per tutti i comandi. Infine, impostare il parametro Voice come più ragionevolmente possibile da altri comandi vocali definiti dall'utente. Maggiore è la somiglianza tra la grammatica vocale per i comandi, più probabile verrà creato un errore di riconoscimento da parte del motore di riconoscimento vocale. È anche possibile usare i punteggi di confidenza per distinguere meglio tra due comandi che possono avere una grammatica vocale simile o simile.

L'impostazione della proprietà [**Voice**](voice-property.md) per un [**comando**](/windows/desktop/lwef/the-command-object) Abilita automaticamente i servizi di riconoscimento vocale di Agent, rendendo disponibili il tasto ascolto e il suggerimento di ascolto. Tuttavia, non carica il motore di riconoscimento vocale.

> [!Note]  
> Le funzionalità di grammatica disponibili possono dipendere dal motore di riconoscimento vocale. Si consiglia di verificare con il fornitore del motore di determinare quali opzioni di grammatica sono supportate. Usare [**IAgentCharacterEx:: SRModeID**](https://www.bing.com/search?q=**IAgentCharacterEx::SRModeID**) per specificare un motore.

 

## <a name="see-also"></a>Vedere anche

[**IAgentCommand:: getvoice**](iagentcommand--getvoice.md), [**IAgentCommand:: Caption**](iagentcommand--setcaption.md), [**IAgentCommand:: seenabled**](iagentcommand--setenabled.md), [**IAgentCommands:: Add**](iagentcommands--add.md), [**IAgentCommands:: Insert**](iagentcommands--insert.md)


 

 