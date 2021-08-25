---
description: La tabella seguente descrive le opzioni socket SOL IRLMP applicabili ai socket creati per la famiglia di indirizzi \_ IrDA (Infrared Data Association) e \_ IRLMP (InfraRed Link Management Protocol).
ms.assetid: 0457159d-8509-435c-8f57-752530d5df65
title: SOL_IRLMP Socket Options (Af \_ irda.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4b2be68bc658cd7d55ff72a77b6ec87568c37d6d786d0a5e654e9276378b837c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119860731"
---
# <a name="sol_irlmp-socket-options"></a>Opzioni \_ socket SOL IRLMP

La tabella seguente descrive le opzioni socket **\_ SOL IRLMP** applicabili ai socket creati per la famiglia di indirizzi IrDA (Infrared Data Association) e \_ IRLMP (InfraRed Link Management Protocol). Per altre informazioni su come ottenere e impostare le opzioni socket, vedere le pagine di riferimento sulle funzioni [**getsockopt**](/windows/desktop/api/winsock/nf-winsock-getsockopt) e [**setsockopt.**](/windows/desktop/api/winsock/nf-winsock-setsockopt)

Per enumerare i protocolli e individuare le proprietà supportate per ogni protocollo installato, usare la funzione [**WSAEnumProtocols**](/windows/desktop/api/Winsock2/nf-winsock2-wsaenumprotocolsa), [**WSCEnumProtocols**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscenumprotocols)o [**WSCEnumProtocols32.**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscenumprotocols32)

<dl> <dt><span id="SOL_IRLMP_Socket_Options"></span><span id="sol_irlmp_socket_options"></span><span id="SOL_IRLMP_SOCKET_OPTIONS"></span>**Opzioni \_ socket SOL IRLMP**</dt> <dd> <dl> <dt> 

| Opzione                 | Recupero | Impostazione | Tipo Optval     | Descrizione                                                            |
|------------------------|-----|-----|-----------------|------------------------------------------------------------------------|
| MODALITÀ DI INDIVIDUAZIONE IRLMP \_ \_ |     |     |                 |                                                                        |
| IRLMP \_ ENUMDEVICES     | sì |     | **DEVICELIST**  | Restituisce un elenco di ID dispositivo IrDA per i dispositivi che supportano IR entro l'intervallo. |
| MODALITÀ ESCLUSIVA \_ IRLMP \_ |     |     | DWORD (booleano) | Imposta il socket per ignorare il livello TinyTP per comunicare direttamente con IrLMP. |
| IRLMP \_ IAS \_ QUERY      | sì |     | **IAS \_ QUERY**  | Esegue una query IAS su un servizio e un nome di classe specifici per i relativi attributi.      |
| IRLMP \_ IAS \_ SET        |     | sì | **IAS \_ SET**    | Imposta un valore di attributo per un nome di classe e un attributo in IAS. |
| MODALITÀ \_ IRLMP \_ IRLPT     |     | sì | DWORD (booleano) | Consente la comunicazione con stampanti con funzionalità di IR.                        |
| PARAMETRI \_ IRLMP      |     |     |                 |                                                                        |
| LEN \_ PDU INVIO IRLMP \_ \_  | sì |     | DWORD           | Recupera la lunghezza massima della PDU necessaria per usare IRLMP \_ 9WIRE \_ MODE.   |
| MODALITÀ SHARP DI \_ IRLMP \_     |     | sì |                 |                                                                        |
| MODALITÀ \_ TINYTP IRLMP \_    |     | sì |                 |                                                                        |
| MODALITÀ IRLMP \_ \_ 9WIRE     | sì | sì | DWORD (booleano) | Attiva la modalità IrCOMM per il socket IrDA.                                 |



 

</dt> </dl> </dd> <dt><span id="Windows_Support_for_SOL_IRLMP_options"></span><span id="windows_support_for_sol_irlmp_options"></span><span id="WINDOWS_SUPPORT_FOR_SOL_IRLMP_OPTIONS"></span>**Windows Supporto per le \_ opzioni SOL IRLMP**</dt> <dd> <dl> <dt> 

| Opzione                            | Windows 7 | Windows Server 2008 | Windows Vista | Windows Server 2003 | Windows XP | Windows 2000 | Windows Me, Windows 98 | Windows NT 4.0 |
|-----------------------------------|-----------|---------------------|---------------|---------------------|------------|--------------|------------------------|----------------|
| MODALITÀ DI INDIVIDUAZIONE IRLMP \_ \_<br/> |           |                     |               |                     |            |              | x                      |                |
| IRLMP \_ ENUMDEVICES<br/>     | x         | x                   | x             | x                   | x          | x            | x                      |                |
| MODALITÀ ESCLUSIVA \_ IRLMP \_<br/> |           |                     |               |                     |            |              |                        |                |
| IRLMP \_ IAS \_ QUERY<br/>      | x         | x                   | x             | x                   | x          | x            | x                      |                |
| IRLMP \_ IAS \_ SET<br/>        | x         | x                   | x             | x                   | x          | x            | x                      |                |
| MODALITÀ \_ IRLMP \_ IRLPT<br/>     | x         | x                   | x             | x                   | x          | x            |                        |                |
| PARAMETRI \_ IRLMP<br/>      |           |                     |               |                     |            |              | x                      |                |
| LEN \_ PDU INVIO IRLMP \_ \_<br/>  | x         | x                   | x             | x                   | x          | x            |                        |                |
| MODALITÀ SHARP DI \_ IRLMP \_<br/>     |           |                     |               |                     |            |              |                        |                |
| MODALITÀ \_ TINYTP IRLMP \_<br/>    |           |                     |               |                     |            |              | x                      |                |
| MODALITÀ IRLMP \_ \_ 9WIRE<br/>     | x         | x                   | x             | x                   | x          | x            |                        |                |



 


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Commenti

Le opzioni del socket **\_ SOL IRLMP** e le strutture usate da queste opzioni del socket sono definite nel file di intestazione *Af \_ irda.h.*

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|---------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>Af \_ irda.h</dt> </dl> |



 

 




