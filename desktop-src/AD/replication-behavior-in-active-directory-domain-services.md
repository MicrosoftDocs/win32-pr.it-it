---
title: Comportamento della replica in Active Directory Domain Services
description: Il comportamento della replica è coerente e prevedibile. Dato un set di modifiche a una determinata replica, il risultato può essere previsto \ 8212; le modifiche verranno propagate a tutte le altre repliche.
ms.assetid: 4e9f2e43-6375-4663-93ca-55112fd00abe
ms.tgt_platform: multiple
keywords:
- Active Directory Domain Services Active Directory , Replica
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e7548ecf146f1d23b97b9db6a0307b21a6c39d359576c2de02285331d165fad4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119025139"
---
# <a name="replication-behavior-in-active-directory-domain-services"></a>Comportamento della replica in Active Directory Domain Services

Il comportamento della replica è coerente e prevedibile. Dato un set di modifiche a una determinata replica, è possibile stimare il risultato. Le modifiche verranno propagate a tutte le altre repliche. La progettazione di un modello generale affidabile per la stima del momento in cui le modifiche verranno applicate a tutte le altre repliche o a una replica specifica non è possibile, perché lo stato futuro del sistema distribuito nel suo complesso non è noto. Si tratta di una "latenza non deterministica" e le applicazioni che usano la directory devono comprenderla e consentirla.

La situazione potrebbe non essere così complessa. Un'applicazione deve contenere solo tre stati:

-   A inclinazione della versione: nessuna delle modifiche applicate a una determinata replica di origine è stata propagata a una determinata replica di destinazione. Un'applicazione che legge la replica di origine vede la nuova versione delle informazioni, mentre un'applicazione che legge la destinazione vede la versione precedente (o nulla, se le nuove informazioni sono state aggiunte per la prima volta). L'a inclinazione delle versioni si applica a tutti i consumer del servizio directory.
-   Aggiornamento parziale: alcune delle modifiche applicate a una determinata replica di origine sono state propagate a una determinata replica di destinazione. Un'applicazione che legge la replica di origine vede le nuove informazioni, mentre un'applicazione che legge la destinazione vede una combinazione di informazioni nuove e meno aggiornate (o solo alcune delle nuove informazioni, se le nuove informazioni sono state aggiunte per la prima volta). L'aggiornamento parziale si applica ai consumer del servizio directory che usano due o più oggetti correlati per archiviare le informazioni.
-   Stato completamente replicato: tutte le modifiche applicate a una determinata replica di origine sono state propagate a una determinata replica di destinazione. Le applicazioni nelle repliche di origine e di destinazione visualizzano le stesse informazioni.

 

 




