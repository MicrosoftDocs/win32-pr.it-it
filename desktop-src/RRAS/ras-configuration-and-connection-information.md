---
title: Informazioni sulla configurazione e sulla connessione RAS
description: Le applicazioni eseguite in Windows NT 4,0 e versioni successive e Windows 95 possono utilizzare la funzione RasEnumConnections per ottenere informazioni sulle connessioni esistenti nel computer locale.
ms.assetid: b738ed87-1ff5-4366-9e83-08ac08ec261c
keywords:
- Configurazione e connessione, RAS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 44c4e768f4686a24857a75212e40f2e64bc91109
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106298183"
---
# <a name="ras-configuration-and-connection-information"></a><span data-ttu-id="b310d-104">Informazioni sulla configurazione e sulla connessione RAS</span><span class="sxs-lookup"><span data-stu-id="b310d-104">RAS Configuration and Connection Information</span></span>

<span data-ttu-id="b310d-105">Le applicazioni eseguite in Windows NT 4,0 e versioni successive e Windows 95 possono utilizzare la funzione [**RasEnumConnections**](/windows/desktop/api/Ras/nf-ras-rasenumconnectionsa) per ottenere informazioni sulle connessioni esistenti nel computer locale.</span><span class="sxs-lookup"><span data-stu-id="b310d-105">Applications running on Windows NT 4.0 and later versions, and Windows 95, can use the [**RasEnumConnections**](/windows/desktop/api/Ras/nf-ras-rasenumconnectionsa) function to get information about the existing connections on the local computer.</span></span> <span data-ttu-id="b310d-106">Le informazioni per ogni connessione includono un handle di connessione e il nome della voce della rubrica telefonica utilizzata per stabilire la connessione.</span><span class="sxs-lookup"><span data-stu-id="b310d-106">The information for each connection includes a connection handle and the name of the phone-book entry used to establish the connection.</span></span> <span data-ttu-id="b310d-107">È possibile usare l'handle di connessione in una chiamata alla funzione [**RasGetConnectStatus**](/windows/desktop/api/Ras/nf-ras-rasgetconnectstatusa) per ottenere lo stato corrente della connessione.</span><span class="sxs-lookup"><span data-stu-id="b310d-107">You can use the connection handle in a call to the [**RasGetConnectStatus**](/windows/desktop/api/Ras/nf-ras-rasgetconnectstatusa) function get the current status of the connection.</span></span>

<span data-ttu-id="b310d-108">Windows NT Server 4,0 e versioni successive forniscono due nuove funzioni per il recupero delle informazioni RAS.</span><span class="sxs-lookup"><span data-stu-id="b310d-108">Windows NT Server 4.0 and later versions provide two new functions for retrieving RAS information.</span></span> <span data-ttu-id="b310d-109">Le funzioni di Windows 95does non sono supportate.</span><span class="sxs-lookup"><span data-stu-id="b310d-109">Windows 95does not support these functions.</span></span>

<span data-ttu-id="b310d-110">La funzione [**RasEnumDevices**](/windows/desktop/api/Ras/nf-ras-rasenumdevicesa) restituisce il nome e il tipo dei dispositivi compatibili con RAS configurati nel computer locale.</span><span class="sxs-lookup"><span data-stu-id="b310d-110">The [**RasEnumDevices**](/windows/desktop/api/Ras/nf-ras-rasenumdevicesa) function returns the name and type of the RAS-capable devices that are configured on the local computer.</span></span>

<span data-ttu-id="b310d-111">La funzione [**RasConnectionNotification**](/windows/desktop/api/Ras/nf-ras-rasconnectionnotificationa) specifica un oggetto evento segnalato dal sistema quando viene creata o terminata una connessione RAS.</span><span class="sxs-lookup"><span data-stu-id="b310d-111">The [**RasConnectionNotification**](/windows/desktop/api/Ras/nf-ras-rasconnectionnotificationa) function specifies an event object that the system signals when a RAS connection is created or terminated.</span></span>

 

 




