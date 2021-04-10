---
title: Gestione remota Windows
description: Gestione remota Windows (Gestione remota Windows) è l'implementazione Microsoft del protocollo WS-Management, un protocollo standard basato su SOAP, che consente l'interoperabilità di hardware e sistemi operativi di fornitori diversi.
ms.assetid: 6429e748-e0bf-431a-8989-db5b211665d5
ms.tgt_platform: multiple
keywords:
- Gestione remota Windows (WinRM), pagina iniziale
- WS-Management
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbOrient
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 27311699fe0321eddc1d3117b17acf3e49e9d518
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "103963114"
---
# <a name="windows-remote-management"></a><span data-ttu-id="4f578-105">Gestione remota Windows</span><span class="sxs-lookup"><span data-stu-id="4f578-105">Windows Remote Management</span></span>

## <a name="purpose"></a><span data-ttu-id="4f578-106">Scopo</span><span class="sxs-lookup"><span data-stu-id="4f578-106">Purpose</span></span>

<span data-ttu-id="4f578-107">Gestione remota Windows (WinRM) è l'implementazione di Microsoft del [protocollo WS-Management](ws-management-protocol.md), un protocollo standard basato su SOAP (Simple Object Access Protocol) adatto al firewall che consente l'interoperabilità di hardware e sistemi operativi di fornitori diversi.</span><span class="sxs-lookup"><span data-stu-id="4f578-107">Windows Remote Management (WinRM) is the Microsoft implementation of [WS-Management Protocol](ws-management-protocol.md), a standard Simple Object Access Protocol (SOAP)-based, firewall-friendly protocol that allows hardware and operating systems, from different vendors, to interoperate.</span></span>

<span data-ttu-id="4f578-108">La specifica del protocollo WS-Management consente ai sistemi di accedere alle informazioni di gestione e scambiarle attraverso un'infrastruttura IT in modo comune.</span><span class="sxs-lookup"><span data-stu-id="4f578-108">The WS-Management protocol specification provides a common way for systems to access and exchange management information across an IT infrastructure.</span></span> <span data-ttu-id="4f578-109">WinRM e [*Intelligent Platform Management Interface (IPMI)*](windows-remote-management-glossary.md), insieme all' [agente di raccolta eventi](/previous-versions/windows/it-pro/windows-server-2003/cc785056(v=ws.10)) sono componenti delle funzionalità di [gestione hardware di Windows](/previous-versions/windows/it-pro/windows-server-2003/cc785056(v=ws.10)) .</span><span class="sxs-lookup"><span data-stu-id="4f578-109">WinRM and [*Intelligent Platform Management Interface (IPMI)*](windows-remote-management-glossary.md), along with the [Event Collector](/previous-versions/windows/it-pro/windows-server-2003/cc785056(v=ws.10)) are components of the [Windows Hardware Management](/previous-versions/windows/it-pro/windows-server-2003/cc785056(v=ws.10)) features.</span></span>

## <a name="where-applicable"></a><span data-ttu-id="4f578-110">Se applicabile</span><span class="sxs-lookup"><span data-stu-id="4f578-110">Where applicable</span></span>

<span data-ttu-id="4f578-111">È possibile utilizzare gli oggetti di scripting WinRM, lo strumento da riga di comando WinRM o lo strumento da riga di comando Windows Remote Shell WinRS per ottenere i dati di gestione da computer locali e remoti che possono disporre di [*controller di gestione battiscopa (BMC)*](windows-remote-management-glossary.md).</span><span class="sxs-lookup"><span data-stu-id="4f578-111">You can use WinRM scripting objects, the WinRM command-line tool, or the Windows Remote Shell command line tool WinRS to obtain management data from local and remote computers that may have [*baseboard management controllers (BMCs)*](windows-remote-management-glossary.md).</span></span> <span data-ttu-id="4f578-112">Se il computer esegue una versione del sistema operativo basata su Windows che include WinRM, i dati di gestione vengono forniti da [Strumentazione gestione Windows (WMI)](/windows/desktop/WmiSdk/wmi-start-page).</span><span class="sxs-lookup"><span data-stu-id="4f578-112">If the computer runs a Windows-based operating system version that includes WinRM, the management data is supplied by [Windows Management Instrumentation (WMI)](/windows/desktop/WmiSdk/wmi-start-page).</span></span>

<span data-ttu-id="4f578-113">È inoltre possibile recuperare dati di sistema e hardware dalle implementazioni del protocollo WS-Management in esecuzione nella propria azienda su sistemi operativi diversi da Windows.</span><span class="sxs-lookup"><span data-stu-id="4f578-113">You can also obtain hardware and system data from WS-Management protocol implementations running on operating systems other than Windows in your enterprise.</span></span> <span data-ttu-id="4f578-114">A differenza di WMI, WinRM stabilisce una sessione con un computer remoto tramite il protocollo WS-Management basato su SOAP anziché una connessione mediante DCOM.</span><span class="sxs-lookup"><span data-stu-id="4f578-114">WinRM establishes a session with a remote computer through the SOAP-based WS-Management protocol rather than a connection through DCOM, as WMI does.</span></span> <span data-ttu-id="4f578-115">I dati restituiti al protocollo WS-Management sono formattati in XML anziché in oggetti.</span><span class="sxs-lookup"><span data-stu-id="4f578-115">Data returned to WS-Management protocol are formatted in XML rather than in objects.</span></span>

