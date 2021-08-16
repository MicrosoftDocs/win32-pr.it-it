---
description: Impostando la proprietà Factoid su Nessuno, il riconoscimento dei caratteri riconosce la grafia per carattere.
ms.assetid: 4dacceab-032e-4b9b-858f-67961fd587b5
title: Confronto tra riconoscimento di parole e caratteri
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e704943afb2b411441752056aace0889e87483fc4992d59c39ea6a135ef76b73
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118966600"
---
# <a name="word-vs-character-recognition"></a>Confronto tra riconoscimento di parole e caratteri

Impostando la [proprietà Factoid](/previous-versions/ms835848(v=msdn.10)) su **Nessuno,** il riconoscimento dei caratteri riconosce la grafia per carattere.

La [proprietà RecoTimeout](/previous-versions/ms835852(v=msdn.10)) ([**RecoTimeout**](/windows/desktop/api/inked/nf-inked-iinkedit-get_recognitiontimeout) in Automazione) specifica il numero di millisecondi di ritardo tra l'ultimo [tratto](/previous-versions/ms552692(v=vs.100)) e la fine dell'input per la grafia. È possibile aumentare questo valore per riconoscere il testo prima che intere parole o frasi siano scritte. È anche possibile forzare immediatamente il riconoscimento dell'input penna usando il [metodo Recognize.](/previous-versions/ms836275(v=msdn.10))

 

 
