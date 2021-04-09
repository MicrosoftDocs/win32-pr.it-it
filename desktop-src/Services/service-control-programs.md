---
description: Un programma di controllo del servizio avvia e controlla i servizi.
ms.assetid: e7ba295f-2937-44ad-89e8-40200c5e58b6
title: Programmi di controllo del servizio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 78b34232f5f87d84bdf30acd51f57afbf79a8385
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103879026"
---
# <a name="service-control-programs"></a>Programmi di controllo del servizio

Un programma di controllo del servizio avvia e controlla i servizi. Esegue le azioni seguenti:

-   Avvia un servizio o un servizio driver, se il tipo di avvio è servizio di \_ \_ avvio richiesta.
-   Invia le richieste di controllo a un servizio in esecuzione.
-   Esegue una query sullo stato corrente di un servizio in esecuzione.

Queste azioni richiedono un handle aperto per l'oggetto servizio. Per ottenere l'handle, il programma di controllo del servizio deve:

1.  Utilizzare la funzione [**OpenSCManager**](/windows/desktop/api/Winsvc/nf-winsvc-openscmanagera) per ottenere un handle per il database SCM in un computer specificato.
2.  Utilizzare la funzione [**OpenService**](/windows/desktop/api/Winsvc/nf-winsvc-openservicea) o [**CreateService**](/windows/desktop/api/Winsvc/nf-winsvc-createservicea) per ottenere un handle per l'oggetto servizio.

Per altre informazioni, vedere i seguenti argomenti:

-   [Avvio del servizio](service-startup.md)
-   [Richieste di controllo del servizio](service-control-requests.md)
-   [Controllo di un servizio con SC](controlling-a-service-using-sc.md)

 

 



