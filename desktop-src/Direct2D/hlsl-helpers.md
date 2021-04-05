---
title: Helper HLSL
description: Per assistere gli autori degli effetti nella scrittura di pixel shader collegabili, d2d1effecthelpers. hlsli definisce un set di estensioni del linguaggio HLSL sotto forma di metodi di supporto e macro.
ms.assetid: 5D0BB99E-7C77-4D45-82E6-F038E4B752A4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ec8f43447c16d93ef9e1839ac319c761b975222a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103955236"
---
# <a name="hlsl-helpers"></a><span data-ttu-id="9aab7-103">Helper HLSL</span><span class="sxs-lookup"><span data-stu-id="9aab7-103">HLSL Helpers</span></span>

<span data-ttu-id="9aab7-104">Per assistere gli autori degli effetti nella scrittura di pixel shader collegabili, d2d1effecthelpers. hlsli definisce un set di estensioni del linguaggio HLSL sotto forma di metodi di supporto e macro.</span><span class="sxs-lookup"><span data-stu-id="9aab7-104">To assist effect authors in writing linkable pixel shaders, d2d1effecthelpers.hlsli defines a set of HLSL language extensions in the form of helper methods and macros.</span></span>

<span data-ttu-id="9aab7-105">Per aggiungere d2d1effecthelpers. hlsli al progetto, aggiungere un' \# istruzione include nel file HLSL.</span><span class="sxs-lookup"><span data-stu-id="9aab7-105">To add d2d1effecthelpers.hlsli to your project, add an \#include statement in the HLSL file.</span></span> <span data-ttu-id="9aab7-106">d2d1effecthelpers. hlsli si trova nella stessa posizione di altre intestazioni Direct2D, ad esempio d2d1. h; è possibile farvi riferimento dalla pagina delle proprietà del file HLSL aggiungendo la macro $ (WindowsSDK \_ IncludePath) alla proprietà directory di inclusione aggiuntive.</span><span class="sxs-lookup"><span data-stu-id="9aab7-106">d2d1effecthelpers.hlsli is located in the same location as other Direct2D headers such as d2d1.h; it can be referenced from the HLSL file's property page by adding the macro $(WindowsSDK\_IncludePath) to the Additional Include Directories property.</span></span> <span data-ttu-id="9aab7-107">Si noti che l' \# istruzione include deve provenire dopo la definizione di tutte le direttive per il preprocessore, come il \_ numero di input D2D \_ .</span><span class="sxs-lookup"><span data-stu-id="9aab7-107">Note that the \#include statement must come after any preprocessor directives such D2D\_INPUT\_COUNT have been defined.</span></span>

``` syntax
#include <d2d1effecthelpers.hlsli>
```

<span data-ttu-id="9aab7-108">Direct2D non supporta il collegamento di COMPUTE o vertex shader.</span><span class="sxs-lookup"><span data-stu-id="9aab7-108">Direct2D does not support linking compute or vertex shaders.</span></span> <span data-ttu-id="9aab7-109">Tuttavia, se l'effetto USA sia un vertex shader che un pixel shader, l'output del pixel shader può ancora essere collegato.</span><span class="sxs-lookup"><span data-stu-id="9aab7-109">However, if your effect uses both a vertex shader and pixel shader, the output of the pixel shader can still be linked.</span></span>

## <a name="preprocessor-directives"></a><span data-ttu-id="9aab7-110">Direttive per il preprocessore</span><span class="sxs-lookup"><span data-stu-id="9aab7-110">Preprocessor Directives</span></span>

<span data-ttu-id="9aab7-111">Le direttive per il preprocessore sono necessarie per comunicare informazioni sull'effetto.</span><span class="sxs-lookup"><span data-stu-id="9aab7-111">Preprocessor directives are required to communicate information about the effect.</span></span> <span data-ttu-id="9aab7-112">Sono inclusi il numero di input e il tipo di campionamento di ogni input.</span><span class="sxs-lookup"><span data-stu-id="9aab7-112">This includes the number of inputs and sampling type of each input.</span></span> <span data-ttu-id="9aab7-113">Quando applicabile, è necessario definire i valori seguenti nel codice dello shader di effetto sopra il punto di ingresso dello shader pertinente.</span><span class="sxs-lookup"><span data-stu-id="9aab7-113">The following values should be defined in the effect shader code above the relevant shader entry point when applicable.</span></span>

