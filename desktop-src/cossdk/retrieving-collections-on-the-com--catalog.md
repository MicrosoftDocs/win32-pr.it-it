---
description: Recupero di raccolte nel catalogo COM+
ms.assetid: 7cd5c491-6c85-410f-845b-c2f7b4f2a560
title: Recupero di raccolte nel catalogo COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 27cbf81bfedd4ba37b74b36e5ad9a8ad320e9c39
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103748031"
---
# <a name="retrieving-collections-on-the-com-catalog"></a>Recupero di raccolte nel catalogo COM+

I dati nel catalogo COM+ vengono archiviati all'interno di una gerarchia di raccolte. Nello strumento di amministrazione Servizi componenti, molte di queste raccolte vengono visualizzate come cartelle nell'albero della console. È possibile accedere alle raccolte che non sono visualizzate come cartelle solo a livello di codice. Le raccolte vengono utilizzate come contenitori per gli elementi. Gli elementi di una raccolta specifica sono tutti di un tipo coerente; ovvero tutti rappresentano lo stesso tipo di elemento e può essere presente un numero arbitrario di elementi in una raccolta. La raccolta [**Applications**](applications.md) , ad esempio, contiene un elemento per ogni applicazione com+ installata nel computer. Questa raccolta viene visualizzata nello strumento di amministrazione come cartella **applicazioni com+** .

Le raccolte si verificano in una struttura gerarchica perché gli elementi che contengono seguono un ordine di inclusione innato. Poiché, ad esempio, i componenti vengono installati in un'applicazione COM+, la raccolta [**Components**](components.md) viene configurata logicamente nella raccolta di [**applicazioni**](applications.md) . In particolare, per conservare i componenti installati in un'applicazione specifica, è presente una raccolta di **componenti** distinti per ogni elemento nella raccolta di **applicazioni** .

È necessario ottenere una raccolta nel catalogo quando si desidera recuperare un elemento e impostare le relative proprietà. Nel caso generale, è necessario eseguire diverse raccolte per ottenere l'elemento desiderato. Per la procedura per eseguire questa operazione, vedere [esplorazione della gerarchia della raccolta com+](navigating-the-com--collection-hierarchy.md).

Dopo aver recuperato una raccolta e prima di poter utilizzare direttamente gli elementi in esso contenuti, è necessario popolare la raccolta, che recupera i dati per il contenuto della raccolta dal catalogo COM+. Per informazioni dettagliate, vedere [popolamento di raccolte com+](populating-com--collections.md).

Inoltre, è possibile usare una funzionalità che consente di eseguire query in modo dinamico per vedere quali raccolte correlate sono disponibili da una determinata raccolta che si sta mantenendo. Per informazioni dettagliate, vedere [esecuzione di query per le raccolte correlate disponibili](querying-for-available-related-collections.md).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Operazioni di amministrazione COM+ all'interno delle transazioni](com--administration-operations-within-transactions.md)
</dt> <dt>

[Gestione degli errori di amministrazione COM+](handling-com--administration-errors.md)
</dt> <dt>

[Esempio introduttivo di utilizzo del catalogo di amministrazione COM+](introductory-example-using-the-com--administration-catalog.md)
</dt> <dt>

[Panoramica degli oggetti COMAdmin](overview-of-the-comadmin-objects.md)
</dt> <dt>

[Impostazione delle proprietà e salvataggio delle modifiche nel catalogo COM+](setting-properties-and-saving-changes-to-the-com--catalog.md)
</dt> </dl>

 

 



