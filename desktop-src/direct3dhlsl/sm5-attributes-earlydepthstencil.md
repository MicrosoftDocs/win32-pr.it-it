---
title: earlydepthstencil
description: Forza i test di stencil Depth prima dell'esecuzione di uno shader.
ms.assetid: f8a9fee7-4a8a-4a34-bf7c-56906592caac
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: a7dd8507986970f2066538cc00b53af08807910e
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/20/2019
ms.locfileid: "104993184"
---
# <a name="earlydepthstencil"></a><span data-ttu-id="fafcb-103">earlydepthstencil</span><span class="sxs-lookup"><span data-stu-id="fafcb-103">earlydepthstencil</span></span>

<span data-ttu-id="fafcb-104">Forza i test di stencil Depth prima dell'esecuzione di uno shader.</span><span class="sxs-lookup"><span data-stu-id="fafcb-104">Forces depth-stencil testing before a shader executes.</span></span>


```
earlydepthstencil   
```



## <a name="remarks"></a><span data-ttu-id="fafcb-105">Commenti</span><span class="sxs-lookup"><span data-stu-id="fafcb-105">Remarks</span></span>

<span data-ttu-id="fafcb-106">Il test di stencil depth viene in genere eseguito durante l'elaborazione dei pixel da un pixel shader.</span><span class="sxs-lookup"><span data-stu-id="fafcb-106">Depth-stencil testing is normally done during pixel processing by a pixel shader.</span></span> <span data-ttu-id="fafcb-107">La forzatura del test di stencil di profondità anticipato fa sì che il test venga eseguito prima dell'esecuzione dello shader. lo scopo è quello di migliorare le prestazioni per pixel mediante l'abbattimento/riduzione/evitare l'elaborazione di pixel superflui.</span><span class="sxs-lookup"><span data-stu-id="fafcb-107">Forcing early depth-stencil testing causes the testing to be done prior to the shader execution; the purpose is to improve per-pixel performance by culling/reducing/avoiding unnecessary pixel processing.</span></span>

<span data-ttu-id="fafcb-108">Un'applicazione può forzare il testing dello stencil di profondità anticipato fornendo l'attributo o l'hardware può eseguire il test di stencil Depth prima che non venga scritto alcun valore di profondità e non vengono eseguite operazioni di accesso non ordinate in uno shader come ottimizzazione.</span><span class="sxs-lookup"><span data-stu-id="fafcb-108">An application can force early depth-stencil testing by supplying the attribute or the hardware may execute early depth-stencil testing provided no depth values are written and no unordered access operations are performed in a shader as an optimization.</span></span>

<span data-ttu-id="fafcb-109">Questo attributo è supportato nei tipi di shader seguenti:</span><span class="sxs-lookup"><span data-stu-id="fafcb-109">This attribute is supported in the following types of shaders:</span></span>



| <span data-ttu-id="fafcb-110">Vertice</span><span class="sxs-lookup"><span data-stu-id="fafcb-110">Vertex</span></span> | <span data-ttu-id="fafcb-111">Hull</span><span class="sxs-lookup"><span data-stu-id="fafcb-111">Hull</span></span> | <span data-ttu-id="fafcb-112">Dominio</span><span class="sxs-lookup"><span data-stu-id="fafcb-112">Domain</span></span> | <span data-ttu-id="fafcb-113">Geometria</span><span class="sxs-lookup"><span data-stu-id="fafcb-113">Geometry</span></span> | <span data-ttu-id="fafcb-114">Pixel</span><span class="sxs-lookup"><span data-stu-id="fafcb-114">Pixel</span></span> | <span data-ttu-id="fafcb-115">Calcolo</span><span class="sxs-lookup"><span data-stu-id="fafcb-115">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | <span data-ttu-id="fafcb-116">x</span><span class="sxs-lookup"><span data-stu-id="fafcb-116">x</span></span>     |         |



 

## <a name="related-topics"></a><span data-ttu-id="fafcb-117">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="fafcb-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fafcb-118">Attributi del modello di shader 5</span><span class="sxs-lookup"><span data-stu-id="fafcb-118">Shader Model 5 Attributes</span></span>](d3d11-graphics-reference-sm5-attributes.md)
</dt> <dt>

[<span data-ttu-id="fafcb-119">Modello Shader 5</span><span class="sxs-lookup"><span data-stu-id="fafcb-119">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




