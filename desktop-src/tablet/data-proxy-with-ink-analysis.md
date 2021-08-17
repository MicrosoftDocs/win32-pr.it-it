---
description: Come accennato in Panoramica dell'analisi dell'input penna, la tecnologia di analisi dell'input penna gestisce internamente un modello di documento basato su albero per contenere i risultati e le relazioni dell'analisi.
ms.assetid: 33ba9292-3bc7-41ba-a602-e2fc94cd3a57
title: Proxy dati con analisi input penna
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ad79a37a3220351adad56c0a131392e96964714114ba1e0a982833b07bc85077
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119092780"
---
# <a name="data-proxy-with-ink-analysis"></a>Proxy dati con analisi input penna

Come accennato in [Panoramica dell'analisi](ink-analysis-overview.md)dell'input penna, la tecnologia di analisi dell'input penna gestisce internamente un modello di documento basato su albero per contenere i risultati e le relazioni dell'analisi. Se l'applicazione ha già un archivio documenti stabilito diverso, sarà necessario usare le funzionalità di analisi dell'input penna progettate per eseguire il proxy dei dati tra modelli di documento diversi.

## <a name="types-of-data-proxy"></a>Tipi di proxy di dati

Le funzionalità del proxy dati consentono all'applicazione di:

-   Integrare di nuovo i dati dei risultati dell'analisi in un modello di documento esistente.
-   Comunicare nuovamente i risultati (o lo stato) precedenti [**in InkAnalyzer.**](inkanalyzer.md)
-   Comunicare lo stato non input penna [**in InkAnalyzer**](inkanalyzer.md).
-   Comunicare solo il set minimo di dati (stato precedente e non input penna) necessario per completare l'operazione di analisi.
-   Aggiornare facilmente il modello di documento interno dell'applicazione con i risultati dell'analisi.

Esistono due approcci di base al proxy dei dati di analisi dell'input penna. Le differenze si verificano nei dettagli di quando e come si verifica la sincronizzazione tra i modelli di documento. Il primo approccio, l'aggiornamento sincrono, richiede la modifica del modello di documento di analisi dell'input penna quando si verificano modifiche nel documento dell'applicazione. Il secondo approccio, l'aggiornamento su richiesta, richiede che solo i dati interessati dalle modifiche al modello di documento dell'applicazione siano passati a [**InkAnalyzer.**](inkanalyzer.md) In altre informazioni, solo i dati per le parti del modello di documento analisi input penna presenti nella stessa area delle modifiche al documento dell'applicazione devono essere passati a **InkAnalyzer** in base alle esigenze.

### <a name="synchronous-update"></a>Aggiornamento sincrono

L'approccio di aggiornamento sincrono richiede la modifica (creazione ed eliminazione) dei nodi nella raccolta di oggetti [**ContextNode**](icontextnode.md) dell'oggetto [**InkAnalyzer**](inkanalyzer.md) nel momento in cui si verificano nel documento dell'applicazione. Ad esempio, ogni volta che viene aggiunta una parola di testo all'applicazione, viene creato un **contextNode** con stile **TextWord** corrispondente in **InkAnalyzer.** Se la posizione della parola di testo nella pagina cambia, la posizione del **ContextNode** corrispondente viene aggiornata contemporaneamente. Questo metodo è meno efficiente in termini di risorse di calcolo rispetto al metodo su richiesta perché ogni modifica del documento comporta un aggiornamento di **InkAnalyzer,** anche se la modifica non influisce sull'input penna analizzato.

L'esempio seguente illustra il funzionamento dell'aggiornamento sincrono. Imagine un'applicazione con un modello di documento esistente. Quando l'utente finale apporta una modifica al documento, ad esempio l'aggiunta di nuovo testo, la modifica viene elaborata nel modo seguente:

1.  L'utente finale crea i nuovi dati.
2.  L'applicazione determina come elaborare i dati, archiviarli ed eseguirne il rendering.
3.  Per scopi pratici, i passaggi seguenti vengono esersi contemporaneamente.
    1.  L'applicazione inserisce i dati nel modello di documento.
    2.  L'applicazione crea [**un oggetto InkAnalyzer**](inkanalyzer.md) e lo aggiorna. Questa operazione assicura contemporaneamente che **InkAnalyzer** abbia sempre le informazioni più recenti.
    3.  L'applicazione chiama [**BackgroundAnalyze**](iinkanalyzer-backgroundanalyze.md) in [**InkAnalyzer per**](inkanalyzer.md) iniziare l'analisi.
4.  Una serie di eventi viene generato se la modifica interessa l'input penna e [**InkAnalyzer**](inkanalyzer.md) determina nuovi risultati. Viene generato un evento per ogni modifica apportata alla raccolta di [**oggetti ContextNode**](icontextnode.md) in **InkAnalyzer.** Questi eventi includono [**ContextNodeCreated,**](-ianalysisproxyevents-contextnodecreated.md) [**ContextNodeDeleting,**](-ianalysisproxyevents-contextnodedeleting.md) [**ContextNodeMovingToPosition,**](-ianalysisproxyevents-contextnodemovingtoposition.md) [**ContextNodePropertiesUpdated,**](-ianalysisproxyevents-contextnodepropertiesupdated.md) [**ContextNodeLinkAdding,**](-ianalysisproxyevents-contextnodelinkadding.md) [**ContextNodeLinkDeleting**](-ianalysisproxyevents-contextnodelinkdeleting.md)e [**ContextNodeReparenting.**](-ianalysisproxyevents-contextnodereparenting.md) L'applicazione gestisce questi eventi per eseguire il proxy dei risultati dell'operazione di analisi nel modello di documento in base alle esigenze.
5.  L'applicazione aggiorna il layout del documento, estraendo i nuovi dati dal modello di documento.
6.  Il rendering dei nuovi dati viene eseguito all'utente finale.

### <a name="on-demand-update"></a>Aggiornamento su richiesta

L'approccio su richiesta richiede solo che i dati vengano passati per gli oggetti [**ContextNode**](icontextnode.md) presenti nelle aree analizzate. Gli oggetti **ContextNode** necessari vengono estratti dal modello di documento dell'applicazione subito dopo la chiamata dell'operazione di analisi e di nuovo prima di riconcilare i risultati. Sebbene sia più complesso da implementare rispetto agli aggiornamenti sincroni, questo approccio produce risultati migliori in termini di prestazioni.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Panoramica dell'analisi dell'input penna](ink-analysis-overview.md)
</dt> <dt>

[**Classe InkAnalyzer (C++)**](inkanalyzer.md)
</dt> <dt>

[**Microsoft.Ink.InkAnalyzer**](/previous-versions/ms583671(v=vs.100))
</dt> <dt>

[**Microsoft.Ink.ContextNode**](/previous-versions/ms551996(v=vs.100))
</dt> </dl>

 

 
