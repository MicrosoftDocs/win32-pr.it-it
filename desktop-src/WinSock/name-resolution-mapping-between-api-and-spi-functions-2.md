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
# <a name="name-resolution-mapping-between-api-and-spi-functions"></a>Mapping della risoluzione dei nomi tra le funzioni API e SPI

L'installazione delle classi di servizio, la registrazione delle istanze del servizio e le operazioni di query di base sono tutte mappate equamente direttamente dall'API a SPI. La funzione [**WSAGetServiceClassNameByClassId**](/windows/desktop/api/Winsock2/nf-winsock2-wsagetserviceclassnamebyclassida) non dispone di una funzione corrispondente in SPI, perché questa funzione è implementata in WS2 \_32.dll effettuando una chiamata a [**NSPGetServiceClassInfo**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpnspgetserviceclassinfo).

Le funzioni di supporto [**WSAAddressToString**](/windows/desktop/api/Winsock2/nf-winsock2-wsaaddresstostringa) e [**WSAStringToAddress non**](/windows/desktop/api/Winsock2/nf-winsock2-wsastringtoaddressa) sono mappate alle funzioni corrispondenti nell'API di trasporto, perché solo un provider di trasporto saprà necessariamente come eseguire la conversione in una struttura [**sockaddr**](sockaddr-2.md) .

 

 



