---
description: "Metodo ID3DXMATRIXStack::LoadIdentity (D3DX10.h): carica l'identità nella matrice corrente."
ms.assetid: 324b49c2-3aca-4bbb-90f3-62f3ffb2fa45
title: Metodo ID3DXMATRIXStack::LoadIdentity (D3DX10.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXMATRIXStack.LoadIdentity
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: f056a911b19c0ea18f5f728a6ce8c4403dd14587
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108107989"
---
# <a name="id3dxmatrixstackloadidentity-method-d3dx10h"></a><span data-ttu-id="279a2-103">Metodo ID3DXMATRIXStack::LoadIdentity (D3DX10.h)</span><span class="sxs-lookup"><span data-stu-id="279a2-103">ID3DXMATRIXStack::LoadIdentity method (D3DX10.h)</span></span>

<span data-ttu-id="279a2-104">Carica l'identità nella matrice corrente.</span><span class="sxs-lookup"><span data-stu-id="279a2-104">Loads identity in the current matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="279a2-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="279a2-105">Syntax</span></span>


```C++
HRESULT LoadIdentity();
```



## <a name="parameters"></a><span data-ttu-id="279a2-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="279a2-106">Parameters</span></span>

<span data-ttu-id="279a2-107">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="279a2-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="279a2-108">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="279a2-108">Return value</span></span>

<span data-ttu-id="279a2-109">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="279a2-109">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="279a2-110">Se il metodo ha esito positivo, il valore restituito è D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="279a2-110">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="279a2-111">Se il metodo ha esito negativo, il valore restituito può essere D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="279a2-111">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="279a2-112">Commenti</span><span class="sxs-lookup"><span data-stu-id="279a2-112">Remarks</span></span>

<span data-ttu-id="279a2-113">La matrice identity è una matrice in cui tutti i coefficienti sono 0,0 ad eccezione dei \[ coefficienti 1,1 \] \[ 2,2 \] \[ 3,3 4,4, che sono impostati su \] \[ \] 1,0.</span><span class="sxs-lookup"><span data-stu-id="279a2-113">The identity matrix is a matrix in which all coefficients are 0.0 except the \[1,1\]\[2,2\]\[3,3\]\[4,4\] coefficients, which are set to 1.0.</span></span> <span data-ttu-id="279a2-114">La matrice di identità è speciale in quanto, quando viene applicata ai vertici, rimane invariata.</span><span class="sxs-lookup"><span data-stu-id="279a2-114">The identity matrix is special in that when it is applied to vertices, they are unchanged.</span></span> <span data-ttu-id="279a2-115">La matrice identity viene usata come punto di partenza per le matrici che modificheranno i valori dei vertici per creare rotazioni, traslazioni e qualsiasi altra trasformazione che può essere rappresentata da una matrice 4x4.</span><span class="sxs-lookup"><span data-stu-id="279a2-115">The identity matrix is used as the starting point for matrices that will modify vertex values to create rotations, translations, and any other transformations that can be represented by a 4x4 matrix.</span></span>

## <a name="requirements"></a><span data-ttu-id="279a2-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="279a2-116">Requirements</span></span>



| <span data-ttu-id="279a2-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="279a2-117">Requirement</span></span> | <span data-ttu-id="279a2-118">Valore</span><span class="sxs-lookup"><span data-stu-id="279a2-118">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="279a2-119">Intestazione</span><span class="sxs-lookup"><span data-stu-id="279a2-119">Header</span></span><br/>  | <dl> <span data-ttu-id="279a2-120"><dt>D3DX10.h</dt></span><span class="sxs-lookup"><span data-stu-id="279a2-120"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="279a2-121">Libreria</span><span class="sxs-lookup"><span data-stu-id="279a2-121">Library</span></span><br/> | <dl> <span data-ttu-id="279a2-122"><dt>D3DX10.lib</dt></span><span class="sxs-lookup"><span data-stu-id="279a2-122"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="279a2-123">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="279a2-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="279a2-124">ID3DXMatrixStack</span><span class="sxs-lookup"><span data-stu-id="279a2-124">ID3DXMatrixStack</span></span>](d3d10-id3dxmatrixstack.md)
</dt> <dt>

[<span data-ttu-id="279a2-125">Interfacce D3DX</span><span class="sxs-lookup"><span data-stu-id="279a2-125">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 




