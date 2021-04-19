---
description: Compila una matrice con i dati della chiave della scala usati per l'animazione del fotogramma chiave.
ms.assetid: 0d595510-6d8c-4bc9-b5ca-0d6f73be3439
title: 'Metodo ID3DXKeyframedAnimationSet:: GetScaleKeys (D3dx9anim. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXKeyframedAnimationSet.GetScaleKeys
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 88c907bc9b45b1203917b092f565096be3ed1fb6
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106323500"
---
# <a name="id3dxkeyframedanimationsetgetscalekeys-method"></a><span data-ttu-id="b3c5f-103">Metodo ID3DXKeyframedAnimationSet:: GetScaleKeys</span><span class="sxs-lookup"><span data-stu-id="b3c5f-103">ID3DXKeyframedAnimationSet::GetScaleKeys method</span></span>

<span data-ttu-id="b3c5f-104">Compila una matrice con i dati della chiave della scala usati per l'animazione del fotogramma chiave.</span><span class="sxs-lookup"><span data-stu-id="b3c5f-104">Fills an array with scale key data used for key frame animation.</span></span>

## <a name="syntax"></a><span data-ttu-id="b3c5f-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="b3c5f-105">Syntax</span></span>


```C++
HRESULT GetScaleKeys(
  [in] UINT              Animation,
  [in] LPD3DXKEY_VECTOR3 pScaleKeys
);
```



## <a name="parameters"></a><span data-ttu-id="b3c5f-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="b3c5f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b3c5f-107">*Animazione* \[ di in\]</span><span class="sxs-lookup"><span data-stu-id="b3c5f-107">*Animation* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b3c5f-108">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="b3c5f-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="b3c5f-109">Indice di animazione.</span><span class="sxs-lookup"><span data-stu-id="b3c5f-109">Animation index.</span></span>

</dd> <dt>

<span data-ttu-id="b3c5f-110">*pScaleKeys* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b3c5f-110">*pScaleKeys* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b3c5f-111">Tipo: **[ **LPD3DXKEY \_ VECTOR3**](d3dxkey-vector3.md)**</span><span class="sxs-lookup"><span data-stu-id="b3c5f-111">Type: **[**LPD3DXKEY\_VECTOR3**](d3dxkey-vector3.md)**</span></span>

<span data-ttu-id="b3c5f-112">Puntatore a una matrice allocata dall'utente di vettori [**D3DXKEY \_ VECTOR3**](d3dxkey-vector3.md) che il metodo deve compilare con i dati della scala dell'animazione.</span><span class="sxs-lookup"><span data-stu-id="b3c5f-112">Pointer to a user-allocated array of [**D3DXKEY\_VECTOR3**](d3dxkey-vector3.md) vectors that the method is to fill with animation scale data.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b3c5f-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="b3c5f-113">Return value</span></span>

<span data-ttu-id="b3c5f-114">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="b3c5f-114">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="b3c5f-115">Se il metodo ha esito positivo, il valore restituito è \_ OK.</span><span class="sxs-lookup"><span data-stu-id="b3c5f-115">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="b3c5f-116">Se il metodo ha esito negativo, verrà restituito il valore seguente: D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="b3c5f-116">If the method fails, the following value will be returned: D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="b3c5f-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b3c5f-117">Requirements</span></span>



| <span data-ttu-id="b3c5f-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="b3c5f-118">Requirement</span></span> | <span data-ttu-id="b3c5f-119">Valore</span><span class="sxs-lookup"><span data-stu-id="b3c5f-119">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="b3c5f-120">Intestazione</span><span class="sxs-lookup"><span data-stu-id="b3c5f-120">Header</span></span><br/>  | <dl> <span data-ttu-id="b3c5f-121"><dt>D3dx9anim. h</dt></span><span class="sxs-lookup"><span data-stu-id="b3c5f-121"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="b3c5f-122">Libreria</span><span class="sxs-lookup"><span data-stu-id="b3c5f-122">Library</span></span><br/> | <dl> <span data-ttu-id="b3c5f-123"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="b3c5f-123"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="b3c5f-124">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="b3c5f-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b3c5f-125">ID3DXKeyframedAnimationSet</span><span class="sxs-lookup"><span data-stu-id="b3c5f-125">ID3DXKeyframedAnimationSet</span></span>](id3dxkeyframedanimationset.md)
</dt> <dt>

[<span data-ttu-id="b3c5f-126">**ID3DXKeyframedAnimationSet::GetNumScaleKeys**</span><span class="sxs-lookup"><span data-stu-id="b3c5f-126">**ID3DXKeyframedAnimationSet::GetNumScaleKeys**</span></span>](id3dxkeyframedanimationset--getnumscalekeys.md)
</dt> </dl>

 

 
