---
title: Informazioni di connessione e configurazione RAS
description: Le applicazioni in esecuzione Windows NT 4.0 e versioni successive e Windows 95 possono usare la funzione RasEnumConnections per ottenere informazioni sulle connessioni esistenti nel computer locale.
ms.assetid: b738ed87-1ff5-4366-9e83-08ac08ec261c
keywords:
- Configurazione e connessione, RAS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: af528af93318247b7f88a50dc1db240670d17bcc48e11a7d683bfccd9054d671
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119673431"
---
# <a name="ras-configuration-and-connection-information"></a>Informazioni di connessione e configurazione RAS

Le applicazioni in esecuzione Windows NT 4.0 e versioni successive e Windows 95 possono usare la funzione [**RasEnumConnections**](/windows/desktop/api/Ras/nf-ras-rasenumconnectionsa) per ottenere informazioni sulle connessioni esistenti nel computer locale. Le informazioni per ogni connessione includono un handle di connessione e il nome della voce della rubrica telefonica usata per stabilire la connessione. È possibile usare l'handle di connessione in una chiamata alla [**funzione RasGetConnectStatus**](/windows/desktop/api/Ras/nf-ras-rasgetconnectstatusa) per ottenere lo stato corrente della connessione.

Windows NT Server 4.0 e versioni successive forniscono due nuove funzioni per il recupero di informazioni RAS. Windows 95 non supportano queste funzioni.

La [**funzione RasEnumDevices**](/windows/desktop/api/Ras/nf-ras-rasenumdevicesa) restituisce il nome e il tipo dei dispositivi con funzionalità RAS configurati nel computer locale.

La [**funzione RasConnectionNotification**](/windows/desktop/api/Ras/nf-ras-rasconnectionnotificationa) specifica un oggetto evento che il sistema segnala quando viene creata o terminata una connessione RAS.

 

 




