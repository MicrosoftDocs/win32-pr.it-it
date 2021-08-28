---
description: In questa sezione viene descritta la programmazione multicast basata sullo stato finale tramite IOCTL anziché opzioni socket. Per una panoramica delle differenze tra la programmazione multicast basata sullo stato finale e la programmazione multicast basata su modifiche, vedere Programmazione multicast.
ms.assetid: 71c05393-3f8c-42c0-9060-e0df9b5e2578
title: Programmazione multicast basata sullo stato finale
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8ad31f0c840228e1fea729582f5e259ec92c4a04381752ed9ee50db2586b3b29
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119132514"
---
# <a name="final-state-based-multicast-programming"></a>Programmazione multicast basata sullo stato finale

In questa sezione viene descritta la programmazione multicast basata sullo stato finale tramite IOCTL anziché opzioni socket. Per una panoramica delle differenze tra la programmazione multicast basata sullo stato finale e la programmazione multicast basata su modifiche, vedere [Programmazione multicast.](multicast-programming.md)

Nella tabella seguente vengono descritti gli ioCCL Windows Sockets usati per la programmazione multicast Windows. 

| Ioctl                       | Tipo di argomento                                   |
|-----------------------------|-------------------------------------------------|
| SIOCSMSFILTER               | [**GROUP \_ Struttura FILTER**](/windows/desktop/api/Ws2ipdef/ns-ws2ipdef-group_filter) |
| SIOCGMSFILTER               | [**GROUP \_ Struttura FILTER**](/windows/desktop/api/Ws2ipdef/ns-ws2ipdef-group_filter) |
| SIO \_ GET \_ MULTICAST \_ FILTER | [**Struttura \_ ip msfilter**](/windows/desktop/api/Ws2ipdef/ns-ws2ipdef-ip_msfilter)   |
| SIO \_ SET \_ MULTICAST \_ FILTER | [**Struttura \_ ip msfilter**](/windows/desktop/api/Ws2ipdef/ns-ws2ipdef-ip_msfilter)   |



 

Si noti che **SIOCSMSFILTER** e **SIOCGMSFILTER** IOCTLS sono disponibili in Windows Vista e versioni successive.

L'uso di questi IOCL per la programmazione multicast offre vantaggi in termini di prestazioni quando si usano elenchi di origini di grandi dimensioni. Per altre informazioni sui parametri e sulle impostazioni associati all'uso di SIO GET MULTICAST FILTER o \_ \_ \_ SIO \_ SET \_ MULTICAST \_ FILTER, vedere la pagina di riferimento [**\_ GROUP FILTER.**](/windows/desktop/api/Ws2ipdef/ns-ws2ipdef-group_filter) Per altre informazioni sui parametri e sulle impostazioni associati all'uso di \_ SIO GET MULTICAST FILTER o SIO SET MULTICAST FILTER, vedere la pagina di riferimento \_ \_ di ip \_ \_ \_ [**\_ msfilter.**](/windows/desktop/api/Ws2ipdef/ns-ws2ipdef-ip_msfilter)

 

 



