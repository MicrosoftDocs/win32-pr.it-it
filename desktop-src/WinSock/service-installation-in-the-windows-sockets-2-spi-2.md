---
description: Installazione del servizio in Windows Sockets 2 (Winsock) SPI.
ms.assetid: a303fbcf-9122-422a-9b12-d00a5df0fc0f
title: Installazione del servizio in Windows Sockets 2 SPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9028f35c21cc7055e8b8dde060c1c178dbf76715
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106310434"
---
# <a name="service-installation-in-the-windows-sockets-2-spi"></a>Installazione del servizio in Windows Sockets 2 SPI

-   [**NSPInstallServiceClass**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpnspinstallserviceclass)
-   [**NSPRemoveServiceClass**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpnspremoveserviceclass)
-   [**NSPSetService**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpnspsetservice)

Quando la classe di servizio necessaria non esiste già, un client SPI dello spazio dei nomi utilizza [**NSPInstallServiceClass**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpnspinstallserviceclass) per installare una nuova classe di servizio fornendo un nome di classe del servizio, un GUID per l'identificatore della classe del servizio e una serie di strutture [**WSANSCLASSINFO**](/windows/desktop/api/Winsock2/ns-winsock2-wsansclassinfow) . Queste strutture sono ognuna specifiche di un determinato spazio dei nomi e forniscono valori comuni, ad esempio i numeri di porta TCP consigliati o gli identificatori SAP NetWare. Una classe di servizio può essere rimossa chiamando [**NSPRemoveServiceClass**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpnspremoveserviceclass) e specificando il GUID corrispondente all'identificatore di classe.

Una volta che è presente una classe del servizio, è possibile installare o rimuovere istanze specifiche di un servizio tramite [**NSPSetService**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpnspsetservice). Questa funzione accetta una struttura [**WSAQUERYSET**](/windows/desktop/api/Winsock2/ns-winsock2-wsaquerysetw) come parametro di input insieme a un codice operativo e ai flag dell'operazione. Il codice dell'operazione indica se il servizio viene installato o rimosso. La struttura **WSAQUERYSET** fornisce tutte le informazioni rilevanti sul servizio, tra cui l'identificatore della classe del servizio, il nome del servizio (per questa istanza), l'identificatore dello spazio dei nomi e le informazioni sul protocollo applicabili e un set di indirizzi di trasporto su cui il servizio è in ascolto.

 

 



