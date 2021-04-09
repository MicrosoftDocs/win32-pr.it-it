---
title: Commenti (menu e altre risorse)
description: RC supporta la sintassi di tipo C per i commenti a riga singola e per i commenti del blocco. I commenti a riga singola iniziano con due barre (//) e vengono eseguite fino alla fine della riga. Di seguito è riportato un esempio di istruzione di risorsa seguita da un commento a riga singola.
ms.assetid: 045268fb-2d6e-446c-8b95-90e42baeb282
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a5fda05690df9b7e7fff6974d75d8275a2842b68
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/10/2020
ms.locfileid: "103739626"
---
# <a name="comments-menus-and-other-resources"></a>Commenti (menu e altre risorse)

RC supporta la sintassi di tipo C per i commenti a riga singola e per i commenti del blocco. I commenti a riga singola iniziano con due barre (//) e vengono eseguite fino alla fine della riga. Di seguito è riportato un esempio di istruzione di risorsa seguita da un commento a riga singola.

``` syntax
NewCursor  CURSOR  NEW.CUR  // a new cursor for the application.
```

I commenti dei blocchi iniziano con un delimitatore di apertura (/ \* ) ed eseguono fino a un delimitatore di chiusura ( \* /). I commenti non vengono annidati. Di seguito è riportato un esempio di un commento di blocco all'inizio di un file RC.

``` syntax
/* 
    Resources.Rc

    Contains the resource definitions for the application.
    Control identifiers are defined in Resources.h.
*/

#include "resources.h"
//...
```

 

 




