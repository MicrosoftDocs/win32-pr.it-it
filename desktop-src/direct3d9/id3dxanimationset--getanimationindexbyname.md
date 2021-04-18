---
description: Ottiene l'indice di un'animazione, dato il relativo nome.
ms.assetid: 6e91a4fe-3202-447b-b486-d29e8da64af2
title: 'Metodo ID3DXAnimationSet:: GetAnimationIndexByName (D3dx9anim. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXAnimationSet.GetAnimationIndexByName
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: f4d3e5fb39ebcfa5ce906d1f90c2c5c10bdd4b3d
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322316"
---
# <a name="id3dxanimationsetgetanimationindexbyname-method"></a><span data-ttu-id="c5f35-103">Metodo ID3DXAnimationSet:: GetAnimationIndexByName</span><span class="sxs-lookup"><span data-stu-id="c5f35-103">ID3DXAnimationSet::GetAnimationIndexByName method</span></span>

<span data-ttu-id="c5f35-104">Ottiene l'indice di un'animazione, dato il relativo nome.</span><span class="sxs-lookup"><span data-stu-id="c5f35-104">Gets the index of an animation, given its name.</span></span>

## <a name="syntax"></a><span data-ttu-id="c5f35-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="c5f35-105">Syntax</span></span>


```C++
HRESULT GetAnimationIndexByName(
  [in]  LPCSTR pName,
  [out] UINT   *pIndex
);
```



## <a name="parameters"></a><span data-ttu-id="c5f35-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="c5f35-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c5f35-107">*pname* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c5f35-107">*pName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c5f35-108">Tipo: **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="c5f35-108">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="c5f35-109">Nome dell'animazione.</span><span class="sxs-lookup"><span data-stu-id="c5f35-109">Name of the animation.</span></span>

</dd> <dt>

<span data-ttu-id="c5f35-110">*pIndex* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="c5f35-110">*pIndex* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c5f35-111">Tipo: **[ **uint**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="c5f35-111">Type: **[**UINT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="c5f35-112">Puntatore all'indice dell'animazione.</span><span class="sxs-lookup"><span data-stu-id="c5f35-112">Pointer to the animation index.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c5f35-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="c5f35-113">Return value</span></span>

<span data-ttu-id="c5f35-114">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="c5f35-114">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="c5f35-115">I valori restituiti da questo metodo sono implementati da un programmatore di applicazioni.</span><span class="sxs-lookup"><span data-stu-id="c5f35-115">The return values of this method are implemented by an application programmer.</span></span> <span data-ttu-id="c5f35-116">In generale, se non si verificano errori, programmare il metodo per restituire D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="c5f35-116">In general, if no error occurs, program the method to return D3D\_OK.</span></span> <span data-ttu-id="c5f35-117">In caso contrario, programmare il metodo per restituire un messaggio di errore appropriato da [D3DERR](d3derr.md) o [**D3DXERR**](./d3dxerr.md).</span><span class="sxs-lookup"><span data-stu-id="c5f35-117">Otherwise, program the method to return an appropriate error message from [D3DERR](d3derr.md) or [**D3DXERR**](./d3dxerr.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="c5f35-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c5f35-118">Requirements</span></span>



| <span data-ttu-id="c5f35-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="c5f35-119">Requirement</span></span> | <span data-ttu-id="c5f35-120">Valore</span><span class="sxs-lookup"><span data-stu-id="c5f35-120">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="c5f35-121">Intestazione</span><span class="sxs-lookup"><span data-stu-id="c5f35-121">Header</span></span><br/>  | <dl> <span data-ttu-id="c5f35-122"><dt>D3dx9anim. h</dt></span><span class="sxs-lookup"><span data-stu-id="c5f35-122"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="c5f35-123">Libreria</span><span class="sxs-lookup"><span data-stu-id="c5f35-123">Library</span></span><br/> | <dl> <span data-ttu-id="c5f35-124"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="c5f35-124"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="c5f35-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="c5f35-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c5f35-126">ID3DXAnimationSet</span><span class="sxs-lookup"><span data-stu-id="c5f35-126">ID3DXAnimationSet</span></span>](id3dxanimationset.md)
</dt> </dl>

 

 
