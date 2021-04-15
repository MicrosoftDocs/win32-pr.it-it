---
title: Chiamata delle funzioni
description: Chiamata delle funzioni
ms.assetid: c5a675f2-86fc-4f53-8d09-604ab4752d7b
keywords:
- Interfacce di Media Player Windows, chiamata di funzioni in JScript
- interfacce, chiamata di funzioni in JScript
- chiamata di funzioni in JScript
- File JScript per interfacce, chiamate di funzioni
- Windows Media Player Skin, attributo scriptFile in JScript
- interfacce, attributo scriptFile in JScript
- attributi, scriptFile in JScript
- attributo scriptFile in JScript
- File JScript per interfacce, attributo scriptFile
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a9450c8ca09b75f66f6206c850a656192bb1bb9b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104516078"
---
# <a name="calling-functions"></a>Chiamata delle funzioni

Se è necessario chiamare più righe di codice, è possibile caricare un file di script usando l'attributo **scriptFile** dell'elemento **View** e chiamare le funzioni nello script. È possibile caricare più di un file per visualizzazione:


```C++
scriptFile = "myfile1.js;myfile2.js;myfile3.js"

```



Una volta caricati i file di script, è possibile chiamare le funzioni all'interno della sezione di visualizzazione. Ad esempio, per chiamare una *funzione denominata Function* quando si fa clic su un elemento, digitare quanto segue:


```C++
onclick = "JScript: myfunction()"

```



> [!Note]  
> Se si dispone di più di una vista, solo le funzioni nei file caricati nella visualizzazione corrente sono disponibili per il codice XML e JScript in esecuzione con la visualizzazione corrente. I file caricati in altre viste non si trovano nell'ambito della visualizzazione corrente.

 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Utilizzo di JScript**](using-jscript.md)
</dt> </dl>

 

 




