---
description: AJAX
ms.assetid: F9907D49-F9FE-406A-BF5F-17C61706ADC1
title: AJAX
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 575ab08530936ab083baa4bb3fcfa2956ffe3b2d
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108088759"
---
# <a name="ajax"></a>AJAX

Le funzionalità AJAX in Windows Internet Explorer 8 come [**XDomainRequest (XDR)**](https://msdn.microsoft.com/library/Cc288060(v=VS.85).aspx) e [XDM (Cross-Document Messaging)](https://download.microsoft.com/download/7/0/D/70D193BF-F818-4539-8325-A2F321C3061E/Cross Document Messaging - Developer Series Information Page.pdf) hanno proprietà native che potrebbero essere in conflitto con le proprietà personalizzate esistenti.

Windows Internet Explorer espone nuove proprietà per determinate funzionalità AJAX, ad esempio [XDM (Cross-Document Messaging),](https://download.microsoft.com/download/7/0/D/70D193BF-F818-4539-8325-A2F321C3061E/Cross Document Messaging - Developer Series Information Page.pdf)anche in Visualizzazione Compatibilità. Se si aggiungono proprietà personalizzate all'oggetto evento, queste potrebbero essere in conflitto con queste nuove proprietà, ad esempio **source.**

L'esempio di codice seguente funziona nelle versioni precedenti di Internet Explorer ma non nelle versioni più recenti perché le nuove funzionalità usano la **proprietà di** origine .


```JScript
event.source = myObject;
```



Nell'esempio di codice seguente viene illustrato come modificare questo oggetto in modo che rimanga compatibile.


```JScript
event.mySource = myObject;// Read-only in IE8, use mySource instead
```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Correzione dei problemi di compatibilità nelle applicazioni Web tramite Visualizzazione Compatibilità](remediating-web-applications-and-add-ons.md)
</dt> </dl>

 

 



