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
# <a name="ajax"></a><span data-ttu-id="f9e92-103">AJAX</span><span class="sxs-lookup"><span data-stu-id="f9e92-103">AJAX</span></span>

<span data-ttu-id="f9e92-104">Le funzionalità AJAX in Windows Internet Explorer 8 come [**XDomainRequest (XDR)**](https://msdn.microsoft.com/library/Cc288060(v=VS.85).aspx) e la [messaggistica tra documenti (XDM)](https://download.microsoft.com/download/7/0/D/70D193BF-F818-4539-8325-A2F321C3061E/Cross Document Messaging - Developer Series Information Page.pdf) hanno proprietà native che possono entrare in conflitto con le proprietà personalizzate esistenti.</span><span class="sxs-lookup"><span data-stu-id="f9e92-104">AJAX features in Windows Internet Explorer 8 like [**XDomainRequest (XDR)**](https://msdn.microsoft.com/library/Cc288060(v=VS.85).aspx) and [Cross-Document Messaging (XDM)](https://download.microsoft.com/download/7/0/D/70D193BF-F818-4539-8325-A2F321C3061E/Cross Document Messaging - Developer Series Information Page.pdf) have native properties that might conflict with existing custom properties.</span></span>

<span data-ttu-id="f9e92-105">Windows Internet Explorer espone nuove proprietà per determinate funzionalità AJAX, ad esempio la [messaggistica tra documenti (XDM)](https://download.microsoft.com/download/7/0/D/70D193BF-F818-4539-8325-A2F321C3061E/Cross Document Messaging - Developer Series Information Page.pdf), anche in visualizzazione compatibilità.</span><span class="sxs-lookup"><span data-stu-id="f9e92-105">Windows Internet Explorer exposes new properties for certain AJAX features, such as [Cross-Document Messaging (XDM)](https://download.microsoft.com/download/7/0/D/70D193BF-F818-4539-8325-A2F321C3061E/Cross Document Messaging - Developer Series Information Page.pdf), even in Compatibility View.</span></span> <span data-ttu-id="f9e92-106">Se si aggiungono proprietà personalizzate all'oggetto evento, è possibile che si verifichino conflitti con queste nuove proprietà, ad esempio **source**.</span><span class="sxs-lookup"><span data-stu-id="f9e92-106">If you add custom properties to the event object, they might conflict with these new properties, such as **source**.</span></span>

<span data-ttu-id="f9e92-107">L'esempio di codice seguente funziona nelle versioni precedenti di Internet Explorer, ma non nelle versioni più recenti perché le nuove funzionalità usano la proprietà **source** .</span><span class="sxs-lookup"><span data-stu-id="f9e92-107">The following code example works in older versions of Internet Explorer but not in newer versions because new features use the **source** property.</span></span>


```JScript
event.source = myObject;
```



<span data-ttu-id="f9e92-108">Nell'esempio di codice riportato di seguito viene illustrato come è possibile modificare questo oggetto per rimanere compatibile.</span><span class="sxs-lookup"><span data-stu-id="f9e92-108">The following code example shows how you can change this object to remain compatible.</span></span>


```JScript
event.mySource = myObject;// Read-only in IE8, use mySource instead
```



## <a name="related-topics"></a><span data-ttu-id="f9e92-109">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="f9e92-109">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f9e92-110">Correzione dei problemi di compatibilità nelle applicazioni Web utilizzando visualizzazione compatibilità</span><span class="sxs-lookup"><span data-stu-id="f9e92-110">Fixing Compatibility Issues in Web Applications by Using Compatibility View</span></span>](remediating-web-applications-and-add-ons.md)
</dt> </dl>

 

 



