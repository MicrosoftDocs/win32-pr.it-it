---
title: Progettazione di estensioni di classi helper NDF
description: Questo argomento ha lo scopo di fornire indicazioni generiche tramite il processo di sviluppo dell'estensione della classe helper.
ms.assetid: f5dbd198-7d22-4e7e-830e-6753e9f4d6c8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 474a9f4ade01fe98a8db30568aa6a7c4978156d2c791747353071f020af27605
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119802361"
---
# <a name="designing-ndf-helper-class-extensions"></a>Progettazione di estensioni di classi helper NDF

Questo argomento ha lo scopo di fornire indicazioni generiche tramite il processo di sviluppo dell'estensione della classe helper. Le indicazioni in questo argomento si applicano a tutte le estensioni di classe helper. Per indicazioni più specifiche, vedere Windows classe helper [estendibile](windows-filtering-platform-extensible-helper-class.md) della piattaforma di filtro e [802.11 Wireless Diagnostics Extensible Helper Classes](802-11-wireless-diagnostics-extensible-helper-classes.md).

## <a name="extending-ndf-functionality"></a>Estensione della funzionalità NDF

Windows Vista e versioni successive vengono forniti con un'ampia gamma di classi helper già implementate in grado di diagnosticare e correggere un'ampia gamma di problemi. A volte, tuttavia, gli sviluppatori di terze parti possono voler estendere queste classi helper per diagnosticare e risolvere i problemi specifici dei prodotti e delle implementazioni specifici.

Le classi helper Microsoft NDF seguenti sono estendibili.

-   [Piattaforma filtro Windows](windows-filtering-platform-extensible-helper-class.md)
-   [Sicurezza wireless](802-11-wireless-diagnostics-extensible-helper-classes.md)

## <a name="implementing-a-helper-class-extension"></a>Implementazione di un'estensione di classe helper

Microsoft fornisce due interfacce che possono essere usate per sviluppare estensioni di classi helper NDF.

