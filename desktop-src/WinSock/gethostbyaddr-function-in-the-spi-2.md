---
description: La query WSALookupServiceBegin usa SVCID \_ INET \_ HOSTNAMEBYADDR come GUID della classe di servizio.
ms.assetid: 6fd54708-dbd0-4402-8eb8-9cdc42cd56ad
title: Funzione gethostbyaddr nell'spi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e343bcd66b7b1482f14a07239ae73710fd789486633219952696406dd8f1bd3d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119132314"
---
# <a name="gethostbyaddr-function-in-the-spi"></a>Funzione gethostbyaddr nell'spi

La query [**WSALookupServiceBegin**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicebegina) usa SVCID \_ INET \_ HOSTNAMEBYADDR come GUID della classe di servizio. L'indirizzo host viene fornito in *lpszServiceInstanceName* come stringa di indirizzo IPv4 con separatore virgola (ad esempio, 192.9.200.120). *L'32.dll\_ Ws2* specifica LUP RETURN BLOB e il provider di servizi di rete inserisce una struttura HOSTENT nel BLOB (usando offset anziché puntatori come descritto in \_ \_ precedenza). [](/windows/desktop/api/winsock/ns-winsock-hostent) I server dei criteri di rete devono rispettare anche questi altri flag LUP \_ \_ \* RETURN.



| Flag              | Descrizione                                                                                                                                                  |
|-------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------|
| NOME \_ RESTITUITO \_ LUP | Restituisce il **membro \_ h name** dalla struttura [**HOSTENT**](/windows/desktop/api/winsock/ns-winsock-hostent) in *lpszServiceInstanceName*.                                                     |
| LUP \_ RETURN \_ ADDR | Restituisce le informazioni di indirizzamento [**da HOSTENT**](/windows/desktop/api/winsock/ns-winsock-hostent) nelle [**strutture CSADDR \_ INFO,**](/windows/win32/api/ws2def/ns-ws2def-csaddr_info) le informazioni sulla porta sono per impostazione predefinita pari a zero. |



 

 

 
