---
description: Carica l'identità nella matrice corrente.
ms.assetid: 324b49c2-3aca-4bbb-90f3-62f3ffb2fa45
title: 'Metodo ID3DXMATRIXStack:: LoadIdentity (D3DX10. h)'
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
ms.openlocfilehash: 85a58529be3bfcb4d52ba096bb6134fe08994d77
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106323664"
---
# <a name="id3dxmatrixstackloadidentity-method-d3dx10h"></a><span data-ttu-id="2badb-103">Metodo ID3DXMATRIXStack:: LoadIdentity (D3DX10. h)</span><span class="sxs-lookup"><span data-stu-id="2badb-103">ID3DXMATRIXStack::LoadIdentity method (D3DX10.h)</span></span>

<span data-ttu-id="2badb-104">Carica l'identità nella matrice corrente.</span><span class="sxs-lookup"><span data-stu-id="2badb-104">Loads identity in the current matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="2badb-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="2badb-105">Syntax</span></span>


```C++
HRESULT LoadIdentity();
```



## <a name="parameters"></a><span data-ttu-id="2badb-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="2badb-106">Parameters</span></span>

<span data-ttu-id="2badb-107">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="2badb-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="2badb-108">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="2badb-108">Return value</span></span>

<span data-ttu-id="2badb-109">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="2badb-109">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="2badb-110">Se il metodo ha esito positivo, il valore restituito è D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="2badb-110">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="2badb-111">Se il metodo ha esito negativo, il valore restituito può essere D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="2badb-111">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="2badb-112">Commenti</span><span class="sxs-lookup"><span data-stu-id="2badb-112">Remarks</span></span>

<span data-ttu-id="2badb-113">La matrice di identità è una matrice in cui tutti i coefficienti sono 0,0 ad eccezione dei coefficienti \[ 1, 1 \] \[ 2, 2 \] \[ 3, 3 \] \[ 4, 4 \] , impostati su 1,0.</span><span class="sxs-lookup"><span data-stu-id="2badb-113">The identity matrix is a matrix in which all coefficients are 0.0 except the \[1,1\]\[2,2\]\[3,3\]\[4,4\] coefficients, which are set to 1.0.</span></span> <span data-ttu-id="2badb-114">La matrice di identità è speciale in quanto quando viene applicata ai vertici, non vengono modificate.</span><span class="sxs-lookup"><span data-stu-id="2badb-114">The identity matrix is special in that when it is applied to vertices, they are unchanged.</span></span> <span data-ttu-id="2badb-115">La matrice di identità viene utilizzata come punto di partenza per le matrici che modificheranno i valori dei vertici per creare rotazioni, traduzioni e altre trasformazioni che possono essere rappresentate da una matrice 4x4.</span><span class="sxs-lookup"><span data-stu-id="2badb-115">The identity matrix is used as the starting point for matrices that will modify vertex values to create rotations, translations, and any other transformations that can be represented by a 4x4 matrix.</span></span>

## <a name="requirements"></a><span data-ttu-id="2badb-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="2badb-116">Requirements</span></span>



| <span data-ttu-id="2badb-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="2badb-117">Requirement</span></span> | <span data-ttu-id="2badb-118">Valore</span><span class="sxs-lookup"><span data-stu-id="2badb-118">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="2badb-119">Intestazione</span><span class="sxs-lookup"><span data-stu-id="2badb-119">Header</span></span><br/>  | <dl> <span data-ttu-id="2badb-120"><dt>D3DX10. h</dt></span><span class="sxs-lookup"><span data-stu-id="2badb-120"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="2badb-121">Libreria</span><span class="sxs-lookup"><span data-stu-id="2badb-121">Library</span></span><br/> | <dl> <span data-ttu-id="2badb-122"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="2badb-122"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2badb-123">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="2badb-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2badb-124">ID3DXMatrixStack</span><span class="sxs-lookup"><span data-stu-id="2badb-124">ID3DXMatrixStack</span></span>](d3d10-id3dxmatrixstack.md)
</dt> <dt>

[<span data-ttu-id="2badb-125">Interfacce D3DX</span><span class="sxs-lookup"><span data-stu-id="2badb-125">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 




