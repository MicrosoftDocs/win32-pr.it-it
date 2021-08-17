---
description: Installazione del servizio in Windows Sockets 2 (Winsock) SPI.
ms.assetid: a303fbcf-9122-422a-9b12-d00a5df0fc0f
title: Installazione del servizio in Windows Sockets 2 SPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: faad2431add9b20ebd3358c48469f382596b658de1339525b147b094a7c3786c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117740525"
---
# <a name="service-installation-in-the-windows-sockets-2-spi"></a>Installazione del servizio in Windows Sockets 2 SPI

-   [**NSPInstallServiceClass**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpnspinstallserviceclass)
-   [**NSPRemoveServiceClass**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpnspremoveserviceclass)
-   [**NSPSetService**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpnspsetservice)

Quando la classe di servizio richiesta non esiste già, un client SPI dello spazio dei nomi usa [**NSPInstallServiceClass**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpnspinstallserviceclass) per installare una nuova classe di servizio fornendo un nome di classe del servizio, un GUID per l'identificatore della classe del servizio e una serie di strutture [**WSANSCLASSINFO.**](/windows/desktop/api/Winsock2/ns-winsock2-wsansclassinfow) Queste strutture sono specifiche di uno spazio dei nomi specifico e forniscono valori comuni, ad esempio i numeri di porta TCP consigliati o gli identificatori SAP NetWare. Una classe del servizio può essere rimossa chiamando [**NSPRemoveServiceClass**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpnspremoveserviceclass) e fornendo il GUID corrispondente all'identificatore di classe.

Quando esiste una classe del servizio, è possibile installare o rimuovere istanze specifiche di un servizio tramite [**NSPSetService.**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpnspsetservice) Questa funzione accetta una [**struttura WSAQUERYSET**](/windows/desktop/api/Winsock2/ns-winsock2-wsaquerysetw) come parametro di input insieme a un codice dell'operazione e ai flag dell'operazione. Il codice operativo indica se il servizio viene installato o rimosso. La **struttura WSAQUERYSET** fornisce tutte le informazioni rilevanti sul servizio, inclusi l'identificatore della classe del servizio, il nome del servizio (per questa istanza), l'identificatore dello spazio dei nomi applicabile e le informazioni sul protocollo e un set di indirizzi di trasporto a cui il servizio è in ascolto.

 

 



