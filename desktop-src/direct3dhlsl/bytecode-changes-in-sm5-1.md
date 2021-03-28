---
title: Modifiche bytecode in SM 5.1
description: SM 5.1 modifica il modo in cui i registri delle risorse vengono dichiarati e viene fatto riferimento nelle istruzioni.
ms.assetid: ABECF705-67B8-4419-8D18-74B43B9DC3AF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c6d66db788b0012a1c3221e37d4c2dd4e41566c6
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104332788"
---
# <a name="bytecode-changes-in-sm51"></a><span data-ttu-id="76f62-103">Modifiche bytecode in SM 5.1</span><span class="sxs-lookup"><span data-stu-id="76f62-103">Bytecode changes in SM5.1</span></span>

<span data-ttu-id="76f62-104">SM 5.1 modifica il modo in cui i registri delle risorse vengono dichiarati e viene fatto riferimento nelle istruzioni.</span><span class="sxs-lookup"><span data-stu-id="76f62-104">SM5.1 changes how resource registers are declared and referenced in instructions.</span></span>

<span data-ttu-id="76f62-105">SM 5.1 si sposta verso la dichiarazione di una "variabile" del registro, in modo analogo al modo in cui viene eseguita per i registri di memoria condivisa del gruppo, illustrata nell'esempio seguente:</span><span class="sxs-lookup"><span data-stu-id="76f62-105">SM5.1 moves towards declaring a register “variable”, similar to how it is done for group shared memory registers, illustrated by the following example:</span></span>

``` syntax
Texture2D<float4> tex0          : register(t5,  space0);
Texture2D<float4> tex1[][5][3]  : register(t10, space0);
Texture2D<float4> tex2[8]       : register(t0,  space1);
SamplerState samp0              : register(s5, space0);

float4 main(float4 coord : COORD) : SV_TARGET
{
    float4 r = coord;
    r += tex0.Sample(samp0, r.xy);
    r += tex2[r.x].Sample(samp0, r.xy);
    r += tex1[r.x][r.y][r.z].Sample(samp0, r.xy);
    return r;
}
```

<span data-ttu-id="76f62-106">Il disassembly di questo esempio segue:</span><span class="sxs-lookup"><span data-stu-id="76f62-106">The disassembly of this example follows:</span></span>

``` syntax
// Resource Bindings:
//
// Name                                 Type  Format         Dim Space Slot  Elements
// ------------------------------ ---------- ------- ----------- ----- ---- ---------
// samp0                             sampler      NA          NA     0    5         1
// tex0                              texture  float4          2d     0    5         1
// tex1[0][5][3]                     texture  float4          2d     0   10 unbounded
// tex2[8]                           texture  float4          2d     1    0         8
//
//
//
// Input signature:
//
// Name                 Index   Mask Register SysValue  Format   Used
// -------------------- ----- ------ -------- -------- ------- ------
// COORD                    0   xyzw        0     NONE   float   xyzw
//
//
// Output signature:
//
// Name                 Index   Mask Register SysValue  Format   Used
// -------------------- ----- ------ -------- -------- ------- ------
// SV_TARGET                0   xyzw        0   TARGET   float   xyzw
//
ps_5_1
dcl_globalFlags refactoringAllowed
dcl_sampler s0[5:5], mode_default, space=0
dcl_resource_texture2d (float,float,float,float) t0[5:5], space=0
dcl_resource_texture2d (float,float,float,float) t1[10:*], space=0
dcl_resource_texture2d (float,float,float,float) t2[0:7], space=1
dcl_input_ps linear v0.xyzw
dcl_output o0.xyzw
dcl_temps 2
sample r0.xyzw, v0.xyxx, t0[0].xyzw, s0[5]
add r0.xyzw, r0.xyzw, v0.xyzw
ftou r1.x, r0.x
sample r1.xyzw, r0.xyxx, t2[r1.x + 0].xyzw, s0[5]
add r0.xyzw, r0.xyzw, r1.xyzw
ftou r1.xyz, r0.zyxz
imul null, r1.yz, r1.zzyz, l(0, 15, 3, 0)
iadd r1.y, r1.z, r1.y
iadd r1.x, r1.x, r1.y
sample r1.xyzw, r0.xyxx, t1[r1.x + 10].xyzw, s0[5]
add o0.xyzw, r0.xyzw, r1.xyzw
ret
// Approximately 12 instruction slots used
```

