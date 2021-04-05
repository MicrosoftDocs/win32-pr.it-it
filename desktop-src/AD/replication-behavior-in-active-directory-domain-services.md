---
title: Comportamento della replica in Active Directory Domain Services
description: Il comportamento della replica è coerente e prevedibile. dato un set di modifiche a una determinata replica, il risultato può essere stimato \ 8212; le modifiche verranno propagate a tutte le altre repliche.
ms.assetid: 4e9f2e43-6375-4663-93ca-55112fd00abe
ms.tgt_platform: multiple
keywords:
- Active Directory Domain Services Active Directory, replica
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 41009a733f99366e499a25baca989f4f28794aea
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103855386"
---
# <a name="replication-behavior-in-active-directory-domain-services"></a>Comportamento della replica in Active Directory Domain Services

Il comportamento della replica è coerente e prevedibile. dato un set di modifiche a una determinata replica, il risultato può essere stimato: le modifiche verranno propagate a tutte le altre repliche. La definizione di un modello generale affidabile per la stima del momento in cui le modifiche verranno applicate a tutte le altre repliche o a una particolare replica non è possibile, perché lo stato futuro del sistema distribuito nel suo complesso non è noto. Questa operazione viene definita "latenza non deterministica" e le applicazioni che usano la directory devono comprenderle e consentirne l'utilizzo.

La situazione non è così complessa in quanto potrebbe essere visualizzata. È necessario che un'applicazione soddisfi solo tre stati:

-   Sfasamento della versione: nessuna delle modifiche applicate a una determinata replica di origine è stata propagata a una replica di destinazione specificata. Un'applicazione che legge la replica di origine Visualizza la nuova versione delle informazioni, mentre un'applicazione che legge la destinazione Visualizza la versione precedente (o nulla se le nuove informazioni sono state aggiunte per la prima volta). Lo sfasamento della versione si applica a tutti i consumer del servizio directory.
-   Aggiornamento parziale: alcune delle modifiche applicate a una determinata replica di origine sono state propagate a una determinata replica di destinazione. Un'applicazione che legge la replica di origine Visualizza le nuove informazioni, mentre un'applicazione che legge la destinazione vede una combinazione di informazioni obsolete e nuove (o solo alcune delle nuove informazioni, se le nuove informazioni sono state aggiunte per la prima volta). L'aggiornamento parziale si applica ai consumer del servizio directory che usano due o più oggetti correlati per archiviare le informazioni.
-   Stato completamente replicato: tutte le modifiche applicate a una determinata replica di origine sono state propagate a una determinata replica di destinazione. Le applicazioni presenti nelle repliche di origine e di destinazione visualizzano le stesse informazioni.

 

 




