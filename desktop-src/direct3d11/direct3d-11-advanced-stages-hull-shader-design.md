---
title: Come progettare un Hull shader
description: In questo argomento viene illustrato come progettare un Hull shader.
ms.assetid: c11c5652-dd7d-433d-bfa2-9853618ba334
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ece816ae33e7f4ecf4d024098e7741f197c423f1
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104993376"
---
# <a name="how-to-design-a-hull-shader"></a><span data-ttu-id="72e89-103">Procedura: progettare un Hull shader</span><span class="sxs-lookup"><span data-stu-id="72e89-103">How To: Design a Hull Shader</span></span>

<span data-ttu-id="72e89-104">Un Hull shader è il primo di tre fasi che interagiscono per implementare lo [schema a mosaico](direct3d-11-advanced-stages-tessellation.md) (le altre due fasi sono mosaico e Domain shader).</span><span class="sxs-lookup"><span data-stu-id="72e89-104">A hull shader is the first of three stages that work together to implement [tessellation](direct3d-11-advanced-stages-tessellation.md) (the other two stages are the tessellator and a domain shader).</span></span> <span data-ttu-id="72e89-105">In questo argomento viene illustrato come progettare un Hull shader.</span><span class="sxs-lookup"><span data-stu-id="72e89-105">This topics shows how to design a hull shader.</span></span>

<span data-ttu-id="72e89-106">Uno scafo shader richiede due funzioni, la principale Hull shader e una funzione costante patch.</span><span class="sxs-lookup"><span data-stu-id="72e89-106">A hull shader requires two functions, the main hull shader and a patch constant function.</span></span> <span data-ttu-id="72e89-107">Hull shader implementa i calcoli in ogni punto di controllo; Hull shader chiama anche la funzione Constant patch che implementa i calcoli in ogni patch.</span><span class="sxs-lookup"><span data-stu-id="72e89-107">The hull shader implements calculations on each control point; the hull shader also calls the patch constant function which implements calculations on each patch.</span></span>

<span data-ttu-id="72e89-108">Dopo aver progettato uno Hull shader, vedere [procedura: creare uno scafo shader](direct3d-11-advanced-stages-hull-shader-create.md) per informazioni su come creare un Hull shader.</span><span class="sxs-lookup"><span data-stu-id="72e89-108">After you have designed a hull shader, see [How To: Create a Hull Shader](direct3d-11-advanced-stages-hull-shader-create.md) to learn how to create a hull shader.</span></span>

<span data-ttu-id="72e89-109">**Per progettare uno Hull shader**</span><span class="sxs-lookup"><span data-stu-id="72e89-109">**To design a hull shader**</span></span>

1.  <span data-ttu-id="72e89-110">Definire i punti di controllo di output e controllo input Hull shader.</span><span class="sxs-lookup"><span data-stu-id="72e89-110">Define hull shader input control and output control points.</span></span>

    ```
    // Input control point
    struct VS_CONTROL_POINT_OUTPUT
    {
        float3 vPosition : WORLDPOS;
        float2 vUV       : TEXCOORD0;
        float3 vTangent  : TANGENT;
    };

    // Output control point
    struct BEZIER_CONTROL_POINT
    {
        float3 vPosition    : BEZIERPOS;
    };
    ```

    

