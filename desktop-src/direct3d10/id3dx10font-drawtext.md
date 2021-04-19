---
description: Creare testo formattato. Questo metodo supporta le stringhe ANSI e Unicode.
ms.assetid: 205e9e23-4293-4195-9e41-d8c06dabd285
title: Metodo ID3DX10Font::D rawText (D3DX10. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10Font.DrawText
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 5fa23684be1b63cfbd8e3d07d3578d87fdfbf46a
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322762"
---
# <a name="id3dx10fontdrawtext-method"></a><span data-ttu-id="aec73-104">ID3DX10Font::D Metodo rawText</span><span class="sxs-lookup"><span data-stu-id="aec73-104">ID3DX10Font::DrawText method</span></span>

<span data-ttu-id="aec73-105">Creare testo formattato.</span><span class="sxs-lookup"><span data-stu-id="aec73-105">Draw formatted text.</span></span> <span data-ttu-id="aec73-106">Questo metodo supporta le stringhe ANSI e Unicode.</span><span class="sxs-lookup"><span data-stu-id="aec73-106">This method supports ANSI and Unicode strings.</span></span>

## <a name="syntax"></a><span data-ttu-id="aec73-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="aec73-107">Syntax</span></span>


```C++
INT DrawText(
  [in] LPD3DX10SPRITE pSprite,
  [in] LPCTSTR        pString,
  [in] INT            Count,
  [in] LPRECT         pRect,
  [in] UINT           Format,
  [in] D3DXCOLOR      Color
);
```



## <a name="parameters"></a><span data-ttu-id="aec73-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="aec73-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="aec73-109">*pSprite* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="aec73-109">*pSprite* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="aec73-110">Tipo: **[ **LPD3DX10SPRITE**](id3dx10sprite.md)**</span><span class="sxs-lookup"><span data-stu-id="aec73-110">Type: **[**LPD3DX10SPRITE**](id3dx10sprite.md)**</span></span>

<span data-ttu-id="aec73-111">Puntatore a un oggetto ID3DX10Sprite che contiene la stringa che si vuole creare.</span><span class="sxs-lookup"><span data-stu-id="aec73-111">Pointer to an ID3DX10Sprite object that contains the string you wish to draw.</span></span> <span data-ttu-id="aec73-112">Può essere **null**, nel qual caso Direct3D eseguirà il rendering della stringa con il proprio oggetto Sprite.</span><span class="sxs-lookup"><span data-stu-id="aec73-112">Can be **NULL**, in which case Direct3D will render the string with its own sprite object.</span></span> <span data-ttu-id="aec73-113">Per migliorare l'efficienza, è necessario specificare un oggetto Sprite se ID3DX10Font::D rawText deve essere chiamato più di una volta in una riga.</span><span class="sxs-lookup"><span data-stu-id="aec73-113">To improve efficiency, a sprite object should be specified if ID3DX10Font::DrawText is to be called more than once in a row.</span></span>

</dd> <dt>

<span data-ttu-id="aec73-114">*pString* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="aec73-114">*pString* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="aec73-115">Tipo: **[ **LPCTSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="aec73-115">Type: **[**LPCTSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="aec73-116">Puntatore a una stringa da creare.</span><span class="sxs-lookup"><span data-stu-id="aec73-116">Pointer to a string to draw.</span></span> <span data-ttu-id="aec73-117">Se è definito UNICODE, questo tipo di parametro viene risolto in un LPCWSTR; in caso contrario, il tipo viene risolto in un LPCSTR.</span><span class="sxs-lookup"><span data-stu-id="aec73-117">If UNICODE is defined, this parameter type resolves to an LPCWSTR, otherwise, the type resolves to an LPCSTR.</span></span> <span data-ttu-id="aec73-118">Se il parametro count è-1, la stringa deve essere con terminazione **null** .</span><span class="sxs-lookup"><span data-stu-id="aec73-118">If the Count parameter is -1, the string must be **NULL** terminated.</span></span>

</dd> <dt>

<span data-ttu-id="aec73-119">*Numero* \[ di in\]</span><span class="sxs-lookup"><span data-stu-id="aec73-119">*Count* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="aec73-120">Tipo: **[ **int**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="aec73-120">Type: **[**INT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="aec73-121">Numero di caratteri nella stringa.</span><span class="sxs-lookup"><span data-stu-id="aec73-121">The number of characters in the string.</span></span> <span data-ttu-id="aec73-122">Se count è-1, viene utilizzato il parametro pString come puntatore a uno sprite contenente una stringa con terminazione NULL e ID3DX10Font::D rawText calcola automaticamente il numero di caratteri.</span><span class="sxs-lookup"><span data-stu-id="aec73-122">If Count is -1, then the pString parameter is assumed to be a pointer to a sprite containing a NULL-terminated string and ID3DX10Font::DrawText computes the character count automatically.</span></span>

</dd> <dt>

<span data-ttu-id="aec73-123">*pRect* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="aec73-123">*pRect* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="aec73-124">Tipo: **lpRect**</span><span class="sxs-lookup"><span data-stu-id="aec73-124">Type: **LPRECT**</span></span>

<span data-ttu-id="aec73-125">Puntatore a una struttura [Rect](/previous-versions//ms536136(v=vs.85)) che contiene il rettangolo, in coordinate logiche, in cui deve essere formattato il testo.</span><span class="sxs-lookup"><span data-stu-id="aec73-125">Pointer to a [RECT](/previous-versions//ms536136(v=vs.85)) structure that contains the rectangle, in logical coordinates, in which the text is to be formatted.</span></span> <span data-ttu-id="aec73-126">Come per qualsiasi oggetto RECT, il valore della coordinata del lato destro del rettangolo deve essere maggiore di quello del lato sinistro.</span><span class="sxs-lookup"><span data-stu-id="aec73-126">As with any RECT object, the coordinate value of the rectangle's right side must be greater than that of its left side.</span></span> <span data-ttu-id="aec73-127">Analogamente, il valore della coordinata della parte inferiore deve essere maggiore di quello della parte superiore.</span><span class="sxs-lookup"><span data-stu-id="aec73-127">Likewise, the coordinate value of the bottom must be greater than that of the top.</span></span>

</dd> <dt>

<span data-ttu-id="aec73-128">*Formato* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="aec73-128">*Format* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="aec73-129">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="aec73-129">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="aec73-130">Specificare il metodo di formattazione del testo.</span><span class="sxs-lookup"><span data-stu-id="aec73-130">Specify the method of formatting the text.</span></span> <span data-ttu-id="aec73-131">Può essere una qualsiasi combinazione dei valori seguenti:</span><span class="sxs-lookup"><span data-stu-id="aec73-131">It can be any combination of the following values:</span></span>



| <span data-ttu-id="aec73-132">Elemento</span><span class="sxs-lookup"><span data-stu-id="aec73-132">Item</span></span>                                                                                      | <span data-ttu-id="aec73-133">Descrizione</span><span class="sxs-lookup"><span data-stu-id="aec73-133">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
|-------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="aec73-134"><span id="DT_BOTTOM"></span><span id="dt_bottom"></span>DT \_ inferiore</span><span class="sxs-lookup"><span data-stu-id="aec73-134"><span id="DT_BOTTOM"></span><span id="dt_bottom"></span>DT\_BOTTOM</span></span><br/>             | <span data-ttu-id="aec73-135">Giustifica il testo nella parte inferiore del rettangolo.</span><span class="sxs-lookup"><span data-stu-id="aec73-135">Justify the text to the bottom of the rectangle.</span></span> <span data-ttu-id="aec73-136">Questo valore deve essere combinato con DT \_ Singleline.</span><span class="sxs-lookup"><span data-stu-id="aec73-136">This value must be combined with DT\_SINGLELINE.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| <span data-ttu-id="aec73-137"><span id="DT_CALCRECT"></span><span id="dt_calcrect"></span>DT \_ CALCRECT</span><span class="sxs-lookup"><span data-stu-id="aec73-137"><span id="DT_CALCRECT"></span><span id="dt_calcrect"></span>DT\_CALCRECT</span></span><br/>       | <span data-ttu-id="aec73-138">Indicare a DrawText di calcolare automaticamente la larghezza e l'altezza del rettangolo in base alla lunghezza della stringa che si indica di creare.</span><span class="sxs-lookup"><span data-stu-id="aec73-138">Tell DrawText to automatically calculate the width and height of the rectangle based on the length of the string you tell it to draw.</span></span> <span data-ttu-id="aec73-139">Se sono presenti più righe di testo, ID3DX10Font::D rawText usa la larghezza del rettangolo a cui punta il parametro pRect ed estende la base del rettangolo per l'associazione dell'ultima riga di testo.</span><span class="sxs-lookup"><span data-stu-id="aec73-139">If there are multiple lines of text, ID3DX10Font::DrawText uses the width of the rectangle pointed to by the pRect parameter and extends the base of the rectangle to bound the last line of text.</span></span> <span data-ttu-id="aec73-140">Se è presente una sola riga di testo, ID3DX10Font::D rawText modifica il lato destro del rettangolo in modo da delegare l'ultimo carattere nella riga.</span><span class="sxs-lookup"><span data-stu-id="aec73-140">If there is only one line of text, ID3DX10Font::DrawText modifies the right side of the rectangle so that it bounds the last character in the line.</span></span> <span data-ttu-id="aec73-141">In entrambi i casi, ID3DX10Font::D rawText restituisce l'altezza del testo formattato ma il testo non viene disegnato.</span><span class="sxs-lookup"><span data-stu-id="aec73-141">In either case, ID3DX10Font::DrawText returns the height of the formatted text but does not draw the text.</span></span><br/> |
| <span data-ttu-id="aec73-142"><span id="DT_CENTER"></span><span id="dt_center"></span>centro di DT \_</span><span class="sxs-lookup"><span data-stu-id="aec73-142"><span id="DT_CENTER"></span><span id="dt_center"></span>DT\_CENTER</span></span><br/>             | <span data-ttu-id="aec73-143">Centra il testo orizzontalmente nel rettangolo.</span><span class="sxs-lookup"><span data-stu-id="aec73-143">Center text horizontally in the rectangle.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| <span data-ttu-id="aec73-144"><span id="DT_EXPANDTABS"></span><span id="dt_expandtabs"></span>DT \_ ExpandTabs</span><span class="sxs-lookup"><span data-stu-id="aec73-144"><span id="DT_EXPANDTABS"></span><span id="dt_expandtabs"></span>DT\_EXPANDTABS</span></span><br/> | <span data-ttu-id="aec73-145">Espandere i caratteri di tabulazione.</span><span class="sxs-lookup"><span data-stu-id="aec73-145">Expand tab characters.</span></span> <span data-ttu-id="aec73-146">Il numero predefinito di caratteri per tabulazione è otto.</span><span class="sxs-lookup"><span data-stu-id="aec73-146">The default number of characters per tab is eight.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| <span data-ttu-id="aec73-147"><span id="DT_LEFT"></span><span id="dt_left"></span>DT a \_ sinistra</span><span class="sxs-lookup"><span data-stu-id="aec73-147"><span id="DT_LEFT"></span><span id="dt_left"></span>DT\_LEFT</span></span><br/>                   | <span data-ttu-id="aec73-148">Allinea il testo a sinistra.</span><span class="sxs-lookup"><span data-stu-id="aec73-148">Align text to the left.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| <span data-ttu-id="aec73-149"><span id="DT_NOCLIP"></span><span id="dt_noclip"></span>DT \_ NOclip</span><span class="sxs-lookup"><span data-stu-id="aec73-149"><span id="DT_NOCLIP"></span><span id="dt_noclip"></span>DT\_NOCLIP</span></span><br/>             | <span data-ttu-id="aec73-150">Viene disegnato senza ritaglio.</span><span class="sxs-lookup"><span data-stu-id="aec73-150">Draw without clipping.</span></span> <span data-ttu-id="aec73-151">ID3DX10Font::D rawText è leggermente più veloce quando \_ si usa DT noclip.</span><span class="sxs-lookup"><span data-stu-id="aec73-151">ID3DX10Font::DrawText is somewhat faster when DT\_NOCLIP is used.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
| <span data-ttu-id="aec73-152"><span id="DT_RIGHT"></span><span id="dt_right"></span>DT a \_ destra</span><span class="sxs-lookup"><span data-stu-id="aec73-152"><span id="DT_RIGHT"></span><span id="dt_right"></span>DT\_RIGHT</span></span><br/>                | <span data-ttu-id="aec73-153">Allinea il testo a destra.</span><span class="sxs-lookup"><span data-stu-id="aec73-153">Align text to the right.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
| <span data-ttu-id="aec73-154"><span id="DT_RTLREADING"></span><span id="dt_rtlreading"></span>DT \_ RTLREADING</span><span class="sxs-lookup"><span data-stu-id="aec73-154"><span id="DT_RTLREADING"></span><span id="dt_rtlreading"></span>DT\_RTLREADING</span></span><br/> | <span data-ttu-id="aec73-155">Consente di visualizzare il testo in ordine di lettura da destra a sinistra per il testo bidirezionale quando viene selezionato un tipo di carattere ebraico o arabo.</span><span class="sxs-lookup"><span data-stu-id="aec73-155">Display text in right-to-left reading order for bidirectional text when a Hebrew or Arabic font is selected.</span></span> <span data-ttu-id="aec73-156">L'ordine di lettura predefinito per tutto il testo è da sinistra a destra.</span><span class="sxs-lookup"><span data-stu-id="aec73-156">The default reading order for all text is left-to-right.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| <span data-ttu-id="aec73-157"><span id="DT_SINGLELINE"></span><span id="dt_singleline"></span>DT \_ Singleline</span><span class="sxs-lookup"><span data-stu-id="aec73-157"><span id="DT_SINGLELINE"></span><span id="dt_singleline"></span>DT\_SINGLELINE</span></span><br/> | <span data-ttu-id="aec73-158">Visualizza il testo solo su una sola riga.</span><span class="sxs-lookup"><span data-stu-id="aec73-158">Display text on a single line only.</span></span> <span data-ttu-id="aec73-159">I ritorni a capo e i feed di riga non interrompono la riga.</span><span class="sxs-lookup"><span data-stu-id="aec73-159">Carriage returns and line feeds do not break the line.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| <span data-ttu-id="aec73-160"><span id="DT_TOP"></span><span id="dt_top"></span>DT \_ superiore</span><span class="sxs-lookup"><span data-stu-id="aec73-160"><span id="DT_TOP"></span><span id="dt_top"></span>DT\_TOP</span></span><br/>                      | <span data-ttu-id="aec73-161">Testo in primo piano.</span><span class="sxs-lookup"><span data-stu-id="aec73-161">Top-justify text.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| <span data-ttu-id="aec73-162"><span id="DT_VCENTER"></span><span id="dt_vcenter"></span>\_vCenter vCenter</span><span class="sxs-lookup"><span data-stu-id="aec73-162"><span id="DT_VCENTER"></span><span id="dt_vcenter"></span>DT\_VCENTER</span></span><br/>          | <span data-ttu-id="aec73-163">Centra il testo verticalmente (solo riga singola).</span><span class="sxs-lookup"><span data-stu-id="aec73-163">Center text vertically (single line only).</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| <span data-ttu-id="aec73-164"><span id="DT_WORDBREAK"></span><span id="dt_wordbreak"></span>DT \_ WordBreak</span><span class="sxs-lookup"><span data-stu-id="aec73-164"><span id="DT_WORDBREAK"></span><span id="dt_wordbreak"></span>DT\_WORDBREAK</span></span><br/>    | <span data-ttu-id="aec73-165">Interrompi parole.</span><span class="sxs-lookup"><span data-stu-id="aec73-165">Break words.</span></span> <span data-ttu-id="aec73-166">Le righe vengono interrotte automaticamente tra le parole se una parola si estende oltre il bordo del rettangolo specificato dal parametro pRect.</span><span class="sxs-lookup"><span data-stu-id="aec73-166">Lines are automatically broken between words if a word would extend past the edge of the rectangle specified by the pRect parameter.</span></span> <span data-ttu-id="aec73-167">Una sequenza di ritorno A capo/avanzamento riga interrompe anche la riga.</span><span class="sxs-lookup"><span data-stu-id="aec73-167">A carriage return/line feed sequence also breaks the line.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                            |



 

</dd> <dt>

<span data-ttu-id="aec73-168">*Colore* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="aec73-168">*Color* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="aec73-169">Tipo: **[ **D3DXCOLOR**](../direct3d9/d3dxcolor.md)**</span><span class="sxs-lookup"><span data-stu-id="aec73-169">Type: **[**D3DXCOLOR**](../direct3d9/d3dxcolor.md)**</span></span>

<span data-ttu-id="aec73-170">Colore del testo.</span><span class="sxs-lookup"><span data-stu-id="aec73-170">Color of the text.</span></span> <span data-ttu-id="aec73-171">Vedere [**D3DXCOLOR**](d3d10-d3dxcolor.md).</span><span class="sxs-lookup"><span data-stu-id="aec73-171">See [**D3DXCOLOR**](d3d10-d3dxcolor.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="aec73-172">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="aec73-172">Return value</span></span>

<span data-ttu-id="aec73-173">Tipo: **[ **int**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="aec73-173">Type: **[**INT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="aec73-174">Se la funzione ha esito positivo, il valore restituito è l'altezza del testo nelle unità logiche.</span><span class="sxs-lookup"><span data-stu-id="aec73-174">If the function succeeds, the return value is the height of the text in logical units.</span></span> <span data-ttu-id="aec73-175">Se \_ si specifica DT vCenter o DT \_ Bottom, il valore restituito è l'offset da pRect (dall'alto verso il basso) del testo creato.</span><span class="sxs-lookup"><span data-stu-id="aec73-175">If DT\_VCENTER or DT\_BOTTOM is specified, the return value is the offset from pRect (top to the bottom) of the drawn text.</span></span> <span data-ttu-id="aec73-176">Se la funzione ha esito negativo, il valore restituito è zero.</span><span class="sxs-lookup"><span data-stu-id="aec73-176">If the function fails, the return value is zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="aec73-177">Commenti</span><span class="sxs-lookup"><span data-stu-id="aec73-177">Remarks</span></span>

<span data-ttu-id="aec73-178">I parametri di questo metodo sono molto simili a quelli della funzione [DrawText di GDI](/previous-versions//ms533909(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="aec73-178">The parameters of this method are very similar to those of the [GDI DrawText](/previous-versions//ms533909(v=vs.85)) function.</span></span>

<span data-ttu-id="aec73-179">Questo metodo supporta le stringhe ANSI e Unicode.</span><span class="sxs-lookup"><span data-stu-id="aec73-179">This method supports both ANSI and Unicode strings.</span></span>

<span data-ttu-id="aec73-180">A meno che non \_ venga utilizzato il formato DT noclip, questo metodo consente di ritagliare il testo in modo che non venga visualizzato all'esterno del rettangolo specificato.</span><span class="sxs-lookup"><span data-stu-id="aec73-180">Unless the DT\_NOCLIP format is used, this method clips the text so that it does not appear outside the specified rectangle.</span></span> <span data-ttu-id="aec73-181">Si presuppone che tutte le formattazioni abbiano più righe, a meno che non \_ sia specificato il formato DT Singleline.</span><span class="sxs-lookup"><span data-stu-id="aec73-181">All formatting is assumed to have multiple lines unless the DT\_SINGLELINE format is specified.</span></span>

<span data-ttu-id="aec73-182">Se il tipo di carattere selezionato è troppo grande per il rettangolo, questo metodo non tenta di sostituire un tipo di carattere più piccolo.</span><span class="sxs-lookup"><span data-stu-id="aec73-182">If the selected font is too large for the rectangle, this method does not attempt to substitute a smaller font.</span></span>

<span data-ttu-id="aec73-183">Questo metodo supporta solo i tipi di carattere il cui scappamento e l'orientamento sono entrambi zero.</span><span class="sxs-lookup"><span data-stu-id="aec73-183">This method supports only fonts whose escapement and orientation are both zero.</span></span>

## <a name="requirements"></a><span data-ttu-id="aec73-184">Requisiti</span><span class="sxs-lookup"><span data-stu-id="aec73-184">Requirements</span></span>



| <span data-ttu-id="aec73-185">Requisito</span><span class="sxs-lookup"><span data-stu-id="aec73-185">Requirement</span></span> | <span data-ttu-id="aec73-186">Valore</span><span class="sxs-lookup"><span data-stu-id="aec73-186">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="aec73-187">Intestazione</span><span class="sxs-lookup"><span data-stu-id="aec73-187">Header</span></span><br/>  | <dl> <span data-ttu-id="aec73-188"><dt>D3DX10. h</dt></span><span class="sxs-lookup"><span data-stu-id="aec73-188"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="aec73-189">Libreria</span><span class="sxs-lookup"><span data-stu-id="aec73-189">Library</span></span><br/> | <dl> <span data-ttu-id="aec73-190"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="aec73-190"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="aec73-191">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="aec73-191">See also</span></span>

<dl> <dt>

[<span data-ttu-id="aec73-192">ID3DX10Font</span><span class="sxs-lookup"><span data-stu-id="aec73-192">ID3DX10Font</span></span>](id3dx10font.md)
</dt> <dt>

[<span data-ttu-id="aec73-193">Interfacce D3DX</span><span class="sxs-lookup"><span data-stu-id="aec73-193">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
