---
title: Progettazione di estensioni di classe helper NDF
description: Questo argomento è destinato a fornire linee guida generiche tramite il processo di sviluppo dell'estensione della classe helper.
ms.assetid: f5dbd198-7d22-4e7e-830e-6753e9f4d6c8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d91ff748d8139aad17fca3710b17e73b5e1eaa14
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103955347"
---
# <a name="designing-ndf-helper-class-extensions"></a>Progettazione di estensioni di classe helper NDF

Questo argomento è destinato a fornire linee guida generiche tramite il processo di sviluppo dell'estensione della classe helper. Le indicazioni fornite in questo argomento si applicano a tutte le estensioni della classe helper. Per informazioni aggiuntive più specifiche, vedere la [classe di supporto di Windows Filtering Platform estensibile](windows-filtering-platform-extensible-helper-class.md) e [le classi di helper estendibili di diagnostica wireless 802,11](802-11-wireless-diagnostics-extensible-helper-classes.md).

## <a name="extending-ndf-functionality"></a>Estensione della funzionalità NDF

Windows Vista e versioni successive vengono forniti con un'ampia gamma di classi helper già implementate che consentono di diagnosticare e correggere un'ampia gamma di problemi. In alcuni casi, tuttavia, gli sviluppatori di terze parti potrebbero desiderare di estendere queste classi helper per diagnosticare e risolvere i problemi specifici dei propri prodotti e implementazioni.

Le seguenti classi helper Microsoft NDF sono estendibili.

-   [Piattaforma filtro Windows](windows-filtering-platform-extensible-helper-class.md)
-   [Sicurezza wireless](802-11-wireless-diagnostics-extensible-helper-classes.md)

## <a name="implementing-a-helper-class-extension"></a>Implementazione di un'estensione di classe helper

Microsoft fornisce due interfacce che possono essere usate per sviluppare estensioni di classe helper NDF.

L'interfaccia [**INetDiagHelperInfo**](/windows/desktop/api/ndhelper/nn-ndhelper-inetdiaghelperinfo) viene chiamata da NDF per verificare che disponga di tutte le informazioni necessarie e che abbia scelto la classe helper corretta. Questa operazione viene eseguita tramite il metodo [**GetAttributeInfo**](/windows/desktop/api/ndhelper/nf-ndhelper-inetdiaghelperinfo-getattributeinfo) .

L'interfaccia [**INetDiagHelper**](/windows/desktop/api/ndhelper/nn-ndhelper-inetdiaghelper) viene chiamata da NDF per la maggior parte delle attività che si verificano durante la procedura di diagnostica. Molti dei metodi sono obbligatori, mentre altri sono facoltativi per usi specifici.

I metodi obbligatori includono [**Initialize**](/windows/desktop/api/ndhelper/nf-ndhelper-inetdiaghelper-initialize) e [**GetDiagnosticsInfo**](/windows/desktop/api/ndhelper/nf-ndhelper-inetdiaghelper-getdiagnosticsinfo). Le chiamate a NDF vengono **inizializzate** per inviare parametri chiave all'estensione della classe helper per inizializzarne lo stato dell'istanza. **GetDiagnosticsInfo** fornisce una stima del tempo necessario per la diagnosi e indica se è necessaria la rappresentazione del contesto utente originale.

Viene chiamato un altro metodo, [**LowHealth**](/windows/desktop/api/ndhelper/nf-ndhelper-inetdiaghelper-lowhealth), per eseguire la diagnosi sul componente di rete corrispondente alla classe helper. Il metodo [**Cancel**](/windows/desktop/api/ndhelper/nf-ndhelper-inetdiaghelper-cancel) viene chiamato quando NDF determina una diagnosi o un ripristino continuo da arrestare. La [**pulizia**](/windows/desktop/api/ndhelper/nf-ndhelper-inetdiaghelper-cleanup) consente a NDF di rilasciare le risorse NDF utilizzate dall'estensione della classe helper dal momento in cui è stata effettuata la chiamata a [**Initialize**](/windows/desktop/api/ndhelper/nf-ndhelper-inetdiaghelper-initialize) .

Per informazioni su altri metodi, vedere [**INetDiagHelper**](/windows/desktop/api/ndhelper/nn-ndhelper-inetdiaghelper).

Le estensioni della classe helper NDF vengono usate per diagnosticare e risolvere i problemi di connettività associati a un'applicazione o a un componente specifico. Consentono anche di convalidare l'esito positivo o negativo di un tentativo di risoluzione.

