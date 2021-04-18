---
title: Bluetooth e BLOB
description: Bluetooth usa la struttura BLOB per passare o ricevere dati specifici del trasporto alla struttura WSAQUERYSET durante le chiamate a WSASetService o WSALookupService \ functions.
ms.assetid: d71f3661-0efb-4376-966c-fb5c340ce1c5
keywords:
- BLOB
- Bluetooth
- Bluetooth
- Bluetooth e BLOB
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 385f4fab053f975672d3b94fa231b3d7632e58eb
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "106300342"
---
# <a name="bluetooth-and-blob"></a>Bluetooth e BLOB

Bluetooth usa la struttura [**BLOB**](/windows/desktop/api/nspapi/ns-nspapi-blob) per passare o ricevere dati specifici del trasporto alla struttura [**WSAQUERYSET**](bluetooth-and-wsaqueryset-for-set-service.md) durante le chiamate alle funzioni [**WSASetService**](bluetooth-and-wsasetservice.md) o **WSALookupService** \* .

Per l'uso con Bluetooth e la funzione [**WSASetService**](bluetooth-and-wsasetservice.md) , è necessario che i membri della struttura [**BLOB**](/windows/desktop/api/nspapi/ns-nspapi-blob) dispongano delle impostazioni seguenti:

-   Il membro **cbSize** deve essere impostato sulla dimensione della struttura del [**\_ \_ servizio del set di BTH**](/windows/desktop/api/Ws2bth/ns-ws2bth-bth_set_service) utilizzata nel membro **pBlobData** , in byte.
-   Il membro **pBlobData** deve essere un puntatore a una struttura del [**\_ \_ servizio set BTH**](/windows/desktop/api/Ws2bth/ns-ws2bth-bth_set_service) .

Per l'uso con Bluetooth e [WSALookupServiceBegin per la richiesta del dispositivo](bluetooth-and-wsalookupservicebegin-for-device-inquiry.md), usare le impostazioni seguenti:

-   Il membro **cbSize** deve essere impostato sulla dimensione della struttura del [**\_ \_ dispositivo di query BTH**](/windows/desktop/api/Ws2bth/ns-ws2bth-bth_query_device) utilizzata nel membro **pBlobData** , in byte.
-   Il membro **pBlobData** deve essere un puntatore a una struttura di [**\_ \_ dispositivi di query BTH**](/windows/desktop/api/Ws2bth/ns-ws2bth-bth_query_device) .

Per l'uso con Bluetooth e [WSALookupServiceBegin per l'individuazione del servizio](bluetooth-and-wsalookupservicebegin-for-service-discovery.md), usare le impostazioni seguenti:

-   Il membro **cbSize** deve essere impostato sulla dimensione della struttura del [**\_ \_ servizio query BTH**](/windows/desktop/api/Ws2bth/ns-ws2bth-bth_query_service) utilizzata nel membro **pBlobData** , in byte.
-   Il membro **pBlobData** deve essere un puntatore a una struttura del [**\_ \_ servizio query BTH**](/windows/desktop/api/Ws2bth/ns-ws2bth-bth_query_service) .

Per ulteriori informazioni, vedere la sezione Osservazioni nella pagina di riferimento relativa alla struttura del [**\_ set di \_ Servizi BTH**](/windows/desktop/api/Ws2bth/ns-ws2bth-bth_set_service) .

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Bluetooth e WSALookupServiceBegin per la richiesta del dispositivo](bluetooth-and-wsalookupservicebegin-for-device-inquiry.md)
</dt> <dt>

[Bluetooth e WSALookupServiceBegin per l'individuazione del servizio](bluetooth-and-wsalookupservicebegin-for-service-discovery.md)
</dt> <dt>

[Bluetooth e WSASetService](bluetooth-and-wsasetservice.md)
</dt> <dt>

[Windows Sockets](/windows/desktop/WinSock/windows-sockets-start-page-2)
</dt> <dt>

[**BLOB**](/windows/desktop/api/nspapi/ns-nspapi-blob)
</dt> <dt>

[**\_dispositivo di query BTH \_**](/windows/desktop/api/Ws2bth/ns-ws2bth-bth_query_device)
</dt> <dt>

[**\_servizio query \_ BTH**](/windows/desktop/api/Ws2bth/ns-ws2bth-bth_query_service)
</dt> <dt>

[**\_servizio set \_ BTH**](/windows/desktop/api/Ws2bth/ns-ws2bth-bth_set_service)
</dt> <dt>

[**WSALookupServiceBegin**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicebegina)
</dt> <dt>

[**WSAQUERYSET**](/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw)
</dt> <dt>

[**WSASetService**](bluetooth-and-wsasetservice.md)
</dt> </dl>

 

 