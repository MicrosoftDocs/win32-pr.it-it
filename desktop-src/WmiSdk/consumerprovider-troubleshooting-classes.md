---
description: Nella tabella seguente sono elencate le classi di evento per la risoluzione dei problemi generate dalle operazioni del provider di consumer di eventi.
ms.assetid: dd685a41-8eae-4977-ab94-902dd8dddcc9
ms.tgt_platform: multiple
title: Classi per la risoluzione dei problemi di ConsumerProvider
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 740b8c0eb1884181fa84efe26e0611dda4b1712f
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/04/2021
ms.locfileid: "111443612"
---
# <a name="consumerprovider-troubleshooting-classes"></a>Classi per la risoluzione dei problemi di ConsumerProvider

Nella tabella seguente sono elencate le classi di evento per la risoluzione dei problemi generate dalle [*operazioni del provider di consumer di*](gloss-e.md) eventi.

È possibile sottoscrivere le notifiche [**MSFT \_ ProviderEvent della**](/previous-versions/windows/desktop/wmisystemprov/msft-wmiessevent) classe di base astratta per ottenere tutti gli eventi seguenti.



| Event                                                                                                | Descrizione                                                                                |
|-------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------|
| [**MSFT \_ WmiProviderEvent**](/previous-versions/windows/desktop/wmisystemprov/msft-wmiproviderevent)                               | Classe padre per tutti gli eventi del provider di consumer.                                  |
| [**MSFT \_ WmiConsumerProviderLoaded**](/previous-versions/windows/desktop/wmisystemprov/msft-wmiconsumerproviderloaded)             | Definisce l'attivazione corretta dell'oggetto COM del provider di consumer di eventi.    |
| [**MSFT \_ WmiConsumerProviderUnloaded**](/previous-versions/windows/desktop/wmisystemprov/msft-wmiconsumerproviderunloaded)         | Definisce la disattivazione corretta dell'oggetto COM del provider di consumer di eventi.  |
| [**MSFT \_ WmiConsumerProviderSinkLoaded**](/previous-versions/windows/desktop/wmisystemprov/msft-wmiconsumerprovidersinkloaded)     | Definisce l'attivazione riuscita dell'oggetto sink del provider di consumer di eventi.   |
| [**MSFT \_ WmiConsumerProviderSinkUnloaded**](/previous-versions/windows/desktop/wmisystemprov/msft-wmiconsumerprovidersinkunloaded) | Definisce la disattivazione riuscita dell'oggetto sink del provider del consumer di eventi. |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Risoluzione dei problemi wmi](wmi-troubleshooting.md)
</dt> <dt>

Risoluzione dei problemi di WMI
</dt> <dt>

[Ricezione di un evento WMI](receiving-a-wmi-event.md)
</dt> </dl>

 

 
