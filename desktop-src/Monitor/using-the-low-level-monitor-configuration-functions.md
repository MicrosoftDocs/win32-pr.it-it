---
title: Uso delle funzioni di configurazione di monitoraggio Low-Level
description: Uso delle funzioni di configurazione di monitoraggio Low-Level
ms.assetid: 014a144b-d01a-4bc1-959d-08a643b3e1f5
keywords:
- monitoraggio, funzioni
- monitoraggio, funzioni di configurazione di basso livello
- monitoraggio, DDC/CI
- monitorare, visualizzare l'interfaccia del comando del canale dati
- configurazione del monitoraggio, funzioni di configurazione di basso livello
- configurazione del monitoraggio, funzioni
- configurazione del monitoraggio, DDC/CI
- configurare il monitoraggio, visualizzare l'interfaccia del comando del canale dati
- funzioni di configurazione di basso livello
- Interfaccia del comando Visualizza canale dati
- DDC/CI
- Set di comandi di controllo VESA monitor (MCCS)
- Set di comandi di controllo Monitor (MCCS)
- MCCS (set di comandi di controllo monitor)
- Pannello di controllo virtuale (VCP)
- VCP (pannello di controllo virtuale)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8d98e2cd4d85cb972b6a13896e9c497e51e16f8d
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "103963027"
---
# <a name="using-the-low-level-monitor-configuration-functions"></a><span data-ttu-id="5a874-119">Uso delle funzioni di configurazione di monitoraggio Low-Level</span><span class="sxs-lookup"><span data-stu-id="5a874-119">Using the Low-Level Monitor Configuration Functions</span></span>

<span data-ttu-id="5a874-120">Prima di usare le funzioni di configurazione di monitoraggio di basso livello, è necessario avere familiarità con questi standard:</span><span class="sxs-lookup"><span data-stu-id="5a874-120">Before using the low-level monitor configuration functions, you should be familiar with these standards:</span></span>

-   <span data-ttu-id="5a874-121">Visualizzazione dell'interfaccia di comando del canale dati (DDC/CI)</span><span class="sxs-lookup"><span data-stu-id="5a874-121">Display Data Channel Command Interface (DDC/CI)</span></span>
-   <span data-ttu-id="5a874-122">Set di comandi di controllo VESA monitor (MCCS)</span><span class="sxs-lookup"><span data-stu-id="5a874-122">VESA Monitor Control Command Set (MCCS)</span></span>

<span data-ttu-id="5a874-123">Le funzioni di basso livello funzionano ottenendo e impostando i valori dei codici del pannello di controllo virtuale (VCP).</span><span class="sxs-lookup"><span data-stu-id="5a874-123">The low-level functions work by getting and setting the values of Virtual Control Panel (VCP) codes.</span></span> <span data-ttu-id="5a874-124">Un codice VCP può essere *continuo* o non *continuo*.</span><span class="sxs-lookup"><span data-stu-id="5a874-124">A VCP code can be *continuous* or *noncontinuous*.</span></span> <span data-ttu-id="5a874-125">I codici continui possono assumere qualsiasi valore compreso tra zero e un valore massimo specifico del fornitore.</span><span class="sxs-lookup"><span data-stu-id="5a874-125">Continuous codes can assume any value between zero and a vendor-specific maximum value.</span></span> <span data-ttu-id="5a874-126">I codici non continui supportano un set definito di valori, anch ' esso specifico per il fornitore.</span><span class="sxs-lookup"><span data-stu-id="5a874-126">Noncontinuous codes support a defined set of values, which is also specific to the vendor.</span></span>

<span data-ttu-id="5a874-127">Per utilizzare le funzioni di configurazione di monitoraggio di basso livello, attenersi alla procedura seguente:</span><span class="sxs-lookup"><span data-stu-id="5a874-127">To use the low-level monitor configuration functions, perform the following steps:</span></span>

