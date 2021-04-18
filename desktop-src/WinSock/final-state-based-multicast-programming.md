---
description: Questa sezione descrive la programmazione multicast basata sullo stato finale usando IOCTLs anziché le opzioni socket. Per una panoramica del modo in cui la programmazione multicast basata sullo stato finale è diversa dalla programmazione multicast basata sulle modifiche, vedere programmazione multicast.
ms.assetid: 71c05393-3f8c-42c0-9060-e0df9b5e2578
title: Programmazione multicast basata sullo stato finale
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6abfebfc7efe27f1c5a6d63312c376bd659dce57
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106306983"
---
# <a name="final-state-based-multicast-programming"></a>Programmazione multicast basata sullo stato finale

Questa sezione descrive la programmazione multicast basata sullo stato finale usando IOCTLs anziché le opzioni socket. Per una panoramica del modo in cui la programmazione multicast basata sullo stato finale è diversa dalla programmazione multicast basata sulle modifiche, vedere [programmazione multicast](multicast-programming.md).

La tabella seguente descrive i IOCTL Windows Sockets usati per la programmazione multicast in Windows. 

| IOCTL                       | Tipo di argomento                                   |
|-----------------------------|-------------------------------------------------|
| SIOCSMSFILTER               | [**Gruppo \_ di Struttura filtro**](/windows/desktop/api/Ws2ipdef/ns-ws2ipdef-group_filter) |
| SIOCGMSFILTER               | [**Gruppo \_ di Struttura filtro**](/windows/desktop/api/Ws2ipdef/ns-ws2ipdef-group_filter) |
| \_ \_ filtro multicast sio \_ Get | [**struttura \_ msfilter IP**](/windows/desktop/api/Ws2ipdef/ns-ws2ipdef-ip_msfilter)   |
| \_ \_ filtro multicast set \_ sio | [**struttura \_ msfilter IP**](/windows/desktop/api/Ws2ipdef/ns-ws2ipdef-ip_msfilter)   |



 

Si noti che le IOCTL **SIOCSMSFILTER** e **SIOCGMSFILTER** sono disponibili in Windows Vista e versioni successive.

L'uso di questi IOCTL per la programmazione multicast offre vantaggi in merito alle prestazioni quando si utilizzano elenchi di origine di grandi dimensioni. Per altre informazioni sui parametri e le impostazioni associati all'uso di SIO \_ get \_ multicast \_ Filter o SIO \_ set \_ multicast \_ Filter, vedere la pagina di riferimento del [**\_ filtro di gruppo**](/windows/desktop/api/Ws2ipdef/ns-ws2ipdef-group_filter) . Per altre informazioni sui parametri e le impostazioni associati all'uso di SIO \_ get \_ multicast \_ Filter o SIO \_ set \_ multicast \_ Filter, vedere la pagina di riferimento [**\_ msfilter IP**](/windows/desktop/api/Ws2ipdef/ns-ws2ipdef-ip_msfilter) .

 

 



