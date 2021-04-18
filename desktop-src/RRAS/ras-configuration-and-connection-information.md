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
# <a name="ras-configuration-and-connection-information"></a>Informazioni sulla configurazione e sulla connessione RAS

Le applicazioni eseguite in Windows NT 4,0 e versioni successive e Windows 95 possono utilizzare la funzione [**RasEnumConnections**](/windows/desktop/api/Ras/nf-ras-rasenumconnectionsa) per ottenere informazioni sulle connessioni esistenti nel computer locale. Le informazioni per ogni connessione includono un handle di connessione e il nome della voce della rubrica telefonica utilizzata per stabilire la connessione. È possibile usare l'handle di connessione in una chiamata alla funzione [**RasGetConnectStatus**](/windows/desktop/api/Ras/nf-ras-rasgetconnectstatusa) per ottenere lo stato corrente della connessione.

Windows NT Server 4,0 e versioni successive forniscono due nuove funzioni per il recupero delle informazioni RAS. Le funzioni di Windows 95does non sono supportate.

La funzione [**RasEnumDevices**](/windows/desktop/api/Ras/nf-ras-rasenumdevicesa) restituisce il nome e il tipo dei dispositivi compatibili con RAS configurati nel computer locale.

La funzione [**RasConnectionNotification**](/windows/desktop/api/Ras/nf-ras-rasconnectionnotificationa) specifica un oggetto evento segnalato dal sistema quando viene creata o terminata una connessione RAS.

 

 




