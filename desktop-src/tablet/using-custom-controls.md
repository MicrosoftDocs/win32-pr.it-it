---
description: Descrizione dell'utilizzo dei controlli cliente per il Tablet PC.
ms.assetid: 43d78acd-1f02-417d-97be-1682e90a81a2
title: Uso di controlli personalizzati
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9c713d2b3912d2bbe4a689c7d8d05d4d977a6eb7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103879138"
---
# <a name="using-custom-controls"></a>Uso di controlli personalizzati

È possibile personalizzare i controlli standard usando il disegno del proprietario per modificare l'aspetto del controllo e stabilire una superclasse o una sottoclasse per modificare il comportamento del controllo. In ogni caso, il codice di sistema sottostante per il tipo di controllo standard gestisce le funzioni di controllo di base. La maggior parte di questi controlli può essere accessibile se vengono utilizzati correttamente.

Un controllo creato dal proprietario basato su un controllo standard viene visualizzato come controllo standard per l'accessibilità e supporta Microsoft Active Accessibility; Tuttavia, presenta un aspetto personalizzato. Alcune applicazioni utilizzano controlli personalizzati per modificare l'aspetto di un controllo, ma i controlli creati dal proprietario sono una soluzione più accessibile. Per ulteriori informazioni su come definire i menu creati dal proprietario ed esporre i controlli creati dal proprietario, vedere [accessibilità](../accessibility/accessibility.md).

La definizione di una superclasse o di una sottoclasse è una tecnica per personalizzare il comportamento dei controlli esistenti. A seconda del nuovo comportamento del controllo, potrebbe essere necessario integrare le informazioni di accessibilità esposte. Ad esempio, un'applicazione può utilizzare un controllo creato dal proprietario per visualizzare una X in una casella di controllo selezionata, anziché un segno di spunta o etichettare un pulsante di comando con un'immagine anziché una parola.

Quando si usano i controlli creati dal proprietario che sono una superclasse o una sottoclasse:

-   Fornire etichette per tutti i controlli, anche quando le etichette non sono visibili sullo schermo. Se si personalizza un controllo in modo che la didascalia standard non sia visibile (ad esempio, un pulsante con una faccia grafica) e si lasci la didascalia come stringa vuota, il supporto per l'accessibilità non è in grado di ottenere la didascalia e usarla per identificare il controllo.
-   Assicurarsi che [**WM \_ gettext**](../winmsg/wm-gettext.md) sia supportato.
-   Verificare che tutti i messaggi specifici della classe siano supportati. È particolarmente importante supportare i messaggi di recupero del testo, ad esempio [**CB \_ GETLBTEXT**](../controls/cb-getlbtext.md) e [**lb \_ gettext**](../controls/lb-gettext.md). Impostare i bit di stile appropriati, ad esempio **CBS \_ HASSTRINGS** e **lbs \_ HASSTRINGS**, per indicare che il controllo supporta tali messaggi.

 

 
