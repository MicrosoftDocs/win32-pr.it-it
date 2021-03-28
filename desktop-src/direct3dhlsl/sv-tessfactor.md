---
title: SV_TessFactor
description: Definisce l'importo a mosaico per ogni bordo di una patch.
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
ms.openlocfilehash: 8fa49b19109985b590747098826199b33a32dd2d
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/25/2019
ms.locfileid: "104976215"
---
# <a name="sv_tessfactor"></a><span data-ttu-id="30b91-104">\_TESSFACTOR SV</span><span class="sxs-lookup"><span data-stu-id="30b91-104">SV\_TessFactor</span></span>

<span data-ttu-id="30b91-105">Definisce l'importo a mosaico per ogni bordo di una patch.</span><span class="sxs-lookup"><span data-stu-id="30b91-105">Defines the tessellation amount on each edge of a patch.</span></span>

## <a name="type"></a><span data-ttu-id="30b91-106">Tipo</span><span class="sxs-lookup"><span data-stu-id="30b91-106">Type</span></span>



|            |                |
|------------|----------------|
| <span data-ttu-id="30b91-107">Tipo</span><span class="sxs-lookup"><span data-stu-id="30b91-107">Type</span></span>       | <span data-ttu-id="30b91-108">Topologia di input</span><span class="sxs-lookup"><span data-stu-id="30b91-108">Input Topology</span></span> |
| <span data-ttu-id="30b91-109">float \[ 4\]</span><span class="sxs-lookup"><span data-stu-id="30b91-109">float\[4\]</span></span> | <span data-ttu-id="30b91-110">patch quad</span><span class="sxs-lookup"><span data-stu-id="30b91-110">quad patch</span></span>     |
| <span data-ttu-id="30b91-111">float \[ 3\]</span><span class="sxs-lookup"><span data-stu-id="30b91-111">float\[3\]</span></span> | <span data-ttu-id="30b91-112">patch Tri</span><span class="sxs-lookup"><span data-stu-id="30b91-112">tri patch</span></span>      |
| <span data-ttu-id="30b91-113">float \[ 2\]</span><span class="sxs-lookup"><span data-stu-id="30b91-113">float\[2\]</span></span> | <span data-ttu-id="30b91-114">isolinea</span><span class="sxs-lookup"><span data-stu-id="30b91-114">isoline</span></span>        |



 

<span data-ttu-id="30b91-115">I fattori a mosaico devono essere dichiarati come matrice; non possono essere compressi in un singolo vettore.</span><span class="sxs-lookup"><span data-stu-id="30b91-115">Tessellation factors must be declared as an array; they cannot be packed into a single vector.</span></span>

## <a name="remarks"></a><span data-ttu-id="30b91-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="30b91-116">Remarks</span></span>

<span data-ttu-id="30b91-117">Il valore per il fattore a mosaico deve essere definito durante la funzione costante patch dello scafo shader.</span><span class="sxs-lookup"><span data-stu-id="30b91-117">The value for tessellation factor must be defined during the patch constant function of the hull shader.</span></span>

<span data-ttu-id="30b91-118">Valore di output necessario per Hull shader se si usano patch quad o tri.</span><span class="sxs-lookup"><span data-stu-id="30b91-118">Required output value for the hull shader if using quad or tri patches.</span></span> <span data-ttu-id="30b91-119">Questo valore è anche un valore di input obbligatorio per lo shader del dominio in modo che corrisponda alle firme dei dati della patch-Constant tra le fasi a mosaico.</span><span class="sxs-lookup"><span data-stu-id="30b91-119">This value is also a required input value for the domain shader to match the patch-constant data signatures between the tessellation stages.</span></span>

<span data-ttu-id="30b91-120">Per un elemento, il primo valore in SV \_ TessFactor è il fattore a mosaico a densità di riga, il secondo valore è il fattore a mosaico a dettaglio di riga.</span><span class="sxs-lookup"><span data-stu-id="30b91-120">For an isoline, the first value in SV\_TessFactor is the line-density tessellation factor, the second value is the line-detail tessellation factor.</span></span>

### <a name="tri-patch-tessellation-factors"></a><span data-ttu-id="30b91-121">Fattori a mosaico della patch Tri</span><span class="sxs-lookup"><span data-stu-id="30b91-121">Tri Patch Tessellation Factors</span></span>

