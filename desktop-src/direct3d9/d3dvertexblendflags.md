---
description: Definisce i flag utilizzati per controllare il numero o le matrici applicate dal sistema quando si esegue la fusione dei vertici a più matrici.
ms.assetid: 5314f455-ce5f-4ff5-81fc-d3dffc8705b7
title: Enumerazione D3DVERTEXBLENDFLAGS (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DVERTEXBLENDFLAGS
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: 0b4d22740a9ad06a9848dc7649d62ac06d37a056
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104354734"
---
# <a name="d3dvertexblendflags-enumeration"></a><span data-ttu-id="f8f39-103">Enumerazione D3DVERTEXBLENDFLAGS</span><span class="sxs-lookup"><span data-stu-id="f8f39-103">D3DVERTEXBLENDFLAGS enumeration</span></span>

<span data-ttu-id="f8f39-104">Definisce i flag utilizzati per controllare il numero o le matrici applicate dal sistema quando si esegue la fusione dei vertici a più matrici.</span><span class="sxs-lookup"><span data-stu-id="f8f39-104">Defines flags used to control the number or matrices that the system applies when performing multimatrix vertex blending.</span></span>

## <a name="syntax"></a><span data-ttu-id="f8f39-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="f8f39-105">Syntax</span></span>


```C++
typedef enum D3DVERTEXBLENDFLAGS { 
  D3DVBF_DISABLE   = 0,
  D3DVBF_1WEIGHTS  = 1,
  D3DVBF_2WEIGHTS  = 2,
  D3DVBF_3WEIGHTS  = 3,
  D3DVBF_TWEENING  = 255,
  D3DVBF_0WEIGHTS  = 256
} D3DVERTEXBLENDFLAGS, *LPD3DVERTEXBLENDFLAGS;
```



## <a name="constants"></a><span data-ttu-id="f8f39-106">Costanti</span><span class="sxs-lookup"><span data-stu-id="f8f39-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="f8f39-107"><span id="D3DVBF_DISABLE"></span><span id="d3dvbf_disable"></span>**\_Disabilitazione D3DVBF**</span><span class="sxs-lookup"><span data-stu-id="f8f39-107"><span id="D3DVBF_DISABLE"></span><span id="d3dvbf_disable"></span>**D3DVBF\_DISABLE**</span></span>
</dt> <dd>

<span data-ttu-id="f8f39-108">Disabilitare la fusione del vertice; applicare solo la matrice globale impostata dalla macro [**D3DTS \_ WORLDMATRIX**](d3dts-worldmatrix.md) , in cui il valore di indice per lo stato della trasformazione è 0.</span><span class="sxs-lookup"><span data-stu-id="f8f39-108">Disable vertex blending; apply only the world matrix set by the [**D3DTS\_WORLDMATRIX**](d3dts-worldmatrix.md) macro, where the index value for the transformation state is 0.</span></span>

</dd> <dt>

<span data-ttu-id="f8f39-109"><span id="D3DVBF_1WEIGHTS"></span><span id="d3dvbf_1weights"></span>**\_1WEIGHTS D3DVBF**</span><span class="sxs-lookup"><span data-stu-id="f8f39-109"><span id="D3DVBF_1WEIGHTS"></span><span id="d3dvbf_1weights"></span>**D3DVBF\_1WEIGHTS**</span></span>
</dt> <dd>

<span data-ttu-id="f8f39-110">Abilitare la fusione dei vertici tra le due matrici impostate dalla macro [**D3DTS \_ WORLDMATRIX**](d3dts-worldmatrix.md) , in cui il valore di indice per gli Stati di trasformazione è 0 e 1.</span><span class="sxs-lookup"><span data-stu-id="f8f39-110">Enable vertex blending between the two matrices set by the [**D3DTS\_WORLDMATRIX**](d3dts-worldmatrix.md) macro, where the index value for the transformation states are 0 and 1.</span></span>

</dd> <dt>

<span data-ttu-id="f8f39-111"><span id="D3DVBF_2WEIGHTS"></span><span id="d3dvbf_2weights"></span>**\_2WEIGHTS D3DVBF**</span><span class="sxs-lookup"><span data-stu-id="f8f39-111"><span id="D3DVBF_2WEIGHTS"></span><span id="d3dvbf_2weights"></span>**D3DVBF\_2WEIGHTS**</span></span>
</dt> <dd>

<span data-ttu-id="f8f39-112">Abilitare la fusione dei vertici tra le tre matrici impostate dalla macro [**D3DTS \_ WORLDMATRIX**](d3dts-worldmatrix.md) , in cui il valore di indice per gli Stati di trasformazione è 0, 1 e 2.</span><span class="sxs-lookup"><span data-stu-id="f8f39-112">Enable vertex blending between the three matrices set by the [**D3DTS\_WORLDMATRIX**](d3dts-worldmatrix.md) macro, where the index value for the transformation states are 0, 1, and 2.</span></span>

</dd> <dt>

<span data-ttu-id="f8f39-113"><span id="D3DVBF_3WEIGHTS"></span><span id="d3dvbf_3weights"></span>**\_3WEIGHTS D3DVBF**</span><span class="sxs-lookup"><span data-stu-id="f8f39-113"><span id="D3DVBF_3WEIGHTS"></span><span id="d3dvbf_3weights"></span>**D3DVBF\_3WEIGHTS**</span></span>
</dt> <dd>

<span data-ttu-id="f8f39-114">Abilitare la fusione dei vertici tra le quattro matrici impostate dalla macro [**D3DTS \_ WORLDMATRIX**](d3dts-worldmatrix.md) , in cui il valore di indice per gli Stati di trasformazione sono 0, 1, 2 e 3.</span><span class="sxs-lookup"><span data-stu-id="f8f39-114">Enable vertex blending between the four matrices set by the [**D3DTS\_WORLDMATRIX**](d3dts-worldmatrix.md) macro, where the index value for the transformation states are 0, 1, 2, and 3.</span></span>

</dd> <dt>

<span data-ttu-id="f8f39-115"><span id="D3DVBF_TWEENING"></span><span id="d3dvbf_tweening"></span>**\_Interpolazione D3DVBF**</span><span class="sxs-lookup"><span data-stu-id="f8f39-115"><span id="D3DVBF_TWEENING"></span><span id="d3dvbf_tweening"></span>**D3DVBF\_TWEENING**</span></span>
</dt> <dd>

<span data-ttu-id="f8f39-116">La fusione dei vertici viene eseguita usando il valore assegnato a D3DRS \_ TWEENFACTOR.</span><span class="sxs-lookup"><span data-stu-id="f8f39-116">Vertex blending is done by using the value assigned to D3DRS\_TWEENFACTOR.</span></span>

</dd> <dt>

<span data-ttu-id="f8f39-117"><span id="D3DVBF_0WEIGHTS"></span><span id="d3dvbf_0weights"></span>**\_0WEIGHTS D3DVBF**</span><span class="sxs-lookup"><span data-stu-id="f8f39-117"><span id="D3DVBF_0WEIGHTS"></span><span id="d3dvbf_0weights"></span>**D3DVBF\_0WEIGHTS**</span></span>
</dt> <dd>

<span data-ttu-id="f8f39-118">Usare una singola matrice con un peso pari a 1,0.</span><span class="sxs-lookup"><span data-stu-id="f8f39-118">Use a single matrix with a weight of 1.0.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="f8f39-119">Commenti</span><span class="sxs-lookup"><span data-stu-id="f8f39-119">Remarks</span></span>

<span data-ttu-id="f8f39-120">I membri di questo tipo vengono utilizzati con lo \_ stato di rendering VERTEXBLEND di D3DRS.</span><span class="sxs-lookup"><span data-stu-id="f8f39-120">Members of this type are used with the D3DRS\_VERTEXBLEND render state.</span></span>

<span data-ttu-id="f8f39-121">La combinazione di geometria (combinazione di vertici multimatrice) richiede che l'applicazione usi un formato di vertice con pesi di fusione (beta) per ogni vertice.</span><span class="sxs-lookup"><span data-stu-id="f8f39-121">Geometry blending (multimatrix vertex blending) requires that your application use a vertex format that has blending (beta) weights for each vertex.</span></span>

## <a name="requirements"></a><span data-ttu-id="f8f39-122">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f8f39-122">Requirements</span></span>



| <span data-ttu-id="f8f39-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="f8f39-123">Requirement</span></span> | <span data-ttu-id="f8f39-124">Valore</span><span class="sxs-lookup"><span data-stu-id="f8f39-124">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="f8f39-125">Intestazione</span><span class="sxs-lookup"><span data-stu-id="f8f39-125">Header</span></span><br/> | <dl> <span data-ttu-id="f8f39-126"><dt>D3D9Types. h</dt></span><span class="sxs-lookup"><span data-stu-id="f8f39-126"><dt>D3D9Types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f8f39-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="f8f39-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f8f39-128">Enumerazioni Direct3D</span><span class="sxs-lookup"><span data-stu-id="f8f39-128">Direct3D Enumerations</span></span>](dx9-graphics-reference-d3d-enums.md)
</dt> <dt>

[<span data-ttu-id="f8f39-129">**D3DRENDERSTATETYPE**</span><span class="sxs-lookup"><span data-stu-id="f8f39-129">**D3DRENDERSTATETYPE**</span></span>](./d3drenderstatetype.md)
</dt> <dt>

[<span data-ttu-id="f8f39-130">**\_Mondo D3DTS**</span><span class="sxs-lookup"><span data-stu-id="f8f39-130">**D3DTS\_WORLD**</span></span>](d3dts-world.md)
</dt> <dt>

[<span data-ttu-id="f8f39-131">**D3DTS \_ mondo**</span><span class="sxs-lookup"><span data-stu-id="f8f39-131">**D3DTS\_WORLDn**</span></span>](d3dts-worldn.md)
</dt> <dt>

[<span data-ttu-id="f8f39-132">**\_WORLDMATRIX D3DTS**</span><span class="sxs-lookup"><span data-stu-id="f8f39-132">**D3DTS\_WORLDMATRIX**</span></span>](d3dts-worldmatrix.md)
</dt> </dl>

 

 
