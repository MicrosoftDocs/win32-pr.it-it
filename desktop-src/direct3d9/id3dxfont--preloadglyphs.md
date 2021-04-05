---
description: Carica una serie di glifi nella memoria video per migliorare l'efficienza del rendering nel dispositivo.
ms.assetid: df023359-bcb3-4c05-950b-19cdeba97c85
title: Metodo ID3DXFont::P reloadGlyphs (D3dx9core. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXFont.PreloadGlyphs
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 954d9e8abb310f962f7188720cb32035baf50d3d
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104058684"
---
# <a name="id3dxfontpreloadglyphs-method"></a><span data-ttu-id="e5710-103">ID3DXFont::P metodo reloadGlyphs</span><span class="sxs-lookup"><span data-stu-id="e5710-103">ID3DXFont::PreloadGlyphs method</span></span>

<span data-ttu-id="e5710-104">Carica una serie di glifi nella memoria video per migliorare l'efficienza del rendering nel dispositivo.</span><span class="sxs-lookup"><span data-stu-id="e5710-104">Loads a series of glyphs into video memory to improve the efficiency of rendering to the device.</span></span>

## <a name="syntax"></a><span data-ttu-id="e5710-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="e5710-105">Syntax</span></span>


```C++
HRESULT PreloadGlyphs(
  [in] UINT First,
  [in] UINT Last
);
```



## <a name="parameters"></a><span data-ttu-id="e5710-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="e5710-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e5710-107">*Primo* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e5710-107">*First* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e5710-108">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="e5710-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="e5710-109">ID del primo glifo da caricare nella memoria video.</span><span class="sxs-lookup"><span data-stu-id="e5710-109">ID of the first glyph to be loaded into video memory.</span></span>

</dd> <dt>

<span data-ttu-id="e5710-110">*Ultima* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e5710-110">*Last* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e5710-111">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="e5710-111">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="e5710-112">ID dell'ultimo glifo da caricare nella memoria video.</span><span class="sxs-lookup"><span data-stu-id="e5710-112">ID of the last glyph to be loaded into video memory.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e5710-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="e5710-113">Return value</span></span>

<span data-ttu-id="e5710-114">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="e5710-114">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="e5710-115">Se il metodo ha esito positivo, il valore restituito è \_ OK.</span><span class="sxs-lookup"><span data-stu-id="e5710-115">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="e5710-116">Se il metodo ha esito negativo, il valore restituito può essere uno dei seguenti: D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA.</span><span class="sxs-lookup"><span data-stu-id="e5710-116">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA.</span></span>

## <a name="remarks"></a><span data-ttu-id="e5710-117">Commenti</span><span class="sxs-lookup"><span data-stu-id="e5710-117">Remarks</span></span>

<span data-ttu-id="e5710-118">Questo metodo genera trame che contengono i glifi di input.</span><span class="sxs-lookup"><span data-stu-id="e5710-118">This method generates textures that contain the input glyphs.</span></span> <span data-ttu-id="e5710-119">I glifi vengono disegnati come una serie di triangoli.</span><span class="sxs-lookup"><span data-stu-id="e5710-119">The glyphs are drawn as a series of triangles.</span></span>

<span data-ttu-id="e5710-120">Non verrà eseguito il rendering dei glifi nel dispositivo. Per eseguire il rendering dei glifi, è comunque necessario chiamare [**DrawText**](id3dxfont--drawtext.md) .</span><span class="sxs-lookup"><span data-stu-id="e5710-120">Glyphs will not be rendered to the device; [**DrawText**](id3dxfont--drawtext.md) must still be called to render the glyphs.</span></span> <span data-ttu-id="e5710-121">Tuttavia, se si precaricano i glifi nella memoria video, **DrawText** utilizzerà in modo sostanziale un minor numero di risorse della CPU.</span><span class="sxs-lookup"><span data-stu-id="e5710-121">However, by pre-loading glyphs into video memory, **DrawText** will use substantially fewer CPU resources.</span></span>

## <a name="requirements"></a><span data-ttu-id="e5710-122">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e5710-122">Requirements</span></span>



| <span data-ttu-id="e5710-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="e5710-123">Requirement</span></span> | <span data-ttu-id="e5710-124">Valore</span><span class="sxs-lookup"><span data-stu-id="e5710-124">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="e5710-125">Intestazione</span><span class="sxs-lookup"><span data-stu-id="e5710-125">Header</span></span><br/>  | <dl> <span data-ttu-id="e5710-126"><dt>D3dx9core. h</dt></span><span class="sxs-lookup"><span data-stu-id="e5710-126"><dt>D3dx9core.h</dt></span></span> </dl> |
| <span data-ttu-id="e5710-127">Libreria</span><span class="sxs-lookup"><span data-stu-id="e5710-127">Library</span></span><br/> | <dl> <span data-ttu-id="e5710-128"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="e5710-128"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="e5710-129">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e5710-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e5710-130">ID3DXFont</span><span class="sxs-lookup"><span data-stu-id="e5710-130">ID3DXFont</span></span>](id3dxfont.md)
</dt> </dl>

 

 
