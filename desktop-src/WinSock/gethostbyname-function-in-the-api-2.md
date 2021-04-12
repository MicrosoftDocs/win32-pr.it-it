---
description: Funzione gethostbyname nell'API Winsock.
ms.assetid: 015637ed-7a3e-49eb-96ef-8fe82d2902f5
title: Funzione gethostbyname nell'API
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dc3881897a0c971c48ca9a02e6205ec1cae0476f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104129191"
---
# <a name="gethostbyname-function-in-the-api"></a>Funzione gethostbyname nell'API

La funzione [**gethostbyname**](/windows/win32/api/wsipv6ok/nf-wsipv6ok-gethostbyname) usa la funzione [**WSALookupServiceBegin**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicebegina) per eseguire una query su SVCID \_ inet \_ HOSTADDRBYNAME come GUID della classe del servizio. Il nome host viene fornito nel membro **lpszServiceInstanceName** della struttura [**WSAQUERYSET**](/windows/desktop/api/Winsock2/ns-winsock2-wsaquerysetw) passato alla funzione **WSALookupServiceBegin** . Il \_32.dll WS2 specifica il \_ BLOB restituito LUP \_ e il provider del servizio nome inserisce una struttura [**hostent**](/windows/desktop/api/winsock/ns-winsock-hostent) nel BLOB (usando gli offset invece dei puntatori come descritto in precedenza). I provider di servizi dei nomi devono rispettare \_ anche questi altri flag restituiti LUP \_ \* .

| Flag              | Descrizione                                                                                                                                                                                                                                            |
|-------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \_nome restituito \_ LUP | Restituisce il membro del **\_ nome h** dalla struttura [**hostent**](/windows/desktop/api/winsock/ns-winsock-hostent) in *lpszServiceInstanceName*.                                                                                                                                           |
| LUP \_ restituire \_ addr | Restituisce le informazioni di indirizzamento da [**hostent**](/windows/desktop/api/winsock/ns-winsock-hostent) nelle strutture delle [**\_ informazioni di CSADDR**](/windows/win32/api/ws2def/ns-ws2def-csaddr_info) . il valore predefinito per le informazioni sulla porta è zero. Si noti che questa routine non risolve i nomi host che sono costituiti da un indirizzo IPv4 punteggiato. |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Risoluzione dei nomi compatibile per TCP/IP nell'API Windows Sockets 1,1](compatible-name-resolution-for-tcp-ip-in-the-windows-sockets-1-1-api-2.md)
</dt> <dt>

[Risoluzione dei nomi indipendente dal protocollo](protocol-independent-name-resolution-2.md)
</dt> <dt>

[Registrazione e risoluzione dei nomi](registration-and-name-resolution-2.md)
</dt> </dl>

 

 
