---
description: Salva una trama in memoria.
ms.assetid: be541b99-6d07-480e-8f28-b7fc44566e7d
title: Funzione D3DX10SaveTextureToMemory (D3DX10Tex. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10SaveTextureToMemory
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: f20278f9fc590e72f93051d5fdd4cfbd918098df
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322768"
---
# <a name="d3dx10savetexturetomemory-function"></a><span data-ttu-id="89f32-103">D3DX10SaveTextureToMemory (funzione)</span><span class="sxs-lookup"><span data-stu-id="89f32-103">D3DX10SaveTextureToMemory function</span></span>

<span data-ttu-id="89f32-104">Salva una trama in memoria.</span><span class="sxs-lookup"><span data-stu-id="89f32-104">Save a texture to memory.</span></span>

## <a name="syntax"></a><span data-ttu-id="89f32-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="89f32-105">Syntax</span></span>


```C++
HRESULT D3DX10SaveTextureToMemory(
  _In_  ID3D10Resource           *pSrcTexture,
  _In_  D3DX10_IMAGE_FILE_FORMAT DestFormat,
  _Out_ LPD3D10BLOB              *ppDestBuf,
  _In_  UINT                     Flags
);
```



## <a name="parameters"></a><span data-ttu-id="89f32-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="89f32-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="89f32-107">*pSrcTexture* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="89f32-107">*pSrcTexture* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="89f32-108">Tipo: **[ **ID3D10Resource**](/windows/desktop/api/D3D10/nn-d3d10-id3d10resource)\***</span><span class="sxs-lookup"><span data-stu-id="89f32-108">Type: **[**ID3D10Resource**](/windows/desktop/api/D3D10/nn-d3d10-id3d10resource)\***</span></span>

<span data-ttu-id="89f32-109">Puntatore alla trama da salvare.</span><span class="sxs-lookup"><span data-stu-id="89f32-109">Pointer to the texture to be saved.</span></span> <span data-ttu-id="89f32-110">Vedere [**interfaccia ID3D10Resource**](/windows/desktop/api/D3D10/nn-d3d10-id3d10resource).</span><span class="sxs-lookup"><span data-stu-id="89f32-110">See [**ID3D10Resource Interface**](/windows/desktop/api/D3D10/nn-d3d10-id3d10resource).</span></span>

</dd> <dt>

<span data-ttu-id="89f32-111">*DestFormat* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="89f32-111">*DestFormat* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="89f32-112">Tipo: **[ **d3dx10 \_ Image \_ file \_ Format**](d3dx10-image-file-format.md)**</span><span class="sxs-lookup"><span data-stu-id="89f32-112">Type: **[**D3DX10\_IMAGE\_FILE\_FORMAT**](d3dx10-image-file-format.md)**</span></span>

<span data-ttu-id="89f32-113">Il formato in cui verrà salvata la trama.</span><span class="sxs-lookup"><span data-stu-id="89f32-113">The format the texture will be saved as.</span></span> <span data-ttu-id="89f32-114">Vedere [**d3dx10 \_ Image \_ file \_ Format**](d3dx10-image-file-format.md).</span><span class="sxs-lookup"><span data-stu-id="89f32-114">See [**D3DX10\_IMAGE\_FILE\_FORMAT**](d3dx10-image-file-format.md).</span></span>

</dd> <dt>

<span data-ttu-id="89f32-115">*ppDestBuf* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="89f32-115">*ppDestBuf* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="89f32-116">Tipo: **[ **LPD3D10BLOB**](/windows/desktop/api/D3DCommon/nn-d3dcommon-id3d10blob)\***</span><span class="sxs-lookup"><span data-stu-id="89f32-116">Type: **[**LPD3D10BLOB**](/windows/desktop/api/D3DCommon/nn-d3dcommon-id3d10blob)\***</span></span>

<span data-ttu-id="89f32-117">Indirizzo di un puntatore alla memoria contenente la trama salvata.</span><span class="sxs-lookup"><span data-stu-id="89f32-117">Address of a pointer to the memory containing the saved texture.</span></span> <span data-ttu-id="89f32-118">Vedere [**interfaccia ID3D10Blob**](/windows/desktop/api/D3DCommon/nn-d3dcommon-id3d10blob).</span><span class="sxs-lookup"><span data-stu-id="89f32-118">See [**ID3D10Blob Interface**](/windows/desktop/api/D3DCommon/nn-d3dcommon-id3d10blob).</span></span>

</dd> <dt>

<span data-ttu-id="89f32-119">*Flag* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="89f32-119">*Flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="89f32-120">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="89f32-120">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="89f32-121">facoltativo.</span><span class="sxs-lookup"><span data-stu-id="89f32-121">Optional.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="89f32-122">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="89f32-122">Return value</span></span>

<span data-ttu-id="89f32-123">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="89f32-123">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="89f32-124">Il valore restituito è uno dei valori elencati in [codici restituiti Direct3D 10](d3d10-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="89f32-124">The return value is one of the values listed in [Direct3D 10 Return Codes](d3d10-graphics-reference-returnvalues.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="89f32-125">Requisiti</span><span class="sxs-lookup"><span data-stu-id="89f32-125">Requirements</span></span>



| <span data-ttu-id="89f32-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="89f32-126">Requirement</span></span> | <span data-ttu-id="89f32-127">Valore</span><span class="sxs-lookup"><span data-stu-id="89f32-127">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="89f32-128">Intestazione</span><span class="sxs-lookup"><span data-stu-id="89f32-128">Header</span></span><br/>  | <dl> <span data-ttu-id="89f32-129"><dt>D3DX10Tex. h</dt></span><span class="sxs-lookup"><span data-stu-id="89f32-129"><dt>D3DX10Tex.h</dt></span></span> </dl> |
| <span data-ttu-id="89f32-130">Libreria</span><span class="sxs-lookup"><span data-stu-id="89f32-130">Library</span></span><br/> | <dl> <span data-ttu-id="89f32-131"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="89f32-131"><dt>D3DX10.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="89f32-132">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="89f32-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="89f32-133">Funzioni di trama in D3DX 10</span><span class="sxs-lookup"><span data-stu-id="89f32-133">Texture Functions in D3DX 10</span></span>](d3d10-graphics-reference-d3dx10-functions-texturing.md)
</dt> <dt>

[<span data-ttu-id="89f32-134">Funzioni per utilizzo generico</span><span class="sxs-lookup"><span data-stu-id="89f32-134">General Purpose Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-general-purpose.md)
</dt> </dl>

 

 
