---
description: Impostando la proprietà del controllo del controllo su None, il riconoscimento di caratteri riconosce la grafia in base a caratteri.
ms.assetid: 4dacceab-032e-4b9b-858f-67961fd587b5
title: Riconoscimento di parole e caratteri
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f521b8abf1064ef87c5c79c3293e725c44190ce3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104128990"
---
# <a name="word-vs-character-recognition"></a>Riconoscimento di parole e caratteri

Impostando la [proprietà del controllo del controllo](/previous-versions/ms835848(v=msdn.10)) su **None**, il riconoscimento di caratteri riconosce la grafia in base a caratteri.

La proprietà [RecoTimeout](/previous-versions/ms835852(v=msdn.10)) ([**RecoTimeout**](/windows/desktop/api/inked/nf-inked-iinkedit-get_recognitiontimeout) in Automation) specifica il numero di millisecondi di ritardo tra l'ultimo [tratto](/previous-versions/ms552692(v=vs.100)) e la fine dell'input della grafia. È possibile aumentare questo valore per riconoscere il testo prima che vengano scritte intere parole o frasi. È anche possibile forzare il riconoscimento immediato dell'input penna usando il metodo [Recognize](/previous-versions/ms836275(v=msdn.10)) .

 

 
