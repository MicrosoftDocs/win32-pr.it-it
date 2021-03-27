---
title: Tipo di trama
description: Per dichiarare una variabile di trama, usare la sintassi seguente.
ms.assetid: 54db5432-dab8-4a4d-a4de-93c6fa640535
keywords:
- Tipo di trama HLSL
topic_type:
- apiref
api_name:
- Texture type
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 89568dc5cf24af38f916375795eea052c8b39200
ms.sourcegitcommit: 6f905c836d3fd04934fb3e5f1a56b4a421f7596f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 05/07/2020
ms.locfileid: "103723983"
---
# <a name="texture-type"></a><span data-ttu-id="b1c27-104">Tipo di trama</span><span class="sxs-lookup"><span data-stu-id="b1c27-104">Texture type</span></span>

<span data-ttu-id="b1c27-105">Per dichiarare una variabile di trama, usare la sintassi seguente.</span><span class="sxs-lookup"><span data-stu-id="b1c27-105">Use the following syntax to declare a texture variable.</span></span>

|                |
|----------------|
| <span data-ttu-id="b1c27-106">**Nome tipo;**</span><span class="sxs-lookup"><span data-stu-id="b1c27-106">**Type Name;**</span></span> |

## <a name="parameters"></a><span data-ttu-id="b1c27-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="b1c27-107">Parameters</span></span>
| <span data-ttu-id="b1c27-108">Elemento</span><span class="sxs-lookup"><span data-stu-id="b1c27-108">Item</span></span>                                                                                     | <span data-ttu-id="b1c27-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b1c27-109">Description</span></span>                                                                                                                                                                                                              |
|------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b1c27-110"><span id="Type"></span><span id="type"></span><span id="TYPE"></span>**Tipo**</span><span class="sxs-lookup"><span data-stu-id="b1c27-110"><span id="Type"></span><span id="type"></span><span id="TYPE"></span>**Type**</span></span><br/> | <span data-ttu-id="b1c27-111">Uno dei tipi seguenti: texture (non tipizzata, per compatibilità con le versioni precedenti), Texture1D, Texture1DArray, Texture2D, Texture2DArray, Texture3D, TextureCube.</span><span class="sxs-lookup"><span data-stu-id="b1c27-111">One of the following types: texture (untyped, for backwards compatibility), Texture1D, Texture1DArray, Texture2D, Texture2DArray, Texture3D, TextureCube.</span></span> <span data-ttu-id="b1c27-112">Le dimensioni dell'elemento devono essere incluse in quantità a 4 32 bit.</span><span class="sxs-lookup"><span data-stu-id="b1c27-112">The element size must fit into 4 32-bit quantities.</span></span><br/> |
| <span data-ttu-id="b1c27-113"><span id="Name"></span><span id="name"></span><span id="NAME"></span>**Nome**</span><span class="sxs-lookup"><span data-stu-id="b1c27-113"><span id="Name"></span><span id="name"></span><span id="NAME"></span>**Name**</span></span><br/> | <span data-ttu-id="b1c27-114">Stringa ASCII che identifica in modo univoco il nome della variabile.</span><span class="sxs-lookup"><span data-stu-id="b1c27-114">An ASCII string that uniquely identifies the variable name.</span></span><br/>                                                                                                                                                   |
## <a name="remarks"></a><span data-ttu-id="b1c27-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="b1c27-115">Remarks</span></span>

<span data-ttu-id="b1c27-116">È possibile utilizzare una trama in tre parti.</span><span class="sxs-lookup"><span data-stu-id="b1c27-116">There are three parts to using a texture.</span></span>

1.  <span data-ttu-id="b1c27-117">Dichiarazione di una variabile di trama.</span><span class="sxs-lookup"><span data-stu-id="b1c27-117">Declaring a texture variable.</span></span> <span data-ttu-id="b1c27-118">Questa operazione viene eseguita con la sintassi illustrata in precedenza.</span><span class="sxs-lookup"><span data-stu-id="b1c27-118">This is done with the syntax shown above.</span></span> <span data-ttu-id="b1c27-119">Ad esempio, si tratta di dichiarazioni valide.</span><span class="sxs-lookup"><span data-stu-id="b1c27-119">For example, these are valid declarations.</span></span>

    ```
    texture g_MeshTexture;
    ```

    <span data-ttu-id="b1c27-120">\- - oppure -</span><span class="sxs-lookup"><span data-stu-id="b1c27-120">\- or -</span></span>

    ```
    Texture2D g_MeshTexture;
    ```

