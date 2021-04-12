---
description: Recupera il dispositivo Direct3D associato all'oggetto del tipo di carattere.
ms.assetid: c713cbe2-6e6e-476b-a995-14fa149cb088
title: 'Metodo ID3DXFont:: GetDevice (D3dx9core. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXFont.GetDevice
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 2de1b6e2c3b2c2b61576c739d96abc8b8fc8851a
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104355854"
---
# <a name="id3dxfontgetdevice-method"></a><span data-ttu-id="68c02-103">Metodo ID3DXFont:: GetDevice</span><span class="sxs-lookup"><span data-stu-id="68c02-103">ID3DXFont::GetDevice method</span></span>

<span data-ttu-id="68c02-104">Recupera il dispositivo Direct3D associato all'oggetto del tipo di carattere.</span><span class="sxs-lookup"><span data-stu-id="68c02-104">Retrieves the Direct3D device associated with the font object.</span></span>

## <a name="syntax"></a><span data-ttu-id="68c02-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="68c02-105">Syntax</span></span>


```C++
HRESULT GetDevice(
  [out] LPDIRECT3DDEVICE9 *ppDevice
);
```



## <a name="parameters"></a><span data-ttu-id="68c02-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="68c02-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="68c02-107">*ppDevice* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="68c02-107">*ppDevice* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="68c02-108">Tipo: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)\***</span><span class="sxs-lookup"><span data-stu-id="68c02-108">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)\***</span></span>

<span data-ttu-id="68c02-109">Indirizzo di un puntatore a un'interfaccia [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) , che rappresenta l'oggetto dispositivo Direct3D associato all'oggetto del tipo di carattere.</span><span class="sxs-lookup"><span data-stu-id="68c02-109">Address of a pointer to an [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) interface, representing the Direct3D device object associated with the font object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="68c02-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="68c02-110">Return value</span></span>

<span data-ttu-id="68c02-111">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="68c02-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="68c02-112">Se il metodo ha esito positivo, il valore restituito è \_ OK.</span><span class="sxs-lookup"><span data-stu-id="68c02-112">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="68c02-113">Se il metodo ha esito negativo, il valore restituito può essere uno dei seguenti: D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA.</span><span class="sxs-lookup"><span data-stu-id="68c02-113">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA.</span></span>

## <a name="remarks"></a><span data-ttu-id="68c02-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="68c02-114">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="68c02-115">La chiamata a questo metodo aumenterà il conteggio dei riferimenti interni nell'interfaccia [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) .</span><span class="sxs-lookup"><span data-stu-id="68c02-115">Calling this method will increase the internal reference count on the [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) interface.</span></span> <span data-ttu-id="68c02-116">Assicurarsi di chiamare [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) al termine dell'uso di questa interfaccia **IDirect3DDevice9** o si disporrà di una perdita di memoria.</span><span class="sxs-lookup"><span data-stu-id="68c02-116">Be sure to call [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) when you are done using this **IDirect3DDevice9** interface or you will have a memory leak.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="68c02-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="68c02-117">Requirements</span></span>



| <span data-ttu-id="68c02-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="68c02-118">Requirement</span></span> | <span data-ttu-id="68c02-119">Valore</span><span class="sxs-lookup"><span data-stu-id="68c02-119">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="68c02-120">Intestazione</span><span class="sxs-lookup"><span data-stu-id="68c02-120">Header</span></span><br/>  | <dl> <span data-ttu-id="68c02-121"><dt>D3dx9core. h</dt></span><span class="sxs-lookup"><span data-stu-id="68c02-121"><dt>D3dx9core.h</dt></span></span> </dl> |
| <span data-ttu-id="68c02-122">Libreria</span><span class="sxs-lookup"><span data-stu-id="68c02-122">Library</span></span><br/> | <dl> <span data-ttu-id="68c02-123"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="68c02-123"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="68c02-124">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="68c02-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="68c02-125">ID3DXFont</span><span class="sxs-lookup"><span data-stu-id="68c02-125">ID3DXFont</span></span>](id3dxfont.md)
</dt> </dl>

 

 
