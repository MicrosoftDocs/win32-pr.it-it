---
description: WMI fornisce un set di classi di risoluzione dei problemi che possono essere usate da script e applicazioni per ottenere informazioni sullo stato interno WMI durante le operazioni di base e del provider WMI.
ms.assetid: 631e0cce-0e83-42e5-a381-e96b1f70d6f9
ms.tgt_platform: multiple
title: Classi per la risoluzione dei problemi WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f9d3c5f1d40cd5da9e61ff289fc0b137ec7613ec8156fb0acc4f225e793a8407
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119049859"
---
# <a name="wmi-troubleshooting-classes"></a>Classi per la risoluzione dei problemi WMI

WMI fornisce un set di classi di risoluzione dei problemi che possono essere usate da script e applicazioni per ottenere informazioni sullo stato interno WMI durante le operazioni di base e del provider WMI. Per altre informazioni sulla risoluzione dei problemi WMI, vedere [Wmi Troubleshooting](wmi-troubleshooting.md) and Provider Configuration and [Troubleshooting Classes](provider-configuration-and-troubleshooting-classes.md).

WMI include diverse classi di risoluzione dei problemi di base per le operazioni di base e del provider WMI:

-   [**Contatori \_ WmiProvider \_ MSFT**](/previous-versions/windows/desktop/wmisystemprov/msft-wmiprovider-counters)

    In ogni sistema di computer è presente solo una di queste classi. Fornisce conteggi di vari tipi di operazioni del provider in tale sistema.

-   [**MSFT \_ WmiSelfEvent**](/previous-versions/windows/desktop/wmisystemprov/msft-wmiselfevent)

    Le classi di risoluzione dei problemi degli eventi derivano [**da \_ WMISelfEvent MSFT.**](/previous-versions/windows/desktop/wmisystemprov/msft-wmiselfevent) Le query di questa classe restituiscono istanze di classi di evento come [**MSFT \_ WmiThreadPoolCreated**](/previous-versions/windows/desktop/wmisystemprov/msft-wmithreadpoolcreated) o [**MSFT \_ WmiProvider \_ CreateInstanceEnumAsyncEvent \_ Post.**](/previous-versions/windows/desktop/wmisystemprov/msft-wmiprovider-createinstanceenumasyncevent-post)

    L'elenco seguente include collegamenti a diverse categorie di classi di eventi derivate da [**\_ WMISelfEvent MSFT:**](/previous-versions/windows/desktop/wmisystemprov/msft-wmiselfevent)

    -   [Classi di risoluzione dei problemi degli eventi del provider](provider-event-troubleshooting-classes.md)
    -   [Classi consumerprovider per la risoluzione dei problemi](consumerprovider-troubleshooting-classes.md)
    -   [Classi di risoluzione dei problemi degli eventi del servizio WMI](wmi-service-event-troubleshooting-classes.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Risoluzione dei problemi di WMI](wmi-troubleshooting.md)
</dt> <dt>

[Ricezione di un evento WMI](receiving-a-wmi-event.md)
</dt> </dl>

 

 
