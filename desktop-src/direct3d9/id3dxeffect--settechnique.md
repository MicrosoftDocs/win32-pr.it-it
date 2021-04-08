---
description: Imposta la tecnica attiva.
ms.assetid: 18f19773-a9f8-47f9-9334-acc95e0f0eb7
title: 'Metodo ID3DXEffect:: setechnique (D3DX9Effect. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXEffect.SetTechnique
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: e93fbff9eb74e8885675b7ccf4ea69cc53d5da53
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "103969314"
---
# <a name="id3dxeffectsettechnique-method"></a><span data-ttu-id="9fe09-103">Metodo ID3DXEffect:: setechnique</span><span class="sxs-lookup"><span data-stu-id="9fe09-103">ID3DXEffect::SetTechnique method</span></span>

<span data-ttu-id="9fe09-104">Imposta la tecnica attiva.</span><span class="sxs-lookup"><span data-stu-id="9fe09-104">Sets the active technique.</span></span>

## <a name="syntax"></a><span data-ttu-id="9fe09-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="9fe09-105">Syntax</span></span>


```C++
HRESULT SetTechnique(
  [in] D3DXHANDLE hTechnique
);
```



## <a name="parameters"></a><span data-ttu-id="9fe09-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="9fe09-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9fe09-107">*hTechnique* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="9fe09-107">*hTechnique* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9fe09-108">Tipo: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="9fe09-108">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="9fe09-109">Handle univoco per la tecnica.</span><span class="sxs-lookup"><span data-stu-id="9fe09-109">Unique handle to the technique.</span></span> <span data-ttu-id="9fe09-110">Vedere [handle (Direct3D 9)](handles.md).</span><span class="sxs-lookup"><span data-stu-id="9fe09-110">See [Handles (Direct3D 9)](handles.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9fe09-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="9fe09-111">Return value</span></span>

<span data-ttu-id="9fe09-112">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="9fe09-112">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="9fe09-113">Se il metodo ha esito positivo, il valore restituito è \_ OK.</span><span class="sxs-lookup"><span data-stu-id="9fe09-113">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="9fe09-114">Se il metodo ha esito negativo, il valore restituito può essere D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="9fe09-114">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="9fe09-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="9fe09-115">Requirements</span></span>



| <span data-ttu-id="9fe09-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="9fe09-116">Requirement</span></span> | <span data-ttu-id="9fe09-117">Valore</span><span class="sxs-lookup"><span data-stu-id="9fe09-117">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="9fe09-118">Intestazione</span><span class="sxs-lookup"><span data-stu-id="9fe09-118">Header</span></span><br/>  | <dl> <span data-ttu-id="9fe09-119"><dt>D3DX9Effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="9fe09-119"><dt>D3DX9Effect.h</dt></span></span> </dl> |
| <span data-ttu-id="9fe09-120">Libreria</span><span class="sxs-lookup"><span data-stu-id="9fe09-120">Library</span></span><br/> | <dl> <span data-ttu-id="9fe09-121"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="9fe09-121"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="9fe09-122">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="9fe09-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9fe09-123">ID3DXEffect</span><span class="sxs-lookup"><span data-stu-id="9fe09-123">ID3DXEffect</span></span>](id3dxeffect.md)
</dt> </dl>

 

 




