---
title: Uso delle funzioni High-Level monitoraggio
description: Uso delle funzioni High-Level monitoraggio
ms.assetid: 23e5d45d-a924-4119-b21d-b24764b53a94
keywords:
- monitor,funzioni
- monitoraggio, funzioni di configurazione di alto livello
- monitoraggio, enumerazione di monitoraggi fisici
- monitoraggio, impostazioni continue
- monitorare la configurazione, funzioni di configurazione di alto livello
- monitorare la configurazione, funzioni
- configurazione del monitoraggio, enumerazione dei monitoraggi fisici
- monitorare la configurazione, impostazioni continue
- enumerazione di monitoraggi fisici
- funzioni di configurazione di alto livello
- impostazioni di monitoraggio continuo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 827d19ef0006dc89208061c18ef34c28c8f993c3e0d6ebd0d1c1005daf2cd640
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119066601"
---
# <a name="using-the-high-level-monitor-configuration-functions"></a>Uso delle funzioni High-Level monitoraggio

## <a name="enumerating-physical-monitors"></a>Enumerazione dei monitoraggi fisici

Esistono diverse funzioni che enumerano i dispositivi di visualizzazione, [**tra cui EnumDisplayMonitors**](/windows/desktop/api/winuser/nf-winuser-enumdisplaymonitors) [**e MonitorFromWindow**](/windows/desktop/api/winuser/nf-winuser-monitorfromwindow). Queste funzioni sono documentate nella documentazione Windows GDI, nell'argomento [Multiple Display Monitors](/windows/desktop/gdi/multiple-display-monitors). Queste funzioni restituiscono **handle HMONITOR.** Nonostante il nome, tuttavia, un handle **HMONITOR** può essere associato a più monitor fisici. Per configurare le impostazioni in un monitoraggio, l'applicazione deve ottenere un handle univoco per il monitoraggio fisico chiamando [**GetPhysicalMonitorsFromHMONITOR**](/windows/desktop/api/PhysicalMonitorEnumerationAPI/nf-physicalmonitorenumerationapi-getphysicalmonitorsfromhmonitor).

Se l'applicazione usa Direct3D, è possibile ottenere un handle di monitoraggio da un dispositivo Direct3D chiamando [**GetPhysicalMonitorsFromIDirect3DDevice9.**](/windows/desktop/api/PhysicalMonitorEnumerationAPI/nf-physicalmonitorenumerationapi-getphysicalmonitorsfromidirect3ddevice9)

## <a name="supported-functions"></a>Funzioni supportate

Un monitoraggio potrebbe non supportare tutte le funzioni di configurazione del monitoraggio. Per individuare le funzioni supportate da un monitoraggio, chiamare [**GetMonitorCapabilities**](/windows/desktop/api/HighLevelMonitorConfigurationAPI/nf-highlevelmonitorconfigurationapi-getmonitorcapabilities).

## <a name="continuous-monitor-settings"></a>Monitoraggio continuo Impostazioni

*Un'impostazione* di monitoraggio continuo è un'impostazione che può variare tra un valore minimo e un valore massimo. La maggior parte delle funzioni di configurazione di monitoraggio di alto livello controlla le impostazioni di monitoraggio continuo. Ad esempio, luminosità e contrasto sono impostazioni continue.

Le impostazioni di monitoraggio continuo non hanno unità reali definite. Le unità sono arbitrarie e possono variare da un produttore a un altro. Se due monitor hanno lo stesso valore di luminosità, ad esempio, un monitor potrebbe avere un aspetto molto più chiaro rispetto a un altro. In genere, un'applicazione presenterà controlli dispositivo di scorrimento o controlli verso l'alto all'utente. L'utente può quindi modificare le impostazioni per offrire la migliore qualità soggettiva.

## <a name="changes-in-monitor-state"></a>Modifiche dello stato del monitoraggio

Un monitoraggio può modificare gli stati per vari motivi, tra cui:

-   L'utente modifica le impostazioni con i controlli del pannello anteriore del monitor.
-   L'utente modifica la risoluzione dello schermo, la frequenza di aggiornamento o la profondità in bit del monitor.
-   L'applicazione usa le funzioni di monitoraggio di basso livello per modificare un'impostazione non accessibile dalle funzioni di alto livello.
-   L'applicazione chiama [**RestoreMonitorFactoryColorDefaults**](/windows/desktop/api/HighLevelMonitorConfigurationAPI/nf-highlevelmonitorconfigurationapi-restoremonitorfactorycolordefaults) [**o RestoreMonitorFactoryDefaults**](/windows/desktop/api/HighLevelMonitorConfigurationAPI/nf-highlevelmonitorconfigurationapi-restoremonitorfactorydefaults).

Tutti questi eventi possono modificare le impostazioni del monitoraggio. Possono anche modificare il valore minimo e massimo di un'impostazione.

## <a name="dependencies-among-monitor-settings"></a>Dipendenze tra le Impostazioni

La modifica della temperatura del colore può modificare le impostazioni correnti dell'unità e del guadagno e anche il contrario è vero. Queste sono le uniche dipendenze tra le funzioni di configurazione di monitoraggio di alto livello. Altre impostazioni potrebbero essere accessibili solo tramite le funzioni di monitoraggio di basso livello. Potrebbero esserci dipendenze tra queste impostazioni e le impostazioni di alto livello. Queste dipendenze sono specifiche del fornitore. Un'applicazione può gestire questo problema in diversi modi:

-   Usare solo funzioni di alto livello.
-   Dopo aver chiamato una funzione di basso livello, ottenere il valore corrente di ogni impostazione del monitoraggio. Sfortunatamente, questo approccio può essere lento, perché per ottenere ogni impostazione sono necessari circa 40 millisecondi.
-   Usare funzioni di basso livello solo con modelli di monitoraggio specifici il cui comportamento è comprensibile.

## <a name="disabled-monitor-settings"></a>Disabled Monitor Impostazioni

Un'applicazione non può disabilitare le impostazioni di monitoraggio chiamando le funzioni di monitoraggio di alto livello. Tuttavia, un'applicazione potrebbe disabilitare accidentalmente un'impostazione se usa le funzioni di basso livello per modificare un'impostazione di monitoraggio non supportata dalle funzioni di alto livello. Inoltre, un utente potrebbe disabilitare un'impostazione usando il controllo pannello anteriore. Questi comportamenti sono specifici del fornitore.

Se un'impostazione di monitoraggio viene disabilitata, qualsiasi funzione che imposta o recupera tale impostazione avrà esito negativo e imposta il codice dell'ultimo errore su ERROR \_ DISABLED \_ MONITOR \_ SETTING. In questo caso, l'applicazione può eseguire una delle operazioni seguenti:

-   Visualizzare un messaggio di errore e suggerire all'utente di provare a modificare l'impostazione usando il controllo del pannello anteriore.
-   Chiamare la [**funzione RestoreMonitorFactoryDefaults.**](/windows/desktop/api/HighLevelMonitorConfigurationAPI/nf-highlevelmonitorconfigurationapi-restoremonitorfactorydefaults) Se un monitoraggio ha il flag di funzionalità MC \_ RESTORE \_ FACTORY DEFAULTS ENABLES MONITOR SETTINGS, questa funzione abilita tutte le impostazioni di monitoraggio supportate dalle funzioni \_ di monitoraggio di alto \_ \_ \_ livello. Sfortunatamente, la funzione reimposta anche le impostazioni di monitoraggio sul valore predefinito di fabbrica.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Uso della configurazione del monitoraggio](using-monitor-configuration.md)
</dt> </dl>

 

 