<span data-ttu-id="76f62-107">Ogni intervallo di risorse shader dispone ora di un ID (un nome) nel bytecode dello shader.</span><span class="sxs-lookup"><span data-stu-id="76f62-107">Each shader resource range now has an ID (a name) in the shader bytecode.</span></span> <span data-ttu-id="76f62-108">Ad esempio, Tex1 texture array diventa ' T'1' nel codice byte dello shader.</span><span class="sxs-lookup"><span data-stu-id="76f62-108">For example, tex1 texture array becomes ‘t1’ in the shader byte code.</span></span> <span data-ttu-id="76f62-109">L'assegnazione di ID univoci a ogni intervallo di risorse consente due elementi:</span><span class="sxs-lookup"><span data-stu-id="76f62-109">Giving unique IDs to each resource range allows two things:</span></span>

-   <span data-ttu-id="76f62-110">Identificare in modo univoco l'intervallo di risorse (vedere \_ la pagina relativa \_ all'indicizzazione della risorsa DCL Texture2D) in un'istruzione (vedere l'istruzione di esempio).</span><span class="sxs-lookup"><span data-stu-id="76f62-110">Unambiguously identify which resource range (see dcl\_resource\_texture2d) is being indexed in an instruction (see sample instruction).</span></span>
-   <span data-ttu-id="76f62-111">Alleghi set di attributi alla dichiarazione, ad esempio il tipo di elemento, le dimensioni stride, la modalità operativa raster e così via.</span><span class="sxs-lookup"><span data-stu-id="76f62-111">Attach set of attributes to the declaration, e.g., element type, stride size, raster operation mode, etc..</span></span>

<span data-ttu-id="76f62-112">Si noti che l'ID dell'intervallo non è correlato alla dichiarazione di limite inferiore HLSL.</span><span class="sxs-lookup"><span data-stu-id="76f62-112">Note that the ID of the range is not related to the HLSL lower bound declaration.</span></span>

<span data-ttu-id="76f62-113">L'ordine delle associazioni delle risorse di reflection e delle istruzioni di dichiarazione dello shader è lo stesso per facilitare l'identificazione della corrispondenza tra le variabili HLSL e gli ID bytecode.</span><span class="sxs-lookup"><span data-stu-id="76f62-113">The order of reflection resource bindings and shader declaration instructions is the same to aid in identifying the correspondence between HLSL variables and bytecode IDs.</span></span>

<span data-ttu-id="76f62-114">Ogni istruzione di dichiarazione in SM 5.1 utilizza un operando 3D per definire: ID intervallo, limiti inferiori e superiori.</span><span class="sxs-lookup"><span data-stu-id="76f62-114">Each declaration instruction in SM5.1 uses a 3D operand to define: range ID, lower and upper bounds.</span></span> <span data-ttu-id="76f62-115">Viene emesso un token aggiuntivo per specificare lo spazio del registro.</span><span class="sxs-lookup"><span data-stu-id="76f62-115">An additional token is emitted to specify the register space.</span></span> <span data-ttu-id="76f62-116">È possibile che vengano generati anche altri token per fornire proprietà aggiuntive dell'intervallo, ad esempio cbuffer o l'istruzione di dichiarazione del buffer strutturato genera la dimensione di cbuffer o della struttura.</span><span class="sxs-lookup"><span data-stu-id="76f62-116">Other tokens may be emitted as well to convey additional properties of the range, e.g., cbuffer or structured buffer declaration instruction emits the size of the cbuffer or structure.</span></span> <span data-ttu-id="76f62-117">I dettagli esatti della codifica sono disponibili in d3d12TokenizedProgramFormat. h e D3D10ShaderBinary:: CShaderCodeParser.</span><span class="sxs-lookup"><span data-stu-id="76f62-117">The exact details of encoding can be found in d3d12TokenizedProgramFormat.h and D3D10ShaderBinary::CShaderCodeParser.</span></span>

