---
description: Ottiene informazioni su un callback specifico nel set di animazioni.
ms.assetid: e8388bfc-5438-4216-a98f-dd0dbca12c87
title: 'Metodo ID3DXAnimationSet:: getCallback (D3dx9anim. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXAnimationSet.GetCallback
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: f4cde6c9d51fd29c0412f33b34ca7bea8260dfea
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104235203"
---
# <a name="id3dxanimationsetgetcallback-method"></a><span data-ttu-id="4c675-103">Metodo ID3DXAnimationSet:: getCallback</span><span class="sxs-lookup"><span data-stu-id="4c675-103">ID3DXAnimationSet::GetCallback method</span></span>

<span data-ttu-id="4c675-104">Ottiene informazioni su un callback specifico nel set di animazioni.</span><span class="sxs-lookup"><span data-stu-id="4c675-104">Gets information about a specific callback in the animation set.</span></span>

## <a name="syntax"></a><span data-ttu-id="4c675-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="4c675-105">Syntax</span></span>


```C++
HRESULT GetCallback(
  [in]  DOUBLE Position,
  [in]  DWORD  Flags,
  [out] DOUBLE *pCallbackPosition,
  [out] LPVOID *ppCallbackData
);
```



## <a name="parameters"></a><span data-ttu-id="4c675-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="4c675-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4c675-107">*Posizione* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="4c675-107">*Position* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4c675-108">Tipo: **[ **Double**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="4c675-108">Type: **[**DOUBLE**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="4c675-109">Posizione da cui trovare i callback.</span><span class="sxs-lookup"><span data-stu-id="4c675-109">Position from which to find callbacks.</span></span>

</dd> <dt>

<span data-ttu-id="4c675-110">*Flag* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="4c675-110">*Flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4c675-111">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="4c675-111">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="4c675-112">Flag di ricerca di callback.</span><span class="sxs-lookup"><span data-stu-id="4c675-112">Callback search flags.</span></span> <span data-ttu-id="4c675-113">Questo parametro può essere impostato su una combinazione di uno o più flag dei [**\_ \_ flag di ricerca D3DXCALLBACK**](./d3dxcallback-search-flags.md).</span><span class="sxs-lookup"><span data-stu-id="4c675-113">This parameter can be set to a combination of one or more flags from [**D3DXCALLBACK\_SEARCH\_FLAGS**](./d3dxcallback-search-flags.md).</span></span>

</dd> <dt>

<span data-ttu-id="4c675-114">*pCallbackPosition* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="4c675-114">*pCallbackPosition* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="4c675-115">Tipo: **[ **Double**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="4c675-115">Type: **[**DOUBLE**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="4c675-116">Puntatore alla posizione del callback.</span><span class="sxs-lookup"><span data-stu-id="4c675-116">Pointer to the position of the callback.</span></span>

</dd> <dt>

<span data-ttu-id="4c675-117">*ppCallbackData* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="4c675-117">*ppCallbackData* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="4c675-118">Tipo: **[ **LPVOID**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="4c675-118">Type: **[**LPVOID**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="4c675-119">Indirizzo del puntatore ai dati di callback.</span><span class="sxs-lookup"><span data-stu-id="4c675-119">Address of the callback data pointer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4c675-120">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="4c675-120">Return value</span></span>

<span data-ttu-id="4c675-121">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="4c675-121">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="4c675-122">I valori restituiti da questo metodo sono implementati da un programmatore di applicazioni.</span><span class="sxs-lookup"><span data-stu-id="4c675-122">The return values of this method are implemented by an application programmer.</span></span> <span data-ttu-id="4c675-123">In generale, se non si verificano errori, programmare il metodo per restituire D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="4c675-123">In general, if no error occurs, program the method to return D3D\_OK.</span></span> <span data-ttu-id="4c675-124">In caso contrario, programmare il metodo per restituire un messaggio di errore appropriato da [D3DERR](d3derr.md) o [**D3DXERR**](./d3dxerr.md).</span><span class="sxs-lookup"><span data-stu-id="4c675-124">Otherwise, program the method to return an appropriate error message from [D3DERR](d3derr.md) or [**D3DXERR**](./d3dxerr.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="4c675-125">Requisiti</span><span class="sxs-lookup"><span data-stu-id="4c675-125">Requirements</span></span>



| <span data-ttu-id="4c675-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="4c675-126">Requirement</span></span> | <span data-ttu-id="4c675-127">Valore</span><span class="sxs-lookup"><span data-stu-id="4c675-127">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="4c675-128">Intestazione</span><span class="sxs-lookup"><span data-stu-id="4c675-128">Header</span></span><br/>  | <dl> <span data-ttu-id="4c675-129"><dt>D3dx9anim. h</dt></span><span class="sxs-lookup"><span data-stu-id="4c675-129"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="4c675-130">Libreria</span><span class="sxs-lookup"><span data-stu-id="4c675-130">Library</span></span><br/> | <dl> <span data-ttu-id="4c675-131"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="4c675-131"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="4c675-132">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="4c675-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4c675-133">ID3DXAnimationSet</span><span class="sxs-lookup"><span data-stu-id="4c675-133">ID3DXAnimationSet</span></span>](id3dxanimationset.md)
</dt> </dl>

 

 
