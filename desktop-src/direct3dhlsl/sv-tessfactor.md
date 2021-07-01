---
title: SV_TessFactor
description: Definisce la quantità a tessellazione su ogni bordo di una patch.
ms.assetid: 970ff744-da5b-4933-866c-dd38b85fb48d
keywords:
- SV_TessFactor HLSL
topic_type:
- apiref
api_name:
- SV_TessFactor
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 308034fe607283ef9f1213cca1cabb4a7229765e
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/30/2021
ms.locfileid: "113118896"
---
# <a name="sv_tessfactor"></a><span data-ttu-id="85069-104">SV \_ TessFactor</span><span class="sxs-lookup"><span data-stu-id="85069-104">SV\_TessFactor</span></span>

<span data-ttu-id="85069-105">Definisce la quantità a tessellazione su ogni bordo di una patch.</span><span class="sxs-lookup"><span data-stu-id="85069-105">Defines the tessellation amount on each edge of a patch.</span></span>

## <a name="type"></a><span data-ttu-id="85069-106">Tipo</span><span class="sxs-lookup"><span data-stu-id="85069-106">Type</span></span>



|  <span data-ttu-id="85069-107">Tipo</span><span class="sxs-lookup"><span data-stu-id="85069-107">Type</span></span>          |  <span data-ttu-id="85069-108">Topologia di input</span><span class="sxs-lookup"><span data-stu-id="85069-108">Input topology</span></span>              |
|------------|----------------|
| <span data-ttu-id="85069-109">float \[ 4\]</span><span class="sxs-lookup"><span data-stu-id="85069-109">float\[4\]</span></span> | <span data-ttu-id="85069-110">quad patch</span><span class="sxs-lookup"><span data-stu-id="85069-110">quad patch</span></span>     |
| <span data-ttu-id="85069-111">float \[ 3\]</span><span class="sxs-lookup"><span data-stu-id="85069-111">float\[3\]</span></span> | <span data-ttu-id="85069-112">tri patch</span><span class="sxs-lookup"><span data-stu-id="85069-112">tri patch</span></span>      |
| <span data-ttu-id="85069-113">float \[ 2\]</span><span class="sxs-lookup"><span data-stu-id="85069-113">float\[2\]</span></span> | <span data-ttu-id="85069-114">isoline</span><span class="sxs-lookup"><span data-stu-id="85069-114">isoline</span></span>        |



 

<span data-ttu-id="85069-115">I fattori a tessellazione devono essere dichiarati come matrice. non possono essere suddivisi in un singolo vettore.</span><span class="sxs-lookup"><span data-stu-id="85069-115">Tessellation factors must be declared as an array; they cannot be packed into a single vector.</span></span>

## <a name="remarks"></a><span data-ttu-id="85069-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="85069-116">Remarks</span></span>

<span data-ttu-id="85069-117">Il valore per il fattore a tessellazione deve essere definito durante la funzione costante patch dello hull shader.</span><span class="sxs-lookup"><span data-stu-id="85069-117">The value for tessellation factor must be defined during the patch constant function of the hull shader.</span></span>

<span data-ttu-id="85069-118">Valore di output obbligatorio per lo hull shader se si usano patch quad o tri.</span><span class="sxs-lookup"><span data-stu-id="85069-118">Required output value for the hull shader if using quad or tri patches.</span></span> <span data-ttu-id="85069-119">Questo valore è anche un valore di input obbligatorio per il domain shader in modo che corrisponda alle firme di dati costanti per la patch tra le fasi a tessellazione.</span><span class="sxs-lookup"><span data-stu-id="85069-119">This value is also a required input value for the domain shader to match the patch-constant data signatures between the tessellation stages.</span></span>

<span data-ttu-id="85069-120">Per un'isolinea, il primo valore in SV TessFactor è il fattore a tessellazione della densità della linea, il secondo valore è il fattore a trama \_ riga-dettaglio.</span><span class="sxs-lookup"><span data-stu-id="85069-120">For an isoline, the first value in SV\_TessFactor is the line-density tessellation factor, the second value is the line-detail tessellation factor.</span></span>

### <a name="tri-patch-tessellation-factors"></a><span data-ttu-id="85069-121">Tri Patch Tessellation Factors</span><span class="sxs-lookup"><span data-stu-id="85069-121">Tri Patch Tessellation Factors</span></span>

