---
description: 'Metodo ID3DX10Mesh::D rawSubset: disegna un subset di una mesh.'
ms.assetid: e785949e-fcda-4ef9-b50a-193cd954e97d
title: Metodo ID3DX10Mesh::D rawSubset (D3DX10.h)
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
ms.openlocfilehash: 8441bfe4c5d965733a40816ff2def1015f3eb79c
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108084039"
---
# <a name="id3dx10meshdrawsubset-method"></a><span data-ttu-id="df1dd-103">Metodo ID3DX10Mesh::D rawSubset</span><span class="sxs-lookup"><span data-stu-id="df1dd-103">ID3DX10Mesh::DrawSubset method</span></span>

<span data-ttu-id="df1dd-104">Disegna un subset di una mesh.</span><span class="sxs-lookup"><span data-stu-id="df1dd-104">Draws a subset of a mesh.</span></span>

## <a name="syntax"></a><span data-ttu-id="df1dd-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="df1dd-105">Syntax</span></span>


```C++
HRESULT DrawSubset(
  [in] UINT AttribId
);
```



## <a name="parameters"></a><span data-ttu-id="df1dd-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="df1dd-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="df1dd-107">*AttribId* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="df1dd-107">*AttribId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="df1dd-108">Tipo: **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="df1dd-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="df1dd-109">Specifica il subset della mesh da disegnare.</span><span class="sxs-lookup"><span data-stu-id="df1dd-109">Specifies which subset of the mesh to draw.</span></span> <span data-ttu-id="df1dd-110">Questo valore viene usato per distinguere i visi in una mesh come appartenenti a uno o più gruppi di attributi.</span><span class="sxs-lookup"><span data-stu-id="df1dd-110">This value is used to differentiate faces in a mesh as belonging to one or more attribute groups.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="df1dd-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="df1dd-111">Return value</span></span>

<span data-ttu-id="df1dd-112">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="df1dd-112">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="df1dd-113">Il valore restituito è uno dei valori elencati in [Codici restituiti Direct3D 10.](d3d10-graphics-reference-returnvalues.md)</span><span class="sxs-lookup"><span data-stu-id="df1dd-113">The return value is one of the values listed in [Direct3D 10 Return Codes](d3d10-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="df1dd-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="df1dd-114">Remarks</span></span>

<span data-ttu-id="df1dd-115">Una tabella di attributi viene usata per identificare le aree della mesh che devono essere disegnate con trame, stati di rendering, materiali e così via diversi.</span><span class="sxs-lookup"><span data-stu-id="df1dd-115">An attribute table is used to identify areas of the mesh that need to be drawn with different textures, render states, materials, and so on.</span></span> <span data-ttu-id="df1dd-116">Inoltre, l'applicazione può usare la tabella degli attributi per nascondere parti di una mesh non disegnando un determinato identificatore di attributo (AttribId) durante il disegno del frame.</span><span class="sxs-lookup"><span data-stu-id="df1dd-116">In addition, the application can use the attribute table to hide portions of a mesh by not drawing a given attribute identifier (AttribId) when drawing the frame.</span></span>

## <a name="requirements"></a><span data-ttu-id="df1dd-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="df1dd-117">Requirements</span></span>



| <span data-ttu-id="df1dd-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="df1dd-118">Requirement</span></span> | <span data-ttu-id="df1dd-119">Valore</span><span class="sxs-lookup"><span data-stu-id="df1dd-119">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="df1dd-120">Intestazione</span><span class="sxs-lookup"><span data-stu-id="df1dd-120">Header</span></span><br/>  | <dl> <span data-ttu-id="df1dd-121"><dt>D3DX10.h</dt></span><span class="sxs-lookup"><span data-stu-id="df1dd-121"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="df1dd-122">Libreria</span><span class="sxs-lookup"><span data-stu-id="df1dd-122">Library</span></span><br/> | <dl> <span data-ttu-id="df1dd-123"><dt>D3DX10.lib</dt></span><span class="sxs-lookup"><span data-stu-id="df1dd-123"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="df1dd-124">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="df1dd-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="df1dd-125">ID3DX10Mesh</span><span class="sxs-lookup"><span data-stu-id="df1dd-125">ID3DX10Mesh</span></span>](id3dx10mesh.md)
</dt> <dt>

[<span data-ttu-id="df1dd-126">Interfacce D3DX</span><span class="sxs-lookup"><span data-stu-id="df1dd-126">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
