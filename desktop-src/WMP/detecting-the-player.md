---
title: Rilevamento del lettore
description: Rilevamento del lettore
ms.assetid: dc034226-578a-45de-9463-e1798fef874e
keywords:
- Windows Media Player Online Stores, rilevamento di giocatori
- negozi online, rilevamento di giocatori
- digitare 1 negozi online, rilevamento di giocatori
- digitare 2 archivi online, rilevamento di giocatori
- Windows Media Player Online Stores, rilevamento giocatori
- archivi online, rilevamento di giocatori
- digitare 1 negozi online, rilevamento del lettore
- digitare 2 archivi online, rilevamento del lettore
- rilevamento del lettore
- rilevamento di giocatori
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cb919e790b07ccf5d8df587abd63d2344534b16b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103955547"
---
# <a name="detecting-the-player"></a><span data-ttu-id="4c6b3-113">Rilevamento del lettore</span><span class="sxs-lookup"><span data-stu-id="4c6b3-113">Detecting the Player</span></span>

<span data-ttu-id="4c6b3-114">Quando si crea una pagina Web per il negozio online, è possibile decidere se si desidera che gli utenti siano in grado di visualizzare la pagina in un Web browser o in Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="4c6b3-114">When creating a webpage for your online store, you may decide that you want users to be able to view the page in a Web browser or in Windows Media Player.</span></span> <span data-ttu-id="4c6b3-115">Per determinare se la pagina Web è ospitata nel lettore, è possibile usare uno script ASP.</span><span class="sxs-lookup"><span data-stu-id="4c6b3-115">You can use an ASP script to determine whether your webpage is hosted in the Player.</span></span>

<span data-ttu-id="4c6b3-116">Il codice di esempio seguente recupera il parametro version dalla stringa di query dell'URL per determinare se la pagina è ospitata in Windows Media Player:</span><span class="sxs-lookup"><span data-stu-id="4c6b3-116">The following example code retrieves the version parameter from the URL query string to determine whether the page is hosted in Windows Media Player:</span></span>


```C++
<%
    Dim sVersion

    sVersion = Trim(Request.QueryString("version")) 
 
    If sVersion = "" Then   
        Response.Write "Not hosted in Windows Media Player"
    Else 
        Response.Write "Hosted in Windows Media Player<BR>"
        Response.Write "Version is " & sVersion
    End If
%>
```



<span data-ttu-id="4c6b3-117">Si noti che il codice precedente presuppone che il parametro version esista nella stringa di query quando è ospitato in Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="4c6b3-117">Note that the preceding code assumes that the version parameter exists in the query string when hosted in Windows Media Player.</span></span> <span data-ttu-id="4c6b3-118">Questo vale per le pagine aperte dall'utente, ma potrebbe non essere true per le pagine aperte tramite **External. NavigateTaskPaneURL**.</span><span class="sxs-lookup"><span data-stu-id="4c6b3-118">This is true for pages opened by the user, but may not be true for pages opened by using **External.NavigateTaskPaneURL**.</span></span> <span data-ttu-id="4c6b3-119">Affinché la stringa di query della versione esista durante la navigazione a livello di codice, è necessario aggiungere il parametro version alla chiamata al metodo o accodare dinamicamente la versione all'URL di base dell'elemento **Navigate** del documento ServiceInfo.</span><span class="sxs-lookup"><span data-stu-id="4c6b3-119">For the version query string to exist when navigating programmatically, you must add the version parameter to the method call or dynamically append the version to the base URL of the **Navigate** element of your ServiceInfo document.</span></span>

## <a name="related-topics"></a><span data-ttu-id="4c6b3-120">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="4c6b3-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4c6b3-121">**Creazione dinamica del documento ServiceInfo**</span><span class="sxs-lookup"><span data-stu-id="4c6b3-121">**Creating the ServiceInfo Document Dynamically**</span></span>](creating-the-serviceinfo-document-dynamically.md)
</dt> <dt>

[<span data-ttu-id="4c6b3-122">**External. NavigateTaskPaneURL**</span><span class="sxs-lookup"><span data-stu-id="4c6b3-122">**External.NavigateTaskPaneURL**</span></span>](external-navigatetaskpaneurl.md)
</dt> <dt>

[<span data-ttu-id="4c6b3-123">**Informazioni comuni ai negozi online di tipo 1 e di tipo 2**</span><span class="sxs-lookup"><span data-stu-id="4c6b3-123">**Information Common to Type 1 and Type 2 Online Stores**</span></span>](information-common-to-type-1-and-type-2-online-stores.md)
</dt> </dl>

 

 




