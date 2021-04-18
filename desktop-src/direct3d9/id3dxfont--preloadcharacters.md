---
description: Carica una serie di caratteri nella memoria video per migliorare l'efficienza del rendering nel dispositivo.
ms.assetid: bb49842e-99de-406b-bf4b-139d6499f96e
title: Metodo ID3DXFont::P reloadCharacters (D3dx9core. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXFont.PreloadCharacters
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 9262fcb386b9362093ad563bd851946fd2305c7c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106323541"
---
# <a name="id3dxfontpreloadcharacters-method"></a><span data-ttu-id="7c30f-103">ID3DXFont::P metodo reloadCharacters</span><span class="sxs-lookup"><span data-stu-id="7c30f-103">ID3DXFont::PreloadCharacters method</span></span>

<span data-ttu-id="7c30f-104">Carica una serie di caratteri nella memoria video per migliorare l'efficienza del rendering nel dispositivo.</span><span class="sxs-lookup"><span data-stu-id="7c30f-104">Loads a series of characters into video memory to improve the efficiency of rendering to the device.</span></span>

## <a name="syntax"></a><span data-ttu-id="7c30f-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="7c30f-105">Syntax</span></span>


```C++
HRESULT PreloadCharacters(
  [in] UINT First,
  [in] UINT Last
);
```



## <a name="parameters"></a><span data-ttu-id="7c30f-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="7c30f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7c30f-107">*Primo* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="7c30f-107">*First* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7c30f-108">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="7c30f-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="7c30f-109">ID del primo carattere da caricare nella memoria video.</span><span class="sxs-lookup"><span data-stu-id="7c30f-109">ID of the first character to be loaded into video memory.</span></span>

</dd> <dt>

<span data-ttu-id="7c30f-110">*Ultima* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="7c30f-110">*Last* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7c30f-111">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="7c30f-111">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="7c30f-112">ID dell'ultimo carattere da caricare nella memoria video.</span><span class="sxs-lookup"><span data-stu-id="7c30f-112">ID of the last character to be loaded into video memory.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7c30f-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="7c30f-113">Return value</span></span>

<span data-ttu-id="7c30f-114">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="7c30f-114">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="7c30f-115">Se il metodo ha esito positivo, il valore restituito è \_ OK.</span><span class="sxs-lookup"><span data-stu-id="7c30f-115">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="7c30f-116">Se il metodo ha esito negativo, il valore restituito può essere uno dei seguenti: D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA.</span><span class="sxs-lookup"><span data-stu-id="7c30f-116">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA.</span></span>

## <a name="remarks"></a><span data-ttu-id="7c30f-117">Commenti</span><span class="sxs-lookup"><span data-stu-id="7c30f-117">Remarks</span></span>

<span data-ttu-id="7c30f-118">Questo metodo genera trame contenenti glifi che rappresentano i caratteri di input.</span><span class="sxs-lookup"><span data-stu-id="7c30f-118">This method generates textures containing glyphs that represent the input characters.</span></span> <span data-ttu-id="7c30f-119">I glifi vengono disegnati come una serie di triangoli.</span><span class="sxs-lookup"><span data-stu-id="7c30f-119">The glyphs are drawn as a series of triangles.</span></span>

<span data-ttu-id="7c30f-120">Non verrà eseguito il rendering dei caratteri nel dispositivo. Per eseguire il rendering dei caratteri, è comunque necessario chiamare [**DrawText**](id3dxfont--drawtext.md) .</span><span class="sxs-lookup"><span data-stu-id="7c30f-120">Characters will not be rendered to the device; [**DrawText**](id3dxfont--drawtext.md) must still be called to render the characters.</span></span> <span data-ttu-id="7c30f-121">Tuttavia, se si precaricano i caratteri nella memoria video, **DrawText** utilizzerà in modo sostanziale un minor numero di risorse della CPU.</span><span class="sxs-lookup"><span data-stu-id="7c30f-121">However, by pre-loading characters into video memory, **DrawText** will use substantially fewer CPU resources.</span></span>

<span data-ttu-id="7c30f-122">Questo metodo converte internamente i caratteri in glifi utilizzando la funzione GDI [**GetCharacterPlacement**](/windows/win32/api/wingdi/nf-wingdi-getcharacterplacementa).</span><span class="sxs-lookup"><span data-stu-id="7c30f-122">This method internally converts characters to glyphs using the GDI function [**GetCharacterPlacement**](/windows/win32/api/wingdi/nf-wingdi-getcharacterplacementa).</span></span>

## <a name="requirements"></a><span data-ttu-id="7c30f-123">Requisiti</span><span class="sxs-lookup"><span data-stu-id="7c30f-123">Requirements</span></span>



| <span data-ttu-id="7c30f-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="7c30f-124">Requirement</span></span> | <span data-ttu-id="7c30f-125">Valore</span><span class="sxs-lookup"><span data-stu-id="7c30f-125">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="7c30f-126">Intestazione</span><span class="sxs-lookup"><span data-stu-id="7c30f-126">Header</span></span><br/>  | <dl> <span data-ttu-id="7c30f-127"><dt>D3dx9core. h</dt></span><span class="sxs-lookup"><span data-stu-id="7c30f-127"><dt>D3dx9core.h</dt></span></span> </dl> |
| <span data-ttu-id="7c30f-128">Libreria</span><span class="sxs-lookup"><span data-stu-id="7c30f-128">Library</span></span><br/> | <dl> <span data-ttu-id="7c30f-129"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="7c30f-129"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="7c30f-130">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="7c30f-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7c30f-131">ID3DXFont</span><span class="sxs-lookup"><span data-stu-id="7c30f-131">ID3DXFont</span></span>](id3dxfont.md)
</dt> </dl>

 

 
