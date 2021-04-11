---
description: Compila una matrice con i dati della chiave di callback utilizzati per l'animazione del fotogramma chiave.
ms.assetid: 2a2aa04a-a889-415b-8aa2-cc5f2bed1f9a
title: 'Metodo ID3DXKeyframedAnimationSet:: GetCallbackKeys (D3dx9anim. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXKeyframedAnimationSet.GetCallbackKeys
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: d3f8dbc771fcdde6d1c07a1bf810b322b0a70a30
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104234961"
---
# <a name="id3dxkeyframedanimationsetgetcallbackkeys-method"></a><span data-ttu-id="e7992-103">Metodo ID3DXKeyframedAnimationSet:: GetCallbackKeys</span><span class="sxs-lookup"><span data-stu-id="e7992-103">ID3DXKeyframedAnimationSet::GetCallbackKeys method</span></span>

<span data-ttu-id="e7992-104">Compila una matrice con i dati della chiave di callback utilizzati per l'animazione del fotogramma chiave.</span><span class="sxs-lookup"><span data-stu-id="e7992-104">Fills an array with callback key data used for key frame animation.</span></span>

## <a name="syntax"></a><span data-ttu-id="e7992-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="e7992-105">Syntax</span></span>


```C++
HRESULT GetCallbackKeys(
  [out] LPD3DXKEY_CALLBACK pCallbackKeys
);
```



## <a name="parameters"></a><span data-ttu-id="e7992-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="e7992-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e7992-107">*pCallbackKeys* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="e7992-107">*pCallbackKeys* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e7992-108">Tipo: **[ **\_ callback LPD3DXKEY**](d3dxkey-callback.md)**</span><span class="sxs-lookup"><span data-stu-id="e7992-108">Type: **[**LPD3DXKEY\_CALLBACK**](d3dxkey-callback.md)**</span></span>

<span data-ttu-id="e7992-109">Puntatore a una matrice allocata dall'utente di strutture di [**\_ callback D3DXKEY**](d3dxkey-callback.md) che il metodo deve compilare con i dati di callback.</span><span class="sxs-lookup"><span data-stu-id="e7992-109">Pointer to a user-allocated array of [**D3DXKEY\_CALLBACK**](d3dxkey-callback.md) structures that the method is to fill with callback data.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e7992-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="e7992-110">Return value</span></span>

<span data-ttu-id="e7992-111">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="e7992-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="e7992-112">Se il metodo ha esito positivo, il valore restituito è \_ OK.</span><span class="sxs-lookup"><span data-stu-id="e7992-112">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="e7992-113">Se il metodo ha esito negativo, verrà restituito il valore seguente: D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="e7992-113">If the method fails, the following value will be returned: D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="e7992-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e7992-114">Requirements</span></span>



| <span data-ttu-id="e7992-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="e7992-115">Requirement</span></span> | <span data-ttu-id="e7992-116">Valore</span><span class="sxs-lookup"><span data-stu-id="e7992-116">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="e7992-117">Intestazione</span><span class="sxs-lookup"><span data-stu-id="e7992-117">Header</span></span><br/>  | <dl> <span data-ttu-id="e7992-118"><dt>D3dx9anim. h</dt></span><span class="sxs-lookup"><span data-stu-id="e7992-118"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="e7992-119">Libreria</span><span class="sxs-lookup"><span data-stu-id="e7992-119">Library</span></span><br/> | <dl> <span data-ttu-id="e7992-120"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="e7992-120"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="e7992-121">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e7992-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e7992-122">ID3DXKeyframedAnimationSet</span><span class="sxs-lookup"><span data-stu-id="e7992-122">ID3DXKeyframedAnimationSet</span></span>](id3dxkeyframedanimationset.md)
</dt> <dt>

[<span data-ttu-id="e7992-123">**ID3DXKeyframedAnimationSet::GetNumCallbackKeys**</span><span class="sxs-lookup"><span data-stu-id="e7992-123">**ID3DXKeyframedAnimationSet::GetNumCallbackKeys**</span></span>](id3dxkeyframedanimationset--getnumcallbackkeys.md)
</dt> </dl>

 

 




