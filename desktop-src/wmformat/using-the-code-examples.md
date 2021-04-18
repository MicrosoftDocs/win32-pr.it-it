---
title: Uso degli esempi di codice di Windows Media Format SDK
description: Uso degli esempi di codice di Windows Media Format SDK
ms.assetid: 1459a438-d42c-4d84-baa8-fc672f5d5d27
keywords:
- Windows Media Format SDK, esempi di codice
- Windows Media Format SDK, esempio di codice
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8db438a8cb42bbb45768421cc34c129f19948f1c
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/10/2020
ms.locfileid: "104400187"
---
# <a name="using-the-windows-media-format-sdk-code-examples"></a><span data-ttu-id="e045d-105">Uso degli esempi di codice di Windows Media Format SDK</span><span class="sxs-lookup"><span data-stu-id="e045d-105">Using the Windows Media Format SDK Code Examples</span></span>

<span data-ttu-id="e045d-106">Molte delle sezioni esplicative di questo SDK includono esempi di codice.</span><span class="sxs-lookup"><span data-stu-id="e045d-106">Many of the explanatory sections of this SDK include code examples.</span></span> <span data-ttu-id="e045d-107">Gli esempi sono scritti nel modo più chiaro e conciso possibile.</span><span class="sxs-lookup"><span data-stu-id="e045d-107">The examples are written to be as clear and concise as possible.</span></span> <span data-ttu-id="e045d-108">Quando si leggono gli esempi, è necessario tenere presente le convenzioni seguenti.</span><span class="sxs-lookup"><span data-stu-id="e045d-108">When reading the examples, you should be aware of the following conventions.</span></span>

-   <span data-ttu-id="e045d-109">Si presuppone che tutti gli esempi includano Windows. h e WMSDK. h.</span><span class="sxs-lookup"><span data-stu-id="e045d-109">All examples are assumed to include windows.h and wmsdk.h.</span></span> <span data-ttu-id="e045d-110">Tutti gli altri file di intestazione obbligatori sono indicati nel testo esplicativo.</span><span class="sxs-lookup"><span data-stu-id="e045d-110">Any other required header files are mentioned in the explanatory text.</span></span>
-   <span data-ttu-id="e045d-111">Se si verifica un errore, il controllo degli errori è stato limitato alla suddivisione della funzione.</span><span class="sxs-lookup"><span data-stu-id="e045d-111">Error checking has been restricted to breaking out of the function if an error occurs.</span></span> <span data-ttu-id="e045d-112">In un'applicazione, è necessario verificare la presenza di codici di errore specifici e fornire un tipo di segnalazione degli errori.</span><span class="sxs-lookup"><span data-stu-id="e045d-112">In an application, you should check for specific error codes and provide some kind of error reporting.</span></span>

    <span data-ttu-id="e045d-113">Quando si controllano i valori restituiti dai metodi o dalle funzioni che restituiscono un valore **HRESULT** , è necessario usare la macro **failed** per individuare se il valore restituito indica un errore.</span><span class="sxs-lookup"><span data-stu-id="e045d-113">When checking return values from methods or functions that return an **HRESULT** value, you should use the **FAILED** macro to discover whether the return value indicates failure.</span></span>

    ```C++
    HRESULT hr;
    hr = SomeFunction();
    if (FAILED(hr))
    {
       // Check for specific error values.
    }
    ```

    

    <span data-ttu-id="e045d-114">Molti degli esempi in questa documentazione usano una macro denominata GOTO \_ Exit \_ se \_ failed, definita nel codice seguente.</span><span class="sxs-lookup"><span data-stu-id="e045d-114">Many of the examples in this documentation use a macro named GOTO\_EXIT\_IF\_FAILED, which is defined in the following code.</span></span>

    ```C++
    #ifndef GOTO_EXIT_IF_FAILED
    #define GOTO_EXIT_IF_FAILED(hr) if(FAILED(hr)) goto Exit;
    #endif
    ```

    

    <span data-ttu-id="e045d-115">Ognuna di queste funzioni di esempio ha un tag denominato "Exit:", dopo il quale vengono rilasciate tutte le interfacce e la memoria allocata nella funzione e viene restituito il codice di errore, se disponibile.</span><span class="sxs-lookup"><span data-stu-id="e045d-115">These example functions each have a tag named "Exit:", after which all interfaces and memory allocated in the function are released and the error code, if any, is returned.</span></span>

-   <span data-ttu-id="e045d-116">Le interfacce e la memoria vengono rilasciate negli esempi di codice che usano le macro denominate SAFE \_ release e Safe \_ array \_ Delete.</span><span class="sxs-lookup"><span data-stu-id="e045d-116">Interfaces and memory are released in the code examples using macros named SAFE\_RELEASE and SAFE\_ARRAY\_DELETE.</span></span> <span data-ttu-id="e045d-117">Queste macro sono definite nel codice seguente:</span><span class="sxs-lookup"><span data-stu-id="e045d-117">These macros are defined in the following code:</span></span>
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

    

-   <span data-ttu-id="e045d-118">Spesso è necessario includere la logica di un esempio in un altro esempio perché l'esempio sia significativo.</span><span class="sxs-lookup"><span data-stu-id="e045d-118">Often, you will need to include the logic of one example in another example for the example to be meaningful.</span></span> <span data-ttu-id="e045d-119">In tali casi, viene incluso un commento TODO con un riferimento all'esempio di codice appropriato.</span><span class="sxs-lookup"><span data-stu-id="e045d-119">In those instances, a TODO comment is included, with a reference to the appropriate code example.</span></span>
-   <span data-ttu-id="e045d-120">Per semplificare la lettura del codice, nessuna delle funzioni di esempio in questa documentazione convalida i relativi parametri di input.</span><span class="sxs-lookup"><span data-stu-id="e045d-120">To make the code easier to read, none of the example functions in this documentation validate their input parameters.</span></span> <span data-ttu-id="e045d-121">Se si copia una di queste funzioni nel codice, è necessario convalidare i parametri di input.</span><span class="sxs-lookup"><span data-stu-id="e045d-121">If you copy any of these functions into your code, you should validate any input parameters.</span></span>

## <a name="related-topics"></a><span data-ttu-id="e045d-122">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="e045d-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e045d-123">**Introduzione**</span><span class="sxs-lookup"><span data-stu-id="e045d-123">**Getting Started**</span></span>](getting-started.md)
</dt> </dl>

 

 




