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
# <a name="summary-of-name-resolution-functions"></a><span data-ttu-id="2af2b-103">Riepilogo delle funzioni di risoluzione dei nomi</span><span class="sxs-lookup"><span data-stu-id="2af2b-103">Summary of Name Resolution Functions</span></span>

<span data-ttu-id="2af2b-104">Le funzioni di risoluzione dei nomi possono essere raggruppate in tre categorie: installazione del servizio, query client e helper (con macro).</span><span class="sxs-lookup"><span data-stu-id="2af2b-104">The name resolution functions can be grouped into three categories: Service installation, client queries, and helper (with macros).</span></span> <span data-ttu-id="2af2b-105">Le sezioni che seguono identificano le funzioni in ogni categoria e ne descrivono brevemente l'utilizzo previsto.</span><span class="sxs-lookup"><span data-stu-id="2af2b-105">The sections that follow identify the functions in each category and briefly describe their intended use.</span></span> <span data-ttu-id="2af2b-106">Sono descritte anche le strutture di dati chiave.</span><span class="sxs-lookup"><span data-stu-id="2af2b-106">Key data structures are also described.</span></span>

## <a name="service-installation"></a><span data-ttu-id="2af2b-107">Installazione del servizio</span><span class="sxs-lookup"><span data-stu-id="2af2b-107">Service Installation</span></span>

-   [<span data-ttu-id="2af2b-108">**WSAInstallServiceClass**</span><span class="sxs-lookup"><span data-stu-id="2af2b-108">**WSAInstallServiceClass**</span></span>](/windows/desktop/api/Winsock2/nf-winsock2-wsainstallserviceclassa)
-   [<span data-ttu-id="2af2b-109">**WSARemoveServiceClass**</span><span class="sxs-lookup"><span data-stu-id="2af2b-109">**WSARemoveServiceClass**</span></span>](/windows/desktop/api/Winsock2/nf-winsock2-wsaremoveserviceclass)
-   [<span data-ttu-id="2af2b-110">**WSASetService**</span><span class="sxs-lookup"><span data-stu-id="2af2b-110">**WSASetService**</span></span>](/windows/desktop/api/Winsock2/nf-winsock2-wsasetservicea)

<span data-ttu-id="2af2b-111">Quando la classe di servizio necessaria non esiste già, un'applicazione usa [**WSAInstallServiceClass**](/windows/desktop/api/Winsock2/nf-winsock2-wsainstallserviceclassa) per installare una nuova classe di servizio fornendo un nome di classe del servizio, un GUID per l'identificatore della classe del servizio e una serie di strutture [**WSANSCLASSINFO**](/windows/desktop/api/Winsock2/ns-winsock2-wsansclassinfow) .</span><span class="sxs-lookup"><span data-stu-id="2af2b-111">When the required service class does not already exist, an application uses [**WSAInstallServiceClass**](/windows/desktop/api/Winsock2/nf-winsock2-wsainstallserviceclassa) to install a new service class by supplying a service class name, a GUID for the service class identifier, and a series of [**WSANSCLASSINFO**](/windows/desktop/api/Winsock2/ns-winsock2-wsansclassinfow) structures.</span></span> <span data-ttu-id="2af2b-112">Queste strutture sono ognuna specifiche di un determinato spazio dei nomi e forniscono valori comuni, ad esempio i numeri di porta TCP consigliati o gli identificatori SAP NetWare.</span><span class="sxs-lookup"><span data-stu-id="2af2b-112">These structures are each specific to a particular namespace, and supply common values such as recommended TCP port numbers or NetWare SAP Identifiers.</span></span> <span data-ttu-id="2af2b-113">Una classe di servizio può essere rimossa chiamando [**WSARemoveServiceClass**](/windows/desktop/api/Winsock2/nf-winsock2-wsaremoveserviceclass) e specificando il GUID corrispondente all'identificatore di classe.</span><span class="sxs-lookup"><span data-stu-id="2af2b-113">A service class can be removed by calling [**WSARemoveServiceClass**](/windows/desktop/api/Winsock2/nf-winsock2-wsaremoveserviceclass) and supplying the GUID corresponding to the class identifier.</span></span>

