---
description: Per ottenere la notifica di reti logiche Invalidate, utilizzare la funzione WSANSPIoctl per registrare gli eventi di modifica del percorso di rete.
ms.assetid: 531b6269-5f35-44c1-ad0f-c5f103029893
title: Esecuzione di query su NLA
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0ac7a4f57e14bb967b04d3a9fd6fe66717da3878
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106310457"
---
# <a name="querying-nla"></a>Esecuzione di query su NLA

Per ottenere la notifica di reti logiche Invalidate, utilizzare la funzione [**WSANSPIoctl**](/windows/desktop/api/Winsock2/nf-winsock2-wsanspioctl) per registrare gli eventi di modifica del percorso di rete. È possibile utilizzare due metodi per determinare se un percorso di rete valido in precedenza non è più valido: metodi di polling o notifica mediante I/O sovrapposti o messaggistica di Windows.

Le query vengono create utilizzando le funzioni [**WSALookupServiceBegin**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicebegina), [**WSALookupServiceNext**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicenexta) e [**WSALookupServiceEnd**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupserviceend) per enumerare tutte le reti logiche disponibili. L'uso di ciascuna di queste funzioni viene illustrato singolarmente nel resto di questa sezione, a partire dalla funzione **WSALookupServiceBegin** .

> [!Note]  
> NLA richiede il file di intestazione mswsock. h, che per impostazione predefinita non è incluso nel file Winsock2. h.

 

## <a name="step-1-initiate-the-query"></a>Passaggio 1: avviare la query

Per riferimento rapido, la funzione [**WSALookupServiceBegin**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicebegina) presenta la sintassi seguente:

``` syntax
INT WSALookupServiceBegin(
  LPWSAQUERYSET lpqsRestrictions,
  DWORD dwControlFlags,
  LPHANDLE lphLookup
);
```

NLA supporta i flag di ricerca *dwControlFlags* seguenti:

<dl> \_nome restituito \_ LUP  
LUP \_ \_ Commento restituito  
\_BLOB restituito \_ LUP  
LUP \_ restituisce \_ tutto  
LUP \_ Deep  
</dl>

Questi flag limitano i set di risultati restituiti nelle chiamate successive a [**WSALookupServiceNext**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicenexta), funzione alle reti che contengono campi del tipo specificato. Se ad esempio si specifica LUP \_ return \_ BLOB nel parametro *dwControlFlags* della chiamata di funzione [**WSALookupServiceBegin**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicebegina) , i set di risultati delle chiamate successive a **WSALookupServiceNext** vengono limitati alle reti che contengono informazioni BLOB. L'utilizzo del \_ flag LUP return \_ All equivale a specificare il \_ nome restituito LUP \_ , LUP \_ return \_ Comment e LUP \_ return \_ BLOB, ma non LUP \_ Deep.

Per una spiegazione di questi flag di ricerca, vedere la pagina di riferimento per la funzione [**WSALookupServiceBegin**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicebegina) .

L'handle di ricerca restituito da NLA nel parametro *lphLookup* è privato per NLA e non deve essere modificato. Poiché l'handle restituito è privato per NLA, le funzioni come [**WSAGetOverlappedResult**](/windows/desktop/api/Winsock2/nf-winsock2-wsagetoverlappedresult) non sono disponibili.

NLA restituisce zero al completamento, come definito nella pagina di riferimento della funzione [**WSALookupServiceBegin**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicebegina) . In caso contrario, NLA supporta i codici di errore seguenti.

| Errore                    | Significato                                                                                                                                                     |
|--------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| WSANOTINITIALISED        | Una chiamata riuscita alla funzione [**WSAStartup**](/windows/desktop/api/winsock/nf-winsock-wsastartup) per inizializzare NLA non è stata eseguita.                                                   |
| WSAEINVAL                | Uno o più parametri non sono validi oppure i parametri specificati nella chiamata di funzione si applicano a protocolli diversi da IP.                                         |
| WSASERVICE \_ non \_ trovato   | Il parametro *lpServiceClassId* della struttura [**WSAQUERYSET**](/windows/desktop/api/Winsock2/ns-winsock2-wsaquerysetw) passata nel parametro *lpqsRestrictions* contiene un GUID non valido. |
| \_dati WSANO              | Il \_ flag LUP Containers è stato specificato nel parametro *dwControlFlags* .                                                                                       |
| WSAEFAULT                | Si è verificata una violazione di accesso durante il tentativo di accedere ai parametri forniti dall'utente.                                                                            |
| WSASYSNOTREADY           | Il servizio NLA non è disponibile per l'elaborazione della richiesta.                                                                                                      |
| \_ \_ memoria insufficiente per WSA \_ | NLA o il servizio NLA non è stato in grado di allocare memoria sufficiente per elaborare la richiesta.                                                                        |



 

## <a name="step-2-perform-the-query"></a>Passaggio 2: eseguire la query

Il passaggio successivo per l'esecuzione di query su NLA richiede l'uso della funzione [**WSALookupServiceNext**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicenexta) . Per riferimento rapido, la funzione **WSALookupServiceNext** ha la sintassi seguente:

``` syntax
INT WSALookupServiceNext(
  HANDLE hLookup,
  DWORD dwControlFlags,
  LPDWORD lpdwBufferLength,
  LPWSAQUERYSET lpqsResults
);
```

Il parametro *lLookup* è l'handle di ricerca restituito dalla chiamata precedente alla funzione [**WSALookupServiceBegin**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicebegina) .

Il parametro *dwControlFlags* supporta i flag seguenti:

