---
description: Oltre a riconoscere il testo, i riconoscitori possono riconoscere una classe di oggetti correlati.
ms.assetid: 53b6137d-2998-4a3b-b469-3d1204ea194b
title: Riconoscitori di oggetti
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 83a258c8486bcf773f5f94c4de51c501e107fac4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103968039"
---
# <a name="object-recognizers"></a>Riconoscitori di oggetti

Oltre a riconoscere il testo, i riconoscitori possono riconoscere una classe di oggetti correlati. I riconoscitori di oggetti riconoscono le forme generali, in base allo scopo. I riconoscitori di oggetti vengono usati per riconoscere:

-   Note musicali
-   Forme geometriche
-   Equazioni matematiche
-   Elementi del diagramma di flusso

In genere, gli oggetti riconosciuti da un riconoscimento di questo tipo si trovano in una relazione spaziale o funzionale bidimensionale. Ad esempio, all'interno delle relazioni complesse in un'equazione matematica, un riconoscitore può restituire risultati diversi per un limite superiore su un integrale definito anziché un numeratore in una frazione.

A causa della natura generale di queste relazioni, è estremamente difficile definire il set di interfacce che funzioneranno per ogni riconoscimento di oggetti.

La tecnologia Tablet PC fornisce un Framework di base per i riconoscitori di oggetti nelle interfacce di automazione e libreria gestita. È tuttavia necessario sviluppare interfacce personalizzate che descrivono relazioni spaziali complesse tra oggetti riconosciuti per ogni riconoscimento di oggetti. In particolare, per i riconoscitori di oggetti, la piattaforma fornisce l'oggetto [**RecognizerContext**](inkrecognizercontext-class.md) di base per associare l'oggetto [**Ink**](inkdisp-class.md) al contesto di riconoscimento e per chiamare il riconoscimento per eseguire il riconoscimento.

 

 