<span data-ttu-id="2af2b-114">Una volta esistente una classe del servizio, è possibile installare o rimuovere istanze specifiche di un servizio tramite [**WSASetService**](/windows/desktop/api/Winsock2/nf-winsock2-wsasetservicea).</span><span class="sxs-lookup"><span data-stu-id="2af2b-114">Once a service class exists, specific instances of a service can be installed or removed through [**WSASetService**](/windows/desktop/api/Winsock2/nf-winsock2-wsasetservicea).</span></span> <span data-ttu-id="2af2b-115">Questa funzione accetta una struttura [**WSAQUERYSET**](/windows/desktop/api/Winsock2/ns-winsock2-wsaquerysetw) come parametro di input insieme a un codice operativo e ai flag dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="2af2b-115">This function takes a [**WSAQUERYSET**](/windows/desktop/api/Winsock2/ns-winsock2-wsaquerysetw) structure as an input parameter along with an operation code and operation flags.</span></span> <span data-ttu-id="2af2b-116">Il codice dell'operazione indica se il servizio viene installato o rimosso.</span><span class="sxs-lookup"><span data-stu-id="2af2b-116">The operation code indicates whether the service is being installed or removed.</span></span> <span data-ttu-id="2af2b-117">La struttura **WSAQUERYSET** fornisce tutte le informazioni rilevanti sul servizio, tra cui l'identificatore della classe del servizio, il nome del servizio (per questa istanza), l'identificatore dello spazio dei nomi e le informazioni sul protocollo applicabili e un set di indirizzi di trasporto in ascolto del servizio.</span><span class="sxs-lookup"><span data-stu-id="2af2b-117">The **WSAQUERYSET** structure provides all of the relevant information about the service including service class identifier, service name (for this instance), applicable namespace identifier and protocol information, and a set of transport addresses at which the service listens.</span></span> <span data-ttu-id="2af2b-118">I servizi devono richiamare **WSASetService** quando vengono inizializzati per annunciare la loro presenza negli spazi dei nomi dinamici.</span><span class="sxs-lookup"><span data-stu-id="2af2b-118">Services should invoke **WSASetService** when they initialize to advertise their presence in dynamic namespaces.</span></span>

## <a name="client-query"></a><span data-ttu-id="2af2b-119">Query client</span><span class="sxs-lookup"><span data-stu-id="2af2b-119">Client Query</span></span>

-   [<span data-ttu-id="2af2b-120">**WSAEnumNameSpaceProviders**</span><span class="sxs-lookup"><span data-stu-id="2af2b-120">**WSAEnumNameSpaceProviders**</span></span>](/windows/desktop/api/Winsock2/nf-winsock2-wsaenumnamespaceprovidersa)
-   [<span data-ttu-id="2af2b-121">**WSALookupServiceBegin**</span><span class="sxs-lookup"><span data-stu-id="2af2b-121">**WSALookupServiceBegin**</span></span>](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicebegina)
-   [<span data-ttu-id="2af2b-122">**WSALookupServiceNext**</span><span class="sxs-lookup"><span data-stu-id="2af2b-122">**WSALookupServiceNext**</span></span>](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicenexta)
-   [<span data-ttu-id="2af2b-123">**WSALookupServiceEnd**</span><span class="sxs-lookup"><span data-stu-id="2af2b-123">**WSALookupServiceEnd**</span></span>](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupserviceend)

<span data-ttu-id="2af2b-124">La funzione [**WSAEnumNameSpaceProviders**](/windows/desktop/api/Winsock2/nf-winsock2-wsaenumnamespaceprovidersa) consente a un'applicazione di individuare gli spazi dei nomi accessibili tramite le funzionalità di risoluzione dei nomi Winsock.</span><span class="sxs-lookup"><span data-stu-id="2af2b-124">The [**WSAEnumNameSpaceProviders**](/windows/desktop/api/Winsock2/nf-winsock2-wsaenumnamespaceprovidersa) function allows an application to discover which namespaces are accessible through Winsock name resolution facilities.</span></span> <span data-ttu-id="2af2b-125">Consente inoltre a un'applicazione di determinare se un determinato spazio dei nomi è supportato da più di un provider dello spazio dei nomi e di individuare l'identificatore del provider per un determinato provider dello spazio dei nomi.</span><span class="sxs-lookup"><span data-stu-id="2af2b-125">It also allows an application to determine whether a given namespace is supported by more than one namespace provider, and to discover the provider identifier for any particular namespace provider.</span></span> <span data-ttu-id="2af2b-126">Utilizzando un identificatore di provider, l'applicazione può limitare un'operazione di query a un provider dello spazio dei nomi specificato.</span><span class="sxs-lookup"><span data-stu-id="2af2b-126">Using a provider identifier, the application can restrict a query operation to a specified namespace provider.</span></span>

