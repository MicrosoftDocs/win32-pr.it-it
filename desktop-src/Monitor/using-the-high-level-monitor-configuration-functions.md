---
title: Uso delle funzioni di configurazione di monitoraggio High-Level
description: Uso delle funzioni di configurazione di monitoraggio High-Level
ms.assetid: 23e5d45d-a924-4119-b21d-b24764b53a94
keywords:
- monitoraggio, funzioni
- monitoraggio, funzioni di configurazione di alto livello
- monitoraggio, enumerazione dei monitoraggi fisici
- monitoraggio, impostazioni continue
- configurazione del monitoraggio, funzioni di configurazione di alto livello
- configurazione del monitoraggio, funzioni
- monitoraggio della configurazione, enumerazione dei monitoraggi fisici
- configurazione del monitoraggio, impostazioni continue
- Enumerazione dei monitoraggi fisici
- funzioni di configurazione di alto livello
- impostazioni di monitoraggio continuo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ff494388aac91d8aacd92ed4fe345722ea18659f
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "106299728"
---
# <a name="using-the-high-level-monitor-configuration-functions"></a>Uso delle funzioni di configurazione di monitoraggio High-Level

## <a name="enumerating-physical-monitors"></a>Enumerazione dei monitoraggi fisici

Sono disponibili diverse funzioni che enumerano i dispositivi di visualizzazione, inclusi [**EnumDisplayMonitors**](/windows/desktop/api/winuser/nf-winuser-enumdisplaymonitors) e [**MonitorFromWindow**](/windows/desktop/api/winuser/nf-winuser-monitorfromwindow). Queste funzioni sono documentate nella documentazione di Windows GDI, nell'argomento [monitoraggi per più](/windows/desktop/gdi/multiple-display-monitors)schermi. Queste funzioni restituiscono handle **HMONITOR** . Nonostante il nome, tuttavia, un handle **HMONITOR** può essere associato a più di un monitor fisico. Per configurare le impostazioni in un monitoraggio, l'applicazione deve ottenere un handle univoco per il monitoraggio fisico chiamando [**GetPhysicalMonitorsFromHMONITOR**](/windows/desktop/api/PhysicalMonitorEnumerationAPI/nf-physicalmonitorenumerationapi-getphysicalmonitorsfromhmonitor).

Se l'applicazione usa Direct3D, è possibile ottenere un handle di monitoraggio da un dispositivo Direct3D chiamando [**GetPhysicalMonitorsFromIDirect3DDevice9**](/windows/desktop/api/PhysicalMonitorEnumerationAPI/nf-physicalmonitorenumerationapi-getphysicalmonitorsfromidirect3ddevice9).

## <a name="supported-functions"></a>Funzioni supportate

Un monitoraggio potrebbe non supportare tutte le funzioni di configurazione del monitoraggio. Per individuare le funzioni supportate da un monitoraggio, chiamare [**GetMonitorCapabilities**](/windows/desktop/api/HighLevelMonitorConfigurationAPI/nf-highlevelmonitorconfigurationapi-getmonitorcapabilities).

## <a name="continuous-monitor-settings"></a>Impostazioni di monitoraggio continuo

Un'impostazione di monitoraggio *continuo* è una che può variare tra un valore minimo e un valore massimo. La maggior parte delle funzioni di configurazione di monitoraggio di alto livello controlla le impostazioni di monitoraggio continuo. Ad esempio, luminosità e contrasto sono impostazioni continue.

Le impostazioni di monitoraggio continuo non dispongono di unità reali definite. Le unità sono arbitrarie e possono variare da un produttore a un altro. Se due monitoraggi hanno lo stesso valore di luminosità, ad esempio, un monitoraggio potrebbe sembrare molto più luminoso di un altro. In genere, un'applicazione consentirà all'utente di visualizzare i controlli di scorrimento o di scorrimento. L'utente può quindi modificare le impostazioni per fornire la migliore qualità soggettiva.

