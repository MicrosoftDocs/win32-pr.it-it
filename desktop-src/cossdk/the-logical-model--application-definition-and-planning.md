---
description: "Il secondo passaggio del processo di progettazione di un'applicazione COM+ consiste nell'suddividere il modello concettuale nei livelli logici dell'architettura a tre livelli: il livello di presentazione o i servizi utente. livello intermedio o servizi aziendali; e il livello dati o i servizi dati. Se non si ha familiarità con l'architettura a tre livelli, vedere uso di un modello di architettura Three-Tier."
ms.assetid: 6dc0a0ab-2cfa-4cc9-92a6-0d7554dd3397
title: "Modello logico: definizione dell'applicazione e pianificazione"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: acb09b0d377fcd9bf5e2319868f4006b5dbfce75
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104127543"
---
# <a name="the-logical-model-application-definition-and-planning"></a>Modello logico: definizione dell'applicazione e pianificazione

Il secondo passaggio del processo di progettazione di un'applicazione COM+ consiste nell'suddividere il modello concettuale nei livelli logici dell'architettura a tre livelli: il *livello di presentazione* o i servizi utente. *livello intermedio* o servizi aziendali; e il *livello dati* o i servizi dati. Se non si ha familiarità con l'architettura a tre livelli, vedere [uso di un modello di architettura Three-Tier](using-a-three-tier-architecture-model.md).

Iniziare questo processo esaminando il modello concettuale per i sostantivi e i verbi. I sostantivi possono spesso tradursi in oggetti business (classi) e i verbi associati possono tradursi in azioni (metodi delle classi). Sebbene possa essere difficile definire tutti i sostantivi come oggetti business, le omissioni o gli errori diventeranno evidenti nel momento in cui si completa il modello logico.

La maggior parte degli oggetti business finirà nel livello dei servizi aziendali, con gli oggetti rimanenti divisi tra gli oggetti dell'interfaccia utente nel livello dei servizi utente e gli oggetti dati nel livello dei servizi dati. Quando si crea un modello logico utilizzando l'architettura a tre livelli, tenere presente quanto segue:

-   Alcuni sostantivi nella progettazione concettuale non rappresenteranno i dati fisici effettivi, ma potrebbero rappresentare un'azione sul sistema o sul ruolo di un oggetto business nel sistema. Un oggetto business può essere anche un servizio che esegue un tipo di controllo del sistema, ad esempio un ID di accesso per la sicurezza.
-   Evitare di creare oggetti business vaghi mediante "lettura tra le righe" nel [modello concettuale](the-conceptual-model--application-requirements.md). Tali oggetti business potrebbero non essere corretti ed è consigliabile considerarli attentamente prima di includerli nel modello logico. Se appaiono corretti, aggiungerli al modello concettuale in modo esplicito.
-   Evitare di creare oggetti business che esprimono le stesse informazioni o funzioni; la duplicazione può essere costosa in termini di velocità e prestazioni dell'applicazione.
-   Determinare le dipendenze degli oggetti. Alcuni sostantivi nel modello concettuale possono essere semplicemente attributi di altri oggetti business. Decidere se l'attributo può esistere in modo indipendente. In caso affermativo, dovrebbe diventare il proprio oggetto business; in caso contrario, è necessario combinarlo con l'oggetto business appropriato.
-   Evitare di creare oggetti business che tentano di eseguire troppe operazioni. L'overload di oggetti business può comportare più tempo per separare il codice in un secondo momento e può essere un mal di manutenzione. Gli oggetti distinti nel modello concettuale non devono essere combinati. devono rimanere oggetti business distinti. È possibile gestire qualsiasi somiglianza usando il codice per delegare le funzioni comuni a un oggetto business.
-   Rimuovere gli oggetti business che non vengono usati in scenari di utilizzo. Se gli oggetti sono destinati a supportare la crescita futura, è consigliabile implementarli al termine dell'applicazione iniziale.

A questo punto, è possibile iniziare a pensare in termini di computer e codice. Da questi servizi aziendali, determinare le funzionalità di visualizzazione e di input che è necessario fornire come servizi utente. Definire quali tabelle e stored procedure devono essere fornite come servizi dati. Per completare il modello logico, definire le interfacce per ogni servizio e includere le definizioni di ogni campo dati e le relative regole di convalida. Includere anche tutte le funzioni, la relativa sintassi e i relativi parametri.

La definizione di un servizio o di un oggetto non deve includere alcun aspetto dell'implementazione fisica. Lo scopo è quello di fornire una linea guida chiara per i generatori di componenti logici da e per consentire ad altri programmatori di scrivere codice dell'applicazione che può utilizzare il componente prima del completamento. Nella progettazione del modello logico è necessario documentare ogni schermata, funzione e oggetto. Non procedere all'implementazione o al modello fisico fino a quando non si soddisfano questi criteri. Se si procede con il modello concettuale e il modello logico non concordati, si verificano gravi problemi in un secondo momento nel ciclo di sviluppo.

Lo sviluppo incrementale di un'applicazione COM+ è comune. Ciò comporta la creazione di un subset di componenti noti finali e la relativa verifica tramite ogni livello dell'applicazione, ovvero i livelli client, business e dati, fino all'archiviazione dei dati. Questo modello di lavoro fornisce informazioni sui requisiti aggiuntivi in base alle considerazioni relative al cliente e all'implementazione. Spesso questo modello funzionante viene testato in un singolo computer.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Modello concettuale: requisiti delle applicazioni](the-conceptual-model--application-requirements.md)
</dt> <dt>

[Modello fisico: architettura dell'applicazione](the-physical-model--application-architecture.md)
</dt> <dt>

[Uso di un modello di architettura Three-Tier](using-a-three-tier-architecture-model.md)
</dt> </dl>

 

 



