---
description: Usare il tag Meta per garantire la compatibilità futura
ms.assetid: 254A1C0D-B24B-4014-8D15-662FC7F2AB81
title: Usare il tag Meta per garantire la compatibilità futura
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9c0cff3dab146d67303d57c97b2298614c5ae0142b18a3bd2d141fbf90e86ce8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118994591"
---
# <a name="use-the-meta-tag-to-ensure-future-compatibility"></a>Usare il tag Meta per garantire la compatibilità futura

Windows Internet Explorer 8 consente di controllare le modalità di compatibilità dei documenti, quindi è possibile indicare al browser di eseguire il rendering delle pagine Web nello stesso modo delle versioni precedenti del browser. È anche possibile scegliere quando aggiornare la pagina Web, pur continuando a essere utilizzabile e funzionare correttamente.

## <a name="setting-the-meta-element"></a>Impostazione dell'elemento Meta

**L'elemento meta** include **un attributo content** che consente di specificare la modalità di rendering del contenuto per la pagina Web, come illustrato nella tabella seguente.



| Valore | Modalità di rendering                                                 |
|-------|----------------------------------------------------------------|
| IE=9  | Usare la modalità Windows Internet Explorer rendering standard di Windows Internet Explorer 9   |
| IE=8  | Usare la modalità di rendering Internet Explorer 8 standard           |
| IE=7  | Usare la modalità di rendering Windows Internet Explorer 7 standard   |
| IE=5  | Usare la modalità di rendering standard di Microsoft Internet Explorer 5 |



 

Per altre informazioni sulla compatibilità e sull'intestazione compatibile con X-UA, vedere [Definizione della compatibilità dei](/previous-versions/windows/internet-explorer/ie-developer/compatibility/cc288325(v=vs.85)) documenti in MSDN Library.

Nell'esempio di codice seguente viene illustrato come forzare il rendering di una pagina Web Internet Explorer modalità 8.


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

Molti siti Web contengono migliaia (o decine di migliaia) di singole pagine Web, quindi l'impostazione dell'elemento **meta** in ogni documento non è pratica. Se si vuole impostare l'elemento **meta** per tutte le pagine o una raccolta di pagine selezionate per cartella, è possibile modificare la configurazione del server e aggiungere i metadati compatibili con X-UA nell'intestazione [HTTP](/previous-versions/cc817572(v=msdn.10)).

Per i siti che richiedono **valori di meta-elemento** diversi per le pagine nello stesso server, sono disponibili diversi strumenti che generano e inseriscono automaticamente l'elemento **meta** appropriato. Ad esempio, l'utilità [Strumenti Web ArtinSoft](https://www.mobilize.net/what-is-aggiorno-ie8-compatibility-tagging.aspx) di Agtura inserisce e rimuove la funzionalità dei tag di compatibilità di Internet Explorer 8 e può aiutare il sito a soddisfare standard di compatibilità specifici.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Correzione dei problemi di compatibilità nelle applicazioni Web tramite Visualizzazione Compatibilità](remediating-web-applications-with-compatibility-view.md)
</dt> </dl>

 

 
