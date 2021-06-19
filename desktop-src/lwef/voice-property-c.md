---
title: Proprietà Voice (oggetto Command)
description: Informazioni sulla proprietà Voice dell'oggetto Command, che restituisce o imposta il testo per la grammatica del motore di riconoscimento vocale per la corrispondenza di questo comando per il carattere.
ms.assetid: e393aa89-6fa7-4080-9faf-66faca83d561
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1ee7981de076fb3c7d8f796a8cc7d1177f96495c
ms.sourcegitcommit: 91530c19d26ba4c57a6af1f37b57f211f580464e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/19/2021
ms.locfileid: "112396146"
---
# <a name="voice-property-command-object"></a>Proprietà Voice (oggetto Command)

\[Microsoft Agent è deprecato a livello di Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]

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
| *string* | Espressione stringa corrispondente alle parole o alle frasi che devono essere usate dal motore di riconoscimento vocale per il riconoscimento di [**questo comando.**](/windows/desktop/lwef/the-command-object) |



 

</dd> </dl>

## <a name="remarks"></a>Commenti

Se non si specifica questo parametro, [**l'oggetto VoiceCaption**](voicecaption-property.md) per [**l'oggetto Commands**](/windows/desktop/lwef/the-commands-collection-object) non verrà visualizzato nella finestra Comandi vocali. Se si specifica un parametro [**Voice**](voice-property.md) ma non **voiceCaption** (o [**Caption),**](https://www.bing.com/search?q=**Caption**)il comando non verrà visualizzato nella finestra Comandi vocali, ma sarà accessibile dalla voce quando l'applicazione client diventa attiva per l'input.

L'espressione stringa può includere parentesi quadre ( ) per indicare parole facoltative e caratteri barra \[ \] verticale ( ) per indicare \| stringhe alternative. Le alternative devono essere racchiuse tra parentesi. Ad esempio, "(hello there hi)" indica al motore di riconoscimento vocale di accettare \[ \] \| "hello", "hello there" o "hi" per il comando. Ricordarsi di includere gli spazi appropriati tra il testo tra parentesi quadre o tra parentesi e il testo che non è tra parentesi o parentesi.

È possibile usare l'operatore star ( ) per specificare zero o più istanze delle parole incluse nel gruppo o l'operatore più (+) per specificare una \* o più istanze. Ad esempio, i risultati seguenti in una grammatica che supporta "prova questo", "prova questo", "prova questo", "prova questo", con iterazioni illimitate di "please":


```
   "please* try this"
```



Il formato grammaticale seguente esclude "try this" perché l'operatore + definisce almeno un'istanza di "please":


```
   "please+ try this"
```



Gli operatori di ripetizione seguono le normali regole di precedenza e si applicano all'elemento di testo immediatamente precedente. Ad esempio, la grammatica seguente determina "New York" e "New York York", ma non "New York New York":


```
   "New York+"
```



Pertanto, in genere si vogliono usare questi operatori con i caratteri di raggruppamento. Ad esempio, la grammatica seguente include sia "New York" che "New York New York":


```
   "(New York)+"
```



Gli operatori di ripetizione sono utili quando si vuole comporre una grammatica che include una sequenza ripetuta, ad esempio un numero di telefono o una specifica di un elenco di elementi.


```
   "call (one|two|three|four|five|six|seven|eight|nine|zero|oh)*"
   "I'd like (cheese|pepperoni|pineapple|canadian bacon|mushrooms|and)+"
```



Anche se gli operatori possono essere usati anche con il carattere di raggruppamento facoltativo tra parentesi quadre, questa operazione può ridurre l'efficienza dell'elaborazione della grammatica da parte di Agent.

È anche possibile usare i puntini di sospensione (...) per supportare l'avvistamento di parole, ovvero  per fare in modo che il motore di riconoscimento vocale ignori le parole pronunciate in questa posizione nella frase (talvolta dette parole non usate). Di conseguenza, il motore di riconoscimento vocale riconosce solo parole specifiche nella stringa, indipendentemente da quando vengono pronunciate con parole o frasi adiacenti. Ad esempio, se si imposta questa proprietà su " \[ ... \] check mail ... ", il motore di riconoscimento vocale corrisponderà a frasi come \[ \] "controlla posta" o "controlla posta per favore" a questo comando. I puntini di sospensione possono essere usati ovunque all'interno di una stringa. Tuttavia, prestare attenzione a usare questa tecnica perché può aumentare il potenziale di corrispondenze indesiderate.

Quando si definisce la grammatica delle parole per il comando, includere almeno una parola necessaria. in altre parole, evitare di specificare solo parole facoltative. Assicurarsi inoltre che la parola includa solo parole e lettere pronunciabili. Per i numeri, è meglio scrivere la parola anziché usare una rappresentazione ambigua. Ad esempio, "345" non è un buon formato grammaticale. Analogamente, invece di "IEEE", usare "I triple E". Omettere anche eventuali segni di punteggiatura o simboli. Ad esempio, anziché "la \# pizza da 1$10!", usare "la pizza numero 10 dollari". Se si includono caratteri o simboli non pronunciabili per un comando, il motore di riconoscimento vocale potrebbe non compilare la grammatica per tutti i comandi. Infine, rendere il parametro voce il più possibile distinto dagli altri comandi vocali definiti. Maggiore è la somiglianza tra la grammatica vocale per i comandi, maggiore è la probabilità che il motore di riconoscimento vocale restituirà un errore di riconoscimento. È anche possibile usare i punteggi di attendibilità per distinguere meglio tra due comandi che possono avere grammatica vocale simile o simile.

È possibile includere nelle parole grammaticali sotto forma di  "*\\ pronuncia* del testo ", dove testo è il testo visualizzato e *pronuncia* è testo che chiarisce la pronuncia. Ad esempio, la grammatica "1st first", verrebbe riconosciuta quando l'utente dice "first", ma l'evento Command restituirà il testo \\ "1st [](/windows/desktop/lwef/the-command-object) \\ first". È anche possibile usare IPA (Alfabeto fonetico internazionale) per specificare una pronuncia iniziando la pronuncia con un carattere cancelletto (" "), quindi includere il testo che rappresenta la \# pronuncia IPA.

Per i motori di riconoscimento vocale giapponese, è possibile definire la grammatica nel formato "*kana \\ kanji*", riducendo le pronunce alternative e aumentando l'accuratezza. L'ordinamento viene invertito per garantire la compatibilità con le versioni precedenti. Ciò è particolarmente importante per la pronuncia dei nomi propri in Kanji. Tuttavia, è possibile passare kanji senza Kana, nel qual caso il motore deve restare in ascolto di tutte le pronunce accettabili per kanji. È anche possibile passare solo Kana.

Si noti anche che per lingue come il giapponese, il cinese e il tailandese, che non usano spazi per designare interruzioni di parola, inserire uno spazio unicode a larghezza zero (0x200B) per indicare interruzioni di parola logiche.

Fatta eccezione per gli errori che usano i caratteri di formattazione di raggruppamento o ripetizione, Agent non segnala gli errori nella grammatica, a meno che il motore non ne restituirà l'errore. Se si passa testo nella grammatica che il motore non riesce a compilare, ma il motore non gestisce e restituisce come errore, Agent non può segnalare l'errore. Pertanto, l'applicazione client deve definire con attenzione la grammatica per la [**proprietà**](voice-property.md) Voice.

> [!Note]  
> Le funzionalità grammaticali disponibili possono dipendere dal motore di riconoscimento vocale. È possibile rivolgersi al fornitore del motore per determinare le opzioni grammaticali supportate. Usare [**SRModeID**](srmodeid-property.md) per usare un motore specifico.

 

Il funzionamento di questa proprietà dipende dallo stato della proprietà di riconoscimento vocale del server. Ad esempio, se il riconoscimento vocale è disabilitato o non installato, questa proprietà non ha alcun effetto.

 

 
