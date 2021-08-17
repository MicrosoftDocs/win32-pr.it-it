---
description: La tabella seguente descrive le opzioni dei socket APPLETALK SOL applicabili ai socket creati per la famiglia di indirizzi \_ AppleTalk \_ (AF APPLETALK).
ms.assetid: 1a6b18e3-1fea-4ba2-8076-c38e7f679e9e
title: SOL_APPLETALK socket di rete (Atalkwsh.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SOL_APPLETALK
- Windows
api_type:
- HeaderDef
api_location:
- Atalkwsh.h
ms.openlocfilehash: 5ea45b4007a3bd36d2cfbceda5b7ec4f2cff20d9bb2387fb2d184710a8a4492c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117740008"
---
# <a name="sol_appletalk-socket-options"></a>Opzioni \_ del socket APPLETALK SOL

La tabella seguente descrive le opzioni dei socket **\_ APPLETALK SOL** applicabili ai socket creati per la famiglia di indirizzi AppleTalk \_ (AF APPLETALK). Per altre informazioni su come ottenere e impostare le opzioni socket, vedere le pagine di riferimento sulle funzioni [**getsockopt**](/windows/desktop/api/winsock/nf-winsock-getsockopt) e [**setsockopt.**](/windows/desktop/api/winsock/nf-winsock-setsockopt)

Per enumerare i protocolli e individuare le proprietà supportate per ogni protocollo installato, usare la funzione [**WSAEnumProtocols**](/windows/desktop/api/Winsock2/nf-winsock2-wsaenumprotocolsa), [**WSCEnumProtocols**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscenumprotocols)o [**WSCEnumProtocols32.**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscenumprotocols32)

<dl> <dt><span id="SOL_APPLETALK_Socket_Options"></span><span id="sol_appletalk_socket_options"></span><span id="SOL_APPLETALK_SOCKET_OPTIONS"></span>**Opzioni \_ del socket APPLETALK SOL**</dt> <dd> <dl> <dt> 

| Opzione                          | Recupero | Impostazione | Tipo Optval                          | Descrizione                                                                                                                                                                                          |
|---------------------------------|-----|-----|--------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| CONFERMARE \_ \_ QUINDI IL NOME               | sì |     | **\_TUPLA NBP WSH \_**                  | Conferma che un determinato nome AppleTalk è associato all'indirizzo specificato.                                                                                                                                  |
| SO \_ DEREGISTER \_ NAME            |     | sì | **NOME REGISTRO \_ \_ WSH**              | Annulla la registrazione del nome dalla rete.                                                                                                                                                               |
| SO \_ GETLOCALZONES               | sì |     | **ZONE DI \_ RICERCA \_ WSH**               | Restituisce un elenco di nomi di zona noti al nome dell'adattatore specificato.                                                                                                                                        |
| QUINDI \_ GETMYZONE                   | sì |     | Char \[\]                            | Restituisce la zona predefinita nella rete.                                                                                                                                                             |
| QUINDI \_ GETNETINFO                  | sì |     | **WSH \_ LOOKUP \_ NETDEF \_ \_ SULL'ADAPTER** | Restituisce i valori di seed per la rete e la zona predefinita. Il *parametro optlen* deve essere di almeno un byte maggiore della dimensione della struttura **WSH LOOKUP \_ \_ NETDEF ON \_ \_ ADAPTER.**  |
| QUINDI \_ GETZONELIST                 | sì |     | **ZONE DI \_ RICERCA \_ WSH**               | Restituisce i nomi delle zone dall'elenco dell'area Internet. Il *parametro optlen* deve essere di almeno un byte maggiore della dimensione della **struttura WSH LOOKUP \_ \_ ZONES.**                                       |
| QUINDI \_ CERCA \_ MYZONE              | sì |     |                                      | Uguale a SO \_ GETMYZONE                                                                                                                                                                                |
| SO \_ LOOKUP \_ NAME                | sì |     | **WSH \_ LOOKUP \_ NAME**                | Cerca un nome NBP specificato e restituisce le tuple corrispondenti di nome e informazioni NBP. Il *parametro optlen* deve essere di almeno un byte maggiore della dimensione della struttura WSH \_ LOOKUP \_ NAME. |
| QUINDI, \_ CERCARE \_ NETDEF \_ \_ NELL'ADAPTER | sì |     | **WSH \_ LOOKUP \_ NETDEF \_ \_ SULL'ADAPTER** | Uguale a SO \_ GETNETINFO.                                                                                                                                                                              |
| QUINDI \_ ZONE DI \_ RICERCA               | sì |     | **ZONE DI \_ RICERCA \_ WSH**               | Uguale a SO \_ GETZONELIST.                                                                                                                                                                             |
| ZONE \_ DI \_ RICERCA \_ \_ NELL'ADAPTER  | sì |     | **ZONE DI \_ RICERCA \_ WSH**               | Uguale a SO \_ GETLOCALZONES.                                                                                                                                                                           |
| QUINDI, \_ PAP \_ OTTIENE LO STATO \_ DEL \_ SERVER    | sì |     | **WSH \_ PAP \_ GET \_ SERVER \_ STATUS**    | Restituisce lo stato PAP da un determinato server                                                                                                                                                           |
| QUINDI, \_ PAP \_ PRIME \_ READ            |     | sì | Char \[\]                            | Questa chiamata avvia una lettura su una connessione PAP in modo che il mittente possa iniziare a inviare i dati                                                                                                                 |
| QUINDI \_ PAP \_ SET SERVER \_ \_ STATUS    |     | sì | Char \[\]                            | Imposta lo stato da inviare se un altro client richiede lo stato                                                                                                                                     |
| QUINDI \_ REGISTER \_ NAME              |     | sì | **NOME REGISTRO \_ \_ WSH**              | Registra il nome specificato nella rete AppleTalk                                                                                                                                                    |
| RIMUOVERE \_ QUINDI \_ IL NOME                |     | sì | **NOME REGISTRO \_ \_ WSH**              | Uguale a SO \_ DEREGISTER \_ NAME                                                                                                                                                                         |



 

</dt> </dl> </dd> <dt><span id="Windows_Support_for_SOL_APPLETALK_options"></span><span id="windows_support_for_sol_appletalk_options"></span><span id="WINDOWS_SUPPORT_FOR_SOL_APPLETALK_OPTIONS"></span>**Windows Supporto per le opzioni \_ APPLETALK SOL**</dt> <dd> <dl> <dt> 

| Opzione                          | Windows Vista e versioni successive | Windows Server 2003 | Windows XP | Windows 2000 | Windows NT4 | Windows 9x/Me |
|---------------------------------|-------------------------|---------------------|------------|--------------|-------------|---------------|
| CONFERMARE \_ \_ QUINDI IL NOME               |                         | x                   | x          | x            | x           |               |
| SO \_ DEREGISTER \_ NAME            |                         | x                   | x          | x            | x           |               |
| SO \_ GETLOCALZONES               |                         | x                   | x          | x            | x           |               |
| QUINDI \_ GETMYZONE                   |                         | x                   | x          | x            | x           |               |
| QUINDI \_ GETNETINFO                  |                         | x                   | x          | x            | x           |               |
| QUINDI \_ GETZONELIST                 |                         | x                   | x          | x            | x           |               |
| QUINDI \_ CERCA \_ MYZONE              |                         | x                   | x          | x            | x           |               |
| SO \_ LOOKUP \_ NAME                |                         | x                   | x          | x            | x           |               |
| QUINDI, \_ CERCARE \_ NETDEF \_ \_ NELL'ADAPTER |                         | x                   | x          | x            | x           |               |
| QUINDI \_ ZONE DI \_ RICERCA               |                         | x                   | x          | x            | x           |               |
| ZONE \_ DI \_ RICERCA \_ \_ NELL'ADAPTER  |                         | x                   | x          | x            | x           |               |
| QUINDI, \_ PAP \_ OTTIENE LO STATO \_ DEL \_ SERVER    |                         | x                   | x          | x            | x           |               |
| QUINDI, \_ PAP \_ PRIME \_ READ            |                         | x                   | x          | x            | x           |               |
| QUINDI \_ PAP \_ SET SERVER \_ \_ STATUS    |                         | x                   | x          | x            | x           |               |
| QUINDI \_ REGISTER \_ NAME              |                         | x                   | x          | x            | x           |               |
| RIMUOVERE \_ QUINDI \_ IL NOME                |                         | x                   | x          | x            | x           |               |



 

Le **opzioni \_ APPLETALK SOL** sono supportate solo nelle versioni server di Windows 2000 e Windows NT 4.0.


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Commenti

Le opzioni del socket **\_ APPLETALK SOL** e le strutture usate da queste opzioni sono definite nel file di intestazione *Atalkwsh.h.*

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|---------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>Atalkwsh.h</dt> </dl> |



 

 




