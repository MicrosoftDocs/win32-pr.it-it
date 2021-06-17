---
description: Informazioni sul rendering di un effetto per Direct3D 10. Un effetto può essere usato per archiviare le informazioni o per eseguire il rendering usando un gruppo di stato.
ms.assetid: c5654335-ad80-4a5b-bf1f-5f32b2cc8ea2
title: Rendering di un effetto (Direct3D 10)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 79db595585c6587648fba12afa5fbb22ff33e845
ms.sourcegitcommit: d0eb44d0a95f5e5efbfec3d3e9c143f5cba25bc3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/17/2021
ms.locfileid: "112262573"
---
# <a name="rendering-an-effect-direct3d-10"></a><span data-ttu-id="8fa5e-104">Rendering di un effetto (Direct3D 10)</span><span class="sxs-lookup"><span data-stu-id="8fa5e-104">Rendering an Effect (Direct3D 10)</span></span>

<span data-ttu-id="8fa5e-105">Un effetto può essere usato per archiviare le informazioni o per eseguire il rendering usando un gruppo di stato.</span><span class="sxs-lookup"><span data-stu-id="8fa5e-105">An effect can be used to store information, or to render using a group of state.</span></span> <span data-ttu-id="8fa5e-106">Ogni tecnica specifica vertex shader, geometry shader, pixel shader, stato dello shader, stato del campionatore e della trama e altro stato della pipeline.</span><span class="sxs-lookup"><span data-stu-id="8fa5e-106">Each technique specifies vertex shaders, geometry shaders, pixel shaders, shader state, sampler and texture state and other pipeline state.</span></span> <span data-ttu-id="8fa5e-107">Quindi, dopo aver organizzato lo stato in un effetto, è possibile incapsulare l'effetto di rendering che risulta da tale stato creando ed esegue il rendering dell'effetto.</span><span class="sxs-lookup"><span data-stu-id="8fa5e-107">So once you have organized state into an effect, you can encapsulate the rendering effect that results from that state by creating and rendering the effect.</span></span>

<span data-ttu-id="8fa5e-108">Esistono alcuni passaggi per preparare un effetto per il rendering.</span><span class="sxs-lookup"><span data-stu-id="8fa5e-108">There are a few steps for preparing an effect for rendering.</span></span> <span data-ttu-id="8fa5e-109">Il primo è la compilazione, che controlla il codice simile a HLSL rispetto alla sintassi del linguaggio HLSL e alle regole del framework degli effetti.</span><span class="sxs-lookup"><span data-stu-id="8fa5e-109">The first is compiling, which checks the HLSL like code against the HLSL language syntax and the effect framework rules.</span></span> <span data-ttu-id="8fa5e-110">È possibile compilare un effetto dall'applicazione usando le chiamate API oppure è possibile compilare un effetto offline usando l'utilità del compilatore di effetti.</span><span class="sxs-lookup"><span data-stu-id="8fa5e-110">You can compile an effect from your application using API calls or you can compile an effect offline using the effect compiler utility.</span></span> <span data-ttu-id="8fa5e-111">Dopo aver compilato correttamente l'effetto, crearlo chiamando un set di API diverso (ma molto simile).</span><span class="sxs-lookup"><span data-stu-id="8fa5e-111">Once your effect has successfully compiled, create it by calling a different (but very similar) set of APIs.</span></span>

