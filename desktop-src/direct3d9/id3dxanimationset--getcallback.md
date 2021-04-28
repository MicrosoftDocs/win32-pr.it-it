---
description: 'Metodo ID3DXAnimationSet::GetCallback: ottiene informazioni su un callback specifico nel set di animazioni.'
ms.assetid: e8388bfc-5438-4216-a98f-dd0dbca12c87
title: Metodo ID3DXAnimationSet::GetCallback (D3dx9anim.h)
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
ms.openlocfilehash: 563c1007cc471ab10a9609e776da69b7c5ed493b
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108097539"
---
# <a name="id3dxanimationsetgetcallback-method"></a><span data-ttu-id="1095f-103">Metodo ID3DXAnimationSet::GetCallback</span><span class="sxs-lookup"><span data-stu-id="1095f-103">ID3DXAnimationSet::GetCallback method</span></span>

<span data-ttu-id="1095f-104">Ottiene informazioni su un callback specifico nel set di animazioni.</span><span class="sxs-lookup"><span data-stu-id="1095f-104">Gets information about a specific callback in the animation set.</span></span>

## <a name="syntax"></a><span data-ttu-id="1095f-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="1095f-105">Syntax</span></span>


```C++
HRESULT GetCallback(
  [in]  DOUBLE Position,
  [in]  DWORD  Flags,
  [out] DOUBLE *pCallbackPosition,
  [out] LPVOID *ppCallbackData
);
```



## <a name="parameters"></a><span data-ttu-id="1095f-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="1095f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1095f-107">*Posizione* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="1095f-107">*Position* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1095f-108">Tipo: **[ **DOUBLE**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="1095f-108">Type: **[**DOUBLE**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="1095f-109">Posizione da cui trovare i callback.</span><span class="sxs-lookup"><span data-stu-id="1095f-109">Position from which to find callbacks.</span></span>

</dd> <dt>

<span data-ttu-id="1095f-110">*Flag* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="1095f-110">*Flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1095f-111">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="1095f-111">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="1095f-112">Flag di ricerca di callback.</span><span class="sxs-lookup"><span data-stu-id="1095f-112">Callback search flags.</span></span> <span data-ttu-id="1095f-113">Questo parametro può essere impostato su una combinazione di uno o più flag [**di D3DXCALLBACK \_ SEARCH \_ FLAGS**](./d3dxcallback-search-flags.md).</span><span class="sxs-lookup"><span data-stu-id="1095f-113">This parameter can be set to a combination of one or more flags from [**D3DXCALLBACK\_SEARCH\_FLAGS**](./d3dxcallback-search-flags.md).</span></span>

</dd> <dt>

<span data-ttu-id="1095f-114">*pCallbackPosition* \[ Cambio\]</span><span class="sxs-lookup"><span data-stu-id="1095f-114">*pCallbackPosition* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="1095f-115">Tipo: **[ **DOUBLE**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="1095f-115">Type: **[**DOUBLE**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="1095f-116">Puntatore alla posizione del callback.</span><span class="sxs-lookup"><span data-stu-id="1095f-116">Pointer to the position of the callback.</span></span>

</dd> <dt>

<span data-ttu-id="1095f-117">*ppCallbackData* \[ Cambio\]</span><span class="sxs-lookup"><span data-stu-id="1095f-117">*ppCallbackData* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="1095f-118">Tipo: **[ **LPVOID**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="1095f-118">Type: **[**LPVOID**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="1095f-119">Indirizzo del puntatore ai dati di callback.</span><span class="sxs-lookup"><span data-stu-id="1095f-119">Address of the callback data pointer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1095f-120">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="1095f-120">Return value</span></span>

<span data-ttu-id="1095f-121">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="1095f-121">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="1095f-122">I valori restituiti di questo metodo vengono implementati da un programmatore di applicazioni.</span><span class="sxs-lookup"><span data-stu-id="1095f-122">The return values of this method are implemented by an application programmer.</span></span> <span data-ttu-id="1095f-123">In generale, se non si verifica alcun errore, programmare il metodo per restituire D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="1095f-123">In general, if no error occurs, program the method to return D3D\_OK.</span></span> <span data-ttu-id="1095f-124">In caso contrario, programmare il metodo per restituire un messaggio di errore appropriato da [D3DERR](d3derr.md) o [**D3DXERR.**](./d3dxerr.md)</span><span class="sxs-lookup"><span data-stu-id="1095f-124">Otherwise, program the method to return an appropriate error message from [D3DERR](d3derr.md) or [**D3DXERR**](./d3dxerr.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="1095f-125">Requisiti</span><span class="sxs-lookup"><span data-stu-id="1095f-125">Requirements</span></span>



| <span data-ttu-id="1095f-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="1095f-126">Requirement</span></span> | <span data-ttu-id="1095f-127">Valore</span><span class="sxs-lookup"><span data-stu-id="1095f-127">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="1095f-128">Intestazione</span><span class="sxs-lookup"><span data-stu-id="1095f-128">Header</span></span><br/>  | <dl> <span data-ttu-id="1095f-129"><dt>D3dx9anim.h</dt></span><span class="sxs-lookup"><span data-stu-id="1095f-129"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="1095f-130">Libreria</span><span class="sxs-lookup"><span data-stu-id="1095f-130">Library</span></span><br/> | <dl> <span data-ttu-id="1095f-131"><dt>D3dx9.lib</dt></span><span class="sxs-lookup"><span data-stu-id="1095f-131"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="1095f-132">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="1095f-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1095f-133">ID3DXAnimationSet</span><span class="sxs-lookup"><span data-stu-id="1095f-133">ID3DXAnimationSet</span></span>](id3dxanimationset.md)
</dt> </dl>

 

 
