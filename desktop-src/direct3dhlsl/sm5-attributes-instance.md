---
title: instance
description: Usare questo attributo per l'istanza di un geometry shader.
ms.assetid: 0e487e52-53d0-4193-99b2-fd018a061b42
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 4749e11db00b38e5e223e11315de86656b2f6488
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/20/2019
ms.locfileid: "104046105"
---
# <a name="instance"></a><span data-ttu-id="b16fe-103">instance</span><span class="sxs-lookup"><span data-stu-id="b16fe-103">instance</span></span>

<span data-ttu-id="b16fe-104">Usare questo attributo per l'istanza di un geometry shader.</span><span class="sxs-lookup"><span data-stu-id="b16fe-104">Use this attribute to instance a geometry shader.</span></span>


```
instance(X)   
```



## <a name="remarks"></a><span data-ttu-id="b16fe-105">Commenti</span><span class="sxs-lookup"><span data-stu-id="b16fe-105">Remarks</span></span>

<span data-ttu-id="b16fe-106">X è un indice Integer che indica il numero di istanze da eseguire per ogni elemento disegnato, ad esempio per ogni triangolo.</span><span class="sxs-lookup"><span data-stu-id="b16fe-106">X is an integer index that indicates the number of instances to be executed for each drawn item (for example, for each triangle).</span></span> <span data-ttu-id="b16fe-107">Quando si usa questo attributo, usare [SV \_ GSInstanceID](sv-gsinstanceid.md) per identificare l'istanza di Geometry shader in esecuzione.</span><span class="sxs-lookup"><span data-stu-id="b16fe-107">When using this attribute, use [SV\_GSInstanceID](sv-gsinstanceid.md) to identify which instance of a geometry shader is being executed.</span></span>

<span data-ttu-id="b16fe-108">Questo attributo è supportato nei tipi di shader seguenti:</span><span class="sxs-lookup"><span data-stu-id="b16fe-108">This attribute is supported in the following types of shaders:</span></span>



| <span data-ttu-id="b16fe-109">Vertice</span><span class="sxs-lookup"><span data-stu-id="b16fe-109">Vertex</span></span> | <span data-ttu-id="b16fe-110">Hull</span><span class="sxs-lookup"><span data-stu-id="b16fe-110">Hull</span></span> | <span data-ttu-id="b16fe-111">Dominio</span><span class="sxs-lookup"><span data-stu-id="b16fe-111">Domain</span></span> | <span data-ttu-id="b16fe-112">Geometria</span><span class="sxs-lookup"><span data-stu-id="b16fe-112">Geometry</span></span> | <span data-ttu-id="b16fe-113">Pixel</span><span class="sxs-lookup"><span data-stu-id="b16fe-113">Pixel</span></span> | <span data-ttu-id="b16fe-114">Calcolo</span><span class="sxs-lookup"><span data-stu-id="b16fe-114">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        | <span data-ttu-id="b16fe-115">x</span><span class="sxs-lookup"><span data-stu-id="b16fe-115">x</span></span>        |       |         |



 

## <a name="related-topics"></a><span data-ttu-id="b16fe-116">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="b16fe-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b16fe-117">Attributi del modello di shader 5</span><span class="sxs-lookup"><span data-stu-id="b16fe-117">Shader Model 5 Attributes</span></span>](d3d11-graphics-reference-sm5-attributes.md)
</dt> <dt>

[<span data-ttu-id="b16fe-118">Modello Shader 5</span><span class="sxs-lookup"><span data-stu-id="b16fe-118">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




