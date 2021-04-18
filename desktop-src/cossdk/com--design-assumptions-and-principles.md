---
description: Il modello di programmazione Microsoft distribuito è costituito da diverse tecnologie, tra cui MSMQ, IIS, DCOM e COM+. Tutti questi servizi sono stati progettati per l'uso da applicazioni distribuite.
ms.assetid: c72bbd47-0219-40ba-a7d5-2a6b725972d0
title: Presupposti e principi di progettazione COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d7dea86c404896a3d6095d39ebd6031767f6ccdd
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106305334"
---
# <a name="com-design-assumptions-and-principles"></a>Presupposti e principi di progettazione COM+

Il modello di programmazione Microsoft distribuito è costituito da diverse tecnologie, tra cui MSMQ, IIS, DCOM e COM+. Tutti questi servizi sono stati progettati per l'uso da applicazioni distribuite.

COM+ è stato sviluppato per semplificare la creazione di applicazioni distribuite. L'architettura complessiva si basa su un set di presupposti e principi.

## <a name="assumptions"></a>Presupposti

I presupposti sono i seguenti:

-   **L'applicazione COM+ supporterà più utenti tra più server.** In altre parole, si sta compilando un'applicazione distribuita e questi più utenti si trovano su computer host diversi da cui viene eseguito il codice. Gli utenti dovranno accedere al codice tramite Internet o tramite una rete privata. L'interfaccia utente verrà visualizzata tramite il browser o potrebbe essere un'applicazione personalizzata, ad esempio un'applicazione basata su form scritta con Microsoft Visual Basic o MFC. L'interfaccia utente verrà posizionata nel computer client.
-   **L'applicazione COM+ può essere resa scalabile e garantire maggiore disponibilità e affidabilità distribuendo l'applicazione tra più computer server.** In questo, è possibile bilanciare il carico di lavoro dell'applicazione e fornire tolleranza di errore usando il servizio cluster di Windows.
-   **In caso di problemi, lo stato dei dati salvati in permanenza, archiviati in un database, da un'applicazione COM+ verrà mantenuto se si utilizzano le transazioni.** Lo stato dell'applicazione deve superare gli incidenti che possono verificarsi, ad esempio errori dell'applicazione, arresti anomali del sistema o errori di rete.

## <a name="principles"></a>Principi

Oltre a questi tre presupposti, il modello di programmazione COM+ pervade i principi seguenti:

-   **La logica dell'applicazione si troverà nei computer server, non nei computer client.** Esistono tre motivi principali per eseguire questa operazione:
    -   È possibile che il computer client non disponga della potenza di elaborazione o delle funzionalità necessarie per eseguire la logica dell'applicazione. Inoltre, il mantenimento della logica dell'applicazione nel server semplifica la distribuzione.
    -   I computer server sono spesso più vicini ai dati e questi dati si trovano più spesso in un database. Poiché l'applicazione accede ai database, si desidera essere molto sensibili al costo delle connessioni al database. Inserendo la maggior parte della logica nei computer server, è possibile condividere le connessioni al database e ottenere un miglioramento significativo delle prestazioni. Sono disponibili anche altre risorse sui computer server che possono essere condivise, con un miglioramento delle prestazioni.
    -   La presenza della logica dell'applicazione nei computer server mantiene il controllo del contesto di sicurezza con l'applicazione. Si ha maggiore controllo sulla sicurezza se si mantiene tale protezione sui componenti dell'applicazione in esecuzione nei computer server anziché nei computer client.
-   **Le transazioni sono le principali.** Per impostazione predefinita, le transazioni permeano il modello di programmazione COM+ che è molto importante per la comprensione. Sebbene sia possibile utilizzare molti dei servizi di COM+ senza utilizzare le transazioni, se si sceglie di non utilizzarli, non è possibile sfruttare appieno i servizi COM+ disponibili. Di seguito sono riportati alcuni importanti vantaggi dell'utilizzo delle transazioni:
    -   Le transazioni sono una soluzione ragionevole per il problema della gestione della concorrenza. Inoltre, le transazioni consentono di proteggersi dagli arresti anomali e hanno un modello di recupero con errori corretto. Inoltre, le transazioni diventano un ottimo modo per gestire le attività tra più sistemi.
    -   È possibile progettare un'applicazione COM+ basata sulle transazioni per usare un gestore di risorse e un database, che consente di proteggere la maggior parte delle informazioni sullo stato. Mantenendo lo stato all'interno di un database o di un'altra archiviazione gestita da un gestore di risorse, non è necessario mantenere molti stati all'interno degli oggetti effettivi creati dall'applicazione. Anche se si tratta di una partenza da un modello orientato agli oggetti puri, funziona bene per la creazione di applicazioni distribuite con il ripristino degli errori.
-   **Le funzionalità dell'applicazione sono compilate come oggetti COM, eseguendo il wrapping dei protocolli utilizzati per comunicare con altri sistemi o tecnologie.** Poiché è probabile che si stiano creando componenti che riuniscono diverse tecnologie o sistemi legacy, pianificare l'utilizzo di un'ampia gamma di protocolli di comunicazione. Utilizzare HTTP per la comunicazione client/server o la comunicazione da applicazione ad applicazione tramite Internet. Usare DCOM per la comunicazione da applicazione ad applicazione o da componente a componente nel server.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Linee guida di base per la progettazione di applicazioni COM+](basic-guidelines-for-designing-com--applications.md)
</dt> <dt>

[Progettazione dell'applicazione COM+ tramite UML](designing-the-com--application-using-uml.md)
</dt> <dt>

[Suggerimenti di progettazione generali per l'utilizzo di COM+](general-design-tips-for-using-com-.md)
</dt> <dt>

[Ottimizzazione delle interazioni con il livello di logica di business COM+](optimizing-interactions-with-the-com--business-logic-tier.md)
</dt> <dt>

[Altri strumenti Microsoft per la creazione di applicazioni distribuite](other-microsoft-tools-for-building-distributed-applications.md)
</dt> </dl>

 

 