<span data-ttu-id="2af2b-127">Spazio dei nomi Winsock: le operazioni di query coinvolgono una serie di chiamate: [**WSALookupServiceBegin**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicebegina), seguite da una o più chiamate a [**WSALookupServiceNext**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicenexta) e terminano con una chiamata a [**WSALookupServiceEnd**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupserviceend).</span><span class="sxs-lookup"><span data-stu-id="2af2b-127">Winsock namespace–query operations involve a series of calls: [**WSALookupServiceBegin**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicebegina), followed by one or more calls to [**WSALookupServiceNext**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicenexta) and ending with a call to [**WSALookupServiceEnd**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupserviceend).</span></span> <span data-ttu-id="2af2b-128">**WSALookupServiceBegin** accetta una struttura [**WSAQUERYSET**](/windows/desktop/api/Winsock2/ns-winsock2-wsaquerysetw) come input per definire i parametri di query insieme a un set di flag per fornire un controllo aggiuntivo sull'operazione di ricerca.</span><span class="sxs-lookup"><span data-stu-id="2af2b-128">**WSALookupServiceBegin** takes a [**WSAQUERYSET**](/windows/desktop/api/Winsock2/ns-winsock2-wsaquerysetw) structure as input to define the query parameters along with a set of flags to provide additional control over the search operation.</span></span> <span data-ttu-id="2af2b-129">Restituisce un handle di query che viene usato nelle chiamate successive a **WSALookupServiceNext** e **WSALookupServiceEnd**.</span><span class="sxs-lookup"><span data-stu-id="2af2b-129">It returns a query handle which is used in the subsequent calls to **WSALookupServiceNext** and **WSALookupServiceEnd**.</span></span>

<span data-ttu-id="2af2b-130">L'applicazione richiama [**WSALookupServiceNext**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicenexta) per ottenere i risultati della query, con i risultati forniti in un buffer [**WSAQUERYSET**](/windows/desktop/api/Winsock2/ns-winsock2-wsaquerysetw) fornito dall'applicazione.</span><span class="sxs-lookup"><span data-stu-id="2af2b-130">The application invokes [**WSALookupServiceNext**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicenexta) to obtain query results, with results supplied in an application-supplied [**WSAQUERYSET**](/windows/desktop/api/Winsock2/ns-winsock2-wsaquerysetw) buffer.</span></span> <span data-ttu-id="2af2b-131">L'applicazione continua a chiamare **WSALookupServiceNext** fino a quando \_ non viene restituito il codice di errore WSA E \_ , a \_ indicare che tutti i risultati sono stati recuperati.</span><span class="sxs-lookup"><span data-stu-id="2af2b-131">The application continues to call **WSALookupServiceNext** until the error code WSA\_E\_NO\_MORE is returned indicating that all results have been retrieved.</span></span> <span data-ttu-id="2af2b-132">La ricerca viene quindi terminata da una chiamata a [**WSALookupServiceEnd**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupserviceend).</span><span class="sxs-lookup"><span data-stu-id="2af2b-132">The search is then terminated by a call to [**WSALookupServiceEnd**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupserviceend).</span></span> <span data-ttu-id="2af2b-133">La funzione **WSALookupServiceEnd** può essere usata anche per annullare un **WSALookupServiceNext** attualmente in sospeso quando viene chiamato da un altro thread.</span><span class="sxs-lookup"><span data-stu-id="2af2b-133">The **WSALookupServiceEnd** function can also be used to cancel a currently pending **WSALookupServiceNext** when called from another thread.</span></span>

