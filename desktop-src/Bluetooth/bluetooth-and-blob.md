---
title: Bluetooth e BLOB
description: Bluetooth usa la struttura BLOB per passare o ricevere dati specifici del trasporto alla struttura WSAQUERYSET durante le chiamate alle funzioni WSASetService o WSALookupService\.
ms.assetid: d71f3661-0efb-4376-966c-fb5c340ce1c5
keywords:
- BLOB
- Bluetooth
- Bluetooth
- Bluetooth e BLOB
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 960362e7f6bc6388d3b93bd6e0329e405bdb33ed6e796a5ec5793d402ba0557c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119081135"
---
# <a name="bluetooth-and-blob"></a>Bluetooth e BLOB

Bluetooth usa la struttura [**BLOB**](/windows/desktop/api/nspapi/ns-nspapi-blob) per passare o ricevere dati specifici del trasporto alla struttura [**WSAQUERYSET**](bluetooth-and-wsaqueryset-for-set-service.md) durante le chiamate alle funzioni [**WSASetService**](bluetooth-and-wsasetservice.md) **o WSALookupService.** \*

Per l'Bluetooth e [**la funzione WSASetService,**](bluetooth-and-wsasetservice.md) i membri della struttura [**BLOB**](/windows/desktop/api/nspapi/ns-nspapi-blob) devono avere le impostazioni seguenti:

-   Il **membro cbsize** deve essere impostato sulla dimensione della struttura [**BTH SET \_ \_ SERVICE**](/windows/desktop/api/Ws2bth/ns-ws2bth-bth_set_service) usata nel membro **pBlobData,** in byte.
-   Il **membro pBlobData** deve essere un puntatore a una [**struttura BTH SET \_ \_ SERVICE.**](/windows/desktop/api/Ws2bth/ns-ws2bth-bth_set_service)

Per l'uso con Bluetooth [e WSALookupServiceBegin per Device Inquiry,](bluetooth-and-wsalookupservicebegin-for-device-inquiry.md)usare le impostazioni seguenti:

-   Il **membro cbsize** deve essere impostato sulla dimensione della struttura [**BTH QUERY \_ \_ DEVICE**](/windows/desktop/api/Ws2bth/ns-ws2bth-bth_query_device) usata nel membro **pBlobData,** in byte.
-   Il **membro pBlobData** deve essere un puntatore a una [**struttura BTH QUERY \_ \_ DEVICE.**](/windows/desktop/api/Ws2bth/ns-ws2bth-bth_query_device)

Per l'Bluetooth [e WSALookupServiceBegin](bluetooth-and-wsalookupservicebegin-for-service-discovery.md)per l'individuazione del servizio, usare le impostazioni seguenti:

-   Il **membro cbsize** deve essere impostato sulla dimensione della struttura [**BTH QUERY \_ \_ SERVICE**](/windows/desktop/api/Ws2bth/ns-ws2bth-bth_query_service) usata nel membro **pBlobData,** in byte.
-   Il **membro pBlobData** deve essere un puntatore a una [**struttura BTH QUERY \_ \_ SERVICE.**](/windows/desktop/api/Ws2bth/ns-ws2bth-bth_query_service)

Per altre informazioni, vedere la sezione Osservazioni nella pagina di riferimento sulla struttura [**BTH \_ SET \_ SERVICE.**](/windows/desktop/api/Ws2bth/ns-ws2bth-bth_set_service)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Bluetooth e WSALookupServiceBegin per la richiesta dei dispositivi](bluetooth-and-wsalookupservicebegin-for-device-inquiry.md)
</dt> <dt>

[Bluetooth e WSALookupServiceBegin per l'individuazione dei servizi](bluetooth-and-wsalookupservicebegin-for-service-discovery.md)
</dt> <dt>

[Bluetooth e WSASetService](bluetooth-and-wsasetservice.md)
</dt> <dt>

[Windows Sockets](/windows/desktop/WinSock/windows-sockets-start-page-2)
</dt> <dt>

[**Blob**](/windows/desktop/api/nspapi/ns-nspapi-blob)
</dt> <dt>

[**DISPOSITIVO DI QUERY BTH \_ \_**](/windows/desktop/api/Ws2bth/ns-ws2bth-bth_query_device)
</dt> <dt>

[**SERVIZIO QUERY BTH \_ \_**](/windows/desktop/api/Ws2bth/ns-ws2bth-bth_query_service)
</dt> <dt>

[**SERVIZIO SET \_ \_ BTH**](/windows/desktop/api/Ws2bth/ns-ws2bth-bth_set_service)
</dt> <dt>

[**WSALookupServiceBegin**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicebegina)
</dt> <dt>

[**WSAQUERYSET**](/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw)
</dt> <dt>

[**WSASetService**](bluetooth-and-wsasetservice.md)
</dt> </dl>

 

 