---
description: Le classi di risoluzione dei problemi degli eventi del servizio WMI vengono generate da eventi all'interno del servizio WMI, ad esempio la creazione di pool di thread.
ms.assetid: 1a1251c8-a2f7-47ac-9db1-d780d7d272f0
ms.tgt_platform: multiple
title: Classi di risoluzione dei problemi degli eventi del servizio WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4e811ac5b276e5562f73b5b432d5f3255af5bab7
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/04/2021
ms.locfileid: "111443062"
---
# <a name="wmi-service-event-troubleshooting-classes"></a>Classi di risoluzione dei problemi degli eventi del servizio WMI

Le classi di risoluzione dei problemi degli eventi del servizio WMI vengono generate da eventi all'interno del servizio WMI, ad esempio la creazione di pool di thread.

È possibile sottoscrivere le notifiche [**MSFT \_ WmiEssEvent**](/previous-versions/windows/desktop/wmisystemprov/msft-wmiessevent) della classe di base astratta per ottenere tutti gli eventi derivati elencati nella tabella seguente.



|   Event                                                                                        |   Descrizione                                                                                             |
|-------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------|
| [**MSFT \_ WmiEssEvent**](/previous-versions/windows/desktop/wmisystemprov/msft-wmiessevent)                                   | Classe padre per tutti gli eventi Strumentazione gestione Windows (WMI) Eventing SubSystem (ESS). |
| [**MSFT \_ WmiRegisterNotificationEvent**](/previous-versions/windows/desktop/wmisystemprov/msft-wmiregisternotificationevent) | Rappresenta la creazione di un sink di evento per la notifica per una query di eventi.                       |
| [**MSFT \_ WmiCancelNotificationSink**](/previous-versions/windows/desktop/wmisystemprov/msft-wmicancelnotificationsink)       | generato quando un sink di evento viene annullato.                                                           |
| [**MSFT \_ WmiThreadPoolEvent**](/previous-versions/windows/desktop/wmisystemprov/msft-wmithreadpoolevent)                     | fornisce la notifica degli eventi del thread nel sistema ESS (Event Sub System) WMI.                           |
| [**MSFT \_ WmiThreadPoolCreated**](/previous-versions/windows/desktop/wmisystemprov/msft-wmithreadpoolcreated)                 | Fornisce una notifica quando viene creato un thread nel sistema ESS (Event Sub System) WMI.                   |
| [**MSFT \_ WmiThreadPoolDeleted**](/previous-versions/windows/desktop/wmisystemprov/msft-wmithreadpooldeleted)                 | Fornisce una notifica quando un thread viene eliminato nel sistema ESS (Event Sub System) WMI.                   |
| [**MSFT \_ WmiFilterEvent**](/previous-versions/windows/desktop/wmisystemprov/msft-wmifilterevent)                             | Classe padre per tutti gli eventi di filtro del consumer di eventi permanenti.                                        |
| [**MSFT \_ WmiFilterActivated**](/previous-versions/windows/desktop/wmisystemprov/msft-wmifilteractivated)                     | Definisce l'attivazione corretta di un filtro di sottoscrizione del consumer di eventi permanente.                |
| [**MSFT \_ WmiFilterDeactivated**](/previous-versions/windows/desktop/wmisystemprov/msft-wmifilterdeactivated)                 | Definisce la disattivazione corretta di un filtro di sottoscrizione consumer permanente.                    |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Risoluzione dei problemi di WMI](wmi-troubleshooting.md)
</dt> <dt>

Risoluzione dei problemi di WMI
</dt> <dt>

[Monitoraggio degli eventi](monitoring-events.md)
</dt> <dt>

[Ricezione di un evento WMI](receiving-a-wmi-event.md)
</dt> </dl>

 

 
