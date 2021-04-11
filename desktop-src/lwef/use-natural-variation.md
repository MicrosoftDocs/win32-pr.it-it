---
title: USA variazione naturale
description: USA variazione naturale
ms.assetid: 5d5750e4-cf30-43dc-9419-7e6bbdb9aa5a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1fd2d35afeb168dc8839ba259f0079434b487c4f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104116757"
---
# <a name="use-natural-variation"></a>USA variazione naturale

\[Microsoft Agent è stato deprecato a partire da Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]

Sebbene la coerenza della presentazione nell'interfaccia convenzionale dell'applicazione, ad esempio i menu e le finestre di dialogo, renda l'interfaccia più prevedibile, variare l'animazione e l'output parlato nell'interfaccia del carattere. La variazione appropriata delle risposte del carattere fornisce un'interfaccia più naturale. Se un carattere indirizza sempre l'utente esattamente allo stesso modo; Se ad esempio si dicono sempre le stesse parole, l'utente può prendere in considerazione il carattere noioso, disinteressato o addirittura rude. La comunicazione umana raramente comporta una ripetizione precisa. Anche quando si ripete qualcosa in una situazione simile, è possibile modificare il wording, i movimenti o l'espressione facciale.

Microsoft Agent consente di compilare alcune varianti per un carattere. Quando si definiscono le animazioni di un carattere, è possibile usare le probabilità di diramazione in qualsiasi frame di animazione per modificare un'animazione durante la riproduzione. È anche possibile assegnare più animazioni a ogni stato. Microsoft Agent sceglie in modo casuale una delle animazioni assegnate ogni volta che viene avviato uno stato. Per l'output vocale, è anche possibile includere caratteri barra verticale nel testo di output per variare automaticamente il testo parlato. Microsoft Agent, ad esempio, selezionerà in modo casuale una delle istruzioni seguenti quando si elabora questo testo come parte del metodo [**Speak**](speak-method.md) :

"Posso dire. \| Posso dirlo. \| Posso pronunciare un altro elemento ".

 

 




