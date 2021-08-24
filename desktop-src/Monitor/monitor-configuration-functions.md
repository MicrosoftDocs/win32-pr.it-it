---
title: Monitorare le funzioni di configurazione
description: Monitorare le funzioni di configurazione
ms.assetid: e9a00792-f471-47a4-93d7-25400e27f13f
keywords:
- monitor,funzioni
- monitor, funzioni di alto livello
- monitor, funzioni di basso livello
- monitor,funzioni di enumerazione
- funzioni di alto livello
- funzioni di basso livello
- funzioni di enumerazione
- monitorare la configurazione, funzioni
- monitorare la configurazione, funzioni di alto livello
- monitorare la configurazione, funzioni di basso livello
- monitorare la configurazione, funzioni di enumerazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0b8b4eca3e18b5a5254ef9adc8cd55e123c26a773149d323caf517c5429d972f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119013439"
---
# <a name="monitor-configuration-functions"></a>Monitorare le funzioni di configurazione

Le funzioni seguenti vengono usate per ottenere informazioni da un monitoraggio e per modificare le impostazioni di un monitoraggio. Le funzioni di configurazione di monitoraggio sono classificate in funzioni di alto livello, funzioni di basso livello e funzioni di enumerazione. Per altre informazioni, vedere [Uso della configurazione di Monitoraggio](using-monitor-configuration.md).

## <a name="high-level-functions"></a>High-Level funzioni