## <a name="changes-in-monitor-state"></a>Modifiche allo stato di monitoraggio

Un monitoraggio può modificare gli Stati per vari motivi, tra cui:

-   L'utente modifica le impostazioni con i controlli Front-Panel del monitoraggio.
-   L'utente modifica la risoluzione dello schermo, la frequenza di aggiornamento o la profondità dei bit del monitoraggio.
-   L'applicazione utilizza le funzioni di monitoraggio di basso livello per modificare un'impostazione non accessibile dalle funzioni di alto livello.
-   L'applicazione chiama [**RestoreMonitorFactoryColorDefaults**](/windows/desktop/api/HighLevelMonitorConfigurationAPI/nf-highlevelmonitorconfigurationapi-restoremonitorfactorycolordefaults) o [**RestoreMonitorFactoryDefaults**](/windows/desktop/api/HighLevelMonitorConfigurationAPI/nf-highlevelmonitorconfigurationapi-restoremonitorfactorydefaults).

Tutti questi eventi possono modificare le impostazioni di monitoraggio. Possono anche modificare il valore minimo e massimo di un'impostazione.

## <a name="dependencies-among-monitor-settings"></a>Dipendenze tra le impostazioni di monitoraggio

La modifica della temperatura del colore può modificare l'unità corrente e ottenere le impostazioni e anche il contrario è true. Queste sono le uniche dipendenze tra le funzioni di configurazione di monitoraggio di alto livello. Altre impostazioni potrebbero essere accessibili solo tramite le funzioni di monitoraggio di basso livello. Potrebbero esserci dipendenze tra queste impostazioni e le impostazioni di alto livello. Queste dipendenze sono specifiche del fornitore. Un'applicazione può gestire questo problema in diversi modi:

-   Usare solo funzioni di alto livello.
-   Dopo la chiamata a una funzione di basso livello, ottenere il valore corrente di ogni impostazione di monitoraggio. Sfortunatamente, questo approccio può essere lento, perché il recupero di ogni impostazione richiede circa 40 millisecondi.
-   Usare le funzioni di basso livello solo con modelli di monitoraggio specifici il cui comportamento è compreso.

## <a name="disabled-monitor-settings"></a>Impostazioni di monitoraggio disabilitate

Un'applicazione non può disabilitare le impostazioni di monitoraggio chiamando le funzioni di monitoraggio di alto livello. Tuttavia, un'applicazione potrebbe disabilitare accidentalmente un'impostazione se utilizza le funzioni di basso livello per modificare un'impostazione di monitoraggio non supportata dalle funzioni di alto livello. Inoltre, un utente potrebbe disabilitare un'impostazione usando il controllo Front-Panel. Questi comportamenti sono specifici del fornitore.

Se un'impostazione di monitoraggio viene disabilitata, qualsiasi funzione che imposta o recupera l'impostazione avrà esito negativo e imposterà l'impostazione del monitoraggio last-error code to ERROR \_ disabled \_ \_ . Quando si verifica questa situazione, l'applicazione può eseguire una delle operazioni seguenti:

-   Visualizzare un messaggio di errore e suggerire all'utente di provare a modificare l'impostazione usando il controllo Front-Panel.
-   Chiamare la funzione [**RestoreMonitorFactoryDefaults**](/windows/desktop/api/HighLevelMonitorConfigurationAPI/nf-highlevelmonitorconfigurationapi-restoremonitorfactorydefaults) . Se per un monitoraggio sono disponibili le impostazioni \_ predefinite MC Restore \_ \_ \_ , Abilita il \_ \_ flag impostazioni di monitoraggio funzionalità, questa funzione Abilita tutte le impostazioni di monitoraggio supportate dalle funzioni di monitoraggio di alto livello. Sfortunatamente, la funzione Reimposta anche le impostazioni predefinite del monitoraggio.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Uso della configurazione di monitoraggio](using-monitor-configuration.md)
</dt> </dl>

 

 