---
title: SV_InsideTessFactor
description: Definisce la quantità a tessellazione all'interno di una superficie patch.
ms.assetid: f0762aca-d84d-44c0-a163-9737ef92c1e5
keywords:
- SV_InsideTessFactor HLSL
topic_type:
- apiref
api_name:
- SV_InsideTessFactor
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 4d047f7961868de020ac50ffce22b6ce02d078a5
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/26/2021
ms.locfileid: "107996918"
---
# <a name="sv_insidetessfactor"></a><span data-ttu-id="01418-104">SV \_ InsideTessFactor</span><span class="sxs-lookup"><span data-stu-id="01418-104">SV\_InsideTessFactor</span></span>

<span data-ttu-id="01418-105">Definisce la quantità a tessellazione all'interno di una superficie patch.</span><span class="sxs-lookup"><span data-stu-id="01418-105">Defines the tessellation amount within a patch surface.</span></span>

## <a name="type"></a><span data-ttu-id="01418-106">Tipo</span><span class="sxs-lookup"><span data-stu-id="01418-106">Type</span></span>



|            |                |
|------------|----------------|
| <span data-ttu-id="01418-107">Tipo</span><span class="sxs-lookup"><span data-stu-id="01418-107">Type</span></span>       | <span data-ttu-id="01418-108">Topologia di input</span><span class="sxs-lookup"><span data-stu-id="01418-108">Input Topology</span></span> |
| <span data-ttu-id="01418-109">float \[ 2\]</span><span class="sxs-lookup"><span data-stu-id="01418-109">float\[2\]</span></span> | <span data-ttu-id="01418-110">quad patch</span><span class="sxs-lookup"><span data-stu-id="01418-110">quad patch</span></span>     |
| <span data-ttu-id="01418-111">float</span><span class="sxs-lookup"><span data-stu-id="01418-111">float</span></span>      | <span data-ttu-id="01418-112">tri patch</span><span class="sxs-lookup"><span data-stu-id="01418-112">tri patch</span></span>      |
| <span data-ttu-id="01418-113">unused</span><span class="sxs-lookup"><span data-stu-id="01418-113">unused</span></span>     | <span data-ttu-id="01418-114">isoline</span><span class="sxs-lookup"><span data-stu-id="01418-114">isoline</span></span>        |



 

<span data-ttu-id="01418-115">I fattori a tessellazione devono essere dichiarati come matrice. non possono essere suddivisi in un singolo vettore.</span><span class="sxs-lookup"><span data-stu-id="01418-115">Tessellation factors must be declared as array; they cannot be packed into a single vector.</span></span>

## <a name="remarks"></a><span data-ttu-id="01418-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="01418-116">Remarks</span></span>

<span data-ttu-id="01418-117">Questo valore deve essere definito durante la funzione costante patch dello hull shader.</span><span class="sxs-lookup"><span data-stu-id="01418-117">This value must be defined during the patch constant function of the hull shader.</span></span>

<span data-ttu-id="01418-118">Valore di output obbligatorio per lo hull shader se si usano patch quad o tri.</span><span class="sxs-lookup"><span data-stu-id="01418-118">Required output value for the hull shader if using quad or tri patches.</span></span> <span data-ttu-id="01418-119">Questo valore è un input obbligatorio per lo shader del dominio in modo che l'hardware corrisponda alle firme tramite il tessellatore.</span><span class="sxs-lookup"><span data-stu-id="01418-119">This value is a required input for the domain shader in order for hardware to match the signatures through the tessellator.</span></span>

<span data-ttu-id="01418-120">Questa funzione è supportata nei tipi di shader seguenti:</span><span class="sxs-lookup"><span data-stu-id="01418-120">This function is supported in the following types of shaders:</span></span>



| <span data-ttu-id="01418-121">Vertice</span><span class="sxs-lookup"><span data-stu-id="01418-121">Vertex</span></span> | <span data-ttu-id="01418-122">Scafo</span><span class="sxs-lookup"><span data-stu-id="01418-122">Hull</span></span> | <span data-ttu-id="01418-123">Dominio</span><span class="sxs-lookup"><span data-stu-id="01418-123">Domain</span></span> | <span data-ttu-id="01418-124">Geometria</span><span class="sxs-lookup"><span data-stu-id="01418-124">Geometry</span></span> | <span data-ttu-id="01418-125">Pixel</span><span class="sxs-lookup"><span data-stu-id="01418-125">Pixel</span></span> | <span data-ttu-id="01418-126">Calcolo</span><span class="sxs-lookup"><span data-stu-id="01418-126">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        | <span data-ttu-id="01418-127">x</span><span class="sxs-lookup"><span data-stu-id="01418-127">x</span></span>    | <span data-ttu-id="01418-128">x</span><span class="sxs-lookup"><span data-stu-id="01418-128">x</span></span>      |          |       |         |



 

## <a name="see-also"></a><span data-ttu-id="01418-129">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="01418-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="01418-130">Semantica</span><span class="sxs-lookup"><span data-stu-id="01418-130">Semantics</span></span>](dx-graphics-hlsl-semantics.md)
</dt> <dt>

[<span data-ttu-id="01418-131">Modello shader 5</span><span class="sxs-lookup"><span data-stu-id="01418-131">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




