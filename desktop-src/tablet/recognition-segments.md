---
description: Un segmento di riconoscimento è l'unità di input penna di base che un riconoscimento utilizza internamente per produrre un risultato di riconoscimento per un oggetto Ink specifico.
ms.assetid: 5215a0bd-6dff-4cda-b2e5-c54f64680e02
title: Segmenti di riconoscimento
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8f7037849378477950b906b85efe6980c4246421
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106317913"
---
# <a name="recognition-segments"></a>Segmenti di riconoscimento

Un segmento di riconoscimento è l'unità di input penna di base che un riconoscimento utilizza internamente per produrre un risultato di riconoscimento per un oggetto Ink specifico. Un segmento di riconoscimento è una raccolta di tratti di input penna. Ad esempio, un riconoscitore in grado di riconoscere la grafia corsiva in lingua inglese potrebbe usare una parola come segmento di riconoscimento di base.

Altri riconoscitori possono usare parti di parole composite come segmenti di base. In spagnolo, ad esempio, le parole brevi sono comunemente combinate per fornire parole composite più lunghe. "Damelo" è una parola spagnola composta da tre parole "da me lo" (Dammi), ma viene scritta come una singola parola. Un riconoscitore spagnolo potrebbe riconoscere ogni sottoparola come segmento.

Un riconoscitore può trovare diversi modi per suddividere un esempio di input penna in segmenti di riconoscimento. Poiché l'ambiguità è richiesta per riconoscere l'input previsto dall'utente, il riconoscimento può restituire molte corrispondenze alternative.

Per ulteriori informazioni sulle alternative, vedere [alternates](alternates.md).

 

 