2.  <span data-ttu-id="72e89-111">Definire i dati costanti della patch di output.</span><span class="sxs-lookup"><span data-stu-id="72e89-111">Define output patch constant data.</span></span>

    ```
    // Output patch constant data.
    struct HS_CONSTANT_DATA_OUTPUT
    {
        float Edges[4]        : SV_TessFactor;
        float Inside[2]       : SV_InsideTessFactor;
        
        float3 vTangent[4]    : TANGENT;
        float2 vUV[4]         : TEXCOORD;
        float3 vTanUCorner[4] : TANUCORNER;
        float3 vTanVCorner[4] : TANVCORNER;
        float4 vCWts          : TANWEIGHTS;
    };
    ```

    

    <span data-ttu-id="72e89-112">Per un dominio quad, [SV \_ TessFactor](/windows/desktop/direct3dhlsl/sv-tessfactor) definisce 4 fattori a mosaico perimetrale (per conteggiarla suddividerla i bordi), perché la funzione fissa mosaico deve conoscere la quantità di conteggiarla suddividerla.</span><span class="sxs-lookup"><span data-stu-id="72e89-112">For a quad domain, [SV\_TessFactor](/windows/desktop/direct3dhlsl/sv-tessfactor) defines 4 edge tessellation factors (to tessellate the edges), since the fixed function tessellator needs to know how much to tessellate.</span></span> <span data-ttu-id="72e89-113">Gli output necessari sono diversi per il triangolo e i domini di deoline.</span><span class="sxs-lookup"><span data-stu-id="72e89-113">The required outputs are different for the triangle and isoline domains.</span></span>

    <span data-ttu-id="72e89-114">La funzione fissa mosaico non esamina altri output di Hull shader, ad esempio altri dati della costante patch o uno dei punti di controllo.</span><span class="sxs-lookup"><span data-stu-id="72e89-114">The fixed function tessellator doesn't look at any other hull shader outputs, such as other patch constant data or any of the control points.</span></span> <span data-ttu-id="72e89-115">Il Domain shader, che viene richiamato per ogni punto che la funzione fissa mosaico genera, vedrà come input tutti i punti di controllo di output di Hull shader e tutti i dati costanti della patch di output. lo shader valuta la patch nella posizione.</span><span class="sxs-lookup"><span data-stu-id="72e89-115">The domain shader -- which is invoked for each point the fixed function tessellator generates -- will see as its input all the hull shader's output control points and all the output patch constant data; the shader evaluates the patch at its location.</span></span>

3.  <span data-ttu-id="72e89-116">Definire una funzione costante patch.</span><span class="sxs-lookup"><span data-stu-id="72e89-116">Define a patch constant function.</span></span> <span data-ttu-id="72e89-117">Una funzione costante patch viene eseguita una volta per ogni patch per calcolare i dati costanti per l'intera patch, anziché i dati del punto di controllo, che vengono calcolati nello scafo dello shader.</span><span class="sxs-lookup"><span data-stu-id="72e89-117">A patch constant function executes once for each patch to calculate any data that is constant for the entire patch (as opposed to per-control point data, which is computed in the hull shader).</span></span>

    ```
    
    #define MAX_POINTS 32

    // Patch Constant Function
    HS_CONSTANT_DATA_OUTPUT SubDToBezierConstantsHS( 
        InputPatch<VS_CONTROL_POINT_OUTPUT, MAX_POINTS> ip,
        uint PatchID : SV_PrimitiveID )
    {   
        HS_CONSTANT_DATA_OUTPUT Output;

        // Insert code to compute Output here
        
        return Output;
    }
    ```

    

    <span data-ttu-id="72e89-118">Le proprietà della funzione costante patch includono:</span><span class="sxs-lookup"><span data-stu-id="72e89-118">Properties of the patch constant function include:</span></span>

    -   <span data-ttu-id="72e89-119">Un input specifica una variabile contenente un ID patch ed è identificato dal valore di sistema **SV \_ PrimitiveID** (vedere [semantica](../direct3dhlsl/dx-graphics-hlsl-semantics.md) in Shader Model 4).</span><span class="sxs-lookup"><span data-stu-id="72e89-119">One input specifies a variable containing a patch id, and is identified by the **SV\_PrimitiveID** system value (see [semantics](../direct3dhlsl/dx-graphics-hlsl-semantics.md) in shader model 4).</span></span>
    -   <span data-ttu-id="72e89-120">Un parametro di input è i punti di controllo di input, dichiarati nell'output del punto di controllo di Visual Studio in questo esempio. **\_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="72e89-120">One input parameter is the input control points, declared in **VS\_CONTROL\_POINT\_OUTPUT** in this example.</span></span> <span data-ttu-id="72e89-121">Una funzione patch può visualizzare tutti i punti di controllo di input per ogni patch, in questo esempio sono presenti 32 punti di controllo per patch.</span><span class="sxs-lookup"><span data-stu-id="72e89-121">A patch function can see all the input control points for each patch, there are 32 control points per patch in this example.</span></span>
    -   <span data-ttu-id="72e89-122">Come minimo, è necessario che la funzione calcoli i fattori a mosaico per patch per la fase mosaico identificati con [SV \_ TessFactor](/windows/desktop/direct3dhlsl/sv-tessfactor).</span><span class="sxs-lookup"><span data-stu-id="72e89-122">As a minimum, the function must calculate per-patch tessellation factors for the tessellator stage which are identified with [SV\_TessFactor](/windows/desktop/direct3dhlsl/sv-tessfactor).</span></span> <span data-ttu-id="72e89-123">Un dominio Quad richiede quattro fattori a mosaico per i bordi e due fattori aggiuntivi (identificati da [SV \_ InsideTessFactor](/windows/desktop/direct3dhlsl/sv-insidetessfactor)) per tessellating all'interno della patch.</span><span class="sxs-lookup"><span data-stu-id="72e89-123">A quad domain requires four tessellation factors for the edges and two additional factors (identified by [SV\_InsideTessFactor](/windows/desktop/direct3dhlsl/sv-insidetessfactor)) for tessellating the inside of the patch.</span></span> <span data-ttu-id="72e89-124">La funzione fissa mosaico non esamina altri output di Hull shader, ad esempio i dati della costante patch o uno dei punti di controllo.</span><span class="sxs-lookup"><span data-stu-id="72e89-124">The fixed function tessellator doesn't look at any other hull shader outputs (such as the patch constant data or any of the control points).</span></span>
    -   <span data-ttu-id="72e89-125">Gli output vengono in genere definiti da una struttura e vengono identificati dall' **\_ \_ \_ output dei dati costanti HS** in questo esempio. la struttura dipende dal tipo di dominio e sarebbe diversa per i domini triangolo o oline.</span><span class="sxs-lookup"><span data-stu-id="72e89-125">The outputs are usually defined by a structure and is identified by **HS\_CONSTANT\_DATA\_OUTPUT** in this example; the structure depends on the domain type and would be different for triangle or isoline domains.</span></span>

    <span data-ttu-id="72e89-126">Un Domain shader viene richiamato per ogni punto che la funzione fissa mosaico genera e deve visualizzare i punti di controllo dell'output e i dati costanti della patch di output (entrambi dallo scafo) per valutare una patch nella relativa posizione.</span><span class="sxs-lookup"><span data-stu-id="72e89-126">A domain shader on the other hand is invoked for each point the fixed function tessellator generates and needs to see the output control points and the output patch constant data (both from the hull shader) to evaluate a patch at its location.</span></span>

