---
description: Quando si utilizza il multicast, è in genere necessario specificare l'ambito in cui deve verificarsi il multicast.
ms.assetid: 744b43a8-dd89-4e63-ae3c-5bee72864df7
title: SIO_MULTICAST_SCOPE di comando per WSAIoctl
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c38269167aa2ed142440b0e1105600d26c59514f72d749595ce44ecdf3a0998f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117927370"
---
# <a name="sio_multicast_scope-command-code-for-wsaioctl"></a>Codice di \_ comando SIO MULTICAST \_ SCOPE per WSAIoctl

Quando si utilizza il multicast, è in genere necessario specificare *l'ambito* in cui deve verificarsi il multicast. L'ambito è definito come il numero di segmenti di rete indirizzati da coprire. Un ambito pari a zero indica che la trasmissione multicast non verrebbe posizionata in transito, ma potrebbe essere inserita tra i socket all'interno dell'host locale. Il valore di ambito 1 (impostazione predefinita) indica che la trasmissione verrà posizionata in transito, ma non attraversa alcun router. I valori di ambito più elevati determinano il numero di router che possono essere attraversati. Si noti che corrisponde al parametro TTL (Time-to-Live) nel multicasting IP.

La funzione [**WSAJoinLeaf**](/windows/desktop/api/Winsock2/nf-winsock2-wsajoinleaf) viene usata per unire un nodo foglia alla sessione multipunto. Per una descrizione dell'utilizzo di questa funzione, vedere quanto segue.

 

 



