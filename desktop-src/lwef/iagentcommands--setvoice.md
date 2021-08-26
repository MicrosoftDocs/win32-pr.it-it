---
title: IAgentCommands SetVoice
description: IAgentCommands SetVoice
ms.assetid: dfb3b58a-7f24-4366-8f04-93a9e956fdc8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d02fb124b51a3be1796258fdcb8ffa31d8b81b59636027f3d99497b27cd2bd00
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119961901"
---
# <a name="iagentcommandssetvoice"></a>IAgentCommands::SetVoice

\[Microsoft Agent è deprecato a Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]

``` syntax
HRESULT SetVoice(
   BSTR bszVoice  // the Voice setting for Command collection
);
```

Imposta la [**proprietà Voice**](voice-property.md) text per un [**oggetto Command.**](/windows/desktop/lwef/the-command-object)

-   Restituisce S \_ OK per indicare che l'operazione è riuscita.

<dl> <dt>

<span id="bszVoice"></span><span id="bszvoice"></span><span id="BSZVOICE"></span>*bszVoice*
</dt> <dd>

Oggetto BSTR che specifica il valore della proprietà [**Voice**](voice-property.md) text di una [**raccolta Commands.**](/windows/desktop/lwef/the-commands-collection-object)

</dd> </dl>

Una [**raccolta Commands**](/windows/desktop/lwef/the-commands-collection-object) deve avere la proprietà [**Voice**](voice-property.md) text impostata per essere accessibile dalla voce. Deve anche avere la proprietà [**VoiceCaption**](voicecaption-property.md) o [**Caption**](caption-property.md) impostata per essere visualizzata nella finestra Comandi vocali e la relativa proprietà [**Visible**](visible-property.md) impostata su **True** per essere visualizzata nel menu a comparsa del carattere.

L'espressione BSTR specificata può includere parentesi quadre ( ) per indicare parole facoltative e caratteri barra verticale ( ) per \[ \] indicare stringhe \| alternative. Le alternative devono essere racchiuse tra parentesi. Ad esempio, "(hello there hi)" indica al motore di riconoscimento vocale di accettare \[ \] \| "hello", "hello there" o "hi" per il comando. Ricordarsi di includere gli spazi appropriati tra le parole incluse tra parentesi o tra parentesi e altro testo. Ricordarsi di includere gli spazi appropriati tra il testo tra parentesi quadre o tra parentesi e il testo che non è tra parentesi o parentesi.

È possibile usare l'operatore star ( ) per specificare zero o più istanze delle parole incluse nel gruppo o l'operatore più (+) per specificare una \* o più istanze. Ad esempio, i risultati seguenti in una grammatica che supporta "prova questo", "prova questo" e "prova questo", con iterazioni illimitate di "please":

``` syntax
   "please* try this"
```

Il formato grammaticale seguente esclude "try this" perché l'operatore + definisce almeno un'istanza di "please":

``` syntax
   "please+ try this"
```

Gli operatori di ripetizione seguono le normali regole di precedenza e si applicano all'elemento di testo immediatamente precedente. Ad esempio, la grammatica seguente determina "New York" e "New York York", ma non "New York New York":

``` syntax
   "New York+"
```

Pertanto, in genere si vogliono usare questi operatori con i caratteri di raggruppamento. Ad esempio, la grammatica seguente include sia "New York" che "New York New York":

``` syntax
   "(New York)+"
```

Gli operatori di ripetizione sono utili quando si vuole comporre una grammatica che include una sequenza ripetuta, ad esempio un numero di telefono o la specifica di un elenco di elementi:

``` syntax
   "call (one|two|three|four|five|six|seven|eight|nine|zero|oh)*"
   "I'd like (cheese|pepperoni|pineapple|canadian bacon|mushrooms|and)+"
```

Anche se gli operatori possono essere usati anche con parentesi quadre (un carattere di raggruppamento facoltativo), questa operazione può ridurre l'efficienza dell'elaborazione della grammatica da parte di Agent.

