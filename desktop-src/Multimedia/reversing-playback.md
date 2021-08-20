---
title: Inverti riproduzione
description: Inverti riproduzione
ms.assetid: cb7c1293-42d7-4c74-b9e6-cc8899ca7c54
keywords:
- Macro MCIWndPlayReverse
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 19e6a951c1dc89ab340883b8447c2e580703d24979a1fbf8f1ce28c4a9f2632c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117801795"
---
# <a name="reversing-playback"></a>Inverti riproduzione

Alcuni dispositivi supportano la riproduzione nella direzione inversa. Puoi riprodurre il contenuto di un dispositivo di questo tipo nella direzione inversa usando la macro [**MCIWndPlayReverse.**](/windows/desktop/api/Vfw/nf-vfw-mciwndplayreverse) Questa macro definisce l'ambito di riproduzione dalla posizione di riproduzione corrente all'inizio del contenuto. Il dispositivo video digitale, MCIAVI. DRV, può essere riprodotto all'indietro. I dispositivi che non possono riprodurre all'indietro, ad esempio l'audio CD, possono inviare un messaggio di errore quando viene richiamato **MCIWndPlayReverse.**

 

 




