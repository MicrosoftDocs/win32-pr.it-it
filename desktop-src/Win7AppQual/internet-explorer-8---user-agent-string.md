---
description: Internet Explorer 8 - Stringa agente utente
ms.assetid: 1cb0456d-501a-4272-b89d-35e79d29d13a
title: Internet Explorer 8 - Stringa agente utente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d94d60930466b7243ad6ecc2b2d8d9c799e0e3da
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108088239"
---
# <a name="internet-explorer-8---user-agent-string"></a><span data-ttu-id="4f508-103">Internet Explorer 8 - Stringa agente utente</span><span class="sxs-lookup"><span data-stu-id="4f508-103">Internet Explorer 8 - User Agent String</span></span>

## <a name="affected-platforms"></a><span data-ttu-id="4f508-104">Piattaforme interessate</span><span class="sxs-lookup"><span data-stu-id="4f508-104">Affected Platforms</span></span>

 <span data-ttu-id="4f508-105">**Client** - Windows XP, Windows Vista, Windows 7</span><span class="sxs-lookup"><span data-stu-id="4f508-105">**Clients** - Windows XP, Windows Vista, Windows 7</span></span>  
<span data-ttu-id="4f508-106">**Server** - Windows Server 2003, Windows Server 2008, Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="4f508-106">**Servers** - Windows Server 2003, Windows Server 2008, Windows Server 2008 R2</span></span>  










## <a name="feature-impact"></a><span data-ttu-id="4f508-107">Impatto sulle funzionalità</span><span class="sxs-lookup"><span data-stu-id="4f508-107">Feature Impact</span></span>

<span data-ttu-id="4f508-108">**Gravità** - Media</span><span class="sxs-lookup"><span data-stu-id="4f508-108">**Severity** - Medium</span></span>  
<span data-ttu-id="4f508-109">**Frequenza** - Alta</span><span class="sxs-lookup"><span data-stu-id="4f508-109">**Frequency** - High</span></span>  











## <a name="description"></a><span data-ttu-id="4f508-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="4f508-110">Description</span></span>

<span data-ttu-id="4f508-111">User Agent String è l'identificatore Internet Explorer che fornisce i dati sulla relativa versione e altri attributi ai server Web.</span><span class="sxs-lookup"><span data-stu-id="4f508-111">The User Agent String is the Internet Explorer identifier that provides data about its version and other attributes to web servers.</span></span> <span data-ttu-id="4f508-112">Molte applicazioni Web si basano sulla stringa agente utente IE e su cui si basa piggyback.</span><span class="sxs-lookup"><span data-stu-id="4f508-112">Many web applications rely on, and piggyback on, the IE User Agent String.</span></span> <span data-ttu-id="4f508-113">Saranno influenzati quelli che e dipendono da un numero di versione precedente.</span><span class="sxs-lookup"><span data-stu-id="4f508-113">Those that do so and depend on an earlier version number will be impacted.</span></span> <span data-ttu-id="4f508-114">La stringa Agente utente include ora la stringa "Trident/4.0" per consentire la differenziazione tra la stringa agente utente di Internet Explorer 7 e la stringa agente utente di Internet Explorer 8 durante l'esecuzione in Internet Explorer 7 Visualizzazione Compatibilità.</span><span class="sxs-lookup"><span data-stu-id="4f508-114">The User Agent string now includes the string 'Trident/4.0' in order to allow differentiation between the Internet Explorer 7 User Agent String and the Internet Explorer 8 User Agent string when running in Internet Explorer 7 Compatibility View.</span></span> <span data-ttu-id="4f508-115">Per informazioni dettagliate, vedere Informazioni sulle stringhe agente utente.</span><span class="sxs-lookup"><span data-stu-id="4f508-115">See Understanding User Agent Strings for details.</span></span>

## <a name="manifestation-of-impact"></a><span data-ttu-id="4f508-116">Impatto significativo</span><span class="sxs-lookup"><span data-stu-id="4f508-116">Manifestation of Impact</span></span>

<span data-ttu-id="4f508-117">Esistono due aree interessate:</span><span class="sxs-lookup"><span data-stu-id="4f508-117">There are two impacted areas:</span></span>

-   <span data-ttu-id="4f508-118">Le pagine Web che controllano in modo esplicito la stringa agente utente e non supportano la Internet Explorer 8 User Agent String potrebbero non essere eseguite correttamente.</span><span class="sxs-lookup"><span data-stu-id="4f508-118">Webpages that explicitly check the User Agent String and do not support the Internet Explorer 8 User Agent String may not run properly.</span></span> <span data-ttu-id="4f508-119">Nella maggior parte dei casi, ciò significa che le pagine verranno bloccate dagli utenti dal contenuto a cui tentano di accedere o visualizzare contenuto errato o in formato non corretto.</span><span class="sxs-lookup"><span data-stu-id="4f508-119">In the majority of cases, this means the pages will be block users from the content they are attempting to access or display incorrect or malformed content.</span></span>
-   <span data-ttu-id="4f508-120">Le applicazioni che ospitano Trident (vedere Hosting e riutilizzo) usano per impostazione predefinita Internet Explorer 7 usando il componente facoltativo Web, ma non avranno accesso Internet Explorer 8 funzionalità.</span><span class="sxs-lookup"><span data-stu-id="4f508-120">Applications that host Trident (see Hosting and Reuse) will default to Internet Explorer 7 using the Web Optional Component, but will not have access to Internet Explorer 8 features.</span></span>

