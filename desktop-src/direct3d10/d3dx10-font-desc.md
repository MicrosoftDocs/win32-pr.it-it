---
description: Definisce gli attributi del tipo di carattere.
ms.assetid: 66e8a320-2b83-4766-a9a7-5571ee6c9f2a
title: Struttura D3DX10_FONT_DESC (D3DX10. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10_FONT_DESC
api_type:
- HeaderDef
api_location:
- D3DX10.h
ms.openlocfilehash: 0b358c57e6410827177e76e3da30b2f5f9896ee2
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322385"
---
# <a name="d3dx10_font_desc-structure"></a><span data-ttu-id="2e5a9-103">\_Struttura Desc del tipo di carattere d3dx10 \_</span><span class="sxs-lookup"><span data-stu-id="2e5a9-103">D3DX10\_FONT\_DESC structure</span></span>

<span data-ttu-id="2e5a9-104">Definisce gli attributi del tipo di carattere.</span><span class="sxs-lookup"><span data-stu-id="2e5a9-104">Defines font attributes.</span></span>

## <a name="syntax"></a><span data-ttu-id="2e5a9-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="2e5a9-105">Syntax</span></span>


```C++
typedef struct D3DX10_FONT_DESC {
  INT   Height;
  UINT  Width;
  UINT  Weight;
  UINT  MipLevels;
  BOOL  Italic;
  BYTE  CharSet;
  BYTE  OutputPrecision;
  BYTE  Quality;
  BYTE  PitchAndFamily;
  TCHAR FaceName[LF_FACESIZE];
} D3DX10_FONT_DESC, *LPD3DX10_FONT_DESC;
```



## <a name="members"></a><span data-ttu-id="2e5a9-106">Members</span><span class="sxs-lookup"><span data-stu-id="2e5a9-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="2e5a9-107">**Altezza**</span><span class="sxs-lookup"><span data-stu-id="2e5a9-107">**Height**</span></span>
</dt> <dd>

<span data-ttu-id="2e5a9-108">Tipo: **[ **int**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="2e5a9-108">Type: **[**INT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="2e5a9-109">Altezza, in unità logiche, della cella del carattere o del carattere del tipo di carattere.</span><span class="sxs-lookup"><span data-stu-id="2e5a9-109">Height, in logical units, of the font's character cell or character.</span></span>

</dd> <dt>

<span data-ttu-id="2e5a9-110">**Larghezza**</span><span class="sxs-lookup"><span data-stu-id="2e5a9-110">**Width**</span></span>
</dt> <dd>

<span data-ttu-id="2e5a9-111">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="2e5a9-111">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="2e5a9-112">Larghezza, in unità logiche, di caratteri nel tipo di carattere.</span><span class="sxs-lookup"><span data-stu-id="2e5a9-112">Width, in logical units, of characters in the font.</span></span>

</dd> <dt>

<span data-ttu-id="2e5a9-113">**Weight**</span><span class="sxs-lookup"><span data-stu-id="2e5a9-113">**Weight**</span></span>
</dt> <dd>

<span data-ttu-id="2e5a9-114">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="2e5a9-114">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="2e5a9-115">Spessore del tipo di carattere nell'intervallo compreso tra 0 e 1000.</span><span class="sxs-lookup"><span data-stu-id="2e5a9-115">Weight of the font in the range from 0 through 1000.</span></span>

</dd> <dt>

<span data-ttu-id="2e5a9-116">**MipLevels**</span><span class="sxs-lookup"><span data-stu-id="2e5a9-116">**MipLevels**</span></span>
</dt> <dd>

<span data-ttu-id="2e5a9-117">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="2e5a9-117">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="2e5a9-118">Numero di livelli di mipmap richiesti.</span><span class="sxs-lookup"><span data-stu-id="2e5a9-118">Number of mipmap levels requested.</span></span> <span data-ttu-id="2e5a9-119">Se questo valore è zero o D3DX \_ default, viene creata una catena mipmap completa.</span><span class="sxs-lookup"><span data-stu-id="2e5a9-119">If this value is zero or D3DX\_DEFAULT, a complete mipmap chain is created.</span></span> <span data-ttu-id="2e5a9-120">Se il valore è 1, lo spazio della trama viene mappato in modo identico allo spazio dello schermo.</span><span class="sxs-lookup"><span data-stu-id="2e5a9-120">If the value is 1, the texture space is mapped identically to the screen space.</span></span>

</dd> <dt>

<span data-ttu-id="2e5a9-121">**Corsivo**</span><span class="sxs-lookup"><span data-stu-id="2e5a9-121">**Italic**</span></span>
</dt> <dd>

<span data-ttu-id="2e5a9-122">Tipo: **[ **bool**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="2e5a9-122">Type: **[**BOOL**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="2e5a9-123">Impostare su **true** per un tipo di carattere corsivo.</span><span class="sxs-lookup"><span data-stu-id="2e5a9-123">Set to **TRUE** for an Italic font.</span></span>

</dd> <dt>

<span data-ttu-id="2e5a9-124">**CharSet**</span><span class="sxs-lookup"><span data-stu-id="2e5a9-124">**CharSet**</span></span>
</dt> <dd>

<span data-ttu-id="2e5a9-125">Tipo: **[ **byte**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="2e5a9-125">Type: **[**BYTE**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="2e5a9-126">Set di caratteri.</span><span class="sxs-lookup"><span data-stu-id="2e5a9-126">Character set.</span></span>

</dd> <dt>

<span data-ttu-id="2e5a9-127">**OutputPrecision**</span><span class="sxs-lookup"><span data-stu-id="2e5a9-127">**OutputPrecision**</span></span>
</dt> <dd>

<span data-ttu-id="2e5a9-128">Tipo: **[ **byte**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="2e5a9-128">Type: **[**BYTE**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="2e5a9-129">Precisione dell'output.</span><span class="sxs-lookup"><span data-stu-id="2e5a9-129">Output precision.</span></span> <span data-ttu-id="2e5a9-130">La precisione di output definisce la distanza con cui l'output deve corrispondere all'altezza, alla larghezza, all'orientamento dei caratteri, alla rotazione, al passo e al tipo di carattere richiesti.</span><span class="sxs-lookup"><span data-stu-id="2e5a9-130">The output precision defines how closely the output must match the requested font height, width, character orientation, escapement, pitch, and font type.</span></span>

</dd> <dt>

<span data-ttu-id="2e5a9-131">**Qualità**</span><span class="sxs-lookup"><span data-stu-id="2e5a9-131">**Quality**</span></span>
</dt> <dd>

<span data-ttu-id="2e5a9-132">Tipo: **[ **byte**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="2e5a9-132">Type: **[**BYTE**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="2e5a9-133">Qualità dell'output.</span><span class="sxs-lookup"><span data-stu-id="2e5a9-133">Output quality.</span></span>

</dd> <dt>

<span data-ttu-id="2e5a9-134">**PitchAndFamily**</span><span class="sxs-lookup"><span data-stu-id="2e5a9-134">**PitchAndFamily**</span></span>
</dt> <dd>

<span data-ttu-id="2e5a9-135">Tipo: **[ **byte**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="2e5a9-135">Type: **[**BYTE**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="2e5a9-136">Pitch e Family del tipo di carattere.</span><span class="sxs-lookup"><span data-stu-id="2e5a9-136">Pitch and family of the font.</span></span>

</dd> <dt>

<span data-ttu-id="2e5a9-137">**FaceName \[ LF \_ FACESIZE\]**</span><span class="sxs-lookup"><span data-stu-id="2e5a9-137">**FaceName\[LF\_FACESIZE\]**</span></span>
</dt> <dd>

<span data-ttu-id="2e5a9-138">Tipo: **TCHAR**</span><span class="sxs-lookup"><span data-stu-id="2e5a9-138">Type: **TCHAR**</span></span>

</dd> <dd>

<span data-ttu-id="2e5a9-139">Stringa con terminazione NULL che specifica il nome tipografico del tipo di carattere.</span><span class="sxs-lookup"><span data-stu-id="2e5a9-139">A NULL-terminated string that specifies the typeface name of the font.</span></span> <span data-ttu-id="2e5a9-140">La lunghezza della stringa non deve superare i 32 caratteri, incluso il carattere **null** di terminazione.</span><span class="sxs-lookup"><span data-stu-id="2e5a9-140">The length of the string must not exceed 32 characters, including the terminating **NULL** character.</span></span> <span data-ttu-id="2e5a9-141">Se FaceName è una stringa vuota, verrà utilizzato il primo carattere corrispondente agli altri attributi specificati.</span><span class="sxs-lookup"><span data-stu-id="2e5a9-141">If FaceName is an empty string, the first font that matches the other specified attributes will be used.</span></span> <span data-ttu-id="2e5a9-142">Se le impostazioni del compilatore richiedono Unicode, il tipo di dati TCHAR viene risolto in WCHAR; in caso contrario, il tipo di dati viene risolto in CHAR.</span><span class="sxs-lookup"><span data-stu-id="2e5a9-142">If the compiler settings require Unicode, the data type TCHAR resolves to WCHAR; otherwise, the data type resolves to CHAR.</span></span> <span data-ttu-id="2e5a9-143">Vedere la sezione Osservazioni.</span><span class="sxs-lookup"><span data-stu-id="2e5a9-143">See Remarks.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="2e5a9-144">Commenti</span><span class="sxs-lookup"><span data-stu-id="2e5a9-144">Remarks</span></span>

<span data-ttu-id="2e5a9-145">L'impostazione del compilatore determina anche il tipo di struttura.</span><span class="sxs-lookup"><span data-stu-id="2e5a9-145">The compiler setting also determines the structure type.</span></span> <span data-ttu-id="2e5a9-146">Se è definito Unicode, il \_ \_ tipo di struttura d3dx10 del tipo di carattere desc viene risolto in un tipo di \_ carattere d3dx10 \_ DESCW; in caso contrario, il tipo di struttura viene risolto in un tipo di \_ carattere d3dx10 \_ Desca.</span><span class="sxs-lookup"><span data-stu-id="2e5a9-146">If Unicode is defined, the D3DX10\_FONT\_DESC structure type resolves to a D3DX10\_FONT\_DESCW; otherwise the structure type resolves to a D3DX10\_FONT\_DESCA.</span></span>

<span data-ttu-id="2e5a9-147">I valori possibili dei membri precedenti sono forniti nella struttura GDI [LOGFONT](/previous-versions//ms533931(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="2e5a9-147">Possible values of the above members are given in the GDI [LOGFONT](/previous-versions//ms533931(v=vs.85)) structure.</span></span>

## <a name="requirements"></a><span data-ttu-id="2e5a9-148">Requisiti</span><span class="sxs-lookup"><span data-stu-id="2e5a9-148">Requirements</span></span>



| <span data-ttu-id="2e5a9-149">Requisito</span><span class="sxs-lookup"><span data-stu-id="2e5a9-149">Requirement</span></span> | <span data-ttu-id="2e5a9-150">Valore</span><span class="sxs-lookup"><span data-stu-id="2e5a9-150">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="2e5a9-151">Intestazione</span><span class="sxs-lookup"><span data-stu-id="2e5a9-151">Header</span></span><br/> | <dl> <span data-ttu-id="2e5a9-152"><dt>D3DX10. h</dt></span><span class="sxs-lookup"><span data-stu-id="2e5a9-152"><dt>D3DX10.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2e5a9-153">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="2e5a9-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2e5a9-154">Strutture D3DX</span><span class="sxs-lookup"><span data-stu-id="2e5a9-154">D3DX Structures</span></span>](d3d10-graphics-reference-d3dx10-structures.md)
</dt> </dl>

 

 