-   <span data-ttu-id="9aab7-114">`D2D_INPUT_COUNT <N>` : Dichiara il numero di input di trama all'effetto.</span><span class="sxs-lookup"><span data-stu-id="9aab7-114">`D2D_INPUT_COUNT <N>` : Declares the number of texture inputs to the effect.</span></span> <span data-ttu-id="9aab7-115">Se l'effetto ha un numero variabile di input, questo valore deve essere definito in modo appropriato per ogni punto di ingresso dello shader.</span><span class="sxs-lookup"><span data-stu-id="9aab7-115">If the effect has a variable number of inputs, this value must be scoped appropriately to each shader entry point.</span></span> <span data-ttu-id="9aab7-116">La definizione di questo valore è obbligatoria.</span><span class="sxs-lookup"><span data-stu-id="9aab7-116">Defining this value is mandatory.</span></span>
-   <span data-ttu-id="9aab7-117">`D2D_INPUT<N>_SIMPLE` : Dichiara l'ennesimo input per usare il campionamento semplice.</span><span class="sxs-lookup"><span data-stu-id="9aab7-117">`D2D_INPUT<N>_SIMPLE` : Declares the Nth input to use simple sampling.</span></span> <span data-ttu-id="9aab7-118">Se non è definito, l'ennesimo input predefinito è complesso.</span><span class="sxs-lookup"><span data-stu-id="9aab7-118">If not defined, the Nth input defaults to complex.</span></span> <span data-ttu-id="9aab7-119">La definizione di questo valore è facoltativa.</span><span class="sxs-lookup"><span data-stu-id="9aab7-119">Defining this value is optional.</span></span>
-   <span data-ttu-id="9aab7-120">`D2D_INPUT<N>_COMPLEX` : Dichiara l'ennesimo input per usare il campionamento complesso.</span><span class="sxs-lookup"><span data-stu-id="9aab7-120">`D2D_INPUT<N>_COMPLEX` : Declares the Nth input to use complex sampling.</span></span> <span data-ttu-id="9aab7-121">Se non è definito, l'ennesimo input predefinito è complesso.</span><span class="sxs-lookup"><span data-stu-id="9aab7-121">If not defined, the Nth input defaults to complex.</span></span> <span data-ttu-id="9aab7-122">La definizione di questo valore è facoltativa.</span><span class="sxs-lookup"><span data-stu-id="9aab7-122">Defining this value is optional.</span></span>
-   <span data-ttu-id="9aab7-123">`D2D_REQUIRES_SCENE_POSITION` : Indica che la funzione shader chiama metodi helper che usano il valore della posizione della scena, ovvero la funzione di supporto [D2DGetScenePosition](d2dgetsceneposition.md) .</span><span class="sxs-lookup"><span data-stu-id="9aab7-123">`D2D_REQUIRES_SCENE_POSITION` : Indicates that the shader function calls helper methods that use the scene position value (namely, the [D2DGetScenePosition](d2dgetsceneposition.md) helper function).</span></span> <span data-ttu-id="9aab7-124">Questo parametro deve essere incluso solo quando necessario, perché solo una funzione per shader collegato può utilizzare questo parametro.</span><span class="sxs-lookup"><span data-stu-id="9aab7-124">This parameter should only be included when necessary, since only one function per linked shader can utilize this parameter.</span></span> <span data-ttu-id="9aab7-125">La definizione di questo valore è facoltativa.</span><span class="sxs-lookup"><span data-stu-id="9aab7-125">Defining this value is optional.</span></span>
-   <span data-ttu-id="9aab7-126">`D2D_CUSTOM_ENTRY` : Indica che la funzione pixel shader utilizza l'output di un vertex shader personalizzato e quindi dichiara i parametri di input.</span><span class="sxs-lookup"><span data-stu-id="9aab7-126">`D2D_CUSTOM_ENTRY` : Indicates that the pixel shader function consumes the output of a custom vertex shader, and thus will declare its input parameters.</span></span> <span data-ttu-id="9aab7-127">Tutti gli input di vertex shader personalizzati usano il campionamento complesso e non possono utilizzare l'output di un'altra funzione shader, ovvero sono solo post-Linkable.</span><span class="sxs-lookup"><span data-stu-id="9aab7-127">All custom vertex shader inputs use complex sampling, and cannot consume the output of another shader function (i.e. they are only post-linkable).</span></span> <span data-ttu-id="9aab7-128">La definizione di questo valore è facoltativa.</span><span class="sxs-lookup"><span data-stu-id="9aab7-128">Defining this value is optional.</span></span>

