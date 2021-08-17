---
description: Le tabelle seguenti descrivono le opzioni socket IPX NSPROTO che si applicano ai socket creati per la famiglia di indirizzi \_ IPX/SPX (AF \_ IPX). Per altre informazioni su come ottenere e impostare le opzioni socket, vedere le pagine di riferimento sulle funzioni getsockopt e setsockopt.
ms.assetid: 0d5c8299-14d7-41e5-8ff6-f57a732acb26
title: NSPROTO_IPX socket (Wsnwlink.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e6803b5ab6cdf3002a60726c30648a1ae61bb59430820f049aeb8b011f367e73
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118993631"
---
# <a name="nsproto_ipx-socket-options"></a>Opzioni socket IPX NSPROTO \_

Le tabelle seguenti descrivono le opzioni socket **\_ IPX NSPROTO** che si applicano ai socket creati per la famiglia di indirizzi IPX/SPX (AF \_ IPX). Per altre informazioni su come ottenere e impostare le opzioni socket, vedere le pagine di riferimento sulle funzioni [**getsockopt**](/windows/desktop/api/winsock/nf-winsock-getsockopt) e [**setsockopt.**](/windows/desktop/api/winsock/nf-winsock-setsockopt)

Per enumerare i protocolli e individuare le proprietà supportate per ogni protocollo installato, usare la funzione [**WSAEnumProtocols,**](/windows/desktop/api/Winsock2/nf-winsock2-wsaenumprotocolsa) [**WSCEnumProtocols**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscenumprotocols)o [**WSCEnumProtocols32.**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscenumprotocols32)

<dl> <dt><span id="NSPROTO_IPX_Socket_Options"></span><span id="nsproto_ipx_socket_options"></span><span id="NSPROTO_IPX_SOCKET_OPTIONS"></span>**Opzioni socket IPX NSPROTO \_**</dt> <dd> <dl> <dt> 

| Opzione                      | Recupero | Impostazione | Tipo optval                  | Descrizione                                                                                                                                                                                                                                                                     |
|-----------------------------|-----|-----|------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| INDIRIZZO \_ IPX                | sì |     | **DATI DEGLI \_ INDIRIZZI \_ IPX**       | Restituisce informazioni sulla scheda specifica su cui è abilitato IPX.                                                                                                                                                                                                          |
| NOTIFICA DELL'INDIRIZZO IPX \_ \_        | sì |     | **DATI DEGLI \_ INDIRIZZI \_ IPX**       | Notifica in modo asincrono quando cambia lo stato di una scheda IPX.                                                                                                                                                                                                              |
| IPX \_ DSTYPE                 | sì | sì | DWORD                        | Ottiene o imposta il valore del campo datastream nell'intestazione SPX con cui inviare pacchetti.                                                                                                                                                                                          |
| INDIRIZZO ESTESO \_ \_ IPX      |     | sì | DWORD (booleano)              | Abilita l'opzione di indirizzamento esteso nei pacchetti IPX.                                                                                                                                                                                                                          |
| IPX \_ FILTERPTYPE            | sì | sì | DWORD                        | Ottiene o imposta il tipo di pacchetto del filtro di ricezione IPX corrente. Verranno restituiti solo pacchetti IPX con un tipo di pacchetto uguale al valore specificato nel parametro optval. I pacchetti con un tipo di pacchetto che non corrisponde vengono eliminati. Questo è applicabile solo a un socket di datagramma. |
| IPX \_ GETNETINFO             | sì |     | **DATI \_ NETNUM IPX \_**        | Restituisce informazioni relative a un numero di rete IPX specifico. Il membro netnum della struttura **IPX \_ NETNUM \_ DATA** deve essere impostato sul numero di rete IPX da restituire.                                                                                                     |
| IPX \_ GETNETINFO \_ NORIP      | sì |     | **DATI \_ NETNUM IPX \_**        | Restituisce informazioni relative a un numero di rete IPX specifico senza inviare una richiesta RIP. Il membro netnum della struttura **IPX \_ NETNUM \_ DATA** deve essere impostato sul numero di rete IPX da restituire.                                                                       |
| IPX \_ IMMEDIATESPXACK        |     | sì | DWORD (booleano)              | Se impostata su **TRUE,** non ritardare l'invio di elenchi di controllo di accesso in una connessione SPX.                                                                                                                                                                                                             |
| IPX \_ MAX \_ ADAPTER \_ NUM      | sì |     | DWORD                        | Restituisce il numero di schede abilitate per IPX presenti.                                                                                                                                                                                                                             |
| IPX \_ MAXSIZE                | sì |     | DWORD                        | Restituisce la dimensione massima in byte del datagramma IPX che può essere inviata.                                                                                                                                                                                                                |
| IPX \_ PTYPE                  | sì | sì | DWORD                        | Ottiene o imposta il tipo di pacchetto. Il valore specificato nel parametro optval verrà impostato come tipo di pacchetto in ogni pacchetto IPX inviato da questo socket.                                                                                                                             |
| TRASMISSIONE DI RICEZIONE IPX \_ \_     |     | sì | DWORD (booleano)              | Se impostato su **TRUE,** ricevere pacchetti IPX trasmessi.                                                                                                                                                                                                                              |
| IPX \_ RECVHDR                |     | sì | DWORD (booleano)              | Se impostato su **TRUE,** ricevere intestazioni del protocollo IPX con dati.                                                                                                                                                                                                                     |
| IPX \_ RERIPNETNUMBER         | sì |     | **DATI \_ NETNUM IPX \_**        | Restituisce informazioni relative a un numero di rete IPX specificato usando una nuova richiesta RIP. Il membro netnum della struttura **IPX \_ NETNUM \_ DATA** deve essere impostato sul numero di rete IPX da restituire.                                                                            |
| IPX \_ SPXGETCONNECTIONSTATUS | sì |     | **DATI \_ SPXCONNSTATUS IPX \_** | Restituisce informazioni relative alle statistiche di un socket SPX connesso.                                                                                                                                                                                                                |
| IPX \_ STOPFILTERPTYPE        |     | sì | DWORD                        | Rimuove il filtro e interrompe il filtro in base al tipo di pacchetto specificato nel parametro optval.                                                                                                                                                                                        |



 

</dt> </dl> </dd> <dt><span id="Windows_Support_for_NSPROTO_IPX_options"></span><span id="windows_support_for_nsproto_ipx_options"></span><span id="WINDOWS_SUPPORT_FOR_NSPROTO_IPX_OPTIONS"></span>**Windows Supporto per le opzioni IPX NSPROTO \_**</dt> <dd> <dl> <dt> 

| Opzione                      | Windows Vista e versioni successive | Windows Server 2003 | Windows XP | Windows 2000 | Windows NT4 | Windows 9x/Me |
|-----------------------------|-------------------------|---------------------|------------|--------------|-------------|---------------|
| INDIRIZZO \_ IPX                |                         | x                   | x          | x            | x           | x             |
| NOTIFICA DELL'INDIRIZZO IPX \_ \_        |                         | x                   | x          | x            | x           | x             |
| IPX \_ DSTYPE                 |                         | x                   | x          | x            | x           | x             |
| INDIRIZZO ESTESO \_ \_ IPX      |                         | x                   | x          | x            | x           | x             |
| IPX \_ FILTERPTYPE            |                         | x                   | x          | x            | x           | x             |
| IPX \_ GETNETINFO             |                         | x                   | x          | x            | x           | x             |
| IPX \_ GETNETINFO \_ NORIP      |                         | x                   | x          | x            | x           | x             |
| IPX \_ IMMEDIATESPXACK        |                         | x                   | x          | x            | x           | x             |
| IPX \_ MAX \_ ADAPTER \_ NUM      |                         | x                   | x          | x            | x           | x             |
| IPX \_ MAXSIZE                |                         | x                   | x          | x            | x           | x             |
| IPX \_ PTYPE                  |                         | x                   | x          | x            | x           | x             |
| TRASMISSIONE DI RICEZIONE IPX \_ \_     |                         | x                   | x          | x            | x           | x             |
| IPX \_ RECVHDR                |                         | x                   | x          | x            | x           | x             |
| IPX \_ RERIPNETNUMBER         |                         | x                   | x          | x            | x           | x             |
| IPX \_ SPXGETCONNECTIONSTATUS |                         | x                   | x          | x            | x           | x             |
| IPX \_ STOPFILTERPTYPE        |                         | x                   | x          | x            | x           | x             |



 


</dt> </dl> </dd> </dl>

Le opzioni socket **\_ IPX NSPROTO** seguenti sono state definite nell'allegato Windows Sockets 2 Protocol-Specific, ma non sono implementate dal protocollo IPX/SPX Windows.

*level* **=** **NSPROTO \_ IPX**



| Opzione           | Type | Predefinito                         | Significato                                                                                                                                                       |
|------------------|------|---------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| IPX \_ CHECKSUM    | Bool | spento                             | Se impostato, IPX esegue un checksum sui pacchetti in uscita e verifica il checksum dei pacchetti in ingresso.                                                          |
| IPX \_ TXPKTSIZE   | int  | Dimensioni dei supporti fino a un massimo di 1466 | Imposta le dimensioni massime del datagramma di invio. Queste dimensioni non includono l'intestazione IPX o eventuali intestazioni multimediali che possono essere usate. Può essere aumentato alle dimensioni del supporto.    |
| IPX \_ RXPKTSIZE   | int  | Dimensioni dei supporti fino a un massimo di 1466 | Imposta le dimensioni massime del datagramma di ricezione. Queste dimensioni non includono l'intestazione IPX o eventuali intestazioni multimediali che possono essere usate. Può essere aumentato alle dimensioni del supporto. |
| IPX \_ TXMEDIASIZE | int  | Scheda primaria                   | Restituisce le dimensioni del supporto di invio che imposta un limite superiore per le dimensioni del datagramma.                                                                                       |
| IPX \_ RXMEDIASIZE | int  | Scheda primaria                   | Restituisce le dimensioni dei supporti di ricezione che impostano un limite superiore per le dimensioni del datagramma.                                                                                    |
| IPX \_ PRIMARY     | Bool | Principale                         | Limita il traffico alla scheda di rete primaria.                                                                                                               |



 

Le opzioni socket **NSPROTO \_ SPX** seguenti sono state definite in Windows Sockets 2 Protocol-Specific Annex, ma non sono implementate in Windows dal protocollo IPX/SPX di Windows.

*level* **=** **NSPROTO \_ SPX**



| Opzione           | Type | Predefinito                         | Significato                                                                                                                                                       |
|------------------|------|---------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| SPX \_ CHECKSUM    | Bool | spento                             | Se impostato, IPX esegue un checksum sui pacchetti in uscita e verifica il checksum dei pacchetti in ingresso. Non supportato in tutte le piattaforme.                          |
| SPX \_ TXPKTSIZE   | int  | Dimensioni dei supporti fino a un massimo di 1466 | Imposta le dimensioni massime del datagramma di invio. Queste dimensioni non includono l'intestazione SPX o eventuali intestazioni multimediali che possono essere utilizzate. Può essere aumentato alle dimensioni del supporto.    |
| SPX \_ RXPKTSIZE   | int  | Dimensioni dei supporti fino a un massimo di 1466 | Imposta le dimensioni massime del datagramma di ricezione. Queste dimensioni non includono l'intestazione SPX o eventuali intestazioni multimediali che possono essere utilizzate. Può essere aumentato alle dimensioni del supporto. |
| SPX \_ TXMEDIASIZE | int  | Scheda primaria                   | Restituisce le dimensioni del supporto di invio meno SPX e le intestazioni dei supporti. In questo modo viene impostato un limite superiore per le dimensioni del pacchetto di segmentazione dei messaggi.                                       |
| SPX \_ RXMEDIASIZE | int  | Scheda primaria                   | Restituisce le dimensioni dei supporti di ricezione meno SPX e le intestazioni dei supporti. In questo modo viene impostato un limite superiore per la dimensione del pacchetto di ricezione.                                                 |
| SPX \_ RAWSPX      | Bool | spento                             | Se impostata, l'intestazione del protocollo IPX/SPX viene passata con i dati.                                                                                                |



 

## <a name="remarks"></a>Commenti

Le opzioni socket **\_ IPX NSPROTO** e le strutture usate da queste opzioni di socket sono definite nel file di intestazione *Wsnwlink.h.*

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|---------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>Wsnwlink.h</dt> </dl> |



 

 




