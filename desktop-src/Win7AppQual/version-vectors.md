---
description: Un vettore di versione elabora i commenti condizionali in una pagina Web HTML. Ovvero i vettori di versione consentono di creare markup in base alla versione del browser.
ms.assetid: 526080CD-CE76-48B8-AEBC-6A135FD95BB0
title: Vettori di versione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e41fb0b24a205b280be163caeb63287fc5036b21
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104350546"
---
# <a name="version-vectors"></a>Vettori di versione

Un *vettore di versione* elabora i commenti condizionali in una pagina Web HTML. Ovvero i vettori di versione consentono di creare markup in base alla versione del browser.

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



In questo caso, se la versione del browser Windows Internet Explorer è almeno 5,5, nella pagina Web viene visualizzato il paragrafo corrispondente. Sebbene la prima condizione in questo esempio illustri la funzione dei commenti condizionali, questi commenti non vengono in genere usati per visualizzare markup come la prima condizione. Al contrario, i restanti commenti condizionali nell'esempio precedente sono più frequenti. Nei commenti rimanenti, i commenti condizionali utilizzano un foglio di stile diverso per ogni versione del browser.

Nell'esempio di codice precedente viene inoltre verificata l'uguaglianza per Microsoft Internet Explorer 6 e Windows Internet Explorer 7. Per Windows Internet Explorer 8, tuttavia, nell'esempio viene utilizzato l'operatore GTE (maggiore o uguale a). Questo operatore consente di provare in futuro l'esempio in modo che venga usata la versione più conforme agli standard del foglio di stile quando viene rilasciata una nuova versione del browser, anziché usare il foglio di stile errato o un foglio di stile. Le applicazioni esistenti spesso non considerano una versione di Internet Explorer precedente 7 (o la versione più recente di Internet Explorer per cui è stato compilato il sito). Per ulteriori informazioni sui vettori di versione, vedere la pagina relativa ai [vettori di versione](/previous-versions/cc817577(v=msdn.10)) in MSDN Library.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Correzione dei problemi di compatibilità nelle applicazioni Web utilizzando visualizzazione compatibilità](remediating-web-applications-and-add-ons.md)
</dt> </dl>

 

 



