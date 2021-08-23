---
title: Bluetooth e WSAQUERYSET per la richiesta di dispositivi
description: Usato per facilitare l'individuazione di dispositivi e servizi nello spazio dei nomi Bluetooth, NS \_ BTH.
ms.assetid: 0c0d26f7-b6c3-42a9-8c01-118278c381cc
keywords:
- Bluetooth e WSAQUERYSET per richieste Bluetooth
- WSAQUERYSET Bluetooth , per la richiesta del dispositivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 75a9250670fda52f2ecdc27ffee949b12049b8ec2860b7ee2df23631c4469076
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118959280"
---
# <a name="bluetooth-and-wsaqueryset-for-device-inquiry"></a>Bluetooth e WSAQUERYSET per la richiesta di dispositivi

In Bluetooth, la struttura [**WSAQUERYSET**](/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw) viene usata per facilitare l'individuazione di dispositivi e servizi nello spazio dei nomi Bluetooth, NS \_ BTH.

Le [**funzioni WSALookupServiceBegin**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicebegina) e [**WSALookupServiceNext**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicenexta) usano la struttura [**WSAQUERYSET**](/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw) per ottenere informazioni sul processo di richiesta del dispositivo. Nella tabella seguente vengono elencati e descritti i valori dei membri **nella struttura WSAQUERYSET.**

| Membro                      | Input per WSALookupServiceBegin con contenitori LUP \_ specificati                                                                                                                                              | Valore restituito da WSALookupServiceNext                                                                                                                                                                                                                                                                                                                                                                                        |
|-----------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **dwSize**                  | Deve essere impostato su **sizeof**([**WSAQUERYSET**](/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw)).                                                                                                                                       | **sizeof**([**WSAQUERYSET**](/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw)) restituito dal sistema.                                                                                                                                                                                                                                                                                                                                                        |
| **dwOutputFlags**           | Non usato.                                                                                                                                                                                                  | Può avere uno o più di questi flag impostati: **BTHNS \_ RESULT \_ DEVICE \_ CONNECTED** Specifica che il dispositivo è connesso.<br/> **BTHNS \_ RESULT \_ DEVICE \_ REMEMBERED** Specifica che il dispositivo è un dispositivo memorizzata. Non tutti i dispositivi memorizzati vengono autenticati.<br/> **BTHNS \_ RESULT \_ DEVICE \_ AUTHENTICATED** Specifica che il dispositivo è autenticato, associato o obbligato. Tutti i dispositivi autenticati vengono memorizzati.<br/> |
| **lpszServiceInstanceName** | Non usato.                                                                                                                                                                                                  | Nome visualizzato del dispositivo, originariamente restituito da un'Bluetooth richiesta di nome remoto ed eventualmente aggiornato dall'utente locale. Restituito se **l'opzione LUP \_ RETURN \_ NAME** è specificata.                                                                                                                                                                                                                                         |
| **lpServiceClassId**        | Non usato.                                                                                                                                                                                                  | Campo della classe Bluetooth dispositivo (COD) a 32 bit mappato al membro **Data1** del GUID. Restituito se **l'opzione LUP \_ RETURN \_ TYPE** è specificata.                                                                                                                                                                                                                                                                                    |
| **lpVersion**               | Non usato.                                                                                                                                                                                                  | Non usato.                                                                                                                                                                                                                                                                                                                                                                                                                       |
| **lpszComment**             | Non usato.                                                                                                                                                                                                  | Non usato.                                                                                                                                                                                                                                                                                                                                                                                                                       |
| **dwNameSpace**             | Deve essere NS \_ BTH.                                                                                                                                                                                           | Restituisce **NS \_ BTH.**                                                                                                                                                                                                                                                                                                                                                                                                            |
| **lpNSProviderId**          | Non usato.                                                                                                                                                                                                  | Non usato.                                                                                                                                                                                                                                                                                                                                                                                                                       |
| **lpszContext**             | Non usato.                                                                                                                                                                                                  | Non usato.                                                                                                                                                                                                                                                                                                                                                                                                                       |
| **dwNumberOfProtocols**     | Non usato.                                                                                                                                                                                                  | Non usato.                                                                                                                                                                                                                                                                                                                                                                                                                       |
| **lpafpProtocols**          | Non usato.                                                                                                                                                                                                  | Non usato.                                                                                                                                                                                                                                                                                                                                                                                                                       |
| **lpszQueryString**         | Non usato.                                                                                                                                                                                                  | Non usato.                                                                                                                                                                                                                                                                                                                                                                                                                       |
| **dwNumberOfCsAddrs**       | Non usato.                                                                                                                                                                                                  | Indica il numero di elementi nella matrice di [**strutture CSADDR \_ INFO.**](/windows/desktop/api/nspapi/ns-nspapi-csaddr_info)                                                                                                                                                                                                                                                                                                                          |
| **lpcsaBuffer**             | Non usato.                                                                                                                                                                                                  | Puntatore a una struttura [**CSADDR \_ INFO**](/windows/desktop/api/nspapi/ns-nspapi-csaddr_info) con il relativo membro **LocalAddr.lpSockaddr** che punta a una struttura [**SOCKADDR \_ BTH**](/windows/desktop/api/Ws2bth/ns-ws2bth-sockaddr_bth) con l'indirizzo del dispositivo remoto. Restituito se **l'opzione LUP \_ RETURN \_ ADDR** è specificata.                                                                                                                                                                  |
| **lpBlob**                  | facoltativo. Può puntare a una [**struttura BLOB**](/windows/desktop/api/nspapi/ns-nspapi-blob) che punta a una struttura [**BTH QUERY \_ \_ DEVICE**](/windows/desktop/api/Ws2bth/ns-ws2bth-bth_query_device) che può limitare la lunghezza delle operazioni di richiesta dei dispositivi non memorizzate nella cache. | Puntatore a [**una struttura BLOB**](/windows/desktop/api/nspapi/ns-nspapi-blob) che punta a una struttura [**BTH DEVICE \_ \_ INFO.**](/windows/desktop/api/Bthdef/ns-bthdef-bth_device_info) **LpBlob viene** restituito se **viene specificato LUP RETURN \_ \_ BLOB.** Specificare **LUP \_ RETURN NAME \_ per** recuperare il campo del nome di **BTH DEVICE \_ \_ INFO**.                                                                                                                                                     |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Bluetooth e WSAQUERYSET per Set Service](bluetooth-and-wsaqueryset-for-set-service.md)
</dt> <dt>