<span data-ttu-id="2af2b-134">In Windows Sockets 2, i codici di errore in conflitto vengono definiti per WSAENOMORE (10102) e WSA \_ e \_ non \_ più (10110).</span><span class="sxs-lookup"><span data-stu-id="2af2b-134">In Windows Sockets 2, conflicting error codes are defined for WSAENOMORE (10102) and WSA\_E\_NO\_MORE (10110).</span></span> <span data-ttu-id="2af2b-135">Il codice di errore WSAENOMORE verrà rimosso in una versione futura e solo WSA \_ e \_ non \_ rimarrà più.</span><span class="sxs-lookup"><span data-stu-id="2af2b-135">The error code WSAENOMORE will be removed in a future version and only WSA\_E\_NO\_MORE will remain.</span></span> <span data-ttu-id="2af2b-136">Per Windows Sockets 2, tuttavia, le applicazioni devono verificare sia WSAENOMORE che WSA e \_ \_ non \_ più per la compatibilità più ampia possibile con i provider dello spazio dei nomi che usano uno di questi due.</span><span class="sxs-lookup"><span data-stu-id="2af2b-136">For Windows Sockets 2, however, applications should check for both WSAENOMORE and WSA\_E\_NO\_MORE for the widest possible compatibility with namespace providers that use either one.</span></span>

## <a name="helper-functions"></a><span data-ttu-id="2af2b-137">Funzioni di supporto</span><span class="sxs-lookup"><span data-stu-id="2af2b-137">Helper Functions</span></span>

-   [<span data-ttu-id="2af2b-138">**WSAGetServiceClassNameByClassId**</span><span class="sxs-lookup"><span data-stu-id="2af2b-138">**WSAGetServiceClassNameByClassId**</span></span>](/windows/desktop/api/Winsock2/nf-winsock2-wsagetserviceclassnamebyclassida)
-   [<span data-ttu-id="2af2b-139">**WSAAddressToString**</span><span class="sxs-lookup"><span data-stu-id="2af2b-139">**WSAAddressToString**</span></span>](/windows/desktop/api/Winsock2/nf-winsock2-wsaaddresstostringa)
-   [<span data-ttu-id="2af2b-140">**WSAStringToAddress non**</span><span class="sxs-lookup"><span data-stu-id="2af2b-140">**WSAStringToAddress**</span></span>](/windows/desktop/api/Winsock2/nf-winsock2-wsastringtoaddressa)
-   [<span data-ttu-id="2af2b-141">**WSAGetServiceClassInfo**</span><span class="sxs-lookup"><span data-stu-id="2af2b-141">**WSAGetServiceClassInfo**</span></span>](/windows/desktop/api/Winsock2/nf-winsock2-wsagetserviceclassinfoa)

<span data-ttu-id="2af2b-142">Le funzioni di supporto per la risoluzione dei nomi includono una funzione per recuperare un nome di classe del servizio, dato un identificatore di classe del servizio, una coppia di funzioni usate per convertire un indirizzo di trasporto tra una struttura [**sockaddr**](sockaddr-2.md) e una rappresentazione di stringa ASCII, una funzione per recuperare le informazioni sullo schema della classe di servizio per una determinata classe di servizio e un set di macro per il mapping di servizi noti</span><span class="sxs-lookup"><span data-stu-id="2af2b-142">The name resolution helper functions include a function to retrieve a service class name given a service class identifier, a pair of functions used to translate a transport address between a [**SOCKADDR**](sockaddr-2.md) structure and an ASCII string representation, a function to retrieve the service class schema information for a given service class, and a set of macros for mapping well known services to preallocated GUIDs.</span></span>

<span data-ttu-id="2af2b-143">Le macro seguenti di Winsock2. h facilitano il mapping tra le classi di servizi note e gli spazi dei nomi seguenti:</span><span class="sxs-lookup"><span data-stu-id="2af2b-143">The following macros from Winsock2.h aid in mapping between well known service classes and these namespaces:</span></span>

