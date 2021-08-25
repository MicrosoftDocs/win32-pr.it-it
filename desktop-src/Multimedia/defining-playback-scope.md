---
title: Definizione dell'ambito di riproduzione
description: Definizione dell'ambito di riproduzione
ms.assetid: f2563226-7af1-4cb3-b468-c59738feeda2
keywords:
- Macro MCIWndPlayFrom
- Macro MCIWndPlayTo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1853c74cc4115cee72e4253e339f934e73b8d8e7e223f1b91e9992969c4ce3f6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119785421"
---
# <a name="defining-playback-scope"></a>Definizione dell'ambito di riproduzione

MCIWnd fornisce macro che consentono di definire l'ambito di *riproduzione*. L'ambito è la parte della riproduzione che si vuole riprodurre. Ad esempio, puoi riprodurre il contenuto da una posizione diversa da quella iniziale usando la macro [**MCIWndPlayFrom.**](/windows/desktop/api/Vfw/nf-vfw-mciwndplayfrom) Questa macro si sposta nella posizione specificata, avvia la riproduzione e continua fino alla fine del contenuto. Analogamente, puoi riprodurre il contenuto fino a un punto finale specificato usando la macro [**MCIWndPlayTo.**](/windows/desktop/api/Vfw/nf-vfw-mciwndplayto) Questa macro inizia dalla posizione di riproduzione corrente e viene riprodotta fino a raggiungere la posizione specificata o fino a raggiungere la fine del contenuto, a seconda del valore che viene raggiunto per primo.

Puoi anche definire sia la posizione iniziale che la posizione finale usando la macro [**MCIWndPlayFromTo.**](/windows/desktop/api/Vfw/nf-vfw-mciwndplayfromto) Questa macro si sposta nella posizione iniziale specificata e viene riprodotta fino a raggiungere la posizione finale specificata o la fine del contenuto.

 

 




