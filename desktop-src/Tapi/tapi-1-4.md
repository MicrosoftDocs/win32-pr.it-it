---
description: TAPI 1.4 ha aggiunto una serie di API, messaggi, costanti ed elementi di struttura alla specifica 1.3.
ms.assetid: 293f732f-0288-46d1-b542-d948c6179158
title: TAPI 1.4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 50f22833639813268420cc1ea202ef260964b42ce2e5119fafc8d0aa18593686
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119060359"
---
# <a name="tapi-14"></a>TAPI 1.4

TAPI 1.4 ha aggiunto una serie di API, messaggi, costanti ed elementi di struttura alla specifica 1.3. TAPI 1.4 supporta solo TSP a 16 bit. Tuttavia, consente lo sviluppo di applicazioni a 32 bit senza doversi preoccupare delle limitazioni delle applicazioni a 16 bit Windows.

I file di intestazione TAPI e TSPI vengono usati per sviluppare entrambe le applicazioni per TAPI 1.4 e TAPI 2.x. Anche se non sono state apportate molte modifiche alle strutture tra queste due specifiche, sono state apportate modifiche all'API (in particolare, il supporto Unicode) che rendono molto importante notare che le intestazioni vengono compilate in modo diverso, a seconda della costante \_ TAPI CURRENT \_ VERSION. Esempio:

``` syntax
#define TAPI_CURRENT_VERSION 0x00010004
#include <tapi.h>
```

> [!Note]  
> È necessario \_ definire TAPI CURRENT \_ VERSION per tutte le applicazioni TAPI. Anche se non è strettamente necessario per lo sviluppo TAPI 2.x, potrebbero essere necessarie modifiche future.

 

 

 



