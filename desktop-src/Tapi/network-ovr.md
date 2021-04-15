---
description: Una rete viene visualizzata come meccanismo di trasporto che trasmette i dati da un punto a un altro.
ms.assetid: 88374ac9-81c3-48c3-bf1a-5cfd734c257c
title: Rete
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 70d25f0c643ed1b54edb0ec45d47abfdc2f29fd5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104485316"
---
# <a name="network"></a>Rete

Una rete viene visualizzata come meccanismo di trasporto che trasmette i dati da un punto a un altro. I provider di servizi TAPI gestiscono i protocolli specifici necessari per eseguire operazioni quali la creazione di una sessione di comunicazione in una determinata rete. Un'applicazione server o un utente finale richiede in genere solo informazioni di rete molto generali, ad esempio il tipo di indirizzo.

Alcuni tipi comuni di reti:

-   **Pot (servizio telefonico Plain Old):** La voce e i dati vengono trasmessi in formato analogico durante il *ciclo locale* e vengono trasmessi digitalmente altrove. In genere, un tipo di supporto per chiamata, un canale per riga.
-   **ISDN (Integrated Services Digital Network):** Trasmesse digitalmente. Velocità fino a 128 kbps nelle righe Basic Rate Interface (BRI-ISDN) e molto più elevate sulle linee PRI-ISDN (Primary Rate Interface). Almeno tre canali e un massimo di 32 canali, per la trasmissione simultanea e gestita in modo indipendente di voce e dati. Standard internazionale.
-   **T1/E1:** Trasmesse digitalmente. T1 è un collegamento di trasmissione con una capacità di 1,544 Mbps, in genere usato per connettere le reti tra le distanze remote. Nell'Unione europea T1 viene chiamato E1.
-   **Switched 56:** Segnalazione a 56 Kbps tramite linee telefoniche remote, ma richiede apparecchiature speciali. Limitato alle chiamate ad altre strutture appositamente fornite.
-   **Centrex:** Servizi di rete centralizzati tramite linee telefoniche normali e l'uso di apparecchiature aziendali telefoniche. Non è necessaria alcuna attrezzatura speciale.
-   **PBX digitali (scambi di rami privati) e sistemi principali:** Voce e dati trasmessi su sistemi telefonici privati mediante interfacce proprietarie.
-   **Reti IP:** Voce e dati trasmessi nelle reti tramite il protocollo IP (Internet Protocol), ad esempio Internet stesso o una rete Intranet aziendale.

Tenere presente che non si tratta di un elenco completo. È possibile supportare qualsiasi meccanismo di trasporto di rete, dato che i provider di servizi appropriati.

 

 



