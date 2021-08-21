---
description: JavaScript Object Notation (JSON)
ms.assetid: 2F6FDE88-C852-46BC-B6B1-630C266AF0AA
title: JavaScript Object Notation (JSON)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 970737e7f19c5043c418941351ea82537b36a4a2429c44428a90031699458525
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119053079"
---
# <a name="javascript-object-notation-json"></a>JavaScript Object Notation (JSON)

[JavaScript Object Notation (JSON)](https://www.json.org/) è un formato di interscambio dati semplice e leggero basato su un subset della notazione letterale oggetto del linguaggio JavaScript. Il motore JavaScript in Windows Internet Explorer 8 implementa la proposta [JSON ECMAScript 3.1](https://www.ecma-international.org/) per le funzioni di gestione JSON native (che usa l'API json2.js di [Douglas Crockford).](https://github.com/douglascrockford/JSON-js/blob/master/json2.js)

Internet Explorer 8 include un oggetto JSON nativo conforme al supporto JSON descritto nella Bozza di lavoro della proposta [ES3.1.](https://www.ecma-international.org/) Alcune pagine Web rilevano l'oggetto JSON nativo e quindi lo usano in modo non standard. Questo utilizzo causa in genere un errore di script e interrompe la gestione delle richieste AJAX. L'esempio di codice seguente illustra il modo errato di usare l'oggetto JSON.


```JScript
    if(!window.JSON) JSON = myJSON; 
    JSON.encode(obj); // Not part of the standard
```



L'esempio di codice seguente illustra invece un buon modo per usare l'oggetto JSON.


```JScript
    JSON = myJSON; 
    JSON.encode(obj);
```



Windows Internet Explorer include il supporto nativo per JSON introducendo un oggetto JSON globale con due metodi predefiniti: **stringify** e **parse.** L'oggetto JSON globale viene definito nel motore JavaScript e viene creato durante la fase di inizializzazione del motore. Per mantenere la compatibilità con le versioni precedenti, questa funzionalità è disponibile solo quando un sito Web usa la versione più recente delle funzionalità JavaScript usando la modalità di layout "standard Internet Explorer 8" (documento). Questa funzionalità può anche influire sul comportamento delle pagine Web che dipendono da una variabile globale JSON o usano [json2.js](https://github.com/douglascrockford/JSON-js/blob/master/json2.js).

È possibile eseguire l'override dell'oggetto JSON globale. Tuttavia, quando una pagina Web usa la modalità layout (documento) "Internet Explorer 8 Standard", non è più un oggetto non definito. Poiché viene creata un'istanza di JSON come nome globale dal motore JavaScript, i controlli come "if(!this.JSON)" restituiscono False e devono essere modificati nel codice utente.

Le pagine Web che [ usanojson2.js](https://github.com/douglascrockford/JSON-js/blob/master/json2.js) non sono probabilmente interessate. Con poche eccezioni, queste pagine dovrebbero funzionare più velocemente. Le eccezioni sono causate dalle differenze tra l'Internet Explorer'implementazione JSON nativa e json2.js. Durante la serializzazione, ad esempio, l'implementazione JSON nativa rileva i cicli e non esegue una ricorsione infinita come json.js. Per altre informazioni su queste eccezioni, vedere i [blog di JavaScript](/archive/blogs/jscript/).

Per altre informazioni, vedere [Documentazione JSON](https://msdn.microsoft.com/library/cc836458(VS.85).aspx) e [Controllo delle versioni e Supporto della versione del motore JavaScript.](https://www.microsoft.com/windows/internet-explorer/readiness/developers-new.aspx)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Correzione dei problemi di compatibilità nelle applicazioni Web tramite Visualizzazione Compatibilità](remediating-web-applications-and-add-ons.md)
</dt> </dl>

 

 
