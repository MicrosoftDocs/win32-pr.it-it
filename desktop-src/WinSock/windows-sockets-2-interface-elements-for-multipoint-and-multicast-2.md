---
description: Elementi dell'interfaccia Windows Sockets 2 (Winsock) per MultiPoint e multicast.
ms.assetid: c6f704cf-031b-4714-9f07-2d7715a157a0
title: Elementi dell'interfaccia Windows Sockets 2 per MultiPoint e multicast
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ad86905fe19c5c4c603db488874039b7cc8a0b2f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106308868"
---
# <a name="windows-sockets-2-interface-elements-for-multipoint-and-multicast"></a>Elementi dell'interfaccia Windows Sockets 2 per MultiPoint e multicast

I meccanismi incorporati in Windows Sockets 2 per l'uso delle funzionalità multipoint possono essere riepilogati come segue:

-   Tre bit di attributo nella struttura di [**\_ informazioni WSAPROTOCOL**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) .
-   Quattro flag definiti per il parametro *dwFlags* di [**WSASocket**](/windows/desktop/api/Winsock2/nf-winsock2-wsasocketa).
-   Una funzione, [**WSAJoinLeaf**](/windows/desktop/api/Winsock2/nf-winsock2-wsajoinleaf), per l'aggiunta di nodi foglia in una sessione multipoint.
-   Due codici di comando di [**WSAIoctl**](/windows/desktop/api/Winsock2/nf-winsock2-wsaioctl) per il controllo di loopback multipoint e l'ambito delle trasmissioni multicast.

Le sezioni seguenti descrivono questi elementi dell'interfaccia in modo più dettagliato:

-   [Semantica per l'Unione di foglie multipoint](semantics-for-joining-multipoint-leaves-2.md)
-   [Supporto di queste estensioni da protocolli multipoint esistenti](how-existing-multipoint-protocols-support-these-extensions-2.md)

 

 
