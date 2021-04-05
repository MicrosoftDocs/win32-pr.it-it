---
title: Automazione interfaccia utente
description: Automazione interfaccia utente Microsoft è un Framework di accessibilità che consente alle applicazioni Windows di fornire e utilizzare informazioni programmatiche sulle interfacce utente.
ms.assetid: 700ca38d-ff40-472b-a95a-11fa94c3bc1d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b8006c79299cc1f736dc43555968443f634d4a51
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "103872769"
---
# <a name="ui-automation"></a><span data-ttu-id="04952-103">Automazione interfaccia utente</span><span class="sxs-lookup"><span data-stu-id="04952-103">UI Automation</span></span>

<span data-ttu-id="04952-104">Automazione interfaccia utente Microsoft è un Framework di accessibilità che consente alle applicazioni Windows di fornire e utilizzare informazioni programmatiche sulle interfacce utente.</span><span class="sxs-lookup"><span data-stu-id="04952-104">Microsoft UI Automation is an accessibility framework that enables Windows applications to provide and consume programmatic information about user interfaces (UIs).</span></span> <span data-ttu-id="04952-105">Consente l'accesso a livello di codice alla maggior parte degli elementi dell'interfaccia utente sul desktop.</span><span class="sxs-lookup"><span data-stu-id="04952-105">It provides programmatic access to most UI elements on the desktop.</span></span> <span data-ttu-id="04952-106">Consente ai prodotti di Assistive Technology, quali utilità per la lettura dello schermo, di fornire informazioni sull'interfaccia utente agli utenti finali e di modificare l'interfaccia utente per mezzo di input standard.</span><span class="sxs-lookup"><span data-stu-id="04952-106">It enables assistive technology products, such as screen readers, to provide information about the UI to end users and to manipulate the UI by means other than standard input.</span></span> <span data-ttu-id="04952-107">Automazione interfaccia utente consente inoltre l'interazione degli script di test automatizzati con l'interfaccia utente.</span><span class="sxs-lookup"><span data-stu-id="04952-107">UI Automation also allows automated test scripts to interact with the UI.</span></span>