<span data-ttu-id="4f578-116">Il provider WMI di [Intelligent Platform Management Interface (IPMI)](/previous-versions/windows/desktop/ipmiprv/ipmi-provider) è un provider WMI standard con classi che ottengono dati del sensore BMC da computer con hardware appropriato.</span><span class="sxs-lookup"><span data-stu-id="4f578-116">The [Intelligent Platform Management Interface (IPMI)](/previous-versions/windows/desktop/ipmiprv/ipmi-provider) WMI provider is a standard WMI provider with classes that obtain BMC sensor data from computers with appropriate hardware.</span></span> <span data-ttu-id="4f578-117">È possibile accedere ai dati IPMI usando l'API di scripting WinRM, lo [Scripting](/windows/desktop/WmiSdk/scripting-api-for-wmi)WMI o le API [com](/windows/desktop/WmiSdk/com-api-for-wmi) .</span><span class="sxs-lookup"><span data-stu-id="4f578-117">IPMI data can be accessed using the WinRM scripting API, the WMI [Scripting](/windows/desktop/WmiSdk/scripting-api-for-wmi), or [COM](/windows/desktop/WmiSdk/com-api-for-wmi) APIs.</span></span>

## <a name="developer-audience"></a><span data-ttu-id="4f578-118">Sviluppatori</span><span class="sxs-lookup"><span data-stu-id="4f578-118">Developer audience</span></span>

<span data-ttu-id="4f578-119">I destinatari degli sviluppatori sono i professionisti IT che scrivono gli script per automatizzare la gestione dei server o degli sviluppatori ISV che ottengono dati per le applicazioni di gestione.</span><span class="sxs-lookup"><span data-stu-id="4f578-119">The developer audience is the IT Pro who writes scripts to automate the management of servers or the ISV developer obtaining data for management applications.</span></span>

## <a name="run-time-requirements"></a><span data-ttu-id="4f578-120">Requisiti di runtime</span><span class="sxs-lookup"><span data-stu-id="4f578-120">Run-time requirements</span></span>

<span data-ttu-id="4f578-121">WinRM fa parte del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="4f578-121">WinRM is part of the operating system.</span></span> <span data-ttu-id="4f578-122">Tuttavia, per ottenere i dati da computer remoti, è necessario configurare un [*listener*](windows-remote-management-glossary.md#l)WinRM.</span><span class="sxs-lookup"><span data-stu-id="4f578-122">However, to obtain data from remote computers, you must configure a WinRM [*listener*](windows-remote-management-glossary.md#l).</span></span> <span data-ttu-id="4f578-123">Per ulteriori informazioni, vedere [installazione e configurazione per gestione remota Windows](installation-and-configuration-for-windows-remote-management.md).</span><span class="sxs-lookup"><span data-stu-id="4f578-123">For more information, see [Installation and Configuration for Windows Remote Management](installation-and-configuration-for-windows-remote-management.md).</span></span> <span data-ttu-id="4f578-124">Se viene rilevato un BMC all'avvio del sistema, il provider IPMI viene caricato; in caso contrario, gli oggetti di scripting WinRM e lo strumento da riga di comando WinRM sono ancora disponibili.</span><span class="sxs-lookup"><span data-stu-id="4f578-124">If a BMC is detected at system startup, then the IPMI provider loads; otherwise, the WinRM scripting objects and the WinRM command-line tool are still available.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="4f578-125">Contenuto della sezione</span><span class="sxs-lookup"><span data-stu-id="4f578-125">In this section</span></span>

<dl> <dt>

[<span data-ttu-id="4f578-126">Informazioni su Gestione remota Windows</span><span class="sxs-lookup"><span data-stu-id="4f578-126">About Windows Remote Management</span></span>](about-windows-remote-management.md)
</dt> <dd>

<span data-ttu-id="4f578-127">Collegamento alla specifica del protocollo public WS-Management, all'architettura WinRM, alla relazione con WMI, alla gestione dell'hardware con il provider IPMI, alla configurazione e all'installazione.</span><span class="sxs-lookup"><span data-stu-id="4f578-127">Link to public WS-Management protocol specification, WinRM architecture, relationship to WMI, hardware management with the IPMI provider, configuration and installation.</span></span>

</dd> <dt>

[<span data-ttu-id="4f578-128">Utilizzo di Gestione remota Windows</span><span class="sxs-lookup"><span data-stu-id="4f578-128">Using Windows Remote Management</span></span>](using-windows-remote-management.md)
</dt> <dd>

<span data-ttu-id="4f578-129">Introduzione all'uso dell'API di scripting WinRM e della gestione dell'hardware.</span><span class="sxs-lookup"><span data-stu-id="4f578-129">Getting started using the WinRM scripting API and hardware management.</span></span>

</dd> <dt>

[<span data-ttu-id="4f578-130">Riferimento Gestione remota Windows</span><span class="sxs-lookup"><span data-stu-id="4f578-130">Windows Remote Management Reference</span></span>](windows-remote-management-reference.md)
</dt> <dd>

<span data-ttu-id="4f578-131">Elenco di interfacce di scripting definite dall'automazione di Microsoft Web Services for Management (WS-Management) e dalle definizioni delle classi WMI create dal provider IPMI e dalle classi che comunicano con il driver IPMI per ottenere i dati [Baseboard Management Controller (BMC)](windows-remote-management-glossary.md) .</span><span class="sxs-lookup"><span data-stu-id="4f578-131">List of scripting interfaces defined by Microsoft Web Services for Management (WS-Management) Automation and class definitions of the WMI classes created by the IPMI provider and classes that communicate with the IPMI driver to obtain [baseboard management controller (BMC)](windows-remote-management-glossary.md) data.</span></span>

</dd> </dl>

 

 