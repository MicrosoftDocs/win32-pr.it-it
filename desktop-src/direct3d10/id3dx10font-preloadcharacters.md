---
description: Caricare una serie di caratteri nella memoria video per migliorare l'efficienza del rendering nel dispositivo.
ms.assetid: 935a6248-e6b7-4fce-aaa7-b7f0c94c1f79
title: Metodo ID3DX10Font::P reloadCharacters (D3DX10. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10Font.PreloadCharacters
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: fafa34d4a243e254e929f7c9a1d65d2a3fb9c8dd
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322755"
---
# <a name="id3dx10fontpreloadcharacters-method"></a><span data-ttu-id="d3934-103">ID3DX10Font::P metodo reloadCharacters</span><span class="sxs-lookup"><span data-stu-id="d3934-103">ID3DX10Font::PreloadCharacters method</span></span>

<span data-ttu-id="d3934-104">Caricare una serie di caratteri nella memoria video per migliorare l'efficienza del rendering nel dispositivo.</span><span class="sxs-lookup"><span data-stu-id="d3934-104">Load a series of characters into video memory to improve the efficiency of rendering to the device.</span></span>

## <a name="syntax"></a><span data-ttu-id="d3934-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="d3934-105">Syntax</span></span>


```C++
HRESULT PreloadCharacters(
  [in] UINT First,
  [in] UINT Last
);
```



## <a name="parameters"></a><span data-ttu-id="d3934-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="d3934-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d3934-107">*Primo* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="d3934-107">*First* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d3934-108">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="d3934-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="d3934-109">ID del primo carattere da caricare nella memoria video.</span><span class="sxs-lookup"><span data-stu-id="d3934-109">ID of the first character to be loaded into video memory.</span></span>

</dd> <dt>

<span data-ttu-id="d3934-110">*Ultima* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="d3934-110">*Last* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d3934-111">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="d3934-111">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="d3934-112">ID dell'ultimo carattere da caricare nella memoria video.</span><span class="sxs-lookup"><span data-stu-id="d3934-112">ID of the last character to be loaded into video memory.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d3934-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="d3934-113">Return value</span></span>

<span data-ttu-id="d3934-114">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="d3934-114">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="d3934-115">Se il metodo ha esito positivo, il valore restituito è \_ OK.</span><span class="sxs-lookup"><span data-stu-id="d3934-115">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="d3934-116">Se il metodo ha esito negativo, il valore restituito può essere uno dei seguenti: D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA.</span><span class="sxs-lookup"><span data-stu-id="d3934-116">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA.</span></span>

## <a name="remarks"></a><span data-ttu-id="d3934-117">Commenti</span><span class="sxs-lookup"><span data-stu-id="d3934-117">Remarks</span></span>

<span data-ttu-id="d3934-118">Questo metodo genera trame contenenti glifi che rappresentano i caratteri di input.</span><span class="sxs-lookup"><span data-stu-id="d3934-118">This method generates textures containing glyphs that represent the input characters.</span></span> <span data-ttu-id="d3934-119">I glifi vengono disegnati come una serie di triangoli.</span><span class="sxs-lookup"><span data-stu-id="d3934-119">The glyphs are drawn as a series of triangles.</span></span>

<span data-ttu-id="d3934-120">Non verrà eseguito il rendering dei caratteri nel dispositivo. ID3DX10Font: è necessario chiamare:D rawText per eseguire il rendering dei caratteri.</span><span class="sxs-lookup"><span data-stu-id="d3934-120">Characters will not be rendered to the device; ID3DX10Font::DrawText must still be called to render the characters.</span></span> <span data-ttu-id="d3934-121">Tuttavia, precaricando i caratteri nella memoria video, ID3DX10Font::D rawText utilizzerà in modo sostanziale un minor numero di risorse della CPU.</span><span class="sxs-lookup"><span data-stu-id="d3934-121">However, by pre-loading characters into video memory, ID3DX10Font::DrawText will use substantially fewer CPU resources.</span></span>

<span data-ttu-id="d3934-122">Questo metodo converte internamente i caratteri in glifi utilizzando la funzione GDI [GetCharacterPlacement](/previous-versions//ms534004(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="d3934-122">This method internally converts characters to glyphs using the GDI function [GetCharacterPlacement](/previous-versions//ms534004(v=vs.85)).</span></span>

## <a name="requirements"></a><span data-ttu-id="d3934-123">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d3934-123">Requirements</span></span>



| <span data-ttu-id="d3934-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="d3934-124">Requirement</span></span> | <span data-ttu-id="d3934-125">Valore</span><span class="sxs-lookup"><span data-stu-id="d3934-125">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="d3934-126">Intestazione</span><span class="sxs-lookup"><span data-stu-id="d3934-126">Header</span></span><br/>  | <dl> <span data-ttu-id="d3934-127"><dt>D3DX10. h</dt></span><span class="sxs-lookup"><span data-stu-id="d3934-127"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="d3934-128">Libreria</span><span class="sxs-lookup"><span data-stu-id="d3934-128">Library</span></span><br/> | <dl> <span data-ttu-id="d3934-129"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="d3934-129"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d3934-130">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="d3934-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d3934-131">ID3DX10Font</span><span class="sxs-lookup"><span data-stu-id="d3934-131">ID3DX10Font</span></span>](id3dx10font.md)
</dt> <dt>

[<span data-ttu-id="d3934-132">Interfacce D3DX</span><span class="sxs-lookup"><span data-stu-id="d3934-132">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
