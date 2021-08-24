---
title: Bluetooth e WSALookupServiceEnd
description: Bluetooth usa la funzione WSALookupServiceEnd per terminare una query avviata in una chiamata precedente a WSALookupServiceBegin e probabilmente estesa nelle chiamate successive a WSALookupServiceNext.
ms.assetid: 3f901176-2433-4d51-ae52-648abbd2e318
keywords:
- Bluetooth
- WSALookupServiceEnd
- Bluetooth e WSALookupServiceEnd
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8bd6c893a06fbf586d07e3a2581d1d25626e161508e505dc089d7660267bae92
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119081095"
---
# <a name="bluetooth-and-wsalookupserviceend"></a>Bluetooth e WSALookupServiceEnd

Bluetooth usa la funzione [**WSALookupServiceEnd**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupserviceend) per terminare una query avviata in una chiamata precedente a [**WSALookupServiceBegin**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicebegina)e forse estesa nelle chiamate successive a [**WSALookupServiceNext.**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicenexta) La chiamata a **WSALookupServiceEnd** termina la query e pulisce il contesto.

I passaggi per la richiesta di informazioni sui dispositivi e l'individuazione dei servizi Bluetooth sono sufficientemente diversi da separare il trattamento. Per altre informazioni su Bluetooth e sulla funzione [**WSALookupServiceBegin**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicebegina) per le richieste dei dispositivi, vedere [Bluetooth e WSALookupServiceBegin](bluetooth-and-wsalookupservicebegin-for-device-inquiry.md)per richieste di dispositivi. Per altre informazioni sulle Bluetooth e sulla funzione **WSALookupServiceBegin** per l'individuazione dei servizi, vedere [Bluetooth e WSALookupServiceBegin](bluetooth-and-wsalookupservicebegin-for-service-discovery.md)per l'individuazione del servizio.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Individuazione di dispositivi e servizi Bluetooth](discovering-bluetooth-devices-and-services.md)
</dt> <dt>

[Bluetooth e WSALookupServiceBegin per la richiesta del dispositivo](bluetooth-and-wsalookupservicebegin-for-device-inquiry.md)
</dt> <dt>

[Bluetooth e WSALookupServiceBegin per l'individuazione del servizio](bluetooth-and-wsalookupservicebegin-for-service-discovery.md)
</dt> <dt>

[Bluetooth e WSALookupServiceNext](bluetooth-and-wsalookupservicenext.md)
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
</dt> <dt>

[Windows Sockets](/windows/desktop/WinSock/windows-sockets-start-page-2)
</dt> </dl>

 

 