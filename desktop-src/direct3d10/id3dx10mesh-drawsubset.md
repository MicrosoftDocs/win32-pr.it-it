---
description: Disegna un subset di una mesh.
ms.assetid: e785949e-fcda-4ef9-b50a-193cd954e97d
title: Metodo ID3DX10Mesh::D rawSubset (D3DX10. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10Mesh.DrawSubset
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 80beceebeead84a782cc7852ac0d2fe15ad61ff3
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322752"
---
# <a name="id3dx10meshdrawsubset-method"></a><span data-ttu-id="58666-103">ID3DX10Mesh::D Metodo rawSubset</span><span class="sxs-lookup"><span data-stu-id="58666-103">ID3DX10Mesh::DrawSubset method</span></span>

<span data-ttu-id="58666-104">Disegna un subset di una mesh.</span><span class="sxs-lookup"><span data-stu-id="58666-104">Draws a subset of a mesh.</span></span>

## <a name="syntax"></a><span data-ttu-id="58666-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="58666-105">Syntax</span></span>


```C++
HRESULT DrawSubset(
  [in] UINT AttribId
);
```



## <a name="parameters"></a><span data-ttu-id="58666-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="58666-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="58666-107">*AttribId* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="58666-107">*AttribId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="58666-108">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="58666-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="58666-109">Specifica il subset della mesh da creare.</span><span class="sxs-lookup"><span data-stu-id="58666-109">Specifies which subset of the mesh to draw.</span></span> <span data-ttu-id="58666-110">Questo valore viene utilizzato per distinguere i visi in una mesh come appartenenti a uno o più gruppi di attributi.</span><span class="sxs-lookup"><span data-stu-id="58666-110">This value is used to differentiate faces in a mesh as belonging to one or more attribute groups.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="58666-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="58666-111">Return value</span></span>

<span data-ttu-id="58666-112">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="58666-112">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="58666-113">Il valore restituito è uno dei valori elencati in [codici restituiti Direct3D 10](d3d10-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="58666-113">The return value is one of the values listed in [Direct3D 10 Return Codes](d3d10-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="58666-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="58666-114">Remarks</span></span>

<span data-ttu-id="58666-115">Una tabella degli attributi viene utilizzata per identificare le aree della mesh che devono essere disegnate con trame, Stati di rendering, materiali e così via.</span><span class="sxs-lookup"><span data-stu-id="58666-115">An attribute table is used to identify areas of the mesh that need to be drawn with different textures, render states, materials, and so on.</span></span> <span data-ttu-id="58666-116">Inoltre, l'applicazione può usare la tabella attribute per nascondere parti di una mesh senza disegnare un identificatore di attributo specificato (AttribId) durante il disegno del frame.</span><span class="sxs-lookup"><span data-stu-id="58666-116">In addition, the application can use the attribute table to hide portions of a mesh by not drawing a given attribute identifier (AttribId) when drawing the frame.</span></span>

## <a name="requirements"></a><span data-ttu-id="58666-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="58666-117">Requirements</span></span>



| <span data-ttu-id="58666-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="58666-118">Requirement</span></span> | <span data-ttu-id="58666-119">Valore</span><span class="sxs-lookup"><span data-stu-id="58666-119">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="58666-120">Intestazione</span><span class="sxs-lookup"><span data-stu-id="58666-120">Header</span></span><br/>  | <dl> <span data-ttu-id="58666-121"><dt>D3DX10. h</dt></span><span class="sxs-lookup"><span data-stu-id="58666-121"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="58666-122">Libreria</span><span class="sxs-lookup"><span data-stu-id="58666-122">Library</span></span><br/> | <dl> <span data-ttu-id="58666-123"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="58666-123"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="58666-124">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="58666-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="58666-125">ID3DX10Mesh</span><span class="sxs-lookup"><span data-stu-id="58666-125">ID3DX10Mesh</span></span>](id3dx10mesh.md)
</dt> <dt>

[<span data-ttu-id="58666-126">Interfacce D3DX</span><span class="sxs-lookup"><span data-stu-id="58666-126">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
