---
description: Un provider dello spazio dei nomi implementa un mapping di interfaccia tra lo spi dello spazio dei nomi Winsock e l'interfaccia programmatica nativa di un servizio nomi esistente, ad esempio DNS, X.500 o NetWare Directory Services (NDS).
ms.assetid: 9b35aa58-9011-4e0d-8c93-02714952b4a5
title: Provider di servizi dello spazio dei nomi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 35e6ecc9ad0dcb9667bdd3d08049b9d41c3211de422cae0530506f6103494527
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118822639"
---
# <a name="namespace-service-providers"></a>Provider di servizi dello spazio dei nomi

Un provider dello spazio dei nomi implementa un mapping di interfaccia tra lo spi dello spazio dei nomi Winsock e l'interfaccia programmatica nativa di un servizio nomi esistente, ad esempio DNS, X.500 o NetWare Directory Services (NDS). Sebbene un provider dello spazio dei nomi supporti esattamente uno spazio dei nomi, è possibile che siano installati più provider per un determinato spazio dei nomi. È anche possibile che una singola DLL crei un'istanza di più provider di spazi dei nomi. Quando vengono installati i provider di spazi dei nomi, viene mantenuto un catalogo [**di strutture WSANAMESPACE \_ INFO.**](/windows/desktop/api/Winsock2/ns-winsock2-wsanamespace_infow) Un'applicazione può [**usare WSAEnumNameSpaceProviders**](/windows/desktop/api/Winsock2/nf-winsock2-wsaenumnamespaceprovidersa) per individuare gli spazi dei nomi supportati in un computer.

In Windows Vista e versioni successive vengono fornite una struttura [**\_ INFOEX WSANAMESPACE**](/windows/desktop/api/Winsock2/ns-winsock2-wsanamespace_infoexw) avanzata e la [**funzione WSAEnumNameSpaceProvidersEx.**](/windows/desktop/api/Winsock2/nf-winsock2-wsaenumnamespaceprovidersexa)

Nelle piattaforme a 64 bit vengono fornite funzioni [**WSCEnumNameSpaceProviders32**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscenumnamespaceproviders32) e [**WSCEnumNameSpaceProvidersEx32**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscenumnamespaceprovidersex32) simili per enumerare il catalogo a 32 bit.

Per informazioni dettagliate, vedere Requisiti del provider di servizi dello spazio dei nomi [Winsock.](winsock-namespace-service-provider-requirements.md)

## <a name="legacy-getxbyy-service-providers"></a>Provider di servizi GetXbyY legacy

Windows Sockets 2 supporta completamente le funzionalità di risoluzione dei nomi specifiche di TCP/IP disponibili in Windows Sockets versione 1.1. A tale scopo, include il set **di funzioni GetXbyY** nell'spi. Tuttavia, il trattamento di questo set di funzioni è leggermente diverso dalle altre funzioni SPI. Le **funzioni GetXbyY** visualizzate nell'spi sono precedute da GETXBYYSP e sono riepilogate \_ nella tabella seguente.

Funzioni in stile Berkeley



| Nome della funzione SPI           | Descrizione                                                                              |
|-----------------------------|------------------------------------------------------------------------------------------|
| GETXBYYSP \_ gethostbyaddr    | Fornisce una struttura [**host per**](/windows/desktop/api/winsock/ns-winsock-hostent) l'indirizzo host specificato.        |
| GETXBYYSP \_ gethostbyname    | Fornisce una struttura [**hostent**](/windows/desktop/api/winsock/ns-winsock-hostent) per il nome host specificato.           |
| GETXBYYSP \_ getprotobyname   | Fornisce una [**struttura protoent**](/windows/desktop/api/winsock/ns-winsock-protoent) per il nome del protocollo specificato.     |
| GETXBYYSP \_ getprotobynumber | Fornisce una [**struttura protoent**](/windows/desktop/api/winsock/ns-winsock-protoent) per il numero di protocollo specificato.   |
| GETXBYYSP \_ getservbyname    | Fornisce una [**struttura di servizio**](/windows/desktop/api/winsock/ns-winsock-servent) per il servizio nam.e specificato        |
| GETXBYYSP \_ getservbyport    | Fornisce una [**struttura di servizio**](/windows/desktop/api/winsock/ns-winsock-servent) per il servizio alla porta specificata. |
| GETXBYYSP \_ gethostname      | Restituisce il nome host standard per il computer locale.                                   |



 

Funzioni di stile asincrone



