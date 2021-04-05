---
title: Destinazioni
description: Una destinazione nella tabella di routing è una voce di rete rappresentata da un indirizzo di rete e un network mask.
ms.assetid: 115d86e3-f933-4601-af10-abaab287b509
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 49c0c758720824284147c2f35be004622157edb3
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103856278"
---
# <a name="destinations"></a>Destinazioni

Una destinazione nella tabella di routing è una voce di rete rappresentata da un indirizzo di rete e un network mask.

Una voce di destinazione nella tabella di routing include:

-   Indirizzo, espresso come indirizzo di rete e network mask.
-   Elenco di route per la destinazione.
-   Elenco di slot del puntatore opaco.
-   Visualizzazioni in cui questa destinazione è valida. La destinazione contiene una struttura per ogni visualizzazione che contiene le informazioni seguenti:
    -   Identificatore per la visualizzazione.
    -   Puntatore al percorso migliore della destinazione in questa visualizzazione.
    -   Proprietario della route migliore in questa visualizzazione.
    -   Flag associati alla route migliore in questa visualizzazione.
    -   Handle per tutte le route in uno stato di attesa in questa visualizzazione.

 

 




