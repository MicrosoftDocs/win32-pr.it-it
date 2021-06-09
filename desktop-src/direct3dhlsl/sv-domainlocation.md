---
title: SV_DomainLocation
description: Definisce la posizione sulla scafo del punto di dominio corrente da valutare.
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
ms.openlocfilehash: fc39a71bcbfb6f3719ecfc7d0abe463a1fd127e4
ms.sourcegitcommit: adba238660d8a5f4fe98fc6f5d105d56aac3a400
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/09/2021
ms.locfileid: "111827050"
---
# <a name="sv_domainlocation"></a><span data-ttu-id="884a9-104">SV \_ DomainLocation</span><span class="sxs-lookup"><span data-stu-id="884a9-104">SV\_DomainLocation</span></span>

<span data-ttu-id="884a9-105">Definisce la posizione sulla scafo del punto di dominio corrente da valutare.</span><span class="sxs-lookup"><span data-stu-id="884a9-105">Defines the location on the hull of the current domain point being evaluated.</span></span>

## <a name="type"></a><span data-ttu-id="884a9-106">Tipo</span><span class="sxs-lookup"><span data-stu-id="884a9-106">Type</span></span>



| <span data-ttu-id="884a9-107">Tipo</span><span class="sxs-lookup"><span data-stu-id="884a9-107">Type</span></span>       | <span data-ttu-id="884a9-108">Topologia di input</span><span class="sxs-lookup"><span data-stu-id="884a9-108">Input topology</span></span>               |
|--------|----------------|
| <span data-ttu-id="884a9-109">float2</span><span class="sxs-lookup"><span data-stu-id="884a9-109">float2</span></span> | <span data-ttu-id="884a9-110">quad patch</span><span class="sxs-lookup"><span data-stu-id="884a9-110">quad patch</span></span>     |
| <span data-ttu-id="884a9-111">float3</span><span class="sxs-lookup"><span data-stu-id="884a9-111">float3</span></span> | <span data-ttu-id="884a9-112">tri patch</span><span class="sxs-lookup"><span data-stu-id="884a9-112">tri patch</span></span>      |
| <span data-ttu-id="884a9-113">float2</span><span class="sxs-lookup"><span data-stu-id="884a9-113">float2</span></span> | <span data-ttu-id="884a9-114">isoline</span><span class="sxs-lookup"><span data-stu-id="884a9-114">isoline</span></span>        |



 

## <a name="remarks"></a><span data-ttu-id="884a9-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="884a9-115">Remarks</span></span>

<span data-ttu-id="884a9-116">Questo valore di sistema è obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="884a9-116">This system value is required.</span></span>

<span data-ttu-id="884a9-117">Questa funzione è supportata nei tipi di shader seguenti:</span><span class="sxs-lookup"><span data-stu-id="884a9-117">This function is supported in the following types of shaders:</span></span>



| <span data-ttu-id="884a9-118">Vertice</span><span class="sxs-lookup"><span data-stu-id="884a9-118">Vertex</span></span> | <span data-ttu-id="884a9-119">Scafo</span><span class="sxs-lookup"><span data-stu-id="884a9-119">Hull</span></span> | <span data-ttu-id="884a9-120">Dominio</span><span class="sxs-lookup"><span data-stu-id="884a9-120">Domain</span></span> | <span data-ttu-id="884a9-121">Geometria</span><span class="sxs-lookup"><span data-stu-id="884a9-121">Geometry</span></span> | <span data-ttu-id="884a9-122">Pixel</span><span class="sxs-lookup"><span data-stu-id="884a9-122">Pixel</span></span> | <span data-ttu-id="884a9-123">Calcolo</span><span class="sxs-lookup"><span data-stu-id="884a9-123">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      | <span data-ttu-id="884a9-124">x</span><span class="sxs-lookup"><span data-stu-id="884a9-124">x</span></span>      |          |       |         |



 

## <a name="see-also"></a><span data-ttu-id="884a9-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="884a9-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="884a9-126">Semantica</span><span class="sxs-lookup"><span data-stu-id="884a9-126">Semantics</span></span>](dx-graphics-hlsl-semantics.md)
</dt> <dt>

[<span data-ttu-id="884a9-127">Modello shader 5</span><span class="sxs-lookup"><span data-stu-id="884a9-127">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




