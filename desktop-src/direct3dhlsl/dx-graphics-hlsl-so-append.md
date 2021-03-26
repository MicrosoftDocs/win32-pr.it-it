---
title: Append (oggetto Stream-Output DirectX HLSL)
description: Accodare i dati di output geometry-shader a un flusso esistente.
ms.assetid: 7df51383-7fc7-4a6f-aaa2-6c929f0443a3
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 97ab88961b22529accb4402fc2bd095ede5275c1
ms.sourcegitcommit: 477b1efe7d9c2f91d5f2ac588a20edf348b1c734
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/10/2019
ms.locfileid: "104335812"
---
# <a name="append-directx-hlsl-stream-output-object"></a><span data-ttu-id="343f4-103">Append (oggetto Stream-Output DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="343f4-103">Append (DirectX HLSL Stream-Output Object)</span></span>

<span data-ttu-id="343f4-104">Accodare i dati di output geometry-shader a un flusso esistente.</span><span class="sxs-lookup"><span data-stu-id="343f4-104">Append geometry-shader-output data to an existing stream.</span></span>



|                            |
|----------------------------|
| <span data-ttu-id="343f4-105">Append ( *StreamDataType*);</span><span class="sxs-lookup"><span data-stu-id="343f4-105">Append( *StreamDataType*);</span></span> |



 

## <a name="parameters"></a><span data-ttu-id="343f4-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="343f4-106">Parameters</span></span>



| <span data-ttu-id="343f4-107">Elemento</span><span class="sxs-lookup"><span data-stu-id="343f4-107">Item</span></span>                                                                                                                             | <span data-ttu-id="343f4-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="343f4-108">Description</span></span>                                                                                                                                            |
|----------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="343f4-109"><span id="StreamDataType"></span><span id="streamdatatype"></span><span id="STREAMDATATYPE"></span>**StreamDataType**</span><span class="sxs-lookup"><span data-stu-id="343f4-109"><span id="StreamDataType"></span><span id="streamdatatype"></span><span id="STREAMDATATYPE"></span>**StreamDataType**</span></span><br/> | <span data-ttu-id="343f4-110">Descrizione dell'input di dati.</span><span class="sxs-lookup"><span data-stu-id="343f4-110">A data input description.</span></span> <span data-ttu-id="343f4-111">Questa descrizione deve corrispondere al parametro del modello di oggetto Stream denominato [DataType](dx-graphics-hlsl-so-type.md).</span><span class="sxs-lookup"><span data-stu-id="343f4-111">This description must match the stream-object template parameter called [DataType](dx-graphics-hlsl-so-type.md).</span></span><br/> |



 

## <a name="return-value"></a><span data-ttu-id="343f4-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="343f4-112">Return Value</span></span>

<span data-ttu-id="343f4-113">nessuno</span><span class="sxs-lookup"><span data-stu-id="343f4-113">None</span></span>

## <a name="example"></a><span data-ttu-id="343f4-114">Esempio</span><span class="sxs-lookup"><span data-stu-id="343f4-114">Example</span></span>

<span data-ttu-id="343f4-115">Questo frammento di codice (dell' [esempio CubeMapGS](https://msdn.microsoft.com/library/Ee416398(v=VS.85).aspx)) Mostra un esempio parziale di aggiunta di primitive di striping a un oggetto Stream-output.</span><span class="sxs-lookup"><span data-stu-id="343f4-115">This code snippet (from the [CubeMapGS Sample](https://msdn.microsoft.com/library/Ee416398(v=VS.85).aspx)) shows a partial example of appending triangle strip primitives to a stream-output object.</span></span>


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



## <a name="minimum-shader-model"></a><span data-ttu-id="343f4-116">Modello Shader minimo</span><span class="sxs-lookup"><span data-stu-id="343f4-116">Minimum Shader Model</span></span>

<span data-ttu-id="343f4-117">Questa funzione è supportata nei modelli shader seguenti.</span><span class="sxs-lookup"><span data-stu-id="343f4-117">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="343f4-118">Modello di shader</span><span class="sxs-lookup"><span data-stu-id="343f4-118">Shader Model</span></span>                                              | <span data-ttu-id="343f4-119">Supportato</span><span class="sxs-lookup"><span data-stu-id="343f4-119">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="343f4-120">Modello Shader 4</span><span class="sxs-lookup"><span data-stu-id="343f4-120">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="343f4-121">sì</span><span class="sxs-lookup"><span data-stu-id="343f4-121">yes</span></span>       |
| [<span data-ttu-id="343f4-122">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="343f4-122">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="343f4-123">no</span><span class="sxs-lookup"><span data-stu-id="343f4-123">no</span></span>        |
| [<span data-ttu-id="343f4-124">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="343f4-124">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="343f4-125">no</span><span class="sxs-lookup"><span data-stu-id="343f4-125">no</span></span>        |
| [<span data-ttu-id="343f4-126">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="343f4-126">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="343f4-127">no</span><span class="sxs-lookup"><span data-stu-id="343f4-127">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="343f4-128">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="343f4-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="343f4-129">Stream-oggetto di output</span><span class="sxs-lookup"><span data-stu-id="343f4-129">Stream-Output Object</span></span>](dx-graphics-hlsl-so-type.md)
</dt> </dl>

 

 





