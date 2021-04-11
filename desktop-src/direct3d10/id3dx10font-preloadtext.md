---
description: Caricare il testo formattato nella memoria video per migliorare l'efficienza del rendering nel dispositivo. Questo metodo supporta le stringhe ANSI e Unicode.
ms.assetid: 0e5380fc-7a01-4e09-9c18-22087be56780
title: Metodo ID3DX10Font::P reloadText (D3DX10. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10Font.PreloadText
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: c7294fb7e86b3532960a34a15e1118dc33f748f2
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104235037"
---
# <a name="id3dx10fontpreloadtext-method"></a><span data-ttu-id="64b9b-104">ID3DX10Font::P metodo reloadText</span><span class="sxs-lookup"><span data-stu-id="64b9b-104">ID3DX10Font::PreloadText method</span></span>

<span data-ttu-id="64b9b-105">Caricare il testo formattato nella memoria video per migliorare l'efficienza del rendering nel dispositivo.</span><span class="sxs-lookup"><span data-stu-id="64b9b-105">Load formatted text into video memory to improve the efficiency of rendering to the device.</span></span> <span data-ttu-id="64b9b-106">Questo metodo supporta le stringhe ANSI e Unicode.</span><span class="sxs-lookup"><span data-stu-id="64b9b-106">This method supports ANSI and Unicode strings.</span></span>

## <a name="syntax"></a><span data-ttu-id="64b9b-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="64b9b-107">Syntax</span></span>


```C++
HRESULT PreloadText(
  [in] LPCSTR pString,
  [in] INT    Count
);
```



## <a name="parameters"></a><span data-ttu-id="64b9b-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="64b9b-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="64b9b-109">*pString* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="64b9b-109">*pString* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="64b9b-110">Tipo: **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="64b9b-110">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="64b9b-111">Puntatore a una stringa di caratteri da caricare nella memoria video.</span><span class="sxs-lookup"><span data-stu-id="64b9b-111">Pointer to a string of characters to be loaded into video memory.</span></span> <span data-ttu-id="64b9b-112">Se le impostazioni del compilatore richiedono Unicode, il tipo di dati LPCTSTR viene risolto in LPCWSTR; in caso contrario, il tipo di dati viene risolto in LPCSTR.</span><span class="sxs-lookup"><span data-stu-id="64b9b-112">If the compiler settings require Unicode, the data type LPCTSTR resolves to LPCWSTR; otherwise, the data type resolves to LPCSTR.</span></span> <span data-ttu-id="64b9b-113">Vedere la sezione Osservazioni.</span><span class="sxs-lookup"><span data-stu-id="64b9b-113">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="64b9b-114">*Numero* \[ di in\]</span><span class="sxs-lookup"><span data-stu-id="64b9b-114">*Count* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="64b9b-115">Tipo: **[ **int**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="64b9b-115">Type: **[**INT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="64b9b-116">Numero di caratteri nella stringa di testo.</span><span class="sxs-lookup"><span data-stu-id="64b9b-116">Number of characters in the text string.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="64b9b-117">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="64b9b-117">Return value</span></span>

<span data-ttu-id="64b9b-118">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="64b9b-118">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="64b9b-119">Se il metodo ha esito positivo, il valore restituito è \_ OK.</span><span class="sxs-lookup"><span data-stu-id="64b9b-119">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="64b9b-120">Se il metodo ha esito negativo, il valore restituito può essere uno dei seguenti: D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA.</span><span class="sxs-lookup"><span data-stu-id="64b9b-120">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA.</span></span>

## <a name="remarks"></a><span data-ttu-id="64b9b-121">Commenti</span><span class="sxs-lookup"><span data-stu-id="64b9b-121">Remarks</span></span>

<span data-ttu-id="64b9b-122">L'impostazione del compilatore determina anche la versione della funzione.</span><span class="sxs-lookup"><span data-stu-id="64b9b-122">The compiler setting also determines the function version.</span></span> <span data-ttu-id="64b9b-123">Se è definito Unicode, la chiamata di funzione viene risolta in PreloadTextW.</span><span class="sxs-lookup"><span data-stu-id="64b9b-123">If Unicode is defined, the function call resolves to PreloadTextW.</span></span> <span data-ttu-id="64b9b-124">In caso contrario, la chiamata di funzione viene risolta in PreloadTextA perché vengono utilizzate le stringhe ANSI.</span><span class="sxs-lookup"><span data-stu-id="64b9b-124">Otherwise, the function call resolves to PreloadTextA because ANSI strings are being used.</span></span>

<span data-ttu-id="64b9b-125">Questo metodo genera trame che contengono glifi che rappresentano il testo di input.</span><span class="sxs-lookup"><span data-stu-id="64b9b-125">This method generates textures that contain glyphs that represent the input text.</span></span> <span data-ttu-id="64b9b-126">I glifi vengono disegnati come una serie di triangoli.</span><span class="sxs-lookup"><span data-stu-id="64b9b-126">The glyphs are drawn as a series of triangles.</span></span>

<span data-ttu-id="64b9b-127">Il rendering del testo non verrà eseguito nel dispositivo. ID3DX10Font: è necessario chiamare:D rawText per eseguire il rendering del testo.</span><span class="sxs-lookup"><span data-stu-id="64b9b-127">Text will not be rendered to the device; ID3DX10Font::DrawText must still be called to render the text.</span></span> <span data-ttu-id="64b9b-128">Tuttavia, precaricando il testo nella memoria video, ID3DX10Font::D rawText utilizzerà in modo sostanziale un minor numero di risorse della CPU.</span><span class="sxs-lookup"><span data-stu-id="64b9b-128">However, by preloading text into video memory, ID3DX10Font::DrawText will use substantially fewer CPU resources.</span></span>

<span data-ttu-id="64b9b-129">Questo metodo converte internamente i caratteri in glifi utilizzando la funzione GDI [GetCharacterPlacement](/previous-versions//ms534004(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="64b9b-129">This method internally converts characters to glyphs using the GDI function [GetCharacterPlacement](/previous-versions//ms534004(v=vs.85)).</span></span>

## <a name="requirements"></a><span data-ttu-id="64b9b-130">Requisiti</span><span class="sxs-lookup"><span data-stu-id="64b9b-130">Requirements</span></span>



| <span data-ttu-id="64b9b-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="64b9b-131">Requirement</span></span> | <span data-ttu-id="64b9b-132">Valore</span><span class="sxs-lookup"><span data-stu-id="64b9b-132">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="64b9b-133">Intestazione</span><span class="sxs-lookup"><span data-stu-id="64b9b-133">Header</span></span><br/>  | <dl> <span data-ttu-id="64b9b-134"><dt>D3DX10. h</dt></span><span class="sxs-lookup"><span data-stu-id="64b9b-134"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="64b9b-135">Libreria</span><span class="sxs-lookup"><span data-stu-id="64b9b-135">Library</span></span><br/> | <dl> <span data-ttu-id="64b9b-136"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="64b9b-136"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="64b9b-137">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="64b9b-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="64b9b-138">ID3DX10Font</span><span class="sxs-lookup"><span data-stu-id="64b9b-138">ID3DX10Font</span></span>](id3dx10font.md)
</dt> <dt>

[<span data-ttu-id="64b9b-139">Interfacce D3DX</span><span class="sxs-lookup"><span data-stu-id="64b9b-139">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