| <span data-ttu-id="2af2b-144">Macro</span><span class="sxs-lookup"><span data-stu-id="2af2b-144">Macro</span></span>                                                                                                            | <span data-ttu-id="2af2b-145">Descrizione</span><span class="sxs-lookup"><span data-stu-id="2af2b-145">Description</span></span>                                                                                                                |
|------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2af2b-146">SVCID \_ TCP (porta) SVCID \_ UDP (porta)</span><span class="sxs-lookup"><span data-stu-id="2af2b-146">SVCID\_TCP(Port) SVCID\_UDP(Port)</span></span><br/> <span data-ttu-id="2af2b-147">SVCID \_ NetWare (tipo di oggetto)</span><span class="sxs-lookup"><span data-stu-id="2af2b-147">SVCID\_NETWARE(Object Type)</span></span><br/>                              | <span data-ttu-id="2af2b-148">Data una porta per TCP/IP o UDP/IP o il tipo di oggetto nel caso di NetWare, restituisce il GUID (numero di porta in ordine host).</span><span class="sxs-lookup"><span data-stu-id="2af2b-148">Given a port for TCP/IP or UDP/IP or the object type in the case of NetWare, returns the GUID (port number in host order).</span></span> |
| <span data-ttu-id="2af2b-149">\_SVCID \_ TCP (Guid) è \_ SVCID \_ UDP (Guid)</span><span class="sxs-lookup"><span data-stu-id="2af2b-149">IS\_SVCID\_TCP(GUID)IS\_SVCID\_UDP(GUID)</span></span><br/> <span data-ttu-id="2af2b-150">è \_ SVCID \_ NetWare (Guid)</span><span class="sxs-lookup"><span data-stu-id="2af2b-150">IS\_SVCID\_NETWARE(GUID)</span></span><br/>                          | <span data-ttu-id="2af2b-151">Restituisce **true** se il GUID è compreso nell'intervallo consentito.</span><span class="sxs-lookup"><span data-stu-id="2af2b-151">Returns **TRUE** if the GUID is within the allowable range.</span></span>                                                                |
| <span data-ttu-id="2af2b-152">SET \_ TCP \_ SVCID (Guid, porta) set \_ UDP \_ SVCID (Guid, Port)</span><span class="sxs-lookup"><span data-stu-id="2af2b-152">SET\_TCP\_SVCID(GUID, port)SET\_UDP\_SVCID(GUID, port)</span></span><br/>                                                | <span data-ttu-id="2af2b-153">Inizializza una struttura GUID con l'equivalente GUID per un numero di porta TCP o UDP. il numero di porta deve essere in ordine host.</span><span class="sxs-lookup"><span data-stu-id="2af2b-153">Initializes a GUID structure with the GUID equivalent for a TCP or UDP port number (port number must be in host order).</span></span>    |
| <span data-ttu-id="2af2b-154">PORTA \_ dalla \_ \_ porta TCP (Guid) SVCID \_ da \_ SVCID \_ UDP (Guid)</span><span class="sxs-lookup"><span data-stu-id="2af2b-154">PORT\_FROM\_SVCID\_TCP(GUID)PORT\_FROM\_SVCID\_UDP(GUID)</span></span><br/> <span data-ttu-id="2af2b-155">SAPIDO \_ da \_ SVCID \_ NetWare (Guid)</span><span class="sxs-lookup"><span data-stu-id="2af2b-155">SAPID\_FROM\_SVCID\_NETWARE(GUID)</span></span><br/> | <span data-ttu-id="2af2b-156">Restituisce la porta o il tipo di oggetto associato al GUID (numero di porta in ordine host).</span><span class="sxs-lookup"><span data-stu-id="2af2b-156">Returns the port or object type associated with the GUID (port number in host order).</span></span>                                      |



 

## <a name="related-topics"></a><span data-ttu-id="2af2b-157">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="2af2b-157">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2af2b-158">**funzione getaddrinfo**</span><span class="sxs-lookup"><span data-stu-id="2af2b-158">**getaddrinfo**</span></span>](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo)
</dt> <dt>

[<span data-ttu-id="2af2b-159">**GetAddrInfoEx**</span><span class="sxs-lookup"><span data-stu-id="2af2b-159">**GetAddrInfoEx**</span></span>](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfoexa)
</dt> <dt>

[<span data-ttu-id="2af2b-160">**GetAddrInfoW**</span><span class="sxs-lookup"><span data-stu-id="2af2b-160">**GetAddrInfoW**</span></span>](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfow)
</dt> <dt>

[<span data-ttu-id="2af2b-161">**GetNameInfo**</span><span class="sxs-lookup"><span data-stu-id="2af2b-161">**getnameinfo**</span></span>](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getnameinfo)
</dt> <dt>

[<span data-ttu-id="2af2b-162">**GetNameInfoW**</span><span class="sxs-lookup"><span data-stu-id="2af2b-162">**GetNameInfoW**</span></span>](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getnameinfow)
</dt> <dt>

