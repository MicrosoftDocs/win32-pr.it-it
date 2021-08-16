---
description: Un vettore di versione elabora i commenti condizionali in una pagina Web HTML. Ciò significa che i vettori di versione consentono di creare markup in base alla versione del browser.
ms.assetid: 526080CD-CE76-48B8-AEBC-6A135FD95BB0
title: Vettori di versione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4b7ba3fb77d13ce6aa08a095f4ae95e88c1ffaecf57251b7d9ad718f51be3326
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118328607"
---
# <a name="version-vectors"></a>Vettori di versione

Un *vettore di* versione elabora i commenti condizionali in una pagina Web HTML. Ciò significa che i vettori di versione consentono di creare markup in base alla versione del browser.

Osservare l'esempio di codice seguente.


```HTML
<!-[if gte IE 5.5]
   <p>you are using IE5 or higher</p>
<![endif]->
<!-[if IE6]
   <linkrel=”stylesheet” type=”text/css” href=”/stylesheets/ie6.css”/>
<![endif]->
<!-[if IE7]
   <linkrel=”stylesheet” type=”text/css” href=”/stylesheets/ie7.css”/>
<![endif]->
<!-[if gte IE8]
   <linkrel=”stylesheet” type=”text/css” href=”/stylesheets/standards.css”/>
<![endif]->
```



In questo caso, se la Windows Internet Explorer del browser è almeno 5.5, il paragrafo corrispondente viene visualizzato nella pagina Web. Anche se la prima condizione in questo esempio illustra la funzione dei commenti condizionali, questi commenti non vengono in genere usati per visualizzare markup come la prima condizione. I commenti condizionali rimanenti nell'esempio precedente sono invece più comuni. In questi commenti rimanenti, i commenti condizionali usano un foglio di stile diverso per ogni versione diversa del browser.

L'esempio di codice precedente verifica anche l'uguaglianza per Microsoft Internet Explorer 6 e Windows Internet Explorer 7. Tuttavia, Windows Internet Explorer 8, nell'esempio viene utilizzato l'operatore gte (maggiore o uguale a). Questo operatore consente di a prova di futuro l'esempio in modo che la versione più conforme agli standard del foglio di stile viene usata quando viene rilasciata una nuova versione del browser (invece di usare il foglio di stile errato o nessun foglio di stile). Le applicazioni esistenti spesso non considerano una versione di Internet Explorer 7 o la versione più recente di Internet Explorer per cui è stato creato il sito. Per altre informazioni sui vettori di versione, vedere [Vettori di versione](/previous-versions/cc817577(v=msdn.10)) in MSDN Library.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Correzione dei problemi di compatibilità nelle applicazioni Web tramite Visualizzazione Compatibilità](remediating-web-applications-and-add-ons.md)
</dt> </dl>

 

 



