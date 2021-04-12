---
description: La query WSALookupServiceBegin USA SVCID \_ inet \_ HOSTNAMEBYADDR come GUID della classe del servizio.
ms.assetid: 6fd54708-dbd0-4402-8eb8-9cdc42cd56ad
title: Funzione gethostbyaddr in SPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c94f4cdead3a19814e535e2dee80dfdcd0c9fa26
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104526172"
---
# <a name="gethostbyaddr-function-in-the-spi"></a>Funzione gethostbyaddr in SPI

La query [**WSALookupServiceBegin**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicebegina) USA SVCID \_ inet \_ HOSTNAMEBYADDR come GUID della classe del servizio. L'indirizzo host viene fornito in *lpszServiceInstanceName* come stringa di indirizzo IPv4 decimale punteggiata (ad esempio, 192.9.200.120). Il *\_32.dllWS2* specifica il \_ BLOB restituito LUP \_ e NSP inserisce una struttura [**hostent**](/windows/desktop/api/winsock/ns-winsock-hostent) nel BLOB (usando gli offset invece dei puntatori come descritto in precedenza). Rete deve rispettare anche questi altri \_ \_ \* flag di LUP restituiti.



| Flag              | Descrizione                                                                                                                                                  |
|-------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \_nome restituito \_ LUP | Restituisce il membro del **\_ nome h** dalla struttura [**hostent**](/windows/desktop/api/winsock/ns-winsock-hostent) in *lpszServiceInstanceName*.                                                     |
| LUP \_ restituire \_ addr | Restituisce le informazioni di indirizzamento da [**hostent**](/windows/desktop/api/winsock/ns-winsock-hostent) nelle strutture delle [**\_ informazioni di CSADDR**](/windows/win32/api/ws2def/ns-ws2def-csaddr_info) . il valore predefinito per le informazioni sulla porta è zero. |



 

 

 