<span data-ttu-id="85069-122">Il primo componente fornisce il fattore di tesselation per il bordo u==0 della patch.</span><span class="sxs-lookup"><span data-stu-id="85069-122">The first component provides the tesselation factor for the u==0 edge of the patch.</span></span> <span data-ttu-id="85069-123">Il secondo componente fornisce il fattore di tesselation per il bordo v==0 della patch.</span><span class="sxs-lookup"><span data-stu-id="85069-123">The second component provides the tesselation factor for the v==0 edge of the patch.</span></span> <span data-ttu-id="85069-124">Il terzo componente fornisce il fattore di suddivisione a tesselation per il bordo w==0 della patch.</span><span class="sxs-lookup"><span data-stu-id="85069-124">The third component provides the tesselation factor for the w==0 edge of the patch.</span></span>

### <a name="quad-patch-tessellation-factors"></a><span data-ttu-id="85069-125">Quad Patch Tessellation Factors</span><span class="sxs-lookup"><span data-stu-id="85069-125">Quad Patch Tessellation Factors</span></span>

<span data-ttu-id="85069-126">Il primo componente fornisce il fattore di tesselation per il bordo u==0 della patch.</span><span class="sxs-lookup"><span data-stu-id="85069-126">The first component provides the tesselation factor for the u==0 edge of the patch.</span></span> <span data-ttu-id="85069-127">Il secondo componente fornisce il fattore di tesselation per il bordo v==0 della patch.</span><span class="sxs-lookup"><span data-stu-id="85069-127">The second component provides the tesselation factor for the v==0 edge of the patch.</span></span> <span data-ttu-id="85069-128">Il terzo componente fornisce il fattore di tesselation per il bordo u==1 della patch.</span><span class="sxs-lookup"><span data-stu-id="85069-128">The third component provides the tesselation factor for the u==1 edge of the patch.</span></span> <span data-ttu-id="85069-129">Il quarto componente fornisce il fattore di tesselation per il bordo v==1 della patch.</span><span class="sxs-lookup"><span data-stu-id="85069-129">The fourth component provides the tesselation factor for the v==1 edge of the patch.</span></span> <span data-ttu-id="85069-130">L'ordinamento dei bordi è in senso orario, a partire dal bordo u==0, ovvero il lato sinistro della patch, e dal bordo v==0, ovvero la parte superiore della patch.</span><span class="sxs-lookup"><span data-stu-id="85069-130">The ordering of the edges is clockwise, starting from the u==0 edge, which is the left side of the patch, and from the v==0 edge, which is the top of the patch.</span></span>

<span data-ttu-id="85069-131">Questa funzione è supportata nei tipi di shader seguenti:</span><span class="sxs-lookup"><span data-stu-id="85069-131">This function is supported in the following types of shaders:</span></span>



| <span data-ttu-id="85069-132">Vertice</span><span class="sxs-lookup"><span data-stu-id="85069-132">Vertex</span></span> | <span data-ttu-id="85069-133">Scafo</span><span class="sxs-lookup"><span data-stu-id="85069-133">Hull</span></span> | <span data-ttu-id="85069-134">Dominio</span><span class="sxs-lookup"><span data-stu-id="85069-134">Domain</span></span> | <span data-ttu-id="85069-135">Geometria</span><span class="sxs-lookup"><span data-stu-id="85069-135">Geometry</span></span> | <span data-ttu-id="85069-136">Pixel</span><span class="sxs-lookup"><span data-stu-id="85069-136">Pixel</span></span> | <span data-ttu-id="85069-137">Calcolo</span><span class="sxs-lookup"><span data-stu-id="85069-137">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        | <span data-ttu-id="85069-138">x</span><span class="sxs-lookup"><span data-stu-id="85069-138">x</span></span>    | <span data-ttu-id="85069-139">x</span><span class="sxs-lookup"><span data-stu-id="85069-139">x</span></span>      |          |       |         |



 

## <a name="see-also"></a><span data-ttu-id="85069-140">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="85069-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="85069-141">Semantica</span><span class="sxs-lookup"><span data-stu-id="85069-141">Semantics</span></span>](dx-graphics-hlsl-semantics.md)
</dt> <dt>

[<span data-ttu-id="85069-142">Modello shader 5</span><span class="sxs-lookup"><span data-stu-id="85069-142">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