| Funzione                                                                         | Descrizione                                                                          |
|----------------------------------------------------------------------------------|--------------------------------------------------------------------------------------|
| [**DegaussMonitor**](/windows/desktop/api/HighLevelMonitorConfigurationAPI/nf-highlevelmonitorconfigurationapi-degaussmonitor)                                         | Esegue la degaussazione di un monitoraggio.                                                                 |
| [**GetMonitorBrightness**](/windows/desktop/api/HighLevelMonitorConfigurationAPI/nf-highlevelmonitorconfigurationapi-getmonitorbrightness)                             | Recupera le impostazioni di luminosità minima, massima e corrente di un monitor.             |
| [**GetMonitorCapabilities**](/windows/desktop/api/HighLevelMonitorConfigurationAPI/nf-highlevelmonitorconfigurationapi-getmonitorcapabilities)                         | Recupera le funzionalità di configurazione di un monitoraggio.                               |
| [**GetMonitorColorTemperature**](/windows/desktop/api/HighLevelMonitorConfigurationAPI/nf-highlevelmonitorconfigurationapi-getmonitorcolortemperature)                 | Recupera la temperatura del colore corrente di un monitoraggio.                                     |
| [**GetMonitorContrast**](/windows/desktop/api/HighLevelMonitorConfigurationAPI/nf-highlevelmonitorconfigurationapi-getmonitorcontrast)                                 | Recupera le impostazioni di contrasto minime, massime e correnti di un monitoraggio.               |
| [**GetMonitorDisplayAreaPosition**](/windows/desktop/api/HighLevelMonitorConfigurationAPI/nf-highlevelmonitorconfigurationapi-getmonitordisplayareaposition)           | Recupera la posizione orizzontale o verticale minima, massima e corrente di un monitor. |
| [**GetMonitorDisplayAreaSize**](/windows/desktop/api/HighLevelMonitorConfigurationAPI/nf-highlevelmonitorconfigurationapi-getmonitordisplayareasize)                   | Recupera la larghezza o l'altezza minima, massima e corrente di un monitor.                 |
| [**GetMonitorRedGreenOrBlueDrive**](/windows/desktop/api/HighLevelMonitorConfigurationAPI/nf-highlevelmonitorconfigurationapi-getmonitorredgreenorbluedrive)           | Recupera il valore dell'unità rossa, verde o blu di un monitoraggio.                               |
| [**GetMonitorRedGreenOrBlueGain**](/windows/desktop/api/HighLevelMonitorConfigurationAPI/nf-highlevelmonitorconfigurationapi-getmonitorredgreenorbluegain)             | Recupera il valore di guadagno rosso, verde o blu di un monitoraggio.                                |
| [**GetMonitorTechnologyType**](/windows/desktop/api/HighLevelMonitorConfigurationAPI/nf-highlevelmonitorconfigurationapi-getmonitortechnologytype)                     | Recupera il tipo di tecnologia usato da un monitoraggio.                                  |
| [**RestoreMonitorFactoryColorDefaults**](/windows/desktop/api/HighLevelMonitorConfigurationAPI/nf-highlevelmonitorconfigurationapi-restoremonitorfactorycolordefaults) | Ripristina le impostazioni dei colori di un monitor alle impostazioni predefinite predefinite.                       |
| [**RestoreMonitorFactoryDefaults**](/windows/desktop/api/HighLevelMonitorConfigurationAPI/nf-highlevelmonitorconfigurationapi-restoremonitorfactorydefaults)           | Ripristina le impostazioni predefinite di un monitoraggio.                             |
| [**SaveCurrentMonitorSettings**](/windows/desktop/api/HighLevelMonitorConfigurationAPI/nf-highlevelmonitorconfigurationapi-savecurrentmonitorsettings)                 | Salva le impostazioni di monitoraggio correnti nella memoria non volatile dello schermo.             |
| [**SetMonitorBrightness**](/windows/desktop/api/HighLevelMonitorConfigurationAPI/nf-highlevelmonitorconfigurationapi-setmonitorbrightness)                             | Imposta il valore di luminosità di un monitor.                                                   |
| [**SetMonitorColorTemperature**](/windows/desktop/api/HighLevelMonitorConfigurationAPI/nf-highlevelmonitorconfigurationapi-setmonitorcolortemperature)                 | Imposta la temperatura del colore di un monitor.                                                  |
| [**SetMonitorContrast**](/windows/desktop/api/HighLevelMonitorConfigurationAPI/nf-highlevelmonitorconfigurationapi-setmonitorcontrast)                                 | Imposta il valore di contrasto di un monitor.                                                     |
| [**SetMonitorDisplayAreaPosition**](/windows/desktop/api/HighLevelMonitorConfigurationAPI/nf-highlevelmonitorconfigurationapi-setmonitordisplayareaposition)           | Imposta la posizione orizzontale o verticale dell'area di visualizzazione di un monitor.                |
| [**SetMonitorDisplayAreaSize**](/windows/desktop/api/HighLevelMonitorConfigurationAPI/nf-highlevelmonitorconfigurationapi-setmonitordisplayareasize)                   | Imposta la larghezza o l'altezza dell'area di visualizzazione di un monitor.                                |
| [**SetMonitorRedGreenOrBlueDrive**](/windows/desktop/api/HighLevelMonitorConfigurationAPI/nf-highlevelmonitorconfigurationapi-setmonitorredgreenorbluedrive)           | Imposta il valore dell'unità rossa, verde o blu di un monitor.                                    |
| [**SetMonitorRedGreenOrBlueGain**](/windows/desktop/api/HighLevelMonitorConfigurationAPI/nf-highlevelmonitorconfigurationapi-setmonitorredgreenorbluegain)             | Imposta il valore di guadagno rosso, verde o blu di un monitor.                                     |



 

## <a name="low-level-functions"></a>Low-Level funzioni



| Funzione                                                                                   | Descrizione                                                                                                    |
|--------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------|
| [**CapabilitiesRequestAndCapabilitiesReply**](/windows/desktop/api/LowLevelMonitorConfigurationAPI/nf-lowlevelmonitorconfigurationapi-capabilitiesrequestandcapabilitiesreply) | Recupera una stringa che descrive le funzionalità di un monitoraggio.                                                        |
| [**GetCapabilitiesStringLength**](/windows/desktop/api/LowLevelMonitorConfigurationAPI/nf-lowlevelmonitorconfigurationapi-getcapabilitiesstringlength)                         | Recupera la lunghezza della stringa di funzionalità di un monitoraggio.                                                       |
| [**GetTimingReport**](/windows/desktop/api/LowLevelMonitorConfigurationAPI/nf-lowlevelmonitorconfigurationapi-gettimingreport)                                                 | Recupera le frequenze di sincronizzazione orizzontale e verticale di un monitoraggio.                                     |
| [**GetVCPFeatureAndVCPFeatureReply**](/windows/desktop/api/LowLevelMonitorConfigurationAPI/nf-lowlevelmonitorconfigurationapi-getvcpfeatureandvcpfeaturereply)                 | Recupera il valore corrente, il valore massimo e il tipo di codice di un codice vcp (Virtual Pannello di controllo) per un monitoraggio. |
| [**SaveCurrentSettings**](/windows/desktop/api/LowLevelMonitorConfigurationAPI/nf-lowlevelmonitorconfigurationapi-savecurrentsettings)                                         | Salva le impostazioni di monitoraggio correnti nella memoria non volatile dello schermo.                                       |
| [**SetVCPFeature**](/windows/desktop/api/LowLevelMonitorConfigurationAPI/nf-lowlevelmonitorconfigurationapi-setvcpfeature)                                                     | Imposta il valore di un codice vcp (Virtual Pannello di controllo) per un monitoraggio.                                            |



 

