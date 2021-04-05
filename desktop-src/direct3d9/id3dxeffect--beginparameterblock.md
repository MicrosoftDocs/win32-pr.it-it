---
description: Avviare l'acquisizione delle modifiche di stato in un blocco di parametri.
ms.assetid: cdf6f572-1a21-4c1d-a113-13b48bacd060
title: 'Metodo ID3DXEffect:: BeginParameterBlock (D3DX9Effect. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXEffect.BeginParameterBlock
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 60a43304c8e0e3d64ac6469c1c075c57b5411e3a
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104058618"
---
# <a name="id3dxeffectbeginparameterblock-method"></a><span data-ttu-id="99037-103">Metodo ID3DXEffect:: BeginParameterBlock</span><span class="sxs-lookup"><span data-stu-id="99037-103">ID3DXEffect::BeginParameterBlock method</span></span>

<span data-ttu-id="99037-104">Avviare l'acquisizione delle modifiche di stato in un blocco di parametri.</span><span class="sxs-lookup"><span data-stu-id="99037-104">Start capturing state changes in a parameter block.</span></span>

## <a name="syntax"></a><span data-ttu-id="99037-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="99037-105">Syntax</span></span>


```C++
HRESULT BeginParameterBlock();
```



## <a name="parameters"></a><span data-ttu-id="99037-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="99037-106">Parameters</span></span>

<span data-ttu-id="99037-107">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="99037-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="99037-108">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="99037-108">Return value</span></span>

<span data-ttu-id="99037-109">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="99037-109">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="99037-110">Se il metodo ha esito positivo, il valore restituito è D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="99037-110">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="99037-111">Se il metodo ha esito negativo, il valore restituito può essere uno dei seguenti: D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA.</span><span class="sxs-lookup"><span data-stu-id="99037-111">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA.</span></span>

## <a name="remarks"></a><span data-ttu-id="99037-112">Commenti</span><span class="sxs-lookup"><span data-stu-id="99037-112">Remarks</span></span>

<span data-ttu-id="99037-113">Lo stato del parametro dell'effetto di acquisizione cambia fino a quando non viene chiamato EndParameterBlock.</span><span class="sxs-lookup"><span data-stu-id="99037-113">Capture effect parameter state changes until EndParameterBlock is called.</span></span> <span data-ttu-id="99037-114">I parametri degli effetti includono qualsiasi modifica dello stato al di fuori di un passaggio.</span><span class="sxs-lookup"><span data-stu-id="99037-114">Effect parameters include any state changes outside of a pass.</span></span> <span data-ttu-id="99037-115">Eliminare i blocchi di parametri se non sono più necessari chiamando DeleteParameterBlock.</span><span class="sxs-lookup"><span data-stu-id="99037-115">Delete parameter blocks if they are no longer needed by calling DeleteParameterBlock.</span></span>

## <a name="requirements"></a><span data-ttu-id="99037-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="99037-116">Requirements</span></span>



| <span data-ttu-id="99037-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="99037-117">Requirement</span></span> | <span data-ttu-id="99037-118">Valore</span><span class="sxs-lookup"><span data-stu-id="99037-118">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="99037-119">Intestazione</span><span class="sxs-lookup"><span data-stu-id="99037-119">Header</span></span><br/>  | <dl> <span data-ttu-id="99037-120"><dt>D3DX9Effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="99037-120"><dt>D3DX9Effect.h</dt></span></span> </dl> |
| <span data-ttu-id="99037-121">Libreria</span><span class="sxs-lookup"><span data-stu-id="99037-121">Library</span></span><br/> | <dl> <span data-ttu-id="99037-122"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="99037-122"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="99037-123">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="99037-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="99037-124">ID3DXEffect</span><span class="sxs-lookup"><span data-stu-id="99037-124">ID3DXEffect</span></span>](id3dxeffect.md)
</dt> <dt>

[<span data-ttu-id="99037-125">**ID3DXEffect::EndParameterBlock**</span><span class="sxs-lookup"><span data-stu-id="99037-125">**ID3DXEffect::EndParameterBlock**</span></span>](id3dxeffect--endparameterblock.md)
</dt> <dt>

[<span data-ttu-id="99037-126">**ID3DXEffect::ApplyParameterBlock**</span><span class="sxs-lookup"><span data-stu-id="99037-126">**ID3DXEffect::ApplyParameterBlock**</span></span>](id3dxeffect--applyparameterblock.md)
</dt> <dt>

[<span data-ttu-id="99037-127">**ID3DXEffect::D eleteParameterBlock**</span><span class="sxs-lookup"><span data-stu-id="99037-127">**ID3DXEffect::DeleteParameterBlock**</span></span>](id3dxeffect--deleteparameterblock.md)
</dt> </dl>

 

 




