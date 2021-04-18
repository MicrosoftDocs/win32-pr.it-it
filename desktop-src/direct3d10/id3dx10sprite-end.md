---
description: 'Chiamare questo dopo ID3DX10Sprite:: Flush. Se è \_ stato \_ \_ specificato lo stato d3dx10 sprite Save quando ID3DX10Sprite:: Begin è stato chiamato, questa API ripristinerà lo stato del dispositivo come prima della chiamata a ID3DX10Sprite:: Begin.'
ms.assetid: 71645edb-be4a-4d87-9fb0-557cf5cf10e5
title: 'Metodo ID3DX10Sprite:: end (D3DX10. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10Sprite.End
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 02d25e41916bd5d7605f3c0e1bc6e7998ea06e86
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106323745"
---
# <a name="id3dx10spriteend-method"></a><span data-ttu-id="6216e-104">Metodo ID3DX10Sprite:: end</span><span class="sxs-lookup"><span data-stu-id="6216e-104">ID3DX10Sprite::End method</span></span>

<span data-ttu-id="6216e-105">Chiamare questo dopo ID3DX10Sprite:: Flush.</span><span class="sxs-lookup"><span data-stu-id="6216e-105">Call this after ID3DX10Sprite::Flush.</span></span> <span data-ttu-id="6216e-106">Se è \_ stato \_ \_ specificato lo stato d3dx10 sprite Save quando ID3DX10Sprite:: Begin è stato chiamato, questa API ripristinerà lo stato del dispositivo come prima della chiamata a ID3DX10Sprite:: Begin.</span><span class="sxs-lookup"><span data-stu-id="6216e-106">If D3DX10\_SPRITE\_SAVE\_STATE was specified when ID3DX10Sprite::Begin was called, this API will restore the device state to how it was before ID3DX10Sprite::Begin was called.</span></span>

## <a name="syntax"></a><span data-ttu-id="6216e-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="6216e-107">Syntax</span></span>


```C++
HRESULT End();
```



## <a name="parameters"></a><span data-ttu-id="6216e-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="6216e-108">Parameters</span></span>

<span data-ttu-id="6216e-109">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="6216e-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="6216e-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="6216e-110">Return value</span></span>

<span data-ttu-id="6216e-111">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="6216e-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="6216e-112">Se il metodo ha esito positivo, il valore restituito è \_ OK.</span><span class="sxs-lookup"><span data-stu-id="6216e-112">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="6216e-113">Se il metodo ha esito negativo, verrà restituito il valore seguente: D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="6216e-113">If the method fails, the following value will be returned: D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="6216e-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="6216e-114">Requirements</span></span>



| <span data-ttu-id="6216e-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="6216e-115">Requirement</span></span> | <span data-ttu-id="6216e-116">Valore</span><span class="sxs-lookup"><span data-stu-id="6216e-116">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="6216e-117">Intestazione</span><span class="sxs-lookup"><span data-stu-id="6216e-117">Header</span></span><br/>  | <dl> <span data-ttu-id="6216e-118"><dt>D3DX10. h</dt></span><span class="sxs-lookup"><span data-stu-id="6216e-118"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="6216e-119">Libreria</span><span class="sxs-lookup"><span data-stu-id="6216e-119">Library</span></span><br/> | <dl> <span data-ttu-id="6216e-120"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="6216e-120"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6216e-121">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="6216e-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6216e-122">ID3DX10Sprite</span><span class="sxs-lookup"><span data-stu-id="6216e-122">ID3DX10Sprite</span></span>](id3dx10sprite.md)
</dt> <dt>

[<span data-ttu-id="6216e-123">Interfacce D3DX</span><span class="sxs-lookup"><span data-stu-id="6216e-123">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 




