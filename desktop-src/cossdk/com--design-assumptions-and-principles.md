---
description: Il modello di programmazione distribuita Microsoft è costituito da diverse tecnologie, tra cui MSMQ, IIS, DCOM e COM+. Tutti questi servizi sono stati progettati per l'uso da parte di applicazioni distribuite.
ms.assetid: c72bbd47-0219-40ba-a7d5-2a6b725972d0
title: Presupposti e principi della progettazione COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 28b87c5ae631cd5517b215efae3a09968649cd49ea94fe33b33d9b826082e911
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118549396"
---
# <a name="com-design-assumptions-and-principles"></a>Presupposti e principi della progettazione COM+

Il modello di programmazione distribuita Microsoft è costituito da diverse tecnologie, tra cui MSMQ, IIS, DCOM e COM+. Tutti questi servizi sono stati progettati per l'uso da parte di applicazioni distribuite.

COM+ è stato sviluppato per semplificare la creazione di applicazioni distribuite. L'architettura generale si basa su un set di presupposti e principi.

## <a name="assumptions"></a>Presupposti

I presupposti sono i seguenti:

-   **L'applicazione COM+ supporterà più utenti su più server.** In altre parole, si sta creando un'applicazione distribuita e questi più utenti si trovaranno in computer host diversi da cui viene eseguito il codice. Gli utenti accederanno al codice tramite Internet o tramite una rete privata. L'interfaccia utente verrà presentata tramite browser o un'applicazione personalizzata, ad esempio un'applicazione basata su form scritta con Microsoft Visual Basic o MFC. Tale interfaccia utente verrà posizionata nel computer client.
-   **L'applicazione COM+ può essere resa scalabile e può offrire maggiore disponibilità e affidabilità distribuendo l'applicazione in più computer server.** In questo modo, è possibile bilanciare il carico di lavoro dell'applicazione e fornire tolleranza di errore usando Windows clustering.
-   **In caso di problemi, lo stato dei dati persistenti, archiviati in un database, da un'applicazione COM+ verrà mantenuto se si usano transazioni.** Lo stato dell'applicazione deve superare gli eventi imprevisti che possono verificarsi, ad esempio errori dell'applicazione, arresti anomali del sistema o errori di rete.

## <a name="principles"></a>Principi

Oltre a questi tre presupposti, i principi seguenti pervadono il modello di programmazione COM+:

-   **La logica dell'applicazione risiederà nei computer server, non nei computer client.** Esistono tre motivi principali per eseguire questa operazione:
    -   Il computer client potrebbe non disporre della potenza di elaborazione o delle funzionalità necessarie per eseguire la logica dell'applicazione. Inoltre, mantenere la logica dell'applicazione nel server semplifica la distribuzione.
    -   I computer server sono spesso più vicini ai dati e questi dati si trovano più spesso in un database. Poiché l'applicazione accede ai database, è necessario essere molto sensibili al costo delle connessioni di database. Inserendo la maggior parte della logica nei computer server, è possibile condividere le connessioni di database e ottenere un miglioramento significativo delle prestazioni. Nei computer server sono presenti anche altre risorse che possono essere condivise, anche in questo caso con un vantaggio in termini di prestazioni.
    -   La presenza della logica dell'applicazione nei computer server mantiene il controllo del contesto di sicurezza con l'applicazione. Si ha un maggiore controllo sulla sicurezza se si mantiene tale sicurezza nei componenti dell'applicazione in esecuzione nei computer server anziché nei computer client.
-   **Le transazioni sono il nucleo.** Per impostazione predefinita, le transazioni permeano il modello di programmazione COM+ che è molto importante comprenderle. Sebbene sia possibile usare molti dei servizi di COM+ senza usare le transazioni, se si sceglie di non usarli, non è possibile sfruttare appieno i servizi COM+ disponibili. Di seguito sono riportati alcuni vantaggi importanti dell'uso delle transazioni:
    -   Le transazioni sono una soluzione ragionevole per il problema della gestione della concorrenza. Inoltre, le transazioni consentono di proteggersi da arresti anomali e hanno un modello di recupero con errori di qualità. Inoltre, le transazioni sono un ottimo modo per gestire le attività in più sistemi.
    -   È possibile progettare un'applicazione COM+ basata su transazioni da usare con un gestore di risorse e un database, che consente di proteggere la maggior parte delle informazioni sullo stato. Mantenendo lo stato all'interno di un database o di un'altra risorsa di archiviazione gestita da un gestore di risorse, non è necessario mantenere molto stato all'interno degli oggetti effettivi creati dall'applicazione. Anche se si tratta di un'uscita da un modello orientato a oggetti puro, funziona bene per la creazione di applicazioni distribuite con il ripristino dagli errori.
-   **La funzionalità dell'applicazione viene compilata come oggetti COM, che esegue il wrapping dei protocolli usati per comunicare con altri sistemi o tecnologie.** Poiché probabilmente si stanno creando componenti che uniranno più tecnologie o sistemi legacy, pianificare l'uso di un'ampia gamma di protocolli di comunicazione. Usare HTTP per la comunicazione client/server o da applicazione ad applicazione tramite Internet. Usare DCOM per la comunicazione da applicazione ad applicazione o da componente a componente nel server.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Linee guida di base per la progettazione di applicazioni COM+](basic-guidelines-for-designing-com--applications.md)
</dt> <dt>

[Progettazione dell'applicazione COM+ tramite UML](designing-the-com--application-using-uml.md)
</dt> <dt>

[Progettazione generale Suggerimenti'uso di COM+](general-design-tips-for-using-com-.md)
</dt> <dt>

[Ottimizzazione delle interazioni con il livello di logica di business COM+](optimizing-interactions-with-the-com--business-logic-tier.md)
</dt> <dt>

[Altri strumenti Microsoft per la creazione di applicazioni distribuite](other-microsoft-tools-for-building-distributed-applications.md)
</dt> </dl>

 

 



