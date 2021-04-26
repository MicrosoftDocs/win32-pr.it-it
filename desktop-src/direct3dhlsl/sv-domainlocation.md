---
title: SV_DomainLocation
description: Definisce la posizione sullo scafo del punto di dominio corrente da valutare.
ms.assetid: 907f568c-7c45-41e5-96c4-6e6b816a4a53
keywords:
- SV_DomainLocation HLSL
topic_type:
- apiref
api_name:
- SV_DomainLocation
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: cb9265734663881981f1626db6e23c6b7dd9415a
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/26/2021
ms.locfileid: "107996508"
---
# <a name="sv_domainlocation"></a><span data-ttu-id="15177-104">SV \_ DomainLocation</span><span class="sxs-lookup"><span data-stu-id="15177-104">SV\_DomainLocation</span></span>

<span data-ttu-id="15177-105">Definisce la posizione sullo scafo del punto di dominio corrente da valutare.</span><span class="sxs-lookup"><span data-stu-id="15177-105">Defines the location on the hull of the current domain point being evaluated.</span></span>

## <a name="type"></a><span data-ttu-id="15177-106">Tipo</span><span class="sxs-lookup"><span data-stu-id="15177-106">Type</span></span>



|        |                |
|--------|----------------|
| <span data-ttu-id="15177-107">Tipo</span><span class="sxs-lookup"><span data-stu-id="15177-107">Type</span></span>   | <span data-ttu-id="15177-108">Topologia di input</span><span class="sxs-lookup"><span data-stu-id="15177-108">Input Topology</span></span> |
| <span data-ttu-id="15177-109">float2</span><span class="sxs-lookup"><span data-stu-id="15177-109">float2</span></span> | <span data-ttu-id="15177-110">quad patch</span><span class="sxs-lookup"><span data-stu-id="15177-110">quad patch</span></span>     |
| <span data-ttu-id="15177-111">float3</span><span class="sxs-lookup"><span data-stu-id="15177-111">float3</span></span> | <span data-ttu-id="15177-112">tri patch</span><span class="sxs-lookup"><span data-stu-id="15177-112">tri patch</span></span>      |
| <span data-ttu-id="15177-113">float2</span><span class="sxs-lookup"><span data-stu-id="15177-113">float2</span></span> | <span data-ttu-id="15177-114">isoline</span><span class="sxs-lookup"><span data-stu-id="15177-114">isoline</span></span>        |



 

## <a name="remarks"></a><span data-ttu-id="15177-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="15177-115">Remarks</span></span>

<span data-ttu-id="15177-116">Questo valore di sistema è obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="15177-116">This system value is required.</span></span>

<span data-ttu-id="15177-117">Questa funzione è supportata nei tipi di shader seguenti:</span><span class="sxs-lookup"><span data-stu-id="15177-117">This function is supported in the following types of shaders:</span></span>



| <span data-ttu-id="15177-118">Vertice</span><span class="sxs-lookup"><span data-stu-id="15177-118">Vertex</span></span> | <span data-ttu-id="15177-119">Scafo</span><span class="sxs-lookup"><span data-stu-id="15177-119">Hull</span></span> | <span data-ttu-id="15177-120">Dominio</span><span class="sxs-lookup"><span data-stu-id="15177-120">Domain</span></span> | <span data-ttu-id="15177-121">Geometria</span><span class="sxs-lookup"><span data-stu-id="15177-121">Geometry</span></span> | <span data-ttu-id="15177-122">Pixel</span><span class="sxs-lookup"><span data-stu-id="15177-122">Pixel</span></span> | <span data-ttu-id="15177-123">Calcolo</span><span class="sxs-lookup"><span data-stu-id="15177-123">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      | <span data-ttu-id="15177-124">x</span><span class="sxs-lookup"><span data-stu-id="15177-124">x</span></span>      |          |       |         |



 

## <a name="see-also"></a><span data-ttu-id="15177-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="15177-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="15177-126">Semantica</span><span class="sxs-lookup"><span data-stu-id="15177-126">Semantics</span></span>](dx-graphics-hlsl-semantics.md)
</dt> <dt>

[<span data-ttu-id="15177-127">Modello shader 5</span><span class="sxs-lookup"><span data-stu-id="15177-127">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




