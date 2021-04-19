---
description: Nella tabella seguente vengono descritte le \_ Opzioni del socket di Sol AppleTalk che si applicano ai socket creati per la famiglia di indirizzi AppleTalk (AF \_ AppleTalk).
ms.assetid: 1a6b18e3-1fea-4ba2-8076-c38e7f679e9e
title: Opzioni di SOL_APPLETALK socket (ATALKWSH. h)
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
ms.openlocfilehash: 146cfa02706cc9a2669cf21ba6d9eac0ac74ee4d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332130"
---
# <a name="sol_appletalk-socket-options"></a>Opzioni del socket per la tecnologia solenoide \_

Nella tabella seguente vengono descritte le opzioni del socket di **Sol \_ AppleTalk** che si applicano ai socket creati per la famiglia di indirizzi AppleTalk (AF \_ AppleTalk). Vedere le pagine di riferimento per le funzioni [**getsockopt**](/windows/desktop/api/winsock/nf-winsock-getsockopt) e [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt) per altre informazioni su come ottenere e impostare le opzioni del socket.

Per enumerare i protocolli e individuare le proprietà supportate per ogni protocollo installato, usare la funzione [**WSAEnumProtocols**](/windows/desktop/api/Winsock2/nf-winsock2-wsaenumprotocolsa), [**WSCEnumProtocols**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscenumprotocols)o [**WSCEnumProtocols32**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscenumprotocols32) .

<dl> <dt><span id="SOL_APPLETALK_Socket_Options"></span><span id="sol_appletalk_socket_options"></span><span id="SOL_APPLETALK_SOCKET_OPTIONS"></span>**Opzioni del socket per la tecnologia solenoide \_**</dt> <dd> <dl> <dt> 

| Opzione                          | Recupero | Set | Tipo optVal                          | Descrizione                                                                                                                                                                                          |
|---------------------------------|-----|-----|--------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| QUINDI, \_ conferma \_ nome               | sì |     | **\_ \_ tupla avvio WSH**                  | Conferma che un determinato nome AppleTalk è associato all'indirizzo specificato.                                                                                                                                  |
| QUINDI, \_ DEregistrare il \_ nome            |     | sì | **\_nome del registro WSH \_**              | Annulla la registrazione del nome dalla rete.                                                                                                                                                               |
| \_GETLOCALZONES               | sì |     | **\_zone di ricerca WSH \_**               | Restituisce un elenco di nomi di zona noti al nome di adapter specificato.                                                                                                                                        |
| \_GETMYZONE                   | sì |     | char \[\]                            | Restituisce l'area predefinita sulla rete.                                                                                                                                                             |
| \_GETNETINFO                  | sì |     | **\_ \_ NETDEF di ricerca WSH \_ sull' \_ Adapter** | Restituisce i valori di inizializzazione per la rete e la zona predefinita. Il parametro *optlen* deve essere di almeno un byte maggiore della dimensione del NETDEF di **ricerca WSH sulla struttura dell' \_ \_ \_ \_ Adapter** .  |
| QUINDI \_ GETzone                 | sì |     | **\_zone di ricerca WSH \_**               | Restituisce i nomi delle zone dall'elenco di aree Internet. Il parametro *optlen* deve essere di almeno un byte maggiore della dimensione della struttura di **\_ \_ zone di ricerca WSH** .                                       |
| \_ricerca quindi \_ area              | sì |     |                                      | Uguale a \_ GETMYZONE                                                                                                                                                                                |
| \_nome ricerca \_                | sì |     | **\_nome ricerca \_ WSH**                | Cerca un nome avvio specificato e restituisce le tuple corrispondenti delle informazioni sul nome e avvio. Il parametro *optlen* deve essere di almeno un byte maggiore della dimensione della \_ struttura del nome di ricerca WSH \_ . |
| QUINDI, \_ cercare \_ NETDEF \_ sull' \_ Adapter | sì |     | **\_ \_ NETDEF di ricerca WSH \_ sull' \_ Adapter** | Uguale a \_ GETNETINFO.                                                                                                                                                                              |
| QUINDI \_ , \_ zone di ricerca               | sì |     | **\_zone di ricerca WSH \_**               | Uguale a \_ getzone.                                                                                                                                                                             |
| QUINDI \_ , \_ zone \_ di ricerca nell' \_ Adapter  | sì |     | **\_zone di ricerca WSH \_**               | Uguale a \_ GETLOCALZONES.                                                                                                                                                                           |
| QUINDI \_ , \_ PAP \_ ottenere \_ lo stato del server    | sì |     | **\_stato del server WSH PAP \_ get \_ \_**    | Restituisce lo stato del PAP da un server specificato                                                                                                                                                           |
| QUINDI, \_ PAP \_ prime \_ letto            |     | sì | char \[\]                            | Questa chiamata inizia un'operazione di lettura su una connessione PAP, in modo che il mittente possa iniziare a inviare i dati                                                                                                                 |
| \_stato del \_ Server PAP set \_ \_ so    |     | sì | char \[\]                            | Imposta lo stato da inviare se un altro client richiede lo stato                                                                                                                                     |
| \_nome registro \_              |     | sì | **\_nome del registro WSH \_**              | Registra il nome specificato nella rete AppleTalk                                                                                                                                                    |
| \_Rimuovi \_ nome                |     | sì | **\_nome del registro WSH \_**              | Come per la \_ DEregistrazione del \_ nome                                                                                                                                                                         |



 