| Nome della funzione SPI                   | Descrizione                                                                              |
|-------------------------------------|------------------------------------------------------------------------------------------|
| GETXBYYSP \_ WSAAsyncGetHostByAddr    | Fornisce una struttura [**host per**](/windows/desktop/api/winsock/ns-winsock-hostent) l'indirizzo host specificato.        |
| GETXBYYSP \_ WSAAsyncGetHostByName    | Fornisce una struttura [**hostent**](/windows/desktop/api/winsock/ns-winsock-hostent) per il nome host specificato.           |
| GETXBYYSP \_ WSAAsyncGetProtoByName   | Fornisce una [**struttura protoent**](/windows/desktop/api/winsock/ns-winsock-protoent) per il nome del protocollo specificato.     |
| GETXBYYSP \_ WSAAsyncGetProtoByNumber | Fornisce una [**struttura protoent**](/windows/desktop/api/winsock/ns-winsock-protoent) per il numero di protocollo specificato.   |
| GETXBYYSP \_ WSAAsyncGetServByName    | Fornisce una struttura [**di servizio**](/windows/desktop/api/winsock/ns-winsock-servent) per il nome del servizio specificato.        |
| GETXBYYSP \_ WSAAsyncGetServByPort    | Fornisce una [**struttura di servizio**](/windows/desktop/api/winsock/ns-winsock-servent) per il servizio alla porta specificata. |
| GETXBYYSP \_ WSACancelAsyncRequest    | Annulla **un'operazione GetXbyY** asincrona.                                           |



 

La sintassi e la semantica di queste funzioni **GetXbyY** nello spi sono esattamente uguali a quelle documentate nella specifica API e non vengono quindi ripetute qui.

La DLL Windows Sockets 2 consente esattamente a un provider di servizi di offrire questi servizi. Pertanto, non è necessario includere puntatori a queste funzioni nella tabella della procedura ricevuta dai provider di servizi all'avvio. Negli Windows il percorso della DLL che implementa queste funzioni viene recuperato dal valore presente nel percorso del Registro di sistema seguente. Questa voce del Registro di sistema non esiste per impostazione predefinita:

**HKEY \_ Local \_ MACHINE** \\ **System** \\ **CurrentControlSet** \\ **Services** \\ **WinSock2** \\ **Parameters** \\ **GetXByYLibraryPath**

## <a name="built-in-default-getxbyy-service-provider"></a>Built-In provider di servizi GetXbyY predefinito

Un provider **di servizi GetXbyY** predefinito è integrato nei componenti di Windows Sockets 2 standard. Questo provider predefinito implementa tutte le funzioni precedenti, pertanto non è necessario che queste funzioni siano implementate da qualsiasi provider dello spazio dei nomi. Tuttavia, un provider dello spazio dei nomi è libero di fornire una o tutte queste funzioni (e quindi eseguire l'override delle impostazioni predefinite) semplicemente archiviando la stringa che rappresenta il percorso della DLL che implementa queste funzioni nella chiave del Registro di sistema indicata. Qualsiasi funzione **GetXbyY** non esportata dalla DLL del provider denominata verrà fornita tramite le impostazioni predefinite predefinite. Si noti, tuttavia, che se un provider sceglie di fornire una delle versioni asincrone delle funzioni **GetXbyY,** deve fornire tutte le funzioni asincrone in modo che l'operazione di annullamento funzioni in modo appropriato.

L'implementazione corrente del provider di **servizi GetXbyY** predefinito si trova all'interno del Wsock32.dll. A seconda di come sono state stabilite le impostazioni TCP/IP tramite Pannello di controllo, la risoluzione dei nomi verrà eseguita usando i file DNS o host locali. Quando si usa DNS, il provider di servizi **GetXbyY** predefinito usa chiamate API Windows Sockets 1.1 standard per comunicare con il server DNS. Queste transazioni verranno eseguite usando qualsiasi stack TCP/IP configurato come stack TCP/IP predefinito. Due casi speciali, tuttavia, meritano una menzione speciale.

L'implementazione predefinita di GETXBYYSP \_ gethostname ottiene il nome host locale dal Registro di sistema. Corrisponderà al nome assegnato a "Computer locale". L'implementazione predefinita di GETXBYYSP \_ gethostbyname e GETXBYYSP WSAAsyncGetHostByName confronta sempre il nome host fornito con il nome \_ host locale. Se corrispondono, l'implementazione predefinita usa un'interfaccia privata per eseguire il probe dello stack TCP/IP Microsoft per individuarne l'indirizzo IP locale. Pertanto, per essere completamente indipendente dallo stack TCP/IP Microsoft, un provider dello spazio dei nomi deve implementare sia GETXBYYSP \_ gethostbyname che GETXBYYSP \_ WSAAsyncGetHostByName.

 

 



