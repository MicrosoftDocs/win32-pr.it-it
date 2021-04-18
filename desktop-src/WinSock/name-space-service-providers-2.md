---
description: Un provider dello spazio dei nomi implementa un mapping di interfaccia tra lo spazio dei nomi di Winsock e l'interfaccia a livello di codice nativo di un servizio dei nomi esistente, ad esempio DNS, X. 500 o servizi directory NetWare (NDS).
ms.assetid: 9b35aa58-9011-4e0d-8c93-02714952b4a5
title: Provider di servizi dello spazio dei nomi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4e975c7ad0e5df29910624bb8f0b9d94fd24d9b8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106306918"
---
# <a name="namespace-service-providers"></a>Provider di servizi dello spazio dei nomi

Un provider dello spazio dei nomi implementa un mapping di interfaccia tra lo spazio dei nomi di Winsock e l'interfaccia a livello di codice nativo di un servizio dei nomi esistente, ad esempio DNS, X. 500 o servizi directory NetWare (NDS). Mentre un provider dello spazio dei nomi supporta esattamente uno spazio dei nomi, è possibile che vengano installati più provider per uno spazio dei nomi specifico. È anche possibile che una singola DLL crei un'istanza di più provider dello spazio dei nomi. Quando vengono installati i provider dello spazio dei nomi, viene mantenuto un catalogo di strutture di [**\_ informazioni WSANAMESPACE**](/windows/desktop/api/Winsock2/ns-winsock2-wsanamespace_infow) . Un'applicazione può utilizzare [**WSAEnumNameSpaceProviders**](/windows/desktop/api/Winsock2/nf-winsock2-wsaenumnamespaceprovidersa) per individuare gli spazi dei nomi supportati in un computer.

In Windows Vista e versioni successive, vengono fornite una struttura [**WSANAMESPACE \_ INFOEX**](/windows/desktop/api/Winsock2/ns-winsock2-wsanamespace_infoexw) avanzata e una funzione [**WSAEnumNameSpaceProvidersEx**](/windows/desktop/api/Winsock2/nf-winsock2-wsaenumnamespaceprovidersexa) .

Sulle piattaforme a 64 bit sono disponibili funzioni [**WSCEnumNameSpaceProviders32**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscenumnamespaceproviders32) e [**WSCEnumNameSpaceProvidersEx32**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscenumnamespaceprovidersex32) simili per enumerare il catalogo a 32 bit.

Per informazioni dettagliate, vedere [requisiti del provider di servizi dello spazio dei nomi Winsock](winsock-namespace-service-provider-requirements.md) .

## <a name="legacy-getxbyy-service-providers"></a>Provider di servizi GetXbyY legacy

Windows Sockets 2 supporta completamente le funzionalità di risoluzione dei nomi specifiche di TCP/IP disponibili in Windows Sockets versione 1,1. Questa operazione viene eseguita includendo il set di funzioni **GetXbyY** in spi. Tuttavia, il trattamento di questo set di funzioni è leggermente diverso dal resto delle funzioni SPI. Le funzioni **GetXbyY** visualizzate in SPI sono precedute da GETXBYYSP \_ e sono riepilogate nella tabella seguente.

Funzioni di stile Berkeley



| Nome della funzione SPI           | Descrizione                                                                              |
|-----------------------------|------------------------------------------------------------------------------------------|
| \_GETHOSTBYADDR GETXBYYSP    | Fornisce una struttura [**hostent**](/windows/desktop/api/winsock/ns-winsock-hostent) per l'indirizzo host specificato.        |
| \_Gethostbyname GETXBYYSP    | Fornisce una struttura [**hostent**](/windows/desktop/api/winsock/ns-winsock-hostent) per il nome host specificato.           |
| \_GETPROTOBYNAME GETXBYYSP   | Fornisce una struttura [**protoent**](/windows/desktop/api/winsock/ns-winsock-protoent) per il nome di protocollo specificato.     |
| \_GETPROTOBYNUMBER GETXBYYSP | Fornisce una struttura [**protoent**](/windows/desktop/api/winsock/ns-winsock-protoent) per il numero di protocollo specificato.   |
| \_GETSERVBYNAME GETXBYYSP    | Fornisce una struttura [**Servent**](/windows/desktop/api/winsock/ns-winsock-servent) per il servizio specificato Nam. e        |
| \_GETSERVBYPORT GETXBYYSP    | Fornisce una struttura [**Servent**](/windows/desktop/api/winsock/ns-winsock-servent) per il servizio sulla porta specificata. |
| GETXBYYSP \_ GetHostName      | Restituisce il nome host standard per il computer locale.                                   |



 

Funzioni di stile asincrono



