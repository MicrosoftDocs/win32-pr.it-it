---
title: Definizione dei nomi per il preprocessore
description: È possibile specificare la compilazione condizionale in uno script, a seconda che un nome sia definito nella riga di comando RC con l'opzione /d o nel file o in un file di inclusione con la direttiva \ define.
ms.assetid: bc72911e-2aca-46a4-b6c1-60cc8ed7d82f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f3bcf9c02b5a4da4487b0c82de8d8b0223662cb30f9529e82204fc66a3de91cc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118972110"
---
# <a name="defining-names-for-the-preprocessor"></a>Definizione dei nomi per il preprocessore

È possibile specificare la compilazione condizionale in uno script, a seconda che un nome sia definito nella riga di comando RC con l'opzione **/d** o nel file o in un file di inclusione con la direttiva [**\# define.**](-define.md)

Si supponga, ad esempio, che l'applicazione abbia un menu a comparsa che deve essere visualizzato solo con le versioni di debug dell'applicazione. Quando si compila l'applicazione per un uso normale, il menu non è incluso. Nell'esempio seguente vengono illustrate le istruzioni che è possibile aggiungere al file di definizione delle risorse per definire un menu Debug:

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

Quando si compilano risorse per una versione di debug dell'applicazione, è possibile includere il menu Debug usando il comando seguente:

**rc -d DEBUG myapp.rc**

Per compilare le risorse per una versione normale dell'applicazione? una che non include il menu Debug? è possibile usare il comando seguente:

**rc myapp.rc**

 

 