</dt> </dl> </dd> <dt><span id="Windows_Support_for_SOL_APPLETALK_options"></span><span id="windows_support_for_sol_appletalk_options"></span><span id="WINDOWS_SUPPORT_FOR_SOL_APPLETALK_OPTIONS"></span>**Supporto di Windows per le opzioni di SOL \_ AppleTalk**</dt> <dd> <dl> <dt> 

| Opzione                          | Windows Vista e versioni successive | Windows Server 2003 | Windows XP | Windows 2000 | Windows NT4 | Windows 9x/Me |
|---------------------------------|-------------------------|---------------------|------------|--------------|-------------|---------------|
| QUINDI, \_ conferma \_ nome               |                         | x                   | x          | x            | x           |               |
| QUINDI, \_ DEregistrare il \_ nome            |                         | x                   | x          | x            | x           |               |
| \_GETLOCALZONES               |                         | x                   | x          | x            | x           |               |
| \_GETMYZONE                   |                         | x                   | x          | x            | x           |               |
| \_GETNETINFO                  |                         | x                   | x          | x            | x           |               |
| QUINDI \_ GETzone                 |                         | x                   | x          | x            | x           |               |
| \_ricerca quindi \_ area              |                         | x                   | x          | x            | x           |               |
| \_nome ricerca \_                |                         | x                   | x          | x            | x           |               |
| QUINDI, \_ cercare \_ NETDEF \_ sull' \_ Adapter |                         | x                   | x          | x            | x           |               |
| QUINDI \_ , \_ zone di ricerca               |                         | x                   | x          | x            | x           |               |
| QUINDI \_ , \_ zone \_ di ricerca nell' \_ Adapter  |                         | x                   | x          | x            | x           |               |
| QUINDI \_ , \_ PAP \_ ottenere \_ lo stato del server    |                         | x                   | x          | x            | x           |               |
| QUINDI, \_ PAP \_ prime \_ letto            |                         | x                   | x          | x            | x           |               |
| \_stato del \_ Server PAP set \_ \_ so    |                         | x                   | x          | x            | x           |               |
| \_nome registro \_              |                         | x                   | x          | x            | x           |               |
| \_Rimuovi \_ nome                |                         | x                   | x          | x            | x           |               |



 

Le opzioni di **Sol \_ AppleTalk** sono supportate solo nelle versioni server di Windows 2000 e Windows NT 4,0.


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Commenti

Le opzioni del socket **\_ AppleTalk di Sol** e le strutture usate da queste opzioni del socket sono definite nel file di intestazione *ATALKWSH. h* .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|---------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>ATALKWSH. h</dt> </dl> |



 

 




