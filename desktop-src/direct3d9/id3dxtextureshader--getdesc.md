---
description: 'Metodo ID3DXTextureShader::GetDesc: ottiene una descrizione della tabella costante.'
ms.assetid: 91b537bb-5f7a-448b-a21f-c0ddf66d7238
title: Metodo ID3DXTextureShader::GetDesc (D3DX9Shader.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXTextureShader.GetDesc
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 6ea94f0e22d838f09dae9b423f85aa1d55d2365b
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108117639"
---
# <a name="id3dxtextureshadergetdesc-method"></a><span data-ttu-id="9e8e5-103">Metodo ID3DXTextureShader::GetDesc</span><span class="sxs-lookup"><span data-stu-id="9e8e5-103">ID3DXTextureShader::GetDesc method</span></span>

<span data-ttu-id="9e8e5-104">Ottiene una descrizione della tabella delle costanti.</span><span class="sxs-lookup"><span data-stu-id="9e8e5-104">Gets a description of the constant table.</span></span>

## <a name="syntax"></a><span data-ttu-id="9e8e5-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="9e8e5-105">Syntax</span></span>


```C++
HRESULT GetDesc(
  [in] D3DXCONSTANTTABLE_DESC *pDesc
);
```



## <a name="parameters"></a><span data-ttu-id="9e8e5-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="9e8e5-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9e8e5-107">*pDesc* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="9e8e5-107">*pDesc* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9e8e5-108">Tipo: **[ **D3DXCONSTANTTABLE \_ DESC**](d3dxconstanttable-desc.md)\***</span><span class="sxs-lookup"><span data-stu-id="9e8e5-108">Type: **[**D3DXCONSTANTTABLE\_DESC**](d3dxconstanttable-desc.md)\***</span></span>

<span data-ttu-id="9e8e5-109">Attributi della tabella delle costanti.</span><span class="sxs-lookup"><span data-stu-id="9e8e5-109">The attributes of the constant table.</span></span> <span data-ttu-id="9e8e5-110">Vedere [**D3DXCONSTANTTABLE \_ DESC**](d3dxconstanttable-desc.md).</span><span class="sxs-lookup"><span data-stu-id="9e8e5-110">See [**D3DXCONSTANTTABLE\_DESC**](d3dxconstanttable-desc.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9e8e5-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="9e8e5-111">Return value</span></span>

<span data-ttu-id="9e8e5-112">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="9e8e5-112">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="9e8e5-113">Se il metodo ha esito positivo, il valore restituito è D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="9e8e5-113">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="9e8e5-114">Se il metodo ha esito negativo, il valore restituito può essere uno dei seguenti: D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA.</span><span class="sxs-lookup"><span data-stu-id="9e8e5-114">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA.</span></span>

## <a name="requirements"></a><span data-ttu-id="9e8e5-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="9e8e5-115">Requirements</span></span>



| <span data-ttu-id="9e8e5-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="9e8e5-116">Requirement</span></span> | <span data-ttu-id="9e8e5-117">Valore</span><span class="sxs-lookup"><span data-stu-id="9e8e5-117">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="9e8e5-118">Intestazione</span><span class="sxs-lookup"><span data-stu-id="9e8e5-118">Header</span></span><br/>  | <dl> <span data-ttu-id="9e8e5-119"><dt>D3DX9Shader.h</dt></span><span class="sxs-lookup"><span data-stu-id="9e8e5-119"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="9e8e5-120">Libreria</span><span class="sxs-lookup"><span data-stu-id="9e8e5-120">Library</span></span><br/> | <dl> <span data-ttu-id="9e8e5-121"><dt>D3dx9.lib</dt></span><span class="sxs-lookup"><span data-stu-id="9e8e5-121"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="9e8e5-122">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="9e8e5-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9e8e5-123">ID3DXTextureShader</span><span class="sxs-lookup"><span data-stu-id="9e8e5-123">ID3DXTextureShader</span></span>](id3dxtextureshader.md)
</dt> </dl>

 

 




