---
description: La tabella seguente descrive le \_ Opzioni del socket IRLMP di Sol che si applicano ai socket creati per la famiglia di indirizzi IrDA (Infrared Data Association) \_ e il protocollo IRLMP (Infrared Link Management Protocol).
ms.assetid: 0457159d-8509-435c-8f57-752530d5df65
title: Opzioni di SOL_IRLMP socket (AF \_ IrDA. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 090193aec00eaebd87494afefbafc7b1450fdb44
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331700"
---
# <a name="sol_irlmp-socket-options"></a>\_Opzioni socket IRLMP Sol

La tabella seguente descrive le opzioni del socket **\_ IRLMP di Sol** che si applicano ai socket creati per la famiglia di indirizzi IrDA (Infrared Data Association) \_ e il protocollo IRLMP (Infrared Link Management Protocol). Vedere le pagine di riferimento per le funzioni [**getsockopt**](/windows/desktop/api/winsock/nf-winsock-getsockopt) e [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt) per altre informazioni su come ottenere e impostare le opzioni del socket.

Per enumerare i protocolli e individuare le proprietà supportate per ogni protocollo installato, usare la funzione [**WSAEnumProtocols**](/windows/desktop/api/Winsock2/nf-winsock2-wsaenumprotocolsa), [**WSCEnumProtocols**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscenumprotocols)o [**WSCEnumProtocols32**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscenumprotocols32) .

<dl> <dt><span id="SOL_IRLMP_Socket_Options"></span><span id="sol_irlmp_socket_options"></span><span id="SOL_IRLMP_SOCKET_OPTIONS"></span>**\_Opzioni socket IRLMP Sol**</dt> <dd> <dl> <dt> 

| Opzione                 | Recupero | Set | Tipo optVal     | Descrizione                                                            |
|------------------------|-----|-----|-----------------|------------------------------------------------------------------------|
| \_modalità di individuazione IRLMP \_ |     |     |                 |                                                                        |
| \_ENUMDEVICES IRLMP     | sì |     | **DEVICELIST**  | Restituisce un elenco di ID dispositivo IrDA per i dispositivi con supporto IR nell'intervallo. |
| \_modalità esclusiva di IRLMP \_ |     |     | DWORD (booleano) | Imposta socket per ignorare il livello TinyTP per comunicare direttamente con IrLMP. |
| \_query IAS \_ IRLMP      | sì |     | **\_query IAS**  | Esegue una query su IAS per un servizio e un nome di classe specificati per i relativi attributi.      |
| \_set IAS \_ IRLMP        |     | sì | **IAS \_ impostato**    | Imposta un valore di attributo per un nome di classe e un attributo specificati in IAS. |
| \_modalità IRLPT \_ IRLMP     |     | sì | DWORD (booleano) | Abilita la comunicazione con stampanti con supporto IR.                        |
| \_parametri IRLMP      |     |     |                 |                                                                        |
| IRLMP \_ inviare \_ PDU \_ Len  | sì |     | DWORD           | Recupera la lunghezza massima della PDU necessaria per usare la \_ modalità 9WIRE di IRLMP \_ .   |
| \_modalità IRLMP Sharp \_     |     | sì |                 |                                                                        |
| \_modalità TINYTP \_ IRLMP    |     | sì |                 |                                                                        |
| \_Modalità 9WIRE \_ IRLMP     | sì | sì | DWORD (booleano) | Inserisce il socket IrDA in modalità IrCOMM.                                 |



 

</dt> </dl> </dd> <dt><span id="Windows_Support_for_SOL_IRLMP_options"></span><span id="windows_support_for_sol_irlmp_options"></span><span id="WINDOWS_SUPPORT_FOR_SOL_IRLMP_OPTIONS"></span>**Supporto di Windows per le \_ Opzioni di IRLMP Sol**</dt> <dd> <dl> <dt> 

| Opzione                            | Windows 7 | Windows Server 2008 | Windows Vista | Windows Server 2003 | Windows XP | Windows 2000 | Windows me, Windows 98 | Windows NT 4.0 |
|-----------------------------------|-----------|---------------------|---------------|---------------------|------------|--------------|------------------------|----------------|
| \_modalità di individuazione IRLMP \_<br/> |           |                     |               |                     |            |              | x                      |                |
| \_ENUMDEVICES IRLMP<br/>     | x         | x                   | x             | x                   | x          | x            | x                      |                |
| \_modalità esclusiva di IRLMP \_<br/> |           |                     |               |                     |            |              |                        |                |
| \_query IAS \_ IRLMP<br/>      | x         | x                   | x             | x                   | x          | x            | x                      |                |
| \_set IAS \_ IRLMP<br/>        | x         | x                   | x             | x                   | x          | x            | x                      |                |
| \_modalità IRLPT \_ IRLMP<br/>     | x         | x                   | x             | x                   | x          | x            |                        |                |
| \_parametri IRLMP<br/>      |           |                     |               |                     |            |              | x                      |                |
| IRLMP \_ inviare \_ PDU \_ Len<br/>  | x         | x                   | x             | x                   | x          | x            |                        |                |
| \_modalità IRLMP Sharp \_<br/>     |           |                     |               |                     |            |              |                        |                |
| \_modalità TINYTP \_ IRLMP<br/>    |           |                     |               |                     |            |              | x                      |                |
| \_Modalità 9WIRE \_ IRLMP<br/>     | x         | x                   | x             | x                   | x          | x            |                        |                |



 


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Commenti

Le opzioni del socket **\_ IRLMP Sol** e le strutture usate da queste opzioni del socket sono definite nel file di intestazione di *AF \_ IrDA. h* .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|---------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>AF \_ IrDA. h</dt> </dl> |



 

 




