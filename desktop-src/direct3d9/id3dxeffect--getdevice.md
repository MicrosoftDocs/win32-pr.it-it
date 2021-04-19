---
description: Recupera il dispositivo associato all'effetto.
ms.assetid: acef5d0a-b185-4054-8982-0580440ab76b
title: 'Metodo ID3DXEffect:: GetDevice (D3DX9Effect. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXEffect.GetDevice
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: fde2d9f3d9db362bf48fda66e9da10b91a864bb0
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106323750"
---
# <a name="id3dxeffectgetdevice-method"></a><span data-ttu-id="6fe37-103">Metodo ID3DXEffect:: GetDevice</span><span class="sxs-lookup"><span data-stu-id="6fe37-103">ID3DXEffect::GetDevice method</span></span>

<span data-ttu-id="6fe37-104">Recupera il dispositivo associato all'effetto.</span><span class="sxs-lookup"><span data-stu-id="6fe37-104">Retrieves the device associated with the effect.</span></span>

## <a name="syntax"></a><span data-ttu-id="6fe37-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="6fe37-105">Syntax</span></span>


```C++
HRESULT GetDevice(
  [out] LPDIRECT3DDEVICE9 *ppDevice
);
```



## <a name="parameters"></a><span data-ttu-id="6fe37-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="6fe37-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6fe37-107">*ppDevice* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="6fe37-107">*ppDevice* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6fe37-108">Tipo: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)\***</span><span class="sxs-lookup"><span data-stu-id="6fe37-108">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)\***</span></span>

<span data-ttu-id="6fe37-109">Indirizzo di un puntatore a un'interfaccia [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) , che rappresenta il dispositivo associato all'effetto.</span><span class="sxs-lookup"><span data-stu-id="6fe37-109">Address of a pointer to an [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) interface, representing the device associated with the effect.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6fe37-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="6fe37-110">Return value</span></span>

<span data-ttu-id="6fe37-111">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="6fe37-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="6fe37-112">Se il metodo ha esito positivo, il valore restituito è \_ OK.</span><span class="sxs-lookup"><span data-stu-id="6fe37-112">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="6fe37-113">Se il metodo ha esito negativo, il valore restituito può essere D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="6fe37-113">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="6fe37-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="6fe37-114">Remarks</span></span>

<span data-ttu-id="6fe37-115">La chiamata a questo metodo aumenterà il conteggio dei riferimenti interni per l'interfaccia [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) .</span><span class="sxs-lookup"><span data-stu-id="6fe37-115">Calling this method will increase the internal reference count for the [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) interface.</span></span> <span data-ttu-id="6fe37-116">Assicurarsi di chiamare IUnknown:: Release quando si è terminato di usare l'interfaccia **IDirect3DDevice9** o si disporrà di una perdita di memoria.</span><span class="sxs-lookup"><span data-stu-id="6fe37-116">Be sure to call IUnknown::Release when you are done using the **IDirect3DDevice9** interface or you will have a memory leak.</span></span>

## <a name="requirements"></a><span data-ttu-id="6fe37-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="6fe37-117">Requirements</span></span>



| <span data-ttu-id="6fe37-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="6fe37-118">Requirement</span></span> | <span data-ttu-id="6fe37-119">Valore</span><span class="sxs-lookup"><span data-stu-id="6fe37-119">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="6fe37-120">Intestazione</span><span class="sxs-lookup"><span data-stu-id="6fe37-120">Header</span></span><br/>  | <dl> <span data-ttu-id="6fe37-121"><dt>D3DX9Effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="6fe37-121"><dt>D3DX9Effect.h</dt></span></span> </dl> |
| <span data-ttu-id="6fe37-122">Libreria</span><span class="sxs-lookup"><span data-stu-id="6fe37-122">Library</span></span><br/> | <dl> <span data-ttu-id="6fe37-123"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="6fe37-123"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="6fe37-124">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="6fe37-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6fe37-125">ID3DXEffect</span><span class="sxs-lookup"><span data-stu-id="6fe37-125">ID3DXEffect</span></span>](id3dxeffect.md)
</dt> </dl>

 

 