[**L'interfaccia INetDiagHelperInfo**](/windows/desktop/api/ndhelper/nn-ndhelper-inetdiaghelperinfo) viene chiamata da NDF per verificare che abbia tutte le informazioni necessarie e che abbia scelto la classe helper corretta. Questa operazione viene eseguita tramite il [**metodo GetAttributeInfo.**](/windows/desktop/api/ndhelper/nf-ndhelper-inetdiaghelperinfo-getattributeinfo)

[**L'interfaccia INetDiagHelper**](/windows/desktop/api/ndhelper/nn-ndhelper-inetdiaghelper) viene chiamata da NDF per la maggior parte delle attività che si verificano durante la procedura di diagnostica. Sono necessari diversi metodi, mentre altri sono facoltativi per usi specifici.

I metodi necessari includono [**Initialize**](/windows/desktop/api/ndhelper/nf-ndhelper-inetdiaghelper-initialize) e [**GetDiagnosticsInfo**](/windows/desktop/api/ndhelper/nf-ndhelper-inetdiaghelper-getdiagnosticsinfo). NDF chiama **Initialize per** inviare i parametri chiave all'estensione della classe helper per inizializzare lo stato dell'istanza. **GetDiagnosticsInfo** fornisce una stima del tempo necessario per la diagnosi e se richiede la rappresentazione del contesto utente originale.

Viene chiamato un [**altro metodo, LowHealth,**](/windows/desktop/api/ndhelper/nf-ndhelper-inetdiaghelper-lowhealth)per eseguire la diagnosi sul componente di rete corrispondente alla classe helper. [**Il metodo**](/windows/desktop/api/ndhelper/nf-ndhelper-inetdiaghelper-cancel) Cancel viene chiamato quando la funzione definita dall'utente determina l'arresto di una diagnosi o di una riparazione in corso. [**La**](/windows/desktop/api/ndhelper/nf-ndhelper-inetdiaghelper-cleanup) pulizia consente a NDF di rilasciare le risorse NDF usate dall'estensione della classe helper dopo la chiamata a [**Initialize.**](/windows/desktop/api/ndhelper/nf-ndhelper-inetdiaghelper-initialize)

Per informazioni sui metodi aggiuntivi, vedere [**INetDiagHelper**](/windows/desktop/api/ndhelper/nn-ndhelper-inetdiaghelper).

Le estensioni della classe helper NDF vengono usate per diagnosticare e risolvere i problemi di connettività associati a un'applicazione o a un componente specifico. Convalidano anche l'esito positivo o negativo di un tentativo di risoluzione.

Gli sviluppatori che considerano l'implementazione di un'estensione di classe helper devono eseguire le attività seguenti.

-   Identificare gli scenari utente in cui le azioni di diagnostica e ripristino sono utili.
-   Fornire soluzioni ai problemi di connettività riscontrati di frequente.
-   Se è necessaria un'estensione della classe helper, definire un modello di integrità del componente usato per rappresentare lo stato di integrità del componente in NDF.

## <a name="identify-user-scenarios"></a>Identificare gli scenari utente

Il test e l'uso di un'applicazione potrebbero aver già fornito modelli individuabili che un'estensione di classe helper può essere in grado di diagnosticare ed eventualmente correggere. Gli sviluppatori di applicazioni possono usare questi dati per determinare i problemi di connettività più importanti da risolvere e per identificare gli scenari utente in cui è probabile che si verifichino problemi di connettività.

Determinare la causa radice di ogni problema è fondamentale in questa parte del processo. Questa operazione può richiedere ricerche approfondite, ma consente di creare software molto più semplice da usare per utenti e amministratori. Se non viene identificata una causa radice, diventa difficile o impossibile offrire la risoluzione dei problemi usando l'estensione della classe helper.

## <a name="provide-resolutions"></a>Fornire risoluzioni

Dopo che un team di sviluppo ha identificato le cause principali dei problemi associati al software, il passaggio successivo consiste nell'identificare le azioni di risoluzione appropriate per aiutare l'utente a risolvere il problema nel modo più efficiente possibile.

Non tutte le risoluzioni richiedono la creazione di un'estensione di classe helper o di un'azione automatizzata. In alcuni casi, il team può determinare che l'approccio migliore per risolvere una causa radice consiste nel correggere o aggiornare il componente, fornire ulteriore contenuto della Guida per il componente o sviluppare altre strategie che forniscono soluzioni migliori a lungo termine.

Per i problemi in cui un'azione automatizzata è ideale, la creazione di un'estensione di classe helper NDF è spesso una soluzione eccellente.

Le estensioni della classe helper restituiscono informazioni sulle cause radice e le informazioni di ripristino agli utenti tramite NDF. Le stringhe usate per descrivere le cause radice e le informazioni di ripristino devono essere semplici e facili da comprendere per un utente non tecnico. Per altre informazioni su queste stringhe, vedere linee guida Interfaccia utente per le estensioni di classe [helper NDF](user-interface-guidelines-for-ndf-helper-class-extensions.md).

## <a name="define-a-component-health-model"></a>Definire un modello di integrità dei componenti

Gli sviluppatori di software devono definire i livelli di "integrità" associati alla gestibilità dei problemi di rete. Un modello di integrità usato per sviluppare classi helper definisce solo due livelli di integrità: integro e non integro. Questi livelli possono essere applicati anche alle estensioni della classe helper NDF.

Un componente integro indica un'assenza di problemi. Un componente può essere considerato non integro a causa dei propri problemi o a causa di problemi che si verificano in altri componenti da cui dipende.



| Termine                                                                                                                             | Descrizione                                                                                                                      |
|----------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------|
| <span id="LowHealth"></span><span id="lowhealth"></span><span id="LOWHEALTH"></span>LowHealth<br/>                         | Questo stato indica un livello inaccettabile di errori da questo componente e che il componente è il problema.<br/>    |
| <span id="LowHealth_Below"></span><span id="lowhealth_below"></span><span id="LOWHEALTH_BELOW"></span>LowHealth di seguito<br/> | Questo stato indica un livello inammissibile di errori da un componente del computer locale da cui dipende questo componente.<br/> |



 

Quando la diagnosi viene fatta usando NDF, all'estensione della classe helper viene posta una serie di domande per determinarne lo stato di integrità. Se l'estensione risponde che non è integra, la funzione definita dall'utente pone domande chiare, provando a diagnosticare il problema, la posizione e la posizione successiva. Ogni classe helper deve essere in grado di rispondere alla domanda di integrità insufficiente per indirizzare meglio le attività diagnostiche appropriate.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Windows Classe helper estendibile della piattaforma di filtro](windows-filtering-platform-extensible-helper-class.md)
</dt> <dt>

[802.11 Wireless Diagnostics Extensible Helper Classes](802-11-wireless-diagnostics-extensible-helper-classes.md)
</dt> </dl>

 

 