<span data-ttu-id="76f62-118">Le istruzioni di SM 5.1 non emetteranno Informazioni aggiuntive sull'operando delle risorse come parte dell'istruzione (ad esempio, SM 5.0).</span><span class="sxs-lookup"><span data-stu-id="76f62-118">SM5.1 instructions will not emit additional resource operand information as part of the instruction (as in SM5.0).</span></span> <span data-ttu-id="76f62-119">Queste informazioni vengono ora spostate nelle istruzioni di dichiarazione.</span><span class="sxs-lookup"><span data-stu-id="76f62-119">This information is now moved to the declaration instructions.</span></span> <span data-ttu-id="76f62-120">In SM 5.0, le istruzioni per l'indicizzazione delle risorse gli attributi delle risorse devono essere descritte in token opcode estesi, perché l'indicizzazione ha offuscato l'associazione alla dichiarazione.</span><span class="sxs-lookup"><span data-stu-id="76f62-120">In SM5.0, instructions indexing resources required resource attributes to be described in extended opcode tokens, since indexing obfuscated the association to the declaration.</span></span> <span data-ttu-id="76f62-121">In SM 5.1 ogni ID (ad esempio,' t 1') viene associato in modo non ambiguo a una singola dichiarazione che descrive le informazioni necessarie sulle risorse.</span><span class="sxs-lookup"><span data-stu-id="76f62-121">In SM5.1 each ID (such as ‘t1’) is unambiguously associated with a single declaration that describes the required resource information.</span></span> <span data-ttu-id="76f62-122">Pertanto, i token opcode estesi usati sulle istruzioni per descrivere le informazioni sulle risorse non vengono più generati.</span><span class="sxs-lookup"><span data-stu-id="76f62-122">Therefore, the extended opcode tokens used on instructions to describe resource information are no longer emitted.</span></span>

<span data-ttu-id="76f62-123">Nelle istruzioni di non dichiarazione, un operando di risorsa per Samplers, SRVs e UAV è un operando 2D.</span><span class="sxs-lookup"><span data-stu-id="76f62-123">In non-declaration instructions, a resource operand for samplers, SRVs, and UAVs is a 2D operand.</span></span> <span data-ttu-id="76f62-124">Il primo indice è una costante letterale che specifica l'ID intervallo.</span><span class="sxs-lookup"><span data-stu-id="76f62-124">The first index is a literal constant that specifies the range ID.</span></span> <span data-ttu-id="76f62-125">Il secondo indice rappresenta il valore linearizzato dell'indice.</span><span class="sxs-lookup"><span data-stu-id="76f62-125">The second index represents the linearized value of the index.</span></span> <span data-ttu-id="76f62-126">Il valore viene calcolato in relazione all'inizio dello spazio di registro corrispondente (non relativo all'inizio dell'intervallo logico) per una migliore correlazione con la firma radice e per ridurre il carico del compilatore del driver per la modifica dell'indice.</span><span class="sxs-lookup"><span data-stu-id="76f62-126">The value is computed relative to the beginning of the corresponding register space (not relative to the beginning of the logical range) to better correlate with the root signature and to reduce the driver compiler burden of adjusting the index.</span></span>

<span data-ttu-id="76f62-127">Un operando di risorsa per CBVs è un operando 3D: ID letterale dell'intervallo, indice di cbuffer, offset nell'istanza specifica di cbuffer.</span><span class="sxs-lookup"><span data-stu-id="76f62-127">A resource operand for CBVs is a 3D operand: literal ID of the range, index of the cbuffer, offset into the particular instance of cbuffer.</span></span>

## <a name="related-topics"></a><span data-ttu-id="76f62-128">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="76f62-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="76f62-129">Funzionalità del modello HLSL shader 5,1 per Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="76f62-129">HLSL Shader Model 5.1 Features for Direct3D 12</span></span>](hlsl-shader-model-5-1-features-for-direct3d-12.md)
</dt> <dt>

[<span data-ttu-id="76f62-130">Modello Shader 5,1</span><span class="sxs-lookup"><span data-stu-id="76f62-130">Shader Model 5.1</span></span>](shader-model-5-1.md)
</dt> </dl>

 

 




