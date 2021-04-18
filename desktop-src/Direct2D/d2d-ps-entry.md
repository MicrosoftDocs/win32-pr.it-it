---
title: Funzione D2D_PS_ENTRY (D2d1effecthelpers. h)
description: Una macro che definisce un punto di ingresso di pixel shader con il nome di funzione specificato.
ms.assetid: 4C87369A-EF51-46BA-9CA4-386630A7F866
keywords:
- Direct2D funzione D2D_PS_ENTRY
topic_type:
- apiref
api_name:
- D2D_PS_ENTRY
api_location:
- d2d1.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7525416eed7700709d02d2ec17823cd57a8c12ba
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324434"
---
# <a name="d2d_ps_entry-function"></a><span data-ttu-id="e75e3-104">\_Funzione di \_ immissione D2D PS</span><span class="sxs-lookup"><span data-stu-id="e75e3-104">D2D\_PS\_ENTRY function</span></span>

<span data-ttu-id="e75e3-105">Una macro che definisce un punto di ingresso di pixel shader con il nome di funzione specificato.</span><span class="sxs-lookup"><span data-stu-id="e75e3-105">A macro that defines a pixel shader entry point with the given function name.</span></span>

## <a name="syntax"></a><span data-ttu-id="e75e3-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="e75e3-106">Syntax</span></span>

``` syntax
void WINAPI D2D_PS_ENTRY(
  in string Entryname
);
```

## <a name="parameters"></a><span data-ttu-id="e75e3-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="e75e3-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e75e3-108">*Entryname* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e75e3-108">*Entryname* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e75e3-109">Nome del punto di ingresso del pixel shader.</span><span class="sxs-lookup"><span data-stu-id="e75e3-109">The pixel shader entry point name.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e75e3-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="e75e3-110">Return value</span></span>

<span data-ttu-id="e75e3-111">Questa funzione non restituisce un valore.</span><span class="sxs-lookup"><span data-stu-id="e75e3-111">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="e75e3-112">Commenti</span><span class="sxs-lookup"><span data-stu-id="e75e3-112">Remarks</span></span>

<span data-ttu-id="e75e3-113">Usare questa macro invece di specificare la firma di input del punto di ingresso in modo normale: tutti i parametri sono impliciti e vengono aggiunti da Direct2D durante la compilazione a seconda del tipo di destinazione della compilazione (funzione shader completa o esportazione).</span><span class="sxs-lookup"><span data-stu-id="e75e3-113">Use this macro instead of specifying the entry point s input signature in the normal manner: all parameters are implicit and added by Direct2D during compilation depending on the compilation target type (full shader or export function).</span></span>

``` syntax
#define D2D_INPUT_COUNT 1 
#define D2D_INPUT0_SIMPLE 
#include  d2d1effectauthor.hlsli  

D2D_PS_ENTRY(LinkingCompatiblePixelShader) 
{ 
    float4 input = D2DGetInput(0);  

    input.rgb *= input.a; 

    return input; 
} 
```

<span data-ttu-id="e75e3-114">In questo breve esempio si noti che non vengono dichiarati parametri di funzione, che il numero di input e il tipo di ogni input sono dichiarati prima della funzione entry, che l'input viene recuperato chiamando [D2DGetInput](d2dgetinput.md)e che le direttive per il preprocessore devono essere definite prima che il file helper venga incluso.</span><span class="sxs-lookup"><span data-stu-id="e75e3-114">In this short example note that no function parameters are declared, that the number of inputs and type of each input is declared before the entry function, the input is retrieved by calling [D2DGetInput](d2dgetinput.md), and that preprocessor directives must be defined before the helper file is included.</span></span>

<span data-ttu-id="e75e3-115">Uno shader compatibile con il collegamento deve fornire sia un pixel shader a singolo passaggio normale che una funzione di esportazione dello shader.</span><span class="sxs-lookup"><span data-stu-id="e75e3-115">A linking-compatible shader must provide both a regular single-pass pixel shader and an export shader function.</span></span> <span data-ttu-id="e75e3-116">La \_ macro di immissione D2D PS consente la generazione di \_ ognuno di questi dallo stesso codice, se usato insieme allo script di compilazione dello shader.</span><span class="sxs-lookup"><span data-stu-id="e75e3-116">The D2D\_PS\_ENTRY macro allows each of these to be generated from the same code, when used in conjunction with the shader compilation script.</span></span>

<span data-ttu-id="e75e3-117">Quando si compila uno shader completo, le macro vengono espanse nel codice seguente, che ha una firma di input compatibile con gli effetti D2D.</span><span class="sxs-lookup"><span data-stu-id="e75e3-117">When compiling a full shader, the macros are expanded into the following code, which has a D2D Effects-compatible input signature.</span></span>

``` syntax
Texture2D<float4> InputTexture0; 
SamplerState InputSampler0; 

float4 LinkingCompatiblePixelShader(
    float4 pos   : SV_POSITION,   
    float4 posScene : SCENE_POSITION,    
    float4 uv0  : TEXCOORD0 
    ) : SV_Target 
{ 
    float4 input = InputTexture0.Sample(InputSampler0, uv0.xy);  

    input.rgb *= input.a; 

    return input; 
} 
```

<span data-ttu-id="e75e3-118">Quando si compila una versione della funzione Export dello stesso codice, viene generato il codice seguente:</span><span class="sxs-lookup"><span data-stu-id="e75e3-118">When compiling an export function version of the same code, the following code is generated:</span></span>

``` syntax
// Shader function version 
export float4 LinkingCompatiblePixelShader_Function( 
    float4 input0 : INPUT0 
    ) 
{ 
    input.rgb *= input.a; 

    return input; 
} 
```

<span data-ttu-id="e75e3-119">Si noti che l'input di trama, generalmente recuperato tramite il campionamento di un Texture2D, è stato sostituito con un input0 di input della funzione.</span><span class="sxs-lookup"><span data-stu-id="e75e3-119">Note that the texture input, normally retrieved by sampling a Texture2D, has been replaced with a function input input0.</span></span>

## <a name="requirements"></a><span data-ttu-id="e75e3-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e75e3-120">Requirements</span></span>



| <span data-ttu-id="e75e3-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="e75e3-121">Requirement</span></span> | <span data-ttu-id="e75e3-122">Valore</span><span class="sxs-lookup"><span data-stu-id="e75e3-122">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e75e3-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="e75e3-123">Header</span></span><br/> | <dl> <span data-ttu-id="e75e3-124"><dt>D2d1effecthelpers. hlsli</dt></span><span class="sxs-lookup"><span data-stu-id="e75e3-124"><dt>D2d1effecthelpers.hlsli</dt></span></span> </dl> |
| <span data-ttu-id="e75e3-125">DLL</span><span class="sxs-lookup"><span data-stu-id="e75e3-125">DLL</span></span><br/>    | <dl> <span data-ttu-id="e75e3-126"><dt>D2d1.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e75e3-126"><dt>D2d1.dll</dt></span></span> </dl>                |



## <a name="see-also"></a><span data-ttu-id="e75e3-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e75e3-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e75e3-128">Collegamento Effect shader</span><span class="sxs-lookup"><span data-stu-id="e75e3-128">Effect Shader Linking</span></span>](effect-shader-linking.md)
</dt> <dt>

[<span data-ttu-id="e75e3-129">Helper HLSL</span><span class="sxs-lookup"><span data-stu-id="e75e3-129">HLSL Helpers</span></span>](hlsl-helpers.md)
</dt> </dl>

 

 





