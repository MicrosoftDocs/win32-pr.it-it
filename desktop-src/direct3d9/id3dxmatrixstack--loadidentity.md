---
description: Carica l'identità nella matrice corrente.
ms.assetid: e314a51f-4016-4819-a95d-d91864a54b2e
title: 'Metodo ID3DXMATRIXStack:: LoadIdentity (D3dx9math. h)'
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
ms.openlocfilehash: e7ebc7b61679dc3938c2a57aa2346a45b136e5a7
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322337"
---
# <a name="id3dxmatrixstackloadidentity-method-d3dx9mathh"></a><span data-ttu-id="678a6-103">Metodo ID3DXMATRIXStack:: LoadIdentity (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="678a6-103">ID3DXMATRIXStack::LoadIdentity method (D3dx9math.h)</span></span>

<span data-ttu-id="678a6-104">Carica l'identità nella matrice corrente.</span><span class="sxs-lookup"><span data-stu-id="678a6-104">Loads identity in the current matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="678a6-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="678a6-105">Syntax</span></span>


```C++
HRESULT LoadIdentity();
```



## <a name="parameters"></a><span data-ttu-id="678a6-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="678a6-106">Parameters</span></span>

<span data-ttu-id="678a6-107">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="678a6-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="678a6-108">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="678a6-108">Return value</span></span>

<span data-ttu-id="678a6-109">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="678a6-109">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="678a6-110">Se il metodo ha esito positivo, il valore restituito è D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="678a6-110">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="678a6-111">Se il metodo ha esito negativo, il valore restituito può essere D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="678a6-111">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="678a6-112">Commenti</span><span class="sxs-lookup"><span data-stu-id="678a6-112">Remarks</span></span>

<span data-ttu-id="678a6-113">La matrice di identità è una matrice in cui tutti i coefficienti sono 0,0 ad eccezione dei coefficienti \[ 1, 1 \] \[ 2, 2 \] \[ 3, 3 \] \[ 4, 4 \] , impostati su 1,0.</span><span class="sxs-lookup"><span data-stu-id="678a6-113">The identity matrix is a matrix in which all coefficients are 0.0 except the \[1,1\]\[2,2\]\[3,3\]\[4,4\] coefficients, which are set to 1.0.</span></span> <span data-ttu-id="678a6-114">La matrice di identità è speciale in quanto quando viene applicata ai vertici, non vengono modificate.</span><span class="sxs-lookup"><span data-stu-id="678a6-114">The identity matrix is special in that when it is applied to vertices, they are unchanged.</span></span> <span data-ttu-id="678a6-115">La matrice di identità viene utilizzata come punto di partenza per le matrici che modificheranno i valori dei vertici per creare rotazioni, traduzioni e altre trasformazioni che possono essere rappresentate da una matrice 4x4.</span><span class="sxs-lookup"><span data-stu-id="678a6-115">The identity matrix is used as the starting point for matrices that will modify vertex values to create rotations, translations, and any other transformations that can be represented by a 4x4 matrix.</span></span>

## <a name="requirements"></a><span data-ttu-id="678a6-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="678a6-116">Requirements</span></span>



| <span data-ttu-id="678a6-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="678a6-117">Requirement</span></span> | <span data-ttu-id="678a6-118">Valore</span><span class="sxs-lookup"><span data-stu-id="678a6-118">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="678a6-119">Intestazione</span><span class="sxs-lookup"><span data-stu-id="678a6-119">Header</span></span><br/>  | <dl> <span data-ttu-id="678a6-120"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="678a6-120"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="678a6-121">Libreria</span><span class="sxs-lookup"><span data-stu-id="678a6-121">Library</span></span><br/> | <dl> <span data-ttu-id="678a6-122"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="678a6-122"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="678a6-123">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="678a6-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="678a6-124">ID3DXMATRIXStack</span><span class="sxs-lookup"><span data-stu-id="678a6-124">ID3DXMATRIXStack</span></span>](id3dxmatrixstack.md)
</dt> <dt>

[<span data-ttu-id="678a6-125">**ID3DXMATRIXStack::LoadMatrix**</span><span class="sxs-lookup"><span data-stu-id="678a6-125">**ID3DXMATRIXStack::LoadMatrix**</span></span>](id3dxmatrixstack--loadmatrix.md)
</dt> </dl>

 

 




