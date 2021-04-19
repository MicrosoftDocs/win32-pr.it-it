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
# <a name="use-the-meta-tag-to-ensure-future-compatibility"></a><span data-ttu-id="39707-103">Usare il tag meta per garantire la compatibilità futura</span><span class="sxs-lookup"><span data-stu-id="39707-103">Use the Meta Tag to Ensure Future Compatibility</span></span>

<span data-ttu-id="39707-104">Windows Internet Explorer 8 consente di controllare le modalità di compatibilità dei documenti, in modo da consentire al browser di eseguire il rendering delle pagine Web in modo analogo alle versioni precedenti del browser.</span><span class="sxs-lookup"><span data-stu-id="39707-104">Windows Internet Explorer 8 enables you to control document compatibility modes, so you can instruct the browser to render webpages in the same way as older browser versions.</span></span> <span data-ttu-id="39707-105">È anche possibile scegliere quando aggiornare la pagina Web, mentre continua a essere utilizzabile e funziona correttamente.</span><span class="sxs-lookup"><span data-stu-id="39707-105">You can also choose when to update the webpage, while it continues to be usable and function correctly.</span></span>

## <a name="setting-the-meta-element"></a><span data-ttu-id="39707-106">Impostazione dell'elemento meta</span><span class="sxs-lookup"><span data-stu-id="39707-106">Setting the Meta Element</span></span>

<span data-ttu-id="39707-107">L'elemento **meta** include un attributo **Content** che consente di specificare la modalità in cui viene eseguito il rendering del contenuto per la pagina Web, come illustrato nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="39707-107">The **meta** element includes a **content** attribute that enables you to specify the mode that content is rendered in for the webpage, as the following table shows.</span></span>



| <span data-ttu-id="39707-108">Valore</span><span class="sxs-lookup"><span data-stu-id="39707-108">Value</span></span> | <span data-ttu-id="39707-109">Modalità di rendering</span><span class="sxs-lookup"><span data-stu-id="39707-109">Rendering mode</span></span>                                                 |
|-------|----------------------------------------------------------------|
| <span data-ttu-id="39707-110">IE = 9</span><span class="sxs-lookup"><span data-stu-id="39707-110">IE=9</span></span>  | <span data-ttu-id="39707-111">Utilizzare la modalità di rendering standard di Windows Internet Explorer 9</span><span class="sxs-lookup"><span data-stu-id="39707-111">Use the Windows Internet Explorer 9 standards rendering mode</span></span>   |
| <span data-ttu-id="39707-112">IE = 8</span><span class="sxs-lookup"><span data-stu-id="39707-112">IE=8</span></span>  | <span data-ttu-id="39707-113">Utilizzare la modalità di rendering standard di Internet Explorer 8</span><span class="sxs-lookup"><span data-stu-id="39707-113">Use the Internet Explorer 8 standards rendering mode</span></span>           |
| <span data-ttu-id="39707-114">IE = 7</span><span class="sxs-lookup"><span data-stu-id="39707-114">IE=7</span></span>  | <span data-ttu-id="39707-115">Utilizzare la modalità di rendering standard di Windows Internet Explorer 7</span><span class="sxs-lookup"><span data-stu-id="39707-115">Use the Windows Internet Explorer 7 standards rendering mode</span></span>   |
| <span data-ttu-id="39707-116">IE=5</span><span class="sxs-lookup"><span data-stu-id="39707-116">IE=5</span></span>  | <span data-ttu-id="39707-117">Utilizzare la modalità di rendering standard di Microsoft Internet Explorer 5</span><span class="sxs-lookup"><span data-stu-id="39707-117">Use the Microsoft Internet Explorer 5 standards rendering mode</span></span> |



 

<span data-ttu-id="39707-118">Per ulteriori informazioni sulla compatibilità e sull'intestazione X-UA-Compatible, vedere [definizione della compatibilità dei documenti](/previous-versions/windows/internet-explorer/ie-developer/compatibility/cc288325(v=vs.85)) in MSDN Library.</span><span class="sxs-lookup"><span data-stu-id="39707-118">For more information about compatibility and the X-UA-Compatible header, see [Defining Document Compatibility](/previous-versions/windows/internet-explorer/ie-developer/compatibility/cc288325(v=vs.85)) in the MSDN Library.</span></span>

<span data-ttu-id="39707-119">Nell'esempio di codice seguente viene illustrato come forzare il rendering di una pagina Web in modalità Internet Explorer 8.</span><span class="sxs-lookup"><span data-stu-id="39707-119">The following code example demonstrates how to force a webpage to be rendered in Internet Explorer 8 mode.</span></span>


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



## <a name="using-an-http-header"></a><span data-ttu-id="39707-120">Uso di un'intestazione HTTP</span><span class="sxs-lookup"><span data-stu-id="39707-120">Using an HTTP Header</span></span>

<span data-ttu-id="39707-121">Molti siti Web contengono migliaia o decine di migliaia di pagine Web singole, **quindi l'impostazione** del metaelemento su ciascun documento è poco pratica.</span><span class="sxs-lookup"><span data-stu-id="39707-121">Many websites contain thousands (or tens of thousands) of individual webpages so setting the **meta** element on each document is impractical.</span></span> <span data-ttu-id="39707-122">Se si desidera impostare l'elemento **meta** per tutte le pagine o una raccolta di pagine selezionate per cartella, è possibile modificare la configurazione del server e aggiungere i metadati compatibili con X-UA nell' [intestazione HTTP](/previous-versions/cc817572(v=msdn.10)).</span><span class="sxs-lookup"><span data-stu-id="39707-122">If you want to set the **meta** element for all pages or a collection of pages that are selected by folder, you can adjust your server configuration instead and add the X-UA-Compatible metadata in the [HTTP header](/previous-versions/cc817572(v=msdn.10)).</span></span>

<span data-ttu-id="39707-123">Per i siti che richiedono valori di **metadati** diversi per le pagine nello stesso server, sono disponibili diversi strumenti che generano automaticamente e inseriscono l'elemento **meta** appropriato.</span><span class="sxs-lookup"><span data-stu-id="39707-123">For sites that require different **meta** element values for pages on the same server, there are several tools that automatically generate and insert the appropriate **meta** element for you.</span></span> <span data-ttu-id="39707-124">Ad esempio, l'utilità [ArtinSoft Web Tools](https://www.mobilize.net/what-is-aggiorno-ie8-compatibility-tagging.aspx) di aggiorno inserisce e rimuove la funzionalità tag di compatibilità di Internet Explorer 8 e può aiutare il sito a soddisfare standard di compatibilità specifici.</span><span class="sxs-lookup"><span data-stu-id="39707-124">For example, the [ArtinSoft Web Tools](https://www.mobilize.net/what-is-aggiorno-ie8-compatibility-tagging.aspx) utility from Aggiorno inserts and removes the Internet Explorer 8 compatibility tag feature and can help your site meet specific compatibility standards.</span></span>

## <a name="related-topics"></a><span data-ttu-id="39707-125">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="39707-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="39707-126">Correzione dei problemi di compatibilità nelle applicazioni Web utilizzando visualizzazione compatibilità</span><span class="sxs-lookup"><span data-stu-id="39707-126">Fixing Compatibility Issues in Web Applications by Using Compatibility View</span></span>](remediating-web-applications-with-compatibility-view.md)
</dt> </dl>

 

 
