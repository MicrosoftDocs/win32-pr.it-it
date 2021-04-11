---
description: Ottiene una descrizione della tabella delle costanti.
ms.assetid: 91b537bb-5f7a-448b-a21f-c0ddf66d7238
title: 'Metodo ID3DXTextureShader:: getdesc (D3DX9Shader. h)'
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
ms.openlocfilehash: 97302b7e0f8c9f05e6229e20c2c9c158173ed944
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104235044"
---
# <a name="id3dxtextureshadergetdesc-method"></a><span data-ttu-id="39e1b-103">Metodo ID3DXTextureShader:: getdesc</span><span class="sxs-lookup"><span data-stu-id="39e1b-103">ID3DXTextureShader::GetDesc method</span></span>

<span data-ttu-id="39e1b-104">Ottiene una descrizione della tabella delle costanti.</span><span class="sxs-lookup"><span data-stu-id="39e1b-104">Gets a description of the constant table.</span></span>

## <a name="syntax"></a><span data-ttu-id="39e1b-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="39e1b-105">Syntax</span></span>


```C++
HRESULT GetDesc(
  [in] D3DXCONSTANTTABLE_DESC *pDesc
);
```



## <a name="parameters"></a><span data-ttu-id="39e1b-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="39e1b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="39e1b-107">*pDesc* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="39e1b-107">*pDesc* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="39e1b-108">Tipo: **[ **D3DXCONSTANTTABLE \_ desc**](d3dxconstanttable-desc.md)\***</span><span class="sxs-lookup"><span data-stu-id="39e1b-108">Type: **[**D3DXCONSTANTTABLE\_DESC**](d3dxconstanttable-desc.md)\***</span></span>

<span data-ttu-id="39e1b-109">Attributi della tabella delle costanti.</span><span class="sxs-lookup"><span data-stu-id="39e1b-109">The attributes of the constant table.</span></span> <span data-ttu-id="39e1b-110">Vedere [**D3DXCONSTANTTABLE \_ desc**](d3dxconstanttable-desc.md).</span><span class="sxs-lookup"><span data-stu-id="39e1b-110">See [**D3DXCONSTANTTABLE\_DESC**](d3dxconstanttable-desc.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="39e1b-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="39e1b-111">Return value</span></span>

<span data-ttu-id="39e1b-112">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="39e1b-112">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="39e1b-113">Se il metodo ha esito positivo, il valore restituito è D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="39e1b-113">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="39e1b-114">Se il metodo ha esito negativo, il valore restituito può essere uno dei seguenti: D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA.</span><span class="sxs-lookup"><span data-stu-id="39e1b-114">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA.</span></span>

## <a name="requirements"></a><span data-ttu-id="39e1b-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="39e1b-115">Requirements</span></span>



| <span data-ttu-id="39e1b-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="39e1b-116">Requirement</span></span> | <span data-ttu-id="39e1b-117">Valore</span><span class="sxs-lookup"><span data-stu-id="39e1b-117">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="39e1b-118">Intestazione</span><span class="sxs-lookup"><span data-stu-id="39e1b-118">Header</span></span><br/>  | <dl> <span data-ttu-id="39e1b-119"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="39e1b-119"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="39e1b-120">Libreria</span><span class="sxs-lookup"><span data-stu-id="39e1b-120">Library</span></span><br/> | <dl> <span data-ttu-id="39e1b-121"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="39e1b-121"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="39e1b-122">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="39e1b-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="39e1b-123">ID3DXTextureShader</span><span class="sxs-lookup"><span data-stu-id="39e1b-123">ID3DXTextureShader</span></span>](id3dxtextureshader.md)
</dt> </dl>

 

 




