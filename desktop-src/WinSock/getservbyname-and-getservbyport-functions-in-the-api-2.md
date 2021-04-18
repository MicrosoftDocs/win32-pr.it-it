---
description: Le funzioni getservbyname e getservbyport usano la funzione WSALookupServiceBegin per eseguire query SVCID \_ inet \_ SERVICEBYNAME come GUID della classe del servizio.
ms.assetid: 6d4eb1d4-1498-4367-886b-6b08e87bc4a0
title: Funzioni getservbyname e getservbyport nell'API
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e0028b9ed090463234d01e2b13191ff2328baf2c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106306958"
---
# <a name="getservbyname-and-getservbyport-functions-in-the-api"></a>Funzioni getservbyname e getservbyport nell'API

Le funzioni [**GetServByName**](/windows/desktop/api/winsock/nf-winsock-getservbyname) e [**getservbyport**](/windows/desktop/api/winsock/nf-winsock-getservbyport) usano la funzione [**WSALookupServiceBegin**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicebegina) per eseguire query SVCID \_ inet \_ SERVICEBYNAME come GUID della classe del servizio. Il membro *lpszServiceInstanceName* della struttura [**WSAQUERYSET**](/windows/desktop/api/Winsock2/ns-winsock2-wsaquerysetw) passato alla funzione **WSALookupServiceBegin** fa riferimento a una stringa che indica il nome del servizio o la porta del servizio e, facoltativamente, il protocollo del servizio. La formattazione della stringa è illustrata come FTP o TCP o 21/TCP o solo FTP. La stringa non distingue tra maiuscole e minuscole. La barra contrassegnata, se presente, separa l'identificatore del protocollo dalla parte precedente della stringa. Il \_32.dll WS2 specifica il \_ BLOB restituito LUP \_ e il provider dello spazio dei nomi inserisce una struttura [**SERVENT**](/windows/desktop/api/winsock/ns-winsock-servent) nel BLOB (usando gli offset invece dei puntatori come descritto in precedenza). I provider dello spazio dei nomi devono rispettare anche questi altri \_ flag restituiti LUP \_ \* .

| Flag              | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
|-------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \_nome restituito \_ LUP | Restituisce il membro del **\_ nome s** dalla struttura [**SERVENT**](/windows/desktop/api/winsock/ns-winsock-servent) in *lpszServiceInstanceName*.                                                                                                                                                                                                                                                                                                                                                                                                               |
| \_tipo restituito \_ LUP | Restituisce il GUID canonico in *lpServiceClassId* . si comprende che un servizio identificato come FTP o 21 può trovarsi in un'altra porta secondo le convenzioni stabilite localmente. Il parametro della **\_ porta s** della struttura [**SERVENT**](/windows/desktop/api/winsock/ns-winsock-servent) deve indicare la posizione in cui il servizio può essere contattato nell'ambiente locale. Il GUID canonico restituito quando \_ \_ è impostato il tipo restituito LUP deve essere uno dei GUID predefiniti di Svcs. h che corrisponde al numero di porta indicato nella struttura **SERVENT** . |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Risoluzione dei nomi compatibile per TCP/IP nell'API Windows Sockets 1,1](compatible-name-resolution-for-tcp-ip-in-the-windows-sockets-1-1-api-2.md)
</dt> <dt>

[Risoluzione dei nomi indipendente dal protocollo](protocol-independent-name-resolution-2.md)
</dt> <dt>

[Registrazione e risoluzione dei nomi](registration-and-name-resolution-2.md)
</dt> </dl>

 

 



