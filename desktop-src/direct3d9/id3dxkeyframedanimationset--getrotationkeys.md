---
description: Compila una matrice con i dati della chiave rotazionale usati per l'animazione del fotogramma chiave.
ms.assetid: 9ae8bc28-d231-4d50-98f0-762b2d2c04e8
title: 'Metodo ID3DXKeyframedAnimationSet:: GetRotationKeys (D3dx9anim. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXKeyframedAnimationSet.GetRotationKeys
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: af9242ccf75bc1e5443f040399ffbd8a939ed92e
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "103762310"
---
# <a name="id3dxkeyframedanimationsetgetrotationkeys-method"></a><span data-ttu-id="9ad31-103">Metodo ID3DXKeyframedAnimationSet:: GetRotationKeys</span><span class="sxs-lookup"><span data-stu-id="9ad31-103">ID3DXKeyframedAnimationSet::GetRotationKeys method</span></span>

<span data-ttu-id="9ad31-104">Compila una matrice con i dati della chiave rotazionale usati per l'animazione del fotogramma chiave.</span><span class="sxs-lookup"><span data-stu-id="9ad31-104">Fills an array with rotational key data used for key frame animation.</span></span>

## <a name="syntax"></a><span data-ttu-id="9ad31-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="9ad31-105">Syntax</span></span>


```C++
HRESULT GetRotationKeys(
  [in] UINT                 Animation,
  [in] LPD3DXKEY_QUATERNION pRotationKeys
);
```



## <a name="parameters"></a><span data-ttu-id="9ad31-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="9ad31-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9ad31-107">*Animazione* \[ di in\]</span><span class="sxs-lookup"><span data-stu-id="9ad31-107">*Animation* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9ad31-108">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="9ad31-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="9ad31-109">Indice di animazione.</span><span class="sxs-lookup"><span data-stu-id="9ad31-109">Animation index.</span></span>

</dd> <dt>

<span data-ttu-id="9ad31-110">*pRotationKeys* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="9ad31-110">*pRotationKeys* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9ad31-111">Tipo: **[ **LPD3DXKEY \_ QUATERNION**](d3dxkey-quaternion.md)**</span><span class="sxs-lookup"><span data-stu-id="9ad31-111">Type: **[**LPD3DXKEY\_QUATERNION**](d3dxkey-quaternion.md)**</span></span>

<span data-ttu-id="9ad31-112">Puntatore a una matrice allocata dall'utente di quaternioni [**\_ Quaternion D3DXKEY**](d3dxkey-quaternion.md) che il metodo deve compilare con i dati di rotazione dell'animazione.</span><span class="sxs-lookup"><span data-stu-id="9ad31-112">Pointer to a user-allocated array of [**D3DXKEY\_QUATERNION**](d3dxkey-quaternion.md) quaternions that the method is to fill with animation rotation data.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9ad31-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="9ad31-113">Return value</span></span>

<span data-ttu-id="9ad31-114">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="9ad31-114">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="9ad31-115">Se il metodo ha esito positivo, il valore restituito è \_ OK.</span><span class="sxs-lookup"><span data-stu-id="9ad31-115">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="9ad31-116">Se il metodo ha esito negativo, verrà restituito il valore seguente: D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="9ad31-116">If the method fails, the following value will be returned: D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="9ad31-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="9ad31-117">Requirements</span></span>



| <span data-ttu-id="9ad31-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="9ad31-118">Requirement</span></span> | <span data-ttu-id="9ad31-119">Valore</span><span class="sxs-lookup"><span data-stu-id="9ad31-119">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="9ad31-120">Intestazione</span><span class="sxs-lookup"><span data-stu-id="9ad31-120">Header</span></span><br/>  | <dl> <span data-ttu-id="9ad31-121"><dt>D3dx9anim. h</dt></span><span class="sxs-lookup"><span data-stu-id="9ad31-121"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="9ad31-122">Libreria</span><span class="sxs-lookup"><span data-stu-id="9ad31-122">Library</span></span><br/> | <dl> <span data-ttu-id="9ad31-123"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="9ad31-123"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="9ad31-124">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="9ad31-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9ad31-125">ID3DXKeyframedAnimationSet</span><span class="sxs-lookup"><span data-stu-id="9ad31-125">ID3DXKeyframedAnimationSet</span></span>](id3dxkeyframedanimationset.md)
</dt> <dt>

[<span data-ttu-id="9ad31-126">**ID3DXKeyframedAnimationSet::GetNumRotationKeys**</span><span class="sxs-lookup"><span data-stu-id="9ad31-126">**ID3DXKeyframedAnimationSet::GetNumRotationKeys**</span></span>](id3dxkeyframedanimationset--getnumrotationkeys.md)
</dt> </dl>

 

 
