---
title: Bluetooth e WSAQUERYSET per la richiesta del dispositivo
description: Usato per facilitare l'individuazione di dispositivi e servizi nello spazio dei nomi Bluetooth, NS \_ BTH.
ms.assetid: 0c0d26f7-b6c3-42a9-8c01-118278c381cc
keywords:
- Bluetooth e WSAQUERYSET per la richiesta di dispositivo Bluetooth
- WSAQUERYSET Bluetooth, per la richiesta del dispositivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7de7adf8c15907fe539ddac5133df08d68ee7c4f
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "103727642"
---
# <a name="bluetooth-and-wsaqueryset-for-device-inquiry"></a>Bluetooth e WSAQUERYSET per la richiesta del dispositivo

In Bluetooth la struttura [**WSAQUERYSET**](/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw) viene usata per facilitare l'individuazione di dispositivi e servizi nello spazio dei nomi Bluetooth, NS \_ BTH.

Le funzioni [**WSALookupServiceBegin**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicebegina) e [**WSALookupServiceNext**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicenexta) usano la struttura [**WSAQUERYSET**](/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw) per ottenere informazioni sul processo di richiesta del dispositivo. Nella tabella seguente sono elencati e descritti i valori dei membri nella struttura **WSAQUERYSET** .

| Membro                      | Input per WSALookupServiceBegin con i \_ contenitori LUP specificati                                                                                                                                              | Valore restituito da WSALookupServiceNext                                                                                                                                                                                                                                                                                                                                                                                        |
|-----------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **dwSize**                  | Deve essere impostato su **sizeof**([**WSAQUERYSET**](/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw)).                                                                                                                                       | **sizeof**([**WSAQUERYSET**](/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw)) restituito dal sistema.                                                                                                                                                                                                                                                                                                                                                        |
| **dwOutputFlags**           | Non usato.                                                                                                                                                                                                  | È possibile che uno o più dei flag impostati siano impostati: il **\_ dispositivo BTHNS result \_ \_ Connected** indica che il dispositivo è connesso.<br/> **BTHNS \_ Il \_ dispositivo \_ di risultati memorizzato** indica che il dispositivo è un dispositivo memorizzato. Non vengono autenticati tutti i dispositivi memorizzati.<br/> **BTHNS \_ RISULTATO \_ \_ autenticato del dispositivo** : specifica che il dispositivo è autenticato, abbinato o associato. Tutti i dispositivi autenticati vengono memorizzati.<br/> |
| **lpszServiceInstanceName** | Non usato.                                                                                                                                                                                                  | Nome visualizzato del dispositivo, originariamente restituito da un'operazione di richiesta di nome remoto Bluetooth e possibilmente aggiornato dall'utente locale. Restituito se viene specificato il **\_ \_ nome restituito di LUP** .                                                                                                                                                                                                                                         |
| **lpServiceClassId**        | Non usato.                                                                                                                                                                                                  | Il campo della classe del dispositivo (COD) Bluetooth a 32 bit mappato al membro **Data1** del GUID. Restituito se viene specificato il **\_ \_ tipo restituito LUP** .                                                                                                                                                                                                                                                                                    |
| **lpVersion**               | Non usato.                                                                                                                                                                                                  | Non usato.                                                                                                                                                                                                                                                                                                                                                                                                                       |
| **lpszComment**             | Non usato.                                                                                                                                                                                                  | Non usato.                                                                                                                                                                                                                                                                                                                                                                                                                       |
| **dwNameSpace**             | Deve essere NS \_ BTH.                                                                                                                                                                                           | Restituisce **NS \_ BTH**.                                                                                                                                                                                                                                                                                                                                                                                                            |
| **lpNSProviderId**          | Non usato.                                                                                                                                                                                                  | Non usato.                                                                                                                                                                                                                                                                                                                                                                                                                       |
| **lpszContext**             | Non usato.                                                                                                                                                                                                  | Non usato.                                                                                                                                                                                                                                                                                                                                                                                                                       |
| **dwNumberOfProtocols**     | Non usato.                                                                                                                                                                                                  | Non usato.                                                                                                                                                                                                                                                                                                                                                                                                                       |
| **lpafpProtocols**          | Non usato.                                                                                                                                                                                                  | Non usato.                                                                                                                                                                                                                                                                                                                                                                                                                       |
| **lpszQueryString**         | Non usato.                                                                                                                                                                                                  | Non usato.                                                                                                                                                                                                                                                                                                                                                                                                                       |
| **dwNumberOfCsAddrs**       | Non usato.                                                                                                                                                                                                  | Indica il numero di elementi nella matrice di strutture [**di \_ informazioni CSADDR**](/windows/desktop/api/nspapi/ns-nspapi-csaddr_info) .                                                                                                                                                                                                                                                                                                                          |
| **lpcsaBuffer**             | Non usato.                                                                                                                                                                                                  | Puntatore a una struttura di [**\_ informazioni CSADDR**](/windows/desktop/api/nspapi/ns-nspapi-csaddr_info) con il membro **LocalAddr. lpSockaddr** che punta a una struttura [**sockaddr \_ BTH**](/windows/desktop/api/Ws2bth/ns-ws2bth-sockaddr_bth) con l'indirizzo del dispositivo remoto. Restituito se viene specificato **LUP \_ return \_ addr** .                                                                                                                                                                  |
| **lpBlob**                  | facoltativo. Può puntare a una struttura [**BLOB**](/windows/desktop/api/nspapi/ns-nspapi-blob) che punta a una struttura di [**\_ \_ dispositivi di query BTH**](/windows/desktop/api/Ws2bth/ns-ws2bth-bth_query_device) che può limitare la durata delle operazioni di richiesta di dispositivi non memorizzati nella cache. | Puntatore a una struttura [**BLOB**](/windows/desktop/api/nspapi/ns-nspapi-blob) che punta a una struttura di [**\_ \_ informazioni sul dispositivo BTH**](/windows/desktop/api/Bthdef/ns-bthdef-bth_device_info) . **lpBlob** viene restituito se viene specificato **LUP \_ return \_ BLOB** . Specificare **il \_ \_ nome restituito LUP** per recuperare il campo nome **delle \_ \_ informazioni sul dispositivo BTH**.                                                                                                                                                     |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Bluetooth e WSAQUERYSET per il servizio set](bluetooth-and-wsaqueryset-for-set-service.md)
</dt> <dt>