[<span data-ttu-id="2af2b-163">Strutture dei dati di risoluzione dei nomi</span><span class="sxs-lookup"><span data-stu-id="2af2b-163">Name Resolution Data Structures</span></span>](name-resolution-data-structures-2.md)
</dt> <dt>

[<span data-ttu-id="2af2b-164">Modello di risoluzione dei nomi</span><span class="sxs-lookup"><span data-stu-id="2af2b-164">Name Resolution Model</span></span>](name-resolution-model-2.md)
</dt> <dt>

[<span data-ttu-id="2af2b-165">Risoluzione dei nomi indipendente dal protocollo</span><span class="sxs-lookup"><span data-stu-id="2af2b-165">Protocol-Independent Name Resolution</span></span>](protocol-independent-name-resolution-2.md)
</dt> <dt>

[<span data-ttu-id="2af2b-166">Registrazione e risoluzione dei nomi</span><span class="sxs-lookup"><span data-stu-id="2af2b-166">Registration and Name Resolution</span></span>](registration-and-name-resolution-2.md)
</dt> <dt>

[<span data-ttu-id="2af2b-167">**SOCKADDR**</span><span class="sxs-lookup"><span data-stu-id="2af2b-167">**SOCKADDR**</span></span>](sockaddr-2.md)
</dt> <dt>

[<span data-ttu-id="2af2b-168">**WSAEnumNameSpaceProviders**</span><span class="sxs-lookup"><span data-stu-id="2af2b-168">**WSAEnumNameSpaceProviders**</span></span>](/windows/desktop/api/Winsock2/nf-winsock2-wsaenumnamespaceprovidersa)
</dt> <dt>

[<span data-ttu-id="2af2b-169">**WSAGetServiceClassNameByClassId**</span><span class="sxs-lookup"><span data-stu-id="2af2b-169">**WSAGetServiceClassNameByClassId**</span></span>](/windows/desktop/api/Winsock2/nf-winsock2-wsagetserviceclassnamebyclassida)
</dt> <dt>

[<span data-ttu-id="2af2b-170">**WSAInstallServiceClass**</span><span class="sxs-lookup"><span data-stu-id="2af2b-170">**WSAInstallServiceClass**</span></span>](/windows/desktop/api/Winsock2/nf-winsock2-wsainstallserviceclassa)
</dt> <dt>

[<span data-ttu-id="2af2b-171">**WSALookupServiceBegin**</span><span class="sxs-lookup"><span data-stu-id="2af2b-171">**WSALookupServiceBegin**</span></span>](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicebegina)
</dt> <dt>

[<span data-ttu-id="2af2b-172">**WSALookupServiceEnd**</span><span class="sxs-lookup"><span data-stu-id="2af2b-172">**WSALookupServiceEnd**</span></span>](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupserviceend)
</dt> <dt>

[<span data-ttu-id="2af2b-173">**WSALookupServiceNext**</span><span class="sxs-lookup"><span data-stu-id="2af2b-173">**WSALookupServiceNext**</span></span>](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicenexta)
</dt> <dt>

[<span data-ttu-id="2af2b-174">**WSARemoveServiceClass**</span><span class="sxs-lookup"><span data-stu-id="2af2b-174">**WSARemoveServiceClass**</span></span>](/windows/desktop/api/Winsock2/nf-winsock2-wsaremoveserviceclass)
</dt> <dt>

[<span data-ttu-id="2af2b-175">**WSASetService**</span><span class="sxs-lookup"><span data-stu-id="2af2b-175">**WSASetService**</span></span>](/windows/desktop/api/Winsock2/nf-winsock2-wsasetservicea)
</dt> <dt>

[<span data-ttu-id="2af2b-176">**WSAQUERYSET**</span><span class="sxs-lookup"><span data-stu-id="2af2b-176">**WSAQUERYSET**</span></span>](/windows/desktop/api/Winsock2/ns-winsock2-wsaquerysetw)
</dt> <dt>

[<span data-ttu-id="2af2b-177">**WSANSCLASSINFO**</span><span class="sxs-lookup"><span data-stu-id="2af2b-177">**WSANSCLASSINFO**</span></span>](/windows/desktop/api/Winsock2/ns-winsock2-wsansclassinfow)
</dt> </dl>

 

 




