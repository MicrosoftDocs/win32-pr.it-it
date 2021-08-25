---
title: IAgentCommand SetVoice
description: IAgentCommand SetVoice
ms.assetid: bee06616-26bf-4e1e-89da-6765dd77fb02
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e45af753dea18e9fda7b613e3b800ac886d949eb6494fd969cd8b7ceb488dfc2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118477241"
---
# <a name="iagentcommandsetvoice"></a>IAgentCommand::SetVoice

\[Microsoft Agent è deprecato a Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]

``` syntax
HRESULT SetVoice(
   BSTR bszVoice  // voice text setting for Command
);
```

Imposta la [**proprietà Voice**](voice-property.md) per un [**oggetto Command.**](/windows/desktop/lwef/the-command-object)

-   Restituisce S \_ OK per indicare che l'operazione è riuscita.

<dl> <dt>

<span id="bszVoice"></span><span id="bszvoice"></span><span id="BSZVOICE"></span>*bszVoice*
</dt> <dd>

Oggetto BSTR che specifica il testo per la [**proprietà Voice**](voice-property.md) di un [**oggetto Command.**](/windows/desktop/lwef/the-command-object)

</dd> </dl>

Un [**oggetto Command**](/windows/desktop/lwef/the-command-object) deve avere la proprietà [**Voice**](voice-property.md) e la [**proprietà Enabled**](enabled-property.md) impostate per essere accessibile tramite voce. Deve anche avere la proprietà [**VoiceCaption**](voicecaption-property.md) impostata per essere visualizzata nella **finestra Comandi vocali**. Per compatibilità con le versioni precedenti, se non è presente **voiceCaption,** viene [**usata l'impostazione Caption.**](caption-property.md)

L'espressione BSTR specificata può includere parentesi quadre ( ) per indicare parole facoltative e caratteri barra verticali ( ) per \[ \] indicare stringhe \| alternative. Le alternative devono essere racchiuse tra parentesi. Ad esempio, "(hello there hi)" indica al motore di riconoscimento vocale di accettare \[ \] \| "hello", "hello there" o "hi" per il comando. Ricordarsi di includere spazi appropriati tra il testo racchiuso tra parentesi quadre o tra parentesi e il testo non racchiuso tra parentesi quadre o tra parentesi.

È possibile usare l'operatore star ( ) per specificare zero o più istanze delle parole incluse nel gruppo o l'operatore più (+) per specificare una o \* più istanze. Ad esempio, il risultato seguente è una grammatica che supporta "try this", "please try this" e "please please try this", con iterazioni illimitate di "please":

``` syntax
   "please* try this"
```

Il formato di grammatica seguente esclude "try this" perché l'operatore + definisce almeno un'istanza di "please":

``` syntax
   "please+ try this"
```

Gli operatori di ripetizione seguono le normali regole di precedenza e si applicano all'elemento di testo immediatamente precedente. Ad esempio, la grammatica seguente determina "New York" e "New York York", ma non "New York New York":

``` syntax
   "New York+"
```

Pertanto, è in genere necessario utilizzare questi operatori con i caratteri di raggruppamento. Ad esempio, la grammatica seguente include sia "New York" che "New York New York":

``` syntax
   "(New York)+"
```

Gli operatori di ripetizione sono utili quando si vuole comporre una grammatica che include una sequenza ripetuta, ad esempio un numero di telefono o la specifica di un elenco di elementi:

``` syntax
   "call (one|two|three|four|five|six|seven|eight|nine|zero|oh)*"
   "I'd like (cheese|pepperoni|pineapple|canadian bacon|mushrooms|and)+"
```

Anche se gli operatori possono essere usati anche con le parentesi quadre (un carattere di raggruppamento facoltativo), questa operazione può ridurre l'efficienza dell'elaborazione della grammatica da parte di Agent.

È anche possibile usare i puntini di sospensione (...) per supportare l'individuazione delle parole, ovvero indicando al motore di riconoscimento vocale di ignorare le parole pronunciate in questa posizione nella frase (talvolta dette parole non errate).  Pertanto, il motore di riconoscimento vocale riconosce solo parole specifiche nella stringa, indipendentemente dal fatto che si parla con parole o frasi adiacenti. Ad esempio, se si imposta questa proprietà su " \[ ... \] check mail ... " il motore di riconoscimento vocale corrisponderà a frasi come \[ \] "please check mail" o "check mail please" a questo comando. I puntini di sospensione possono essere usati in qualsiasi punto all'interno di una stringa. Tuttavia, prestare attenzione a usare questa tecnica, perché le impostazioni vocali con puntini di sospensione possono aumentare il rischio di corrispondenze indesiderate.

Quando si definiscono le parole e la grammatica per il comando, assicurarsi sempre di includere almeno una parola necessaria. in altre parole, evitare di specificare solo parole facoltative. Assicurarsi inoltre che la parola includa solo parole e lettere pronunciabili. Per i numeri, è meglio scrivere la parola anziché usare la rappresentazione numerica. Omettere anche eventuali segni di punteggiatura o simboli. Ad esempio, invece di \# "1 pizza da 10 dollari!", usare "the number one ten dollar pizza". L'inclusione di caratteri o simboli non pronunciabili per un comando può causare la mancata compilazione della grammatica da parte del motore di riconoscimento vocale per tutti i comandi. Infine, rendere il parametro voce il più possibile distinto dagli altri comandi vocali definiti. Maggiore è la somiglianza tra la grammatica vocale per i comandi, maggiore è la probabilità che il motore di riconoscimento vocale restituirà un errore di riconoscimento. È anche possibile usare i punteggi di attendibilità per distinguere meglio tra due comandi che possono avere una grammatica vocale simile o simile.

L'impostazione [**della proprietà Voice**](voice-property.md) per un comando [**abilita**](/windows/desktop/lwef/the-command-object) automaticamente i servizi voce di Agent, rendendo disponibili la chiave di ascolto e la descrizione di ascolto. Tuttavia, non carica il motore di riconoscimento vocale.

> [!Note]  
> Le funzionalità di grammatica disponibili possono dipendere dal motore di riconoscimento vocale. È possibile rivolgersi al fornitore del motore per determinare quali opzioni di grammatica sono supportate. Usare [**IAgentCharacterEx::SRModeID**](https://www.bing.com/search?q=**IAgentCharacterEx::SRModeID**) per specificare un motore.

 

## <a name="see-also"></a>Vedere anche

[**IAgentCommand::GetVoice**](iagentcommand--getvoice.md), [**IAgentCommand::SetCaption**](iagentcommand--setcaption.md), [**IAgentCommand::SetEnabled**](iagentcommand--setenabled.md), [**IAgentCommands::Add**](iagentcommands--add.md), [**IAgentCommands::Insert**](iagentcommands--insert.md)


 

 