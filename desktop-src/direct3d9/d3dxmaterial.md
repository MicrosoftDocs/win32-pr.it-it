---
description: Restituisce le informazioni sul materiale salvate nei file Direct3D (. x).
ms.assetid: dfa021ba-61d8-4f99-9bbb-0cfbe11b787d
title: Struttura D3DXMATERIAL (D3dx9mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXMATERIAL
api_type:
- HeaderDef
api_location:
- d3dx9mesh.h
ms.openlocfilehash: 89079b716a8c5808255b2bc660f1d364bb97315f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322137"
---
# <a name="d3dxmaterial-structure"></a><span data-ttu-id="7d7da-103">Struttura D3DXMATERIAL</span><span class="sxs-lookup"><span data-stu-id="7d7da-103">D3DXMATERIAL structure</span></span>

<span data-ttu-id="7d7da-104">Restituisce le informazioni sul materiale salvate nei file Direct3D (. x).</span><span class="sxs-lookup"><span data-stu-id="7d7da-104">Returns material information saved in Direct3D (.x) files.</span></span>

## <a name="syntax"></a><span data-ttu-id="7d7da-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="7d7da-105">Syntax</span></span>


```C++
typedef struct D3DXMATERIAL {
  D3DMATERIAL9 MatD3D;
  LPSTR        pTextureFilename;
} D3DXMATERIAL, *LPD3DXMATERIAL;
```



## <a name="members"></a><span data-ttu-id="7d7da-106">Members</span><span class="sxs-lookup"><span data-stu-id="7d7da-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="7d7da-107">**MatD3D**</span><span class="sxs-lookup"><span data-stu-id="7d7da-107">**MatD3D**</span></span>
</dt> <dd>

<span data-ttu-id="7d7da-108">Tipo: **[ **D3DMATERIAL9**](d3dmaterial9.md)**</span><span class="sxs-lookup"><span data-stu-id="7d7da-108">Type: **[**D3DMATERIAL9**](d3dmaterial9.md)**</span></span>

</dd> <dd>

<span data-ttu-id="7d7da-109">Struttura [**D3DMATERIAL9**](d3dmaterial9.md) che descrive le proprietà del materiale.</span><span class="sxs-lookup"><span data-stu-id="7d7da-109">[**D3DMATERIAL9**](d3dmaterial9.md) structure that describes the material properties.</span></span>

</dd> <dt>

<span data-ttu-id="7d7da-110">**pTextureFilename**</span><span class="sxs-lookup"><span data-stu-id="7d7da-110">**pTextureFilename**</span></span>
</dt> <dd>

<span data-ttu-id="7d7da-111">Tipo: **LPSTR**</span><span class="sxs-lookup"><span data-stu-id="7d7da-111">Type: **LPSTR**</span></span>

</dd> <dd>

<span data-ttu-id="7d7da-112">Puntatore a una stringa che specifica il nome del file della trama.</span><span class="sxs-lookup"><span data-stu-id="7d7da-112">Pointer to a string that specifies the file name of the texture.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="7d7da-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="7d7da-113">Remarks</span></span>

<span data-ttu-id="7d7da-114">Le funzioni [**D3DXLoadMeshFromX**](d3dxloadmeshfromx.md) e [**D3DXLoadMeshFromXof**](d3dxloadmeshfromxof.md) restituiscono una matrice di strutture **D3DXMATERIAL** che specificano il colore e il nome del materiale della trama per ogni materiale presente nella rete.</span><span class="sxs-lookup"><span data-stu-id="7d7da-114">The [**D3DXLoadMeshFromX**](d3dxloadmeshfromx.md) and [**D3DXLoadMeshFromXof**](d3dxloadmeshfromxof.md) functions return an array of **D3DXMATERIAL** structures that specify the material color and name of the texture for each material in the mesh.</span></span> <span data-ttu-id="7d7da-115">L'applicazione è quindi necessaria per caricare la trama.</span><span class="sxs-lookup"><span data-stu-id="7d7da-115">The application is then required to load the texture.</span></span>

<span data-ttu-id="7d7da-116">Il tipo LPD3DXMATERIAL è definito come un puntatore alla struttura **D3DXMATERIAL** .</span><span class="sxs-lookup"><span data-stu-id="7d7da-116">The LPD3DXMATERIAL type is defined as a pointer to the **D3DXMATERIAL** structure.</span></span>


```
typedef struct D3DXMATERIAL* LPD3DXMATERIAL;
```



## <a name="requirements"></a><span data-ttu-id="7d7da-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="7d7da-117">Requirements</span></span>



| <span data-ttu-id="7d7da-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="7d7da-118">Requirement</span></span> | <span data-ttu-id="7d7da-119">Valore</span><span class="sxs-lookup"><span data-stu-id="7d7da-119">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="7d7da-120">Intestazione</span><span class="sxs-lookup"><span data-stu-id="7d7da-120">Header</span></span><br/> | <dl> <span data-ttu-id="7d7da-121"><dt>D3dx9mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="7d7da-121"><dt>D3dx9mesh.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7d7da-122">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="7d7da-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7d7da-123">Strutture D3DX</span><span class="sxs-lookup"><span data-stu-id="7d7da-123">D3DX Structures</span></span>](dx9-graphics-reference-d3dx-structures.md)
</dt> <dt>

[<span data-ttu-id="7d7da-124">**D3DXLoadMeshFromX**</span><span class="sxs-lookup"><span data-stu-id="7d7da-124">**D3DXLoadMeshFromX**</span></span>](d3dxloadmeshfromx.md)
</dt> <dt>

[<span data-ttu-id="7d7da-125">**D3DXLoadMeshFromXof**</span><span class="sxs-lookup"><span data-stu-id="7d7da-125">**D3DXLoadMeshFromXof**</span></span>](d3dxloadmeshfromxof.md)
</dt> </dl>

 

 




