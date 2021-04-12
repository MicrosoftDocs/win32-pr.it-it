---
title: Definizione dei nomi per il preprocessore
description: È possibile specificare la compilazione condizionale in uno script, a seconda che un nome venga definito nella riga di comando RC con l'opzione/d oppure nel file o in un file di inclusione con la direttiva \ define.
ms.assetid: bc72911e-2aca-46a4-b6c1-60cc8ed7d82f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e64b339959ace5a70d83fa8ee8beb615f1bc5ce4
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104328772"
---
# <a name="defining-names-for-the-preprocessor"></a>Definizione dei nomi per il preprocessore

È possibile specificare la compilazione condizionale in uno script, a seconda che un nome venga definito nella riga di comando RC con l'opzione **/d** oppure nel file o in un file di inclusione con la direttiva [**\# define**](-define.md) .

Si supponga, ad esempio, che l'applicazione disponga di un menu a comparsa che dovrebbe essere visualizzato solo con le versioni di debug dell'applicazione. Quando si compila l'applicazione per l'uso normale, il menu non è incluso. Nell'esempio seguente vengono illustrate le istruzioni che possono essere aggiunte al file di definizione delle risorse per definire un menu debug:

``` syntax
#include <windows.h>

MainMenu MENU
{
    //. . .
#ifdef DEBUG
    POPUP "&Debug"
    {
        MENUITEM "&Memory usage", ID_MEMORY
        MENUITEM "&Walk data heap", ID_WALK_HEAP
    }
#endif
}
```

Quando si compilano risorse per una versione di debug dell'applicazione, è possibile includere il menu debug usando il comando seguente:

**DEBUG RC-d: MyApp. RC**

Per compilare le risorse per una versione normale dell'applicazione? una che non include il menu debug? è possibile usare il comando seguente:

**RC MyApp. RC**

 

 




