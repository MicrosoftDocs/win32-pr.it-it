---
description: Un'azione viene eseguita nel Windows Installer chiamando la funzione MsiDoAction o includendo l'azione in una tabella di sequenza.
ms.assetid: ee5bdc72-adf4-46f4-ae1f-4c41d22a1ed8
title: Uso di azioni standard
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1f52118580f4e18f07f86bd15da73f9aafb453c8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106309992"
---
# <a name="using-standard-actions"></a>Uso di azioni standard

Un'azione viene eseguita nel Windows Installer chiamando la funzione [**MsiDoAction**](/windows/desktop/api/Msiquery/nf-msiquery-msidoactiona) o includendo l'azione in una tabella di sequenza. Poiché la maggior parte delle azioni incapsula un solo scopo, il modo più comune per usare le azioni consiste nell'ordinare una serie di azioni in una sequenza per eseguire un'attività più ampia. Il programma di installazione prevede tre azioni di livello principale standard che chiamano un set associato di tabelle di sequenza. Queste tabelle di sequenza associate possono contenere azioni standard, azioni personalizzate ed elementi dell'interfaccia utente. A ogni azione in una tabella di sequenza è associato un numero di sequenza e può inoltre essere associata un'espressione condizionale. Tutte le azioni in una tabella di sequenza vengono visitate in ordine e vengono eseguite solo se l'espressione condizionale restituisce true.

Mentre un'azione standard può avere un numero di sequenza associato, molti presentano restrizioni di sequenza che devono essere seguite per il corretto funzionamento dell'azione. Ad esempio, l' [azione filecost](filecost-action.md)deve essere chiamata dopo l' [azione CostInitialize](costinitialize-action.md). Per ulteriori informazioni sulle restrizioni di sequenziazione delle azioni standard, vedere [azioni con restrizioni di sequenziazione](actions-with-sequencing-restrictions.md), [azioni senza restrizioni di sequenziazione](actions-without-sequencing-restrictions.md)o [riferimento a azioni standard](standard-actions-reference.md).

Negli argomenti seguenti vengono fornite ulteriori informazioni sull'utilizzo delle azioni standard.

-   [Pubblicazione di prodotti, funzionalità e componenti](publishing-products-features-and-components.md)
-   [Ricerca file](file-searching.md)
-   [Costo file](file-costing.md)
-   [Installazione file](file-installation.md)
-   [Modifica del registro di sistema](modifying-the-registry.md)
-   [Azioni in esecuzione](running-actions.md)

Vedere anche le [informazioni di riferimento sulle azioni standard o sulle](about-standard-actions.md) [azioni standard](standard-actions-reference.md).

 

 



