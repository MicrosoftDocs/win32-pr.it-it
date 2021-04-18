---
title: Monitorare le funzioni di configurazione
description: Monitorare le funzioni di configurazione
ms.assetid: e9a00792-f471-47a4-93d7-25400e27f13f
keywords:
- monitoraggio, funzioni
- monitoraggio, funzioni di alto livello
- monitoraggio, funzioni di basso livello
- funzioni di monitoraggio, enumerazione
- funzioni di alto livello
- funzioni di basso livello
- funzioni di enumerazione
- configurazione del monitoraggio, funzioni
- configurazione del monitoraggio, funzioni di alto livello
- configurazione del monitoraggio, funzioni di basso livello
- configurazione del monitoraggio, funzioni di enumerazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 86925cd25912c17b8fb1bdd339888e5429de135b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106298780"
---
# <a name="monitor-configuration-functions"></a>Monitorare le funzioni di configurazione

Le funzioni seguenti vengono utilizzate per ottenere informazioni da un monitoraggio e per modificare le impostazioni di un monitoraggio. Le funzioni di configurazione del monitoraggio sono categorizzate in funzioni di alto livello, funzioni di basso livello e funzioni di enumerazione. Per ulteriori informazioni, vedere [utilizzo della configurazione di monitoraggio](using-monitor-configuration.md).

## <a name="high-level-functions"></a>Funzioni High-Level



