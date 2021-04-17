---
description: Imposta la dichiarazione del vertice.
ms.assetid: cbb802ac-f0ba-41e6-8c67-a787982f975f
title: 'Metodo ID3DXSkinInfo:: sedeclaration (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXSkinInfo.SetDeclaration
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 821801647ca1aee3deabe69d911bd1cab5f7eb4f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104354049"
---
# <a name="id3dxskininfosetdeclaration-method"></a><span data-ttu-id="3050a-103">Metodo ID3DXSkinInfo:: sedeclaration</span><span class="sxs-lookup"><span data-stu-id="3050a-103">ID3DXSkinInfo::SetDeclaration method</span></span>

<span data-ttu-id="3050a-104">Imposta la dichiarazione del vertice.</span><span class="sxs-lookup"><span data-stu-id="3050a-104">Sets the vertex declaration.</span></span>

## <a name="syntax"></a><span data-ttu-id="3050a-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="3050a-105">Syntax</span></span>


```C++
HRESULT SetDeclaration(
  [in] const D3DVERTEXELEMENT9 *pDeclaration
);
```



## <a name="parameters"></a><span data-ttu-id="3050a-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="3050a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3050a-107">*pDeclaration* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="3050a-107">*pDeclaration* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3050a-108">Tipo: **const [**D3DVERTEXELEMENT9**](d3dvertexelement9.md) \***</span><span class="sxs-lookup"><span data-stu-id="3050a-108">Type: **const [**D3DVERTEXELEMENT9**](d3dvertexelement9.md)\***</span></span>

<span data-ttu-id="3050a-109">Puntatore a una matrice di elementi [**D3DVERTEXELEMENT9**](d3dvertexelement9.md) .</span><span class="sxs-lookup"><span data-stu-id="3050a-109">Pointer to an array of [**D3DVERTEXELEMENT9**](d3dvertexelement9.md) elements.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3050a-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="3050a-110">Return value</span></span>

<span data-ttu-id="3050a-111">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="3050a-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="3050a-112">Se il metodo ha esito positivo, il valore restituito è D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="3050a-112">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="3050a-113">Se il metodo ha esito negativo, il valore restituito può essere D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="3050a-113">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="3050a-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="3050a-114">Requirements</span></span>



| <span data-ttu-id="3050a-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="3050a-115">Requirement</span></span> | <span data-ttu-id="3050a-116">Valore</span><span class="sxs-lookup"><span data-stu-id="3050a-116">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="3050a-117">Intestazione</span><span class="sxs-lookup"><span data-stu-id="3050a-117">Header</span></span><br/>  | <dl> <span data-ttu-id="3050a-118"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="3050a-118"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="3050a-119">Libreria</span><span class="sxs-lookup"><span data-stu-id="3050a-119">Library</span></span><br/> | <dl> <span data-ttu-id="3050a-120"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="3050a-120"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="3050a-121">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="3050a-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3050a-122">ID3DXSkinInfo</span><span class="sxs-lookup"><span data-stu-id="3050a-122">ID3DXSkinInfo</span></span>](id3dxskininfo.md)
</dt> <dt>

[<span data-ttu-id="3050a-123">**ID3DXSkinInfo:: getDeclaration**</span><span class="sxs-lookup"><span data-stu-id="3050a-123">**ID3DXSkinInfo::GetDeclaration**</span></span>](id3dxskininfo--getdeclaration.md)
</dt> </dl>

 

 




