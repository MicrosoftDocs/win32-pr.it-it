---
description: Funzione Gethostbyname in Winsock SPI.
ms.assetid: 3e63a6db-1ecc-4ce1-b772-25dc9a57e0d9
title: Funzione gethostbyname nell'spi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9435480ef01a7ac843c8f00028250e1ba05c09fe921c3e7c4c068072f673eea0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118112264"
---
# <a name="gethostbyname-function-in-the-spi"></a>Funzione gethostbyname nell'spi

La query [**WSALookupServiceBegin**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicebegina) usa SVCID \_ INET \_ HOSTADDRBYNAME come GUID della classe di servizio. Il nome host viene specificato in *lpszServiceInstanceName*. *L'32.dll\_ Ws2* specifica LUP RETURN BLOB e il provider di servizi di rete inserisce una struttura HOSTENT nel BLOB (usando offset anziché puntatori come descritto in \_ \_ precedenza). [](/windows/desktop/api/winsock/ns-winsock-hostent) I server dei criteri di rete devono rispettare anche questi altri flag LUP \_ \_ \* RETURN.



| Flag              | Descrizione                                                                                                                                                                                                                                                         |
|-------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| NOME \_ RESTITUITO \_ LUP | Restituisce il **membro \_ h name** dalla struttura [**HOSTENT**](/windows/desktop/api/winsock/ns-winsock-hostent) in *lpszServiceInstanceName*.                                                                                                                                                            |
| LUP \_ RETURN \_ ADDR | Restituisce le informazioni di indirizzamento [**da HOSTENT**](/windows/desktop/api/winsock/ns-winsock-hostent) nelle [**strutture CSADDR \_ INFO,**](/windows/win32/api/ws2def/ns-ws2def-csaddr_info) le informazioni sulla porta sono per impostazione predefinita pari a zero. Si noti che questa routine non risolve i nomi host costituiti da una stringa di indirizzi IPv4 con separatore tratteggiato. |



 

 

 
