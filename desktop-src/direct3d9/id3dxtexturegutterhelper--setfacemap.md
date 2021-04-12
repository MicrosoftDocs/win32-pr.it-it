---
description: Imposta l'indice della faccia mesh a cui appartiene ogni Texel.
ms.assetid: 45d931bc-fb8b-48da-b30d-99d5dc183494
title: 'Metodo ID3DXTextureGutterHelper:: SetFaceMap (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXTextureGutterHelper.SetFaceMap
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 8ba0472052d5e2e06d759c83a404a197ecda148f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104235161"
---
# <a name="id3dxtexturegutterhelpersetfacemap-method"></a><span data-ttu-id="ac07b-103">Metodo ID3DXTextureGutterHelper:: SetFaceMap</span><span class="sxs-lookup"><span data-stu-id="ac07b-103">ID3DXTextureGutterHelper::SetFaceMap method</span></span>

<span data-ttu-id="ac07b-104">Imposta l'indice della faccia mesh a cui appartiene ogni Texel.</span><span class="sxs-lookup"><span data-stu-id="ac07b-104">Sets the index of the mesh face to which each texel belongs.</span></span>

## <a name="syntax"></a><span data-ttu-id="ac07b-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="ac07b-105">Syntax</span></span>


```C++
HRESULT SetFaceMap(
  [in] UINT *pFaceData
);
```



## <a name="parameters"></a><span data-ttu-id="ac07b-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="ac07b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ac07b-107">*pFaceData* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ac07b-107">*pFaceData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ac07b-108">Tipo: **[ **uint**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="ac07b-108">Type: **[**UINT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="ac07b-109">Puntatore all'indice della faccia mesh a cui appartiene ogni Texel.</span><span class="sxs-lookup"><span data-stu-id="ac07b-109">Pointer to the index of the mesh face to which each texel belongs.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ac07b-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="ac07b-110">Return value</span></span>

<span data-ttu-id="ac07b-111">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="ac07b-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="ac07b-112">Se il metodo ha esito positivo, il valore restituito è \_ OK.</span><span class="sxs-lookup"><span data-stu-id="ac07b-112">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="ac07b-113">Se il metodo ha esito negativo, verrà restituito il valore seguente. \_INVALIDCALL D3DERR</span><span class="sxs-lookup"><span data-stu-id="ac07b-113">If the method fails, the following value will be returned.D3DERR\_INVALIDCALL</span></span>

## <a name="remarks"></a><span data-ttu-id="ac07b-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="ac07b-114">Remarks</span></span>

<span data-ttu-id="ac07b-115">L'input dei dati della faccia mesh per questo metodo è valido solo per Texel validi (non di classe 0).</span><span class="sxs-lookup"><span data-stu-id="ac07b-115">The mesh face data input to this method is valid only for valid (non-class 0) texels.</span></span> <span data-ttu-id="ac07b-116">[**ID3DXTextureGutterHelper:: GetGutterMap**](id3dxtexturegutterhelper--getguttermap.md) restituirà valori diversi da zero per i Texel validi.</span><span class="sxs-lookup"><span data-stu-id="ac07b-116">[**ID3DXTextureGutterHelper::GetGutterMap**](id3dxtexturegutterhelper--getguttermap.md) will return non-zero values for valid texels.</span></span>

## <a name="requirements"></a><span data-ttu-id="ac07b-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ac07b-117">Requirements</span></span>



| <span data-ttu-id="ac07b-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="ac07b-118">Requirement</span></span> | <span data-ttu-id="ac07b-119">Valore</span><span class="sxs-lookup"><span data-stu-id="ac07b-119">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="ac07b-120">Intestazione</span><span class="sxs-lookup"><span data-stu-id="ac07b-120">Header</span></span><br/>  | <dl> <span data-ttu-id="ac07b-121"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="ac07b-121"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="ac07b-122">Libreria</span><span class="sxs-lookup"><span data-stu-id="ac07b-122">Library</span></span><br/> | <dl> <span data-ttu-id="ac07b-123"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="ac07b-123"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="ac07b-124">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="ac07b-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ac07b-125">ID3DXTextureGutterHelper</span><span class="sxs-lookup"><span data-stu-id="ac07b-125">ID3DXTextureGutterHelper</span></span>](id3dxtexturegutterhelper.md)
</dt> </dl>

 

 
