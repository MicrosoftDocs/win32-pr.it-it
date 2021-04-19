---
description: Caricare una serie di glifi nella memoria video per migliorare l'efficienza del rendering nel dispositivo.
ms.assetid: 7d063d52-af2c-44a6-9019-3d546acfbd4a
title: Metodo ID3DX10Font::P reloadGlyphs (D3DX10. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10Font.PreloadGlyphs
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: fdb67b8a25912c6efc49ef27082d3b6b4e843b33
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322754"
---
# <a name="id3dx10fontpreloadglyphs-method"></a><span data-ttu-id="9173d-103">ID3DX10Font::P metodo reloadGlyphs</span><span class="sxs-lookup"><span data-stu-id="9173d-103">ID3DX10Font::PreloadGlyphs method</span></span>

<span data-ttu-id="9173d-104">Caricare una serie di glifi nella memoria video per migliorare l'efficienza del rendering nel dispositivo.</span><span class="sxs-lookup"><span data-stu-id="9173d-104">Load a series of glyphs into video memory to improve the efficiency of rendering to the device.</span></span>

## <a name="syntax"></a><span data-ttu-id="9173d-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="9173d-105">Syntax</span></span>


```C++
HRESULT PreloadGlyphs(
  [in] UINT First,
  [in] UINT Last
);
```



## <a name="parameters"></a><span data-ttu-id="9173d-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="9173d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9173d-107">*Primo* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="9173d-107">*First* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9173d-108">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="9173d-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="9173d-109">ID del primo glifo da caricare nella memoria video.</span><span class="sxs-lookup"><span data-stu-id="9173d-109">ID of the first glyph to be loaded into video memory.</span></span>

</dd> <dt>

<span data-ttu-id="9173d-110">*Ultima* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="9173d-110">*Last* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9173d-111">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="9173d-111">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="9173d-112">ID dell'ultimo glifo da caricare nella memoria video.</span><span class="sxs-lookup"><span data-stu-id="9173d-112">ID of the last glyph to be loaded into video memory.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9173d-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="9173d-113">Return value</span></span>

<span data-ttu-id="9173d-114">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="9173d-114">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="9173d-115">Se il metodo ha esito positivo, il valore restituito è \_ OK.</span><span class="sxs-lookup"><span data-stu-id="9173d-115">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="9173d-116">Se il metodo ha esito negativo, il valore restituito può essere uno dei seguenti: D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA.</span><span class="sxs-lookup"><span data-stu-id="9173d-116">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA.</span></span>

## <a name="remarks"></a><span data-ttu-id="9173d-117">Commenti</span><span class="sxs-lookup"><span data-stu-id="9173d-117">Remarks</span></span>

<span data-ttu-id="9173d-118">Questo metodo genera trame che contengono i glifi di input.</span><span class="sxs-lookup"><span data-stu-id="9173d-118">This method generates textures that contain the input glyphs.</span></span> <span data-ttu-id="9173d-119">I glifi vengono disegnati come una serie di triangoli.</span><span class="sxs-lookup"><span data-stu-id="9173d-119">The glyphs are drawn as a series of triangles.</span></span>

<span data-ttu-id="9173d-120">Non verrà eseguito il rendering dei glifi nel dispositivo. ID3DX10Font: è necessario chiamare:D rawText per eseguire il rendering dei glifi.</span><span class="sxs-lookup"><span data-stu-id="9173d-120">Glyphs will not be rendered to the device; ID3DX10Font::DrawText must still be called to render the glyphs.</span></span> <span data-ttu-id="9173d-121">Tuttavia, se si precaricano i glifi nella memoria video, ID3DX10Font::D rawText utilizzerà in modo sostanziale un minor numero di risorse della CPU.</span><span class="sxs-lookup"><span data-stu-id="9173d-121">However, by pre-loading glyphs into video memory, ID3DX10Font::DrawText will use substantially fewer CPU resources.</span></span>

## <a name="requirements"></a><span data-ttu-id="9173d-122">Requisiti</span><span class="sxs-lookup"><span data-stu-id="9173d-122">Requirements</span></span>



| <span data-ttu-id="9173d-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="9173d-123">Requirement</span></span> | <span data-ttu-id="9173d-124">Valore</span><span class="sxs-lookup"><span data-stu-id="9173d-124">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="9173d-125">Intestazione</span><span class="sxs-lookup"><span data-stu-id="9173d-125">Header</span></span><br/>  | <dl> <span data-ttu-id="9173d-126"><dt>D3DX10. h</dt></span><span class="sxs-lookup"><span data-stu-id="9173d-126"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="9173d-127">Libreria</span><span class="sxs-lookup"><span data-stu-id="9173d-127">Library</span></span><br/> | <dl> <span data-ttu-id="9173d-128"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="9173d-128"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9173d-129">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="9173d-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9173d-130">ID3DX10Font</span><span class="sxs-lookup"><span data-stu-id="9173d-130">ID3DX10Font</span></span>](id3dx10font.md)
</dt> <dt>

[<span data-ttu-id="9173d-131">Interfacce D3DX</span><span class="sxs-lookup"><span data-stu-id="9173d-131">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
