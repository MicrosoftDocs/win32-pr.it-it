---
title: Bluetooth e WSALookupServiceNext
description: Bluetooth usa la funzione WSALookupServiceNext per trovare la corrispondenza con le query specificate in una precedente chiamata a WSALookupServiceBegin.
ms.assetid: d43cf444-adb6-4313-9614-a8d6d868a88f
keywords:
- Bluetooth
- WSALookupServiceNext
- Bluetooth e WSALookupServiceNext
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9d3ece06e27c9e80e25f22ef0fb09a5790cdf69b
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "103872578"
---
# <a name="bluetooth-and-wsalookupservicenext"></a>Bluetooth e WSALookupServiceNext

Bluetooth usa la funzione [**WSALookupServiceNext**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicenexta) per trovare la corrispondenza con le query specificate in una precedente chiamata a [**WSALookupServiceBegin**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicebegina). I risultati della funzione **WSALookupServiceNext** sono determinati dalle impostazioni definite nella struttura [**WSAQUERYSET**](/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw) passata nella chiamata di funzione **WSALookupServiceBegin** iniziale.

I passaggi per la richiesta del dispositivo e l'individuazione dei servizi in Bluetooth sono sufficientemente diversi per meritare un trattamento distinto. Per altre informazioni su Bluetooth e sulla funzione [**WSALookupServiceBegin**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicebegina) per le richieste dei dispositivi, vedere [Bluetooth e WSALookupServiceBegin per la richiesta del dispositivo](bluetooth-and-wsalookupservicebegin-for-device-inquiry.md). Per ulteriori informazioni su Bluetooth e sulla funzione **WSALookupServiceBegin** per l'individuazione del servizio, vedere [Bluetooth e WSALookupServiceBegin per l'individuazione del servizio](bluetooth-and-wsalookupservicebegin-for-service-discovery.md).

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

[**\_servizio query \_ BTH**](/windows/desktop/api/Ws2bth/ns-ws2bth-bth_query_service)
</dt> <dt>

[**connessione**](/windows/desktop/api/winsock2/nf-winsock2-connect)
</dt> <dt>

[**\_BTH sockaddr**](/windows/desktop/api/Ws2bth/ns-ws2bth-sockaddr_bth)
</dt> <dt>

[**WSALookupServiceBegin**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicebegina)
</dt> <dt>

[**WSALookupServiceEnd**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupserviceend)
</dt> <dt>

[**WSALookupServiceNext**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicenexta)
</dt> <dt>

[**WSAQUERYSET**](/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw)
</dt> </dl>

 

 