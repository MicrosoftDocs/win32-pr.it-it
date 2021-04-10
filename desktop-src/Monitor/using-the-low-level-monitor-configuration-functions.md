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
# <a name="using-the-low-level-monitor-configuration-functions"></a>Uso delle funzioni di configurazione di monitoraggio Low-Level

Prima di usare le funzioni di configurazione di monitoraggio di basso livello, è necessario avere familiarità con questi standard:

-   Visualizzazione dell'interfaccia di comando del canale dati (DDC/CI)
-   Set di comandi di controllo VESA monitor (MCCS)

Le funzioni di basso livello funzionano ottenendo e impostando i valori dei codici del pannello di controllo virtuale (VCP). Un codice VCP può essere *continuo* o non *continuo*. I codici continui possono assumere qualsiasi valore compreso tra zero e un valore massimo specifico del fornitore. I codici non continui supportano un set definito di valori, anch ' esso specifico per il fornitore.

Per utilizzare le funzioni di configurazione di monitoraggio di basso livello, attenersi alla procedura seguente:

1.  Ottenere un handle **HMONITOR** chiamando [**EnumDisplayMonitors**](/windows/desktop/api/winuser/nf-winuser-enumdisplaymonitors) o [**MonitorFromWindow**](/windows/desktop/api/winuser/nf-winuser-monitorfromwindow).
2.  Chiamare [**GetNumberOfPhysicalMonitorsFromHMONITOR**](/windows/desktop/api/PhysicalMonitorEnumerationAPI/nf-physicalmonitorenumerationapi-getnumberofphysicalmonitorsfromhmonitor) per ottenere il numero di monitoraggi fisici associati all'handle **HMONITOR** .
3.  Chiamare [**GetPhysicalMonitorsFromHMONITOR**](/windows/desktop/api/PhysicalMonitorEnumerationAPI/nf-physicalmonitorenumerationapi-getphysicalmonitorsfromhmonitor) per ottenere un elenco di handle per i monitoraggi fisici.
4.  Chiamare [**GetCapabilitiesStringLength**](/windows/desktop/api/LowLevelMonitorConfigurationAPI/nf-lowlevelmonitorconfigurationapi-getcapabilitiesstringlength) per ottenere la lunghezza della stringa delle funzionalità DDC/ci di un monitoraggio. La stringa capabilities è una stringa ASCII che contiene informazioni statiche sul monitoraggio. Una parte della stringa elenca i codici VCP supportati dal monitoraggio. Nella stringa sono inoltre elencati i valori supportati dei codici VCP non continui.
5.  Allocare un buffer per memorizzare la stringa delle funzionalità e chiamare [**CapabilitiesRequestAndCapabilitiesReply**](/windows/desktop/api/LowLevelMonitorConfigurationAPI/nf-lowlevelmonitorconfigurationapi-capabilitiesrequestandcapabilitiesreply) per ottenere la stringa.
6.  Analizzare la stringa delle funzionalità per determinare quali codici VCP sono supportati dal monitoraggio.
7.  Per un codice VCP continuo, chiamare [**GetVCPFeatureAndVCPFeatureReply**](/windows/desktop/api/LowLevelMonitorConfigurationAPI/nf-lowlevelmonitorconfigurationapi-getvcpfeatureandvcpfeaturereply) per ottenere i valori correnti e massimi del codice. Per un codice VCP non continuo, analizzare la stringa delle funzionalità per ottenere i valori supportati.
8.  Chiamare [**SetVCPFeature**](/windows/desktop/api/LowLevelMonitorConfigurationAPI/nf-lowlevelmonitorconfigurationapi-setvcpfeature) per impostare un nuovo valore per un codice VCP.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Uso della configurazione di monitoraggio**](using-monitor-configuration.md)
</dt> </dl>

 

 