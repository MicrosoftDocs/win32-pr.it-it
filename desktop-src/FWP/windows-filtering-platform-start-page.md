---
title: Piattaforma filtro Windows
description: Windows Filtering Platform (WFP) è un set di servizi API e di sistema che forniscono una piattaforma per la creazione di applicazioni di filtro di rete.
ms.assetid: 0436f559-20e6-4199-8391-10eb7d85df23
keywords:
- Piattaforma filtro Windows
- Pagina iniziale della piattaforma filtro Windows, pagina iniziale
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5cf63f995b44be607977dd0c70c6c91eed024e81
ms.sourcegitcommit: 773fa6257ead6c74154ad3cf46d21e49adc900aa
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/09/2020
ms.locfileid: "106300628"
---
# <a name="windows-filtering-platform"></a><span data-ttu-id="82fe2-105">Piattaforma filtro Windows</span><span class="sxs-lookup"><span data-stu-id="82fe2-105">Windows Filtering Platform</span></span>

## <a name="purpose"></a><span data-ttu-id="82fe2-106">Scopo</span><span class="sxs-lookup"><span data-stu-id="82fe2-106">Purpose</span></span>

<span data-ttu-id="82fe2-107">Windows Filtering Platform (WFP) è un set di servizi API e di sistema che forniscono una piattaforma per la creazione di applicazioni di filtro di rete.</span><span class="sxs-lookup"><span data-stu-id="82fe2-107">Windows Filtering Platform (WFP) is a set of API and system services that provide a platform for creating network filtering applications.</span></span> <span data-ttu-id="82fe2-108">L'API di Piattaforma filtro Windows consente agli sviluppatori di scrivere codice che interagisce con l'elaborazione dei pacchetti che si verifica a diversi livelli nello stack di rete del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="82fe2-108">The WFP API allows developers to write code that interacts with the packet processing that takes place at several layers in the networking stack of the operating system.</span></span> <span data-ttu-id="82fe2-109">È possibile filtrare e modificare i dati di rete prima che raggiungano la destinazione.</span><span class="sxs-lookup"><span data-stu-id="82fe2-109">Network data can be filtered and also modified before it reaches its destination.</span></span>

<span data-ttu-id="82fe2-110">Grazie a una piattaforma di sviluppo più semplice, Pam è progettato per sostituire le tecnologie di filtro dei pacchetti precedenti, ad esempio i filtri Transport Driver Interface (TDI), i filtri NDIS (Network Driver Interface Specification) e i provider di servizi a più livelli Winsock (LSP).</span><span class="sxs-lookup"><span data-stu-id="82fe2-110">By providing a simpler development platform, WFP is designed to replace previous packet filtering technologies such as Transport Driver Interface (TDI) filters, Network Driver Interface Specification (NDIS) filters, and Winsock Layered Service Providers (LSP).</span></span> <span data-ttu-id="82fe2-111">A partire da Windows Server 2008 e Windows Vista, l'hook del firewall e i driver dell'hook di filtro non sono disponibili. le applicazioni che usavano questi driver dovrebbero invece usare Pam.</span><span class="sxs-lookup"><span data-stu-id="82fe2-111">Starting in Windows Server 2008 and Windows Vista, the firewall hook and the filter hook drivers are not available; applications that were using these drivers should use WFP instead.</span></span>

<span data-ttu-id="82fe2-112">Con l'API WFP gli sviluppatori possono implementare firewall, sistemi di rilevamento delle intrusioni, programmi antivirus, strumenti di monitoraggio della rete e controlli padre.</span><span class="sxs-lookup"><span data-stu-id="82fe2-112">With the WFP API, developers can implement firewalls, intrusion detection systems, antivirus programs, network monitoring tools, and parental controls.</span></span> <span data-ttu-id="82fe2-113">Pam si integra con e fornisce il supporto per le funzionalità del firewall, ad esempio la comunicazione autenticata e la configurazione dinamica del firewall basata sull'utilizzo dell'API Sockets da parte delle applicazioni (criteri basati su applicazioni).</span><span class="sxs-lookup"><span data-stu-id="82fe2-113">WFP integrates with and provides support for firewall features such as authenticated communication and dynamic firewall configuration based on applications' use of sockets API (application-based policy).</span></span> <span data-ttu-id="82fe2-114">PAM fornisce inoltre l'infrastruttura per la gestione dei criteri IPsec, le notifiche di modifica, la diagnostica di rete e i filtri con stato.</span><span class="sxs-lookup"><span data-stu-id="82fe2-114">WFP also provides infrastructure for IPsec policy management, change notifications, network diagnostics, and stateful filtering.</span></span>

