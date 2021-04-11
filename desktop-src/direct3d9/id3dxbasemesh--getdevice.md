---
description: Recupera il dispositivo associato alla mesh.
ms.assetid: 16ff5267-0c64-4c3d-925d-6fc10f54c9c4
title: 'Metodo ID3DXBaseMesh:: GetDevice (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseMesh.GetDevice
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 2b866c86bf759305a4626f0ff5ecaa8e35bfd75d
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104058632"
---
# <a name="id3dxbasemeshgetdevice-method"></a><span data-ttu-id="0041d-103">Metodo ID3DXBaseMesh:: GetDevice</span><span class="sxs-lookup"><span data-stu-id="0041d-103">ID3DXBaseMesh::GetDevice method</span></span>

<span data-ttu-id="0041d-104">Recupera il dispositivo associato alla mesh.</span><span class="sxs-lookup"><span data-stu-id="0041d-104">Retrieves the device associated with the mesh.</span></span>

## <a name="syntax"></a><span data-ttu-id="0041d-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="0041d-105">Syntax</span></span>


```C++
HRESULT GetDevice(
  [out, retval] LPDIRECT3DDEVICE9 *ppDevice
);
```



## <a name="parameters"></a><span data-ttu-id="0041d-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="0041d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0041d-107">*ppDevice* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="0041d-107">*ppDevice* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="0041d-108">Tipo: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)\***</span><span class="sxs-lookup"><span data-stu-id="0041d-108">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)\***</span></span>

<span data-ttu-id="0041d-109">Indirizzo di un puntatore a un'interfaccia [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) , che rappresenta l'oggetto dispositivo Direct3D associato alla mesh.</span><span class="sxs-lookup"><span data-stu-id="0041d-109">Address of a pointer to an [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) interface, representing the Direct3D device object associated with the mesh.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0041d-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="0041d-110">Return value</span></span>

<span data-ttu-id="0041d-111">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="0041d-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="0041d-112">Se il metodo ha esito positivo, il valore restituito è D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="0041d-112">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="0041d-113">Se il metodo ha esito negativo, il valore restituito può essere D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="0041d-113">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="0041d-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="0041d-114">Remarks</span></span>

<span data-ttu-id="0041d-115">La chiamata a questo metodo aumenterà il conteggio dei riferimenti interni nell'interfaccia [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) .</span><span class="sxs-lookup"><span data-stu-id="0041d-115">Calling this method will increase the internal reference count on the [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) interface.</span></span> <span data-ttu-id="0041d-116">Assicurarsi di chiamare [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) al termine dell'uso di questa interfaccia **IDirect3DDevice9** o si disporrà di una perdita di memoria.</span><span class="sxs-lookup"><span data-stu-id="0041d-116">Be sure to call [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) when you are done using this **IDirect3DDevice9** interface or you will have a memory leak.</span></span>

## <a name="requirements"></a><span data-ttu-id="0041d-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="0041d-117">Requirements</span></span>



| <span data-ttu-id="0041d-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="0041d-118">Requirement</span></span> | <span data-ttu-id="0041d-119">Valore</span><span class="sxs-lookup"><span data-stu-id="0041d-119">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="0041d-120">Intestazione</span><span class="sxs-lookup"><span data-stu-id="0041d-120">Header</span></span><br/>  | <dl> <span data-ttu-id="0041d-121"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="0041d-121"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="0041d-122">Libreria</span><span class="sxs-lookup"><span data-stu-id="0041d-122">Library</span></span><br/> | <dl> <span data-ttu-id="0041d-123"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="0041d-123"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="0041d-124">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="0041d-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0041d-125">ID3DXBaseMesh</span><span class="sxs-lookup"><span data-stu-id="0041d-125">ID3DXBaseMesh</span></span>](id3dxbasemesh.md)
</dt> </dl>

 

 
