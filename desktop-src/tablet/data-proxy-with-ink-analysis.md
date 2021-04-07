---
description: Come indicato nella panoramica dell'analisi dell'input penna, la tecnologia di analisi dell'input penna gestisce internamente un modello di documento basato su albero per contenere i risultati dell'analisi e le relazioni.
ms.assetid: 33ba9292-3bc7-41ba-a602-e2fc94cd3a57
title: Proxy di dati con analisi dell'input penna
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 52717b955625e67f50c20703dd0e84449aa1037f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103884942"
---
# <a name="data-proxy-with-ink-analysis"></a>Proxy di dati con analisi dell'input penna

Come indicato nella [Panoramica dell'analisi dell'input penna](ink-analysis-overview.md), la tecnologia di analisi dell'input penna gestisce internamente un modello di documento basato su albero per contenere i risultati dell'analisi e le relazioni. Se l'applicazione dispone già di un archivio documenti stabilito diverso, sarà necessario utilizzare le funzionalità di analisi dell'input penna progettate per il proxy dei dati tra modelli di documento diversi.

## <a name="types-of-data-proxy"></a>Tipi di proxy di dati

Le funzionalità del proxy di dati consentono all'applicazione di:

-   Integrare nuovamente i dati dei risultati di analisi in un modello di documento esistente.
-   Comunicare nuovamente i risultati precedenti (o lo stato) in [**InkAnalyzer**](inkanalyzer.md).
-   Comunica lo stato non input penna in [**InkAnalyzer**](inkanalyzer.md).
-   Per completare l'operazione di analisi è necessario comunicare solo il set minimo di dati (stato precedente e non input penna).
-   Aggiornare facilmente il modello di documento interno dell'applicazione con i risultati dell'analisi.

Esistono due approcci di base al proxy di dati di analisi dell'input penna. Le differenze depongono i dettagli relativi a quando e come viene eseguita la sincronizzazione tra i modelli di documento. Il primo approccio, aggiornamento sincrono, richiede la modifica del modello di documento di analisi dell'input penna quando si verificano modifiche nel documento dell'applicazione. Il secondo approccio, aggiornamento su richiesta, richiede che vengano passati a [**InkAnalyzer**](inkanalyzer.md)solo i dati interessati dalle modifiche apportate al modello di documento dell'applicazione. Ovvero solo i dati per le parti del modello di documento di analisi dell'input penna che si trovano nella stessa area delle modifiche al documento dell'applicazione devono essere passati a **InkAnalyzer** , perché sono necessari.

### <a name="synchronous-update"></a>Aggiornamento sincrono

L'approccio di aggiornamento sincrono richiede la modifica (creazione ed eliminazione) dei nodi nella raccolta dell'oggetto [**InkAnalyzer**](inkanalyzer.md) degli oggetti [**ContextNode**](icontextnode.md) che si verificano nel documento dell'applicazione. Ad esempio, ogni volta che viene aggiunta una parola di testo all'applicazione, in **InkAnalyzer** viene creato un **oggetto ContextNode** con stile **TextWord** corrispondente. Se la posizione della parola di testo sulla pagina viene modificata, la posizione dell' **oggetto ContextNode** corrispondente viene aggiornata nello stesso momento. Questo metodo è meno efficiente in termini di risorse di elaborazione rispetto al metodo su richiesta, perché ogni modifica del documento comporta un aggiornamento a **InkAnalyzer**, anche se la modifica non influisce sull'input penna.

Nell'esempio seguente viene illustrato il funzionamento dell'aggiornamento sincrono. Si supponga di disporre di un'applicazione con un modello di documento esistente. Quando l'utente finale apporta una modifica al documento, ad esempio aggiungendo nuovo testo, la modifica viene elaborata come indicato di seguito:

1.  L'utente finale crea i nuovi dati.
2.  L'applicazione determina come elaborare i dati, archiviarli ed eseguirne il rendering.
3.  Ai fini pratici, i passaggi seguenti avvengono simultaneamente.
    1.  L'applicazione inserisce i dati nel modello di documento.
    2.  L'applicazione crea un [**oggetto InkAnalyzer**](inkanalyzer.md) e lo aggiorna. Questa operazione garantisce simultaneamente che l' **oggetto InkAnalyzer** disponga sempre delle informazioni più recenti.
    3.  L'applicazione chiama [**BackgroundAnalyze**](iinkanalyzer-backgroundanalyze.md) sull' [**oggetto InkAnalyzer**](inkanalyzer.md) per iniziare l'analisi.
4.  Una serie di eventi viene generata se la modifica riguarda l'input penna e l' [**oggetto InkAnalyzer**](inkanalyzer.md) determina nuovi risultati. Viene generato un evento per ogni modifica apportata alla raccolta di oggetti [**ContextNode**](icontextnode.md) nell' **oggetto InkAnalyzer**. Questi eventi includono [**ContextNodeCreated**](-ianalysisproxyevents-contextnodecreated.md), [**l'ContextNodeDeleting**](-ianalysisproxyevents-contextnodedeleting.md), [**ContextNodeMovingToPosition**](-ianalysisproxyevents-contextnodemovingtoposition.md), [**ContextNodePropertiesUpdated**](-ianalysisproxyevents-contextnodepropertiesupdated.md), [**ContextNodeLinkAdding**](-ianalysisproxyevents-contextnodelinkadding.md), [**l'ContextNodeLinkDeleting**](-ianalysisproxyevents-contextnodelinkdeleting.md)e [**l'ContextNodeReparenting**](-ianalysisproxyevents-contextnodereparenting.md). L'applicazione gestisce questi eventi per eseguire il proxy dei risultati dell'operazione di analisi nel modello di documento nel modo appropriato.
5.  L'applicazione aggiorna il layout del documento, estraendo i nuovi dati dal modello di documento.
6.  Viene eseguito il rendering dei nuovi dati all'utente finale.

### <a name="on-demand-update"></a>Aggiornamento su richiesta

L'approccio su richiesta richiede solo che i dati vengano passati per gli oggetti [**ContextNode**](icontextnode.md) presenti nelle aree analizzate. Gli oggetti **ContextNode** necessari vengono estratti dal modello di documento dell'applicazione subito dopo che è stata richiamata l'operazione di analisi e di nuovo prima di riconciliare i risultati. Sebbene sia più complicato implementare degli aggiornamenti sincroni, questo approccio consente di ottenere risultati migliori delle prestazioni.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Panoramica dell'analisi dell'input penna](ink-analysis-overview.md)
</dt> <dt>

[**Classe InkAnalyzer (C++)**](inkanalyzer.md)
</dt> <dt>

[**Microsoft. Ink. InkAnalyzer**](/previous-versions/ms583671(v=vs.100))
</dt> <dt>

[**Microsoft. Ink. ContextNode**](/previous-versions/ms551996(v=vs.100))
</dt> </dl>

 

 
