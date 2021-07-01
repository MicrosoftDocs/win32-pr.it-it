---
title: Append (oggetto Stream-Output DirectX HLSL)
description: Aggiungere dati di output geometry shader a un flusso esistente.
ms.assetid: 7df51383-7fc7-4a6f-aaa2-6c929f0443a3
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 19d767f3c501cc42e21bbc44a196ba08cd6f1883
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/30/2021
ms.locfileid: "113120186"
---
# <a name="append-directx-hlsl-stream-output-object"></a><span data-ttu-id="ada41-103">Append (oggetto Stream-Output DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="ada41-103">Append (DirectX HLSL Stream-Output Object)</span></span>

<span data-ttu-id="ada41-104">Aggiungere dati di output geometry shader a un flusso esistente.</span><span class="sxs-lookup"><span data-stu-id="ada41-104">Append geometry-shader-output data to an existing stream.</span></span>

<span data-ttu-id="ada41-105">Append( *StreamDataType*);</span><span class="sxs-lookup"><span data-stu-id="ada41-105">Append( *StreamDataType*);</span></span>



 

## <a name="parameters"></a><span data-ttu-id="ada41-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="ada41-106">Parameters</span></span>



| <span data-ttu-id="ada41-107">Elemento</span><span class="sxs-lookup"><span data-stu-id="ada41-107">Item</span></span>                                                                                                                             | <span data-ttu-id="ada41-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ada41-108">Description</span></span>                                                                                                                                            |
|----------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ada41-109"><span id="StreamDataType"></span><span id="streamdatatype"></span><span id="STREAMDATATYPE"></span>**StreamDataType**</span><span class="sxs-lookup"><span data-stu-id="ada41-109"><span id="StreamDataType"></span><span id="streamdatatype"></span><span id="STREAMDATATYPE"></span>**StreamDataType**</span></span><br/> | <span data-ttu-id="ada41-110">Descrizione dell'input di dati.</span><span class="sxs-lookup"><span data-stu-id="ada41-110">A data input description.</span></span> <span data-ttu-id="ada41-111">Questa descrizione deve corrispondere al parametro del modello stream-object denominato [DataType](dx-graphics-hlsl-so-type.md).</span><span class="sxs-lookup"><span data-stu-id="ada41-111">This description must match the stream-object template parameter called [DataType](dx-graphics-hlsl-so-type.md).</span></span><br/> |



 

## <a name="return-value"></a><span data-ttu-id="ada41-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="ada41-112">Return Value</span></span>

<span data-ttu-id="ada41-113">nessuno</span><span class="sxs-lookup"><span data-stu-id="ada41-113">None</span></span>

## <a name="example"></a><span data-ttu-id="ada41-114">Esempio</span><span class="sxs-lookup"><span data-stu-id="ada41-114">Example</span></span>

<span data-ttu-id="ada41-115">Questo frammento di codice (dall'esempio [CubeMapGS)](https://msdn.microsoft.com/library/Ee416398(v=VS.85).aspx)illustra un esempio parziale di aggiunta di primitive di striscia triangolare a un oggetto di output del flusso.</span><span class="sxs-lookup"><span data-stu-id="ada41-115">This code snippet (from the [CubeMapGS Sample](https://msdn.microsoft.com/library/Ee416398(v=VS.85).aspx)) shows a partial example of appending triangle strip primitives to a stream-output object.</span></span>


```
[maxvertexcount(18)]
void GS_CubeMap( triangle GS_CUBEMAP_IN input[3], 
                 inout TriangleStream<PS_CUBEMAP_IN> CubeMapStream )
{
    for( int f = 0; f < 6; ++f )
    {
        // Compute screen coordinates
        PS_CUBEMAP_IN output;
        output.RTIndex = f;
        for( int v = 0; v < 3; v++ )
        {
            output.Pos = mul( input[v].Pos, g_mViewCM[f] );
            output.Pos = mul( output.Pos, mProj );
            output.Tex = input[v].Tex;
            CubeMapStream.Append( output );
        }
        CubeMapStream.RestartStrip();
    }
}
```



## <a name="minimum-shader-model"></a><span data-ttu-id="ada41-116">Modello di shader minimo</span><span class="sxs-lookup"><span data-stu-id="ada41-116">Minimum Shader Model</span></span>

<span data-ttu-id="ada41-117">Questa funzione è supportata nei modelli di shader seguenti.</span><span class="sxs-lookup"><span data-stu-id="ada41-117">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="ada41-118">Modello di shader</span><span class="sxs-lookup"><span data-stu-id="ada41-118">Shader Model</span></span>                                              | <span data-ttu-id="ada41-119">Supportato</span><span class="sxs-lookup"><span data-stu-id="ada41-119">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="ada41-120">Modello shader 4</span><span class="sxs-lookup"><span data-stu-id="ada41-120">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="ada41-121">yes</span><span class="sxs-lookup"><span data-stu-id="ada41-121">yes</span></span>       |
| [<span data-ttu-id="ada41-122">Modello shader 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="ada41-122">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="ada41-123">No</span><span class="sxs-lookup"><span data-stu-id="ada41-123">no</span></span>        |
| [<span data-ttu-id="ada41-124">Modello shader 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="ada41-124">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="ada41-125">No</span><span class="sxs-lookup"><span data-stu-id="ada41-125">no</span></span>        |
| [<span data-ttu-id="ada41-126">Modello shader 1 (HLSL DirectX)</span><span class="sxs-lookup"><span data-stu-id="ada41-126">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="ada41-127">No</span><span class="sxs-lookup"><span data-stu-id="ada41-127">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="ada41-128">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="ada41-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ada41-129">Oggetto Stream-Output</span><span class="sxs-lookup"><span data-stu-id="ada41-129">Stream-Output Object</span></span>](dx-graphics-hlsl-so-type.md)
</dt> </dl>

 

 