4.  <span data-ttu-id="72e89-127">Definire un Hull shader.</span><span class="sxs-lookup"><span data-stu-id="72e89-127">Define a hull shader.</span></span> <span data-ttu-id="72e89-128">Uno scafo shader identifica le proprietà di una patch, inclusa una funzione costante patch.</span><span class="sxs-lookup"><span data-stu-id="72e89-128">A hull shader identifies the properties of a patch including a patch constant function.</span></span> <span data-ttu-id="72e89-129">Un Hull shader viene richiamato una volta per ogni punto di controllo dell'output.</span><span class="sxs-lookup"><span data-stu-id="72e89-129">A hull shader is invoked once for each output control point.</span></span>

    ```
    [domain("quad")]
    [partitioning("integer")]
    [outputtopology("triangle_cw")]
    [outputcontrolpoints(16)]
    [patchconstantfunc("SubDToBezierConstantsHS")]
    BEZIER_CONTROL_POINT SubDToBezierHS( 
        InputPatch<VS_CONTROL_POINT_OUTPUT, MAX_POINTS> ip, 
        uint i : SV_OutputControlPointID,
        uint PatchID : SV_PrimitiveID )
    {
        VS_CONTROL_POINT_OUTPUT Output;

        // Insert code to compute Output here.
        
        return Output;
    }
    ```

    

    <span data-ttu-id="72e89-130">Uno Hull shader usa i seguenti attributi:</span><span class="sxs-lookup"><span data-stu-id="72e89-130">A hull shader uses the following attributes:</span></span>

    -   <span data-ttu-id="72e89-131">Attributo di [dominio](/windows/desktop/direct3dhlsl/sm5-attributes-domain) .</span><span class="sxs-lookup"><span data-stu-id="72e89-131">A [domain](/windows/desktop/direct3dhlsl/sm5-attributes-domain) attribute.</span></span>
    -   <span data-ttu-id="72e89-132">Attributo di [partizionamento](/windows/desktop/direct3dhlsl/sm5-attributes-partitioning) .</span><span class="sxs-lookup"><span data-stu-id="72e89-132">A [partitioning](/windows/desktop/direct3dhlsl/sm5-attributes-partitioning) attribute.</span></span>
    -   <span data-ttu-id="72e89-133">Attributo [outputtopology](/windows/desktop/direct3dhlsl/sm5-attributes-outputtopology) .</span><span class="sxs-lookup"><span data-stu-id="72e89-133">An [outputtopology](/windows/desktop/direct3dhlsl/sm5-attributes-outputtopology) attribute.</span></span>
    -   <span data-ttu-id="72e89-134">Attributo [outputcontrolpoints](/windows/desktop/direct3dhlsl/sm5-attributes-outputcontrolpoints) .</span><span class="sxs-lookup"><span data-stu-id="72e89-134">An [outputcontrolpoints](/windows/desktop/direct3dhlsl/sm5-attributes-outputcontrolpoints) attribute.</span></span>
    -   <span data-ttu-id="72e89-135">Attributo [patchconstantfunc](/windows/desktop/direct3dhlsl/sm5-attributes-patchconstantfunc) .</span><span class="sxs-lookup"><span data-stu-id="72e89-135">A [patchconstantfunc](/windows/desktop/direct3dhlsl/sm5-attributes-patchconstantfunc) attribute.</span></span> <span data-ttu-id="72e89-136">Uno scafo shader calcola i punti di controllo di output. in questo esempio sono presenti 16 punti di controllo di Bezier di output.</span><span class="sxs-lookup"><span data-stu-id="72e89-136">A hull shader calculates output control points, there are 16 output Bezier control points in this example.</span></span>

