---
description: Recupera il dispositivo Direct3D associato alla mappa dell'ambiente.
ms.assetid: 15f342c5-7665-443a-b7b8-32cc67034c41
title: 'Metodo ID3DXRenderToEnvMap:: GetDevice (D3dx9core. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXRenderToEnvMap.GetDevice
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 8b5adc045beeefa220a849a6da752a8d3efc82ff
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322445"
---
# <a name="id3dxrendertoenvmapgetdevice-method"></a><span data-ttu-id="a9a83-103">Metodo ID3DXRenderToEnvMap:: GetDevice</span><span class="sxs-lookup"><span data-stu-id="a9a83-103">ID3DXRenderToEnvMap::GetDevice method</span></span>

<span data-ttu-id="a9a83-104">Recupera il dispositivo Direct3D associato alla mappa dell'ambiente.</span><span class="sxs-lookup"><span data-stu-id="a9a83-104">Retrieves the Direct3D device associated with the environment map.</span></span>

## <a name="syntax"></a><span data-ttu-id="a9a83-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="a9a83-105">Syntax</span></span>


```C++
HRESULT GetDevice(
  [out, retval] LPDIRECT3DDEVICE9 *ppDevice
);
```



## <a name="parameters"></a><span data-ttu-id="a9a83-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="a9a83-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a9a83-107">*ppDevice* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="a9a83-107">*ppDevice* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="a9a83-108">Tipo: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)\***</span><span class="sxs-lookup"><span data-stu-id="a9a83-108">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)\***</span></span>

<span data-ttu-id="a9a83-109">Indirizzo di un puntatore a un'interfaccia [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) che rappresenta l'oggetto dispositivo Direct3D associato alla mappa dell'ambiente.</span><span class="sxs-lookup"><span data-stu-id="a9a83-109">Address of a pointer to an [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) interface that represents the Direct3D device object associated with the environment map.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a9a83-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="a9a83-110">Return value</span></span>

<span data-ttu-id="a9a83-111">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="a9a83-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="a9a83-112">Se il metodo ha esito positivo, il valore restituito è D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="a9a83-112">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="a9a83-113">Se il metodo ha esito negativo, il valore restituito può essere D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="a9a83-113">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span> <span data-ttu-id="a9a83-114">La chiamata a questo metodo aumenta il conteggio dei riferimenti interni nell'interfaccia [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) .</span><span class="sxs-lookup"><span data-stu-id="a9a83-114">Calling this method increases the internal reference count on the [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) interface.</span></span> <span data-ttu-id="a9a83-115">Assicurarsi di chiamare [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) al termine dell'uso di questa interfaccia **IDirect3DDevice9** o si disporrà di una perdita di memoria.</span><span class="sxs-lookup"><span data-stu-id="a9a83-115">Be sure to call [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) when you are done using this **IDirect3DDevice9** interface or you will have a memory leak.</span></span>

## <a name="requirements"></a><span data-ttu-id="a9a83-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a9a83-116">Requirements</span></span>



| <span data-ttu-id="a9a83-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="a9a83-117">Requirement</span></span> | <span data-ttu-id="a9a83-118">Valore</span><span class="sxs-lookup"><span data-stu-id="a9a83-118">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="a9a83-119">Intestazione</span><span class="sxs-lookup"><span data-stu-id="a9a83-119">Header</span></span><br/>  | <dl> <span data-ttu-id="a9a83-120"><dt>D3dx9core. h</dt></span><span class="sxs-lookup"><span data-stu-id="a9a83-120"><dt>D3dx9core.h</dt></span></span> </dl> |
| <span data-ttu-id="a9a83-121">Libreria</span><span class="sxs-lookup"><span data-stu-id="a9a83-121">Library</span></span><br/> | <dl> <span data-ttu-id="a9a83-122"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="a9a83-122"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="a9a83-123">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a9a83-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a9a83-124">ID3DXRenderToEnvMap</span><span class="sxs-lookup"><span data-stu-id="a9a83-124">ID3DXRenderToEnvMap</span></span>](id3dxrendertoenvmap.md)
</dt> </dl>

 

 