-   [<span data-ttu-id="04952-108">Ove applicabile</span><span class="sxs-lookup"><span data-stu-id="04952-108">Where Applicable</span></span>](#where-applicable)
-   [<span data-ttu-id="04952-109">Destinatari degli sviluppatori</span><span class="sxs-lookup"><span data-stu-id="04952-109">Developer Audience</span></span>](#developer-audience)
-   [<span data-ttu-id="04952-110">Requisiti della fase di esecuzione</span><span class="sxs-lookup"><span data-stu-id="04952-110">Run-Time Requirements</span></span>](#run-time-requirements)
-   [<span data-ttu-id="04952-111">Supporto per sistemi operativi di livello inferiore</span><span class="sxs-lookup"><span data-stu-id="04952-111">Support for Down-level Operating Systems</span></span>](#support-for-down-level-operating-systems)

## <a name="where-applicable"></a><span data-ttu-id="04952-112">Ambito di applicazione</span><span class="sxs-lookup"><span data-stu-id="04952-112">Where Applicable</span></span>

<span data-ttu-id="04952-113">Utilizzando l'automazione interfaccia utente e le seguenti procedure di progettazione accessibili, gli sviluppatori possono rendere le applicazioni in esecuzione in Windows più accessibili a molti utenti con problemi di visione, udito o movimento.</span><span class="sxs-lookup"><span data-stu-id="04952-113">By using UI Automation and following accessible design practices, developers can make applications running on Windows more accessible to many people with vision, hearing, or motion disabilities.</span></span> <span data-ttu-id="04952-114">Inoltre, l'automazione dell'interfaccia utente è progettata appositamente per fornire funzionalità affidabili per gli scenari di test automatizzati.</span><span class="sxs-lookup"><span data-stu-id="04952-114">Also, UI Automation is specifically designed to provide robust functionality for automated testing scenarios.</span></span>

## <a name="developer-audience"></a><span data-ttu-id="04952-115">Sviluppatori</span><span class="sxs-lookup"><span data-stu-id="04952-115">Developer Audience</span></span>

<span data-ttu-id="04952-116">Automazione interfaccia utente è progettata per gli sviluppatori C/C++ esperti.</span><span class="sxs-lookup"><span data-stu-id="04952-116">UI Automation is designed for experienced C/C++ developers.</span></span> <span data-ttu-id="04952-117">In generale, gli sviluppatori necessitano di un livello moderato di informazioni sugli oggetti e le interfacce di Component Object Model (COM), Unicode e la programmazione dell'API Windows.</span><span class="sxs-lookup"><span data-stu-id="04952-117">In general, developers need a moderate level of understanding about Component Object Model (COM) objects and interfaces, Unicode, and Windows API programming.</span></span>

<span data-ttu-id="04952-118">Per informazioni sull'automazione dell'interfaccia utente per il codice gestito, vedere l'articolo relativo all' [accessibilità](/dotnet/framework/ui-automation/) nella sezione della Guida per sviluppatori .NET Framework di MSDN.</span><span class="sxs-lookup"><span data-stu-id="04952-118">For information about UI Automation for managed code, please see [Accessibility](/dotnet/framework/ui-automation/) in the .NET Framework Developer's Guide section of MSDN.</span></span>

## <a name="run-time-requirements"></a><span data-ttu-id="04952-119">Requisiti di runtime</span><span class="sxs-lookup"><span data-stu-id="04952-119">Run-Time Requirements</span></span>

<span data-ttu-id="04952-120">Automazione interfaccia utente è supportata nei sistemi operativi seguenti: Windows XP, Windows Server 2003, Windows Server 2003 R2, Windows Vista, Windows 7, Windows 10, Windows Server 2008, Windows Server 2008 R2, Windows Server 2012, Windows Server 2012 R2, Windows Server 2016 e Windows Server 2019.</span><span class="sxs-lookup"><span data-stu-id="04952-120">UI Automation is supported on the following operating systems: Windows XP, Windows Server 2003, Windows Server 2003 R2, Windows Vista, Windows 7, Windows 10, Windows Server 2008, Windows Server 2008 R2, Windows Server 2012, Windows Server 2012 R2, Windows Server 2016, and Windows Server 2019.</span></span>

> [!Note]  
> <span data-ttu-id="04952-121">Windows XP e Windows Server 2003 richiedono anche Microsoft .NET Framework 3,0.</span><span class="sxs-lookup"><span data-stu-id="04952-121">Windows XP and Windows Server 2003 also require Microsoft .NET Framework 3.0.</span></span>

 

## <a name="support-for-down-level-operating-systems"></a><span data-ttu-id="04952-122">Supporto per sistemi operativi di livello inferiore</span><span class="sxs-lookup"><span data-stu-id="04952-122">Support for Down-level Operating Systems</span></span>

<span data-ttu-id="04952-123">L'aggiornamento della piattaforma per Windows Vista è costituito da un set di librerie di runtime che consente agli sviluppatori di utilizzare le applicazioni sia per i sistemi operativi Windows 7 che per quelli di livello inferiore.</span><span class="sxs-lookup"><span data-stu-id="04952-123">The Platform Update for Windows Vista is a set of run-time libraries that enables developers to target applications to both Windows 7 and down-level operating systems.</span></span> <span data-ttu-id="04952-124">L'aggiornamento della piattaforma per Windows Server 2008 è costituito da un set di librerie di runtime che consente agli sviluppatori di utilizzare le applicazioni in Windows Server 2008 R2 e versioni precedenti di Windows Server.</span><span class="sxs-lookup"><span data-stu-id="04952-124">The Platform Update for Windows Server 2008 is a set of run-time libraries that enables developers to target applications to both Windows Server 2008 R2 and previous versions of Windows Server.</span></span> <span data-ttu-id="04952-125">L'aggiornamento della piattaforma per Windows Vista e l'aggiornamento della piattaforma per Windows Server 2008 saranno disponibili per tutti i clienti di Windows Vista e Windows Server 2008 tramite Windows Update.</span><span class="sxs-lookup"><span data-stu-id="04952-125">The Platform Update for Windows Vista and the Platform Update for Windows Server 2008 will be available to all Windows Vista and Windows Server 2008 customers through Windows Update.</span></span> <span data-ttu-id="04952-126">Le applicazioni di terze parti che richiedono l'aggiornamento della piattaforma per Windows Vista o l'aggiornamento della piattaforma per Windows Server 2008 possono avere Windows Update rilevare se è installato; in caso contrario, Windows Update lo scaricherà e installerà in background.</span><span class="sxs-lookup"><span data-stu-id="04952-126">Third-party applications that require Platform Update for Windows Vista or Platform Update for Windows Server 2008 can have Windows Update detect whether it is installed; if it is not, Windows Update will download and install it in the background.</span></span>

<span data-ttu-id="04952-127">L'aggiornamento della piattaforma per Windows Vista e l'aggiornamento della piattaforma per Windows Server 2008 supportano entrambi l'intero set di funzionalità dell'API di automazione Windows 3,0 nei sistemi operativi seguenti.</span><span class="sxs-lookup"><span data-stu-id="04952-127">The Platform Update for Windows Vista and the Platform Update for Windows Server 2008 both support the entire Windows Automation API 3.0 feature set on the following operating systems.</span></span>

-   <span data-ttu-id="04952-128">Windows XP (Inglese)</span><span class="sxs-lookup"><span data-stu-id="04952-128">Windows XP (English)</span></span> <dl> <span data-ttu-id="04952-129">Windows XP Home SP3 x86</span><span class="sxs-lookup"><span data-stu-id="04952-129">Windows XP Home SP3 x86</span></span>  
    <span data-ttu-id="04952-130">Windows XP Professional SP3 x86</span><span class="sxs-lookup"><span data-stu-id="04952-130">Windows XP Professional SP3 x86</span></span>  
    </dl>
-   Windows Server 2003 (English) <dl> <span data-ttu-id="04952-131">Windows Server 2003 SP2 (x86 e x64)</span><span class="sxs-lookup"><span data-stu-id="04952-131">Windows Server 2003 SP2 (x86 and x64)</span></span>  
    </dl>
-   <span data-ttu-id="04952-132">Windows Vista (Inglese)</span><span class="sxs-lookup"><span data-stu-id="04952-132">Windows Vista (English)</span></span> <dl> <span data-ttu-id="04952-133">Starter SP2 (x86 e x64)</span><span class="sxs-lookup"><span data-stu-id="04952-133">Starter SP2 (x86 and x64)</span></span>  
    <span data-ttu-id="04952-134">Home Premium SP2 (x86 e x64)</span><span class="sxs-lookup"><span data-stu-id="04952-134">Home Premium SP2 (x86 and x64)</span></span>  
    <span data-ttu-id="04952-135">Business SP2 (x86 e x64)</span><span class="sxs-lookup"><span data-stu-id="04952-135">Business SP2 (x86 and x64)</span></span>  
    <span data-ttu-id="04952-136">Enterprise SP2 (x86 e x64)</span><span class="sxs-lookup"><span data-stu-id="04952-136">Enterprise SP2 (x86 and x64)</span></span>  
    <span data-ttu-id="04952-137">Ultimate SP2 (x86 e x64)</span><span class="sxs-lookup"><span data-stu-id="04952-137">Ultimate SP2 (x86 and x64)</span></span>  
    </dl>
-   <span data-ttu-id="04952-138">Windows Server 2008 (Inglese)</span><span class="sxs-lookup"><span data-stu-id="04952-138">Windows Server 2008 (English)</span></span> <dl> <span data-ttu-id="04952-139">Windows Server 2008 SP2 (x86 e x64)</span><span class="sxs-lookup"><span data-stu-id="04952-139">Windows Server 2008 SP2 (x86 and x64)</span></span>  
    </dl>

<span data-ttu-id="04952-140">Per ulteriori informazioni su entrambi gli aggiornamenti, vedere [aggiornamento della piattaforma per Windows Vista](../win7ip/platform-update-for-windows-vista-portal.md).</span><span class="sxs-lookup"><span data-stu-id="04952-140">For more information about both updates, see [Platform Update for Windows Vista](../win7ip/platform-update-for-windows-vista-portal.md).</span></span>

## <a name="in-this-section"></a><span data-ttu-id="04952-141">Contenuto della sezione</span><span class="sxs-lookup"><span data-stu-id="04952-141">In this section</span></span>

-   [<span data-ttu-id="04952-142">Nozioni fondamentali sull'automazione interfaccia utente</span><span class="sxs-lookup"><span data-stu-id="04952-142">UI Automation Fundamentals</span></span>](entry-uiautocore-overview.md)
-   [<span data-ttu-id="04952-143">Guida per programmatori del provider di automazione interfaccia utente</span><span class="sxs-lookup"><span data-stu-id="04952-143">UI Automation Provider Programmer's Guide</span></span>](uiauto-providerportal.md)
-   [<span data-ttu-id="04952-144">Guida per programmatori client di automazione interfaccia utente</span><span class="sxs-lookup"><span data-stu-id="04952-144">UI Automation Client Programmer's Guide</span></span>](uiauto-clientportal.md)
-   [<span data-ttu-id="04952-145">Riferimento</span><span class="sxs-lookup"><span data-stu-id="04952-145">Reference</span></span>](entry-uiautocore-ref.md)
-   [<span data-ttu-id="04952-146">Esempi</span><span class="sxs-lookup"><span data-stu-id="04952-146">Samples</span></span>](samples-entry.md)
-   [<span data-ttu-id="04952-147">Appendici</span><span class="sxs-lookup"><span data-stu-id="04952-147">Appendixes</span></span>](appendix-entry.md)

 

 