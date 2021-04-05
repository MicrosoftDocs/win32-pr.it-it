---
title: Creazione dinamica del documento ServiceInfo
description: Creazione dinamica del documento ServiceInfo
ms.assetid: 96937b04-f705-49f6-8ddf-25c98a51dc9a
keywords:
- Windows Media Player Online Stores, creazione di un documento ServiceInfo
- archivi online, creazione di un documento ServiceInfo
- digitare 1 negozi online, creazione del documento ServiceInfo
- digitare 2 archivi online, creazione del documento ServiceInfo
- Windows Media Player Online Stores, creazione dinamica del documento ServiceInfo
- negozi online, creazione dinamica di documenti ServiceInfo
- digitare 1 negozi online, creazione dinamica del documento ServiceInfo
- digitare 2 archivi online, creazione dinamica del documento ServiceInfo
- Windows Media Player Online Stores, documento ServiceInfo
- archivi online, documento ServiceInfo
- digitare 1 negozi online, documento ServiceInfo
- digitare 2 archivi online, documento ServiceInfo
- creazione dinamica di un documento ServiceInfo
- creazione del documento ServiceInfo
- Documento ServiceInfo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 90159e72046536cf6b69521586a0640935478eb1
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103955181"
---
# <a name="creating-the-serviceinfo-document-dynamically"></a><span data-ttu-id="df5cf-118">Creazione dinamica del documento ServiceInfo</span><span class="sxs-lookup"><span data-stu-id="df5cf-118">Creating the ServiceInfo Document Dynamically</span></span>

<span data-ttu-id="df5cf-119">Per creare il documento ServiceInfo, è possibile utilizzare ASP.</span><span class="sxs-lookup"><span data-stu-id="df5cf-119">You can use ASP to create your ServiceInfo document.</span></span> <span data-ttu-id="df5cf-120">Questo consente di ottenere una maggiore flessibilità nel negozio online usando le tecniche seguenti:</span><span class="sxs-lookup"><span data-stu-id="df5cf-120">This can give you greater flexibility in your online store by using the following techniques:</span></span>

-   <span data-ttu-id="df5cf-121">Generazione dinamica del nome host per gli URL.</span><span class="sxs-lookup"><span data-stu-id="df5cf-121">Dynamically generating the host name for URLs.</span></span>
-   <span data-ttu-id="df5cf-122">Modifica degli URL per la localizzazione in base ai parametri delle impostazioni locali e di Geoid.</span><span class="sxs-lookup"><span data-stu-id="df5cf-122">Changing URLs for localization based on locale and geoid parameters.</span></span>
-   <span data-ttu-id="df5cf-123">Accodare dinamicamente i parametri della stringa di query dall'URL ServiceInfo ad altri URL, ad esempio l'URL della pagina Navigate.</span><span class="sxs-lookup"><span data-stu-id="df5cf-123">Dynamically appending query string parameters from the ServiceInfo URL to other URLs, such as the navigate page URL.</span></span>

<span data-ttu-id="df5cf-124">Il codice di esempio seguente mostra una pagina ASP semplice che crea dinamicamente un documento ServiceInfo:</span><span class="sxs-lookup"><span data-stu-id="df5cf-124">The following example code shows a simple ASP page that dynamically creates a ServiceInfo document:</span></span>


```C++
<%
    Dim sHost
    Dim sLocale

    sHost = Request.ServerVariables("HTTP_HOST")
    sLocale = Request.QueryString("locale")
%>

<?xml version="1.0" encoding="utf-8"?>
<ServiceInfo Version="1.00" Key="MyCommerceService">
    <FriendlyName>My Online Store</FriendlyName>
    <ServiceTask1
        URL = "https://<%= sHost %>/service/html/Music.asp">
    </ServiceTask1>
    <ServiceTask2
        URL = "https://<%= sHost %>/service/html/Video.asp">
    </ServiceTask2>
    <ServiceTask3
        URL = "https://<%= sHost %>/service/html/Radio.asp">
    </ServiceTask3>
    <Navigate
        BaseURL = "https://<%= sHost %>/service/html/navigate.asp?myloc<%= sLocale %>">
    </Navigate>
</ServiceInfo>
```



<span data-ttu-id="df5cf-125">Il codice di esempio precedente utilizza ASP per recuperare il nome host dal server Web e creare in modo dinamico gli URL nel documento.</span><span class="sxs-lookup"><span data-stu-id="df5cf-125">The preceding example code uses ASP to retrieve the host name from the web server and dynamically create the URLs in the document.</span></span> <span data-ttu-id="df5cf-126">Il codice recupera anche il parametro della stringa di query delle *impostazioni locali* dalla richiesta ServiceInfo e lo aggiunge all'URL per la pagina Navigate.</span><span class="sxs-lookup"><span data-stu-id="df5cf-126">The code also retrieves the *locale* query string parameter from the ServiceInfo request and appends it to the URL for the navigate page.</span></span>

## <a name="related-topics"></a><span data-ttu-id="df5cf-127">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="df5cf-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="df5cf-128">**Informazioni comuni ai negozi online di tipo 1 e di tipo 2**</span><span class="sxs-lookup"><span data-stu-id="df5cf-128">**Information Common to Type 1 and Type 2 Online Stores**</span></span>](information-common-to-type-1-and-type-2-online-stores.md)
</dt> <dt>

[<span data-ttu-id="df5cf-129">**Navigazione per i negozi di tipo 2 online**</span><span class="sxs-lookup"><span data-stu-id="df5cf-129">**Navigation for Type 2 Online Stores**</span></span>](navigation-for-type-2-online-stores.md)
</dt> <dt>

[<span data-ttu-id="df5cf-130">**Documento ServiceInfo per un negozio online di tipo 1**</span><span class="sxs-lookup"><span data-stu-id="df5cf-130">**ServiceInfo Document for a Type 1 Online Store**</span></span>](serviceinfo-document-for-a-type-1-online-store.md)
</dt> <dt>

[<span data-ttu-id="df5cf-131">**Documento ServiceInfo per un negozio online di tipo 2**</span><span class="sxs-lookup"><span data-stu-id="df5cf-131">**ServiceInfo Document for a Type 2 Online Store**</span></span>](serviceinfo-document-for-a-type-2-online-store.md)
</dt> <dt>

[<span data-ttu-id="df5cf-132">**Documento ServiceInfo**</span><span class="sxs-lookup"><span data-stu-id="df5cf-132">**ServiceInfo Document**</span></span>](serviceinfo-document.md)
</dt> </dl>

 

 




