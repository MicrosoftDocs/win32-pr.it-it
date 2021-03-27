---
title: SV_DomainLocation
description: Definisce la posizione sullo scafo del punto di dominio corrente valutato.
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
ms.openlocfilehash: 3c5195881df438c94cdaed7de8484d0df65e4d54
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/25/2019
ms.locfileid: "104398035"
---
# <a name="sv_domainlocation"></a><span data-ttu-id="62678-104">\_DOMAINLOCATION SV</span><span class="sxs-lookup"><span data-stu-id="62678-104">SV\_DomainLocation</span></span>

<span data-ttu-id="62678-105">Definisce la posizione sullo scafo del punto di dominio corrente valutato.</span><span class="sxs-lookup"><span data-stu-id="62678-105">Defines the location on the hull of the current domain point being evaluated.</span></span>

## <a name="type"></a><span data-ttu-id="62678-106">Tipo</span><span class="sxs-lookup"><span data-stu-id="62678-106">Type</span></span>



|        |                |
|--------|----------------|
| <span data-ttu-id="62678-107">Tipo</span><span class="sxs-lookup"><span data-stu-id="62678-107">Type</span></span>   | <span data-ttu-id="62678-108">Topologia di input</span><span class="sxs-lookup"><span data-stu-id="62678-108">Input Topology</span></span> |
| <span data-ttu-id="62678-109">float2</span><span class="sxs-lookup"><span data-stu-id="62678-109">float2</span></span> | <span data-ttu-id="62678-110">patch quad</span><span class="sxs-lookup"><span data-stu-id="62678-110">quad patch</span></span>     |
| <span data-ttu-id="62678-111">float3</span><span class="sxs-lookup"><span data-stu-id="62678-111">float3</span></span> | <span data-ttu-id="62678-112">patch Tri</span><span class="sxs-lookup"><span data-stu-id="62678-112">tri patch</span></span>      |
| <span data-ttu-id="62678-113">float2</span><span class="sxs-lookup"><span data-stu-id="62678-113">float2</span></span> | <span data-ttu-id="62678-114">isolinea</span><span class="sxs-lookup"><span data-stu-id="62678-114">isoline</span></span>        |



 

## <a name="remarks"></a><span data-ttu-id="62678-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="62678-115">Remarks</span></span>

<span data-ttu-id="62678-116">Questo valore di sistema è obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="62678-116">This system value is required.</span></span>

<span data-ttu-id="62678-117">Questa funzione è supportata nei tipi di shader seguenti:</span><span class="sxs-lookup"><span data-stu-id="62678-117">This function is supported in the following types of shaders:</span></span>



|        |      |        |          |       |         |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="62678-118">Vertice</span><span class="sxs-lookup"><span data-stu-id="62678-118">Vertex</span></span> | <span data-ttu-id="62678-119">Hull</span><span class="sxs-lookup"><span data-stu-id="62678-119">Hull</span></span> | <span data-ttu-id="62678-120">Dominio</span><span class="sxs-lookup"><span data-stu-id="62678-120">Domain</span></span> | <span data-ttu-id="62678-121">Geometria</span><span class="sxs-lookup"><span data-stu-id="62678-121">Geometry</span></span> | <span data-ttu-id="62678-122">Pixel</span><span class="sxs-lookup"><span data-stu-id="62678-122">Pixel</span></span> | <span data-ttu-id="62678-123">Calcolo</span><span class="sxs-lookup"><span data-stu-id="62678-123">Compute</span></span> |
|        |      | <span data-ttu-id="62678-124">x</span><span class="sxs-lookup"><span data-stu-id="62678-124">x</span></span>      |          |       |         |



 

## <a name="see-also"></a><span data-ttu-id="62678-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="62678-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="62678-126">Semantica</span><span class="sxs-lookup"><span data-stu-id="62678-126">Semantics</span></span>](dx-graphics-hlsl-semantics.md)
</dt> <dt>

[<span data-ttu-id="62678-127">Modello Shader 5</span><span class="sxs-lookup"><span data-stu-id="62678-127">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