<span data-ttu-id="9aab7-129">Ad esempio:</span><span class="sxs-lookup"><span data-stu-id="9aab7-129">For example:</span></span>

``` syntax
#define D2D_INPUT_COUNT 3
#define D2D_INPUT0_SIMPLE
#define D2D_INPUT1_SIMPLE
#define D2D_INPUT2_COMPLEX
#include <d2d1effecthelpers.hlsli>
          
```

## <a name="helper-functions"></a><span data-ttu-id="9aab7-130">Funzioni di supporto</span><span class="sxs-lookup"><span data-stu-id="9aab7-130">Helper Functions</span></span>

<span data-ttu-id="9aab7-131">Le funzioni di supporto vengono usate come sostituzione per alcune funzioni intrinseche HLSL native.</span><span class="sxs-lookup"><span data-stu-id="9aab7-131">Helper functions are used as a replacement for some native HLSL intrinsic functions.</span></span> <span data-ttu-id="9aab7-132">In fase di compilazione, queste funzioni di supporto vengono ridefinite da Direct2D nella versione appropriata a seconda del tipo di destinazione della compilazione (funzione shader completa o funzione di esportazione).</span><span class="sxs-lookup"><span data-stu-id="9aab7-132">At compile time, these helper functions are redefined by Direct2D into the appropriate version depending on the compilation target type (full shader or export function).</span></span>

<span data-ttu-id="9aab7-133">Funzioni helper:</span><span class="sxs-lookup"><span data-stu-id="9aab7-133">The helper functions:</span></span>

<dl>

[<span data-ttu-id="9aab7-134">D2DGetInput</span><span class="sxs-lookup"><span data-stu-id="9aab7-134">D2DGetInput</span></span>](d2dgetinput.md)  
[<span data-ttu-id="9aab7-135">D2DSampleInput</span><span class="sxs-lookup"><span data-stu-id="9aab7-135">D2DSampleInput</span></span>](d2dsampleinput.md)  
[<span data-ttu-id="9aab7-136">D2DSampleInputAtOffset</span><span class="sxs-lookup"><span data-stu-id="9aab7-136">D2DSampleInputAtOffset</span></span>](d2dsampleinputatoffset.md)  
[<span data-ttu-id="9aab7-137">D2DSampleInputAtPosition</span><span class="sxs-lookup"><span data-stu-id="9aab7-137">D2DSampleInputAtPosition</span></span>](d2dsampleinputatposition.md)  
[<span data-ttu-id="9aab7-138">D2DGetInputCoordinate</span><span class="sxs-lookup"><span data-stu-id="9aab7-138">D2DGetInputCoordinate</span></span>](d2dgetinputcoordinate.md)  
[<span data-ttu-id="9aab7-139">D2DGetScenePosition</span><span class="sxs-lookup"><span data-stu-id="9aab7-139">D2DGetScenePosition</span></span>](d2dgetsceneposition.md)  
[<span data-ttu-id="9aab7-140">\_Voce D2D PS \_</span><span class="sxs-lookup"><span data-stu-id="9aab7-140">D2D\_PS\_ENTRY</span></span>](d2d-ps-entry.md)  
</dl>

## <a name="related-topics"></a><span data-ttu-id="9aab7-141">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="9aab7-141">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9aab7-142">Collegamento Effect shader</span><span class="sxs-lookup"><span data-stu-id="9aab7-142">Effect Shader Linking</span></span>](effect-shader-linking.md)
</dt> </dl>

 

 




