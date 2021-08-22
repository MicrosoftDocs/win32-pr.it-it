---
description: Windows Elementi dell'interfaccia Sockets 2 (Winsock) per multipoint e multicast.
ms.assetid: c6f704cf-031b-4714-9f07-2d7715a157a0
title: Windows Elementi dell'interfaccia Sockets 2 per Multipoint e Multicast
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dcf2422d8171a041f75ba8abed6ea490982187af3affb3d3c3d1349984210ce0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118558853"
---
# <a name="windows-sockets-2-interface-elements-for-multipoint-and-multicast"></a>Windows Elementi dell'interfaccia Sockets 2 per Multipoint e Multicast

I meccanismi incorporati in Windows Sockets 2 per l'utilizzo di funzionalità multipunto possono essere riepilogati come segue:

-   Tre bit di attributo nella [**struttura WSAPROTOCOL \_ INFO.**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa)
-   Quattro flag definiti per il *parametro dwFlags* di [**WSASocket.**](/windows/desktop/api/Winsock2/nf-winsock2-wsasocketa)
-   Una funzione, [**WSAJoinLeaf,**](/windows/desktop/api/Winsock2/nf-winsock2-wsajoinleaf)per l'aggiunta di nodi foglia in una sessione multipunto.
-   Due [**codici di comando WSAIoctl**](/windows/desktop/api/Winsock2/nf-winsock2-wsaioctl) per il controllo del loopback multipoint e l'ambito delle trasmissioni multicast.

Le sezioni seguenti descrivono questi elementi dell'interfaccia in modo più dettagliato:

-   [Semantica per unire le foglia multipunto](semantics-for-joining-multipoint-leaves-2.md)
-   [Supporto di queste estensioni da parte dei protocolli Multipoint esistenti](how-existing-multipoint-protocols-support-these-extensions-2.md)

 

 
