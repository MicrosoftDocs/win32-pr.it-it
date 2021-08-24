---
title: Chiamata delle funzioni
description: Chiamata delle funzioni
ms.assetid: c5a675f2-86fc-4f53-8d09-604ab4752d7b
keywords:
- Windows Media Player, chiamata di funzioni in JScript
- interfaccia, chiamata di funzioni in JScript
- chiamata di funzioni in JScript
- JScript file per le interfaccia, chiamata di funzioni
- Windows Media Player, attributo scriptFile in JScript
- attributo skins,scriptFile in JScript
- attributi,scriptFile in JScript
- Attributo scriptFile in JScript
- JScript per le interfaccia, attributo scriptFile
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4e41b5fdfd6109292a1a42cae43e42e8424348090541fd50a8d83f04d23b8329
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119764271"
---
# <a name="calling-functions"></a>Chiamata delle funzioni

Se è necessario chiamare più righe di codice, è possibile caricare un file script usando l'attributo **scriptFile** dell'elemento **VIEW** e chiamare le funzioni nello script. È possibile caricare più di un file per ogni visualizzazione:


```C++
scriptFile = "myfile1.js;myfile2.js;myfile3.js"

```



Dopo aver caricato i file di script, è possibile chiamare le funzioni all'interno della sezione View. Ad esempio, per chiamare una funzione denominata *myfunction quando* si fa clic su un elemento, digitare quanto segue:


```C++
onclick = "JScript: myfunction()"

```



> [!Note]  
> Se si dispone di più di una visualizzazione, solo le funzioni nei file caricati nella visualizzazione corrente sono disponibili per il codice XML e JScript in esecuzione con la visualizzazione corrente. I file caricati in altre visualizzazioni non sono nell'ambito della visualizzazione corrente.

 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Uso di JScript**](using-jscript.md)
</dt> </dl>

 

 




