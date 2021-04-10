---
description: Interdipendenze tra proprietà
ms.assetid: 1c7c7c76-ec27-4ee4-a860-24244843a1e5
title: Interdipendenze tra proprietà
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6df8015c3fc49e35f5079315f6c056f680ebcc12
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103966172"
---
# <a name="interdependencies-between-properties"></a>Interdipendenze tra proprietà

Quando si impostano le proprietà, il catalogo COM+ applica una logica coerenza per assicurarsi di configurare gli elementi in modo ragionevole. Questa logica può essere implementata in due modi, come indicato di seguito:

-   **Dipendenze.** È possibile che non vengano apportate modifiche perché un'altra proprietà dipende da una particolare impostazione per una proprietà che si tenta di impostare. Se, ad esempio, un componente viene impostato con le transazioni dell'attributo richieste e se si tenta di modificare l'impostazione di sincronizzazione su None, viene generato un errore quando si tenta di chiamare [**SaveChanges**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-savechanges) perché le transazioni dipendono dalla sincronizzazione.
-   **Effetti collaterali.** Alcune proprietà possono essere modificate senza impostarle in modo esplicito. Se, ad esempio, si imposta un componente con le transazioni degli attributi necessarie, anche la sincronizzazione verrà impostata su Required. Si tratta in realtà del lato invertito delle dipendenze: una proprietà ha la precedenza rispetto a un'altra e la relativa dipendenza viene espressa tramite la prima impostazione della proprietà secondaria e quindi bloccando le modifiche apportate a tale proprietà.

Nell'elenco delle proprietà esposte da elementi di una raccolta, tutte elencate in [raccolte di amministrazione com+](com--administration-collections.md), le dipendenze e gli effetti collaterali vengono indicati per ogni proprietà. Quando si configurano le applicazioni e i componenti COM+, è necessario tenere presente quali vincoli vengono imposti alle configurazioni.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Recupero e impostazione delle proprietà](getting-and-setting-properties.md)
</dt> <dt>

[Esecuzione di query per le proprietà disponibili](querying-for-available-properties.md)
</dt> <dt>

[Salvataggio o eliminazione di modifiche](saving-or-discarding-changes.md)
</dt> </dl>

 

 



