---
title: Bluetooth e getaddrinfo
description: La funzione getaddrinfo fornisce la conversione dal nome host all'indirizzo per i trasporti basati su IP. Poiché la funzione getaddrinfo è specifica per i trasporti basati su IP, non riesce Bluetooth socket.
ms.assetid: e17d8542-d4bc-499c-bae4-1f41bff493c3
keywords:
- Bluetooth e getaddrinfo Bluetooth
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: de9faea4cebf9eee183942da04f39dfae123feea4900483d27ae2d70d8cb5b82
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120004531"
---
# <a name="bluetooth-and-getaddrinfo"></a>Bluetooth e getaddrinfo

La [**funzione getaddrinfo**](/windows/desktop/api/ws2tcpip/nf-ws2tcpip-getaddrinfo) fornisce la conversione dal nome host all'indirizzo per i trasporti basati su IP. Poiché la **funzione getaddrinfo** è specifica per i trasporti basati su IP, non riesce Bluetooth socket.

Per eseguire la conversione dal nome host all'indirizzo per i socket Bluetooth, usare la funzione [**WSALookupServiceBegin**](bluetooth-and-wsalookupservicebegin-for-device-inquiry.md) con **CONTENITORI LUP \_** per eseguire query sui dispositivi remoti, quindi cercare un nome remoto e un indirizzo corrispondenti corrispondenti.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Windows Sockets](/windows/desktop/WinSock/windows-sockets-start-page-2)
</dt> <dt>

[**getaddrinfo**](/windows/desktop/api/ws2tcpip/nf-ws2tcpip-getaddrinfo)
</dt> <dt>

[**WSALookupServiceBegin**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicebegina)
</dt> </dl>

 

 