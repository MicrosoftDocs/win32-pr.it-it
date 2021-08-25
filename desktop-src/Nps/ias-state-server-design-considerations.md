---
title: Considerazioni sulla progettazione del server di stato
description: A seconda della progettazione, potrebbe essere necessario un server per tenere traccia degli utenti attualmente connessi alla rete.
ms.assetid: 2f8d268b-5518-4ad2-aed6-5971c913db6d
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b39fa2460fbad5ffedd4a517da588cc0c951f734926c1219d750e28f71734c24
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119889481"
---
# <a name="state-server-design-considerations"></a>Considerazioni sulla progettazione del server di stato

> [!Note]  
> Il servizio di autenticazione Internet (IAS) è stato rinominato Server dei criteri di rete (NPS) a partire Windows Server 2008. Il contenuto di questo argomento si applica sia a IAS che a Server dei criteri di rete. In tutto il testo, Server dei criteri di rete viene usato per fare riferimento a tutte le versioni del servizio, incluse le versioni originariamente indicate come IAS.

 

A seconda della progettazione, potrebbe essere necessario un server per tenere traccia degli utenti attualmente connessi alla rete. La sfida principale con il server di stato è mantenere sincronizzate le informazioni nel database del server di stato con chi è effettivamente connesso. Se le informazioni nel server di stato non sono sincronizzate, gli utenti potrebbero riuscire ad avere più sessioni quando non sono autorizzati a eseguire questa operazione. Inoltre, gli utenti che non hanno più sessioni potrebbero essere inavvertitamente penalizzati.

Nell'implementazione del server di stato è necessario tenere in considerazione quanto segue:

-   Il server di stato deve prendere la decisione online in pochi secondi. Per questo motivo il server di stato richiede un'infrastruttura scalabile in grado di supportare molti aggiornamenti e query al secondo. I database relazionali non sono appropriati per query di grandi dimensioni con aggiornamenti simultanei. I database relazionali vengono creati principalmente per mantenere la coerenza dei dati e fornire una visualizzazione coerente dei dati a tutti i consumer. Non vengono compilati per gli aggiornamenti rapidi.
-   La coerenza transazionale sugli aggiornamenti tra più oggetti non è importante. Ciò è dovuto al fatto che il server di stato può tollerare una piccola finestra di opportunità. Tuttavia, la coerenza transazionale di un singolo aggiornamento è importante per ridurre le probabilità di lasciare il server di stato in uno stato incoerente se uno dei server RADIUS viene arrestato durante l'aggiornamento.
-   La persistenza (salvataggio dello stato della rete nell'archiviazione permanente) non è importante perché le informazioni persistenti non saranno rapidamente sincronizzate con lo stato effettivo della rete.
-   Se nella rete sono supportati ISDN o altre forme di multilink, il server di stato deve essere in grado di gestire scenari che usano queste funzionalità.

Una possibile progettazione è implementare sia una DLL dell'estensione di autenticazione che una DLL dell'estensione di autorizzazione. Ognuna di queste DLL può comunicare in rete con un database. La DLL dell'estensione di autorizzazione può aggiornare il database con le informazioni sugli utenti attualmente connessi alla rete. La DLL dell'estensione di autenticazione può eseguire una query sul database per ottenere queste informazioni per decidere se accettare o rifiutare la richiesta di autenticazione di un determinato utente. Se l'utente è già connesso, la richiesta viene rifiutata.

Il vantaggio di fare in modo che la DLL dell'estensione di autorizzazione aggiorni il database del server di stato è che la DLL dell'estensione di autorizzazione ha accesso ad altre informazioni sull'utente autenticato. La DLL dell'estensione di autorizzazione ha accesso a tutti gli attributi di autorizzazione dal meccanismo di autorizzazione di Server dei criteri di rete. Ad esempio, alcuni utenti potrebbero avere autorizzazioni che consentono loro di avere più sessioni. Il server di stato deve considerare tali utenti come un caso speciale.

 

 