Gli sviluppatori che considerano l'implementazione di un'estensione di classe helper devono eseguire le attività seguenti.

-   Identificare gli scenari utente in cui sono utili le azioni di diagnostica e ripristino.
-   Fornire risoluzioni ai problemi di connettività riscontrati di frequente.
-   Se è necessaria un'estensione della classe helper, definire un modello di integrità dei componenti usato per rappresentare lo stato di integrità del componente in NDF.

## <a name="identify-user-scenarios"></a>Identificare gli scenari utente

Il test e l'utilizzo di un'applicazione potrebbero avere già fornito modelli individuabili che un'estensione della classe helper potrebbe essere in grado di diagnosticare e possibilmente ripristinare. Gli sviluppatori di applicazioni possono utilizzare questi dati per determinare i problemi di connettività più importanti da affrontare e per identificare gli scenari utente in cui si verificano probabilmente problemi di connettività.

La determinazione della causa principale di ogni problema è fondamentale in questa parte del processo. Questa operazione può richiedere una ricerca completa, ma consente di creare software molto più facile da usare per gli utenti e gli amministratori. Se la causa principale non è identificata, diventa difficile o impossibile offrire la risoluzione del problema usando l'estensione della classe helper.

## <a name="provide-resolutions"></a>Fornire le risoluzioni

Dopo che un team di sviluppo ha identificato le cause principali dei problemi associati al software, il passaggio successivo consiste nell'identificare le azioni di risoluzione appropriate per consentire all'utente di risolvere il problema nel modo più efficiente possibile.

Non tutte le risoluzioni richiedono che venga creata un'estensione della classe helper o un'azione automatizzata. In alcuni casi, il team può determinare che l'approccio migliore per la risoluzione di una causa principale consiste nel correggere o aggiornare il componente, fornire contenuto della Guida aggiuntivo per il componente o sviluppare altre strategie che forniscano soluzioni a lungo termine migliori.

Per i problemi in cui un'azione automatizzata è ideale, la creazione di un'estensione di classe helper NDF è spesso un'ottima soluzione.

Le estensioni della classe helper restituiscono informazioni sulle cause principali e ripristinano le informazioni agli utenti tramite NDF. Le stringhe utilizzate per descrivere le cause principali e le informazioni di ripristino devono essere semplici e facili da comprendere per un utente non tecnico. Per ulteriori informazioni su queste stringhe, vedere [linee guida sull'interfaccia utente per le estensioni della classe helper NDF](user-interface-guidelines-for-ndf-helper-class-extensions.md).

## <a name="define-a-component-health-model"></a>Definire un modello di integrità del componente

Gli sviluppatori di software devono definire i livelli di "integrità" associati alla gestibilità dei problemi di rete. Un modello di integrità utilizzato per sviluppare classi helper definisce solo due livelli di integrità: integro e non integro. Questi livelli possono anche essere applicati alle estensioni della classe helper NDF.

Un componente integro indica un'assenza di problemi. Un componente può essere considerato non integro a causa di problemi propri o a causa di problemi che si verificano in altri componenti da cui dipende.



| Termine                                                                                                                             | Descrizione                                                                                                                      |
|----------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------|
| <span id="LowHealth"></span><span id="lowhealth"></span><span id="LOWHEALTH"></span>LowHealth<br/>                         | Questo stato indica un livello di errore inaccettabile da questo componente e che il componente costituisce il problema.<br/>    |
| <span id="LowHealth_Below"></span><span id="lowhealth_below"></span><span id="LOWHEALTH_BELOW"></span>LowHealth di seguito<br/> | Questo stato indica un livello di errore inaccettabile da un componente del computer locale da cui dipende il componente.<br/> |



 

Quando la diagnosi viene utilizzata usando NDF, all'estensione della classe helper viene richiesta una serie di domande per determinare lo stato di integrità. Se l'estensione risponde che non è integro, NDF chiede di chiarire le domande, provare a diagnosticare il problema, la posizione e la posizione in cui eseguire la ricerca. Ogni classe helper deve essere in grado di rispondere alla domanda di basso livello di integrità per poter indirizzare meglio le attività di diagnostica appropriate.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Classe helper Windows Filtering Platform estendibile](windows-filtering-platform-extensible-helper-class.md)
</dt> <dt>

[Classi helper estendibili di diagnostica wireless 802,11](802-11-wireless-diagnostics-extensible-helper-classes.md)
</dt> </dl>

 

 





