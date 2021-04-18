---
description: La funzione GetHostName utilizza la funzione WSALookupServiceBegin per eseguire una query sul \_ nome host SVCID come GUID della classe del servizio.
ms.assetid: 39498c2f-6047-484d-a8ea-253461e5b0f5
title: Funzione GetHostName nell'API
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d8629083c49e3915dd0ec4f1cfeb9363caabf8b9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106306967"
---
# <a name="gethostname-function-in-the-api"></a>Funzione GetHostName nell'API

La funzione [**GetHostName**](/windows/desktop/api/winsock/nf-winsock-gethostname) utilizza la funzione [**WSALookupServiceBegin**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicebegina) per eseguire una query sul \_ nome host SVCID come GUID della classe del servizio. Se il membro **lpszServiceInstanceName** della struttura [**WSAQUERYSET**](/windows/desktop/api/Winsock2/ns-winsock2-wsaquerysetw) passato alla funzione **WSALookupServiceBegin** è **null** o fa riferimento a una stringa **null** , ovvero. ""), l'host locale deve essere risolto. In caso contrario, viene eseguita una ricerca in un nome host specificato. Ai fini dell'emulazione di **GetHostName** , WS2 \_32.dll specifica un puntatore **null** per il membro **lpszServiceInstanceName** e specifica LUP \_ nome restituito \_ in modo che il nome host venga restituito nel membro **lpszServiceInstanceName** . Se un'applicazione usa questa query e specifica LUP \_ return \_ addr, l'indirizzo host viene fornito in una struttura di [**\_ informazioni di CSADDR**](/windows/win32/api/ws2def/ns-ws2def-csaddr_info) . L' \_ azione LUP return \_ BLOB non è definita per questa query. Le informazioni sulla porta vengono predefinite su zero, a meno che il membro **lpszQueryString** della struttura **WSAQUERYSET** passato alla funzione **WSALookupServiceBegin** faccia riferimento a un servizio quale FTP, nel qual caso viene fornito l'indirizzo di trasporto completo del servizio indicato.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Risoluzione dei nomi compatibile per TCP/IP nell'API Windows Sockets 1,1](compatible-name-resolution-for-tcp-ip-in-the-windows-sockets-1-1-api-2.md)
</dt> <dt>

[Risoluzione dei nomi indipendente dal protocollo](protocol-independent-name-resolution-2.md)
</dt> <dt>

[Registrazione e risoluzione dei nomi](registration-and-name-resolution-2.md)
</dt> </dl>

 

 
