---
description: 'Le funzioni di risoluzione dei nomi possono essere raggruppate in tre categorie: installazione del servizio, query client e helper (con macro).'
ms.assetid: c16a7163-11f5-4ad6-9df1-9bad2a964e48
title: Riepilogo delle funzioni di risoluzione dei nomi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d5969cb2cf145124446374dcb86eb1e0a8a837c5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103751399"
---
# <a name="summary-of-name-resolution-functions"></a>Riepilogo delle funzioni di risoluzione dei nomi

Le funzioni di risoluzione dei nomi possono essere raggruppate in tre categorie: installazione del servizio, query client e helper (con macro). Le sezioni che seguono identificano le funzioni in ogni categoria e ne descrivono brevemente l'utilizzo previsto. Sono descritte anche le strutture di dati chiave.

## <a name="service-installation"></a>Installazione del servizio

-   [**WSAInstallServiceClass**](/windows/desktop/api/Winsock2/nf-winsock2-wsainstallserviceclassa)
-   [**WSARemoveServiceClass**](/windows/desktop/api/Winsock2/nf-winsock2-wsaremoveserviceclass)
-   [**WSASetService**](/windows/desktop/api/Winsock2/nf-winsock2-wsasetservicea)

Quando la classe di servizio necessaria non esiste già, un'applicazione usa [**WSAInstallServiceClass**](/windows/desktop/api/Winsock2/nf-winsock2-wsainstallserviceclassa) per installare una nuova classe di servizio fornendo un nome di classe del servizio, un GUID per l'identificatore della classe del servizio e una serie di strutture [**WSANSCLASSINFO**](/windows/desktop/api/Winsock2/ns-winsock2-wsansclassinfow) . Queste strutture sono ognuna specifiche di un determinato spazio dei nomi e forniscono valori comuni, ad esempio i numeri di porta TCP consigliati o gli identificatori SAP NetWare. Una classe di servizio può essere rimossa chiamando [**WSARemoveServiceClass**](/windows/desktop/api/Winsock2/nf-winsock2-wsaremoveserviceclass) e specificando il GUID corrispondente all'identificatore di classe.

Una volta esistente una classe del servizio, è possibile installare o rimuovere istanze specifiche di un servizio tramite [**WSASetService**](/windows/desktop/api/Winsock2/nf-winsock2-wsasetservicea). Questa funzione accetta una struttura [**WSAQUERYSET**](/windows/desktop/api/Winsock2/ns-winsock2-wsaquerysetw) come parametro di input insieme a un codice operativo e ai flag dell'operazione. Il codice dell'operazione indica se il servizio viene installato o rimosso. La struttura **WSAQUERYSET** fornisce tutte le informazioni rilevanti sul servizio, tra cui l'identificatore della classe del servizio, il nome del servizio (per questa istanza), l'identificatore dello spazio dei nomi e le informazioni sul protocollo applicabili e un set di indirizzi di trasporto in ascolto del servizio. I servizi devono richiamare **WSASetService** quando vengono inizializzati per annunciare la loro presenza negli spazi dei nomi dinamici.

## <a name="client-query"></a>Query client

-   [**WSAEnumNameSpaceProviders**](/windows/desktop/api/Winsock2/nf-winsock2-wsaenumnamespaceprovidersa)
-   [**WSALookupServiceBegin**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicebegina)
-   [**WSALookupServiceNext**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicenexta)
-   [**WSALookupServiceEnd**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupserviceend)

La funzione [**WSAEnumNameSpaceProviders**](/windows/desktop/api/Winsock2/nf-winsock2-wsaenumnamespaceprovidersa) consente a un'applicazione di individuare gli spazi dei nomi accessibili tramite le funzionalità di risoluzione dei nomi Winsock. Consente inoltre a un'applicazione di determinare se un determinato spazio dei nomi è supportato da più di un provider dello spazio dei nomi e di individuare l'identificatore del provider per un determinato provider dello spazio dei nomi. Utilizzando un identificatore di provider, l'applicazione può limitare un'operazione di query a un provider dello spazio dei nomi specificato.

Spazio dei nomi Winsock: le operazioni di query coinvolgono una serie di chiamate: [**WSALookupServiceBegin**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicebegina), seguite da una o più chiamate a [**WSALookupServiceNext**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicenexta) e terminano con una chiamata a [**WSALookupServiceEnd**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupserviceend). **WSALookupServiceBegin** accetta una struttura [**WSAQUERYSET**](/windows/desktop/api/Winsock2/ns-winsock2-wsaquerysetw) come input per definire i parametri di query insieme a un set di flag per fornire un controllo aggiuntivo sull'operazione di ricerca. Restituisce un handle di query che viene usato nelle chiamate successive a **WSALookupServiceNext** e **WSALookupServiceEnd**.

L'applicazione richiama [**WSALookupServiceNext**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicenexta) per ottenere i risultati della query, con i risultati forniti in un buffer [**WSAQUERYSET**](/windows/desktop/api/Winsock2/ns-winsock2-wsaquerysetw) fornito dall'applicazione. L'applicazione continua a chiamare **WSALookupServiceNext** fino a quando \_ non viene restituito il codice di errore WSA E \_ , a \_ indicare che tutti i risultati sono stati recuperati. La ricerca viene quindi terminata da una chiamata a [**WSALookupServiceEnd**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupserviceend). La funzione **WSALookupServiceEnd** può essere usata anche per annullare un **WSALookupServiceNext** attualmente in sospeso quando viene chiamato da un altro thread.