<span data-ttu-id="82fe2-115">Windows Filtering Platform è una piattaforma di sviluppo e non un firewall.</span><span class="sxs-lookup"><span data-stu-id="82fe2-115">Windows Filtering Platform is a development platform and not a firewall itself.</span></span> <span data-ttu-id="82fe2-116">L'applicazione firewall incorporata nei sistemi operativi Windows Vista, Windows Server 2008 e versioni successive Windows Firewall with Advanced Security (WFAS) viene implementata tramite WFP.</span><span class="sxs-lookup"><span data-stu-id="82fe2-116">The firewall application that is built into Windows Vista, Windows Server 2008, and later operating systems   Windows Firewall with Advanced Security (WFAS)   is implemented using WFP.</span></span> <span data-ttu-id="82fe2-117">Pertanto, le applicazioni sviluppate con l'API Pam o l' [API wfas](/previous-versions/windows/desktop/ics/windows-firewall-with-advanced-security-reference) utilizzano la logica di arbitraggio di filtro comune incorporata in Pam.</span><span class="sxs-lookup"><span data-stu-id="82fe2-117">Therefore, applications developed with the WFP API or the [WFAS API](/previous-versions/windows/desktop/ics/windows-firewall-with-advanced-security-reference) use the common filtering arbitration logic that is built into WFP.</span></span>

<span data-ttu-id="82fe2-118">L'API PAM è costituita da un'API in modalità utente e da un'API in modalità kernel.</span><span class="sxs-lookup"><span data-stu-id="82fe2-118">The WFP API consists of a user-mode API and a kernel-mode API.</span></span> <span data-ttu-id="82fe2-119">In questa sezione viene fornita una panoramica dell'intero WFP e viene descritto in dettaglio solo la parte in modalità utente dell'API Pam.</span><span class="sxs-lookup"><span data-stu-id="82fe2-119">This section provides an overview of the entire WFP and describes in detail only the user-mode portion of the WFP API.</span></span> <span data-ttu-id="82fe2-120">Per una descrizione dettagliata dell'API PAM in modalità kernel, vedere la Guida in linea di [Windows Driver Kit](/windows-hardware/drivers/network/windows-filtering-platform-callout-drivers2) .</span><span class="sxs-lookup"><span data-stu-id="82fe2-120">For a detailed description of the kernel-mode WFP API, see the [Windows Driver Kit](/windows-hardware/drivers/network/windows-filtering-platform-callout-drivers2) online help.</span></span>

## <a name="developer-audience"></a><span data-ttu-id="82fe2-121">Sviluppatori</span><span class="sxs-lookup"><span data-stu-id="82fe2-121">Developer audience</span></span>

<span data-ttu-id="82fe2-122">L'API Windows Filtering Platform è progettata per l'uso da parte dei programmatori che usano il software di sviluppo C/C++.</span><span class="sxs-lookup"><span data-stu-id="82fe2-122">The Windows Filtering Platform API is designed for use by programmers using C/C++ development software.</span></span> <span data-ttu-id="82fe2-123">I programmatori devono acquisire familiarità con i concetti di rete e la progettazione dei sistemi mediante componenti in modalità utente e kernel.</span><span class="sxs-lookup"><span data-stu-id="82fe2-123">Programmers should be familiar with networking concepts and design of systems using user-mode and kernel-mode components.</span></span>

## <a name="run-time-requirements"></a><span data-ttu-id="82fe2-124">Requisiti di runtime</span><span class="sxs-lookup"><span data-stu-id="82fe2-124">Run-time requirements</span></span>

<span data-ttu-id="82fe2-125">Windows Filtering Platform è supportato nei client che eseguono Windows Vista e versioni successive e nei server che eseguono Windows Server 2008 e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="82fe2-125">The Windows Filtering Platform is supported on clients running Windows Vista and later, and on servers running Windows Server 2008 and later.</span></span> <span data-ttu-id="82fe2-126">Per informazioni sui requisiti di run-time per un elemento di programmazione specifico, vedere la sezione requisiti della pagina di riferimento per tale elemento.</span><span class="sxs-lookup"><span data-stu-id="82fe2-126">For information about the run-time requirements for a specific programming element, see the Requirements section of the reference page for that element.</span></span>





 

## <a name="in-this-section"></a><span data-ttu-id="82fe2-127">Contenuto della sezione</span><span class="sxs-lookup"><span data-stu-id="82fe2-127">In this section</span></span>



