---
description: Recupera il dispositivo Direct3D associato alla superficie di rendering.
ms.assetid: 579cf7da-b8e0-4d9f-93b8-b1f47c3d5654
title: 'Metodo ID3DXRenderToSurface:: GetDevice (D3dx9core. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXRenderToSurface.GetDevice
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: ac01744887412349c71daa34194fc3a0b03b19a9
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104355834"
---
# <a name="id3dxrendertosurfacegetdevice-method"></a><span data-ttu-id="80d37-103">Metodo ID3DXRenderToSurface:: GetDevice</span><span class="sxs-lookup"><span data-stu-id="80d37-103">ID3DXRenderToSurface::GetDevice method</span></span>

<span data-ttu-id="80d37-104">Recupera il dispositivo Direct3D associato alla superficie di rendering.</span><span class="sxs-lookup"><span data-stu-id="80d37-104">Retrieves the Direct3D device associated with the render surface.</span></span>

## <a name="syntax"></a><span data-ttu-id="80d37-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="80d37-105">Syntax</span></span>


```C++
HRESULT GetDevice(
  [out, retval] LPDIRECT3DDEVICE9 *ppDevice
);
```



## <a name="parameters"></a><span data-ttu-id="80d37-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="80d37-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="80d37-107">*ppDevice* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="80d37-107">*ppDevice* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="80d37-108">Tipo: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)\***</span><span class="sxs-lookup"><span data-stu-id="80d37-108">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)\***</span></span>

<span data-ttu-id="80d37-109">Indirizzo di un puntatore a un'interfaccia [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) , che rappresenta l'oggetto dispositivo Direct3D associato alla superficie di rendering.</span><span class="sxs-lookup"><span data-stu-id="80d37-109">Address of a pointer to an [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) interface, representing the Direct3D device object associated with the render surface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="80d37-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="80d37-110">Return value</span></span>

<span data-ttu-id="80d37-111">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="80d37-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="80d37-112">Se il metodo ha esito positivo, il valore restituito è D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="80d37-112">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="80d37-113">Se il metodo ha esito negativo, il valore restituito può essere D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="80d37-113">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span> <span data-ttu-id="80d37-114">La chiamata a questo metodo aumenterà il conteggio dei riferimenti interni nell'interfaccia [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) .</span><span class="sxs-lookup"><span data-stu-id="80d37-114">Calling this method will increase the internal reference count on the [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) interface.</span></span> <span data-ttu-id="80d37-115">Assicurarsi di chiamare [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) al termine dell'uso di questa interfaccia **IDirect3DDevice9** o si disporrà di una perdita di memoria.</span><span class="sxs-lookup"><span data-stu-id="80d37-115">Be sure to call [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) when you are done using this **IDirect3DDevice9** interface or you will have a memory leak.</span></span>

## <a name="requirements"></a><span data-ttu-id="80d37-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="80d37-116">Requirements</span></span>



| <span data-ttu-id="80d37-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="80d37-117">Requirement</span></span> | <span data-ttu-id="80d37-118">Valore</span><span class="sxs-lookup"><span data-stu-id="80d37-118">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="80d37-119">Intestazione</span><span class="sxs-lookup"><span data-stu-id="80d37-119">Header</span></span><br/>  | <dl> <span data-ttu-id="80d37-120"><dt>D3dx9core. h</dt></span><span class="sxs-lookup"><span data-stu-id="80d37-120"><dt>D3dx9core.h</dt></span></span> </dl> |
| <span data-ttu-id="80d37-121">Libreria</span><span class="sxs-lookup"><span data-stu-id="80d37-121">Library</span></span><br/> | <dl> <span data-ttu-id="80d37-122"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="80d37-122"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="80d37-123">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="80d37-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="80d37-124">ID3DXRenderToSurface</span><span class="sxs-lookup"><span data-stu-id="80d37-124">ID3DXRenderToSurface</span></span>](id3dxrendertosurface.md)
</dt> </dl>

 

 
