---
description: .
ms.assetid: F9907D49-F9FE-406A-BF5F-17C61706ADC1
title: AJAX
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e140604846570b523910bb8ab815b185f26fa4dd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103968556"
---
# <a name="ajax"></a>AJAX

Le funzionalità AJAX in Windows Internet Explorer 8 come [**XDomainRequest (XDR)**](https://msdn.microsoft.com/library/Cc288060(v=VS.85).aspx) e la [messaggistica tra documenti (XDM)](https://download.microsoft.com/download/7/0/D/70D193BF-F818-4539-8325-A2F321C3061E/Cross Document Messaging - Developer Series Information Page.pdf) hanno proprietà native che possono entrare in conflitto con le proprietà personalizzate esistenti.

Windows Internet Explorer espone nuove proprietà per determinate funzionalità AJAX, ad esempio la [messaggistica tra documenti (XDM)](https://download.microsoft.com/download/7/0/D/70D193BF-F818-4539-8325-A2F321C3061E/Cross Document Messaging - Developer Series Information Page.pdf), anche in visualizzazione compatibilità. Se si aggiungono proprietà personalizzate all'oggetto evento, è possibile che si verifichino conflitti con queste nuove proprietà, ad esempio **source**.

L'esempio di codice seguente funziona nelle versioni precedenti di Internet Explorer, ma non nelle versioni più recenti perché le nuove funzionalità usano la proprietà **source** .


```JScript
event.source = myObject;
```



Nell'esempio di codice riportato di seguito viene illustrato come è possibile modificare questo oggetto per rimanere compatibile.


```JScript
event.mySource = myObject;// Read-only in IE8, use mySource instead
```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Correzione dei problemi di compatibilità nelle applicazioni Web utilizzando visualizzazione compatibilità](remediating-web-applications-and-add-ons.md)
</dt> </dl>

 

 



