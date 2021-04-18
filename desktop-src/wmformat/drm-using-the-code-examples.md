---
title: Uso degli esempi di codice client DRM di Microsoft Windows Media
description: Uso degli esempi di codice client DRM di Microsoft Windows Media
ms.assetid: 75db2663-9eb8-406d-b1a9-8f6092c95f9d
keywords:
- Windows Media Format SDK, esempi di codice
- Windows Media Format SDK, esempio di codice
- Windows Media Format SDK, esempi di codice DRM
- Digital Rights Management (DRM), esempi di codice
- DRM (Digital Rights Management), esempi di codice
- Digital Rights Management (DRM), codice di esempio
- DRM (Digital Rights Management), codice di esempio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 054d1ed804873c8aca104203ee1f235ecb3856f5
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/10/2020
ms.locfileid: "104400067"
---
# <a name="using-the-microsoft-windows-media-drm-client-code-examples"></a><span data-ttu-id="7ae49-110">Uso degli esempi di codice client DRM di Microsoft Windows Media</span><span class="sxs-lookup"><span data-stu-id="7ae49-110">Using the Microsoft Windows Media DRM Client Code Examples</span></span>

<span data-ttu-id="7ae49-111">Gli esempi di codice sono inclusi in questa documentazione per illustrare l'utilizzo dei componenti di.</span><span class="sxs-lookup"><span data-stu-id="7ae49-111">Code examples are included in this documentation to illustrate the use of components.</span></span> <span data-ttu-id="7ae49-112">Gli esempi sono scritti nel modo più chiaro e conciso possibile.</span><span class="sxs-lookup"><span data-stu-id="7ae49-112">The examples are written to be as clear and concise as possible.</span></span> <span data-ttu-id="7ae49-113">Quando si leggono gli esempi, è necessario tenere presente le convenzioni seguenti.</span><span class="sxs-lookup"><span data-stu-id="7ae49-113">When reading the examples, you should be aware of the following conventions.</span></span>

-   <span data-ttu-id="7ae49-114">Si presuppone che tutti gli esempi includano Windows. h e wmdrmsdk. h.</span><span class="sxs-lookup"><span data-stu-id="7ae49-114">All examples are assumed to include windows.h and wmdrmsdk.h.</span></span> <span data-ttu-id="7ae49-115">Nell'esempio sarà inclusa una nota se sono necessarie altre intestazioni per la compilazione.</span><span class="sxs-lookup"><span data-stu-id="7ae49-115">The example will include a note if it requires other headers in order to compile.</span></span>
-   <span data-ttu-id="7ae49-116">Se si verifica un errore, il controllo degli errori è stato limitato alla suddivisione della funzione.</span><span class="sxs-lookup"><span data-stu-id="7ae49-116">Error checking has been restricted to breaking out of the function if an error occurs.</span></span> <span data-ttu-id="7ae49-117">In un'applicazione, è necessario verificare la presenza di codici di errore specifici e fornire un tipo di segnalazione degli errori.</span><span class="sxs-lookup"><span data-stu-id="7ae49-117">In an application, you should check for specific error codes and provide some kind of error reporting.</span></span>
-   <span data-ttu-id="7ae49-118">Le interfacce e la memoria vengono rilasciate negli esempi di codice che usano le macro denominate SAFE \_ release e Safe \_ array \_ Delete.</span><span class="sxs-lookup"><span data-stu-id="7ae49-118">Interfaces and memory are released in the code examples using macros named SAFE\_RELEASE and SAFE\_ARRAY\_DELETE.</span></span> <span data-ttu-id="7ae49-119">Queste macro sono definite nel codice seguente:</span><span class="sxs-lookup"><span data-stu-id="7ae49-119">These macros are defined in the following code:</span></span>
    ```C++
    #ifndef SAFE_RELEASE
    #define SAFE_RELEASE(x) \
       if(x != NULL)        \
       {                    \
          x->Release();     \
          x = NULL;         \
       }
    #endif

    #ifndef SAFE_ARRAY_DELETE
    #define SAFE_ARRAY_DELETE(x) \
       if(x != NULL)             \
       {                         \
          delete[] x;            \
          x = NULL;              \
       }
    #endif
    ```

    

## <a name="related-topics"></a><span data-ttu-id="7ae49-120">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="7ae49-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7ae49-121">**Introduzione**</span><span class="sxs-lookup"><span data-stu-id="7ae49-121">**Getting Started**</span></span>](drm-getting-started.md)
</dt> </dl>

 

 




