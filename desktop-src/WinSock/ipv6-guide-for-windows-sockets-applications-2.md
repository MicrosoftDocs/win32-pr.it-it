---
description: Questa guida fornisce le informazioni necessarie per consentire all'applicazione Microsoft Windows di usare la nuova generazione di protocollo Internet, versione 6 (IPv6).
ms.assetid: 8e862eb0-2ba9-40b0-ac73-fcb0e625965e
title: Guida a IPv6 per le applicazioni Windows Sockets
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e3c582ba8dc10c167d47aafe98b1e8742551f948
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104129170"
---
# <a name="ipv6-guide-for-windows-sockets-applications"></a><span data-ttu-id="21a3d-103">Guida a IPv6 per le applicazioni Windows Sockets</span><span class="sxs-lookup"><span data-stu-id="21a3d-103">IPv6 Guide for Windows Sockets Applications</span></span>

<span data-ttu-id="21a3d-104">Questa guida fornisce le informazioni necessarie per consentire all'applicazione Microsoft Windows di usare la nuova generazione di protocollo Internet, versione 6 (IPv6).</span><span class="sxs-lookup"><span data-stu-id="21a3d-104">This guide provides the information you need to enable your Microsoft Windows application to use the next generation of Internet Protocol, version 6 (IPv6).</span></span> <span data-ttu-id="21a3d-105">L'aggiunta di funzionalità IPv6 all'applicazione non è necessariamente un processo di porting.</span><span class="sxs-lookup"><span data-stu-id="21a3d-105">Adding IPv6 capability to your application is not necessarily a porting process.</span></span> <span data-ttu-id="21a3d-106">Per eseguire il porting di un'applicazione, è necessario modificare il codice per lavorare su una piattaforma diversa, che implica l'uscita dalla precedente piattaforma.</span><span class="sxs-lookup"><span data-stu-id="21a3d-106">To port an application suggests modifying code to work on a different platform, which implies leaving the previous platform behind.</span></span> <span data-ttu-id="21a3d-107">Questa guida è strutturata in modo specifico per consentire l'aggiunta di funzionalità IPv6 a un'applicazione, mantenendo al tempo stesso la funzionalità IPv4.</span><span class="sxs-lookup"><span data-stu-id="21a3d-107">This guide is specifically structured to help add IPv6 capability to an application while retaining IPv4 functionality.</span></span>

<span data-ttu-id="21a3d-108">In questa guida vengono illustrati i problemi associati all'aggiunta di funzionalità IPv6, quindi vengono indirizzate le aree di sviluppo più interessate dalla transizione.</span><span class="sxs-lookup"><span data-stu-id="21a3d-108">This guide discusses the issues associated with adding IPv6 functionality, then targets the areas of development most affected by the transition.</span></span> <span data-ttu-id="21a3d-109">Ogni area riceve una spiegazione completa degli errori da tenere sotto controllo, le strategie suggerite per evitarle e suggerimenti su come sfruttare al meglio i nuovi elementi programmatici di [Windows Sockets 2](what-s-new-for-windows-sockets-2.md) (funzioni e strutture).</span><span class="sxs-lookup"><span data-stu-id="21a3d-109">Each area receives a thorough explanation of the pitfalls to watch out for, the strategies suggested to avoid them, and tips on how to make the best use of new [Windows Sockets 2](what-s-new-for-windows-sockets-2.md) programmatic elements (functions and structures).</span></span> <span data-ttu-id="21a3d-110">Per ulteriori informazioni su IPv6, vedere [supporto per IPv6](ipv6-support-2.md).</span><span class="sxs-lookup"><span data-stu-id="21a3d-110">For additional information on IPv6, see [IPv6 Support](ipv6-support-2.md).</span></span>