È anche possibile usare i puntini di sospensione (...) per supportare l'avvistamento di parole, ovvero  indicando al motore di riconoscimento vocale di ignorare le parole pronunciate in questa posizione nella frase (talvolta dette parole non usate). Quando si usano i puntini di sospensione, il motore di riconoscimento vocale riconosce solo parole specifiche nella stringa indipendentemente da quando vengono pronunciate con parole o frasi adiacenti. Ad esempio, se si imposta questa proprietà su " \[ ... \] check mail ... " il motore di riconoscimento vocale corrisponderà a frasi come \[ \] "controlla posta" o "controlla la posta per favore" a questo comando. I puntini di sospensione possono essere usati in qualsiasi punto all'interno di una stringa. Tuttavia, prestare attenzione a usare questa tecnica perché le impostazioni vocali con i puntini di sospensione possono aumentare il potenziale di corrispondenze indesiderate.

Quando si definiscono le parole e la grammatica per il comando, includere almeno una parola necessaria. in altre parole, evitare di specificare solo parole facoltative. Assicurarsi inoltre che la parola includa solo parole e lettere pronunciabili. Per i numeri, è meglio scrivere la parola anziché usare una rappresentazione ambigua. Ad esempio, "345" non è una forma grammaticale buona. Analogamente, invece di "IEEE", usare "I triple E". Omettere anche eventuali segni di punteggiatura o simboli. Ad esempio, anziché "la \# pizza da 1$10!", usare "la pizza numero 10 dollari". Se si includono caratteri o simboli non pronunciabili per un comando, il motore di riconoscimento vocale potrebbe non compilare la grammatica per tutti i comandi. Infine, rendere il parametro voce il più possibile distinto dagli altri comandi vocali definiti. Maggiore è la somiglianza tra la grammatica vocale per i comandi, maggiore è la probabilità che il motore di riconoscimento vocale restituirà un errore di riconoscimento. È anche possibile usare i punteggi di attendibilità per distinguere meglio tra due comandi che possono avere grammatica vocale simile o simile.

È possibile includere nelle parole grammaticali sotto forma di "*\\ pronuncia* del testo ", dove "testo" è il testo visualizzato e "pronuncia" è il testo che chiarisce la pronuncia. Ad esempio, la grammatica "1st first", verrebbe riconosciuta quando l'utente dice "first", ma l'evento Command restituirà il testo \\ "1st [](/windows/desktop/lwef/the-command-object) \\ first". È anche possibile usare IPA (Alfabeto fonetico internazionale) per specificare una pronuncia iniziando la pronuncia con un carattere cancelletto (" "), quindi il testo che rappresenta la \# pronuncia IPA.

Per i motori di riconoscimento vocale giapponese, è possibile definire la grammatica nel formato *"kana \\ kanji",* riducendo le pronunce alternative e aumentando l'accuratezza. L'ordinamento viene invertito per garantire la compatibilità con le versioni precedenti. Ciò è particolarmente importante per la pronuncia dei nomi propri in Kanji. Tuttavia, è possibile passare semplicemente "kanji", senza Kana, nel qual caso il motore deve restare in ascolto di tutte le pronunce accettabili per kanji. È anche possibile passare solo Kana.

Fatta eccezione per gli errori che usano i caratteri di formattazione di raggruppamento o ripetizione, Microsoft Agent non segnala errori nella grammatica, a meno che il motore non ne restituirà l'errore. Se si passa testo nella grammatica che il motore non riesce a compilare, ma il motore non gestisce e restituisce come errore, Agent non può segnalare l'errore. Pertanto, l'applicazione client deve prestare attenzione a definire la grammatica per la [**proprietà**](voice-property.md) Voice.

> [!Note]  
> Le funzionalità grammaticali disponibili possono dipendere dal motore di riconoscimento vocale. È possibile rivolgersi al fornitore del motore per determinare le opzioni grammaticali supportate. Usare [**SRModeID**](srmodeid-property.md) per usare un motore specifico.

 

Il funzionamento di questa proprietà dipende dallo stato del riconoscimento vocale del server Microsoft Agent. Ad esempio, se il riconoscimento vocale è disabilitato o non installato, questa funzione non ha alcun effetto immediato. Se il riconoscimento vocale è abilitato durante una sessione, tuttavia, il comando diventerà accessibile quando l'applicazione client è attiva per l'input.

## <a name="see-also"></a>Vedere anche

[**IAgentCommands::GetVoice**](iagentcommands--getvoice.md), [**IAgentCommands::SetCaption**](iagentcommands--setcaption.md), [**IAgentCommands::SetVisible**](iagentcommands--setvisible.md)


 

 