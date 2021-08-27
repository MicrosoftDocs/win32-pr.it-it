---
description: "Il secondo passaggio del processo di progettazione di un'applicazione COM+ consiste nell'suddividere il modello concettuale nei livelli logici dell'architettura a tre livelli: il livello presentazione o i servizi utente. il livello intermedio o i servizi aziendali; e il livello dati o i servizi dati. Se non si ha familiarità con l'architettura a tre livelli, vedere Uso di un modello Three-Tier architettura."
ms.assetid: 6dc0a0ab-2cfa-4cc9-92a6-0d7554dd3397
title: "Modello logico: definizione e pianificazione dell'applicazione"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d19a493ebdacebac27edd291e747b5c42612f5fffd3ac7ea489f99b41de272b9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120120331"
---
# <a name="the-logical-model-application-definition-and-planning"></a>Modello logico: definizione e pianificazione dell'applicazione

Il secondo passaggio del processo di progettazione di un'applicazione COM+ consiste nell'suddividere il modello concettuale nei livelli logici dell'architettura a tre livelli: il livello presentazione o i servizi utente. il *livello intermedio* o i servizi aziendali; e il *livello dati* o i servizi dati. Se non si ha familiarità con l'architettura a tre livelli, vedere [Using a Three-Tier Architecture Model](using-a-three-tier-architecture-model.md).

Iniziare questo processo esaminando il modello concettuale per i sostantivi e i verbi. I sostantivi spesso possono essere tradotti in oggetti business (classi) e i verbi associati possono essere tradotti in azioni (metodi delle classi). Anche se può essere difficile definire tutti i sostantivi come oggetti business, le omissioni o gli errori diventeranno evidenti quando si completa il modello logico.

La maggior parte degli oggetti business finirà nel livello dei servizi business, con gli oggetti rimanenti divisi tra gli oggetti dell'interfaccia utente nel livello servizi utente e gli oggetti dati nel livello dei servizi dati. Quando si crea un modello logico usando l'architettura a tre livelli, tenere presente quanto segue:

-   Alcuni dei sostantivi nella progettazione concettuale non rappresenteranno i dati fisici effettivi, ma possono rappresentare un'azione nel sistema o il ruolo di un oggetto business nel sistema. Un oggetto business può anche essere un servizio che esegue un tipo di controllo di sistema, ad esempio un ID di accesso per la sicurezza.
-   Evitare di creare oggetti business erghiosi "leggendo tra le righe" nel [modello concettuale](the-conceptual-model--application-requirements.md). Tali oggetti business potrebbero non essere corretti ed è necessario valutarli attentamente prima di includerli nel modello logico. Se sembrano corretti, aggiungerli al modello concettuale in modo esplicito.
-   Evitare di creare oggetti business che esprimono le stesse informazioni o la stessa funzione; La duplicazione può essere diss costosa in termini di velocità e prestazioni dell'applicazione.
-   Determinare le dipendenze degli oggetti. Alcuni sostantivi nel modello concettuale possono essere semplicemente attributi di altri oggetti business. Decidere se l'attributo può esistere in modo indipendente. In tal caso, deve diventare il proprio oggetto business. In caso contrario, deve essere combinato con l'oggetto business appropriato.
-   Evitare di creare oggetti business che tentano di eseguire troppe attività. L'overload di oggetti business può significare più tempo impiegato per separare il codice in un secondo momento e può essere un problema di manutenzione. Gli oggetti distinti nel modello concettuale non devono essere combinati. devono rimanere oggetti business separati. È possibile gestire eventuali analogie usando il codice per delegare le funzioni comuni a un oggetto business.
-   Rimuovere tutti gli oggetti business che non vengono utilizzati in alcuno scenario di utilizzo. Se gli oggetti sono destinati a supportare la crescita futura, è consigliabile implementarli dopo il completamento dell'applicazione iniziale.

A questo punto, è possibile iniziare a pensare in termini di computer e codice. Da questi servizi aziendali determinare la funzionalità di visualizzazione e input che è necessario fornire come servizi utente. Definire quali tabelle e stored procedure devono essere fornite come servizi dati. Per completare il modello logico, definire le interfacce per ogni servizio e includere le definizioni di ogni campo dati e le relative regole di convalida. Includere anche tutte le funzioni, la relativa sintassi e i relativi parametri.

La definizione del servizio o dell'oggetto non deve includere alcun aspetto dell'implementazione fisica. Lo scopo è fornire una linea guida chiara per i generatori di componenti logici da cui lavorare e per consentire ad altri programmatori di codificare parti dell'applicazione che potrebbero usare il componente prima che venga effettivamente completato. Nella progettazione del modello logico è necessario documentare ogni schermata, funzione e oggetto. Non procedere al modello fisico o all'implementazione fino a quando non si soddisfano questi criteri. Se si procede mentre il modello concettuale e il modello logico non sono in accordo, si avranno gravi problemi più avanti nel ciclo di sviluppo.

Lo sviluppo incrementale di un'applicazione COM+ è comune. Ciò comporta la creazione di un subset dei componenti noti finali e il test tramite ogni livello dell'applicazione: livelli client, business e dati, fino all'archiviazione dei dati. Questo modello di lavoro fornisce informazioni dettagliate su requisiti aggiuntivi da parte del cliente e considerazioni sull'implementazione. Spesso questo modello funzionante viene testato in un singolo computer.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Modello concettuale: requisiti dell'applicazione](the-conceptual-model--application-requirements.md)
</dt> <dt>

[Modello fisico: Architettura dell'applicazione](the-physical-model--application-architecture.md)
</dt> <dt>

[Uso di un modello Three-Tier architettura](using-a-three-tier-architecture-model.md)
</dt> </dl>

 

 