2.  <span data-ttu-id="b1c27-121">Dichiarazione e inizializzazione di un oggetto Sampler.</span><span class="sxs-lookup"><span data-stu-id="b1c27-121">Declaring and initializing a sampler object.</span></span> <span data-ttu-id="b1c27-122">Questa operazione viene eseguita con sintassi leggermente diversa in Direct3D 9 e Direct3D 10.</span><span class="sxs-lookup"><span data-stu-id="b1c27-122">This is done with slightly different syntax in Direct3D 9 and Direct3D 10.</span></span> <span data-ttu-id="b1c27-123">Per informazioni dettagliate sulla sintassi degli oggetti Sampler, vedere [Sampler Type (DirectX HLSL)](dx-graphics-hlsl-sampler.md).</span><span class="sxs-lookup"><span data-stu-id="b1c27-123">For details about sampler object syntax, see [Sampler Type (DirectX HLSL)](dx-graphics-hlsl-sampler.md).</span></span>
3.  <span data-ttu-id="b1c27-124">Richiamo di una funzione di trama in uno shader.</span><span class="sxs-lookup"><span data-stu-id="b1c27-124">Invoking a texture function in a shader.</span></span>

<span data-ttu-id="b1c27-125">Differenze tra Direct3D 9 e Direct3D 10:</span><span class="sxs-lookup"><span data-stu-id="b1c27-125">Differences between Direct3D 9 and Direct3D 10:</span></span>

<span data-ttu-id="b1c27-126">Direct3D 9 utilizza [funzioni di trama intrinseche](dx-graphics-hlsl-intrinsic-functions.md) per eseguire operazioni di trama.</span><span class="sxs-lookup"><span data-stu-id="b1c27-126">Direct3D 9 uses [intrinsic texture functions](dx-graphics-hlsl-intrinsic-functions.md) to perform texture operations.</span></span> <span data-ttu-id="b1c27-127">Questo esempio è relativo all' [esempio BasicHLSL](/previous-versions/windows/desktop/bb153287(v%3Dvs.85)) e USA [tex2D (s, t) (DirectX HLSL)](dx-graphics-hlsl-tex2d.md) per eseguire il campionamento della trama.</span><span class="sxs-lookup"><span data-stu-id="b1c27-127">This example is from the [BasicHLSL Sample](/previous-versions/windows/desktop/bb153287(v%3Dvs.85)) and uses [tex2D(s, t) (DirectX HLSL)](dx-graphics-hlsl-tex2d.md) to perform texture sampling.</span></span>

<code>Output.RGBColor = tex2D(MeshTextureSampler, In.TextureUV) * In.Diffuse;</code>

<span data-ttu-id="b1c27-128">Direct3D 10 usa invece [oggetti trama basati su modelli](dx-graphics-hlsl-to-type.md) .</span><span class="sxs-lookup"><span data-stu-id="b1c27-128">Direct3D 10 uses [templated texture objects](dx-graphics-hlsl-to-type.md) instead.</span></span> <span data-ttu-id="b1c27-129">Di seguito è riportato un esempio dell'operazione di trama equivalente.</span><span class="sxs-lookup"><span data-stu-id="b1c27-129">Here is an example of the equivalent texture operation.</span></span>

<code>Output.RGBColor = g_MeshTexture.Sample(MeshTextureSampler, In.TextureUV) * In.Diffuse;</code>

## <a name="see-also"></a><span data-ttu-id="b1c27-130">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="b1c27-130">See also</span></span>

[<span data-ttu-id="b1c27-131">Tipi di dati (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="b1c27-131">Data Types (DirectX HLSL)</span></span>](dx-graphics-hlsl-data-types.md)
