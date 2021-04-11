---
description: Carica il testo formattato nella memoria video per migliorare l'efficienza del rendering nel dispositivo. Questo metodo supporta le stringhe ANSI e Unicode.
ms.assetid: f2a4e9f5-87c5-46c0-965d-ce1535a6921d
title: Metodo ID3DXFont::P reloadText (D3dx9core. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXFont.PreloadText
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 958979e3008cf9ae0b79e2de3591635187df0f12
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104132402"
---
# <a name="id3dxfontpreloadtext-method"></a><span data-ttu-id="56a10-104">ID3DXFont::P metodo reloadText</span><span class="sxs-lookup"><span data-stu-id="56a10-104">ID3DXFont::PreloadText method</span></span>

<span data-ttu-id="56a10-105">Carica il testo formattato nella memoria video per migliorare l'efficienza del rendering nel dispositivo.</span><span class="sxs-lookup"><span data-stu-id="56a10-105">Loads formatted text into video memory to improve the efficiency of rendering to the device.</span></span> <span data-ttu-id="56a10-106">Questo metodo supporta le stringhe ANSI e Unicode.</span><span class="sxs-lookup"><span data-stu-id="56a10-106">This method supports ANSI and Unicode strings.</span></span>

## <a name="syntax"></a><span data-ttu-id="56a10-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="56a10-107">Syntax</span></span>


```C++
HRESULT PreloadText(
  [in] LPCTSTR *pString,
  [in] INT     Count
);
```



## <a name="parameters"></a><span data-ttu-id="56a10-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="56a10-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="56a10-109">*pString* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="56a10-109">*pString* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="56a10-110">Tipo: **[ **LPCTSTR**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="56a10-110">Type: **[**LPCTSTR**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="56a10-111">Puntatore a una stringa di caratteri da caricare nella memoria video.</span><span class="sxs-lookup"><span data-stu-id="56a10-111">Pointer to a string of characters to be loaded into video memory.</span></span> <span data-ttu-id="56a10-112">Se le impostazioni del compilatore richiedono Unicode, il tipo di dati LPCTSTR viene risolto in LPCWSTR; in caso contrario, il tipo di dati viene risolto in LPCSTR.</span><span class="sxs-lookup"><span data-stu-id="56a10-112">If the compiler settings require Unicode, the data type LPCTSTR resolves to LPCWSTR; otherwise, the data type resolves to LPCSTR.</span></span> <span data-ttu-id="56a10-113">Vedere la sezione Osservazioni.</span><span class="sxs-lookup"><span data-stu-id="56a10-113">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="56a10-114">*Numero* \[ di in\]</span><span class="sxs-lookup"><span data-stu-id="56a10-114">*Count* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="56a10-115">Tipo: **[ **int**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="56a10-115">Type: **[**INT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="56a10-116">Numero di caratteri nella stringa di testo.</span><span class="sxs-lookup"><span data-stu-id="56a10-116">Number of characters in the text string.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="56a10-117">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="56a10-117">Return value</span></span>

<span data-ttu-id="56a10-118">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="56a10-118">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="56a10-119">Se il metodo ha esito positivo, il valore restituito è \_ OK.</span><span class="sxs-lookup"><span data-stu-id="56a10-119">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="56a10-120">Se il metodo ha esito negativo, il valore restituito può essere uno dei seguenti: D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA.</span><span class="sxs-lookup"><span data-stu-id="56a10-120">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA.</span></span>

## <a name="remarks"></a><span data-ttu-id="56a10-121">Commenti</span><span class="sxs-lookup"><span data-stu-id="56a10-121">Remarks</span></span>

<span data-ttu-id="56a10-122">L'impostazione del compilatore determina anche la versione della funzione.</span><span class="sxs-lookup"><span data-stu-id="56a10-122">The compiler setting also determines the function version.</span></span> <span data-ttu-id="56a10-123">Se è definito Unicode, la chiamata di funzione viene risolta in PreloadTextW.</span><span class="sxs-lookup"><span data-stu-id="56a10-123">If Unicode is defined, the function call resolves to PreloadTextW.</span></span> <span data-ttu-id="56a10-124">In caso contrario, la chiamata di funzione viene risolta in PreloadTextA perché vengono utilizzate le stringhe ANSI.</span><span class="sxs-lookup"><span data-stu-id="56a10-124">Otherwise, the function call resolves to PreloadTextA because ANSI strings are being used.</span></span>

<span data-ttu-id="56a10-125">Questo metodo genera trame che contengono glifi che rappresentano il testo di input.</span><span class="sxs-lookup"><span data-stu-id="56a10-125">This method generates textures that contain glyphs that represent the input text.</span></span> <span data-ttu-id="56a10-126">I glifi vengono disegnati come una serie di triangoli.</span><span class="sxs-lookup"><span data-stu-id="56a10-126">The glyphs are drawn as a series of triangles.</span></span>

<span data-ttu-id="56a10-127">Il rendering del testo non verrà eseguito nel dispositivo. Per eseguire il rendering del testo, è necessario che l'oggetto [**DrawText**](id3dxfont--drawtext.md) venga ancora chiamato.</span><span class="sxs-lookup"><span data-stu-id="56a10-127">Text will not be rendered to the device; [**DrawText**](id3dxfont--drawtext.md) must still be called to render the text.</span></span> <span data-ttu-id="56a10-128">Tuttavia, precaricando il testo nella memoria video, **DrawText** utilizzerà in modo sostanziale un minor numero di risorse della CPU.</span><span class="sxs-lookup"><span data-stu-id="56a10-128">However, by preloading text into video memory, **DrawText** will use substantially fewer CPU resources.</span></span>

<span data-ttu-id="56a10-129">Questo metodo converte internamente i caratteri in glifi utilizzando la funzione GDI [**GetCharacterPlacement**](/windows/win32/api/wingdi/nf-wingdi-getcharacterplacementa).</span><span class="sxs-lookup"><span data-stu-id="56a10-129">This method internally converts characters to glyphs using the GDI function [**GetCharacterPlacement**](/windows/win32/api/wingdi/nf-wingdi-getcharacterplacementa).</span></span>

## <a name="requirements"></a><span data-ttu-id="56a10-130">Requisiti</span><span class="sxs-lookup"><span data-stu-id="56a10-130">Requirements</span></span>



| <span data-ttu-id="56a10-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="56a10-131">Requirement</span></span> | <span data-ttu-id="56a10-132">Valore</span><span class="sxs-lookup"><span data-stu-id="56a10-132">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="56a10-133">Intestazione</span><span class="sxs-lookup"><span data-stu-id="56a10-133">Header</span></span><br/>  | <dl> <span data-ttu-id="56a10-134"><dt>D3dx9core. h</dt></span><span class="sxs-lookup"><span data-stu-id="56a10-134"><dt>D3dx9core.h</dt></span></span> </dl> |
| <span data-ttu-id="56a10-135">Libreria</span><span class="sxs-lookup"><span data-stu-id="56a10-135">Library</span></span><br/> | <dl> <span data-ttu-id="56a10-136"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="56a10-136"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="56a10-137">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="56a10-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="56a10-138">ID3DXFont</span><span class="sxs-lookup"><span data-stu-id="56a10-138">ID3DXFont</span></span>](id3dxfont.md)
</dt> </dl>

 

 
