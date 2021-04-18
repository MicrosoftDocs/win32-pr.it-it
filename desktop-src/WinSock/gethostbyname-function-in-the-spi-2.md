---
description: Funzione gethostbyname nell'SPI Winsock.
ms.assetid: 3e63a6db-1ecc-4ce1-b772-25dc9a57e0d9
title: Funzione gethostbyname in SPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6a04f39ca00dc712ef7b8ce3bdef480aa253a5b7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106306968"
---
# <a name="gethostbyname-function-in-the-spi"></a>Funzione gethostbyname in SPI

La query [**WSALookupServiceBegin**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicebegina) USA SVCID \_ inet \_ HOSTADDRBYNAME come GUID della classe del servizio. Il nome host viene fornito in *lpszServiceInstanceName*. Il *\_32.dllWS2* specifica il \_ BLOB restituito LUP \_ e NSP inserisce una struttura [**hostent**](/windows/desktop/api/winsock/ns-winsock-hostent) nel BLOB (usando gli offset invece dei puntatori come descritto in precedenza). Rete deve rispettare anche questi altri \_ \_ \* flag di LUP restituiti.



| Flag              | Descrizione                                                                                                                                                                                                                                                         |
|-------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \_nome restituito \_ LUP | Restituisce il membro del **\_ nome h** dalla struttura [**hostent**](/windows/desktop/api/winsock/ns-winsock-hostent) in *lpszServiceInstanceName*.                                                                                                                                                            |
| LUP \_ restituire \_ addr | Restituisce le informazioni di indirizzamento da [**hostent**](/windows/desktop/api/winsock/ns-winsock-hostent) nelle strutture delle [**\_ informazioni di CSADDR**](/windows/win32/api/ws2def/ns-ws2def-csaddr_info) . il valore predefinito per le informazioni sulla porta è zero. Si noti che questa routine non risolve i nomi host costituiti da una stringa di indirizzo IPv4 decimale punteggiata. |



 

 

 