<span data-ttu-id="21a3d-111">Questa guida fornisce anche esempi di codice per offrire un'esperienza pratica e rappresentazioni visive dei problemi che possono verificarsi quando si modificano le applicazioni.</span><span class="sxs-lookup"><span data-stu-id="21a3d-111">This guide also provides code examples to give you hands-on experience and visual representations of the issues you could encounter when modifying your applications.</span></span> <span data-ttu-id="21a3d-112">Gli esempi derivano da esempi completi e funzionanti di una semplice applicazione Windows Sockets che è stata modificata per supportare sia IPv4 che IPv6.</span><span class="sxs-lookup"><span data-stu-id="21a3d-112">The examples come from complete, working examples of a simple Windows Sockets application that has been modified to support both IPv4 and IPv6.</span></span> <span data-ttu-id="21a3d-113">Il codice sorgente per questi esempi funzionanti è incluso interamente in due appendici alla fine di questo documento: [appendice a: il codice sorgente solo IPv4](appendix-a-ipv4-only-source-code-2.md) include il codice sorgente di un'applicazione prima che venga modificato per supportare IPv6. [Appendice B: codice sorgente indipendente dalla versione IP](appendix-b-ip-version-agnostic-source-code-2.md) fornisce il codice sorgente dopo che l'applicazione è stata abilitata per IPv6.</span><span class="sxs-lookup"><span data-stu-id="21a3d-113">Source code for these working examples is included in its entirety in two appendixes at the end of this document: [Appendix A: IPv4-only Source Code](appendix-a-ipv4-only-source-code-2.md) includes the source code for an application before it is modified to support IPv6; [Appendix B: IP-version Agnostic Source Code](appendix-b-ip-version-agnostic-source-code-2.md) provides the source code after the application has been IPv6-enabled.</span></span>