In Windows Sockets 2, i codici di errore in conflitto vengono definiti per WSAENOMORE (10102) e WSA \_ e \_ non \_ più (10110). Il codice di errore WSAENOMORE verrà rimosso in una versione futura e solo WSA \_ e \_ non \_ rimarrà più. Per Windows Sockets 2, tuttavia, le applicazioni devono verificare sia WSAENOMORE che WSA e \_ \_ non \_ più per la compatibilità più ampia possibile con i provider dello spazio dei nomi che usano uno di questi due.

## <a name="helper-functions"></a>Funzioni di supporto

-   [**WSAGetServiceClassNameByClassId**](/windows/desktop/api/Winsock2/nf-winsock2-wsagetserviceclassnamebyclassida)
-   [**WSAAddressToString**](/windows/desktop/api/Winsock2/nf-winsock2-wsaaddresstostringa)
-   [**WSAStringToAddress non**](/windows/desktop/api/Winsock2/nf-winsock2-wsastringtoaddressa)
-   [**WSAGetServiceClassInfo**](/windows/desktop/api/Winsock2/nf-winsock2-wsagetserviceclassinfoa)

Le funzioni di supporto per la risoluzione dei nomi includono una funzione per recuperare un nome di classe del servizio, dato un identificatore di classe del servizio, una coppia di funzioni usate per convertire un indirizzo di trasporto tra una struttura [**sockaddr**](sockaddr-2.md) e una rappresentazione di stringa ASCII, una funzione per recuperare le informazioni sullo schema della classe di servizio per una determinata classe di servizio e un set di macro per il mapping di servizi noti

Le macro seguenti di Winsock2. h facilitano il mapping tra le classi di servizi note e gli spazi dei nomi seguenti:

| Macro                                                                                                            | Descrizione                                                                                                                |
|------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| SVCID \_ TCP (porta) SVCID \_ UDP (porta)<br/> SVCID \_ NetWare (tipo di oggetto)<br/>                              | Data una porta per TCP/IP o UDP/IP o il tipo di oggetto nel caso di NetWare, restituisce il GUID (numero di porta in ordine host). |
| \_SVCID \_ TCP (Guid) è \_ SVCID \_ UDP (Guid)<br/> è \_ SVCID \_ NetWare (Guid)<br/>                          | Restituisce **true** se il GUID è compreso nell'intervallo consentito.                                                                |
| SET \_ TCP \_ SVCID (Guid, porta) set \_ UDP \_ SVCID (Guid, Port)<br/>                                                | Inizializza una struttura GUID con l'equivalente GUID per un numero di porta TCP o UDP. il numero di porta deve essere in ordine host.    |
| PORTA \_ dalla \_ \_ porta TCP (Guid) SVCID \_ da \_ SVCID \_ UDP (Guid)<br/> SAPIDO \_ da \_ SVCID \_ NetWare (Guid)<br/> | Restituisce la porta o il tipo di oggetto associato al GUID (numero di porta in ordine host).                                      |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**funzione getaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo)
</dt> <dt>

[**GetAddrInfoEx**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfoexa)
</dt> <dt>

[**GetAddrInfoW**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfow)
</dt> <dt>

[**GetNameInfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getnameinfo)
</dt> <dt>

[**GetNameInfoW**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getnameinfow)
</dt> <dt>

[Strutture dei dati di risoluzione dei nomi](name-resolution-data-structures-2.md)
</dt> <dt>

[Modello di risoluzione dei nomi](name-resolution-model-2.md)
</dt> <dt>

[Risoluzione dei nomi indipendente dal protocollo](protocol-independent-name-resolution-2.md)
</dt> <dt>

[Registrazione e risoluzione dei nomi](registration-and-name-resolution-2.md)
</dt> <dt>

[**SOCKADDR**](sockaddr-2.md)
</dt> <dt>

[**WSAEnumNameSpaceProviders**](/windows/desktop/api/Winsock2/nf-winsock2-wsaenumnamespaceprovidersa)
</dt> <dt>

[**WSAGetServiceClassNameByClassId**](/windows/desktop/api/Winsock2/nf-winsock2-wsagetserviceclassnamebyclassida)
</dt> <dt>

[**WSAInstallServiceClass**](/windows/desktop/api/Winsock2/nf-winsock2-wsainstallserviceclassa)
</dt> <dt>

[**WSALookupServiceBegin**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicebegina)
</dt> <dt>

[**WSALookupServiceEnd**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupserviceend)
</dt> <dt>

[**WSALookupServiceNext**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicenexta)
</dt> <dt>

[**WSARemoveServiceClass**](/windows/desktop/api/Winsock2/nf-winsock2-wsaremoveserviceclass)
</dt> <dt>

[**WSASetService**](/windows/desktop/api/Winsock2/nf-winsock2-wsasetservicea)
</dt> <dt>

[**WSAQUERYSET**](/windows/desktop/api/Winsock2/ns-winsock2-wsaquerysetw)
</dt> <dt>

[**WSANSCLASSINFO**](/windows/desktop/api/Winsock2/ns-winsock2-wsansclassinfow)
</dt> </dl>

 

 




