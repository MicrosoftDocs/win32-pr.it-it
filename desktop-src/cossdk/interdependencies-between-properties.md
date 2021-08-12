---
description: Interdipendenze tra proprietà
ms.assetid: 1c7c7c76-ec27-4ee4-a860-24244843a1e5
title: Interdipendenze tra proprietà
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fdb039db26ee06868da0b1832e1a3af2692ac47cde73bf7fe5c2e934916c4f4c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118547677"
---
# <a name="interdependencies-between-properties"></a>Interdipendenze tra proprietà

Quando si impostano le proprietà, il catalogo COM+ applica una logica di coerenza per assicurarsi di configurare gli elementi in modo ragionevole. Questa logica può essere implementata in due modi, come indicato di seguito:

-   **Dipendenze.** Potrebbe essere impedito di apportare alcune modifiche perché un'altra proprietà dipende da un'impostazione specifica per una proprietà che si tenta di impostare. Ad esempio, se un componente è impostato con l'attributo Transactions Required e quindi si tenta di modificare l'impostazione Synchronization su None, viene generato un errore quando si tenta di chiamare [**SaveChanges**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-savechanges) perché le transazioni dipendono dalla sincronizzazione.
-   **Effetti collaterali.** Alcune proprietà potrebbero essere modificate automaticamente senza impostarle in modo esplicito. Ad esempio, se si imposta un componente con l'attributo Transazioni necessarie, anche la sincronizzazione verrà impostata su Obbligatorio. Si tratta in realtà del rovescio della pagina delle dipendenze: una proprietà ha la precedenza su un'altra e la relativa dipendenza viene espressa impostando prima la proprietà secondaria e quindi bloccando le modifiche.

Nell'elenco delle proprietà esposte dagli elementi di una raccolta, tutte elencate in Raccolte di amministrazione [COM+,](com--administration-collections.md)le dipendenze e gli effetti collaterali vengono indicati per ogni proprietà. Quando si configurano applicazioni e componenti COM+, è necessario tenere presenti i vincoli imposti alle configurazioni.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Recupero e impostazione delle proprietà](getting-and-setting-properties.md)
</dt> <dt>

[Esecuzione di query per le proprietà disponibili](querying-for-available-properties.md)
</dt> <dt>

[Salvataggio o rimozione delle modifiche](saving-or-discarding-changes.md)
</dt> </dl>

 

 



