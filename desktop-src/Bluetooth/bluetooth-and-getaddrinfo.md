---
title: Bluetooth e funzione getaddrinfo
description: La funzione funzione getaddrinfo fornisce la conversione dal nome host all'indirizzo per i trasporti basati su IP. Poiché la funzione funzione getaddrinfo è specifica per i trasporti basati su IP, l'operazione ha esito negativo sui socket Bluetooth.
ms.assetid: e17d8542-d4bc-499c-bae4-1f41bff493c3
keywords:
- Bluetooth e funzione getaddrinfo Bluetooth
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 96c2e62b83ac947b74479ff435b93914661aa8da
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "103729850"
---
# <a name="bluetooth-and-getaddrinfo"></a>Bluetooth e funzione getaddrinfo

La funzione [**funzione getaddrinfo**](/windows/desktop/api/ws2tcpip/nf-ws2tcpip-getaddrinfo) fornisce la conversione dal nome host all'indirizzo per i trasporti basati su IP. Poiché la funzione **funzione getaddrinfo** è specifica per i trasporti basati su IP, l'operazione ha esito negativo sui socket Bluetooth.

Per eseguire la conversione dal nome host all'indirizzo per i Socket Bluetooth, usare la funzione [**WSALookupServiceBegin**](bluetooth-and-wsalookupservicebegin-for-device-inquiry.md) con i **\_ contenitori LUP** per eseguire query sui dispositivi remoti, quindi cercare un nome remoto e un indirizzo corrispondente specifici corrispondenti.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Windows Sockets](/windows/desktop/WinSock/windows-sockets-start-page-2)
</dt> <dt>

[**funzione getaddrinfo**](/windows/desktop/api/ws2tcpip/nf-ws2tcpip-getaddrinfo)
</dt> <dt>

[**WSALookupServiceBegin**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicebegina)
</dt> </dl>

 

 