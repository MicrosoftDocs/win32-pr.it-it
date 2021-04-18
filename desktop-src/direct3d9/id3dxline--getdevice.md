---
description: Recupera il dispositivo Direct3D associato all'oggetto riga.
ms.assetid: 42459668-aa18-478d-82d9-b8b25dc4a898
title: 'Metodo ID3DXLine:: GetDevice (D3dx9core. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXLine.GetDevice
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: a97edf37d14edce4982d62d76f9429091ad491ce
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106323734"
---
# <a name="id3dxlinegetdevice-method"></a><span data-ttu-id="ac8d2-103">Metodo ID3DXLine:: GetDevice</span><span class="sxs-lookup"><span data-stu-id="ac8d2-103">ID3DXLine::GetDevice method</span></span>

<span data-ttu-id="ac8d2-104">Recupera il dispositivo Direct3D associato all'oggetto riga.</span><span class="sxs-lookup"><span data-stu-id="ac8d2-104">Retrieves the Direct3D device associated with the line object.</span></span>

## <a name="syntax"></a><span data-ttu-id="ac8d2-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="ac8d2-105">Syntax</span></span>


```C++
HRESULT GetDevice(
  [out, retval] LPDIRECT3DDEVICE9 *ppDevice
);
```



## <a name="parameters"></a><span data-ttu-id="ac8d2-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="ac8d2-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ac8d2-107">*ppDevice* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="ac8d2-107">*ppDevice* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="ac8d2-108">Tipo: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)\***</span><span class="sxs-lookup"><span data-stu-id="ac8d2-108">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)\***</span></span>

<span data-ttu-id="ac8d2-109">Indirizzo di un puntatore a un'interfaccia [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) , che rappresenta l'oggetto dispositivo Direct3D associato all'oggetto riga.</span><span class="sxs-lookup"><span data-stu-id="ac8d2-109">Address of a pointer to an [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) interface, representing the Direct3D device object associated with the line object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ac8d2-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="ac8d2-110">Return value</span></span>

<span data-ttu-id="ac8d2-111">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="ac8d2-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="ac8d2-112">Se il metodo ha esito positivo, il valore restituito è D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="ac8d2-112">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="ac8d2-113">Se il metodo ha esito negativo, il valore restituito può essere uno dei seguenti: D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA.</span><span class="sxs-lookup"><span data-stu-id="ac8d2-113">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA.</span></span>

## <a name="requirements"></a><span data-ttu-id="ac8d2-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ac8d2-114">Requirements</span></span>



| <span data-ttu-id="ac8d2-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="ac8d2-115">Requirement</span></span> | <span data-ttu-id="ac8d2-116">Valore</span><span class="sxs-lookup"><span data-stu-id="ac8d2-116">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="ac8d2-117">Intestazione</span><span class="sxs-lookup"><span data-stu-id="ac8d2-117">Header</span></span><br/>  | <dl> <span data-ttu-id="ac8d2-118"><dt>D3dx9core. h</dt></span><span class="sxs-lookup"><span data-stu-id="ac8d2-118"><dt>D3dx9core.h</dt></span></span> </dl> |
| <span data-ttu-id="ac8d2-119">Libreria</span><span class="sxs-lookup"><span data-stu-id="ac8d2-119">Library</span></span><br/> | <dl> <span data-ttu-id="ac8d2-120"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="ac8d2-120"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="ac8d2-121">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="ac8d2-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ac8d2-122">ID3DXLine</span><span class="sxs-lookup"><span data-stu-id="ac8d2-122">ID3DXLine</span></span>](id3dxline.md)
</dt> </dl>

 

 
