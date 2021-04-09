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
# <a name="word-vs-character-recognition"></a><span data-ttu-id="a3a4e-103">Riconoscimento di parole e caratteri</span><span class="sxs-lookup"><span data-stu-id="a3a4e-103">Word vs. Character Recognition</span></span>

<span data-ttu-id="a3a4e-104">Impostando la [proprietà del controllo del controllo](/previous-versions/ms835848(v=msdn.10)) su **None**, il riconoscimento di caratteri riconosce la grafia in base a caratteri.</span><span class="sxs-lookup"><span data-stu-id="a3a4e-104">By setting the [Factoid](/previous-versions/ms835848(v=msdn.10)) property to **None**, the character recognizer recognizes handwriting on a character-by-character basis.</span></span>

<span data-ttu-id="a3a4e-105">La proprietà [RecoTimeout](/previous-versions/ms835852(v=msdn.10)) ([**RecoTimeout**](/windows/desktop/api/inked/nf-inked-iinkedit-get_recognitiontimeout) in Automation) specifica il numero di millisecondi di ritardo tra l'ultimo [tratto](/previous-versions/ms552692(v=vs.100)) e la fine dell'input della grafia.</span><span class="sxs-lookup"><span data-stu-id="a3a4e-105">The [RecoTimeout](/previous-versions/ms835852(v=msdn.10)) ([**RecoTimeout**](/windows/desktop/api/inked/nf-inked-iinkedit-get_recognitiontimeout) in Automation) property specifies the number of milliseconds of delay between the last [Stroke](/previous-versions/ms552692(v=vs.100)) and the end of handwriting input.</span></span> <span data-ttu-id="a3a4e-106">È possibile aumentare questo valore per riconoscere il testo prima che vengano scritte intere parole o frasi.</span><span class="sxs-lookup"><span data-stu-id="a3a4e-106">You can increase this value to recognize text before entire words or sentences are written.</span></span> <span data-ttu-id="a3a4e-107">È anche possibile forzare il riconoscimento immediato dell'input penna usando il metodo [Recognize](/previous-versions/ms836275(v=msdn.10)) .</span><span class="sxs-lookup"><span data-stu-id="a3a4e-107">You can also force the recognition of ink immediately by using the [Recognize](/previous-versions/ms836275(v=msdn.10)) method.</span></span>

 

 
