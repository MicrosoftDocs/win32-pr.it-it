---
description: Definisce gli attributi di un tipo di carattere.
ms.assetid: 6f456f26-3410-4205-a013-e3c12bf0feb1
title: Struttura D3DXFONT_DESC (D3dx9core. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXFONT_DESC
api_type:
- HeaderDef
api_location:
- d3dx9core.h
ms.openlocfilehash: d7c142787e4e4fac5be53763a3c19fd86a27efd9
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322687"
---
# <a name="d3dxfont_desc-structure"></a><span data-ttu-id="680f9-103">\_Struttura D3DXFONT DESC</span><span class="sxs-lookup"><span data-stu-id="680f9-103">D3DXFONT\_DESC structure</span></span>

<span data-ttu-id="680f9-104">Definisce gli attributi di un tipo di carattere.</span><span class="sxs-lookup"><span data-stu-id="680f9-104">Defines the attributes of a font.</span></span>

## <a name="syntax"></a><span data-ttu-id="680f9-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="680f9-105">Syntax</span></span>


```C++
typedef struct D3DXFONT_DESC {
  INT   Height;
  UINT  Width;
  UINT  Weight;
  UINT  MipLevels;
  BOOL  Italic;
  BYTE  CharSet;
  BYTE  OutputPrecision;
  BYTE  Quality;
  BYTE  PitchAndFamily;
  TCHAR FaceName;
} D3DXFONT_DESC, *LPD3DXFONT_DESC;
```



## <a name="members"></a><span data-ttu-id="680f9-106">Members</span><span class="sxs-lookup"><span data-stu-id="680f9-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="680f9-107">**Altezza**</span><span class="sxs-lookup"><span data-stu-id="680f9-107">**Height**</span></span>
</dt> <dd>

<span data-ttu-id="680f9-108">Tipo: **[ **int**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="680f9-108">Type: **[**INT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="680f9-109">Altezza, in unità logiche, della cella del carattere o del carattere del tipo di carattere.</span><span class="sxs-lookup"><span data-stu-id="680f9-109">Height, in logical units, of the font's character cell or character.</span></span>

</dd> <dt>

<span data-ttu-id="680f9-110">**Larghezza**</span><span class="sxs-lookup"><span data-stu-id="680f9-110">**Width**</span></span>
</dt> <dd>

<span data-ttu-id="680f9-111">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="680f9-111">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="680f9-112">Larghezza, in unità logiche, di caratteri nel tipo di carattere.</span><span class="sxs-lookup"><span data-stu-id="680f9-112">Width, in logical units, of characters in the font.</span></span>

</dd> <dt>

<span data-ttu-id="680f9-113">**Weight**</span><span class="sxs-lookup"><span data-stu-id="680f9-113">**Weight**</span></span>
</dt> <dd>

<span data-ttu-id="680f9-114">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="680f9-114">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="680f9-115">Spessore del tipo di carattere nell'intervallo compreso tra 0 e 1000.</span><span class="sxs-lookup"><span data-stu-id="680f9-115">Weight of the font in the range from 0 through 1000.</span></span>

</dd> <dt>

<span data-ttu-id="680f9-116">**MipLevels**</span><span class="sxs-lookup"><span data-stu-id="680f9-116">**MipLevels**</span></span>
</dt> <dd>

<span data-ttu-id="680f9-117">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="680f9-117">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="680f9-118">Numero di livelli MIP richiesti.</span><span class="sxs-lookup"><span data-stu-id="680f9-118">Number of mip levels requested.</span></span> <span data-ttu-id="680f9-119">Se questo valore è zero o D3DX \_ default, viene creata una catena mipmap completa.</span><span class="sxs-lookup"><span data-stu-id="680f9-119">If this value is zero or D3DX\_DEFAULT, a complete mipmap chain is created.</span></span> <span data-ttu-id="680f9-120">Se il valore è 1, lo spazio della trama viene mappato in modo identico allo spazio dello schermo.</span><span class="sxs-lookup"><span data-stu-id="680f9-120">If the value is 1, the texture space is mapped identically to the screen space.</span></span>

</dd> <dt>

<span data-ttu-id="680f9-121">**Corsivo**</span><span class="sxs-lookup"><span data-stu-id="680f9-121">**Italic**</span></span>
</dt> <dd>

<span data-ttu-id="680f9-122">Tipo: **[ **bool**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="680f9-122">Type: **[**BOOL**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="680f9-123">Impostare su **true** per un tipo di carattere corsivo.</span><span class="sxs-lookup"><span data-stu-id="680f9-123">Set to **TRUE** for an Italic font.</span></span>

</dd> <dt>

<span data-ttu-id="680f9-124">**CharSet**</span><span class="sxs-lookup"><span data-stu-id="680f9-124">**CharSet**</span></span>
</dt> <dd>

<span data-ttu-id="680f9-125">Tipo: **[ **byte**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="680f9-125">Type: **[**BYTE**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="680f9-126">Set di caratteri.</span><span class="sxs-lookup"><span data-stu-id="680f9-126">Character set.</span></span>

</dd> <dt>

<span data-ttu-id="680f9-127">**OutputPrecision**</span><span class="sxs-lookup"><span data-stu-id="680f9-127">**OutputPrecision**</span></span>
</dt> <dd>

<span data-ttu-id="680f9-128">Tipo: **[ **byte**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="680f9-128">Type: **[**BYTE**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="680f9-129">Precisione dell'output.</span><span class="sxs-lookup"><span data-stu-id="680f9-129">Output precision.</span></span> <span data-ttu-id="680f9-130">La precisione di output definisce la distanza con cui l'output deve corrispondere all'altezza, alla larghezza, all'orientamento dei caratteri, alla rotazione, al passo e al tipo di carattere richiesti.</span><span class="sxs-lookup"><span data-stu-id="680f9-130">The output precision defines how closely the output must match the requested font height, width, character orientation, escapement, pitch, and font type.</span></span>

</dd> <dt>

<span data-ttu-id="680f9-131">**Qualità**</span><span class="sxs-lookup"><span data-stu-id="680f9-131">**Quality**</span></span>
</dt> <dd>

<span data-ttu-id="680f9-132">Tipo: **[ **byte**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="680f9-132">Type: **[**BYTE**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="680f9-133">Qualità dell'output.</span><span class="sxs-lookup"><span data-stu-id="680f9-133">Output quality.</span></span>

</dd> <dt>

<span data-ttu-id="680f9-134">**PitchAndFamily**</span><span class="sxs-lookup"><span data-stu-id="680f9-134">**PitchAndFamily**</span></span>
</dt> <dd>

<span data-ttu-id="680f9-135">Tipo: **[ **byte**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="680f9-135">Type: **[**BYTE**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="680f9-136">Pitch e Family del tipo di carattere.</span><span class="sxs-lookup"><span data-stu-id="680f9-136">Pitch and family of the font.</span></span>

</dd> <dt>

<span data-ttu-id="680f9-137">**Contemplato**</span><span class="sxs-lookup"><span data-stu-id="680f9-137">**FaceName**</span></span>
</dt> <dd>

<span data-ttu-id="680f9-138">Tipo: **TCHAR**</span><span class="sxs-lookup"><span data-stu-id="680f9-138">Type: **TCHAR**</span></span>

</dd> <dd>

<span data-ttu-id="680f9-139">Stringa o caratteri con terminazione null che specifica il nome tipografico del tipo di carattere.</span><span class="sxs-lookup"><span data-stu-id="680f9-139">A null-terminated string or characters that specifies the typeface name of the font.</span></span> <span data-ttu-id="680f9-140">La lunghezza della stringa non deve superare i 32 caratteri, incluso il carattere null di terminazione.</span><span class="sxs-lookup"><span data-stu-id="680f9-140">The length of the string must not exceed 32 characters, including the terminating null character.</span></span> <span data-ttu-id="680f9-141">Se FaceName è una stringa vuota, verrà utilizzato il primo carattere corrispondente agli altri attributi specificati.</span><span class="sxs-lookup"><span data-stu-id="680f9-141">If FaceName is an empty string, the first font that matches the other specified attributes will be used.</span></span> <span data-ttu-id="680f9-142">Se le impostazioni del compilatore richiedono Unicode, il tipo di dati TCHAR viene risolto in WCHAR; in caso contrario, il tipo di dati viene risolto in CHAR.</span><span class="sxs-lookup"><span data-stu-id="680f9-142">If the compiler settings require Unicode, the data type TCHAR resolves to WCHAR; otherwise, the data type resolves to CHAR.</span></span> <span data-ttu-id="680f9-143">Vedere la sezione Osservazioni.</span><span class="sxs-lookup"><span data-stu-id="680f9-143">See Remarks.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="680f9-144">Commenti</span><span class="sxs-lookup"><span data-stu-id="680f9-144">Remarks</span></span>

<span data-ttu-id="680f9-145">L'impostazione del compilatore determina anche il tipo di struttura.</span><span class="sxs-lookup"><span data-stu-id="680f9-145">The compiler setting also determines the structure type.</span></span> <span data-ttu-id="680f9-146">Se è definito Unicode, il \_ tipo di struttura D3DXFONT desc viene risolto in un \_ DESCW D3DXFONT; in caso contrario, il tipo di struttura viene risolto in un D3DXFONT \_ Desca.</span><span class="sxs-lookup"><span data-stu-id="680f9-146">If Unicode is defined, the D3DXFONT\_DESC structure type resolves to a D3DXFONT\_DESCW; otherwise the structure type resolves to a D3DXFONT\_DESCA.</span></span>

<span data-ttu-id="680f9-147">I valori possibili dei membri precedenti sono forniti nella struttura GDI [**LOGFONT**](/windows/win32/api/wingdi/ns-wingdi-logfonta) .</span><span class="sxs-lookup"><span data-stu-id="680f9-147">Possible values of the above members are given in the GDI [**LOGFONT**](/windows/win32/api/wingdi/ns-wingdi-logfonta) structure.</span></span>

## <a name="requirements"></a><span data-ttu-id="680f9-148">Requisiti</span><span class="sxs-lookup"><span data-stu-id="680f9-148">Requirements</span></span>



| <span data-ttu-id="680f9-149">Requisito</span><span class="sxs-lookup"><span data-stu-id="680f9-149">Requirement</span></span> | <span data-ttu-id="680f9-150">Valore</span><span class="sxs-lookup"><span data-stu-id="680f9-150">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="680f9-151">Intestazione</span><span class="sxs-lookup"><span data-stu-id="680f9-151">Header</span></span><br/> | <dl> <span data-ttu-id="680f9-152"><dt>D3dx9core. h</dt></span><span class="sxs-lookup"><span data-stu-id="680f9-152"><dt>D3dx9core.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="680f9-153">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="680f9-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="680f9-154">Strutture D3DX</span><span class="sxs-lookup"><span data-stu-id="680f9-154">D3DX Structures</span></span>](dx9-graphics-reference-d3dx-structures.md)
</dt> <dt>

[<span data-ttu-id="680f9-155">**Getdesc**</span><span class="sxs-lookup"><span data-stu-id="680f9-155">**GetDesc**</span></span>](id3dxfont--getdesc.md)
</dt> </dl>

 

 
