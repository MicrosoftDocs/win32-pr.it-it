---
description: Le espressioni sono istruzioni matematiche o logiche che vengono usate sul lato destro di un segno di uguale. Sono disponibili molti tipi di espressioni.
ms.assetid: 642aa188-5dd7-49fc-b6cc-845f8fc22530
title: Espressioni (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3aa574069094853eb506f7a1b38cdb6cd4379d3b
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "106303726"
---
# <a name="expressions-direct3d-9"></a><span data-ttu-id="f60d0-104">Espressioni (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="f60d0-104">Expressions (Direct3D 9)</span></span>

<span data-ttu-id="f60d0-105">Le espressioni sono istruzioni matematiche o logiche che vengono usate sul lato destro di un segno di uguale.</span><span class="sxs-lookup"><span data-stu-id="f60d0-105">Expressions are mathematical or logical statements that are used on the right hand side of an equals sign.</span></span> <span data-ttu-id="f60d0-106">Sono disponibili molti tipi di espressioni.</span><span class="sxs-lookup"><span data-stu-id="f60d0-106">There are many types of expressions.</span></span>

## <a name="expressions"></a><span data-ttu-id="f60d0-107">Espressioni</span><span class="sxs-lookup"><span data-stu-id="f60d0-107">Expressions</span></span>

1.  <span data-ttu-id="f60d0-108">Riferimento a una variabile</span><span class="sxs-lookup"><span data-stu-id="f60d0-108">Variable Reference</span></span>
    ```
    ( variable ) or<variable >
    ```

    

2.  <span data-ttu-id="f60d0-109">Scalare numerico</span><span class="sxs-lookup"><span data-stu-id="f60d0-109">Numeric Scalar</span></span>
    ```
    scalar 
    ```

    

3.  <span data-ttu-id="f60d0-110">Espressione numerica</span><span class="sxs-lookup"><span data-stu-id="f60d0-110">Numeric Expression</span></span>

    ```
    ( numeric expression )
    ```

    

    <span data-ttu-id="f60d0-111">Qui sono supportate tutte le espressioni HLL numeriche standard.</span><span class="sxs-lookup"><span data-stu-id="f60d0-111">All standard numeric HLL expressions are supported here.</span></span>

4.  <span data-ttu-id="f60d0-112">Costruttore</span><span class="sxs-lookup"><span data-stu-id="f60d0-112">Constructor</span></span>
    ```
    type ( constructor arguments )
    ```

    

5.  <span data-ttu-id="f60d0-113">Elenco di inizializzatori</span><span class="sxs-lookup"><span data-stu-id="f60d0-113">List of Initializers</span></span>

    ```
    { scalar value [, scalar value ...  ] }
    
    ```

    

    <span data-ttu-id="f60d0-114">I valori scalari devono essere valori scalari letterali.</span><span class="sxs-lookup"><span data-stu-id="f60d0-114">The scalars must be literal scalar values.</span></span>

    <span data-ttu-id="f60d0-115">Il numero di inizializzatori deve essere compatibile con la variabile (stato) sul lato sinistro del segno di uguale.</span><span class="sxs-lookup"><span data-stu-id="f60d0-115">The number of initializers must be compatible with the variable (state) on the left hand side of the equals sign.</span></span>

6.  <span data-ttu-id="f60d0-116">Espressione OR</span><span class="sxs-lookup"><span data-stu-id="f60d0-116">OR Expression</span></span>

    ```
    token [ | token ... ]
    ```

    

    <span data-ttu-id="f60d0-117">I token devono essere compatibili con la variabile (stato) sul lato sinistro del segno di uguale.</span><span class="sxs-lookup"><span data-stu-id="f60d0-117">The tokens must be compatible with the variable (state) on the left hand side of the equals sign.</span></span>

    <span data-ttu-id="f60d0-118">I token non fanno distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="f60d0-118">The tokens are not case sensitive.</span></span>

7.  <span data-ttu-id="f60d0-119">NULL</span><span class="sxs-lookup"><span data-stu-id="f60d0-119">NULL</span></span>

    ```
    NULL
    ```

    

    <span data-ttu-id="f60d0-120">NULL può essere assegnato solo a uno shader, un campionatore o un oggetto trama.</span><span class="sxs-lookup"><span data-stu-id="f60d0-120">NULL can only be assigned to a shader, sampler, or a texture object.</span></span>

8.  <span data-ttu-id="f60d0-121">Blocco assembly</span><span class="sxs-lookup"><span data-stu-id="f60d0-121">Assembly Block</span></span>

    ```
    asm { code }
    ```

    

    <span data-ttu-id="f60d0-122">È necessario assegnare i blocchi di assembly PS allo stato PIXELSHADER.</span><span class="sxs-lookup"><span data-stu-id="f60d0-122">PS Assembly Blocks must be assigned to the PIXELSHADER state.</span></span>

    <span data-ttu-id="f60d0-123">I blocchi di assembly di Visual Studio devono essere assegnati allo stato VERTEXSHADER.</span><span class="sxs-lookup"><span data-stu-id="f60d0-123">VS Assembly Blocks must be assigned to the VERTEXSHADER state.</span></span>

9.  <span data-ttu-id="f60d0-124">Blocco dello stato del campionatore</span><span class="sxs-lookup"><span data-stu-id="f60d0-124">Sampler State Block</span></span>

    ```
    sampler_state { [ state = expression ; [ state = ... ] ] }
    ```

    

    <span data-ttu-id="f60d0-125">I blocchi di stato del campionatore sono sequenze di assegnazioni di trame o stato della fase del campionatore non indicizzato.</span><span class="sxs-lookup"><span data-stu-id="f60d0-125">Sampler state blocks are sequences of un-indexed sampler stage state or texture assignments.</span></span>

    <span data-ttu-id="f60d0-126">I blocchi di stato del campionatore devono essere assegnati allo stato dell'effetto CAMPIONATOre.</span><span class="sxs-lookup"><span data-stu-id="f60d0-126">Sampler state blocks must be assigned to the SAMPLER effect state.</span></span>

10. <span data-ttu-id="f60d0-127">Blocco dello stato di stato dell'effetto</span><span class="sxs-lookup"><span data-stu-id="f60d0-127">Effect State State Block</span></span>

    ```
    stateblock_state { [ state [ [index] ] = expression; 
        [ state [ [index] ] = ... ] ] }
    ```

    

    <span data-ttu-id="f60d0-128">I blocchi di stato sono sequenze di stato generale.</span><span class="sxs-lookup"><span data-stu-id="f60d0-128">State blocks are sequences of general state.</span></span> <span data-ttu-id="f60d0-129">I blocchi di stato possono essere annidati, ma non possono contenere riferimenti circolari.</span><span class="sxs-lookup"><span data-stu-id="f60d0-129">State blocks can be nested, but cannot contain circular references.</span></span>

    <span data-ttu-id="f60d0-130">I blocchi di stato devono essere assegnati allo stato dell'effetto STATEBLOCK.</span><span class="sxs-lookup"><span data-stu-id="f60d0-130">State blocks must be assigned to the STATEBLOCK effect state.</span></span>

11. <span data-ttu-id="f60d0-131">Compilazione HLSL</span><span class="sxs-lookup"><span data-stu-id="f60d0-131">HLSL Compile</span></span>

    ```
    compile target entrypoint ( [ arguments ] )
    ```

    

    <span data-ttu-id="f60d0-132">La destinazione vertex shader \_ e m \_ n indica D3DVS \_ versione (m, n) vertex shader Version.</span><span class="sxs-lookup"><span data-stu-id="f60d0-132">The vertex shader vs\_m\_n target indicates D3DVS\_VERSION(m, n) vertex shader version.</span></span> <span data-ttu-id="f60d0-133">La destinazione pixel shader PS m n indica che la versione di \_ \_ D3DPS \_ (m, n) pixel shader.</span><span class="sxs-lookup"><span data-stu-id="f60d0-133">The pixel shader ps\_m\_n target indicates D3DPS\_VERSION(m, n) pixel shader version.</span></span>

    <span data-ttu-id="f60d0-134">Le espressioni di compilazione del linguaggio di alto livello del vertex shader possono essere assegnate solo allo stato dell'effetto VERTEXSHADER.</span><span class="sxs-lookup"><span data-stu-id="f60d0-134">Vertex shader high-level language compile expressions can only be assigned to the VERTEXSHADER effect state.</span></span> <span data-ttu-id="f60d0-135">Le espressioni di compilazione del linguaggio di alto livello del pixel shader possono essere assegnate solo allo stato dell'effetto PIXELSHADER.</span><span class="sxs-lookup"><span data-stu-id="f60d0-135">Pixel shader high-level language compile expressions can only be assigned to the PIXELSHADER effect state.</span></span>

## <a name="related-topics"></a><span data-ttu-id="f60d0-136">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="f60d0-136">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f60d0-137">Formato effetto</span><span class="sxs-lookup"><span data-stu-id="f60d0-137">Effect Format</span></span>](dx9-graphics-reference-effects-file-format.md)
</dt> </dl>

 

 