[Bluetooth e WSAQUERYSET per la richiesta di assistenza](bluetooth-and-wsaqueryset-for-service-inquiry.md)
</dt> <dt>

[Bluetooth e BLOB](bluetooth-and-blob.md)
</dt> <dt>

[Bluetooth e WSALookupServiceBegin](bluetooth-and-wsasetservice.md)
</dt> <dt>

[Bluetooth e WSALookupServiceNext](bluetooth-and-wsasetservice.md)
</dt> <dt>

[**Blob**](/windows/desktop/api/nspapi/ns-nspapi-blob)
</dt> <dt>

[**INFORMAZIONI SUL DISPOSITIVO BTH \_ \_**](/windows/desktop/api/Bthdef/ns-bthdef-bth_device_info)
</dt> <dt>

[**BTH \_ QUERY \_ DEVICE**](/windows/desktop/api/Ws2bth/ns-ws2bth-bth_query_device)
</dt> <dt>

[**CSADDR \_ INFO**](/windows/desktop/api/nspapi/ns-nspapi-csaddr_info)
</dt> <dt>

[**SOCKADDR \_ BTH**](/windows/desktop/api/Ws2bth/ns-ws2bth-sockaddr_bth)
</dt> <dt>

[**WSAQUERYSET**](/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw)
</dt> <dt>

[Windows Sockets](/windows/desktop/WinSock/windows-sockets-start-page-2)
</dt> </dl>

 

