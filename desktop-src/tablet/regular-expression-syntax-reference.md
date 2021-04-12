---
description: È possibile definire e assegnare ambiti di input personalizzati utilizzando la sintassi delle espressioni regolari della grafia riconosciuta da alcuni riconoscitori della grafia Microsoft.
ms.assetid: e3afe735-eca8-4fda-bd5b-cc0ab0b6a872
title: Riferimento alla sintassi delle espressioni regolari
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 23c0de50ff37795032719d9bc90ee81891324ba9
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/10/2021
ms.locfileid: "104234437"
---
# <a name="regular-expression-syntax-reference"></a>Riferimento alla sintassi delle espressioni regolari

È possibile definire e assegnare ambiti di input personalizzati utilizzando la sintassi delle espressioni regolari della grafia riconosciuta da alcuni riconoscitori della grafia Microsoft. La sintassi è un subset dell' [implementazione del linguaggio delle espressioni regolari](/documentation/?url=%2flibrary%2fcpgenref%2fhtml%2fcpconRegularExpressionsLanguageElements.asp%3fframe%3dtrue) nel .NET Framework.

Esistono alcune differenze nel modo in cui vengono utilizzate le espressioni regolari della grafia e il modo in cui vengono utilizzati gli altri tipi di espressioni regolari. La sintassi della grafia viene utilizzata per specificare una stringa esatta che verrà confrontata con il motore di riconoscimento e non con una sottostringa. Ad esempio, l'espressione regolare s ( \[ a-z \] +) p restituirà corrispondenze per "soup", "Stop", "Instep" e "esofago". Invece, un'espressione regolare di grafia equivalente, ad esempio s (! IS \_ ONechar) + p, corrisponderebbe a "soup" e "Stop", ma non a "Instep" e "esofago".

Le espressioni regolari di grafia non supportano gli spazi non di suddivisione nelle espressioni regolari. Ovvero non è possibile utilizzare l'entità "nbsp" all'interno di un'espressione regolare di grafia.

Le sezioni seguenti descrivono la sintassi in modo più dettagliato.

## <a name="valid-operators"></a>Operatori validi

Gli operatori seguenti sono validi per la creazione di espressioni regolari per la definizione degli ambiti di input per i riconoscitori della grafia.



| Operatore      | Descrizione                                                                           |
|---------------|---------------------------------------------------------------------------------------|
| \*<br/> | Operatore unario suffisso che significa zero o più occorrenze dell'operando.<br/> |
| +<br/>  | Operatore unario suffisso che indica una o più occorrenze dell'operando.<br/>  |
| ?<br/>  | Operatore unario suffisso che significa zero o una occorrenza dell'operando.<br/>   |
| \|<br/> | Operatore infisso binario che significa "or".<br/>                                        |
| ()<br/> | Utilizzato per raggruppare gli elementi.<br/>                                                       |



 

L'implementazione Microsoft di espressioni regolari per i riconoscitori della grafia consente le applicazioni ripetute di operatori unari di suffisso. Ad esempio, a \* \* = (a \* ) \* = a \* , b?? = (b?)? = b?. Consentono inoltre ripetizioni non consecutive, ad esempio: a \* ? \* = ((a \* )?) \* = (a \* ) \* = a \* . Si tratta di una differenza rispetto a .NET Framework espressioni regolari, che consentono solo? operatore da ripetere.

Un'altra differenza rispetto a .NET Framework espressioni regolari è che le espressioni regolari della grafia non supportano un'espressione vuota designata con una coppia di parentesi vuota, ().

> [!Note]  
> Solo i caratteri della tabella codici 1252 sono supportati per le espressioni regolari di grafia.

 

## <a name="using-input-scopes"></a>Uso degli ambiti di input

È anche possibile usare il set di ambiti di input normali definiti come parte della funzione [**SetInputScope**](/windows/win32/api/inputscope/nf-inputscope-setinputscope) nelle espressioni regolari. Il valore per month (Numerical), ad esempio, è \_ date \_ Month. La sintassi per specificare un ambito di input come parte di un'espressione regolare è anteporre il valore enumerato dell'ambito di input con una parentesi aperta e un punto esclamativo, (!, e inserire una parentesi di chiusura,) alla fine. Ad esempio:

(! È \_ \_mese data)

Se si combina l' \_ ambito di input predefinito Oring con qualsiasi altro ambito di input, l'effetto è che il riconoscimento può restituire qualsiasi espressione singola supportata dal modello di lingua predefinito (ad esempio, una parola dal dizionario di sistema o una data) con o senza punteggiatura oppure qualsiasi valore che soddisfi il resto dell'espressione regolare passata al riconoscimento.

> [!Note]  
> I membri seguenti di [**SetInputScope**](/windows/win32/api/inputscope/nf-inputscope-setinputscope) non sono supportati nelle espressioni regolari: è l'oggetto \_ Phrase, è \_ REGULAREXPRESSION, è \_ SRGS, è \_ XML.

 

## <a name="unsupported-operators"></a>Operatori non supportati

Gli operatori di espressioni regolari seguenti non sono supportati quando si creano espressioni regolari della grafia.



| Operatore                                     | Descrizione                                                         |
|----------------------------------------------|---------------------------------------------------------------------|
| .<br/>                                 | Carattere punto.<br/>                                        |
| \[\]<br/>                              | Parentesi quadre. Usare le parentesi per raggruppare gli elementi.<br/>     |
| {}<br/>                                | Parentesi graffe.<br/>                                          |
| (?\# commento) e \# \[ Commento\]<br/> | Commenti.<br/>                                                |
| $<br/>                                 | Segno di dollaro.<br/>                                   |
| ^<br/>                                 | Carattere del punto di inserimento.<br/>                                         |
| -<br/>                                 | Carattere tratteggiato. Deve o ( \| ) insieme tutti i set di elementi.<br/> |



 

## <a name="escaping-characters"></a>Utilizzo di caratteri di escape

I caratteri ordinari, diversi da quelli nella tabella seguente, corrispondono a se stessi. Ovvero un "a" in un'espressione regolare specifica che l'input deve corrispondere a "a".

Un'altra differenza significativa nella scrittura di espressioni regolari di grafia è che è possibile escludere solo un set limitato di caratteri all'interno di un'espressione regolare. Nella tabella seguente viene descritto il set di caratteri consentito di cui è possibile utilizzare il carattere di escape. Qualsiasi altro tentativo di eseguire l'escape di un carattere provocherà un errore generato dal riconoscimento.



| Carattere       |
|-----------------|
| \\\*<br/> |
| \\+<br/>  |
| \\?<br/>  |
| \\(<br/>  |
| \\)<br/>  |
| \\\|<br/> |
| \\\\<br/> |
| \\!<br/>  |
| \\.<br/>  |
| \\\[<br/> |
| \\\]<br/> |
| \\^<br/>  |
| \\{<br/>  |
| \\}<br/>  |
| \\$<br/>  |
| \\\#<br/> |



 

 

 