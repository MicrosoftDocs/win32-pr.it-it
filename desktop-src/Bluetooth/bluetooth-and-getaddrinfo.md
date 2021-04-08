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
# <a name="bluetooth-and-getaddrinfo"></a><span data-ttu-id="a3d78-105">Bluetooth e funzione getaddrinfo</span><span class="sxs-lookup"><span data-stu-id="a3d78-105">Bluetooth and getaddrinfo</span></span>

<span data-ttu-id="a3d78-106">La funzione [**funzione getaddrinfo**](/windows/desktop/api/ws2tcpip/nf-ws2tcpip-getaddrinfo) fornisce la conversione dal nome host all'indirizzo per i trasporti basati su IP.</span><span class="sxs-lookup"><span data-stu-id="a3d78-106">The [**getaddrinfo**](/windows/desktop/api/ws2tcpip/nf-ws2tcpip-getaddrinfo) function provides translation from host name to address for IP-based transports.</span></span> <span data-ttu-id="a3d78-107">Poiché la funzione **funzione getaddrinfo** è specifica per i trasporti basati su IP, l'operazione ha esito negativo sui socket Bluetooth.</span><span class="sxs-lookup"><span data-stu-id="a3d78-107">Because the **getaddrinfo** function is specific to IP-based transports, it fails on Bluetooth sockets.</span></span>

<span data-ttu-id="a3d78-108">Per eseguire la conversione dal nome host all'indirizzo per i Socket Bluetooth, usare la funzione [**WSALookupServiceBegin**](bluetooth-and-wsalookupservicebegin-for-device-inquiry.md) con i **\_ contenitori LUP** per eseguire query sui dispositivi remoti, quindi cercare un nome remoto e un indirizzo corrispondente specifici corrispondenti.</span><span class="sxs-lookup"><span data-stu-id="a3d78-108">To perform translation from host name to address for Bluetooth sockets, use the [**WSALookupServiceBegin**](bluetooth-and-wsalookupservicebegin-for-device-inquiry.md) function with **LUP\_CONTAINERS** to query remote devices, then search for a specific matching Remote Name and corresponding address.</span></span>

## <a name="related-topics"></a><span data-ttu-id="a3d78-109">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="a3d78-109">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a3d78-110">Windows Sockets</span><span class="sxs-lookup"><span data-stu-id="a3d78-110">Windows Sockets</span></span>](/windows/desktop/WinSock/windows-sockets-start-page-2)
</dt> <dt>

[<span data-ttu-id="a3d78-111">**funzione getaddrinfo**</span><span class="sxs-lookup"><span data-stu-id="a3d78-111">**getaddrinfo**</span></span>](/windows/desktop/api/ws2tcpip/nf-ws2tcpip-getaddrinfo)
</dt> <dt>

[<span data-ttu-id="a3d78-112">**WSALookupServiceBegin**</span><span class="sxs-lookup"><span data-stu-id="a3d78-112">**WSALookupServiceBegin**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicebegina)
</dt> </dl>

 

 