<span data-ttu-id="30b91-122">Il primo componente fornisce il fattore geometrica per il bordo u = = 0 della patch.</span><span class="sxs-lookup"><span data-stu-id="30b91-122">The first component provides the tesselation factor for the u==0 edge of the patch.</span></span> <span data-ttu-id="30b91-123">Il secondo componente fornisce il fattore geometrica per il bordo v = = 0 della patch.</span><span class="sxs-lookup"><span data-stu-id="30b91-123">The second component provides the tesselation factor for the v==0 edge of the patch.</span></span> <span data-ttu-id="30b91-124">Il terzo componente fornisce il fattore geometrica per il bordo w = = 0 della patch.</span><span class="sxs-lookup"><span data-stu-id="30b91-124">The third component provides the tesselation factor for the w==0 edge of the patch.</span></span>

### <a name="quad-patch-tessellation-factors"></a><span data-ttu-id="30b91-125">Fattori a mosaico patch quad</span><span class="sxs-lookup"><span data-stu-id="30b91-125">Quad Patch Tessellation Factors</span></span>

<span data-ttu-id="30b91-126">Il primo componente fornisce il fattore geometrica per il bordo u = = 0 della patch.</span><span class="sxs-lookup"><span data-stu-id="30b91-126">The first component provides the tesselation factor for the u==0 edge of the patch.</span></span> <span data-ttu-id="30b91-127">Il secondo componente fornisce il fattore geometrica per il bordo v = = 0 della patch.</span><span class="sxs-lookup"><span data-stu-id="30b91-127">The second component provides the tesselation factor for the v==0 edge of the patch.</span></span> <span data-ttu-id="30b91-128">Il terzo componente fornisce il fattore geometrica per il bordo u = = 1 della patch.</span><span class="sxs-lookup"><span data-stu-id="30b91-128">The third component provides the tesselation factor for the u==1 edge of the patch.</span></span> <span data-ttu-id="30b91-129">Il quarto componente fornisce il fattore geometrica per il bordo v = = 1 della patch.</span><span class="sxs-lookup"><span data-stu-id="30b91-129">The fourth component provides the tesselation factor for the v==1 edge of the patch.</span></span> <span data-ttu-id="30b91-130">L'ordinamento dei bordi è in senso orario, a partire dal bordo u = = 0, che è il lato sinistro della patch, e dal bordo v = = 0, che è la parte superiore della patch.</span><span class="sxs-lookup"><span data-stu-id="30b91-130">The ordering of the edges is clockwise, starting from the u==0 edge, which is the left side of the patch, and from the v==0 edge, which is the top of the patch.</span></span>

<span data-ttu-id="30b91-131">Questa funzione è supportata nei tipi di shader seguenti:</span><span class="sxs-lookup"><span data-stu-id="30b91-131">This function is supported in the following types of shaders:</span></span>



|        |      |        |          |       |         |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="30b91-132">Vertice</span><span class="sxs-lookup"><span data-stu-id="30b91-132">Vertex</span></span> | <span data-ttu-id="30b91-133">Hull</span><span class="sxs-lookup"><span data-stu-id="30b91-133">Hull</span></span> | <span data-ttu-id="30b91-134">Dominio</span><span class="sxs-lookup"><span data-stu-id="30b91-134">Domain</span></span> | <span data-ttu-id="30b91-135">Geometria</span><span class="sxs-lookup"><span data-stu-id="30b91-135">Geometry</span></span> | <span data-ttu-id="30b91-136">Pixel</span><span class="sxs-lookup"><span data-stu-id="30b91-136">Pixel</span></span> | <span data-ttu-id="30b91-137">Calcolo</span><span class="sxs-lookup"><span data-stu-id="30b91-137">Compute</span></span> |
|        | <span data-ttu-id="30b91-138">x</span><span class="sxs-lookup"><span data-stu-id="30b91-138">x</span></span>    | <span data-ttu-id="30b91-139">x</span><span class="sxs-lookup"><span data-stu-id="30b91-139">x</span></span>      |          |       |         |



 

## <a name="see-also"></a><span data-ttu-id="30b91-140">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="30b91-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="30b91-141">Semantica</span><span class="sxs-lookup"><span data-stu-id="30b91-141">Semantics</span></span>](dx-graphics-hlsl-semantics.md)
</dt> <dt>

[<span data-ttu-id="30b91-142">Modello Shader 5</span><span class="sxs-lookup"><span data-stu-id="30b91-142">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




