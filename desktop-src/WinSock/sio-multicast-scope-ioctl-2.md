---
description: Utilizzo del codice di \_ comando SIO MULTICAST \_ SCOPE per specificare l'ambito in cui deve verificarsi il multicast.
ms.assetid: 3acec987-9cb4-446c-af6e-ea0e6a96e70c
title: SIO_MULTICAST_SCOPE Ioctl
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1be65ee600b680805177a44125c03e65e49364ae9008d306349da8f60f9d9de8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118559689"
---
# <a name="sio_multicast_scope-ioctl"></a>SIO \_ MULTICAST \_ SCOPE Ioctl

Quando si utilizza il multicast, è in genere necessario specificare l'ambito in cui deve verificarsi il multicast. In questo caso l'ambito è definito come il numero di segmenti di rete instradati da coprire. A tale scopo, viene usato il codice di comando \_ SIO MULTICAST SCOPE per \_ [**WSPIoctl.**](/previous-versions/windows/hardware/network/ff566296(v=vs.85)) Un ambito pari a zero indica che la trasmissione multicast non verrebbe posizionata in transito, ma potrebbe essere inserita tra i socket all'interno dell'host locale. Un valore di ambito pari a uno (impostazione predefinita) indica che la trasmissione verrà posizionata in transito, ma non attraversa alcun router. I valori di ambito più elevati determinano il numero di router che possono essere attraversati. Si noti che corrisponde al parametro TTL (Time-to-Live) nel multicasting IP.

 

 
