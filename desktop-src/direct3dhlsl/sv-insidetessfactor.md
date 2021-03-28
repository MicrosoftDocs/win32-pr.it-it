---
title: SV_InsideTessFactor
description: Definisce l'importo a mosaico all'interno di una superficie della patch.
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
ms.openlocfilehash: 4a05cabbb9410136d2bd82ee272ad92ff1b1f430
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/25/2019
ms.locfileid: "104976210"
---
# <a name="sv_insidetessfactor"></a><span data-ttu-id="d2bbd-104">\_INSIDETESSFACTOR SV</span><span class="sxs-lookup"><span data-stu-id="d2bbd-104">SV\_InsideTessFactor</span></span>

<span data-ttu-id="d2bbd-105">Definisce l'importo a mosaico all'interno di una superficie della patch.</span><span class="sxs-lookup"><span data-stu-id="d2bbd-105">Defines the tessellation amount within a patch surface.</span></span>

## <a name="type"></a><span data-ttu-id="d2bbd-106">Tipo</span><span class="sxs-lookup"><span data-stu-id="d2bbd-106">Type</span></span>



|            |                |
|------------|----------------|
| <span data-ttu-id="d2bbd-107">Tipo</span><span class="sxs-lookup"><span data-stu-id="d2bbd-107">Type</span></span>       | <span data-ttu-id="d2bbd-108">Topologia di input</span><span class="sxs-lookup"><span data-stu-id="d2bbd-108">Input Topology</span></span> |
| <span data-ttu-id="d2bbd-109">float \[ 2\]</span><span class="sxs-lookup"><span data-stu-id="d2bbd-109">float\[2\]</span></span> | <span data-ttu-id="d2bbd-110">patch quad</span><span class="sxs-lookup"><span data-stu-id="d2bbd-110">quad patch</span></span>     |
| <span data-ttu-id="d2bbd-111">float</span><span class="sxs-lookup"><span data-stu-id="d2bbd-111">float</span></span>      | <span data-ttu-id="d2bbd-112">patch Tri</span><span class="sxs-lookup"><span data-stu-id="d2bbd-112">tri patch</span></span>      |
| <span data-ttu-id="d2bbd-113">unused</span><span class="sxs-lookup"><span data-stu-id="d2bbd-113">unused</span></span>     | <span data-ttu-id="d2bbd-114">isolinea</span><span class="sxs-lookup"><span data-stu-id="d2bbd-114">isoline</span></span>        |



 

<span data-ttu-id="d2bbd-115">I fattori a mosaico devono essere dichiarati come matrici; non possono essere compressi in un singolo vettore.</span><span class="sxs-lookup"><span data-stu-id="d2bbd-115">Tessellation factors must be declared as array; they cannot be packed into a single vector.</span></span>

## <a name="remarks"></a><span data-ttu-id="d2bbd-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="d2bbd-116">Remarks</span></span>

<span data-ttu-id="d2bbd-117">Questo valore deve essere definito durante la funzione costante patch dello scafo shader.</span><span class="sxs-lookup"><span data-stu-id="d2bbd-117">This value must be defined during the patch constant function of the hull shader.</span></span>

<span data-ttu-id="d2bbd-118">Valore di output necessario per Hull shader se si usano patch quad o tri.</span><span class="sxs-lookup"><span data-stu-id="d2bbd-118">Required output value for the hull shader if using quad or tri patches.</span></span> <span data-ttu-id="d2bbd-119">Questo valore è un input obbligatorio per lo shader del dominio in modo che l'hardware corrisponda alle firme tramite il mosaico.</span><span class="sxs-lookup"><span data-stu-id="d2bbd-119">This value is a required input for the domain shader in order for hardware to match the signatures through the tessellator.</span></span>

<span data-ttu-id="d2bbd-120">Questa funzione è supportata nei tipi di shader seguenti:</span><span class="sxs-lookup"><span data-stu-id="d2bbd-120">This function is supported in the following types of shaders:</span></span>



|        |      |        |          |       |         |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="d2bbd-121">Vertice</span><span class="sxs-lookup"><span data-stu-id="d2bbd-121">Vertex</span></span> | <span data-ttu-id="d2bbd-122">Hull</span><span class="sxs-lookup"><span data-stu-id="d2bbd-122">Hull</span></span> | <span data-ttu-id="d2bbd-123">Dominio</span><span class="sxs-lookup"><span data-stu-id="d2bbd-123">Domain</span></span> | <span data-ttu-id="d2bbd-124">Geometria</span><span class="sxs-lookup"><span data-stu-id="d2bbd-124">Geometry</span></span> | <span data-ttu-id="d2bbd-125">Pixel</span><span class="sxs-lookup"><span data-stu-id="d2bbd-125">Pixel</span></span> | <span data-ttu-id="d2bbd-126">Calcolo</span><span class="sxs-lookup"><span data-stu-id="d2bbd-126">Compute</span></span> |
|        | <span data-ttu-id="d2bbd-127">x</span><span class="sxs-lookup"><span data-stu-id="d2bbd-127">x</span></span>    | <span data-ttu-id="d2bbd-128">x</span><span class="sxs-lookup"><span data-stu-id="d2bbd-128">x</span></span>      |          |       |         |



 

## <a name="see-also"></a><span data-ttu-id="d2bbd-129">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="d2bbd-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d2bbd-130">Semantica</span><span class="sxs-lookup"><span data-stu-id="d2bbd-130">Semantics</span></span>](dx-graphics-hlsl-semantics.md)
</dt> <dt>

[<span data-ttu-id="d2bbd-131">Modello Shader 5</span><span class="sxs-lookup"><span data-stu-id="d2bbd-131">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




