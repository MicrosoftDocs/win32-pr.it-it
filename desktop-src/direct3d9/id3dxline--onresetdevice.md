---
description: Usare questo metodo per acquisire nuovamente le risorse e salvare lo stato iniziale.
ms.assetid: beca7a51-e799-4e03-81a3-218552231428
title: 'Metodo ID3DXLine:: OnResetDevice (D3dx9core. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXLine.OnResetDevice
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 0c85a93084e3a4f3d8308e5111338d0c5127e22c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106323727"
---
# <a name="id3dxlineonresetdevice-method"></a><span data-ttu-id="63142-103">Metodo ID3DXLine:: OnResetDevice</span><span class="sxs-lookup"><span data-stu-id="63142-103">ID3DXLine::OnResetDevice method</span></span>

<span data-ttu-id="63142-104">Usare questo metodo per acquisire nuovamente le risorse e salvare lo stato iniziale.</span><span class="sxs-lookup"><span data-stu-id="63142-104">Use this method to re-acquire resources and save initial state.</span></span>

## <a name="syntax"></a><span data-ttu-id="63142-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="63142-105">Syntax</span></span>


```C++
HRESULT OnResetDevice();
```



## <a name="parameters"></a><span data-ttu-id="63142-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="63142-106">Parameters</span></span>

<span data-ttu-id="63142-107">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="63142-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="63142-108">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="63142-108">Return value</span></span>

<span data-ttu-id="63142-109">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="63142-109">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="63142-110">Se il metodo ha esito positivo, il valore restituito è \_ OK.</span><span class="sxs-lookup"><span data-stu-id="63142-110">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="63142-111">Se il metodo ha esito negativo, il valore restituito può essere D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="63142-111">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="63142-112">Commenti</span><span class="sxs-lookup"><span data-stu-id="63142-112">Remarks</span></span>

<span data-ttu-id="63142-113">**ID3DXLine:: OnResetDevice** deve essere chiamato ogni volta che il dispositivo viene reimpostato (usando [**IDirect3DDevice9:: Reset**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-reset)), prima di qualsiasi altro metodo chiamato.</span><span class="sxs-lookup"><span data-stu-id="63142-113">**ID3DXLine::OnResetDevice** should be called each time the device is reset (using [**IDirect3DDevice9::Reset**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-reset)), before any other methods are called.</span></span> <span data-ttu-id="63142-114">Si tratta di una posizione ideale per acquisire nuovamente le risorse di memoria video e i blocchi di stato di acquisizione.</span><span class="sxs-lookup"><span data-stu-id="63142-114">This is a good place to re-acquire video-memory resources and capture state blocks.</span></span>

## <a name="requirements"></a><span data-ttu-id="63142-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="63142-115">Requirements</span></span>



| <span data-ttu-id="63142-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="63142-116">Requirement</span></span> | <span data-ttu-id="63142-117">Valore</span><span class="sxs-lookup"><span data-stu-id="63142-117">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="63142-118">Intestazione</span><span class="sxs-lookup"><span data-stu-id="63142-118">Header</span></span><br/>  | <dl> <span data-ttu-id="63142-119"><dt>D3dx9core. h</dt></span><span class="sxs-lookup"><span data-stu-id="63142-119"><dt>D3dx9core.h</dt></span></span> </dl> |
| <span data-ttu-id="63142-120">Libreria</span><span class="sxs-lookup"><span data-stu-id="63142-120">Library</span></span><br/> | <dl> <span data-ttu-id="63142-121"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="63142-121"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="63142-122">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="63142-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="63142-123">ID3DXLine</span><span class="sxs-lookup"><span data-stu-id="63142-123">ID3DXLine</span></span>](id3dxline.md)
</dt> </dl>

 

 
