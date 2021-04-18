---
description: Crea un'interfaccia del set di animazioni con fotogrammi chiave ID3DXKeyframedAnimationSet.
ms.assetid: 7b4fffdc-696c-400c-a0cc-fc755fd25b75
title: Funzione D3DXCreateKeyframedAnimationSet (D3dx9anim. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateKeyframedAnimationSet
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 3f3eb45e999d25c776014c3df5824e0468d03ffd
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106323251"
---
# <a name="d3dxcreatekeyframedanimationset-function"></a><span data-ttu-id="2c894-103">D3DXCreateKeyframedAnimationSet (funzione)</span><span class="sxs-lookup"><span data-stu-id="2c894-103">D3DXCreateKeyframedAnimationSet function</span></span>

<span data-ttu-id="2c894-104">Crea un'interfaccia del set di animazioni con fotogrammi chiave [**ID3DXKeyframedAnimationSet**](id3dxkeyframedanimationset.md) .</span><span class="sxs-lookup"><span data-stu-id="2c894-104">Creates a [**ID3DXKeyframedAnimationSet**](id3dxkeyframedanimationset.md) key framed animation set interface.</span></span>

## <a name="syntax"></a><span data-ttu-id="2c894-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="2c894-105">Syntax</span></span>


```C++
HRESULT D3DXCreateKeyframedAnimationSet(
  _In_        LPCSTR                      pName,
  _In_        DOUBLE                      TicksPerSecond,
  _In_        D3DXPLAYBACK_TYPE           Playback,
  _In_        UINT                        NumAnimations,
  _In_        UINT                        NumCallbackKeys,
  _In_  const LPD3DXKEY_CALLBACK          *pCallKeys,
  _Out_       LPD3DXKEYFRAMEDANIMATIONSET *ppAnimationSet
);
```



## <a name="parameters"></a><span data-ttu-id="2c894-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="2c894-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2c894-107">*pname* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="2c894-107">*pName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2c894-108">Tipo: **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="2c894-108">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="2c894-109">Puntatore al nome del set di animazioni.</span><span class="sxs-lookup"><span data-stu-id="2c894-109">Pointer to the name of the animation set.</span></span>

</dd> <dt>

<span data-ttu-id="2c894-110">*TicksPerSecond* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="2c894-110">*TicksPerSecond* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2c894-111">Tipo: **[ **Double**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="2c894-111">Type: **[**DOUBLE**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="2c894-112">Numero di cicli del fotogramma chiave che intercorrono al secondo.</span><span class="sxs-lookup"><span data-stu-id="2c894-112">Number of key frame ticks that elapse per second.</span></span>

</dd> <dt>

<span data-ttu-id="2c894-113">*Riproduzione* \[ in esecuzione in\]</span><span class="sxs-lookup"><span data-stu-id="2c894-113">*Playback* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2c894-114">Tipo: **[ **D3DXPLAYBACK \_**](./d3dxplayback-type.md)**</span><span class="sxs-lookup"><span data-stu-id="2c894-114">Type: **[**D3DXPLAYBACK\_TYPE**](./d3dxplayback-type.md)**</span></span>

<span data-ttu-id="2c894-115">Tipo del ciclo di riproduzione del set di animazioni.</span><span class="sxs-lookup"><span data-stu-id="2c894-115">Type of the animation set playback loop.</span></span> <span data-ttu-id="2c894-116">Vedere [**D3DXPLAYBACK \_ Type**](./d3dxplayback-type.md).</span><span class="sxs-lookup"><span data-stu-id="2c894-116">See [**D3DXPLAYBACK\_TYPE**](./d3dxplayback-type.md).</span></span>

</dd> <dt>

<span data-ttu-id="2c894-117">*NumAnimations* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="2c894-117">*NumAnimations* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2c894-118">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="2c894-118">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="2c894-119">Numero di set di animazioni di scala, rotazione e conversione (SRT).</span><span class="sxs-lookup"><span data-stu-id="2c894-119">Number of scale, rotate, and translate (SRT) animation sets.</span></span>

</dd> <dt>

<span data-ttu-id="2c894-120">*NumCallbackKeys* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="2c894-120">*NumCallbackKeys* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2c894-121">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="2c894-121">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="2c894-122">Numero di chiavi di callback.</span><span class="sxs-lookup"><span data-stu-id="2c894-122">Number of callback keys.</span></span>

</dd> <dt>

<span data-ttu-id="2c894-123">*pCallKeys* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="2c894-123">*pCallKeys* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2c894-124">Tipo: **const [**LPD3DXKEY \_ callback**](d3dxkey-callback.md) \***</span><span class="sxs-lookup"><span data-stu-id="2c894-124">Type: **const [**LPD3DXKEY\_CALLBACK**](d3dxkey-callback.md)\***</span></span>

<span data-ttu-id="2c894-125">Puntatore a una struttura di [**\_ callback D3DXKEY**](d3dxkey-callback.md) che archivia i dati di callback utente.</span><span class="sxs-lookup"><span data-stu-id="2c894-125">Pointer to a [**D3DXKEY\_CALLBACK**](d3dxkey-callback.md) structure that stores user callback data.</span></span>

</dd> <dt>

<span data-ttu-id="2c894-126">*ppAnimationSet* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="2c894-126">*ppAnimationSet* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="2c894-127">Tipo: **[ **LPD3DXKEYFRAMEDANIMATIONSET**](id3dxkeyframedanimationset.md)\***</span><span class="sxs-lookup"><span data-stu-id="2c894-127">Type: **[**LPD3DXKEYFRAMEDANIMATIONSET**](id3dxkeyframedanimationset.md)\***</span></span>

<span data-ttu-id="2c894-128">Indirizzo di un puntatore all'interfaccia del set di animazioni con fotogrammi chiave [**ID3DXKeyframedAnimationSet**](id3dxkeyframedanimationset.md) .</span><span class="sxs-lookup"><span data-stu-id="2c894-128">Address of a pointer to the [**ID3DXKeyframedAnimationSet**](id3dxkeyframedanimationset.md) key framed animation set interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2c894-129">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="2c894-129">Return value</span></span>

<span data-ttu-id="2c894-130">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="2c894-130">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="2c894-131">Se la funzione ha esito positivo, il valore restituito è \_ OK.</span><span class="sxs-lookup"><span data-stu-id="2c894-131">If the function succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="2c894-132">Se la funzione ha esito negativo, il valore restituito può essere uno dei valori seguenti: D3DERR \_ INVALIDCALL, E \_ OutOfMemory.</span><span class="sxs-lookup"><span data-stu-id="2c894-132">If the function fails, the return value can be one of the following values: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="requirements"></a><span data-ttu-id="2c894-133">Requisiti</span><span class="sxs-lookup"><span data-stu-id="2c894-133">Requirements</span></span>



| <span data-ttu-id="2c894-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="2c894-134">Requirement</span></span> | <span data-ttu-id="2c894-135">Valore</span><span class="sxs-lookup"><span data-stu-id="2c894-135">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="2c894-136">Intestazione</span><span class="sxs-lookup"><span data-stu-id="2c894-136">Header</span></span><br/>  | <dl> <span data-ttu-id="2c894-137"><dt>D3dx9anim. h</dt></span><span class="sxs-lookup"><span data-stu-id="2c894-137"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="2c894-138">Libreria</span><span class="sxs-lookup"><span data-stu-id="2c894-138">Library</span></span><br/> | <dl> <span data-ttu-id="2c894-139"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="2c894-139"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="2c894-140">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="2c894-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2c894-141">Funzioni di animazione</span><span class="sxs-lookup"><span data-stu-id="2c894-141">Animation Functions</span></span>](dx9-graphics-reference-d3dx-functions-animation.md)
</dt> </dl>

 

 
