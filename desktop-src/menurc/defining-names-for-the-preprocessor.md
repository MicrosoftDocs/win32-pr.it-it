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
# <a name="defining-names-for-the-preprocessor"></a><span data-ttu-id="757f4-103">Definizione dei nomi per il preprocessore</span><span class="sxs-lookup"><span data-stu-id="757f4-103">Defining Names for the Preprocessor</span></span>

<span data-ttu-id="757f4-104">È possibile specificare la compilazione condizionale in uno script, a seconda che un nome venga definito nella riga di comando RC con l'opzione **/d** oppure nel file o in un file di inclusione con la direttiva [**\# define**](-define.md) .</span><span class="sxs-lookup"><span data-stu-id="757f4-104">You can specify conditional compilation in a script, based on whether a name is defined on the RC command line with the **/d** option, or in the file or an include file with the [**\#define**](-define.md) directive.</span></span>

<span data-ttu-id="757f4-105">Si supponga, ad esempio, che l'applicazione disponga di un menu a comparsa che dovrebbe essere visualizzato solo con le versioni di debug dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="757f4-105">For example, suppose your application has a pop-up menu that should appear only with debugging versions of the application.</span></span> <span data-ttu-id="757f4-106">Quando si compila l'applicazione per l'uso normale, il menu non è incluso.</span><span class="sxs-lookup"><span data-stu-id="757f4-106">When you compile the application for normal use, the menu is not included.</span></span> <span data-ttu-id="757f4-107">Nell'esempio seguente vengono illustrate le istruzioni che possono essere aggiunte al file di definizione delle risorse per definire un menu debug:</span><span class="sxs-lookup"><span data-stu-id="757f4-107">The following example shows the statements that can be added to the resource-definition file to define a Debug menu:</span></span>

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

<span data-ttu-id="757f4-108">Quando si compilano risorse per una versione di debug dell'applicazione, è possibile includere il menu debug usando il comando seguente:</span><span class="sxs-lookup"><span data-stu-id="757f4-108">When compiling resources for a debugging version of the application, you could include the Debug menu by using the following command:</span></span>

<span data-ttu-id="757f4-109">**DEBUG RC-d: MyApp. RC**</span><span class="sxs-lookup"><span data-stu-id="757f4-109">**rc -d DEBUG myapp.rc**</span></span>

<span data-ttu-id="757f4-110">Per compilare le risorse per una versione normale dell'applicazione? una che non include il menu debug? è possibile usare il comando seguente:</span><span class="sxs-lookup"><span data-stu-id="757f4-110">To compile resources for a normal version of the application?one that does not include the Debug menu?you could use the following command:</span></span>

<span data-ttu-id="757f4-111">**RC MyApp. RC**</span><span class="sxs-lookup"><span data-stu-id="757f4-111">**rc myapp.rc**</span></span>

 

 