| Nome della funzione SPI                   | Descrizione                                                                              |
|-------------------------------------|------------------------------------------------------------------------------------------|
| \_WSAASYNCGETHOSTBYADDR GETXBYYSP    | Fornisce una struttura [**hostent**](/windows/desktop/api/winsock/ns-winsock-hostent) per l'indirizzo host specificato.        |
| \_WSAASYNCGETHOSTBYNAME GETXBYYSP    | Fornisce una struttura [**hostent**](/windows/desktop/api/winsock/ns-winsock-hostent) per il nome host specificato.           |
| \_WSAASYNCGETPROTOBYNAME GETXBYYSP   | Fornisce una struttura [**protoent**](/windows/desktop/api/winsock/ns-winsock-protoent) per il nome di protocollo specificato.     |
| \_WSAASYNCGETPROTOBYNUMBER GETXBYYSP | Fornisce una struttura [**protoent**](/windows/desktop/api/winsock/ns-winsock-protoent) per il numero di protocollo specificato.   |
| \_WSAASYNCGETSERVBYNAME GETXBYYSP    | Fornisce una struttura [**Servent**](/windows/desktop/api/winsock/ns-winsock-servent) per il nome del servizio specificato.        |
| \_WSAASYNCGETSERVBYPORT GETXBYYSP    | Fornisce una struttura [**Servent**](/windows/desktop/api/winsock/ns-winsock-servent) per il servizio sulla porta specificata. |
| \_WSACANCELASYNCREQUEST GETXBYYSP    | Annulla un'operazione **GetXbyY** asincrona.                                           |



 

La sintassi e la semantica di queste funzioni **GetXbyY** in SPI sono esattamente le stesse di quelle documentate nella specifica API e, pertanto, non vengono ripetute qui.

La DLL di Windows Sockets 2 consente esattamente a un provider di servizi di offrire questi servizi. Non è pertanto necessario includere i puntatori a queste funzioni nella tabella delle procedure ricevuta dai provider di servizi all'avvio. Negli ambienti Windows il percorso della DLL che implementa queste funzioni viene recuperato dal valore trovato nel seguente percorso del registro di sistema. Questa voce del registro di sistema non esiste per impostazione predefinita:

**HKEY \_ \_Computer locale** \\ **sistema** \\ **CurrentControlSet** \\ **Servizi** \\ **WinSock2** \\ **parametri** \\ **GetXByYLibraryPath**

## <a name="built-in-default-getxbyy-service-provider"></a>Built-In provider di servizi GetXbyY predefinito

Un provider di servizi **GetXbyY** predefinito è integrato nei componenti della fase di esecuzione standard di Windows Sockets 2. Questo provider predefinito implementa tutte le funzioni descritte in precedenza, pertanto non è necessario che queste funzioni vengano implementate da alcun provider dello spazio dei nomi. Tuttavia, un provider dello spazio dei nomi è libero di fornire una o tutte le funzioni (e di conseguenza eseguire l'override delle impostazioni predefinite) semplicemente archiviando la stringa che rappresenta il percorso della DLL che implementa queste funzioni nella chiave del registro di sistema indicata. Le funzioni **GetXbyY** non esportate dalla dll del provider denominato verranno fornite tramite le impostazioni predefinite predefinite. Si noti, tuttavia, che se un provider sceglie di fornire una qualsiasi versione asincrona delle funzioni **GetXbyY** , deve fornire tutte le funzioni asincrone in modo che l'operazione di annullamento funzioni correttamente.

L'implementazione corrente del provider di servizi **GetXbyY** predefinito risiede all'interno del Wsock32.dll. A seconda del modo in cui sono state stabilite le impostazioni TCP/IP tramite il pannello di controllo, la risoluzione dei nomi viene eseguita utilizzando i file host DNS o locali. Quando si usa DNS, il provider di servizi **GetXbyY** predefinito usa le chiamate API standard di Windows sockets 1,1 per comunicare con il server DNS. Queste transazioni vengono eseguite utilizzando qualsiasi stack TCP/IP configurato come lo stack TCP/IP predefinito. Tuttavia, due casi particolari meritano una menzione speciale.

L'implementazione predefinita di GETXBYYSP \_ GetHostName ottiene il nome host locale dal registro di sistema. Corrisponderà al nome assegnato a "Computer locale". L'implementazione predefinita di GETXBYYSP \_ gethostbyname e GETXBYYSP \_ WSAAsyncGetHostByName confronta sempre il nome host specificato con il nome host locale. Se corrispondono, l'implementazione predefinita usa un'interfaccia privata per eseguire il probe dello stack TCP/IP Microsoft per individuare l'indirizzo IP locale. Pertanto, per essere completamente indipendenti dallo stack Microsoft TCP/IP, un provider dello spazio dei nomi deve implementare GETXBYYSP \_ gethostbyname e GETXBYYSP \_ WSAAsyncGetHostByName.

 

 



