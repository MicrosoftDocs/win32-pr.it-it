---
description: Un programma di controllo del servizio avvia e controlla i servizi.
ms.assetid: e7ba295f-2937-44ad-89e8-40200c5e58b6
title: Programmi di controllo dei servizi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bb11e8224a23edcebd0688039502c5bc38da929d47cba470e6f397f4430e444f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118889044"
---
# <a name="service-control-programs"></a>Programmi di controllo dei servizi

Un programma di controllo del servizio avvia e controlla i servizi. Esegue le azioni seguenti:

-   Avvia un servizio o un servizio driver, se il tipo di avvio è SERVICE \_ DEMAND \_ START.
-   Invia richieste di controllo a un servizio in esecuzione.
-   Esegue una query sullo stato corrente di un servizio in esecuzione.

Queste azioni richiedono un handle aperto per l'oggetto servizio. Per ottenere l'handle, il programma di controllo del servizio deve:

1.  Usare la [**funzione OpenSCManager**](/windows/desktop/api/Winsvc/nf-winsvc-openscmanagera) per ottenere un handle per il database SCM in un computer specificato.
2.  Usare la [**funzione OpenService**](/windows/desktop/api/Winsvc/nf-winsvc-openservicea) [**o CreateService**](/windows/desktop/api/Winsvc/nf-winsvc-createservicea) per ottenere un handle per l'oggetto servizio.

Per altre informazioni, vedere i seguenti argomenti:

-   [Avvio del servizio](service-startup.md)
-   [Richieste di controllo del servizio](service-control-requests.md)
-   [Controllo di un servizio tramite SC](controlling-a-service-using-sc.md)

 

 



