---
description: L'installazione delle classi di servizio, la registrazione delle istanze del servizio e le operazioni di query di base sono tutte mappate equamente direttamente dall'API a SPI.
ms.assetid: 2ae937f6-e0a6-4a02-9838-0a42575bae66
title: Mapping della risoluzione dei nomi tra le funzioni API e SPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a031ea8af72bb2733fc647c817a850ab7f311b1c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103879201"
---
# <a name="name-resolution-mapping-between-api-and-spi-functions"></a><span data-ttu-id="beb65-103">Mapping della risoluzione dei nomi tra le funzioni API e SPI</span><span class="sxs-lookup"><span data-stu-id="beb65-103">Name Resolution Mapping Between API and SPI Functions</span></span>

<span data-ttu-id="beb65-104">L'installazione delle classi di servizio, la registrazione delle istanze del servizio e le operazioni di query di base sono tutte mappate equamente direttamente dall'API a SPI.</span><span class="sxs-lookup"><span data-stu-id="beb65-104">The installation of service classes, registration of service instances and basic query operations all map fairly directly from the API to the SPI.</span></span> <span data-ttu-id="beb65-105">La funzione [**WSAGetServiceClassNameByClassId**](/windows/desktop/api/Winsock2/nf-winsock2-wsagetserviceclassnamebyclassida) non dispone di una funzione corrispondente in SPI, perché questa funzione è implementata in WS2 \_32.dll effettuando una chiamata a [**NSPGetServiceClassInfo**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpnspgetserviceclassinfo).</span><span class="sxs-lookup"><span data-stu-id="beb65-105">The [**WSAGetServiceClassNameByClassId**](/windows/desktop/api/Winsock2/nf-winsock2-wsagetserviceclassnamebyclassida) function does not have a corresponding function in the SPI, as this function is implemented in Ws2\_32.dll by making a call to [**NSPGetServiceClassInfo**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpnspgetserviceclassinfo).</span></span>

<span data-ttu-id="beb65-106">Le funzioni di supporto [**WSAAddressToString**](/windows/desktop/api/Winsock2/nf-winsock2-wsaaddresstostringa) e [**WSAStringToAddress non**](/windows/desktop/api/Winsock2/nf-winsock2-wsastringtoaddressa) sono mappate alle funzioni corrispondenti nell'API di trasporto, perché solo un provider di trasporto saprà necessariamente come eseguire la conversione in una struttura [**sockaddr**](sockaddr-2.md) .</span><span class="sxs-lookup"><span data-stu-id="beb65-106">The helper functions [**WSAAddressToString**](/windows/desktop/api/Winsock2/nf-winsock2-wsaaddresstostringa) and [**WSAStringToAddress**](/windows/desktop/api/Winsock2/nf-winsock2-wsastringtoaddressa) are mapped to the corresponding functions in the transport API, as only a transport provider will necessarily know how to perform the translation on a [**sockaddr**](sockaddr-2.md) structure.</span></span>

 

 



