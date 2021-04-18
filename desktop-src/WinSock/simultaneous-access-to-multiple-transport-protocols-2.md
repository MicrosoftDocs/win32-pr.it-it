---
description: Per poter accedere a un'applicazione, è necessario che nel sistema sia installato correttamente un protocollo di trasporto e che sia registrato con Windows Sockets.
ms.assetid: 45b20f66-4e12-44df-b64b-c96cd5b24cd4
title: Accesso simultaneo a più protocolli di trasporto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d5e4b9d97743691bc527c455881cd0da5803b62b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106309932"
---
# <a name="simultaneous-access-to-multiple-transport-protocols"></a>Accesso simultaneo a più protocolli di trasporto

Per poter accedere a un'applicazione, è necessario che nel sistema sia installato correttamente un protocollo di trasporto e che sia registrato con Windows Sockets. La \_ libreria32.dll WS2 esporta un set di funzioni per facilitare il processo di registrazione. È inclusa la creazione di una nuova registrazione e la rimozione di una esistente.

Quando vengono create nuove registrazioni, il chiamante (ovvero lo script di installazione del fornitore dello stack) fornisce una o più strutture di [**\_ informazioni WSAPROTOCOL**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) contenenti un set completo di informazioni sul protocollo. Per ulteriori informazioni, vedere [Windows Sockets 2 SPI](about-the-winsock-spi.md). Qualsiasi stack di trasporto installato in questo modo viene definito provider di servizi Windows Sockets.

In Windows XP con Service Pack 2 (SP2), Windows Server 2003 con Service Pack 1 (SP1) e Windows Vista e versioni successive. il catalogo Winsock contenente un elenco di provider di trasporto e spazio dei nomi installati può essere visualizzato in un prompt dei comandi con il comando seguente:

**netsh winsock Show Catalog**

Il Software Development Kit (SDK) di Microsoft Windows include *Sporder.exe*, che consente all'utente di visualizzare e modificare l'ordine in cui vengono enumerati i provider di servizi. Utilizzando *Sporder.exe*, un utente può stabilire manualmente un particolare stack di protocolli TCP/IP come provider TCP/IP predefinito se è presente più di uno stack di questo tipo.

L'applicazione *Sporder.exe* usa le funzioni esportate da *Sporder.dll* per riordinare i provider di servizi. Di conseguenza, le applicazioni di installazione possono utilizzare l'interfaccia fornita da *Sporder.dll* per riordinare i provider di servizi a livello di codice.

-   [Protocolli sovrapposti e catene di protocolli](layered-protocols-and-protocol-chains-2.md)
-   [Uso di più protocolli](using-multiple-protocols-2.md)
-   [Limitazioni di più provider per Select](multiple-provider-restrictions-on-select-2.md)

 

 
