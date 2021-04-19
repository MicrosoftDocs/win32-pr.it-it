---
description: Definisce le opzioni per l'esecuzione di calcoli della distanza geodetica, quando si adatta una trama a una superficie curva. Usare questo flag per scegliere tra i calcoli di alta qualità rispetto a quelli veloci durante il calcolo di un Atlante di trama.
ms.assetid: 76649c57-e5ae-4e0d-a7ab-f56385a327c2
title: Enumerazione D3DXUVATLAS (D3dx9mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXUVATLAS
api_type:
- HeaderDef
api_location:
- d3dx9mesh.h
ms.openlocfilehash: 64cc116199b688fc9dcd8d6fbf331d85da508948
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322470"
---
# <a name="d3dxuvatlas-enumeration"></a><span data-ttu-id="e95b1-104">Enumerazione D3DXUVATLAS</span><span class="sxs-lookup"><span data-stu-id="e95b1-104">D3DXUVATLAS enumeration</span></span>

<span data-ttu-id="e95b1-105">Definisce le opzioni per l'esecuzione di calcoli della distanza geodetica, quando si adatta una trama a una superficie curva.</span><span class="sxs-lookup"><span data-stu-id="e95b1-105">Defines options for performing geodesic distance calculations, when fitting a texture to a curved surface.</span></span> <span data-ttu-id="e95b1-106">Usare questo flag per scegliere tra i calcoli di alta qualità rispetto a quelli veloci durante il calcolo di un Atlante di trama.</span><span class="sxs-lookup"><span data-stu-id="e95b1-106">Use this flag to choose between high quality versus fast calculations when computing a texture atlas.</span></span>

## <a name="syntax"></a><span data-ttu-id="e95b1-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="e95b1-107">Syntax</span></span>


```C++
typedef enum _D3DXUVATLAS { 
  D3DXUVATLAS_DEFAULT           = 1,
  D3DXUVATLAS_GEODESIC_FAST     = 2,
  D3DXUVATLAS_GEODESIC_QUALITY  = 3
} D3DXUVATLAS;
```



## <a name="constants"></a><span data-ttu-id="e95b1-108">Costanti</span><span class="sxs-lookup"><span data-stu-id="e95b1-108">Constants</span></span>

<dl> <dt>

<span data-ttu-id="e95b1-109"><span id="D3DXUVATLAS_DEFAULT"></span><span id="d3dxuvatlas_default"></span>**\_Impostazione predefinita D3DXUVATLAS**</span><span class="sxs-lookup"><span data-stu-id="e95b1-109"><span id="D3DXUVATLAS_DEFAULT"></span><span id="d3dxuvatlas_default"></span>**D3DXUVATLAS\_DEFAULT**</span></span>
</dt> <dd>

<span data-ttu-id="e95b1-110">Ai mesh con più di 25K visi sarà applicato il metodo di distanza geodasic veloce, mentre i mesh con meno di 25K visi avranno a disposizione il metodo di distanza geodetica di qualità superiore.</span><span class="sxs-lookup"><span data-stu-id="e95b1-110">Meshes with more than 25k faces will have the fast geodasic distance method applied to them while meshes with fewer than 25k faces will have the higher quality geodesic distance method applied to them instead.</span></span>

</dd> <dt>

<span data-ttu-id="e95b1-111"><span id="D3DXUVATLAS_GEODESIC_FAST"></span><span id="d3dxuvatlas_geodesic_fast"></span>**D3DXUVATLAS \_ geodetica \_ veloce**</span><span class="sxs-lookup"><span data-stu-id="e95b1-111"><span id="D3DXUVATLAS_GEODESIC_FAST"></span><span id="d3dxuvatlas_geodesic_fast"></span>**D3DXUVATLAS\_GEODESIC\_FAST**</span></span>
</dt> <dd>

<span data-ttu-id="e95b1-112">USA approssimazioni per migliorare la velocità di creazione dei grafici a scapito dell'estensione aggiuntiva o di più grafici restituiti per la mesh.</span><span class="sxs-lookup"><span data-stu-id="e95b1-112">Uses approximations to improve charting speed at the cost of added stretch or more charts being output for the mesh.</span></span>

</dd> <dt>

<span data-ttu-id="e95b1-113"><span id="D3DXUVATLAS_GEODESIC_QUALITY"></span><span id="d3dxuvatlas_geodesic_quality"></span>**\_Qualità geodetica D3DXUVATLAS \_**</span><span class="sxs-lookup"><span data-stu-id="e95b1-113"><span id="D3DXUVATLAS_GEODESIC_QUALITY"></span><span id="d3dxuvatlas_geodesic_quality"></span>**D3DXUVATLAS\_GEODESIC\_QUALITY**</span></span>
</dt> <dd>

<span data-ttu-id="e95b1-114">Fornisce grafici di qualità migliori, ma richiede più tempo e memoria rispetto alla velocità.</span><span class="sxs-lookup"><span data-stu-id="e95b1-114">Provides better quality charts, but requires more time and memory than fast.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="e95b1-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e95b1-115">Requirements</span></span>



| <span data-ttu-id="e95b1-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="e95b1-116">Requirement</span></span> | <span data-ttu-id="e95b1-117">Valore</span><span class="sxs-lookup"><span data-stu-id="e95b1-117">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="e95b1-118">Intestazione</span><span class="sxs-lookup"><span data-stu-id="e95b1-118">Header</span></span><br/> | <dl> <span data-ttu-id="e95b1-119"><dt>D3dx9mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="e95b1-119"><dt>D3dx9mesh.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e95b1-120">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e95b1-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e95b1-121">Enumerazioni D3DX</span><span class="sxs-lookup"><span data-stu-id="e95b1-121">D3DX Enumerations</span></span>](dx9-graphics-reference-d3dx-enums.md)
</dt> </dl>

 

 




