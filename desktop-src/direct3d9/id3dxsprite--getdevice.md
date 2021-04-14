---
description: Recupera il dispositivo associato all'oggetto Sprite.
ms.assetid: 9ce18623-893e-4395-bdf7-8d16a641a557
title: 'Metodo ID3DXSprite:: GetDevice (D3dx9core. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXSprite.GetDevice
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: cf98eb932971a22232a5dbc8f0d5449f8639db97
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104401995"
---
# <a name="id3dxspritegetdevice-method"></a><span data-ttu-id="f5dd1-103">Metodo ID3DXSprite:: GetDevice</span><span class="sxs-lookup"><span data-stu-id="f5dd1-103">ID3DXSprite::GetDevice method</span></span>

<span data-ttu-id="f5dd1-104">Recupera il dispositivo associato all'oggetto Sprite.</span><span class="sxs-lookup"><span data-stu-id="f5dd1-104">Retrieves the device associated with the sprite object.</span></span>

## <a name="syntax"></a><span data-ttu-id="f5dd1-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="f5dd1-105">Syntax</span></span>


```C++
HRESULT GetDevice(
  [out, retval] LPDIRECT3DDEVICE9 *ppDevice
);
```



## <a name="parameters"></a><span data-ttu-id="f5dd1-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="f5dd1-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f5dd1-107">*ppDevice* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="f5dd1-107">*ppDevice* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="f5dd1-108">Tipo: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)\***</span><span class="sxs-lookup"><span data-stu-id="f5dd1-108">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)\***</span></span>

<span data-ttu-id="f5dd1-109">Indirizzo di un puntatore a un'interfaccia [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) , che rappresenta l'oggetto dispositivo Direct3D associato all'oggetto Sprite.</span><span class="sxs-lookup"><span data-stu-id="f5dd1-109">Address of a pointer to an [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) interface, representing the Direct3D device object associated with the sprite object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f5dd1-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="f5dd1-110">Return value</span></span>

<span data-ttu-id="f5dd1-111">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="f5dd1-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="f5dd1-112">Se il metodo ha esito positivo, il valore restituito è \_ OK.</span><span class="sxs-lookup"><span data-stu-id="f5dd1-112">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="f5dd1-113">Se il metodo ha esito negativo, verrà restituito il valore seguente. \_INVALIDCALL D3DERR</span><span class="sxs-lookup"><span data-stu-id="f5dd1-113">If the method fails, the following value will be returned.D3DERR\_INVALIDCALL</span></span>

## <a name="remarks"></a><span data-ttu-id="f5dd1-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="f5dd1-114">Remarks</span></span>

<span data-ttu-id="f5dd1-115">La chiamata a questo metodo aumenterà il conteggio dei riferimenti interni nell'interfaccia [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) .</span><span class="sxs-lookup"><span data-stu-id="f5dd1-115">Calling this method will increase the internal reference count on the [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) interface.</span></span>

## <a name="requirements"></a><span data-ttu-id="f5dd1-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f5dd1-116">Requirements</span></span>



| <span data-ttu-id="f5dd1-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="f5dd1-117">Requirement</span></span> | <span data-ttu-id="f5dd1-118">Valore</span><span class="sxs-lookup"><span data-stu-id="f5dd1-118">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="f5dd1-119">Intestazione</span><span class="sxs-lookup"><span data-stu-id="f5dd1-119">Header</span></span><br/>  | <dl> <span data-ttu-id="f5dd1-120"><dt>D3dx9core. h</dt></span><span class="sxs-lookup"><span data-stu-id="f5dd1-120"><dt>D3dx9core.h</dt></span></span> </dl> |
| <span data-ttu-id="f5dd1-121">Libreria</span><span class="sxs-lookup"><span data-stu-id="f5dd1-121">Library</span></span><br/> | <dl> <span data-ttu-id="f5dd1-122"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="f5dd1-122"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="f5dd1-123">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="f5dd1-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f5dd1-124">ID3DXSprite</span><span class="sxs-lookup"><span data-stu-id="f5dd1-124">ID3DXSprite</span></span>](id3dxsprite.md)
</dt> </dl>

 

 
