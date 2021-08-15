---
title: Bluetooth e WSALookupServiceNext
description: Bluetooth usa la funzione WSALookupServiceNext per trovare la corrispondenza con le query specificate in una chiamata precedente a WSALookupServiceBegin.
ms.assetid: d43cf444-adb6-4313-9614-a8d6d868a88f
keywords:
- Bluetooth
- WSALookupServiceNext
- Bluetooth e WSALookupServiceNext
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7ac95ee58bc0c7da8c95d1b9d4577bdc18bba2236ea1ee13cdbc12fc0d852f5a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118010393"
---
# <a name="bluetooth-and-wsalookupservicenext"></a>Bluetooth e WSALookupServiceNext

Bluetooth usa la [**funzione WSALookupServiceNext**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicenexta) per trovare la corrispondenza con le query specificate in una chiamata precedente a [**WSALookupServiceBegin.**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicebegina) I risultati della **funzione WSALookupServiceNext** sono determinati dalle impostazioni stabilite nella struttura [**WSAQUERYSET**](/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw) passata nella chiamata di funzione **WSALookupServiceBegin** iniziale.

I passaggi per la richiesta di informazioni sui dispositivi e l'individuazione dei servizi Bluetooth sono sufficientemente diversi da separare il trattamento. Per altre informazioni su Bluetooth e sulla funzione [**WSALookupServiceBegin**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicebegina) per le richieste dei dispositivi, vedere [Bluetooth e WSALookupServiceBegin](bluetooth-and-wsalookupservicebegin-for-device-inquiry.md)per richieste di dispositivi. Per altre informazioni sulle Bluetooth e sulla funzione **WSALookupServiceBegin** per l'individuazione dei servizi, vedere [Bluetooth e WSALookupServiceBegin](bluetooth-and-wsalookupservicebegin-for-service-discovery.md)per l'individuazione del servizio.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Individuazione di dispositivi e servizi Bluetooth](discovering-bluetooth-devices-and-services.md)
</dt> <dt>

[Bluetooth e WSALookupServiceBegin per la richiesta del dispositivo](bluetooth-and-wsalookupservicebegin-for-device-inquiry.md)
</dt> <dt>

[Bluetooth e WSALookupServiceBegin per l'individuazione del servizio](bluetooth-and-wsalookupservicebegin-for-service-discovery.md)
</dt> <dt>

[Bluetooth e WSALookupServiceEnd](bluetooth-and-wsalookupserviceend.md)
</dt> <dt>

[**BTH \_ QUERY \_ SERVICE**](/windows/desktop/api/Ws2bth/ns-ws2bth-bth_query_service)
</dt> <dt>

[**connettersi**](/windows/desktop/api/winsock2/nf-winsock2-connect)
</dt> <dt>

[**SOCKADDR \_ BTH**](/windows/desktop/api/Ws2bth/ns-ws2bth-sockaddr_bth)
</dt> <dt>

[**WSALookupServiceBegin**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicebegina)
</dt> <dt>

[**WSALookupServiceEnd**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupserviceend)
</dt> <dt>

[**WSALookupServiceNext**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicenexta)
</dt> <dt>

[**WSAQUERYSET**](/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw)
</dt> </dl>

 

 