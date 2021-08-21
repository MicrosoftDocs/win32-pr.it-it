---
description: Le funzioni getservbyname e getservbyport usano la funzione WSALookupServiceBegin per eseguire una query su SVCID \_ INET SERVICEBYNAME come GUID della classe \_ del servizio.
ms.assetid: 6d4eb1d4-1498-4367-886b-6b08e87bc4a0
title: Funzioni getservbyname e getservbyport nell'API
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 47e5d7cc9b1811eef98cc6d337abc3230ea46bd537a19969a4b412473e671b39
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119132214"
---
# <a name="getservbyname-and-getservbyport-functions-in-the-api"></a>Funzioni getservbyname e getservbyport nell'API

Le [**funzioni getservbyname**](/windows/desktop/api/winsock/nf-winsock-getservbyname) e [**getservbyport**](/windows/desktop/api/winsock/nf-winsock-getservbyport) usano la funzione [**WSALookupServiceBegin**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicebegina) per eseguire una query su SVCID \_ INET SERVICEBYNAME come GUID della classe \_ del servizio. Il membro *lpszServiceInstanceName* nella struttura [**WSAQUERYSET**](/windows/desktop/api/Winsock2/ns-winsock2-wsaquerysetw) passata alla funzione **WSALookupServiceBegin** fa riferimento a una stringa per indicare il nome del servizio o la porta del servizio e(facoltativamente) il protocollo del servizio. La formattazione della stringa viene illustrata come FTP, TCP o 21/TCP o solo FTP. La stringa non fa distinzione tra maiuscole e minuscole. La barra, se presente, separa l'identificatore di protocollo dalla parte precedente della stringa. L'32.dll Ws2 specifica LUP RETURN BLOB e il provider dello spazio dei nomi inserirà una struttura SERVENT nel BLOB (usando offset anziché puntatori come descritto \_ \_ in \_ precedenza). [](/windows/desktop/api/winsock/ns-winsock-servent) I provider dello spazio dei nomi devono rispettare anche questi \_ altri flag LUP \_ \* RETURN.

| Flag              | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
|-------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| NOME \_ RESTITUITO \_ LUP | Restituisce il **membro \_ del nome s** dalla struttura [**SERVENT**](/windows/desktop/api/winsock/ns-winsock-servent) in *lpszServiceInstanceName.*                                                                                                                                                                                                                                                                                                                                                                                                               |
| TIPO \_ RESTITUITO \_ LUP | Restituisce il GUID canonico in *lpServiceClassId.* Si è compreso che un servizio identificato come FTP o 21 può essere su un'altra porta in base alle convenzioni stabilite localmente. Il **parametro \_ s port** della struttura [**SERVENT**](/windows/desktop/api/winsock/ns-winsock-servent) deve indicare dove il servizio può essere contattato nell'ambiente locale. Il GUID canonico restituito quando l'opzione LUP RETURN TYPE è impostata deve essere uno dei GUID predefiniti di \_ Svcs.h che corrisponde al numero di porta indicato nella \_ **struttura SERVENT.** |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Risoluzione dei nomi compatibile per TCP/IP nell'API Windows Sockets 1.1](compatible-name-resolution-for-tcp-ip-in-the-windows-sockets-1-1-api-2.md)
</dt> <dt>

[Risoluzione dei nomi indipendente dal protocollo](protocol-independent-name-resolution-2.md)
</dt> <dt>

[Registrazione e risoluzione dei nomi](registration-and-name-resolution-2.md)
</dt> </dl>

 

 



