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
# <a name="service-installation-in-the-windows-sockets-2-spi"></a><span data-ttu-id="a6ed7-103">Installazione del servizio in Windows Sockets 2 SPI</span><span class="sxs-lookup"><span data-stu-id="a6ed7-103">Service Installation in the Windows Sockets 2 SPI</span></span>

-   [<span data-ttu-id="a6ed7-104">**NSPInstallServiceClass**</span><span class="sxs-lookup"><span data-stu-id="a6ed7-104">**NSPInstallServiceClass**</span></span>](/windows/desktop/api/Ws2spi/nc-ws2spi-lpnspinstallserviceclass)
-   [<span data-ttu-id="a6ed7-105">**NSPRemoveServiceClass**</span><span class="sxs-lookup"><span data-stu-id="a6ed7-105">**NSPRemoveServiceClass**</span></span>](/windows/desktop/api/Ws2spi/nc-ws2spi-lpnspremoveserviceclass)
-   [<span data-ttu-id="a6ed7-106">**NSPSetService**</span><span class="sxs-lookup"><span data-stu-id="a6ed7-106">**NSPSetService**</span></span>](/windows/desktop/api/Ws2spi/nc-ws2spi-lpnspsetservice)

<span data-ttu-id="a6ed7-107">Quando la classe di servizio necessaria non esiste già, un client SPI dello spazio dei nomi utilizza [**NSPInstallServiceClass**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpnspinstallserviceclass) per installare una nuova classe di servizio fornendo un nome di classe del servizio, un GUID per l'identificatore della classe del servizio e una serie di strutture [**WSANSCLASSINFO**](/windows/desktop/api/Winsock2/ns-winsock2-wsansclassinfow) .</span><span class="sxs-lookup"><span data-stu-id="a6ed7-107">When the required service class does not already exist, a namespace SPI client uses [**NSPInstallServiceClass**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpnspinstallserviceclass) to install a new service class by supplying a service class name, a GUID for the service class identifier, and a series of [**WSANSCLASSINFO**](/windows/desktop/api/Winsock2/ns-winsock2-wsansclassinfow) structures.</span></span> <span data-ttu-id="a6ed7-108">Queste strutture sono ognuna specifiche di un determinato spazio dei nomi e forniscono valori comuni, ad esempio i numeri di porta TCP consigliati o gli identificatori SAP NetWare.</span><span class="sxs-lookup"><span data-stu-id="a6ed7-108">These structures are each specific to a particular namespace, and supply common values such as recommended TCP port numbers or NetWare SAP Identifiers.</span></span> <span data-ttu-id="a6ed7-109">Una classe di servizio può essere rimossa chiamando [**NSPRemoveServiceClass**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpnspremoveserviceclass) e specificando il GUID corrispondente all'identificatore di classe.</span><span class="sxs-lookup"><span data-stu-id="a6ed7-109">A service class can be removed by calling [**NSPRemoveServiceClass**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpnspremoveserviceclass) and supplying the GUID corresponding to the class identifier.</span></span>

<span data-ttu-id="a6ed7-110">Una volta che è presente una classe del servizio, è possibile installare o rimuovere istanze specifiche di un servizio tramite [**NSPSetService**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpnspsetservice).</span><span class="sxs-lookup"><span data-stu-id="a6ed7-110">Once a service class exists, specific instances of a service can be installed or removed via [**NSPSetService**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpnspsetservice).</span></span> <span data-ttu-id="a6ed7-111">Questa funzione accetta una struttura [**WSAQUERYSET**](/windows/desktop/api/Winsock2/ns-winsock2-wsaquerysetw) come parametro di input insieme a un codice operativo e ai flag dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="a6ed7-111">This function takes a [**WSAQUERYSET**](/windows/desktop/api/Winsock2/ns-winsock2-wsaquerysetw) structure as an input parameter along with an operation code and operation flags.</span></span> <span data-ttu-id="a6ed7-112">Il codice dell'operazione indica se il servizio viene installato o rimosso.</span><span class="sxs-lookup"><span data-stu-id="a6ed7-112">The operation code indicates whether the service is being installed or removed.</span></span> <span data-ttu-id="a6ed7-113">La struttura **WSAQUERYSET** fornisce tutte le informazioni rilevanti sul servizio, tra cui l'identificatore della classe del servizio, il nome del servizio (per questa istanza), l'identificatore dello spazio dei nomi e le informazioni sul protocollo applicabili e un set di indirizzi di trasporto su cui il servizio è in ascolto.</span><span class="sxs-lookup"><span data-stu-id="a6ed7-113">The **WSAQUERYSET** structure provides all of the relevant information about the service including service class identifier, service name (for this instance), applicable namespace identifier and protocol information, and a set of transport addresses to which the service listens.</span></span>

 

 



