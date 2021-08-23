---
description: Descrizione dell'uso dei controlli del cliente per il Tablet PC.
ms.assetid: 43d78acd-1f02-417d-97be-1682e90a81a2
title: Uso di controlli personalizzati
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 70699a141f0319f917953e25363db0e0cd38eb21ecc06345c581b55526ad6bbb
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119551881"
---
# <a name="using-custom-controls"></a>Uso di controlli personalizzati

È possibile personalizzare i controlli standard usando il disegno del proprietario per modificare l'aspetto del controllo e stabilendo una superclasse o una sottoclasse per modificare il comportamento del controllo. In ogni caso, il codice di sistema sottostante per il tipo di controllo standard gestisce le funzioni di controllo di base. La maggior parte di questi controlli può essere accessibile se vengono utilizzati correttamente.

Un controllo disegnato dal proprietario basato su un controllo standard viene visualizzato come controllo standard per supportare l'accessibilità e supporta Microsoft Active Accessibility; ha tuttavia un aspetto personalizzato. Alcune applicazioni usano controlli personalizzati per modificare l'aspetto di un controllo, ma i controlli disegnati dal proprietario sono una soluzione più accessibile. Per altre informazioni su come definire menu disegnati dal proprietario ed esporre controlli disegnati dal proprietario, vedere [Accessibilità](../accessibility/accessibility.md).

La definizione di una superclasse o di una sottoclasse è una tecnica per personalizzare il comportamento dei controlli esistenti. A seconda del nuovo comportamento del controllo, potrebbe essere necessario integrare le informazioni sull'accessibilità che espone. Ad esempio, un'applicazione può usare un controllo disegnato dal proprietario per visualizzare una X in una casella di controllo selezionata, anziché un segno di spunta, oppure assegnare un'etichetta a un pulsante di comando con un'immagine anziché una parola.

Quando si usano controlli disegnati dal proprietario che sono una superclasse o una sottoclasse:

-   Specificare etichette per tutti i controlli, anche quando le etichette non sono visibili sullo schermo. Se si personalizza un controllo in modo che la didascalia standard non sia visibile (ad esempio, un pulsante con un viso grafico) e si lascia la didascalia come stringa vuota, l'aiuto per l'accessibilità non è in grado di ottenere la didascalia e usarla per identificare il controllo.
-   Assicurarsi che [**WM \_ GETTEXT**](../winmsg/wm-gettext.md) sia supportato.
-   Assicurarsi che tutti i messaggi specifici della classe siano supportati. È particolarmente importante supportare i messaggi di recupero del testo, ad esempio [**CB \_ GETLBTEXT**](../controls/cb-getlbtext.md) e [**LB \_ GETTEXT.**](../controls/lb-gettext.md) Impostare i bit di stile appropriati, ad esempio **CBS \_ HASSTRINGS** e **LBS \_ HASSTRINGS,** per indicare che il controllo supporta tali messaggi.

 

 
