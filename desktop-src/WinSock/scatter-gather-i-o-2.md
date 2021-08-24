---
description: Le funzioni WSARecv, WSARecvFrom, WSARecvMsg, WSASend, WSASendMsg e WSASendTo accettano tutte una matrice di buffer dell'applicazione come parametri di input e possono essere usate per l'I/O a dispersione/raccolta (o vettoriale).
ms.assetid: c42e6cea-3b40-44ad-8715-09ce57e82217
title: I/O a dispersione/raccolta
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b4dc580065655c2d69485a49cd41919345c566c32ec2ff9cd1055383853c7438
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119794681"
---
# <a name="scattergather-io"></a>I/O a dispersione/raccolta

Le funzioni [**WSARecv**](/windows/desktop/api/Winsock2/nf-winsock2-wsarecv), [**WSARecvFrom**](/windows/desktop/api/Winsock2/nf-winsock2-wsarecvfrom), [**LPFN_WSARECVMSG (WSARecvMsg)**](/windows/win32/api/mswsock/nc-mswsock-lpfn_wsarecvmsg), [**WSASend**](/windows/desktop/api/Winsock2/nf-winsock2-wsasend), [**WSASendMsg**](/windows/desktop/api/winsock2/nf-winsock2-wsasendmsg)e [**WSASendTo**](/windows/desktop/api/Winsock2/nf-winsock2-wsasendto) accettano tutte una matrice di buffer dell'applicazione come parametri di input e possono essere usate per l'I/O a dispersione/raccolta (o vettoriale). Ciò può essere molto utile nei casi in cui parti di ogni messaggio trasmesso sono costituite da uno o più componenti di intestazione a lunghezza fissa oltre al corpo del messaggio. Tali componenti di intestazione non devono essere concatenati dall'applicazione in un singolo buffer contiguo prima dell'invio. Analogamente alla ricezione, i componenti di intestazione possono essere suddivisi automaticamente in buffer separati, lasciando il corpo del messaggio da solo.

Quando si riceve in più buffer, il completamento avviene quando i dati arrivano dalla rete, indipendentemente dal fatto che tutti i buffer forniti siano utilizzati.

 

 
