---
description: Un effetto può essere utilizzato per archiviare le informazioni o per eseguire il rendering utilizzando un gruppo di stato.
ms.assetid: c5654335-ad80-4a5b-bf1f-5f32b2cc8ea2
title: Rendering di un effetto (Direct3D 10)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cfba9432412846e2dc634d6ab68be999b504e06f
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104225577"
---
# <a name="rendering-an-effect-direct3d-10"></a><span data-ttu-id="66d96-103">Rendering di un effetto (Direct3D 10)</span><span class="sxs-lookup"><span data-stu-id="66d96-103">Rendering an Effect (Direct3D 10)</span></span>

<span data-ttu-id="66d96-104">Un effetto può essere utilizzato per archiviare le informazioni o per eseguire il rendering utilizzando un gruppo di stato.</span><span class="sxs-lookup"><span data-stu-id="66d96-104">An effect can be used to store information, or to render using a group of state.</span></span> <span data-ttu-id="66d96-105">Ogni tecnica specifica i vertex shader, i geometry shader, i pixel shader, lo stato dello shader, il campionatore e lo stato della trama e altro stato della pipeline.</span><span class="sxs-lookup"><span data-stu-id="66d96-105">Each technique specifies vertex shaders, geometry shaders, pixel shaders, shader state, sampler and texture state and other pipeline state.</span></span> <span data-ttu-id="66d96-106">Quindi, dopo avere organizzato lo stato in un effetto, è possibile incapsulare l'effetto di rendering risultante da tale stato creando ed eseguendo il rendering dell'effetto.</span><span class="sxs-lookup"><span data-stu-id="66d96-106">So once you have organized state into an effect, you can encapsulate the rendering effect that results from that state by creating and rendering the effect.</span></span>

<span data-ttu-id="66d96-107">Sono necessari alcuni passaggi per preparare un effetto per il rendering.</span><span class="sxs-lookup"><span data-stu-id="66d96-107">There are a few steps for preparing an effect for rendering.</span></span> <span data-ttu-id="66d96-108">Il primo sta eseguendo la compilazione, che controlla HLSL come il codice rispetto alla sintassi del linguaggio HLSL e alle regole del Framework effetti.</span><span class="sxs-lookup"><span data-stu-id="66d96-108">The first is compiling, which checks the HLSL like code against the HLSL language syntax and the effect framework rules.</span></span> <span data-ttu-id="66d96-109">È possibile compilare un effetto dall'applicazione usando le chiamate API oppure è possibile compilare un effetto offline usando l'utilità del compilatore di effetti.</span><span class="sxs-lookup"><span data-stu-id="66d96-109">You can compile an effect from your application using API calls or you can compile an effect offline using the effect compiler utility.</span></span> <span data-ttu-id="66d96-110">Una volta che l'effetto è stato compilato correttamente, crearlo chiamando un set di API diverso (ma molto simile).</span><span class="sxs-lookup"><span data-stu-id="66d96-110">Once your effect has successfully compiled, create it by calling a different (but very similar) set of APIs.</span></span>

<span data-ttu-id="66d96-111">Dopo aver creato l'effetto, per utilizzarlo sono necessari due passaggi.</span><span class="sxs-lookup"><span data-stu-id="66d96-111">After the effect is created, there are two remaining steps for using it.</span></span> <span data-ttu-id="66d96-112">In primo luogo, è necessario inizializzare i valori dello stato dell'effetto (i valori delle variabili dell'effetto) usando diversi metodi per impostare lo stato.</span><span class="sxs-lookup"><span data-stu-id="66d96-112">First, you must initialize the effect state values (the values of the effect variables) using a number of methods for setting state.</span></span> <span data-ttu-id="66d96-113">Per alcune variabili questa operazione può essere eseguita una volta quando viene creato un effetto; altri devono essere aggiornati ogni volta che l'applicazione chiama il ciclo di rendering.</span><span class="sxs-lookup"><span data-stu-id="66d96-113">For some variables this can be done once when an effect is created; others must be updated each time your application calls the render loop.</span></span> <span data-ttu-id="66d96-114">Una volta impostate le variabili di effetto, si indica al runtime di eseguire il rendering dell'effetto applicando una tecnica.</span><span class="sxs-lookup"><span data-stu-id="66d96-114">Once the effect variables are set, you tell the runtime to render the affect by applying a technique.</span></span> <span data-ttu-id="66d96-115">Questi argomenti sono descritti in dettaglio più avanti.</span><span class="sxs-lookup"><span data-stu-id="66d96-115">These topics are all discussed in further detail below.</span></span>

-   [<span data-ttu-id="66d96-116">Compilare un effetto (Direct3D 10)</span><span class="sxs-lookup"><span data-stu-id="66d96-116">Compile an Effect (Direct3D 10)</span></span>](d3d10-graphics-programming-guide-effects-compile.md)
-   [<span data-ttu-id="66d96-117">Creazione di un effetto (Direct3D 10)</span><span class="sxs-lookup"><span data-stu-id="66d96-117">Create an Effect (Direct3D 10)</span></span>](d3d10-graphics-programming-guide-effects-create.md)
-   [<span data-ttu-id="66d96-118">Impostare lo stato dell'effetto (Direct3D 10)</span><span class="sxs-lookup"><span data-stu-id="66d96-118">Set Effect State (Direct3D 10)</span></span>](d3d10-graphics-programming-guide-effects-set-state.md)
-   [<span data-ttu-id="66d96-119">Applicare una tecnica (Direct3D 10)</span><span class="sxs-lookup"><span data-stu-id="66d96-119">Apply a Technique (Direct3D 10)</span></span>](d3d10-graphics-programming-guide-effects-apply-technique.md)

<span data-ttu-id="66d96-120">Naturalmente, esistono [considerazioni sulle prestazioni](d3d10-graphics-programming-guide-effects-performance.md) per l'utilizzo di effetti.</span><span class="sxs-lookup"><span data-stu-id="66d96-120">Naturally there are [performance considerations](d3d10-graphics-programming-guide-effects-performance.md) for using effects.</span></span> <span data-ttu-id="66d96-121">Queste considerazioni sono in gran parte identiche se non si utilizza un effetto.</span><span class="sxs-lookup"><span data-stu-id="66d96-121">These considerations are largely the same if you are not using an effect.</span></span> <span data-ttu-id="66d96-122">Come, ridurre al minimo la quantità di modifiche di stato o organizzare le variabili che devono essere aggiornate in base alla frequenza.</span><span class="sxs-lookup"><span data-stu-id="66d96-122">Things like, minimizing the amount of state changes, or organizing the variables that need to be updated by frequency.</span></span> <span data-ttu-id="66d96-123">Queste tattiche vengono usate per ridurre al minimo la quantità di dati che devono essere inviati dalla CPU alla GPU e quindi ridurre al minimo i potenziali problemi di sincronizzazione.</span><span class="sxs-lookup"><span data-stu-id="66d96-123">These tactics are used to minimize the amount of data that needs to be sent from the CPU to the GPU, and therefore minimize potential synchronization problems.</span></span>

## <a name="related-topics"></a><span data-ttu-id="66d96-124">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="66d96-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="66d96-125">Effetti (Direct3D 10)</span><span class="sxs-lookup"><span data-stu-id="66d96-125">Effects (Direct3D 10)</span></span>](d3d10-graphics-programming-guide-effects.md)
</dt> </dl>

 

 



