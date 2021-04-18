---
description: 'Ripristina lo stato del dispositivo nel modo in cui si trovava quando è stato chiamato ID3DXLine:: Begin.'
ms.assetid: 06243c30-2d1d-4101-a373-46fd9a0d88d3
title: 'Metodo ID3DXLine:: end (D3dx9core. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXLine.End
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 69d8324ab54f37af3f45a5475f08894e278c32e0
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106323473"
---
# <a name="id3dxlineend-method"></a><span data-ttu-id="702d9-103">Metodo ID3DXLine:: end</span><span class="sxs-lookup"><span data-stu-id="702d9-103">ID3DXLine::End method</span></span>

<span data-ttu-id="702d9-104">Ripristina lo stato del dispositivo nel modo in cui si trovava quando è stato chiamato [**ID3DXLine:: Begin**](id3dxline--begin.md) .</span><span class="sxs-lookup"><span data-stu-id="702d9-104">Restores the device state to how it was when [**ID3DXLine::Begin**](id3dxline--begin.md) was called.</span></span>

## <a name="syntax"></a><span data-ttu-id="702d9-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="702d9-105">Syntax</span></span>


```C++
HRESULT End();
```



## <a name="parameters"></a><span data-ttu-id="702d9-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="702d9-106">Parameters</span></span>

<span data-ttu-id="702d9-107">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="702d9-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="702d9-108">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="702d9-108">Return value</span></span>

<span data-ttu-id="702d9-109">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="702d9-109">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="702d9-110">Se il metodo ha esito positivo, il valore restituito è D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="702d9-110">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="702d9-111">Se il metodo ha esito negativo, il valore restituito può essere uno dei seguenti: D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA.</span><span class="sxs-lookup"><span data-stu-id="702d9-111">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA.</span></span>

## <a name="remarks"></a><span data-ttu-id="702d9-112">Commenti</span><span class="sxs-lookup"><span data-stu-id="702d9-112">Remarks</span></span>

<span data-ttu-id="702d9-113">Non è possibile usare **ID3DXLine:: end** come sostituto di [**IDirect3DDevice9:: EndScene**](/windows/desktop/api) o [**ID3DXRenderToSurface:: EndScene**](id3dxrendertosurface--endscene.md).</span><span class="sxs-lookup"><span data-stu-id="702d9-113">**ID3DXLine::End** cannot be used as a substitute for either [**IDirect3DDevice9::EndScene**](/windows/desktop/api) or [**ID3DXRenderToSurface::EndScene**](id3dxrendertosurface--endscene.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="702d9-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="702d9-114">Requirements</span></span>



| <span data-ttu-id="702d9-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="702d9-115">Requirement</span></span> | <span data-ttu-id="702d9-116">Valore</span><span class="sxs-lookup"><span data-stu-id="702d9-116">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="702d9-117">Intestazione</span><span class="sxs-lookup"><span data-stu-id="702d9-117">Header</span></span><br/>  | <dl> <span data-ttu-id="702d9-118"><dt>D3dx9core. h</dt></span><span class="sxs-lookup"><span data-stu-id="702d9-118"><dt>D3dx9core.h</dt></span></span> </dl> |
| <span data-ttu-id="702d9-119">Libreria</span><span class="sxs-lookup"><span data-stu-id="702d9-119">Library</span></span><br/> | <dl> <span data-ttu-id="702d9-120"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="702d9-120"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="702d9-121">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="702d9-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="702d9-122">ID3DXLine</span><span class="sxs-lookup"><span data-stu-id="702d9-122">ID3DXLine</span></span>](id3dxline.md)
</dt> <dt>

[<span data-ttu-id="702d9-123">**ID3DXLine:: Begin**</span><span class="sxs-lookup"><span data-stu-id="702d9-123">**ID3DXLine::Begin**</span></span>](id3dxline--begin.md)
</dt> </dl>

 

 




