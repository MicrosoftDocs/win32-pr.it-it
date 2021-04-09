---
description: WMI fornisce un set di classi di risoluzione dei problemi che gli script e le applicazioni possono utilizzare per ottenere informazioni sullo stato interno WMI durante le operazioni di base e del provider WMI.
ms.assetid: 631e0cce-0e83-42e5-a381-e96b1f70d6f9
ms.tgt_platform: multiple
title: Classi di risoluzione dei problemi WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 65b3972ba59c80a1495916ab24a72f6e93bef8e6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103968547"
---
# <a name="wmi-troubleshooting-classes"></a>Classi di risoluzione dei problemi WMI

WMI fornisce un set di classi di risoluzione dei problemi che gli script e le applicazioni possono utilizzare per ottenere informazioni sullo stato interno WMI durante le operazioni di base e del provider WMI. Per ulteriori informazioni sulla risoluzione dei problemi relativi a WMI, vedere la pagina relativa alla risoluzione dei problemi e alle [classi](provider-configuration-and-troubleshooting-classes.md)di risoluzione dei problemi di [WMI](wmi-troubleshooting.md) .

WMI include diverse classi di risoluzione dei problemi di base per le operazioni di base e del provider WMI:

-   [**\_Contatori provider WMI \_ MSFT**](/previous-versions/windows/desktop/wmisystemprov/msft-wmiprovider-counters)

    In ogni computer viene individuata solo una di queste classi. Fornisce i conteggi di diversi tipi di operazioni del provider nel sistema.

-   [**MSFT \_ WmiSelfEvent**](/previous-versions/windows/desktop/wmisystemprov/msft-wmiselfevent)

    Le classi di risoluzione dei problemi degli eventi derivano da [**MSFT \_ WmiSelfEvent**](/previous-versions/windows/desktop/wmisystemprov/msft-wmiselfevent). Le query di questa classe restituiscono istanze delle classi di evento, ad esempio [**MSFT \_ WmiThreadPoolCreated**](/previous-versions/windows/desktop/wmisystemprov/msft-wmithreadpoolcreated) o [**MSFT \_ provider WMI \_ CreateInstanceEnumAsyncEvent \_ post**](/previous-versions/windows/desktop/wmisystemprov/msft-wmiprovider-createinstanceenumasyncevent-post).

    Nell'elenco seguente vengono forniti i collegamenti a diverse categorie di classi di evento derivate da [**MSFT \_ WmiSelfEvent**](/previous-versions/windows/desktop/wmisystemprov/msft-wmiselfevent):

    -   [Classi di risoluzione dei problemi degli eventi del provider](provider-event-troubleshooting-classes.md)
    -   [Classi di risoluzione dei problemi ConsumerProvider](consumerprovider-troubleshooting-classes.md)
    -   [Classi di risoluzione dei problemi degli eventi del servizio WMI](wmi-service-event-troubleshooting-classes.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Risoluzione dei problemi WMI](wmi-troubleshooting.md)
</dt> <dt>

[Ricezione di un evento WMI](receiving-a-wmi-event.md)
</dt> </dl>

 

 