| <span data-ttu-id="82fe2-128">Argomento</span><span class="sxs-lookup"><span data-stu-id="82fe2-128">Topic</span></span>                                                                                               | <span data-ttu-id="82fe2-129">Descrizione</span><span class="sxs-lookup"><span data-stu-id="82fe2-129">Description</span></span>                                                                                       |
|-----------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="82fe2-130">Novità della piattaforma filtro Windows</span><span class="sxs-lookup"><span data-stu-id="82fe2-130">What's New in Windows Filtering Platform</span></span>](what-s-new-in-windows-filtering-platform.md)<br/> | <span data-ttu-id="82fe2-131">Informazioni sulle nuove funzionalità e API nella piattaforma filtro Windows.</span><span class="sxs-lookup"><span data-stu-id="82fe2-131">Information on new features and APIs in Windows Filtering Platform.</span></span><br/>                    |
| [<span data-ttu-id="82fe2-132">Informazioni sulla piattaforma filtro Windows</span><span class="sxs-lookup"><span data-stu-id="82fe2-132">About Windows Filtering Platform</span></span>](about-windows-filtering-platform.md)<br/>                 | <span data-ttu-id="82fe2-133">Panoramica della piattaforma filtro Windows.</span><span class="sxs-lookup"><span data-stu-id="82fe2-133">An overview of Windows Filtering Platform.</span></span><br/>                                             |
| [<span data-ttu-id="82fe2-134">Uso della piattaforma filtro Windows</span><span class="sxs-lookup"><span data-stu-id="82fe2-134">Using Windows Filtering Platform</span></span>](using-windows-filtering-platform.md)<br/>                 | <span data-ttu-id="82fe2-135">Codice di esempio che usa l'API della piattaforma filtro Windows.</span><span class="sxs-lookup"><span data-stu-id="82fe2-135">Example code using the Windows Filtering Platform API.</span></span> <br/>                                |
| [<span data-ttu-id="82fe2-136">Informazioni di riferimento sulle API della piattaforma filtro Windows</span><span class="sxs-lookup"><span data-stu-id="82fe2-136">Windows Filtering Platform API Reference</span></span>](fwp-reference.md)<br/>                            | <span data-ttu-id="82fe2-137">Documentazione per le funzioni, le strutture e le costanti di Windows Filtering Platform.</span><span class="sxs-lookup"><span data-stu-id="82fe2-137">Documentation for the Windows Filtering Platform functions, structures, and constants.</span></span><br/> |



 

## <a name="additional-resources"></a><span data-ttu-id="82fe2-138">Risorse aggiuntive</span><span class="sxs-lookup"><span data-stu-id="82fe2-138">Additional resources</span></span>

<span data-ttu-id="82fe2-139">Per porre domande e discutere sull'uso dell'API Pam, visitare il forum relativo alla [piattaforma filtro Windows](https://social.msdn.microsoft.com/forums/wfp/threads/).</span><span class="sxs-lookup"><span data-stu-id="82fe2-139">To ask questions and have discussions about using the WFP API, visit the [Windows Filtering Platform Forum](https://social.msdn.microsoft.com/forums/wfp/threads/).</span></span>

## <a name="related-topics"></a><span data-ttu-id="82fe2-140">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="82fe2-140">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="82fe2-141">Guida alla progettazione dell'API della piattaforma filtro Windows in modalità kernel</span><span class="sxs-lookup"><span data-stu-id="82fe2-141">Kernel-Mode Windows Filtering Platform API - Design Guide</span></span>](/windows-hardware/drivers/network/windows-filtering-platform-callout-drivers2)
</dt> <dt>

[<span data-ttu-id="82fe2-142">Informazioni di riferimento sull'API della piattaforma filtro Windows in modalità kernel</span><span class="sxs-lookup"><span data-stu-id="82fe2-142">Kernel-Mode Windows Filtering Platform API - Reference</span></span>](/windows-hardware/drivers/ddi/_netvista/)
</dt> <dt>

[<span data-ttu-id="82fe2-143">Windows Firewall con sicurezza avanzata</span><span class="sxs-lookup"><span data-stu-id="82fe2-143">Windows Firewall with Advanced Security</span></span>](/previous-versions/windows/desktop/ics/windows-firewall-advanced-security-start-page)
</dt> <dt>

[<span data-ttu-id="82fe2-144">Classe helper di diagnostica WFP</span><span class="sxs-lookup"><span data-stu-id="82fe2-144">WFP Diagnostics Extensible Helper Class</span></span>](/windows/desktop/NDF/windows-filtering-platform-extensible-helper-class)
</dt> <dt>

[<span data-ttu-id="82fe2-145">Estensioni Secure socket Winsock</span><span class="sxs-lookup"><span data-stu-id="82fe2-145">Winsock Secure Socket Extensions</span></span>](/windows/desktop/WinSock/winsock-secure-socket-extensions)
</dt> </dl>

 

