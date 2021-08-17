---
description: È possibile definire e assegnare ambiti di input personalizzati usando la sintassi delle espressioni regolari per la grafia riconosciuta da alcuni riconoscitori della grafia Microsoft.
ms.assetid: e3afe735-eca8-4fda-bd5b-cc0ab0b6a872
title: Informazioni di riferimento sulla sintassi delle espressioni regolari
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 33f09bbf81f86e3609f745358f0b18e35cf3f4712f3b1770fb3eb9c8becebc99
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118715531"
---
# <a name="regular-expression-syntax-reference"></a>Informazioni di riferimento sulla sintassi delle espressioni regolari

È possibile definire e assegnare ambiti di input personalizzati usando la sintassi delle espressioni regolari per la grafia riconosciuta da alcuni riconoscitori della grafia Microsoft. La sintassi è un subset [dell'implementazione del linguaggio](/documentation/?url=%2flibrary%2fcpgenref%2fhtml%2fcpconRegularExpressionsLanguageElements.asp%3fframe%3dtrue) delle espressioni regolari nel .NET Framework.

Esistono alcune differenze nel modo in cui vengono usate le espressioni regolari di scrittura manuale e nel modo in cui vengono usati gli altri tipi di espressioni regolari. La sintassi di scrittura manuale viene usata per specificare una stringa esatta che verrà trovata una corrispondenza con il motore di riconoscimento e non con una sottostringa. Ad esempio, l'espressione regolare s( a-z +)p restituirebbe corrispondenze per \[ \] "minestra", "stop", "instep" e "esophagus". Mentre un'espressione regolare di scrittura manuale equivalente, ad esempio s(!IS \_ ONECHAR)+p, corrisponde a "minestra" e "stop", ma non a "instep" e "esophagus".

Le espressioni regolari di scrittura manuale non supportano spazi non di rilievo all'interno delle espressioni regolari. Ciò significa che non è possibile usare l'entità "nbsp" all'interno di un'espressione regolare di scrittura manuale.

Le sezioni seguenti descrivono la sintassi in modo più dettagliato.

## <a name="valid-operators"></a>Operatori validi

Gli operatori seguenti sono validi per la creazione di espressioni regolari per definire gli ambiti di input per i riconoscitori della grafia.



| Operatore      | Descrizione                                                                           |
|---------------|---------------------------------------------------------------------------------------|
| \*<br/> | Operatore unario suffisso che indica zero o più occorrenze dell'operando.<br/> |
| +<br/>  | Operatore unario suffisso che indica una o più occorrenze dell'operando.<br/>  |
| ?<br/>  | Operatore unario suffisso che indica zero o un'occorrenza dell'operando.<br/>   |
| \|<br/> | Operatore infisso binario che significa "or".<br/>                                        |
| ()<br/> | Usato per raggruppare gli elementi.<br/>                                                       |



 

L'implementazione Microsoft di espressioni regolari per i riconoscitori di grafia consente applicazioni ripetute di operatori unari suffissi. Ad esempio, a \* \* = (a \* ) = a , \* \* b?? = (b?)? = b?. Consentono anche ripetizioni non consecutive, ad esempio? \* \* = ((a \* )?) \* = (a ) = a \* \* \* . Questa operazione è diversa .NET Framework espressioni regolari, che consentono solo ? operatore da ripetere.

Un'altra differenza .NET Framework espressioni regolari è che le espressioni regolari di scrittura manuale non supportano un'espressione vuota designata con una coppia vuota di parentesi ( ).

> [!Note]  
> Solo i caratteri nella tabella codici 1252 sono supportati per la scrittura manuale delle espressioni regolari.

 

## <a name="using-input-scopes"></a>Uso degli ambiti di input

È anche possibile usare il set di ambiti di input regolari definiti come parte della [**funzione SetInputScope**](/windows/win32/api/inputscope/nf-inputscope-setinputscope) nelle espressioni regolari. Ad esempio, il valore di Month (numerico) è IS \_ DATE \_ MONTH. La sintassi per specificare un ambito di input come parte di un'espressione regolare è anteporre al valore enumerato dell'ambito di input una parentesi aperta e un punto esclamativo , (!, e inserire una parentesi di chiusura, ), alla fine. Esempio:

(!IS \_ DATE \_ MONTH)

Se si combina l'ambito di input IS DEFAULT ometterlo con qualsiasi altro ambito di input, il riconoscimento può restituire qualsiasi singola espressione che il modello di linguaggio predefinito supporta (ad esempio, una parola del dizionario di sistema o una data) con o senza punteggiatura o qualsiasi valore che soddisfi il resto dell'espressione regolare passata al riconoscitore. \_

> [!Note]  
> I membri seguenti di [**SetInputScope**](/windows/win32/api/inputscope/nf-inputscope-setinputscope) non sono supportati nelle espressioni regolari: IS \_ PHRASELIST, IS \_ REGULAREXPRESSION, IS \_ SRGS, IS \_ XML.

 

## <a name="unsupported-operators"></a>Operatori non supportati

Gli operatori di espressione regolare seguenti non sono supportati durante la creazione di espressioni regolari di scrittura manuale.



| Operatore                                     | Descrizione                                                         |
|----------------------------------------------|---------------------------------------------------------------------|
| .<br/>                                 | Carattere punto.<br/>                                        |
| \[\]<br/>                              | Parentesi quadre. Usare le parentesi per raggruppare gli elementi.<br/>     |
| {}<br/>                                | Parentesi graffe.<br/>                                          |
| (?\# comment) e \# \[ comment\]<br/> | Commenti.<br/>                                                |
| $<br/>                                 | Carattere di segno di dollaro.<br/>                                   |
| ^<br/>                                 | Carattere di caret.<br/>                                         |
| -<br/>                                 | Carattere trattino. Deve essere OR ( \| ) insieme a tutti i set di elementi.<br/> |



 

## <a name="escaping-characters"></a>Utilizzo di caratteri di escape

I caratteri ordinari, diversi da quelli nella tabella seguente, corrispondono a se stessi. In altri, una "a" in un'espressione regolare specifica che l'input deve corrispondere a "a".

Un'altra differenza significativa nella scrittura di espressioni regolari di scrittura manuale è che è possibile eseguire l'escape solo di un set limitato di caratteri all'interno di un'espressione regolare. Nella tabella seguente viene descritto il set di caratteri consentiti che possono essere preceduti da caratteri di escape. Qualsiasi altro tentativo di escape di un carattere restituirà un errore generato dal sistema di riconoscimento.



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



 

 

 