## <a name="enumeration-functions"></a>Funzioni di enumerazione



| Funzione                                                                                                   | Descrizione                                                                               |
|------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------|
| [**DestroyPhysicalMonitor**](/windows/desktop/api/PhysicalMonitorEnumerationAPI/nf-physicalmonitorenumerationapi-destroyphysicalmonitor)                                                   | Chiude un handle per un monitoraggio fisico.                                                    |
| [**DestroyPhysicalMonitors**](/windows/desktop/api/PhysicalMonitorEnumerationAPI/nf-physicalmonitorenumerationapi-destroyphysicalmonitors)                                                 | Chiude una matrice di handle di monitoraggio fisico.                                              |
| [**GetNumberOfPhysicalMonitorsFromHMONITOR**](/windows/desktop/api/PhysicalMonitorEnumerationAPI/nf-physicalmonitorenumerationapi-getnumberofphysicalmonitorsfromhmonitor)                 | Recupera il numero di monitoraggi fisici associati a un handle di monitoraggio **HMONITOR.** |
| [**GetNumberOfPhysicalMonitorsFromIDirect3DDevice9**](/windows/desktop/api/PhysicalMonitorEnumerationAPI/nf-physicalmonitorenumerationapi-getnumberofphysicalmonitorsfromidirect3ddevice9) | Recupera il numero di monitor fisici associati a un dispositivo Direct3D.              |
| [**GetPhysicalMonitorsFromHMONITOR**](/windows/desktop/api/PhysicalMonitorEnumerationAPI/nf-physicalmonitorenumerationapi-getphysicalmonitorsfromhmonitor)                                 | Recupera i monitoraggi fisici associati a un handle di monitoraggio **HMONITOR.**           |
| [**GetPhysicalMonitorsFromIDirect3DDevice9**](/windows/desktop/api/PhysicalMonitorEnumerationAPI/nf-physicalmonitorenumerationapi-getphysicalmonitorsfromidirect3ddevice9)                 | Recupera i monitoraggi fisici associati a un dispositivo Direct3D.                        |



 

## <a name="internal-functions"></a>Funzioni interne

Le funzioni seguenti vengono usate dall'API di configurazione del monitoraggio per accedere alle funzionalità nel driver video. Le applicazioni non devono chiamare queste funzioni.

-   [**DDCCIGetCapabilitiesString**](ddccigetcapabilitiesstring.md)
-   [**DDCCIGetCapabilitiesStringLength**](ddccigetcapabilitiesstringlength.md)
-   [**DDCCIGetTimingReport**](ddccigettimingreport.md)
-   [**DDCCIGetVCPFeature**](ddccigetvcpfeature.md)
-   [**DDCCISaveCurrentSettings**](ddccisavecurrentsettings.md)
-   [**DDCCISetVCPFeature**](ddccisetvcpfeature.md)
-   [**DestroyPhysicalMonitorInternal**](destroyphysicalmonitorinternal.md)
-   [**GetNumberOfPhysicalMonitors**](getnumberofphysicalmonitors.md)
-   [**GetPhysicalMonitorDescription**](getphysicalmonitordescription.md)
-   [**GetPhysicalMonitors**](getphysicalmonitors.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Informazioni di riferimento sulla configurazione del monitoraggio](monitor-configuration-reference.md)
</dt> </dl>

 

 




