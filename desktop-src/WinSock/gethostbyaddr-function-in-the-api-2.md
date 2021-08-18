---
description: La funzione gethostbyaddr usa la funzione WSALookupServiceBegin per eseguire una query su SVCID \_ INET \_ HOSTNAMEBYADDR come GUID della classe del servizio.
ms.assetid: 9b1e3f3f-bfc0-4099-b699-af56019055e6
title: Funzione gethostbyaddr nell'API
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cac84d30ba919a4fc61456d5ca4772c12df786d89241e8249b57068b9aac3f7f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119132324"
---
# <a name="gethostbyaddr-function-in-the-api"></a>Funzione gethostbyaddr nell'API

La [**funzione gethostbyaddr**](/windows/win32/api/wsipv6ok/nf-wsipv6ok-gethostbyaddr) usa la funzione [**WSALookupServiceBegin**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicebegina) per eseguire una query su SVCID \_ INET \_ HOSTNAMEBYADDR come GUID della classe del servizio. L'indirizzo host viene fornito come stringa IPv4 decimale tratteggiata (ad esempio, "192.9.200.120") nel membro *lpszServiceInstanceName* della struttura [**WSAQUERYSET**](/windows/desktop/api/Winsock2/ns-winsock2-wsaquerysetw) passata alla funzione **WSALookupServiceBegin.** L'32.dll Ws2 specifica LUP RETURN BLOB e il provider di servizi dei nomi inserisce una struttura HOSTENT nel BLOB (usando offset anziché puntatori come descritto \_ \_ in \_ precedenza). [](/windows/desktop/api/winsock/ns-winsock-hostent) I provider di servizi dei nomi devono rispettare anche questi altri \_ flag LUP \_ \* RETURN. 

| Flag              | Descrizione                                                                                                                                                  |
|-------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------|
| NOME \_ RESTITUITO \_ LUP | Restituisce il **membro \_ h name** dalla struttura [**HOSTENT**](/windows/desktop/api/winsock/ns-winsock-hostent) in *lpszServiceInstanceName*.                                                     |
| LUP \_ RETURN \_ ADDR | Restituisce informazioni di indirizzamento da [**HOSTENT**](/windows/desktop/api/winsock/ns-winsock-hostent) nelle [**strutture CSADDR \_ INFO,**](/windows/win32/api/ws2def/ns-ws2def-csaddr_info) le informazioni sulla porta vengono visualizzate per impostazione predefinita su zero. |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Risoluzione dei nomi compatibile per TCP/IP nell'API Windows Sockets 1.1](compatible-name-resolution-for-tcp-ip-in-the-windows-sockets-1-1-api-2.md)
</dt> <dt>

[Risoluzione dei nomi indipendente dal protocollo](protocol-independent-name-resolution-2.md)
</dt> <dt>

[Registrazione e risoluzione dei nomi](registration-and-name-resolution-2.md)
</dt> </dl>

 

 
