---
description: .
ms.assetid: 254A1C0D-B24B-4014-8D15-662FC7F2AB81
title: Usare il tag meta per garantire la compatibilità futura
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5e965711053a7108c69295ac737953a05536a76e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106319829"
---
# <a name="use-the-meta-tag-to-ensure-future-compatibility"></a>Usare il tag meta per garantire la compatibilità futura

Windows Internet Explorer 8 consente di controllare le modalità di compatibilità dei documenti, in modo da consentire al browser di eseguire il rendering delle pagine Web in modo analogo alle versioni precedenti del browser. È anche possibile scegliere quando aggiornare la pagina Web, mentre continua a essere utilizzabile e funziona correttamente.

## <a name="setting-the-meta-element"></a>Impostazione dell'elemento meta

L'elemento **meta** include un attributo **Content** che consente di specificare la modalità in cui viene eseguito il rendering del contenuto per la pagina Web, come illustrato nella tabella seguente.



| Valore | Modalità di rendering                                                 |
|-------|----------------------------------------------------------------|
| IE = 9  | Utilizzare la modalità di rendering standard di Windows Internet Explorer 9   |
| IE = 8  | Utilizzare la modalità di rendering standard di Internet Explorer 8           |
| IE = 7  | Utilizzare la modalità di rendering standard di Windows Internet Explorer 7   |
| IE=5  | Utilizzare la modalità di rendering standard di Microsoft Internet Explorer 5 |



 

Per ulteriori informazioni sulla compatibilità e sull'intestazione X-UA-Compatible, vedere [definizione della compatibilità dei documenti](/previous-versions/windows/internet-explorer/ie-developer/compatibility/cc288325(v=vs.85)) in MSDN Library.

Nell'esempio di codice seguente viene illustrato come forzare il rendering di una pagina Web in modalità Internet Explorer 8.


```HTML
<html>
   <head>
   <!-- Mimic Internet Explorer 8 -->
      <title>My Web Page</title>
      <meta http-equiv="X-UA-Compatible" content="IE=EmulateIE8" />
   </head>
   <body>
      <p>Content goes here.</p>
   </body>
</html>
```



## <a name="using-an-http-header"></a>Uso di un'intestazione HTTP

Molti siti Web contengono migliaia o decine di migliaia di pagine Web singole, **quindi l'impostazione** del metaelemento su ciascun documento è poco pratica. Se si desidera impostare l'elemento **meta** per tutte le pagine o una raccolta di pagine selezionate per cartella, è possibile modificare la configurazione del server e aggiungere i metadati compatibili con X-UA nell' [intestazione HTTP](/previous-versions/cc817572(v=msdn.10)).

Per i siti che richiedono valori di **metadati** diversi per le pagine nello stesso server, sono disponibili diversi strumenti che generano automaticamente e inseriscono l'elemento **meta** appropriato. Ad esempio, l'utilità [ArtinSoft Web Tools](https://www.mobilize.net/what-is-aggiorno-ie8-compatibility-tagging.aspx) di aggiorno inserisce e rimuove la funzionalità tag di compatibilità di Internet Explorer 8 e può aiutare il sito a soddisfare standard di compatibilità specifici.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Correzione dei problemi di compatibilità nelle applicazioni Web utilizzando visualizzazione compatibilità](remediating-web-applications-with-compatibility-view.md)
</dt> </dl>

 

 
