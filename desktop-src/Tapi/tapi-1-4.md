---
description: TAPI 1,4 ha aggiunto una serie di API, messaggi, costanti ed elementi della struttura alla specifica 1,3.
ms.assetid: 293f732f-0288-46d1-b542-d948c6179158
title: TAPI 1,4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c32f4320043ada2e2ae5477a698bde63f28d2f25
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103967461"
---
# <a name="tapi-14"></a>TAPI 1,4

TAPI 1,4 ha aggiunto una serie di API, messaggi, costanti ed elementi della struttura alla specifica 1,3. TAPI 1,4 supporta solo TSPs a 16 bit. Tuttavia, consente di sviluppare applicazioni a 32 bit senza doversi preoccupare delle limitazioni di Windows a 16 bit.

I file di intestazione TAPI e TSPI vengono usati per sviluppare entrambe le applicazioni sia per TAPI 1,4 che per TAPI 2. x. Sebbene non siano state apportate numerose modifiche alle strutture tra queste due specifiche, sono state apportate modifiche all'API, in particolare al supporto Unicode, che rendono molto importante notare che le intestazioni vengono compilate in modo diverso, a seconda della \_ costante della versione corrente di TAPI \_ . Ad esempio:

``` syntax
#define TAPI_CURRENT_VERSION 0x00010004
#include <tapi.h>
```

> [!Note]  
> \_ \_ Per tutte le applicazioni TAPI è necessario definire la versione corrente di TAPI. Sebbene non sia strettamente necessario per lo sviluppo di TAPI 2. x, potrebbero verificarsi modifiche future per richiederlo.

 

 

 



