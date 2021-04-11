---
title: Inversione della riproduzione
description: Inversione della riproduzione
ms.assetid: cb7c1293-42d7-4c74-b9e6-cc8899ca7c54
keywords:
- MCIWndPlayReverse (macro)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a708915679f75bfe478c160d71d35b0bcfa48a23
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104395914"
---
# <a name="reversing-playback"></a>Inversione della riproduzione

Alcuni dispositivi supportano la riproduzione in direzione inversa. È possibile riprodurre il contenuto di un dispositivo di questo tipo in direzione inversa usando la macro [**MCIWndPlayReverse**](/windows/desktop/api/Vfw/nf-vfw-mciwndplayreverse) . Questa macro definisce l'ambito di riproduzione dalla posizione corrente fino all'inizio del contenuto. Il dispositivo Digital-video, MCIAVI. DRV, può riprodurre le versioni precedenti. Quando viene richiamato **MCIWndPlayReverse** , i dispositivi che non possono riprodurre versioni precedenti, ad esempio audio CD, possono generare un messaggio di errore.

 

 




