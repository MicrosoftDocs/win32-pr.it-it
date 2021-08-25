---
title: Uso delle funzioni Low-Level Monitoraggio prestazioni
description: Uso delle funzioni Low-Level Monitoraggio prestazioni
ms.assetid: 014a144b-d01a-4bc1-959d-08a643b3e1f5
keywords:
- monitoraggio, funzioni
- monitoraggio, funzioni di configurazione di basso livello
- monitoraggio, DDC/CI
- monitor,Display Data Channel Command Interface
- monitorare la configurazione, funzioni di configurazione di basso livello
- monitorare la configurazione, funzioni
- configurazione del monitoraggio, DDC/CI
- configurazione del monitoraggio, interfaccia dei comandi del canale dati di visualizzazione
- funzioni di configurazione di basso livello
- Interfaccia dei comandi del canale dati di visualizzazione
- DDC/CI
- VESA Monitor Control Command Set (MCCS)
- Monitor Control Command Set (MCCS)
- MCCS (Monitor Control Command Set)
- Virtual Pannello di controllo (VCP)
- VCP (Virtual Pannello di controllo)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f3ffd21f0b232db71bb6023f968122271ce70f03b0a632dc33d9df1e7ee993bf
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119927391"
---
# <a name="using-the-low-level-monitor-configuration-functions"></a>Uso delle funzioni Low-Level Monitoraggio prestazioni

Prima di usare le funzioni di configurazione del monitoraggio di basso livello, è necessario avere familiarità con questi standard:

-   Interfaccia DDC/CI (Display Data Channel Command Interface)
-   VESA Monitor Control Command Set (MCCS)

Le funzioni di basso livello funzionano ottenendo e impostando i valori dei codici vcp (Virtual Pannello di controllo). Un codice VCP può *essere continuo* o *non costante.* I codici continui possono presupporre qualsiasi valore compreso tra zero e un valore massimo specifico del fornitore. I codici non contigui supportano un set definito di valori, che è anche specifico del fornitore.

Per usare le funzioni di configurazione del monitoraggio di basso livello, seguire questa procedura:

1.  Ottenere un handle **HMONITOR** chiamando [**EnumDisplayMonitors**](/windows/desktop/api/winuser/nf-winuser-enumdisplaymonitors) o [**MonitorFromWindow.**](/windows/desktop/api/winuser/nf-winuser-monitorfromwindow)
2.  Chiamare [**GetNumberOfPhysicalMonitorsFromHMONITOR**](/windows/desktop/api/PhysicalMonitorEnumerationAPI/nf-physicalmonitorenumerationapi-getnumberofphysicalmonitorsfromhmonitor) per ottenere il numero di monitor fisici associati all'handle **HMONITOR.**
3.  Chiamare [**GetPhysicalMonitorsFromHMONITOR**](/windows/desktop/api/PhysicalMonitorEnumerationAPI/nf-physicalmonitorenumerationapi-getphysicalmonitorsfromhmonitor) per ottenere un elenco di handle per i monitor fisici.
4.  Chiamare [**GetCapabilitiesStringLength**](/windows/desktop/api/LowLevelMonitorConfigurationAPI/nf-lowlevelmonitorconfigurationapi-getcapabilitiesstringlength) per ottenere la lunghezza della stringa delle funzionalità DDC/CI di un monitoraggio. La stringa capabilities è una stringa ASCII che contiene informazioni statiche sul monitoraggio. Una parte della stringa elenca i codici VCP supportati dal monitoraggio. La stringa elenca anche i valori supportati dei codici VCP non contigui.
5.  Allocare un buffer per contenere la stringa capabilities e chiamare [**CapabilitiesRequestAndCapabilitiesReply**](/windows/desktop/api/LowLevelMonitorConfigurationAPI/nf-lowlevelmonitorconfigurationapi-capabilitiesrequestandcapabilitiesreply) per ottenere la stringa.
6.  Analizzare la stringa capabilities per determinare i codici VCP supportati dal monitoraggio.
7.  Per un codice VCP continuo, chiamare [**GetVCPFeatureAndVCPFeatureReply**](/windows/desktop/api/LowLevelMonitorConfigurationAPI/nf-lowlevelmonitorconfigurationapi-getvcpfeatureandvcpfeaturereply) per ottenere i valori correnti e massimi del codice. Per un codice VCP non contiguo, analizzare la stringa capabilities per ottenere i valori supportati.
8.  Chiamare [**SetVCPFeature**](/windows/desktop/api/LowLevelMonitorConfigurationAPI/nf-lowlevelmonitorconfigurationapi-setvcpfeature) per impostare un nuovo valore per un codice VCP.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Uso della configurazione del monitoraggio**](using-monitor-configuration.md)
</dt> </dl>

 

 