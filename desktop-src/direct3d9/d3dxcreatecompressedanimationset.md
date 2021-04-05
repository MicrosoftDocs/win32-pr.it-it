---
description: Crea un'interfaccia del set di animazioni con fotogrammi chiave ID3DXCompressedAnimationSet che archivia i dati del fotogramma chiave in un formato compresso.
ms.assetid: c3f97d35-5654-4d85-a337-d77819ce3874
title: Funzione D3DXCreateCompressedAnimationSet (D3dx9anim. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateCompressedAnimationSet
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 8aab23466cecf43a50a4136eb0b3d93a271dcb0e
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "103969382"
---
# <a name="d3dxcreatecompressedanimationset-function"></a><span data-ttu-id="78dcb-103">D3DXCreateCompressedAnimationSet (funzione)</span><span class="sxs-lookup"><span data-stu-id="78dcb-103">D3DXCreateCompressedAnimationSet function</span></span>

<span data-ttu-id="78dcb-104">Crea un'interfaccia del set di animazioni con fotogrammi chiave [**ID3DXCompressedAnimationSet**](id3dxcompressedanimationset.md) che archivia i dati del fotogramma chiave in un formato compresso.</span><span class="sxs-lookup"><span data-stu-id="78dcb-104">Creates a [**ID3DXCompressedAnimationSet**](id3dxcompressedanimationset.md) key framed animation set interface that stores key frame data in a compressed format.</span></span>

## <a name="syntax"></a><span data-ttu-id="78dcb-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="78dcb-105">Syntax</span></span>


```C++
HRESULT D3DXCreateCompressedAnimationSet(
  _In_        LPCSTR                       pName,
  _In_        DOUBLE                       TicksPerSecond,
  _In_        D3DXPLAYBACK_TYPE            Playback,
  _In_        LPD3DXBUFFER                 pCompressedData,
  _In_        UINT                         NumCallbackKeys,
  _In_  const LPD3DXKEY_CALLBACK           *pCallKeys,
  _Out_       LPD3DXCOMPRESSEDANIMATIONSET *ppAnimationSet
);
```



## <a name="parameters"></a><span data-ttu-id="78dcb-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="78dcb-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="78dcb-107">*pname* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="78dcb-107">*pName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="78dcb-108">Tipo: **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="78dcb-108">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="78dcb-109">Puntatore al nome del set di animazioni.</span><span class="sxs-lookup"><span data-stu-id="78dcb-109">Pointer to the name of the animation set.</span></span>

</dd> <dt>

<span data-ttu-id="78dcb-110">*TicksPerSecond* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="78dcb-110">*TicksPerSecond* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="78dcb-111">Tipo: **[ **Double**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="78dcb-111">Type: **[**DOUBLE**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="78dcb-112">Numero di cicli del fotogramma chiave che intercorrono al secondo.</span><span class="sxs-lookup"><span data-stu-id="78dcb-112">Number of key frame ticks that elapse per second.</span></span>

</dd> <dt>

<span data-ttu-id="78dcb-113">*Riproduzione* \[ in esecuzione in\]</span><span class="sxs-lookup"><span data-stu-id="78dcb-113">*Playback* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="78dcb-114">Tipo: **[ **D3DXPLAYBACK \_**](./d3dxplayback-type.md)**</span><span class="sxs-lookup"><span data-stu-id="78dcb-114">Type: **[**D3DXPLAYBACK\_TYPE**](./d3dxplayback-type.md)**</span></span>

<span data-ttu-id="78dcb-115">Tipo del ciclo di riproduzione del set di animazioni.</span><span class="sxs-lookup"><span data-stu-id="78dcb-115">Type of the animation set playback loop.</span></span> <span data-ttu-id="78dcb-116">Vedere [**D3DXPLAYBACK \_ Type**](./d3dxplayback-type.md).</span><span class="sxs-lookup"><span data-stu-id="78dcb-116">See [**D3DXPLAYBACK\_TYPE**](./d3dxplayback-type.md).</span></span>

</dd> <dt>

<span data-ttu-id="78dcb-117">*pCompressedData* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="78dcb-117">*pCompressedData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="78dcb-118">Tipo: **[ **LPD3DXBUFFER**](id3dxbuffer.md)**</span><span class="sxs-lookup"><span data-stu-id="78dcb-118">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)**</span></span>

<span data-ttu-id="78dcb-119">Puntatore al buffer [**ID3DXBuffer**](id3dxbuffer.md) che archivia il set di animazioni come dati compressi.</span><span class="sxs-lookup"><span data-stu-id="78dcb-119">Pointer to the [**ID3DXBuffer**](id3dxbuffer.md) buffer that stores the animation set as compressed data.</span></span>

</dd> <dt>

<span data-ttu-id="78dcb-120">*NumCallbackKeys* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="78dcb-120">*NumCallbackKeys* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="78dcb-121">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="78dcb-121">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="78dcb-122">Numero di chiavi di callback.</span><span class="sxs-lookup"><span data-stu-id="78dcb-122">Number of callback keys.</span></span>

</dd> <dt>

<span data-ttu-id="78dcb-123">*pCallKeys* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="78dcb-123">*pCallKeys* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="78dcb-124">Tipo: **const [**LPD3DXKEY \_ callback**](d3dxkey-callback.md) \***</span><span class="sxs-lookup"><span data-stu-id="78dcb-124">Type: **const [**LPD3DXKEY\_CALLBACK**](d3dxkey-callback.md)\***</span></span>

<span data-ttu-id="78dcb-125">Puntatore a una struttura di [**\_ callback D3DXKEY**](d3dxkey-callback.md) che archivia i dati di callback utente.</span><span class="sxs-lookup"><span data-stu-id="78dcb-125">Pointer to a [**D3DXKEY\_CALLBACK**](d3dxkey-callback.md) structure that stores user callback data.</span></span>

</dd> <dt>

<span data-ttu-id="78dcb-126">*ppAnimationSet* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="78dcb-126">*ppAnimationSet* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="78dcb-127">Tipo: **[ **LPD3DXCOMPRESSEDANIMATIONSET**](id3dxcompressedanimationset.md)\***</span><span class="sxs-lookup"><span data-stu-id="78dcb-127">Type: **[**LPD3DXCOMPRESSEDANIMATIONSET**](id3dxcompressedanimationset.md)\***</span></span>

<span data-ttu-id="78dcb-128">Indirizzo di un puntatore all'interfaccia [**ID3DXCompressedAnimationSet**](id3dxcompressedanimationset.md) che archivia i dati del set di animazioni con fotogrammi chiave in un formato compresso.</span><span class="sxs-lookup"><span data-stu-id="78dcb-128">Address of a pointer to the [**ID3DXCompressedAnimationSet**](id3dxcompressedanimationset.md) interface that stores key framed animation set data in a compressed format.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="78dcb-129">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="78dcb-129">Return value</span></span>

<span data-ttu-id="78dcb-130">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="78dcb-130">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="78dcb-131">Se la funzione ha esito positivo, il valore restituito è \_ OK.</span><span class="sxs-lookup"><span data-stu-id="78dcb-131">If the function succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="78dcb-132">Se la funzione ha esito negativo, il valore restituito può essere uno dei valori seguenti: D3DERR \_ INVALIDCALL, E \_ OutOfMemory.</span><span class="sxs-lookup"><span data-stu-id="78dcb-132">If the function fails, the return value can be one of the following values: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="requirements"></a><span data-ttu-id="78dcb-133">Requisiti</span><span class="sxs-lookup"><span data-stu-id="78dcb-133">Requirements</span></span>



| <span data-ttu-id="78dcb-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="78dcb-134">Requirement</span></span> | <span data-ttu-id="78dcb-135">Valore</span><span class="sxs-lookup"><span data-stu-id="78dcb-135">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="78dcb-136">Intestazione</span><span class="sxs-lookup"><span data-stu-id="78dcb-136">Header</span></span><br/>  | <dl> <span data-ttu-id="78dcb-137"><dt>D3dx9anim. h</dt></span><span class="sxs-lookup"><span data-stu-id="78dcb-137"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="78dcb-138">Libreria</span><span class="sxs-lookup"><span data-stu-id="78dcb-138">Library</span></span><br/> | <dl> <span data-ttu-id="78dcb-139"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="78dcb-139"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="78dcb-140">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="78dcb-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="78dcb-141">Funzioni di animazione</span><span class="sxs-lookup"><span data-stu-id="78dcb-141">Animation Functions</span></span>](dx9-graphics-reference-d3dx-functions-animation.md)
</dt> </dl>

 

 
