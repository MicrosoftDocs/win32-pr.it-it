---
description: Un'azione viene eseguita nel Windows installer chiamando la funzione MsiDoAction o includendo l'azione in una tabella di sequenza.
ms.assetid: ee5bdc72-adf4-46f4-ae1f-4c41d22a1ed8
title: Uso di azioni standard
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 60696e79c12b054739d87ffe5696e898a8eb955c4c7bfe0aa9c2341db7c2d720
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119996211"
---
# <a name="using-standard-actions"></a>Uso di azioni standard

Un'azione viene eseguita nel Windows installer chiamando la [**funzione MsiDoAction**](/windows/desktop/api/Msiquery/nf-msiquery-msidoactiona) o includendo l'azione in una tabella di sequenza. Poiché la maggior parte delle azioni incapsula un singolo scopo, il modo più comune per usare le azioni è ordinare una serie di azioni in una sequenza per eseguire un'attività più grande. Il programma di installazione dispone di tre azioni standard di primo livello che chiamano un set associato di tabelle di sequenza. Queste tabelle di sequenza associate possono contenere azioni standard, azioni personalizzate ed elementi dell'interfaccia utente. A ogni azione in una tabella di sequenza è associato un numero di sequenza e può anche essere associata un'espressione condizionale. Tutte le azioni in una tabella di sequenza vengono visitate nell'ordine e vengono eseguite solo se l'espressione condizionale restituisce True.

Anche se a un'azione standard può essere associato qualsiasi numero di sequenza, molti hanno restrizioni di sequenza che devono essere seguite per il corretto funzionamento dell'azione. Ad esempio, [l'azione FileCost](filecost-action.md)deve essere chiamata dopo [l'azione CostInitialize](costinitialize-action.md). Per altre informazioni sulle restrizioni di sequenziazione delle azioni standard, vedere Actions [with Sequencing Restrictions](actions-with-sequencing-restrictions.md)( Azioni con restrizioni di sequenziazione), [Actions without Sequencing Restrictions](actions-without-sequencing-restrictions.md)(Azioni senza restrizioni di sequenziazione) o [Standard Actions Reference (Informazioni di riferimento sulle azioni standard).](standard-actions-reference.md)

Negli argomenti seguenti vengono fornite altre informazioni sull'uso delle azioni standard.

-   [Pubblicazione di prodotti, funzionalità e componenti](publishing-products-features-and-components.md)
-   [Ricerca di file](file-searching.md)
-   [Determinazione dei costi dei file](file-costing.md)
-   [Installazione di file](file-installation.md)
-   [Modifica del Registro di sistema](modifying-the-registry.md)
-   [Esecuzione di azioni](running-actions.md)

Vedere anche [Informazioni sulle azioni standard](about-standard-actions.md) o le informazioni di riferimento sulle azioni [standard.](standard-actions-reference.md)

 

 