<span data-ttu-id="21a3d-114">Microsoft fornisce un'utilità denominata Checkv4.exe che consente di trovare codice potenzialmente dipendente dal porting nel codice dell'applicazione, oltre a indicazioni per le correzioni.</span><span class="sxs-lookup"><span data-stu-id="21a3d-114">Microsoft provides a utility called Checkv4.exe that helps you find potentially porting-sensitive code in your application code, and also makes recommendations for fixes.</span></span> <span data-ttu-id="21a3d-115">L'utilità Checkv4.exe viene illustrata in questo documento, utilizzando l'applicazione di esempio inclusa nelle appendici, insieme a schermate che visualizzano l'output prodotto dall'utilità Checkv4.exe.</span><span class="sxs-lookup"><span data-stu-id="21a3d-115">The Checkv4.exe utility is demonstrated in this document, using the sample application included in the appendixes, along with screen shots displaying the output that the Checkv4.exe utility produces.</span></span> <span data-ttu-id="21a3d-116">Per ulteriori informazioni, vedere [utilizzo dell'utilità Checkv4.exe](using-the-checkv4-exe-utility-2.md).</span><span class="sxs-lookup"><span data-stu-id="21a3d-116">For more information, see [Using the Checkv4.exe Utility](using-the-checkv4-exe-utility-2.md).</span></span>

<span data-ttu-id="21a3d-117">Le aree di programmazione indirizzate in questa guida sono:</span><span class="sxs-lookup"><span data-stu-id="21a3d-117">The programming areas addressed by this guide are:</span></span>

-   [<span data-ttu-id="21a3d-118">Modifica delle strutture di dati per applicazioni Winsock IPv6</span><span class="sxs-lookup"><span data-stu-id="21a3d-118">Changing Data Structures for IPv6 Winsock Appications</span></span>](changing-data-structures-2.md)
-   [<span data-ttu-id="21a3d-119">Chiamate di funzione per applicazioni Winsock IPv6</span><span class="sxs-lookup"><span data-stu-id="21a3d-119">Function Calls for IPv6 Winsock Applications</span></span>](function-calls-2.md)
-   [<span data-ttu-id="21a3d-120">Utilizzo di indirizzi IPv4 hardcoded</span><span class="sxs-lookup"><span data-stu-id="21a3d-120">Use of Hardcoded IPv4 Addresses</span></span>](use-of-hardcoded-ipv4-addresses-2.md)
-   [<span data-ttu-id="21a3d-121">Problemi dell'interfaccia utente per le applicazioni Winsock IPv6</span><span class="sxs-lookup"><span data-stu-id="21a3d-121">User Interface Issues for IPv6 Winsock Applications</span></span>](user-interface-issues-2.md)
-   [<span data-ttu-id="21a3d-122">Protocolli sottostanti per applicazioni Winsock IPv6</span><span class="sxs-lookup"><span data-stu-id="21a3d-122">Underlying Protocols for IPv6 Winsock Applications</span></span>](underlying-protocols-2.md)
-   [<span data-ttu-id="21a3d-123">Socket dual stack per applicazioni Winsock IPv6</span><span class="sxs-lookup"><span data-stu-id="21a3d-123">Dual-Stack Sockets for IPv6 Winsock Applications</span></span>](dual-stack-sockets.md)

<span data-ttu-id="21a3d-124">Poiché non esiste una sequenza uniforme di eventi, le sezioni che indirizzano i problemi di abilitazione di IPv6 non vengono disposte in modo sequenziale, quindi è possibile fare riferimento a qualsiasi sezione in qualsiasi momento.</span><span class="sxs-lookup"><span data-stu-id="21a3d-124">Because there is no uniform sequence of events, the sections that address IPv6-enabling issues are not arranged in a sequentially significant manner, so you can reference any section at any time.</span></span> <span data-ttu-id="21a3d-125">Si consiglia vivamente di rivedere ogni sezione durante l'aggiunta della funzionalità IPv6 all'applicazione.</span><span class="sxs-lookup"><span data-stu-id="21a3d-125">It is strongly recommended that you review each section while adding IPv6 capability to your application.</span></span> <span data-ttu-id="21a3d-126">È inoltre consigliabile leggere informazioni sull'utilità Checkv4.exe, in quanto include suggerimenti sull'ordine di risoluzione dei problemi di abilitazione di IPv6.</span><span class="sxs-lookup"><span data-stu-id="21a3d-126">It is also advisable to read about the Checkv4.exe utility, as it includes tips on the order in which to address IPv6-enabling issues.</span></span>

<span data-ttu-id="21a3d-127">Per esaminare l'utilità di Checkv4.exe e per rivedere l'ordine in cui è necessario affrontare il processo di porting nelle applicazioni, vedere [utilizzo dell'utilità di Checkv4.exe](using-the-checkv4-exe-utility-2.md).</span><span class="sxs-lookup"><span data-stu-id="21a3d-127">To look at the Checkv4.exe utility, and to review the order in which you should approach the porting process in your applications, see [Using the Checkv4.exe Utility](using-the-checkv4-exe-utility-2.md).</span></span> <span data-ttu-id="21a3d-128">In questa sezione sono incluse informazioni su un flag della fase di compilazione che controlla rigorosamente gli elementi di programmazione incompatibili con IPv6.</span><span class="sxs-lookup"><span data-stu-id="21a3d-128">This section includes information on a compile-time flag that strictly checks for programming elements incompatible with IPv6.</span></span>

<span data-ttu-id="21a3d-129">Per passare direttamente all'applicazione di esempio, vedere [appendice a: codice sorgente solo IPv4](appendix-a-ipv4-only-source-code-2.md) e [Appendice B: codice sorgente indipendente dalla versione IP](appendix-b-ip-version-agnostic-source-code-2.md).</span><span class="sxs-lookup"><span data-stu-id="21a3d-129">To go straight to the sample application, see [Appendix A: IPv4-only Source Code](appendix-a-ipv4-only-source-code-2.md) and [Appendix B: IP-version Agnostic Source Code](appendix-b-ip-version-agnostic-source-code-2.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="21a3d-130">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="21a3d-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="21a3d-131">Protocollo IP versione 6 (IPv6)</span><span class="sxs-lookup"><span data-stu-id="21a3d-131">Internet Protocol Version 6 (IPv6)</span></span>](internet-protocol-version-6-ipv6-2.md)
</dt> <dt>

[<span data-ttu-id="21a3d-132">Supporto IPv6</span><span class="sxs-lookup"><span data-stu-id="21a3d-132">IPv6 Support</span></span>](ipv6-support-2.md)
</dt> <dt>

[<span data-ttu-id="21a3d-133">Anteprima della tecnologia IPv6 per Windows 2000</span><span class="sxs-lookup"><span data-stu-id="21a3d-133">IPv6 Technology Preview for Windows 2000</span></span>](https://www.microsoft.com/downloads/details.aspx?FamilyID=27b1e6a6-bbdd-43c9-af57-dae19795a088)
</dt> <dt>

[<span data-ttu-id="21a3d-134">Utilizzo dell'utilità Checkv4.exe</span><span class="sxs-lookup"><span data-stu-id="21a3d-134">Using the Checkv4.exe Utility</span></span>](using-the-checkv4-exe-utility-2.md)
</dt> <dt>

[<span data-ttu-id="21a3d-135">Appendice A: codice sorgente solo IPv4</span><span class="sxs-lookup"><span data-stu-id="21a3d-135">Appendix A: IPv4-only Source Code</span></span>](appendix-a-ipv4-only-source-code-2.md)
</dt> <dt>

[<span data-ttu-id="21a3d-136">Appendice B: codice sorgente indipendente dalla versione IP</span><span class="sxs-lookup"><span data-stu-id="21a3d-136">Appendix B: IP-version Agnostic Source Code</span></span>](appendix-b-ip-version-agnostic-source-code-2.md)
</dt> </dl>

 

 



