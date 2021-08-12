---
title: Proprietà Voice (oggetto Command)
description: Informazioni sulla proprietà Voice dell'oggetto Command, che restituisce o imposta il testo per la grammatica del motore di riconoscimento vocale per la corrispondenza di questo comando per il carattere.
ms.assetid: e393aa89-6fa7-4080-9faf-66faca83d561
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 698b39bf2129ff30eae78a949cf6d694af3c356e4c994a1a192bc55ab29fa23c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118245077"
---
# <a name="voice-property-command-object"></a>Proprietà Voice (oggetto Command)

\[Microsoft Agent è deprecato a Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descrizione**
</dt> <dd>

Restituisce o imposta il testo passato alla grammatica del motore di riconoscimento vocale (per il riconoscimento) per la corrispondenza di [**questo comando**](/windows/desktop/lwef/the-command-object) per il carattere.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintassi**
</dt> <dd>

*agent***. Caratteri ("**_CharacterID_*_"). Comandi ("_*_name_*_"). Stringa_ *  \[  =  *vocale*\]



| Parte     | Descrizione                                                                                                                                       |
|----------|---------------------------------------------------------------------------------------------------------------------------------------------------|
| *string* | Espressione stringa corrispondente alle parole o alla frase che il motore di riconoscimento vocale deve usare per il riconoscimento di questo [**comando.**](/windows/desktop/lwef/the-command-object) |



 

</dd> </dl>

## <a name="remarks"></a>Commenti

Se non si specifica questo parametro, [**l'oggetto VoiceCaption**](voicecaption-property.md) per [**l'oggetto Commands**](/windows/desktop/lwef/the-commands-collection-object) non verrà visualizzato nella finestra Comandi vocali. Se si specifica un parametro [**Voice**](voice-property.md) ma non **voiceCaption** (o [**Caption),**](https://www.bing.com/search?q=**Caption**)il comando non verrà visualizzato nella finestra Comandi vocali, ma sarà accessibile dalla voce quando l'applicazione client diventa attiva per l'input.

L'espressione stringa può includere parentesi quadre ( ) per indicare parole facoltative e caratteri \[ \] barra verticale ( ) per indicare \| stringhe alternative. Le alternative devono essere racchiuse tra parentesi. Ad esempio, "(hello there hi)" indica al motore di riconoscimento vocale di accettare \[ \] \| "hello", "hello there" o "hi" per il comando. Ricordarsi di includere spazi appropriati tra il testo racchiuso tra parentesi quadre o tra parentesi e il testo non racchiuso tra parentesi quadre o tra parentesi.

È possibile usare l'operatore star ( ) per specificare zero o più istanze delle parole incluse nel gruppo o l'operatore più (+) per specificare una o \* più istanze. Ad esempio, il risultato seguente è una grammatica che supporta "try this", "please try this", "please try this", con iterazioni illimitate di "please":


```
   "please* try this"
```



Il formato di grammatica seguente esclude "try this" perché l'operatore + definisce almeno un'istanza di "please":


```
   "please+ try this"
```



Gli operatori di ripetizione seguono le normali regole di precedenza e si applicano all'elemento di testo immediatamente precedente. Ad esempio, la grammatica seguente determina "New York" e "New York York", ma non "New York New York":


```
   "New York+"
```



Pertanto, in genere si desidera utilizzare questi operatori con i caratteri di raggruppamento. Ad esempio, la grammatica seguente include sia "New York" che "New York New York":


```
   "(New York)+"
```



Gli operatori di ripetizione sono utili quando si vuole comporre una grammatica che include una sequenza ripetuta, ad esempio un numero di telefono o la specifica di un elenco di elementi.


```
   "call (one|two|three|four|five|six|seven|eight|nine|zero|oh)*"
   "I'd like (cheese|pepperoni|pineapple|canadian bacon|mushrooms|and)+"
```



Sebbene gli operatori possano essere usati anche con il carattere di raggruppamento facoltativo tra parentesi quadre, questa operazione può ridurre l'efficienza dell'elaborazione della grammatica da parte di Agent.

È anche possibile usare i puntini di sospensione (...) per supportare l'individuazione delle parole, ovvero indicando al motore di riconoscimento vocale di ignorare le parole pronunciate in questa posizione nella frase (talvolta dette parole non errate).  Pertanto, il motore di riconoscimento vocale riconosce solo parole specifiche nella stringa, indipendentemente dal fatto che si parla con parole o frasi adiacenti. Ad esempio, se si imposta questa proprietà su " \[ ... \] check mail \[ ... \] ", the speech recognition engine will match phrases like "please check mail" or "check mail please" to this command. I puntini di sospensione possono essere usati in qualsiasi punto all'interno di una stringa. Tuttavia, prestare attenzione a usare questa tecnica perché può aumentare il rischio di corrispondenze indesiderate.

Quando si definisce la grammatica delle parole per il comando, includere almeno una parola obbligatoria. in altre parole, evitare di specificare solo parole facoltative. Assicurarsi inoltre che la parola includa solo parole e lettere pronunciabili. Per i numeri, è meglio scrivere la parola anziché usare una rappresentazione ambigua. Ad esempio, "345" non è una forma grammaticale buona. Analogamente, invece di "IEEE", usare "I triple E". Omettere anche eventuali segni di punteggiatura o simboli. Ad esempio, invece di \# "1 pizza da 10 dollari!", usare "the number one ten dollar pizza". L'inclusione di caratteri o simboli non pronunciabili per un comando può causare la mancata compilazione della grammatica da parte del motore di riconoscimento vocale per tutti i comandi. Infine, rendere il parametro voce il più possibile distinto dagli altri comandi vocali definiti. Maggiore è la somiglianza tra la grammatica vocale per i comandi, maggiore è la probabilità che il motore di riconoscimento vocale restituirà un errore di riconoscimento. È anche possibile usare i punteggi di attendibilità per distinguere meglio tra due comandi che possono avere una grammatica vocale simile o simile.

È possibile includere nelle parole grammaticali sotto forma di  "*\\ pronuncia* del testo ", dove testo è il testo visualizzato e *pronuncia* è il testo che chiarisce la pronuncia. Ad esempio, la grammatica "1st first" verrebbe riconosciuta quando l'utente dice "first", ma l'evento Command restituirà il testo \\ "1st [](/windows/desktop/lwef/the-command-object) \\ first". È anche possibile usare IPA (International Phonetic Alphabet) per specificare una pronuncia iniziando la pronuncia con un carattere cancelletto (" "), quindi includere il testo che rappresenta la \# pronuncia IPA.

Per i motori di riconoscimento vocale giapponese, è possibile definire la grammatica nel formato "*kana \\ kanji*", riducendo le pronunce alternative e aumentando l'accuratezza. L'ordinamento viene invertito per garantire la compatibilità con le versioni precedenti. Ciò è particolarmente importante per la pronuncia dei nomi propri in Kanji. Tuttavia, è possibile passare kanji senza il Kana, nel qual caso il motore deve restare in ascolto di tutte le pronunce accettabili per i Kanji. È anche possibile passare solo Kana.

Si noti anche che per lingue come giapponese, cinese e thai, che non usano spazi per designare le interruzioni di parola, inserire uno spazio unicode di larghezza zero (0x200B) per indicare interruzioni di parola logiche.

Ad eccezione degli errori che usano i caratteri di formattazione di raggruppamento o ripetizione, Agent non segnala gli errori nella grammatica, a meno che il motore stesso non restituirà l'errore. Se nella grammatica si passa testo che il motore non riesce a compilare, ma il motore non gestisce e restituisce un errore, Agent non può segnalare l'errore. Pertanto, l'applicazione client deve definire con attenzione la grammatica per la [**proprietà**](voice-property.md) Voice.

> [!Note]  
> Le funzionalità di grammatica disponibili possono dipendere dal motore di riconoscimento vocale. È possibile rivolgersi al fornitore del motore per determinare quali opzioni di grammatica sono supportate. Usare [**SRModeID per**](srmodeid-property.md) usare un motore specifico.

 

L'operazione di questa proprietà dipende dallo stato della proprietà di riconoscimento vocale del server. Ad esempio, se il riconoscimento vocale è disabilitato o non installato, questa proprietà non ha alcun effetto.

 

 
