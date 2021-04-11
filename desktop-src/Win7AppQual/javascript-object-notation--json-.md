---
description: .
ms.assetid: 2F6FDE88-C852-46BC-B6B1-630C266AF0AA
title: JavaScript Object Notation (JSON)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 18b995edc8e83405791a1d96598b827fc77f0204
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104232030"
---
# <a name="javascript-object-notation-json"></a>JavaScript Object Notation (JSON)

[JavaScript Object Notation (JSON)](https://www.json.org/) è un formato di interscambio dati semplice e leggero basato su un subset della notazione del valore letterale dell'oggetto del linguaggio JavaScript. Il motore JavaScript in Windows Internet Explorer 8 implementa la [proposta json 3,1 JSON](https://www.ecma-international.org/) per le funzioni native di gestione JSON, che usa l' [API json2.js di Douglas Crockford](https://github.com/douglascrockford/JSON-js/blob/master/json2.js).

Internet Explorer 8 include un oggetto JSON nativo che è conforme al supporto JSON descritto nella [bozza di lavoro della proposta es 3.1](https://www.ecma-international.org/). Alcune pagine web rilevano l'oggetto JSON nativo e quindi lo usano in modo non standard. Questo utilizzo causa in genere un errore di script e interrompe la gestione delle richieste AJAX. Nell'esempio di codice seguente viene illustrato il modo errato di utilizzare l'oggetto JSON.


```JScript
    if(!window.JSON) JSON = myJSON; 
    JSON.encode(obj); // Not part of the standard
```



Al contrario, l'esempio di codice seguente illustra un modo efficace per usare l'oggetto JSON.


```JScript
    JSON = myJSON; 
    JSON.encode(obj);
```



Windows Internet Explorer include i supporti nativi per JSON introducendo un oggetto JSON globale con due metodi predefiniti: **stringify** e **Parse**. L'oggetto JSON globale è definito nel motore JavaScript e viene creato durante la fase di inizializzazione del motore. Per mantenere la compatibilità con le versioni precedenti, questa funzionalità è disponibile solo quando un sito Web usa la versione più recente delle funzionalità JavaScript usando la modalità di layout (documento) "standard di Internet Explorer 8". Questa funzionalità può anche influire sul comportamento delle pagine Web che dipendono da una variabile globale JSON o usano [json2.js](https://github.com/douglascrockford/JSON-js/blob/master/json2.js).

È possibile eseguire l'override dell'oggetto JSON globale. Tuttavia, quando una pagina Web utilizza la modalità layout (documento) "standard di Internet Explorer 8", non è più un oggetto non definito. Poiché viene creata un'istanza di JSON come nome globale dal motore JavaScript, i controlli come "if (! this.JSON)" restituiscono false e devono essere modificati nel codice utente.

È probabile che le pagine Web che usano [json2.js](https://github.com/douglascrockford/JSON-js/blob/master/json2.js) non siano interessate. Con poche eccezioni, queste pagine dovrebbero funzionare più velocemente. Le eccezioni sono dovute alle differenze tra l'implementazione JSON nativa di Internet Explorer e la json2.js. Ad esempio, durante la serializzazione, l'implementazione JSON nativa rileva i cicli e non entra in una ricorsione infinita come json.js. Per ulteriori informazioni su queste eccezioni, vedere i [Blog di JavaScript](/archive/blogs/jscript/).

Per ulteriori informazioni, vedere la [documentazione JSON](https://msdn.microsoft.com/library/cc836458(VS.85).aspx) e [il controllo delle versioni e il supporto della versione del motore JavaScript](https://www.microsoft.com/windows/internet-explorer/readiness/developers-new.aspx).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Correzione dei problemi di compatibilità nelle applicazioni Web utilizzando visualizzazione compatibilità](remediating-web-applications-and-add-ons.md)
</dt> </dl>

 

 