[Bluetooth e WSAQUERYSET per la richiesta di assistenza](bluetooth-and-wsaqueryset-for-service-inquiry.md)
</dt> <dt>

[Bluetooth e BLOB](bluetooth-and-blob.md)
</dt> <dt>

[Bluetooth e WSALookupServiceBegin](bluetooth-and-wsasetservice.md)
</dt> <dt>

[Bluetooth e WSALookupServiceNext](bluetooth-and-wsasetservice.md)
</dt> <dt>

[**BLOB**](/windows/desktop/api/nspapi/ns-nspapi-blob)
</dt> <dt>

[**\_informazioni sul dispositivo BTH \_**](/windows/desktop/api/Bthdef/ns-bthdef-bth_device_info)
</dt> <dt>

[**\_dispositivo di query BTH \_**](/windows/desktop/api/Ws2bth/ns-ws2bth-bth_query_device)
</dt> <dt>

[**\_informazioni CSADDR**](/windows/desktop/api/nspapi/ns-nspapi-csaddr_info)
</dt> <dt>

[**\_BTH sockaddr**](/windows/desktop/api/Ws2bth/ns-ws2bth-sockaddr_bth)
</dt> <dt>

[**WSAQUERYSET**](/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw)
</dt> <dt>

[Windows Sockets](/windows/desktop/WinSock/windows-sockets-start-page-2)
</dt> </dl>

 

