---
title: Considerazioni sulla progettazione del server di stato
description: A seconda della progettazione, potrebbe essere necessario un server per tenere traccia degli utenti attualmente connessi alla rete.
ms.assetid: 2f8d268b-5518-4ad2-aed6-5971c913db6d
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7a0ef654f3641138075acc667d733b20c94c4840
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104396459"
---
# <a name="state-server-design-considerations"></a>Considerazioni sulla progettazione del server di stato

> [!Note]  
> Il servizio di autenticazione Internet (IAS) è stato rinominato server dei criteri di rete (NPS) a partire da Windows Server 2008. Il contenuto di questo argomento si applica sia a IAS che a NPS. In tutto il testo, NPS viene utilizzato per fare riferimento a tutte le versioni del servizio, incluse le versioni originariamente indicate come IAS.

 

A seconda della progettazione, potrebbe essere necessario un server per tenere traccia degli utenti attualmente connessi alla rete. Il problema principale del server di stato è mantenere le informazioni nel database del server di stato sincronizzate con chi è effettivamente connesso. Se le informazioni nel server di stato non sono sincronizzate, è possibile che gli utenti abbiano più sessioni se non sono autorizzate a farlo. Inoltre, è possibile che gli utenti che non dispongono di più sessioni vengano penalizzati inavvertitamente.

Quando si implementa il server di stato, è necessario prendere in considerazione quanto segue:

-   Il server di stato deve prendere la decisione online entro pochi secondi. Per questo motivo, il server di stato richiede un'infrastruttura scalabile in grado di supportare molti aggiornamenti e query al secondo. I database relazionali non sono appropriati per le query di grandi dimensioni con aggiornamenti simultanei. I database relazionali vengono creati principalmente per garantire la coerenza dei dati e fornire una visualizzazione coerente dei dati a tutti i consumer. Non sono compilati per aggiornamenti rapidi.
-   La coerenza transazionale sugli aggiornamenti tra più oggetti non è importante. Questo è dovuto al fatto che il server di stato può tollerare una piccola finestra di opportunità. Tuttavia, la coerenza transazionale di un singolo aggiornamento è importante per ridurre le possibilità di lasciare il server di stato in uno stato incoerente se uno dei server RADIUS viene arrestato durante l'aggiornamento.
-   La persistenza (il salvataggio dello stato della rete in un archivio permanente) non è importante perché le informazioni persistenti non risulteranno rapidamente sincronizzate con lo stato effettivo della rete.
-   Se nella rete sono supportati ISDN o altre forme di collegamento multiplo, il server di stato deve essere in grado di gestire scenari che usano queste funzionalità.

Una possibile progettazione consiste nell'implementare sia una DLL dell'estensione di autenticazione che una DLL di estensione di autorizzazione. Ognuna di queste dll può comunicare in rete con un database. La DLL dell'estensione di autorizzazione può aggiornare il database con informazioni sugli utenti attualmente connessi alla rete. La DLL dell'estensione di autenticazione può eseguire una query sul database per ottenere queste informazioni per decidere se accettare o rifiutare la richiesta di autenticazione di un utente specifico. Se l'utente è già connesso, la richiesta viene rifiutata.

Il vantaggio della DLL dell'estensione di autorizzazione che aggiorna il database del server di stato è che la DLL dell'estensione di autorizzazione ha accesso ad altre informazioni sull'utente autenticato. La DLL dell'estensione di autorizzazione ha accesso a tutti gli attributi di autorizzazione dal meccanismo di autorizzazione NPS. Ad esempio, alcuni utenti possono disporre di autorizzazioni che consentono loro di avere più sessioni. Il server di stato deve considerare tali utenti come un caso speciale.

 

 




