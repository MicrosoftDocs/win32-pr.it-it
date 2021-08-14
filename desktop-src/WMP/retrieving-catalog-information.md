---
title: Recupero delle informazioni del catalogo
description: Recupero delle informazioni del catalogo
ms.assetid: f2ec795f-6e6f-4c0c-9332-f1e96524221a
keywords:
- Windows Media Player negozi online, recupero di informazioni sul catalogo
- negozi online, recupero di informazioni sul catalogo
- tipo 1 negozi online, recupero di informazioni sul catalogo
- Windows Media Player online, informazioni di diagnostica sui cataloghi
- negozi online, informazioni di diagnostica sui cataloghi
- store online di tipo 1, informazioni di diagnostica sui cataloghi
- Windows Media Player negozi online, catcomp.exe
- negozi online, catcomp.exe
- tipo 1 negozi online, catcomp.exe
- catcomp.exe
- informazioni di diagnostica sui cataloghi
- recupero di informazioni sul catalogo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ae3b28da6d2d5f5143dab0664c10d0c906f971a6a60e4fdb502f4331fa71f408
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118570202"
---
# <a name="retrieving-catalog-information"></a>Recupero delle informazioni del catalogo

È possibile visualizzare informazioni di diagnostica in un catalogo eseguendo catcomp con la sintassi seguente:


```C++
catcomp info <catalogpath> [track|artist|album] [ID]
```



Ad esempio, il comando seguente visualizza informazioni su un intero catalogo, incluse la versione, le impostazioni locali e le informazioni interne sugli elementi del catalogo:


```C++
catcomp info C:\Catalog210\catalog.wmdb
```



Di seguito vengono visualizzate le informazioni per la traccia con ID 3256:


```C++
catcomp info C:\Catalog210\catalog.wmdb track 3256
```



 

 