1.  <span data-ttu-id="5a874-128">Ottenere un handle **HMONITOR** chiamando [**EnumDisplayMonitors**](/windows/desktop/api/winuser/nf-winuser-enumdisplaymonitors) o [**MonitorFromWindow**](/windows/desktop/api/winuser/nf-winuser-monitorfromwindow).</span><span class="sxs-lookup"><span data-stu-id="5a874-128">Obtain an **HMONITOR** handle by calling [**EnumDisplayMonitors**](/windows/desktop/api/winuser/nf-winuser-enumdisplaymonitors) or [**MonitorFromWindow**](/windows/desktop/api/winuser/nf-winuser-monitorfromwindow).</span></span>
2.  <span data-ttu-id="5a874-129">Chiamare [**GetNumberOfPhysicalMonitorsFromHMONITOR**](/windows/desktop/api/PhysicalMonitorEnumerationAPI/nf-physicalmonitorenumerationapi-getnumberofphysicalmonitorsfromhmonitor) per ottenere il numero di monitoraggi fisici associati all'handle **HMONITOR** .</span><span class="sxs-lookup"><span data-stu-id="5a874-129">Call [**GetNumberOfPhysicalMonitorsFromHMONITOR**](/windows/desktop/api/PhysicalMonitorEnumerationAPI/nf-physicalmonitorenumerationapi-getnumberofphysicalmonitorsfromhmonitor) to get the number of physical monitors associated with the **HMONITOR** handle.</span></span>
3.  <span data-ttu-id="5a874-130">Chiamare [**GetPhysicalMonitorsFromHMONITOR**](/windows/desktop/api/PhysicalMonitorEnumerationAPI/nf-physicalmonitorenumerationapi-getphysicalmonitorsfromhmonitor) per ottenere un elenco di handle per i monitoraggi fisici.</span><span class="sxs-lookup"><span data-stu-id="5a874-130">Call [**GetPhysicalMonitorsFromHMONITOR**](/windows/desktop/api/PhysicalMonitorEnumerationAPI/nf-physicalmonitorenumerationapi-getphysicalmonitorsfromhmonitor) to get a list of handles to the physical monitors.</span></span>
4.  <span data-ttu-id="5a874-131">Chiamare [**GetCapabilitiesStringLength**](/windows/desktop/api/LowLevelMonitorConfigurationAPI/nf-lowlevelmonitorconfigurationapi-getcapabilitiesstringlength) per ottenere la lunghezza della stringa delle funzionalità DDC/ci di un monitoraggio.</span><span class="sxs-lookup"><span data-stu-id="5a874-131">Call [**GetCapabilitiesStringLength**](/windows/desktop/api/LowLevelMonitorConfigurationAPI/nf-lowlevelmonitorconfigurationapi-getcapabilitiesstringlength) to get the length of a monitor's DDC/CI capabilities string.</span></span> <span data-ttu-id="5a874-132">La stringa capabilities è una stringa ASCII che contiene informazioni statiche sul monitoraggio.</span><span class="sxs-lookup"><span data-stu-id="5a874-132">The capabilities string is an ASCII string that contains static information about the monitor.</span></span> <span data-ttu-id="5a874-133">Una parte della stringa elenca i codici VCP supportati dal monitoraggio.</span><span class="sxs-lookup"><span data-stu-id="5a874-133">One part of the string lists the VCP codes that the monitor supports.</span></span> <span data-ttu-id="5a874-134">Nella stringa sono inoltre elencati i valori supportati dei codici VCP non continui.</span><span class="sxs-lookup"><span data-stu-id="5a874-134">The string also lists the supported values of the noncontinuous VCP codes.</span></span>
5.  <span data-ttu-id="5a874-135">Allocare un buffer per memorizzare la stringa delle funzionalità e chiamare [**CapabilitiesRequestAndCapabilitiesReply**](/windows/desktop/api/LowLevelMonitorConfigurationAPI/nf-lowlevelmonitorconfigurationapi-capabilitiesrequestandcapabilitiesreply) per ottenere la stringa.</span><span class="sxs-lookup"><span data-stu-id="5a874-135">Allocate a buffer to hold the capabilities string and call [**CapabilitiesRequestAndCapabilitiesReply**](/windows/desktop/api/LowLevelMonitorConfigurationAPI/nf-lowlevelmonitorconfigurationapi-capabilitiesrequestandcapabilitiesreply) to get the string.</span></span>
6.  <span data-ttu-id="5a874-136">Analizzare la stringa delle funzionalità per determinare quali codici VCP sono supportati dal monitoraggio.</span><span class="sxs-lookup"><span data-stu-id="5a874-136">Parse the capabilities string to determine which VCP codes the monitor supports.</span></span>
7.  <span data-ttu-id="5a874-137">Per un codice VCP continuo, chiamare [**GetVCPFeatureAndVCPFeatureReply**](/windows/desktop/api/LowLevelMonitorConfigurationAPI/nf-lowlevelmonitorconfigurationapi-getvcpfeatureandvcpfeaturereply) per ottenere i valori correnti e massimi del codice.</span><span class="sxs-lookup"><span data-stu-id="5a874-137">For a continuous VCP code, call [**GetVCPFeatureAndVCPFeatureReply**](/windows/desktop/api/LowLevelMonitorConfigurationAPI/nf-lowlevelmonitorconfigurationapi-getvcpfeatureandvcpfeaturereply) to get the current and maximum values of the code.</span></span> <span data-ttu-id="5a874-138">Per un codice VCP non continuo, analizzare la stringa delle funzionalità per ottenere i valori supportati.</span><span class="sxs-lookup"><span data-stu-id="5a874-138">For a noncontinuous VCP code, parse the capabilities string to get the supported values.</span></span>
8.  <span data-ttu-id="5a874-139">Chiamare [**SetVCPFeature**](/windows/desktop/api/LowLevelMonitorConfigurationAPI/nf-lowlevelmonitorconfigurationapi-setvcpfeature) per impostare un nuovo valore per un codice VCP.</span><span class="sxs-lookup"><span data-stu-id="5a874-139">Call [**SetVCPFeature**](/windows/desktop/api/LowLevelMonitorConfigurationAPI/nf-lowlevelmonitorconfigurationapi-setvcpfeature) to set a new value for a VCP code.</span></span>

## <a name="related-topics"></a><span data-ttu-id="5a874-140">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="5a874-140">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5a874-141">**Uso della configurazione di monitoraggio**</span><span class="sxs-lookup"><span data-stu-id="5a874-141">**Using Monitor Configuration**</span></span>](using-monitor-configuration.md)
</dt> </dl>

 

 