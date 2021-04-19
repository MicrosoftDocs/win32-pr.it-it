---
description: .
ms.assetid: 1cb0456d-501a-4272-b89d-35e79d29d13a
title: Internet Explorer 8-stringa agente utente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3aea44572f32e252a4e1d4dc2209e411834c12d4
ms.sourcegitcommit: 78b64f3865e64768b5319d4f010032ee68924a98
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/13/2021
ms.locfileid: "107314794"
---
# <a name="internet-explorer-8---user-agent-string"></a><span data-ttu-id="81b0d-103">Internet Explorer 8-stringa agente utente</span><span class="sxs-lookup"><span data-stu-id="81b0d-103">Internet Explorer 8 - User Agent String</span></span>

## <a name="affected-platforms"></a><span data-ttu-id="81b0d-104">Piattaforme interessate</span><span class="sxs-lookup"><span data-stu-id="81b0d-104">Affected Platforms</span></span>

 <span data-ttu-id="81b0d-105">**Client** -Windows XP, Windows Vista, Windows 7</span><span class="sxs-lookup"><span data-stu-id="81b0d-105">**Clients** - Windows XP, Windows Vista, Windows 7</span></span>  
<span data-ttu-id="81b0d-106">**Server** : windows Server 2003, windows Server 2008, windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="81b0d-106">**Servers** - Windows Server 2003, Windows Server 2008, Windows Server 2008 R2</span></span>  










## <a name="feature-impact"></a><span data-ttu-id="81b0d-107">Effetto sulle funzionalità</span><span class="sxs-lookup"><span data-stu-id="81b0d-107">Feature Impact</span></span>

<span data-ttu-id="81b0d-108">**Gravità** -medio</span><span class="sxs-lookup"><span data-stu-id="81b0d-108">**Severity** - Medium</span></span>  
<span data-ttu-id="81b0d-109">**Frequenza** -alta</span><span class="sxs-lookup"><span data-stu-id="81b0d-109">**Frequency** - High</span></span>  











## <a name="description"></a><span data-ttu-id="81b0d-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="81b0d-110">Description</span></span>

<span data-ttu-id="81b0d-111">La stringa agente utente è l'identificatore di Internet Explorer che fornisce i dati sulla versione e altri attributi ai server Web.</span><span class="sxs-lookup"><span data-stu-id="81b0d-111">The User Agent String is the Internet Explorer identifier that provides data about its version and other attributes to web servers.</span></span> <span data-ttu-id="81b0d-112">Molte applicazioni Web si basano su e su Piggyback, la stringa dell'agente utente di IE.</span><span class="sxs-lookup"><span data-stu-id="81b0d-112">Many web applications rely on, and piggyback on, the IE User Agent String.</span></span> <span data-ttu-id="81b0d-113">Verranno ripercussioni le operazioni che consentono di eseguire questa operazione e che dipendono da un numero di versione precedente.</span><span class="sxs-lookup"><span data-stu-id="81b0d-113">Those that do so and depend on an earlier version number will be impacted.</span></span> <span data-ttu-id="81b0d-114">La stringa agente utente include ora la stringa "Trident/4.0" per consentire la differenziazione tra la stringa agente utente Internet Explorer 7 e la stringa agente utente di Internet Explorer 8 durante l'esecuzione in visualizzazione compatibilità di Internet Explorer 7.</span><span class="sxs-lookup"><span data-stu-id="81b0d-114">The User Agent string now includes the string 'Trident/4.0' in order to allow differentiation between the Internet Explorer 7 User Agent String and the Internet Explorer 8 User Agent string when running in Internet Explorer 7 Compatibility View.</span></span> <span data-ttu-id="81b0d-115">Per informazioni dettagliate, vedere informazioni sulle stringhe agente utente.</span><span class="sxs-lookup"><span data-stu-id="81b0d-115">See Understanding User Agent Strings for details.</span></span>

## <a name="manifestation-of-impact"></a><span data-ttu-id="81b0d-116">Manifesto di effetto</span><span class="sxs-lookup"><span data-stu-id="81b0d-116">Manifestation of Impact</span></span>

<span data-ttu-id="81b0d-117">Sono presenti due aree interessate:</span><span class="sxs-lookup"><span data-stu-id="81b0d-117">There are two impacted areas:</span></span>

-   <span data-ttu-id="81b0d-118">Le pagine Web che controllano in modo esplicito la stringa agente utente e non supportano la stringa agente utente Internet Explorer 8 potrebbero non funzionare correttamente.</span><span class="sxs-lookup"><span data-stu-id="81b0d-118">Webpages that explicitly check the User Agent String and do not support the Internet Explorer 8 User Agent String may not run properly.</span></span> <span data-ttu-id="81b0d-119">Nella maggior parte dei casi, ciò significa che le pagine bloccano gli utenti dal contenuto a cui tentano di accedere o visualizzano contenuto non corretto o non valido.</span><span class="sxs-lookup"><span data-stu-id="81b0d-119">In the majority of cases, this means the pages will be block users from the content they are attempting to access or display incorrect or malformed content.</span></span>
-   <span data-ttu-id="81b0d-120">Le applicazioni che ospitano Trident (vedere Hosting e riuso) utilizzeranno per impostazione predefinita Internet Explorer 7 utilizzando il componente facoltativo Web, ma non avranno accesso alle funzionalità di Internet Explorer 8.</span><span class="sxs-lookup"><span data-stu-id="81b0d-120">Applications that host Trident (see Hosting and Reuse) will default to Internet Explorer 7 using the Web Optional Component, but will not have access to Internet Explorer 8 features.</span></span>

