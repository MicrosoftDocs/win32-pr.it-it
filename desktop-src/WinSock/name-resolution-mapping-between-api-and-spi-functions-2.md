---
description: L'installazione di classi del servizio, la registrazione delle istanze del servizio e le operazioni di query di base esequamente eseere mappate direttamente dall'API a SPI.
ms.assetid: 2ae937f6-e0a6-4a02-9838-0a42575bae66
title: Mapping della risoluzione dei nomi tra funzioni API e SPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ad02896ea15fb1b7c7e2aa2e01d9ec0727492da43d0446819dd1f2e04ad591d2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119733625"
---
# <a name="name-resolution-mapping-between-api-and-spi-functions"></a>Mapping della risoluzione dei nomi tra funzioni API e SPI

L'installazione di classi del servizio, la registrazione delle istanze del servizio e le operazioni di query di base esequamente eseere mappate direttamente dall'API a SPI. La [**funzione WSAGetServiceClassNameByClassId**](/windows/desktop/api/Winsock2/nf-winsock2-wsagetserviceclassnamebyclassida) non ha una funzione corrispondente in SPI, perché questa funzione viene implementata in Ws232.dll effettuando una chiamata \_ a [**NSPGetServiceClassInfo**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpnspgetserviceclassinfo).

Le funzioni helper [**WSAAddressToString**](/windows/desktop/api/Winsock2/nf-winsock2-wsaaddresstostringa) e [**WSAStringToAddress**](/windows/desktop/api/Winsock2/nf-winsock2-wsastringtoaddressa) vengono mappate alle funzioni corrispondenti nell'API di trasporto, perché solo un provider di trasporto saprà necessariamente come eseguire la conversione in una [**struttura sockaddr.**](sockaddr-2.md)

 

 



