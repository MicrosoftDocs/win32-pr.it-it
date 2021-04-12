---
description: Le classi di risoluzione dei problemi degli eventi del servizio WMI sono generate da eventi all'interno del servizio WMI, ad esempio la creazione di pool di thread.
ms.assetid: 1a1251c8-a2f7-47ac-9db1-d780d7d272f0
ms.tgt_platform: multiple
title: Classi di risoluzione dei problemi degli eventi del servizio WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bbf3728b6ae150a948fdf71515e27f17ca7280f5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104233668"
---
# <a name="wmi-service-event-troubleshooting-classes"></a>Classi di risoluzione dei problemi degli eventi del servizio WMI

Le classi di risoluzione dei problemi degli eventi del servizio WMI sono generate da eventi all'interno del servizio WMI, ad esempio la creazione di pool di thread.

È possibile sottoscrivere le notifiche [**\_ WmiEssEvent**](/previous-versions/windows/desktop/wmisystemprov/msft-wmiessevent) della classe base astratta MSFT per ottenere tutti gli eventi derivati elencati nella tabella seguente.



|                                                                                           |                                                                                                     |
|-------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------|
| [**MSFT \_ WmiEssEvent**](/previous-versions/windows/desktop/wmisystemprov/msft-wmiessevent)                                   | Classe padre per tutti gli eventi del sottosistema di gestione degli eventi (SSE) di Strumentazione gestione Windows (WMI). |
| [**MSFT \_ WmiRegisterNotificationEvent**](/previous-versions/windows/desktop/wmisystemprov/msft-wmiregisternotificationevent) | Rappresenta la creazione di un sink di evento per la notifica per una query di eventi.                       |
| [**MSFT \_ WmiCancelNotificationSink**](/previous-versions/windows/desktop/wmisystemprov/msft-wmicancelnotificationsink)       | generato quando viene annullato un sink di evento.                                                           |
| [**MSFT \_ WmiThreadPoolEvent**](/previous-versions/windows/desktop/wmisystemprov/msft-wmithreadpoolevent)                     | fornisce la notifica di eventi del thread nel sistema di eventi WMI (ESS).                           |
| [**MSFT \_ WmiThreadPoolCreated**](/previous-versions/windows/desktop/wmisystemprov/msft-wmithreadpoolcreated)                 | Fornisce una notifica quando un thread viene creato nel sistema di eventi WMI (SSE).                   |
| [**MSFT \_ WmiThreadPoolDeleted**](/previous-versions/windows/desktop/wmisystemprov/msft-wmithreadpooldeleted)                 | Fornisce una notifica quando un thread viene eliminato nel sistema di eventi WMI (SSE).                   |
| [**MSFT \_ WmiFilterEvent**](/previous-versions/windows/desktop/wmisystemprov/msft-wmifilterevent)                             | Classe padre per tutti gli eventi di filtro del consumer di eventi permanenti.                                        |
| [**MSFT \_ WmiFilterActivated**](/previous-versions/windows/desktop/wmisystemprov/msft-wmifilteractivated)                     | Definisce la riuscita dell'attivazione di un filtro di sottoscrizione di un consumer di eventi permanente.                |
| [**MSFT \_ WmiFilterDeactivated**](/previous-versions/windows/desktop/wmisystemprov/msft-wmifilterdeactivated)                 | Definisce la corretta disattivazione di un filtro di sottoscrizione permanente del consumer.                    |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Risoluzione dei problemi WMI](wmi-troubleshooting.md)
</dt> <dt>

Risoluzione dei problemi di WMI
</dt> <dt>

[Monitoraggio degli eventi](monitoring-events.md)
</dt> <dt>

[Ricezione di un evento WMI](receiving-a-wmi-event.md)
</dt> </dl>

 

 
