---
title: maxtessfactor
description: Indica il valore massimo che lo scafo shader restituisce per qualsiasi fattore di mosaico.
ms.assetid: 2c12ed56-cd64-4143-8dda-6998aa212356
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 261ab17bd40c24c19b4b929f2e8307ccc6bb9b56
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/20/2019
ms.locfileid: "103857793"
---
# <a name="maxtessfactor"></a><span data-ttu-id="59638-103">maxtessfactor</span><span class="sxs-lookup"><span data-stu-id="59638-103">maxtessfactor</span></span>

<span data-ttu-id="59638-104">Indica il valore massimo che lo scafo shader restituisce per qualsiasi fattore di mosaico.</span><span class="sxs-lookup"><span data-stu-id="59638-104">Indicates the maximum value that the hull shader would return for any tessellation factor.</span></span>


```
maxtessfactor(X)   
```



## <a name="remarks"></a><span data-ttu-id="59638-105">Commenti</span><span class="sxs-lookup"><span data-stu-id="59638-105">Remarks</span></span>

<span data-ttu-id="59638-106">Questo attributo impone un limite superiore per la quantità di mosaico richiesto per aiutare un driver a determinare la quantità massima di risorse necessarie per lo schema a mosaico.</span><span class="sxs-lookup"><span data-stu-id="59638-106">This attribute puts an upper bound on the amount of tessellation requested to help a driver determine the maximum amount of resources required for tessellation.</span></span>

<span data-ttu-id="59638-107">Questo attributo è supportato nei tipi di shader seguenti:</span><span class="sxs-lookup"><span data-stu-id="59638-107">This attribute is supported in the following types of shaders:</span></span>



| <span data-ttu-id="59638-108">Vertice</span><span class="sxs-lookup"><span data-stu-id="59638-108">Vertex</span></span> | <span data-ttu-id="59638-109">Hull</span><span class="sxs-lookup"><span data-stu-id="59638-109">Hull</span></span> | <span data-ttu-id="59638-110">Dominio</span><span class="sxs-lookup"><span data-stu-id="59638-110">Domain</span></span> | <span data-ttu-id="59638-111">Geometria</span><span class="sxs-lookup"><span data-stu-id="59638-111">Geometry</span></span> | <span data-ttu-id="59638-112">Pixel</span><span class="sxs-lookup"><span data-stu-id="59638-112">Pixel</span></span> | <span data-ttu-id="59638-113">Calcolo</span><span class="sxs-lookup"><span data-stu-id="59638-113">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        | <span data-ttu-id="59638-114">x</span><span class="sxs-lookup"><span data-stu-id="59638-114">x</span></span>    |        |          |       |         |



 

## <a name="related-topics"></a><span data-ttu-id="59638-115">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="59638-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="59638-116">Attributi del modello di shader 5</span><span class="sxs-lookup"><span data-stu-id="59638-116">Shader Model 5 Attributes</span></span>](d3d11-graphics-reference-sm5-attributes.md)
</dt> <dt>

[<span data-ttu-id="59638-117">Modello Shader 5</span><span class="sxs-lookup"><span data-stu-id="59638-117">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