<span data-ttu-id="8fa5e-112">Dopo aver creato l'effetto, esistono due passaggi rimanenti per usarlo.</span><span class="sxs-lookup"><span data-stu-id="8fa5e-112">After the effect is created, there are two remaining steps for using it.</span></span> <span data-ttu-id="8fa5e-113">In primo luogo, è necessario inizializzare i valori dello stato dell'effetto (i valori delle variabili dell'effetto) usando diversi metodi per impostare lo stato.</span><span class="sxs-lookup"><span data-stu-id="8fa5e-113">First, you must initialize the effect state values (the values of the effect variables) using a number of methods for setting state.</span></span> <span data-ttu-id="8fa5e-114">Per alcune variabili questa operazione può essere eseguita una sola volta quando viene creato un effetto. altri devono essere aggiornati ogni volta che l'applicazione chiama il ciclo di rendering.</span><span class="sxs-lookup"><span data-stu-id="8fa5e-114">For some variables this can be done once when an effect is created; others must be updated each time your application calls the render loop.</span></span> <span data-ttu-id="8fa5e-115">Dopo aver impostato le variabili di effetto, si indica al runtime di eseguire il rendering dell'effetto applicando una tecnica.</span><span class="sxs-lookup"><span data-stu-id="8fa5e-115">Once the effect variables are set, you tell the runtime to render the affect by applying a technique.</span></span> <span data-ttu-id="8fa5e-116">Questi argomenti vengono tutti discussi in dettaglio più avanti.</span><span class="sxs-lookup"><span data-stu-id="8fa5e-116">These topics are all discussed in further detail below.</span></span>

-   [<span data-ttu-id="8fa5e-117">Compilare un effetto (Direct3D 10)</span><span class="sxs-lookup"><span data-stu-id="8fa5e-117">Compile an Effect (Direct3D 10)</span></span>](d3d10-graphics-programming-guide-effects-compile.md)
-   [<span data-ttu-id="8fa5e-118">Creare un effetto (Direct3D 10)</span><span class="sxs-lookup"><span data-stu-id="8fa5e-118">Create an Effect (Direct3D 10)</span></span>](d3d10-graphics-programming-guide-effects-create.md)
-   [<span data-ttu-id="8fa5e-119">Impostare lo stato dell'effetto (Direct3D 10)</span><span class="sxs-lookup"><span data-stu-id="8fa5e-119">Set Effect State (Direct3D 10)</span></span>](d3d10-graphics-programming-guide-effects-set-state.md)
-   [<span data-ttu-id="8fa5e-120">Applicare una tecnica (Direct3D 10)</span><span class="sxs-lookup"><span data-stu-id="8fa5e-120">Apply a Technique (Direct3D 10)</span></span>](d3d10-graphics-programming-guide-effects-apply-technique.md)

<span data-ttu-id="8fa5e-121">Naturalmente, esistono considerazioni sulle [prestazioni per l'uso](d3d10-graphics-programming-guide-effects-performance.md) degli effetti.</span><span class="sxs-lookup"><span data-stu-id="8fa5e-121">Naturally there are [performance considerations](d3d10-graphics-programming-guide-effects-performance.md) for using effects.</span></span> <span data-ttu-id="8fa5e-122">Queste considerazioni sono in gran parte le stesse se non si usa un effetto.</span><span class="sxs-lookup"><span data-stu-id="8fa5e-122">These considerations are largely the same if you are not using an effect.</span></span> <span data-ttu-id="8fa5e-123">Ad esempio, riducendo al minimo la quantità di modifiche di stato o organizzando le variabili che devono essere aggiornate in base alla frequenza.</span><span class="sxs-lookup"><span data-stu-id="8fa5e-123">Things like, minimizing the amount of state changes, or organizing the variables that need to be updated by frequency.</span></span> <span data-ttu-id="8fa5e-124">Queste tattiche vengono usate per ridurre al minimo la quantità di dati che devono essere inviati dalla CPU alla GPU e quindi ridurre al minimo i potenziali problemi di sincronizzazione.</span><span class="sxs-lookup"><span data-stu-id="8fa5e-124">These tactics are used to minimize the amount of data that needs to be sent from the CPU to the GPU, and therefore minimize potential synchronization problems.</span></span>

## <a name="related-topics"></a><span data-ttu-id="8fa5e-125">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="8fa5e-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8fa5e-126">Effetti (Direct3D 10)</span><span class="sxs-lookup"><span data-stu-id="8fa5e-126">Effects (Direct3D 10)</span></span>](d3d10-graphics-programming-guide-effects.md)
</dt> </dl>

 

 



