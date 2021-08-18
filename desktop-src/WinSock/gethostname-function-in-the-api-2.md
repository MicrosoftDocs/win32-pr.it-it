---
description: La funzione gethostname usa la funzione WSALookupServiceBegin per eseguire una query su SVCID \_ HOSTNAME come GUID della classe del servizio.
ms.assetid: 39498c2f-6047-484d-a8ea-253461e5b0f5
title: Funzione gethostname nell'API
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6ec72c7eab46ccb9988dc166d8121304850ea49e2488901496e5c0377a395a48
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119132274"
---
# <a name="gethostname-function-in-the-api"></a>Funzione gethostname nell'API

La [**funzione gethostname**](/windows/desktop/api/winsock/nf-winsock-gethostname) usa la [**funzione WSALookupServiceBegin**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicebegina) per eseguire una query su SVCID \_ HOSTNAME come GUID della classe del servizio. Se il membro **lpszServiceInstanceName** della struttura [**WSAQUERYSET**](/windows/desktop/api/Winsock2/ns-winsock2-wsaquerysetw) passato alla funzione **WSALookupServiceBegin** è **NULL** o fa riferimento a una stringa **NULL** (ovvero . ""), l'host locale deve essere risolto. In caso contrario, viene eseguita una ricerca in un nome host specificato. Ai fini dell'emulazione di **gethostname,** il32.dll Ws2 specifica un puntatore NULL per il membro \_ **lpszServiceInstanceName** e specifica LUP RETURN NAME in modo che il nome host sia restituito nel membro  \_ \_ **lpszServiceInstanceName.** Se un'applicazione usa questa query e specifica LUP RETURN ADDR, l'indirizzo host viene fornito \_ \_ in una struttura [**CSADDR \_ INFO.**](/windows/win32/api/ws2def/ns-ws2def-csaddr_info) L'azione \_ LUP RETURN \_ BLOB non è definita per questa query. Per impostazione predefinita, le informazioni sulla porta sono pari a zero, a meno che il membro **lpszQueryString** della struttura **WSAQUERYSET** passato alla funzione **WSALookupServiceBegin** non faccia riferimento a un servizio come FTP, nel qual caso viene fornito l'indirizzo di trasporto completo del servizio indicato.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Risoluzione dei nomi compatibile per TCP/IP nell'API Windows Sockets 1.1](compatible-name-resolution-for-tcp-ip-in-the-windows-sockets-1-1-api-2.md)
</dt> <dt>

[Risoluzione dei nomi indipendente dal protocollo](protocol-independent-name-resolution-2.md)
</dt> <dt>

[Registrazione e risoluzione dei nomi](registration-and-name-resolution-2.md)
</dt> </dl>

 

 
