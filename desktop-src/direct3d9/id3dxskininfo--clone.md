---
description: Clona un oggetto info di interfaccia.
ms.assetid: 82d0a78a-95f3-4b09-bc1a-b4bc663e0850
title: 'Metodo ID3DXSkinInfo:: Clone (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXSkinInfo.Clone
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: edd9776b75d027a32b32b58c59fc82daaebfa3ad
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104234987"
---
# <a name="id3dxskininfoclone-method"></a><span data-ttu-id="de465-103">Metodo ID3DXSkinInfo:: Clone</span><span class="sxs-lookup"><span data-stu-id="de465-103">ID3DXSkinInfo::Clone method</span></span>

<span data-ttu-id="de465-104">Clona un oggetto info di interfaccia.</span><span class="sxs-lookup"><span data-stu-id="de465-104">Clones a skin info object.</span></span>

## <a name="syntax"></a><span data-ttu-id="de465-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="de465-105">Syntax</span></span>


```C++
HRESULT Clone(
  [in, out] LPD3DXSKININFO *ppSkinInfo
);
```



## <a name="parameters"></a><span data-ttu-id="de465-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="de465-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="de465-107">*ppSkinInfo* \[ in uscita\]</span><span class="sxs-lookup"><span data-stu-id="de465-107">*ppSkinInfo* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="de465-108">Tipo: **[ **LPD3DXSKININFO**](id3dxskininfo.md)\***</span><span class="sxs-lookup"><span data-stu-id="de465-108">Type: **[**LPD3DXSKININFO**](id3dxskininfo.md)\***</span></span>

<span data-ttu-id="de465-109">Indirizzo di un puntatore a un oggetto [**ID3DXSkinInfo**](id3dxskininfo.md) , che conterrà l'oggetto clonato se il metodo ha esito positivo.</span><span class="sxs-lookup"><span data-stu-id="de465-109">Address of a pointer to an [**ID3DXSkinInfo**](id3dxskininfo.md) object, which will contain the cloned object if the method is successful.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="de465-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="de465-110">Return value</span></span>

<span data-ttu-id="de465-111">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="de465-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="de465-112">Se il metodo ha esito positivo, il valore restituito è D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="de465-112">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="de465-113">Se il metodo ha esito negativo, il valore restituito può essere D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="de465-113">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="de465-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="de465-114">Requirements</span></span>



| <span data-ttu-id="de465-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="de465-115">Requirement</span></span> | <span data-ttu-id="de465-116">Valore</span><span class="sxs-lookup"><span data-stu-id="de465-116">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="de465-117">Intestazione</span><span class="sxs-lookup"><span data-stu-id="de465-117">Header</span></span><br/>  | <dl> <span data-ttu-id="de465-118"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="de465-118"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="de465-119">Libreria</span><span class="sxs-lookup"><span data-stu-id="de465-119">Library</span></span><br/> | <dl> <span data-ttu-id="de465-120"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="de465-120"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="de465-121">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="de465-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="de465-122">ID3DXSkinInfo</span><span class="sxs-lookup"><span data-stu-id="de465-122">ID3DXSkinInfo</span></span>](id3dxskininfo.md)
</dt> </dl>

 

 




