---
description: Nella tabella seguente sono elencate le classi di evento per la risoluzione dei problemi generate dalle operazioni del provider consumer di eventi.
ms.assetid: dd685a41-8eae-4977-ab94-902dd8dddcc9
ms.tgt_platform: multiple
title: Classi di risoluzione dei problemi ConsumerProvider
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 536c23fb35ca6a4d2146cf87782768c51f37a6ea
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106315232"
---
# <a name="consumerprovider-troubleshooting-classes"></a>Classi di risoluzione dei problemi ConsumerProvider

Nella tabella seguente sono elencate le classi di evento per la risoluzione dei problemi generate dalle operazioni del [*provider consumer di eventi*](gloss-e.md) .

È possibile sottoscrivere le notifiche [**\_ ProviderEvent**](/previous-versions/windows/desktop/wmisystemprov/msft-wmiessevent) della classe base astratta MSFT per ottenere tutti gli eventi seguenti.



|                                                                                                 |                                                                                 |
|-------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------|
| [**MSFT \_ WmiProviderEvent**](/previous-versions/windows/desktop/wmisystemprov/msft-wmiproviderevent)                               | Classe padre per tutti gli eventi del provider di consumer.                                  |
| [**MSFT \_ WmiConsumerProviderLoaded**](/previous-versions/windows/desktop/wmisystemprov/msft-wmiconsumerproviderloaded)             | Definisce la riuscita dell'attivazione dell'oggetto COM del provider di consumer di eventi.    |
| [**MSFT \_ WmiConsumerProviderUnloaded**](/previous-versions/windows/desktop/wmisystemprov/msft-wmiconsumerproviderunloaded)         | Definisce la disattivazione riuscita dell'oggetto COM del provider consumer di eventi.  |
| [**MSFT \_ WmiConsumerProviderSinkLoaded**](/previous-versions/windows/desktop/wmisystemprov/msft-wmiconsumerprovidersinkloaded)     | Definisce la riuscita dell'attivazione dell'oggetto sink del provider consumer di eventi.   |
| [**MSFT \_ WmiConsumerProviderSinkUnloaded**](/previous-versions/windows/desktop/wmisystemprov/msft-wmiconsumerprovidersinkunloaded) | Definisce la disattivazione riuscita dell'oggetto sink del provider consumer di eventi. |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Risoluzione dei problemi WMI](wmi-troubleshooting.md)
</dt> <dt>

Risoluzione dei problemi di WMI
</dt> <dt>

[Ricezione di un evento WMI](receiving-a-wmi-event.md)
</dt> </dl>

 

 