<dl> \_nome restituito \_ LUP  
LUP \_ \_ Commento restituito  
\_BLOB restituito \_ LUP  
LUP \_ restituisce \_ tutto  
\_FLUSHPREVIOUS LUP  
</dl>

Questi flag sono indipendenti dai flag supportati nella chiamata di funzione [**WSALookupServiceBegin**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicebegina) . Si noti che tutti i vincoli specificati nella chiamata precedente alla funzione **WSALookupServiceBegin** vincolano la ricerca; l'aggiunta di flag con la funzione [**WSALookupServiceNext**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicenexta) nel tentativo di ampliare la query oltre i vincoli specificati nella chiamata **WSALookupServiceBegin** viene ignorata automaticamente. Tuttavia, è consentito specificare un set più restrittivo di flag rispetto a quello specificato nella chiamata **WSALookupServiceBegin** .

Se la rete descritta in dettaglio in *lpqsResults* è una rete attiva, viene aggiunta una serie di strutture **\_ BLOB NLA** come specificato nel **membro lpBlob** della struttura [**WSAQUERYSET**](/windows/desktop/api/Winsock2/ns-winsock2-wsaquerysetw) restituita in *lpqsResults*. Queste strutture del **\_ BLOB NLA** possono essere concatenate e possono essere enumerate attraversando l'elenco mentre NLA \_ BLOB. Header. nextOffset è diverso da zero. Per ottenere risultati per tutte le informazioni sul percorso di rete, continuare a chiamare la funzione [**WSALookupServiceNext**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicenexta)fino a quando \_ \_ non \_ viene restituito l'errore WSA e, come illustrato nella pagina di riferimento **WSALookupServiceNext**.

La funzione [**WSALookupServiceNext**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicenexta) viene usata anche in combinazione con la funzione [**WSANSPIoctl**](/windows/desktop/api/Winsock2/nf-winsock2-wsanspioctl) per ricevere la notifica delle modifiche di rete. Per ulteriori informazioni, vedere [notifica da NLA](notification-from-nla-2.md) .

NLA restituisce zero al termine del completamento. I client di NLA devono continuare a chiamare il [**WSALookupServiceNext**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicenexta), funzione fino a quando \_ \_ non \_ viene restituito WSA E, a indicare che sono state restituite tutte le informazioni sulle reti disponibili.

In caso contrario, la chiamata a [**WSALookupServiceNext**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicenexta), funzione per NLA supporta i codici di errore seguenti.

| Errore                    | Significato                                                                                                                                                                                                                                                                                                                                                                                                     |
|--------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| WSANOTINITIALISED        | Una chiamata alla funzione [**WSAStartup**](/windows/desktop/api/winsock/nf-winsock-wsastartup) che ha inizializzato l'NLA non è stata eseguita.                                                                                                                                                                                                                                                                                                |
| \_handle non valido WSA \_     | L'handle di ricerca specificato nel parametro *hLookup* non è un handle NLA SP valido. I client devono prima chiamare la funzione [**WSALookupServiceBegin**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicebegina) e ricevere un handle NLA SP valido per ottenere i risultati della query.                                                                                                                                                               |
| WSAESYSNOTREADY          | Il servizio NLA non è disponibile per l'elaborazione della richiesta.                                                                                                                                                                                                                                                                                                                                                     |
| WSAEFAULT                | La dimensione del buffer specificata nel parametro *lpdwBufferLength* non è sufficiente per conservare i risultati a cui punta *lpqsResults*. Il buffer richiesto è specificato in *lpdwBufferLength*; Se il client non è in grado di fornire un buffer sufficientemente grande, il client può chiamare la funzione [**WSALookupServiceNext**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicenexta) con *DWCONTROLFLAGS* impostato su LUP \_ FLUSHPREVIOUS per ignorare la voce. |
| \_ \_ memoria insufficiente per WSA \_ | NLA non è in grado di ottenere le informazioni di rete dal servizio di sistema NLA a causa di memoria insufficiente nel processo chiamante.                                                                                                                                                                                                                                                                                  |
| WSA \_ E \_ nient' \_ altro         | Non sono presenti reti aggiuntive da enumerare per la query.                                                                                                                                                                                                                                                                                                                                                |



 

## <a name="step-3-terminate-the-query"></a>Passaggio 3: terminare la query

Quando tutte le query a NLA sono completate e per un'applicazione non è più necessario usare NLA, è necessario effettuare una chiamata alla funzione [**WSALookupServiceEnd**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupserviceend) . Non chiamare **WSALookupServiceEnd** se l'applicazione riceverà una notifica di modifica basata sulla query inviata. Per ulteriori informazioni sulla ricezione di notifiche, vedere [notifica da NLA](notification-from-nla-2.md) . Come per la maggior parte dei provider di servizi Windows Sockets, NLA mantiene un conteggio dei riferimenti per i client. La chiamata della funzione **WSALookupServiceEnd** quando vengono completate le query per NLA consente di liberare le risorse di sistema non più richieste da NLA.

NLA supporta i codici di errore seguenti per le chiamate di funzione [**WSALookupServiceEnd**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupserviceend) .

| Errore                | Significato                                                                                                   |
|----------------------|-----------------------------------------------------------------------------------------------------------|
| WSANOTINITIALISED    | Una chiamata riuscita alla funzione [**WSAStartup**](/windows/desktop/api/winsock/nf-winsock-wsastartup) per inizializzare NLA non è stata eseguita. |
| \_handle non valido WSA \_ | L'handle specificato nel parametro *hLookup* non è un handle di NLA SP valido.                             |



 

 

 



