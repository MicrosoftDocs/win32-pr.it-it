---
title: Proprietà Voice (oggetto Command)
description: Proprietà Voice
ms.assetid: e393aa89-6fa7-4080-9faf-66faca83d561
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 88a8f9003b5200882fc01ee37edb868a261c68c7
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/10/2020
ms.locfileid: "106300907"
---
# <a name="voice-property-command-object"></a>Proprietà Voice (oggetto Command)

\[Microsoft Agent è stato deprecato a partire da Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descrizione**
</dt> <dd>

Restituisce o imposta il testo passato alla grammatica del motore vocale (per il riconoscimento) per la corrispondenza di questo [**comando**](/windows/desktop/lwef/the-command-object) per il carattere.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintassi**
</dt> <dd>

*agente ***. Caratteri ("**_CharacterID_*_"). Comandi ("_*_Name_*_")._ *  \[  =  *Stringa* vocale\]



| Parte     | Descrizione                                                                                                                                       |
|----------|---------------------------------------------------------------------------------------------------------------------------------------------------|
| *string* | Espressione stringa corrispondente alle parole o alla frase che deve essere utilizzata dal motore di sintesi vocale per riconoscere questo [**comando**](/windows/desktop/lwef/the-command-object). |



 

</dd> </dl>

## <a name="remarks"></a>Commenti

Se non si specifica questo parametro, il [**VoiceCaption**](voicecaption-property.md) per l'oggetto [**Commands**](/windows/desktop/lwef/the-commands-collection-object) non verrà visualizzato nella finestra dei comandi vocali. Se si specifica un parametro [**Voice**](voice-property.md) ma non un **VoiceCaption** (o una [**didascalia**](https://www.bing.com/search?q=**Caption**)), il comando non verrà visualizzato nella finestra comandi vocali, ma sarà accessibile tramite voce quando l'applicazione client diventa input-Active.

L'espressione stringa può includere caratteri di parentesi quadre ( \[ \] ) per indicare parole facoltative e caratteri barra verticale ( \| ) per indicare stringhe alternative. Le alternative devono essere racchiuse tra parentesi. Ad esempio, "(Hello \[ There \] \| HI)" indica al motore di riconoscimento vocale di accettare "Hello", "Hello there" o "Hi" per il comando. Ricordarsi di includere spazi appropriati tra il testo racchiuso tra parentesi quadre o le parentesi e il testo che non è racchiuso tra parentesi quadre.

È possibile usare l'operatore Star ( \* ) per specificare zero o più istanze delle parole incluse nel gruppo o l'operatore più (+) per specificare una o più istanze. Il codice seguente, ad esempio, genera una grammatica che supporta "try this", "try this", try this ", with Unlimited iteraziones of" Please ":


```
   "please* try this"
```



Il formato di grammatica seguente esclude "try this" perché l'operatore + definisce almeno un'istanza di "Please":


```
   "please+ try this"
```



Gli operatori di ripetizione seguono le normali regole di precedenza e si applicano all'elemento di testo immediatamente precedente. Ad esempio, la grammatica seguente restituisce "New York" e "New York York", ma non "New York New York":


```
   "New York+"
```



Pertanto, in genere si desidera utilizzare questi operatori con i caratteri di raggruppamento. Ad esempio, la grammatica seguente include sia "New York" sia "New York New York":


```
   "(New York)+"
```



Gli operatori di ripetizione sono utili quando si desidera comporre una grammatica che includa una sequenza ripetuta, ad esempio un numero di telefono o una specifica di un elenco di elementi.


```
   "call (one|two|three|four|five|six|seven|eight|nine|zero|oh)*"
   "I'd like (cheese|pepperoni|pineapple|canadian bacon|mushrooms|and)+"
```



Anche se gli operatori possono essere utilizzati con il carattere di raggruppamento facoltativo tra parentesi quadre, in questo modo è possibile ridurre l'efficienza dell'elaborazione della grammatica da parte dell'agente.

È anche possibile usare i puntini di sospensione (...) per supportare l' *individuazione* di parole, ovvero indicare al motore di riconoscimento vocale di ignorare le parole pronunciate in questa posizione nella frase (talvolta denominata *Garbage* Word). Pertanto, il motore di riconoscimento vocale riconosce solo parole specifiche nella stringa, indipendentemente dal fatto che vengano pronunciate parole o frasi adiacenti. Se ad esempio si imposta questa proprietà su " \[ ... \] check mail \[ ... \] ", il motore di riconoscimento vocale corrisponderà a frasi come" controllare la posta elettronica "o" selezionare la posta elettronica "per questo comando. I puntini di sospensione possono essere usati in qualsiasi punto all'interno di una stringa. Tuttavia, prestare attenzione quando si utilizza questa tecnica perché potrebbe aumentare il rischio di corrispondenze indesiderate.

Quando si definisce la grammatica della parola per il comando, includere almeno una parola richiesta. ovvero evitare di fornire solo parole facoltative. Assicurarsi inoltre che la parola includa solo parole e lettere pronunciabili. Per i numeri, è preferibile scrivere la parola anziché usare una rappresentazione ambigua. Ad esempio, "345" non è un formato di grammatica valido. Analogamente, anziché "IEEE", utilizzare "I triple E". Omettere anche segni di punteggiatura o simboli. Ad esempio, invece di "The \# $1 10 pizza!", usare "The number 1 10 Dollar pizza". L'inclusione di caratteri o simboli non pronunciabili per un comando può causare la mancata compilazione della grammatica da parte del motore vocale per tutti i comandi. Infine, impostare il parametro Voice come più ragionevolmente possibile da altri comandi vocali definiti dall'utente. Maggiore è la somiglianza tra la grammatica vocale per i comandi, più probabile verrà creato un errore di riconoscimento da parte del motore di riconoscimento vocale. È anche possibile usare i punteggi di confidenza per distinguere meglio tra due comandi che possono avere una grammatica vocale simile o simile.

È possibile includere nelle parole grammaticali sotto forma di "*\\ pronuncia del testo*" *, dove il testo è* il testo visualizzato e la *pronuncia* è il testo che chiarisce la pronuncia. Ad esempio, la grammatica "1st \\ First" viene riconosciuta quando l'utente dice "First", ma l'evento del [**comando**](/windows/desktop/lwef/the-command-object) restituirà il testo "1st \\ First". È anche possibile usare IPA (alfabeto fonetico internazionale) per specificare una pronuncia iniziando la pronuncia con un segno di cancelletto (" \# "), quindi includere il testo che rappresenta la pronuncia IPA.

Per i motori di riconoscimento vocale giapponese è possibile definire la grammatica nel formato "*Kana \\ kanji*", riducendo le pronunce alternative e aumentando la precisione. L'ordine è invertito per compatibilità con le versioni precedenti. Questa operazione è particolarmente importante per la pronuncia dei nomi appropriati in kanji. Tuttavia, è possibile passare solo Kanji senza kana, nel qual caso il motore deve restare in ascolto di tutte le pronunce accettabili per il kanji. È anche possibile passare solo Kana.

Si noti inoltre che per lingue quali giapponese, cinese e tailandese, che non utilizzano caratteri di spazio per designare le interruzioni di parola, inserire un carattere di spazio a larghezza zero Unicode (0x200B) per indicare le interruzioni di parola logiche.

Ad eccezione degli errori che usano i caratteri di raggruppamento o di ripetizione, Agent non segnala gli errori della grammatica, a meno che il motore non segnali l'errore. Se si passa un testo nella grammatica che non riesce a compilare il motore, ma il motore non viene gestito e restituito come errore, Agent non è in grado di segnalare l'errore. Pertanto, l'applicazione client deve definire con attenzione la grammatica per la proprietà [**Voice**](voice-property.md) .

> [!Note]  
> Le funzionalità di grammatica disponibili possono dipendere dal motore di riconoscimento vocale. Si consiglia di verificare con il fornitore del motore di determinare quali opzioni di grammatica sono supportate. Usare [**SRModeID**](srmodeid-property.md) per usare un motore specifico.

 

Il funzionamento di questa proprietà dipende dallo stato della proprietà di riconoscimento vocale del server. Se, ad esempio, il riconoscimento vocale è disabilitato o non è installato, questa proprietà non ha alcun effetto.

 

 