<span data-ttu-id="72e89-137">Tutti i punti di controllo di input (identificati dall'output del punto di controllo di Visual Studio) sono visibili per ogni chiamata a Hull shader. **\_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="72e89-137">All the input control points (identified by **VS\_CONTROL\_POINT\_OUTPUT**) are visible to each hull shader invocation.</span></span> <span data-ttu-id="72e89-138">In questo esempio sono presenti 32 punti di controllo di input.</span><span class="sxs-lookup"><span data-stu-id="72e89-138">In this example, there are 32 input control points.</span></span>

<span data-ttu-id="72e89-139">Un Hull shader viene richiamato una volta per ogni punto di controllo dell'output (identificato con [SV \_ OutputControlPointID](/windows/desktop/direct3dhlsl/sv-outputcontrolpointid)) per ogni patch (identificato con SV \_ PrimitiveID).</span><span class="sxs-lookup"><span data-stu-id="72e89-139">A hull shader is invoked once per output control point (identified with [SV\_OutputControlPointID](/windows/desktop/direct3dhlsl/sv-outputcontrolpointid)) for each patch (identified with SV\_PrimitiveID).</span></span> <span data-ttu-id="72e89-140">Lo scopo di questo particolare shader consiste nel calcolare l' *i*/o di output, che è stato definito come un punto di controllo di Bezier (in questo esempio sono presenti 16 punti di controllo di output definiti da outputcontrolpoints).</span><span class="sxs-lookup"><span data-stu-id="72e89-140">The purpose of this particular shader is to calculate output *i*, which was defined to be a BEZIER control point (this example has 16 output control points defined by outputcontrolpoints).</span></span>

<span data-ttu-id="72e89-141">Uno Hull shader esegue una routine una volta per patch (funzione costante patch) per calcolare i dati di una costante di patch (come minimo i fattori a mosaico).</span><span class="sxs-lookup"><span data-stu-id="72e89-141">A hull shader runs a routine once per patch (the patch constant function) to compute patch-constant data (tessellation factors as a minimum).</span></span> <span data-ttu-id="72e89-142">Separatamente, un Hull shader esegue una funzione costante patch (denominata SubDToBezierConstantsHS) in ogni patch per calcolare i dati di una costante patch, ad esempio i fattori a mosaico per la fase mosaico.</span><span class="sxs-lookup"><span data-stu-id="72e89-142">Separately, a hull shader runs a patch constant function (called SubDToBezierConstantsHS) on each patch to compute patch-constant data such as tessellation factors for the tessellator stage.</span></span>

## <a name="related-topics"></a><span data-ttu-id="72e89-143">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="72e89-143">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="72e89-144">Come usare Direct3D 11</span><span class="sxs-lookup"><span data-stu-id="72e89-144">How to Use Direct3D 11</span></span>](how-to-use-direct3d-11.md)
</dt> <dt>

[<span data-ttu-id="72e89-145">Panoramica dello schema a mosaico</span><span class="sxs-lookup"><span data-stu-id="72e89-145">Tessellation Overview</span></span>](direct3d-11-advanced-stages-tessellation.md)
</dt> </dl>

 

 