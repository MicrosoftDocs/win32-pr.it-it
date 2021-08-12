---
description: Oltre al riconoscimento del testo, i riconoscitori possono riconoscere una classe di oggetti correlati.
ms.assetid: 53b6137d-2998-4a3b-b469-3d1204ea194b
title: Riconoscitori di oggetti
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aabfd44a5eb126d48df70efd1c391584d12afc94e5e21c714aa0c740a7d486f3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118449662"
---
# <a name="object-recognizers"></a>Riconoscitori di oggetti

Oltre al riconoscimento del testo, i riconoscitori possono riconoscere una classe di oggetti correlati. I riconoscitori di oggetti riconoscono le forme generali in base allo scopo. I riconoscitori di oggetti vengono usati per riconoscere:

-   Note per il tempo
-   Forme geometriche
-   Equazioni matematiche
-   Flow elementi del grafico

In genere, gli oggetti riconosciuti da tale sistema di riconoscimento si trovano in una relazione spaziale o funzionale bidimensionale tra loro. Ad esempio, all'interno delle relazioni complesse in un'equazione matematica, un riconoscitore può restituire risultati diversi per un limite superiore su un integrale definito anziché su un numeratore in una frazione.

A causa della natura molto generale di queste relazioni, è estremamente difficile definire il set di interfacce che funzioneranno per ogni sistema di riconoscimento di oggetti.

La tecnologia Tablet PC fornisce un framework di base per i riconoscitori di oggetti nelle interfacce di automazione e della libreria gestita. Tuttavia, è necessario sviluppare interfacce personalizzate che descrivono relazioni spaziali complesse tra gli oggetti riconosciuti per ogni sistema di riconoscimento di oggetti. In particolare, per i riconoscitori di oggetti, la piattaforma fornisce l'oggetto [**RecognizerContext**](inkrecognizercontext-class.md) di base per associare l'oggetto [**Ink**](inkdisp-class.md) al contesto del riconoscitore e per chiamare il riconoscitore per eseguire il riconoscimento.

 

 



