---
description: Uso \_ \_ del codice del comando per ambito multicast Sio per specificare l'ambito in cui deve essere eseguito il multicast.
ms.assetid: 3acec987-9cb4-446c-af6e-ea0e6a96e70c
title: IOCTL SIO_MULTICAST_SCOPE
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 90d1fd6f2bea76d095ea88d66c0ac029fb9168ac
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106315779"
---
# <a name="sio_multicast_scope-ioctl"></a>\_ \_ IOCTL ambito multicast sio

Quando viene utilizzato il multicast, in genere è necessario specificare l'ambito sul quale deve essere eseguito il multicast. Questo ambito è definito come il numero di segmenti di rete indirizzati da coprire. Il \_ codice del \_ comando per l'ambito multicast Sio per [**WSPIoctl**](/previous-versions/windows/hardware/network/ff566296(v=vs.85)) viene usato per controllare questa operazione. Un ambito pari a zero indicherà che la trasmissione multicast non verrà distribuita in transito, ma potrebbe essere divulgata tra i socket all'interno dell'host locale. Un valore di ambito pari a uno (impostazione predefinita) indica che la trasmissione verrà posizionata in transito, ma non incrocierà alcun router. I valori di ambito più elevati determinano il numero di router che possono essere superati. Si noti che corrisponde al parametro time-to-Live (TTL) in multicast IP.

 

 
