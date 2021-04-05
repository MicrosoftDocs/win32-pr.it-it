---
description: Quando viene utilizzato il multicast, in genere è necessario specificare l'ambito sul quale deve essere eseguito il multicast.
ms.assetid: 744b43a8-dd89-4e63-ae3c-5bee72864df7
title: Codice del comando SIO_MULTICAST_SCOPE per WSAIoctl
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 209a43e461907dcded8e59c6ffee9b1376989d6e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104049765"
---
# <a name="sio_multicast_scope-command-code-for-wsaioctl"></a>\_ \_ Codice del comando per ambito multicast Sio per WSAIoctl

Quando viene utilizzato il multicast, in genere è necessario specificare l' *ambito* sul quale deve essere eseguito il multicast. L'ambito è definito come il numero di segmenti di rete indirizzati da coprire. Un ambito pari a zero indicherà che la trasmissione multicast non verrà distribuita in transito, ma potrebbe essere divulgata tra i socket all'interno dell'host locale. Un valore di ambito pari a 1 (impostazione predefinita) indica che la trasmissione verrà posizionata in transito, ma non incrocierà alcun router. I valori di ambito più elevati determinano il numero di router che possono essere superati. Si noti che corrisponde al parametro time-to-Live (TTL) in multicast IP.

La funzione [**WSAJoinLeaf**](/windows/desktop/api/Winsock2/nf-winsock2-wsajoinleaf) viene usata per aggiungere un nodo foglia alla sessione multipoint. Per una discussione su come viene usata questa funzione, vedere quanto segue.

 

 