| Funzione                                                                         | Descrizione                                                                          |
|----------------------------------------------------------------------------------|--------------------------------------------------------------------------------------|
| [**DegaussMonitor**](/windows/desktop/api/HighLevelMonitorConfigurationAPI/nf-highlevelmonitorconfigurationapi-degaussmonitor)                                         | Viene degaussato un monitoraggio.                                                                 |
| [**GetMonitorBrightness**](/windows/desktop/api/HighLevelMonitorConfigurationAPI/nf-highlevelmonitorconfigurationapi-getmonitorbrightness)                             | Recupera le impostazioni di luminosità minime, massime e correnti di un monitor.             |
| [**GetMonitorCapabilities**](/windows/desktop/api/HighLevelMonitorConfigurationAPI/nf-highlevelmonitorconfigurationapi-getmonitorcapabilities)                         | Recupera le funzionalità di configurazione di un monitoraggio.                               |
| [**GetMonitorColorTemperature**](/windows/desktop/api/HighLevelMonitorConfigurationAPI/nf-highlevelmonitorconfigurationapi-getmonitorcolortemperature)                 | Recupera la temperatura corrente del colore di un monitor.                                     |
| [**GetMonitorContrast**](/windows/desktop/api/HighLevelMonitorConfigurationAPI/nf-highlevelmonitorconfigurationapi-getmonitorcontrast)                                 | Recupera le impostazioni minime, massime e di contrasto correnti di un monitoraggio.               |
| [**GetMonitorDisplayAreaPosition**](/windows/desktop/api/HighLevelMonitorConfigurationAPI/nf-highlevelmonitorconfigurationapi-getmonitordisplayareaposition)           | Recupera la posizione minima, massima e orizzontale corrente di un monitoraggio. |
| [**GetMonitorDisplayAreaSize**](/windows/desktop/api/HighLevelMonitorConfigurationAPI/nf-highlevelmonitorconfigurationapi-getmonitordisplayareasize)                   | Recupera la larghezza o l'altezza minima, massima e corrente di un monitoraggio.                 |
| [**GetMonitorRedGreenOrBlueDrive**](/windows/desktop/api/HighLevelMonitorConfigurationAPI/nf-highlevelmonitorconfigurationapi-getmonitorredgreenorbluedrive)           | Recupera il valore dell'unità rossa, verde o blu di un monitor.                               |
| [**GetMonitorRedGreenOrBlueGain**](/windows/desktop/api/HighLevelMonitorConfigurationAPI/nf-highlevelmonitorconfigurationapi-getmonitorredgreenorbluegain)             | Recupera il valore di guadagno rosso, verde o blu di un monitoraggio.                                |
| [**GetMonitorTechnologyType**](/windows/desktop/api/HighLevelMonitorConfigurationAPI/nf-highlevelmonitorconfigurationapi-getmonitortechnologytype)                     | Recupera il tipo di tecnologia utilizzato da un monitoraggio.                                  |
| [**RestoreMonitorFactoryColorDefaults**](/windows/desktop/api/HighLevelMonitorConfigurationAPI/nf-highlevelmonitorconfigurationapi-restoremonitorfactorycolordefaults) | Ripristina le impostazioni predefinite dei colori di un monitor.                       |
| [**RestoreMonitorFactoryDefaults**](/windows/desktop/api/HighLevelMonitorConfigurationAPI/nf-highlevelmonitorconfigurationapi-restoremonitorfactorydefaults)           | Ripristina le impostazioni predefinite di un monitoraggio.                             |
| [**SaveCurrentMonitorSettings**](/windows/desktop/api/HighLevelMonitorConfigurationAPI/nf-highlevelmonitorconfigurationapi-savecurrentmonitorsettings)                 | Salva le impostazioni di monitoraggio correnti nell'archiviazione non volatile dello schermo.             |
| [**SetMonitorBrightness**](/windows/desktop/api/HighLevelMonitorConfigurationAPI/nf-highlevelmonitorconfigurationapi-setmonitorbrightness)                             | Imposta un valore di luminosità del monitoraggio.                                                   |
| [**SetMonitorColorTemperature**](/windows/desktop/api/HighLevelMonitorConfigurationAPI/nf-highlevelmonitorconfigurationapi-setmonitorcolortemperature)                 | Imposta la temperatura del colore di un monitor.                                                  |
| [**SetMonitorContrast**](/windows/desktop/api/HighLevelMonitorConfigurationAPI/nf-highlevelmonitorconfigurationapi-setmonitorcontrast)                                 | Imposta un valore di contrasto del monitoraggio.                                                     |
| [**SetMonitorDisplayAreaPosition**](/windows/desktop/api/HighLevelMonitorConfigurationAPI/nf-highlevelmonitorconfigurationapi-setmonitordisplayareaposition)           | Imposta la posizione orizzontale o verticale dell'area di visualizzazione di un monitor.                |
| [**SetMonitorDisplayAreaSize**](/windows/desktop/api/HighLevelMonitorConfigurationAPI/nf-highlevelmonitorconfigurationapi-setmonitordisplayareasize)                   | Imposta la larghezza o l'altezza dell'area di visualizzazione di un monitor.                                |
| [**SetMonitorRedGreenOrBlueDrive**](/windows/desktop/api/HighLevelMonitorConfigurationAPI/nf-highlevelmonitorconfigurationapi-setmonitorredgreenorbluedrive)           | Imposta il valore dell'unità rossa, verde o blu di un monitor.                                    |
| [**SetMonitorRedGreenOrBlueGain**](/windows/desktop/api/HighLevelMonitorConfigurationAPI/nf-highlevelmonitorconfigurationapi-setmonitorredgreenorbluegain)             | Imposta un valore di guadagno rosso, verde o blu di un monitor.                                     |



 

## <a name="low-level-functions"></a>Funzioni Low-Level