## <a name="solution"></a><span data-ttu-id="4f508-121">Soluzione</span><span class="sxs-lookup"><span data-stu-id="4f508-121">Solution</span></span>

<span data-ttu-id="4f508-122">Assicurarsi che le applicazioni gestino correttamente la nuova versione "MSIE 8.0" nella stringa agente utente.</span><span class="sxs-lookup"><span data-stu-id="4f508-122">Ensure that your applications properly handle the new 'MSIE 8.0' version in the User Agent String.</span></span> <span data-ttu-id="4f508-123">È anche possibile acconsentire esplicitamente all'Internet Explorer 7 Visualizzazione Compatibilità per le applicazioni basate su Internet Explorer 7.</span><span class="sxs-lookup"><span data-stu-id="4f508-123">You may also opt in to the Internet Explorer 7 Compatibility View for those applications based on Internet Explorer 7.</span></span> <span data-ttu-id="4f508-124">Questa operazione può essere eseguita con i metatag.</span><span class="sxs-lookup"><span data-stu-id="4f508-124">This can be done with meta tags.</span></span> <span data-ttu-id="4f508-125">Per informazioni dettagliate, vedere la discussione informazioni sulle stringhe agente utente.</span><span class="sxs-lookup"><span data-stu-id="4f508-125">See the discussion in Understanding User Agent Strings for details.</span></span>

## <a name="compatibility-performance-reliability-and-usability-testing"></a><span data-ttu-id="4f508-126">Test di compatibilità, prestazioni, affidabilità e usabilità</span><span class="sxs-lookup"><span data-stu-id="4f508-126">Compatibility, Performance, Reliability, and Usability Testing</span></span>

-   <span data-ttu-id="4f508-127">Eseguire le applicazioni e le pagine Web in un ambiente Internet Explorer 8 in Windows Vista o Windows XP per assicurarsi che si comportino nel modo desiderato.</span><span class="sxs-lookup"><span data-stu-id="4f508-127">Run your applications and webpages in an Internet Explorer 8 environment on Windows Vista or Windows XP to ensure that they behave in the desired manner.</span></span>
-   <span data-ttu-id="4f508-128">In alternativa, è possibile eseguire lo strumento Internet Explorer Compatibility Test Tool (IECTT) fornito con Application Compatibility Toolkit (ACT) per individuare eventuali problemi potenziali dovuti agli aggiornamenti delle funzionalità di sicurezza.</span><span class="sxs-lookup"><span data-stu-id="4f508-128">Alternatively, you can run the Internet Explorer Compatibility Test Tool (IECTT) provided with the Application Compatibility Toolkit (ACT) to locate any potential issues due to security feature updates.</span></span>

## <a name="links-to-other-resources"></a><span data-ttu-id="4f508-129">Collegamenti ad altre risorse</span><span class="sxs-lookup"><span data-stu-id="4f508-129">Links to Other Resources</span></span>

-   <span data-ttu-id="4f508-130">[Informazioni sulle stringhe dell'agente utente](/previous-versions/windows/internet-explorer/ie-developer/compatibility/ms537503(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="4f508-130">[Understanding User Agent Strings](/previous-versions/windows/internet-explorer/ie-developer/compatibility/ms537503(v=vs.85))</span></span>
-   [<span data-ttu-id="4f508-131">Internet Explorer 8 User-Agent stringa</span><span class="sxs-lookup"><span data-stu-id="4f508-131">Internet Explorer 8 User-Agent String</span></span>](/archive/blogs/ie/)
-   [<span data-ttu-id="4f508-132">Stringa dell'agente utente e vettore di versione</span><span class="sxs-lookup"><span data-stu-id="4f508-132">User-Agent String and Version Vector</span></span>](https://archive.msdn.microsoft.com/ie8whitepapers)
-   <span data-ttu-id="4f508-133">[Hosting e riutilizzo](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa752038(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="4f508-133">[Hosting and Reuse](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa752038(v=vs.85))</span></span>
-   [<span data-ttu-id="4f508-134">Application Compatibility Toolkit Download</span><span class="sxs-lookup"><span data-stu-id="4f508-134">Application Compatibility Toolkit Download</span></span>](/windows-hardware/get-started/adk-install)
-   <span data-ttu-id="4f508-135">[Problemi noti Internet Explorer funzionalità di sicurezza](/previous-versions/windows/it-pro/windows-7/cc722079(v=ws.10))</span><span class="sxs-lookup"><span data-stu-id="4f508-135">[Known Internet Explorer Security Feature Issues](/previous-versions/windows/it-pro/windows-7/cc722079(v=ws.10))</span></span>

 

 
