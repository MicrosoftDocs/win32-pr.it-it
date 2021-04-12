---
title: IAgentCommands
description: IAgentCommands
ms.assetid: dfb3b58a-7f24-4366-8f04-93a9e956fdc8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8a8e29936dbca65ffded5f8a5e5ea5297b28362e
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "104472862"
---
# <a name="iagentcommandssetvoice"></a>IAgentCommands:: sevoice

\[Microsoft Agent è stato deprecato a partire da Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]

``` syntax
HRESULT SetVoice(
   BSTR bszVoice  // the Voice setting for Command collection
);
```

Imposta la proprietà del testo [**vocale**](voice-property.md) per un [**comando**](/windows/desktop/lwef/the-command-object).

-   Restituisce \_ OK per indicare che l'operazione è stata completata.

<dl> <dt>

<span id="bszVoice"></span><span id="bszvoice"></span><span id="BSZVOICE"></span>*bszVoice*
</dt> <dd>

BSTR che specifica il valore per la proprietà del testo [**vocale**](voice-property.md) di una raccolta di [**comandi**](/windows/desktop/lwef/the-commands-collection-object) .

</dd> </dl>

Una raccolta di [**comandi**](/windows/desktop/lwef/the-commands-collection-object) deve avere la proprietà testo [**vocale**](voice-property.md) impostata per essere accessibile tramite voce. È necessario che la proprietà [**VoiceCaption**](voicecaption-property.md) o [**Caption**](caption-property.md) impostata su venga visualizzata nella finestra comandi vocali e che la relativa proprietà [**Visible**](visible-property.md) sia impostata su **true** per essere visualizzata nel menu di scelta rapida del carattere.

L'espressione BSTR fornita può includere caratteri di parentesi quadre ( \[ \] ) per indicare parole facoltative e caratteri barra verticale ( \| ) per indicare stringhe alternative. Le alternative devono essere racchiuse tra parentesi. Ad esempio, "(Hello \[ There \] \| HI)" indica al motore di riconoscimento vocale di accettare "Hello", "Hello there" o "Hi" per il comando. Ricordarsi di includere spazi appropriati tra le parole incluse tra parentesi quadre o tra parentesi e altro testo. Ricordarsi di includere spazi appropriati tra il testo racchiuso tra parentesi quadre o le parentesi e il testo che non è racchiuso tra parentesi quadre.

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

Sebbene gli operatori possano essere utilizzati anche con le parentesi quadre (un carattere di raggruppamento facoltativo), in questo modo è possibile ridurre l'efficienza dell'elaborazione della grammatica da parte dell'agente.

È anche possibile usare i puntini di sospensione (...) per supportare l' *individuazione* di parole, ovvero indicare al motore di riconoscimento vocale di ignorare le parole pronunciate in questa posizione nella frase (talvolta denominata *Garbage* Word). Quando si usano i puntini di sospensione, il motore di riconoscimento vocale riconosce solo parole specifiche nella stringa, indipendentemente dal fatto che vengano pronunciate parole o frasi adiacenti. Se ad esempio si imposta questa proprietà su " \[ ... \] controllare la posta elettronica \[ ... \] "il motore di riconoscimento vocale corrisponde a frasi come" controllare la posta elettronica "o" selezionare la posta elettronica "per questo comando. I puntini di sospensione possono essere usati in qualsiasi punto all'interno di una stringa. Tuttavia, prestare attenzione all'uso di questa tecnica poiché le impostazioni vocali con ellissi possono aumentare il rischio di corrispondenze indesiderate.

Quando si definiscono le parole e la grammatica del comando, includere almeno una parola richiesta; ovvero evitare di fornire solo parole facoltative. Assicurarsi inoltre che la parola includa solo parole e lettere pronunciabili. Per i numeri, è preferibile scrivere la parola anziché usare una rappresentazione ambigua. Ad esempio, "345" non è un formato di grammatica valido. Analogamente, anziché "IEEE", utilizzare "I triple E". Omettere anche segni di punteggiatura o simboli. Ad esempio, invece di "The \# $1 10 pizza!", usare "The number 1 10 Dollar pizza". L'inclusione di caratteri o simboli non pronunciabili per un comando può causare la mancata compilazione della grammatica da parte del motore vocale per tutti i comandi. Infine, impostare il parametro Voice come più ragionevolmente possibile da altri comandi vocali definiti dall'utente. Maggiore è la somiglianza tra la grammatica vocale per i comandi, più probabile verrà creato un errore di riconoscimento da parte del motore di riconoscimento vocale. È anche possibile usare i punteggi di confidenza per distinguere meglio tra due comandi che possono avere una grammatica vocale simile o simile.

È possibile includere nelle parole grammaticali sotto forma di "*\\ pronuncia del testo*", dove "testo" è il testo visualizzato e "Pronuncia" è un testo che chiarisce la pronuncia. Ad esempio, la grammatica "1st \\ First" viene riconosciuta quando l'utente dice "First", ma l'evento del [**comando**](/windows/desktop/lwef/the-command-object) restituirà il testo "1st \\ First". È anche possibile usare IPA (alfabeto fonetico internazionale) per specificare una pronuncia iniziando la pronuncia con un carattere di cancelletto (" \# "), quindi il testo che rappresenta la pronuncia IPA.

Per i motori di riconoscimento vocale giapponese è possibile definire la grammatica nel formato "*Kana \\ kanji*", riducendo le pronunce alternative e aumentando la precisione. L'ordine è invertito per compatibilità con le versioni precedenti. Questa operazione è particolarmente importante per la pronuncia dei nomi appropriati in kanji. Tuttavia, è possibile passare solo "kanji" senza il kana, nel qual caso il motore deve restare in ascolto di tutte le pronunce accettabili per il kanji. È anche possibile passare solo Kana.

Ad eccezione degli errori che utilizzano i caratteri di raggruppamento o di ripetizione, l'agente Microsoft non riporterà errori nella grammatica, a meno che il motore non segnali l'errore. Se si passa un testo nella grammatica che non riesce a compilare il motore, ma il motore non viene gestito e restituito come errore, Agent non è in grado di segnalare l'errore. Pertanto, l'applicazione client deve prestare particolare attenzione alla definizione della grammatica per la proprietà [**Voice**](voice-property.md) .

> [!Note]  
> Le funzionalità di grammatica disponibili possono dipendere dal motore di riconoscimento vocale. Si consiglia di verificare con il fornitore del motore di determinare quali opzioni di grammatica sono supportate. Usare [**SRModeID**](srmodeid-property.md) per usare un motore specifico.

 

Il funzionamento di questa proprietà dipende dallo stato di riconoscimento vocale del server di Microsoft Agent. Se, ad esempio, il riconoscimento vocale è disabilitato o non è installato, questa funzione non ha alcun effetto immediato. Se il riconoscimento vocale è abilitato durante una sessione, tuttavia, il comando diventerà accessibile quando la relativa applicazione client è di input-attivo.

## <a name="see-also"></a>Vedere anche

[**IAgentCommands:: getvoice**](iagentcommands--getvoice.md), [**IAgentCommands:: Caption**](iagentcommands--setcaption.md), [**IAgentCommands:: sevisible**](iagentcommands--setvisible.md)


 

 