## <a name="solution"></a><span data-ttu-id="81b0d-121">Soluzione</span><span class="sxs-lookup"><span data-stu-id="81b0d-121">Solution</span></span>

<span data-ttu-id="81b0d-122">Verificare che le applicazioni gestiscano correttamente la nuova versione di ' MSIE 8,0' nella stringa agente utente.</span><span class="sxs-lookup"><span data-stu-id="81b0d-122">Ensure that your applications properly handle the new 'MSIE 8.0' version in the User Agent String.</span></span> <span data-ttu-id="81b0d-123">È inoltre possibile acconsentire esplicitamente alla visualizzazione di compatibilità di Internet Explorer 7 per le applicazioni basate su Internet Explorer 7.</span><span class="sxs-lookup"><span data-stu-id="81b0d-123">You may also opt in to the Internet Explorer 7 Compatibility View for those applications based on Internet Explorer 7.</span></span> <span data-ttu-id="81b0d-124">Questa operazione può essere eseguita con i tag meta.</span><span class="sxs-lookup"><span data-stu-id="81b0d-124">This can be done with meta tags.</span></span> <span data-ttu-id="81b0d-125">Per informazioni dettagliate, vedere la discussione in informazioni sulle stringhe agente utente.</span><span class="sxs-lookup"><span data-stu-id="81b0d-125">See the discussion in Understanding User Agent Strings for details.</span></span>

## <a name="compatibility-performance-reliability-and-usability-testing"></a><span data-ttu-id="81b0d-126">Compatibilità, prestazioni, affidabilità e test di usabilità</span><span class="sxs-lookup"><span data-stu-id="81b0d-126">Compatibility, Performance, Reliability, and Usability Testing</span></span>

-   <span data-ttu-id="81b0d-127">Eseguire le applicazioni e le pagine Web in un ambiente Internet Explorer 8 in Windows Vista o Windows XP per assicurarsi che si comportino nel modo desiderato.</span><span class="sxs-lookup"><span data-stu-id="81b0d-127">Run your applications and webpages in an Internet Explorer 8 environment on Windows Vista or Windows XP to ensure that they behave in the desired manner.</span></span>
-   <span data-ttu-id="81b0d-128">In alternativa, è possibile eseguire lo strumento di test della compatibilità di Internet Explorer (IECTT) fornito con Application Compatibility Toolkit (ACT) per individuare eventuali problemi causati da aggiornamenti delle funzionalità di sicurezza.</span><span class="sxs-lookup"><span data-stu-id="81b0d-128">Alternatively, you can run the Internet Explorer Compatibility Test Tool (IECTT) provided with the Application Compatibility Toolkit (ACT) to locate any potential issues due to security feature updates.</span></span>

## <a name="links-to-other-resources"></a><span data-ttu-id="81b0d-129">Collegamenti ad altre risorse</span><span class="sxs-lookup"><span data-stu-id="81b0d-129">Links to Other Resources</span></span>

-   <span data-ttu-id="81b0d-130">[Informazioni sulle stringhe agente utente](/previous-versions/windows/internet-explorer/ie-developer/compatibility/ms537503(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="81b0d-130">[Understanding User Agent Strings](/previous-versions/windows/internet-explorer/ie-developer/compatibility/ms537503(v=vs.85))</span></span>
-   [<span data-ttu-id="81b0d-131">Stringa di User-Agent di Internet Explorer 8</span><span class="sxs-lookup"><span data-stu-id="81b0d-131">Internet Explorer 8 User-Agent String</span></span>](/archive/blogs/ie/)
-   [<span data-ttu-id="81b0d-132">Stringa dell'agente utente e vettore della versione</span><span class="sxs-lookup"><span data-stu-id="81b0d-132">User-Agent String and Version Vector</span></span>](https://archive.msdn.microsoft.com/ie8whitepapers)
-   <span data-ttu-id="81b0d-133">[Hosting e riutilizzo](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa752038(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="81b0d-133">[Hosting and Reuse](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa752038(v=vs.85))</span></span>
-   [<span data-ttu-id="81b0d-134">Download di Application Compatibility Toolkit</span><span class="sxs-lookup"><span data-stu-id="81b0d-134">Application Compatibility Toolkit Download</span></span>](/windows-hardware/get-started/adk-install)
-   <span data-ttu-id="81b0d-135">[Problemi noti relativi alle funzionalità di sicurezza di Internet Explorer](/previous-versions/windows/it-pro/windows-7/cc722079(v=ws.10))</span><span class="sxs-lookup"><span data-stu-id="81b0d-135">[Known Internet Explorer Security Feature Issues](/previous-versions/windows/it-pro/windows-7/cc722079(v=ws.10))</span></span>

 

 
