---
description: "Metodo ID3DXMATRIXStack::LoadIdentity (D3dx9math.h): carica l'identità nella matrice corrente."
ms.assetid: e314a51f-4016-4819-a95d-d91864a54b2e
title: Metodo ID3DXMATRIXStack::LoadIdentity (D3dx9math.h)
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
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 663559db0746b9d689066e537c1473f467341cbc
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108093559"
---
# <a name="id3dxmatrixstackloadidentity-method-d3dx9mathh"></a><span data-ttu-id="0847b-103">Metodo ID3DXMATRIXStack::LoadIdentity (D3dx9math.h)</span><span class="sxs-lookup"><span data-stu-id="0847b-103">ID3DXMATRIXStack::LoadIdentity method (D3dx9math.h)</span></span>

<span data-ttu-id="0847b-104">Carica l'identità nella matrice corrente.</span><span class="sxs-lookup"><span data-stu-id="0847b-104">Loads identity in the current matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="0847b-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="0847b-105">Syntax</span></span>


```C++
HRESULT LoadIdentity();
```



## <a name="parameters"></a><span data-ttu-id="0847b-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="0847b-106">Parameters</span></span>

<span data-ttu-id="0847b-107">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="0847b-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="0847b-108">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="0847b-108">Return value</span></span>

<span data-ttu-id="0847b-109">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="0847b-109">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="0847b-110">Se il metodo ha esito positivo, il valore restituito è D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="0847b-110">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="0847b-111">Se il metodo ha esito negativo, il valore restituito può essere D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="0847b-111">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="0847b-112">Commenti</span><span class="sxs-lookup"><span data-stu-id="0847b-112">Remarks</span></span>

<span data-ttu-id="0847b-113">La matrice di identità è una matrice in cui tutti i coefficienti sono 0,0 ad eccezione dei \[ coefficienti 1,1 \] \[ 2,2 \] \[ 3,3 \] \[ 4,4, impostati su \] 1,0.</span><span class="sxs-lookup"><span data-stu-id="0847b-113">The identity matrix is a matrix in which all coefficients are 0.0 except the \[1,1\]\[2,2\]\[3,3\]\[4,4\] coefficients, which are set to 1.0.</span></span> <span data-ttu-id="0847b-114">La matrice di identità è speciale in quanto, quando viene applicata ai vertici, rimane invariata.</span><span class="sxs-lookup"><span data-stu-id="0847b-114">The identity matrix is special in that when it is applied to vertices, they are unchanged.</span></span> <span data-ttu-id="0847b-115">La matrice di identità viene usata come punto iniziale per le matrici che modificheranno i valori dei vertici per creare rotazioni, traslazioni ed eventuali altre trasformazioni che possono essere rappresentate da una matrice 4x4.</span><span class="sxs-lookup"><span data-stu-id="0847b-115">The identity matrix is used as the starting point for matrices that will modify vertex values to create rotations, translations, and any other transformations that can be represented by a 4x4 matrix.</span></span>

## <a name="requirements"></a><span data-ttu-id="0847b-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="0847b-116">Requirements</span></span>



| <span data-ttu-id="0847b-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="0847b-117">Requirement</span></span> | <span data-ttu-id="0847b-118">Valore</span><span class="sxs-lookup"><span data-stu-id="0847b-118">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="0847b-119">Intestazione</span><span class="sxs-lookup"><span data-stu-id="0847b-119">Header</span></span><br/>  | <dl> <span data-ttu-id="0847b-120"><dt>D3dx9math.h</dt></span><span class="sxs-lookup"><span data-stu-id="0847b-120"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="0847b-121">Libreria</span><span class="sxs-lookup"><span data-stu-id="0847b-121">Library</span></span><br/> | <dl> <span data-ttu-id="0847b-122"><dt>D3dx9.lib</dt></span><span class="sxs-lookup"><span data-stu-id="0847b-122"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="0847b-123">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="0847b-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0847b-124">ID3DXMATRIXStack</span><span class="sxs-lookup"><span data-stu-id="0847b-124">ID3DXMATRIXStack</span></span>](id3dxmatrixstack.md)
</dt> <dt>

[<span data-ttu-id="0847b-125">**ID3DXMATRIXStack::LoadMatrix**</span><span class="sxs-lookup"><span data-stu-id="0847b-125">**ID3DXMATRIXStack::LoadMatrix**</span></span>](id3dxmatrixstack--loadmatrix.md)
</dt> </dl>

 

 




