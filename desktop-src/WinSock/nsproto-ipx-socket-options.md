---
description: Le tabelle seguenti descrivono le \_ Opzioni del socket IPX NSPROTO che si applicano ai socket creati per la famiglia di indirizzi IPX/SPX (AF \_ IPX). Vedere le pagine di riferimento per le funzioni getsockopt e setsockopt per altre informazioni su come ottenere e impostare le opzioni del socket.
ms.assetid: 0d5c8299-14d7-41e5-8ff6-f57a732acb26
title: Opzioni di NSPROTO_IPX socket (Wsnwlink. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 433e1fabed1963c3549d2d5a34fb432cac795e07
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331848"
---
# <a name="nsproto_ipx-socket-options"></a>\_Opzioni socket IPX NSPROTO

Le tabelle seguenti descrivono le opzioni del socket **\_ IPX NSPROTO** che si applicano ai socket creati per la famiglia di indirizzi IPX/SPX (AF \_ IPX). Vedere le pagine di riferimento per le funzioni [**getsockopt**](/windows/desktop/api/winsock/nf-winsock-getsockopt) e [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt) per altre informazioni su come ottenere e impostare le opzioni del socket.

Per enumerare i protocolli e individuare le proprietà supportate per ogni protocollo installato, usare la funzione [**WSAEnumProtocols**](/windows/desktop/api/Winsock2/nf-winsock2-wsaenumprotocolsa), [**WSCEnumProtocols**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscenumprotocols)o [**WSCEnumProtocols32**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscenumprotocols32) .

<dl> <dt><span id="NSPROTO_IPX_Socket_Options"></span><span id="nsproto_ipx_socket_options"></span><span id="NSPROTO_IPX_SOCKET_OPTIONS"></span>**\_Opzioni socket IPX NSPROTO**</dt> <dd> <dl> <dt> 

| Opzione                      | Recupero | Set | Tipo optVal                  | Descrizione                                                                                                                                                                                                                                                                     |
|-----------------------------|-----|-----|------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \_indirizzo IPX                | sì |     | **\_dati indirizzo \_ IPX**       | Restituisce informazioni sull'adapter specifico su cui è abilitato IPX.                                                                                                                                                                                                          |
| \_notifica indirizzo \_ IPX        | sì |     | **\_dati indirizzo \_ IPX**       | Notifica in modo asincrono quando lo stato di un adapter IPX viene modificato.                                                                                                                                                                                                              |
| \_DSTYPE IPX                 | sì | sì | DWORD                        | Ottiene o imposta il valore del campo datastream nell'intestazione SPX con cui inviare i pacchetti.                                                                                                                                                                                          |
| \_indirizzo esteso \_ IPX      |     | sì | DWORD (booleano)              | Abilita l'opzione di indirizzamento esteso nei pacchetti IPX.                                                                                                                                                                                                                          |
| \_FILTERPTYPE IPX            | sì | sì | DWORD                        | Ottiene o imposta il tipo di pacchetto del filtro di ricezione IPX corrente. Verranno restituiti solo i pacchetti IPX con un tipo di pacchetto uguale al valore specificato nel parametro optVal. I pacchetti con un tipo di pacchetto non corrispondente vengono rimossi. Questa operazione è applicabile solo a un socket di datagramma. |
| \_GETNETINFO IPX             | sì |     | **\_dati NETNUM \_ IPX**        | Restituisce informazioni relative a un numero di rete IPX specifico. Il membro netnum della struttura **di \_ \_ dati IPX netnum** deve essere impostato sul numero di rete IPX da restituire.                                                                                                     |
| \_NORIP GETNETINFO \_ IPX      | sì |     | **\_dati NETNUM \_ IPX**        | Restituisce informazioni relative a un numero di rete IPX specifico senza inviare una richiesta RIP. Il membro netnum della struttura **di \_ \_ dati IPX netnum** deve essere impostato sul numero di rete IPX da restituire.                                                                       |
| \_IMMEDIATESPXACK IPX        |     | sì | DWORD (booleano)              | Se impostato su **true**, non ritardare l'invio di ACK su una connessione SPX.                                                                                                                                                                                                             |
| \_numero massimo di \_ adapter \_ IPX      | sì |     | DWORD                        | Restituisce il numero di adapter abilitati per IPX presenti.                                                                                                                                                                                                                             |
| \_MaxSize IPX                | sì |     | DWORD                        | Restituisce la dimensione massima del datagramma IPX in byte che può essere inviata.                                                                                                                                                                                                                |
| \_pType IPX                  | sì | sì | DWORD                        | Ottiene o imposta il tipo di pacchetto. Il valore specificato nel parametro optVal verrà impostato come tipo di pacchetto in ogni pacchetto IPX inviato da questo socket.                                                                                                                             |
| \_trasmissione di ricezione IPX \_     |     | sì | DWORD (booleano)              | Se impostato su **true**, ricevere i pacchetti IPX broadcast.                                                                                                                                                                                                                              |
| \_RECVHDR IPX                |     | sì | DWORD (booleano)              | Se impostato su **true**, ricevere le intestazioni del protocollo IPX con i dati.                                                                                                                                                                                                                     |
| \_RERIPNETNUMBER IPX         | sì |     | **\_dati NETNUM \_ IPX**        | Restituisce informazioni relative a un numero di rete IPX specificato utilizzando una nuova richiesta RIP. Il membro netnum della struttura **di \_ \_ dati IPX netnum** deve essere impostato sul numero di rete IPX da restituire.                                                                            |
| \_SPXGETCONNECTIONSTATUS IPX | sì |     | **\_dati SPXCONNSTATUS \_ IPX** | Restituisce informazioni relative alle statistiche del socket SPX connesse.                                                                                                                                                                                                                |
| \_STOPFILTERPTYPE IPX        |     | sì | DWORD                        | Rimuove il filtro e interrompe il filtro sul tipo di pacchetto specificato nel parametro optVal.                                                                                                                                                                                        |



 

</dt> </dl> </dd> <dt><span id="Windows_Support_for_NSPROTO_IPX_options"></span><span id="windows_support_for_nsproto_ipx_options"></span><span id="WINDOWS_SUPPORT_FOR_NSPROTO_IPX_OPTIONS"></span>**Supporto di Windows per le \_ Opzioni IPX di NSPROTO**</dt> <dd> <dl> <dt> 

| Opzione                      | Windows Vista e versioni successive | Windows Server 2003 | Windows XP | Windows 2000 | Windows NT4 | Windows 9x/Me |
|-----------------------------|-------------------------|---------------------|------------|--------------|-------------|---------------|
| \_indirizzo IPX                |                         | x                   | x          | x            | x           | x             |
| \_notifica indirizzo \_ IPX        |                         | x                   | x          | x            | x           | x             |
| \_DSTYPE IPX                 |                         | x                   | x          | x            | x           | x             |
| \_indirizzo esteso \_ IPX      |                         | x                   | x          | x            | x           | x             |
| \_FILTERPTYPE IPX            |                         | x                   | x          | x            | x           | x             |
| \_GETNETINFO IPX             |                         | x                   | x          | x            | x           | x             |
| \_NORIP GETNETINFO \_ IPX      |                         | x                   | x          | x            | x           | x             |
| \_IMMEDIATESPXACK IPX        |                         | x                   | x          | x            | x           | x             |
| \_numero massimo di \_ adapter \_ IPX      |                         | x                   | x          | x            | x           | x             |
| \_MaxSize IPX                |                         | x                   | x          | x            | x           | x             |
| \_pType IPX                  |                         | x                   | x          | x            | x           | x             |
| \_trasmissione di ricezione IPX \_     |                         | x                   | x          | x            | x           | x             |
| \_RECVHDR IPX                |                         | x                   | x          | x            | x           | x             |
| \_RERIPNETNUMBER IPX         |                         | x                   | x          | x            | x           | x             |
| \_SPXGETCONNECTIONSTATUS IPX |                         | x                   | x          | x            | x           | x             |
| \_STOPFILTERPTYPE IPX        |                         | x                   | x          | x            | x           | x             |



 


</dt> </dl> </dd> </dl>

Le seguenti opzioni del socket **\_ IPX NSPROTO** sono state definite in Windows sockets 2 Protocol-Specific allegato, ma non sono implementate dal protocollo IPX/SPX di Windows.

*livello* **=** di **NSPROTO \_ IPX**



| Opzione           | Type | Predefinito                         | Significato                                                                                                                                                       |
|------------------|------|---------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \_checksum IPX    | Bool | spento                             | Quando è impostato, IPX esegue un checksum sui pacchetti in uscita e verifica il checksum dei pacchetti in arrivo.                                                          |
| \_TXPKTSIZE IPX   | INT  | Dimensioni supporti fino a un massimo di 1466 | Imposta la dimensione massima del datagramma di invio. Questa dimensione non include l'intestazione IPX o eventuali intestazioni del supporto che possono essere usate anche. Può essere aumentata alla dimensione del supporto.    |
| \_RXPKTSIZE IPX   | INT  | Dimensioni supporti fino a un massimo di 1466 | Imposta la dimensione massima del datagramma di ricezione. Questa dimensione non include l'intestazione IPX o eventuali intestazioni del supporto che possono essere usate anche. Può essere aumentata alla dimensione del supporto. |
| \_TXMEDIASIZE IPX | INT  | Lavagna primaria                   | Restituisce la dimensione del supporto di trasmissione che imposta un limite superiore per le dimensioni del datagramma.                                                                                       |
| \_RXMEDIASIZE IPX | INT  | Lavagna primaria                   | Restituisce la dimensione del supporto di ricezione che imposta un limite superiore per le dimensioni del datagramma.                                                                                    |
| \_primario IPX     | Bool | Principale                         | Limita il traffico alla scheda di rete primaria.                                                                                                               |



 

Le opzioni del socket **\_ SPX NSPROTO** seguenti sono state definite in Windows sockets 2 Protocol-Specific allegato, ma non sono implementate in Windows dal protocollo IPX/SPX di Windows.

*livello* **=** di **NSPROTO \_ SPX**



| Opzione           | Type | Predefinito                         | Significato                                                                                                                                                       |
|------------------|------|---------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \_checksum SPX    | Bool | spento                             | Quando è impostato, IPX esegue un checksum sui pacchetti in uscita e verifica il checksum dei pacchetti in arrivo. Non supportato in tutte le piattaforme.                          |
| \_TXPKTSIZE SPX   | INT  | Dimensioni supporti fino a un massimo di 1466 | Imposta la dimensione massima del datagramma di invio. Questa dimensione non include l'intestazione SPX o eventuali intestazioni multimediali che possono essere usate. Può essere aumentata alla dimensione del supporto.    |
| \_RXPKTSIZE SPX   | INT  | Dimensioni supporti fino a un massimo di 1466 | Imposta la dimensione massima del datagramma di ricezione. Questa dimensione non include l'intestazione SPX o eventuali intestazioni multimediali che possono essere usate. Può essere aumentata alla dimensione del supporto. |
| \_TXMEDIASIZE SPX | INT  | Lavagna primaria                   | Restituisce le dimensioni dei supporti di invio meno SPX e le intestazioni del supporto. In questo modo viene impostato un limite superiore per le dimensioni del pacchetto di segmentazione del messaggio.                                       |
| \_RXMEDIASIZE SPX | INT  | Lavagna primaria                   | Restituisce le dimensioni del supporto di ricezione meno SPX e le intestazioni del supporto. In questo modo viene impostato un limite superiore per le dimensioni del pacchetto di ricezione.                                                 |
| \_RAWSPX SPX      | Bool | spento                             | Se impostato, l'intestazione del protocollo IPX/SPX viene passata con i dati.                                                                                                |



 

## <a name="remarks"></a>Commenti

Le opzioni del socket **\_ IPX NSPROTO** e le strutture usate da queste opzioni del socket sono definite nel file di intestazione *Wsnwlink. h* .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|---------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>Wsnwlink. h</dt> </dl> |



 

 