| Funzione                                                                                   | Descrizione                                                                                                    |
|--------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------|
| [**CapabilitiesRequestAndCapabilitiesReply**](/windows/desktop/api/LowLevelMonitorConfigurationAPI/nf-lowlevelmonitorconfigurationapi-capabilitiesrequestandcapabilitiesreply) | Recupera una stringa che descrive le funzionalità di un monitoraggio.                                                        |
| [**GetCapabilitiesStringLength**](/windows/desktop/api/LowLevelMonitorConfigurationAPI/nf-lowlevelmonitorconfigurationapi-getcapabilitiesstringlength)                         | Recupera la lunghezza della stringa delle funzionalità di un monitoraggio.                                                       |
| [**GetTimingReport**](/windows/desktop/api/LowLevelMonitorConfigurationAPI/nf-lowlevelmonitorconfigurationapi-gettimingreport)                                                 | Recupera le frequenze di sincronizzazione orizzontale e verticale di un monitoraggio.                                     |
| [**GetVCPFeatureAndVCPFeatureReply**](/windows/desktop/api/LowLevelMonitorConfigurationAPI/nf-lowlevelmonitorconfigurationapi-getvcpfeatureandvcpfeaturereply)                 | Recupera il valore corrente, il valore massimo e il tipo di codice di un codice del pannello di controllo virtuale (VCP) per un monitoraggio. |
| [**SaveCurrentSettings**](/windows/desktop/api/LowLevelMonitorConfigurationAPI/nf-lowlevelmonitorconfigurationapi-savecurrentsettings)                                         | Salva le impostazioni di monitoraggio correnti nell'archiviazione non volatile dello schermo.                                       |
| [**SetVCPFeature**](/windows/desktop/api/LowLevelMonitorConfigurationAPI/nf-lowlevelmonitorconfigurationapi-setvcpfeature)                                                     | Imposta il valore di un codice del pannello di controllo virtuale (VCP) per un monitoraggio.                                            |



 

## <a name="enumeration-functions"></a>Funzioni di enumerazione



| Funzione                                                                                                   | Descrizione                                                                               |
|------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------|
| [**DestroyPhysicalMonitor**](/windows/desktop/api/PhysicalMonitorEnumerationAPI/nf-physicalmonitorenumerationapi-destroyphysicalmonitor)                                                   | Chiude un handle a un monitor fisico.                                                    |
| [**DestroyPhysicalMonitors**](/windows/desktop/api/PhysicalMonitorEnumerationAPI/nf-physicalmonitorenumerationapi-destroyphysicalmonitors)                                                 | Chiude una matrice di handle di monitoraggio fisici.                                              |
| [**GetNumberOfPhysicalMonitorsFromHMONITOR**](/windows/desktop/api/PhysicalMonitorEnumerationAPI/nf-physicalmonitorenumerationapi-getnumberofphysicalmonitorsfromhmonitor)                 | Recupera il numero di monitoraggi fisici associati a un handle di monitoraggio **HMONITOR** . |
| [**GetNumberOfPhysicalMonitorsFromIDirect3DDevice9**](/windows/desktop/api/PhysicalMonitorEnumerationAPI/nf-physicalmonitorenumerationapi-getnumberofphysicalmonitorsfromidirect3ddevice9) | Recupera il numero di monitoraggi fisici associati a un dispositivo Direct3D.              |
| [**GetPhysicalMonitorsFromHMONITOR**](/windows/desktop/api/PhysicalMonitorEnumerationAPI/nf-physicalmonitorenumerationapi-getphysicalmonitorsfromhmonitor)                                 | Recupera i monitoraggi fisici associati a un handle di monitoraggio **HMONITOR** .           |
| [**GetPhysicalMonitorsFromIDirect3DDevice9**](/windows/desktop/api/PhysicalMonitorEnumerationAPI/nf-physicalmonitorenumerationapi-getphysicalmonitorsfromidirect3ddevice9)                 | Recupera i monitoraggi fisici associati a un dispositivo Direct3D.                        |



 

## <a name="internal-functions"></a>Funzioni interne

Le funzioni seguenti vengono usate dall'API di configurazione del monitoraggio per accedere alle funzionalità nel driver di visualizzazione. Le applicazioni non devono chiamare queste funzioni.

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

[Riferimento alla configurazione del monitoraggio](monitor-configuration-reference.md)
</dt> </dl>

 

 




