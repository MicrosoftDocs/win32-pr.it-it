---
description: Disegna il testo formattato. Questo metodo supporta le stringhe ANSI e Unicode.
ms.assetid: c1c3657e-632e-46a5-91da-e102ac8ef9bb
title: Metodo ID3DXFont::D rawText (D3dx9core. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXFont.DrawText
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 96636c372ee48d516286935f03d80b8e9815ffc8
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104235010"
---
# <a name="id3dxfontdrawtext-method"></a><span data-ttu-id="df074-104">ID3DXFont::D Metodo rawText</span><span class="sxs-lookup"><span data-stu-id="df074-104">ID3DXFont::DrawText method</span></span>

<span data-ttu-id="df074-105">Disegna il testo formattato.</span><span class="sxs-lookup"><span data-stu-id="df074-105">Draws formatted text.</span></span> <span data-ttu-id="df074-106">Questo metodo supporta le stringhe ANSI e Unicode.</span><span class="sxs-lookup"><span data-stu-id="df074-106">This method supports ANSI and Unicode strings.</span></span>

## <a name="syntax"></a><span data-ttu-id="df074-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="df074-107">Syntax</span></span>


```C++
INT DrawText(
  [in] LPD3DXSPRITE pSprite,
  [in] LPCTSTR      pString,
  [in] INT          Count,
  [in] LPRECT       pRect,
  [in] DWORD        Format,
  [in] D3DCOLOR     Color
);
```



## <a name="parameters"></a><span data-ttu-id="df074-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="df074-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="df074-109">*pSprite* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="df074-109">*pSprite* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="df074-110">Tipo: **[ **LPD3DXSPRITE**](id3dxsprite.md)**</span><span class="sxs-lookup"><span data-stu-id="df074-110">Type: **[**LPD3DXSPRITE**](id3dxsprite.md)**</span></span>

<span data-ttu-id="df074-111">Puntatore a un oggetto [**ID3DXSprite**](id3dxsprite.md) che contiene la stringa.</span><span class="sxs-lookup"><span data-stu-id="df074-111">Pointer to an [**ID3DXSprite**](id3dxsprite.md) object that contains the string.</span></span> <span data-ttu-id="df074-112">Può essere **null**, nel qual caso Direct3D eseguirà il rendering della stringa con il proprio oggetto Sprite.</span><span class="sxs-lookup"><span data-stu-id="df074-112">Can be **NULL**, in which case Direct3D will render the string with its own sprite object.</span></span> <span data-ttu-id="df074-113">Per migliorare l'efficienza, è necessario specificare un oggetto Sprite se **DrawText** viene chiamato più di una volta in una riga.</span><span class="sxs-lookup"><span data-stu-id="df074-113">To improve efficiency, a sprite object should be specified if **DrawText** is to be called more than once in a row.</span></span>

</dd> <dt>

<span data-ttu-id="df074-114">*pString* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="df074-114">*pString* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="df074-115">Tipo: **[ **LPCTSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="df074-115">Type: **[**LPCTSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="df074-116">Puntatore a una stringa da creare.</span><span class="sxs-lookup"><span data-stu-id="df074-116">Pointer to a string to draw.</span></span> <span data-ttu-id="df074-117">Se il parametro count è-1, la stringa deve essere con terminazione null.</span><span class="sxs-lookup"><span data-stu-id="df074-117">If the Count parameter is -1, the string must be null-terminated.</span></span>

</dd> <dt>

<span data-ttu-id="df074-118">*Numero* \[ di in\]</span><span class="sxs-lookup"><span data-stu-id="df074-118">*Count* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="df074-119">Tipo: **[ **int**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="df074-119">Type: **[**INT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="df074-120">Specifica il numero di caratteri nella stringa.</span><span class="sxs-lookup"><span data-stu-id="df074-120">Specifies the number of characters in the string.</span></span> <span data-ttu-id="df074-121">Se count è-1, il parametro pString viene considerato un puntatore a una stringa con terminazione null e **DrawText** calcola automaticamente il numero di caratteri.</span><span class="sxs-lookup"><span data-stu-id="df074-121">If Count is -1, then the pString parameter is assumed to be a pointer to a null-terminated string and **DrawText** computes the character count automatically.</span></span>

</dd> <dt>

<span data-ttu-id="df074-122">*pRect* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="df074-122">*pRect* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="df074-123">Tipo: **[ **lpRect**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="df074-123">Type: **[**LPRECT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="df074-124">Puntatore a una struttura [**Rect**](/previous-versions//dd162897(v=vs.85)) che contiene il rettangolo, in coordinate logiche, in cui deve essere formattato il testo.</span><span class="sxs-lookup"><span data-stu-id="df074-124">Pointer to a [**RECT**](/previous-versions//dd162897(v=vs.85)) structure that contains the rectangle, in logical coordinates, in which the text is to be formatted.</span></span> <span data-ttu-id="df074-125">Il valore della coordinata del lato destro del rettangolo deve essere maggiore di quello del lato sinistro.</span><span class="sxs-lookup"><span data-stu-id="df074-125">The coordinate value of the rectangle's right side must be greater than that of its left side.</span></span> <span data-ttu-id="df074-126">Analogamente, il valore della coordinata della parte inferiore deve essere maggiore di quello della parte superiore.</span><span class="sxs-lookup"><span data-stu-id="df074-126">Likewise, the coordinate value of the bottom must be greater than that of the top.</span></span>

</dd> <dt>

<span data-ttu-id="df074-127">*Formato* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="df074-127">*Format* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="df074-128">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="df074-128">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="df074-129">Specifica il metodo di formattazione del testo.</span><span class="sxs-lookup"><span data-stu-id="df074-129">Specifies the method of formatting the text.</span></span> <span data-ttu-id="df074-130">Può essere una qualsiasi combinazione dei valori seguenti:</span><span class="sxs-lookup"><span data-stu-id="df074-130">It can be any combination of the following values:</span></span>



| <span data-ttu-id="df074-131">Valore</span><span class="sxs-lookup"><span data-stu-id="df074-131">Value</span></span>                                                                                                                                                         | <span data-ttu-id="df074-132">Significato</span><span class="sxs-lookup"><span data-stu-id="df074-132">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="DT_BOTTOM"></span><span id="dt_bottom"></span><dl> <span data-ttu-id="df074-133"><dt>**DT \_ inferiore**</dt></span><span class="sxs-lookup"><span data-stu-id="df074-133"><dt>**DT\_BOTTOM**</dt></span></span> </dl>             | <span data-ttu-id="df074-134">Giustifica il testo nella parte inferiore del rettangolo.</span><span class="sxs-lookup"><span data-stu-id="df074-134">Justifies the text to the bottom of the rectangle.</span></span> <span data-ttu-id="df074-135">Questo valore deve essere combinato con DT \_ Singleline.</span><span class="sxs-lookup"><span data-stu-id="df074-135">This value must be combined with DT\_SINGLELINE.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                      |
| <span id="DT_CALCRECT"></span><span id="dt_calcrect"></span><dl> <span data-ttu-id="df074-136"><dt>**DT \_ CALCRECT**</dt></span><span class="sxs-lookup"><span data-stu-id="df074-136"><dt>**DT\_CALCRECT**</dt></span></span> </dl>       | <span data-ttu-id="df074-137">Determina la larghezza e l'altezza del rettangolo.</span><span class="sxs-lookup"><span data-stu-id="df074-137">Determines the width and height of the rectangle.</span></span> <span data-ttu-id="df074-138">Se sono presenti più righe di testo, **DrawText** usa la larghezza del rettangolo a cui punta il parametro pRect ed estende la base del rettangolo per l'associazione dell'ultima riga di testo.</span><span class="sxs-lookup"><span data-stu-id="df074-138">If there are multiple lines of text, **DrawText** uses the width of the rectangle pointed to by the pRect parameter and extends the base of the rectangle to bound the last line of text.</span></span> <span data-ttu-id="df074-139">Se è presente una sola riga di testo, **DrawText** modifica il lato destro del rettangolo in modo da delegare l'ultimo carattere nella riga.</span><span class="sxs-lookup"><span data-stu-id="df074-139">If there is only one line of text, **DrawText** modifies the right side of the rectangle so that it bounds the last character in the line.</span></span> <span data-ttu-id="df074-140">In entrambi i casi, per **DrawText** viene restituita l'altezza del testo formattato ma il testo non viene disegnato.</span><span class="sxs-lookup"><span data-stu-id="df074-140">In either case, **DrawText** returns the height of the formatted text but does not draw the text.</span></span><br/> |
| <span id="DT_CENTER"></span><span id="dt_center"></span><dl> <span data-ttu-id="df074-141"><dt>**centro di DT \_**</dt></span><span class="sxs-lookup"><span data-stu-id="df074-141"><dt>**DT\_CENTER**</dt></span></span> </dl>             | <span data-ttu-id="df074-142">Centra il testo orizzontalmente nel rettangolo.</span><span class="sxs-lookup"><span data-stu-id="df074-142">Centers text horizontally in the rectangle.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| <span id="DT_EXPANDTABS"></span><span id="dt_expandtabs"></span><dl> <span data-ttu-id="df074-143"><dt>**DT \_ ExpandTabs**</dt></span><span class="sxs-lookup"><span data-stu-id="df074-143"><dt>**DT\_EXPANDTABS**</dt></span></span> </dl> | <span data-ttu-id="df074-144">Espande i caratteri di tabulazione.</span><span class="sxs-lookup"><span data-stu-id="df074-144">Expands tab characters.</span></span> <span data-ttu-id="df074-145">Il numero predefinito di caratteri per tabulazione è otto.</span><span class="sxs-lookup"><span data-stu-id="df074-145">The default number of characters per tab is eight.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                               |
| <span id="DT_LEFT"></span><span id="dt_left"></span><dl> <span data-ttu-id="df074-146"><dt>**DT a \_ sinistra**</dt></span><span class="sxs-lookup"><span data-stu-id="df074-146"><dt>**DT\_LEFT**</dt></span></span> </dl>                   | <span data-ttu-id="df074-147">Allinea il testo a sinistra.</span><span class="sxs-lookup"><span data-stu-id="df074-147">Aligns text to the left.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| <span id="DT_NOCLIP"></span><span id="dt_noclip"></span><dl> <span data-ttu-id="df074-148"><dt>**DT \_ NOclip**</dt></span><span class="sxs-lookup"><span data-stu-id="df074-148"><dt>**DT\_NOCLIP**</dt></span></span> </dl>             | <span data-ttu-id="df074-149">Disegna senza ritaglio.</span><span class="sxs-lookup"><span data-stu-id="df074-149">Draws without clipping.</span></span> <span data-ttu-id="df074-150">**DrawText** è leggermente più veloce quando \_ si usa DT noclip.</span><span class="sxs-lookup"><span data-stu-id="df074-150">**DrawText** is somewhat faster when DT\_NOCLIP is used.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                         |
| <span id="DT_RIGHT"></span><span id="dt_right"></span><dl> <span data-ttu-id="df074-151"><dt>**DT a \_ destra**</dt></span><span class="sxs-lookup"><span data-stu-id="df074-151"><dt>**DT\_RIGHT**</dt></span></span> </dl>                | <span data-ttu-id="df074-152">Allinea il testo a destra.</span><span class="sxs-lookup"><span data-stu-id="df074-152">Aligns text to the right.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
| <span id="DT_RTLREADING"></span><span id="dt_rtlreading"></span><dl> <span data-ttu-id="df074-153"><dt>**DT \_ RTLREADING**</dt></span><span class="sxs-lookup"><span data-stu-id="df074-153"><dt>**DT\_RTLREADING**</dt></span></span> </dl> | <span data-ttu-id="df074-154">Visualizza il testo in ordine di lettura da destra a sinistra per il testo bidirezionale quando viene selezionato un tipo di carattere ebraico o arabo.</span><span class="sxs-lookup"><span data-stu-id="df074-154">Displays text in right-to-left reading order for bidirectional text when a Hebrew or Arabic font is selected.</span></span> <span data-ttu-id="df074-155">L'ordine di lettura predefinito per tutto il testo è da sinistra a destra.</span><span class="sxs-lookup"><span data-stu-id="df074-155">The default reading order for all text is left-to-right.</span></span><br/>                                                                                                                                                                                                                                                                                                                   |
| <span id="DT_SINGLELINE"></span><span id="dt_singleline"></span><dl> <span data-ttu-id="df074-156"><dt>**DT \_ Singleline**</dt></span><span class="sxs-lookup"><span data-stu-id="df074-156"><dt>**DT\_SINGLELINE**</dt></span></span> </dl> | <span data-ttu-id="df074-157">Visualizza il testo solo su una sola riga.</span><span class="sxs-lookup"><span data-stu-id="df074-157">Displays text on a single line only.</span></span> <span data-ttu-id="df074-158">I ritorni a capo e i feed di riga non interrompono la riga.</span><span class="sxs-lookup"><span data-stu-id="df074-158">Carriage returns and line feeds do not break the line.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                              |
| <span id="DT_TOP"></span><span id="dt_top"></span><dl> <span data-ttu-id="df074-159"><dt>**DT \_ superiore**</dt></span><span class="sxs-lookup"><span data-stu-id="df074-159"><dt>**DT\_TOP**</dt></span></span> </dl>                      | <span data-ttu-id="df074-160">Top: giustifica il testo.</span><span class="sxs-lookup"><span data-stu-id="df074-160">Top-justifies text.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| <span id="DT_VCENTER"></span><span id="dt_vcenter"></span><dl> <span data-ttu-id="df074-161"><dt>**\_vCenter vCenter**</dt></span><span class="sxs-lookup"><span data-stu-id="df074-161"><dt>**DT\_VCENTER**</dt></span></span> </dl>          | <span data-ttu-id="df074-162">Centra il testo verticalmente (solo riga singola).</span><span class="sxs-lookup"><span data-stu-id="df074-162">Centers text vertically (single line only).</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| <span id="DT_WORDBREAK"></span><span id="dt_wordbreak"></span><dl> <span data-ttu-id="df074-163"><dt>**DT \_ WordBreak**</dt></span><span class="sxs-lookup"><span data-stu-id="df074-163"><dt>**DT\_WORDBREAK**</dt></span></span> </dl>    | <span data-ttu-id="df074-164">Interrompe le parole.</span><span class="sxs-lookup"><span data-stu-id="df074-164">Breaks words.</span></span> <span data-ttu-id="df074-165">Le righe vengono interrotte automaticamente tra le parole se una parola si estende oltre il bordo del rettangolo specificato dal parametro pRect.</span><span class="sxs-lookup"><span data-stu-id="df074-165">Lines are automatically broken between words if a word would extend past the edge of the rectangle specified by the pRect parameter.</span></span> <span data-ttu-id="df074-166">Una sequenza di ritorno A capo/avanzamento riga interrompe anche la riga.</span><span class="sxs-lookup"><span data-stu-id="df074-166">A carriage return/line feed sequence also breaks the line.</span></span><br/>                                                                                                                                                                                                                                                                            |



 

</dd> <dt>

<span data-ttu-id="df074-167">*Colore* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="df074-167">*Color* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="df074-168">Tipo: **[ **D3DCOLOR**](d3dcolor.md)**</span><span class="sxs-lookup"><span data-stu-id="df074-168">Type: **[**D3DCOLOR**](d3dcolor.md)**</span></span>

<span data-ttu-id="df074-169">Colore del testo.</span><span class="sxs-lookup"><span data-stu-id="df074-169">Color of the text.</span></span> <span data-ttu-id="df074-170">Per ulteriori informazioni, vedere [**D3DCOLOR**](d3dcolor.md).</span><span class="sxs-lookup"><span data-stu-id="df074-170">For more information, see [**D3DCOLOR**](d3dcolor.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="df074-171">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="df074-171">Return value</span></span>

<span data-ttu-id="df074-172">Tipo: **[ **int**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="df074-172">Type: **[**INT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="df074-173">Se la funzione ha esito positivo, il valore restituito è l'altezza del testo nelle unità logiche.</span><span class="sxs-lookup"><span data-stu-id="df074-173">If the function succeeds, the return value is the height of the text in logical units.</span></span> <span data-ttu-id="df074-174">Se \_ si specifica DT vCenter o DT \_ Bottom, il valore restituito è l'offset da pRect (dall'alto verso il basso) del testo creato.</span><span class="sxs-lookup"><span data-stu-id="df074-174">If DT\_VCENTER or DT\_BOTTOM is specified, the return value is the offset from pRect (top to the bottom) of the drawn text.</span></span> <span data-ttu-id="df074-175">Se la funzione ha esito negativo, il valore restituito è zero.</span><span class="sxs-lookup"><span data-stu-id="df074-175">If the function fails, the return value is zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="df074-176">Commenti</span><span class="sxs-lookup"><span data-stu-id="df074-176">Remarks</span></span>

<span data-ttu-id="df074-177">I parametri di questo metodo sono molto simili a quelli della funzione [**DrawText**](/windows/win32/api/winuser/nf-winuser-drawtext) di GDI.</span><span class="sxs-lookup"><span data-stu-id="df074-177">The parameters of this method are very similar to those of the GDI [**DrawText**](/windows/win32/api/winuser/nf-winuser-drawtext) function.</span></span>

<span data-ttu-id="df074-178">Questo metodo supporta le stringhe ANSI e Unicode.</span><span class="sxs-lookup"><span data-stu-id="df074-178">This method supports both ANSI and Unicode strings.</span></span>

<span data-ttu-id="df074-179">Questo metodo deve essere chiamato all'interno di un [**BeginScene**](/windows/desktop/api) ... Blocco [**EndScene**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-endscene) .</span><span class="sxs-lookup"><span data-stu-id="df074-179">This method must be called inside a [**BeginScene**](/windows/desktop/api) ... [**EndScene**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-endscene) block.</span></span> <span data-ttu-id="df074-180">L'unica eccezione è rappresentata dal caso in cui un'applicazione chiama **DrawText** con DT \_ CALCRECT per calcolare le dimensioni di un blocco di testo specificato.</span><span class="sxs-lookup"><span data-stu-id="df074-180">The only exception is when an application calls **DrawText** with DT\_CALCRECT to calculate the size of a given block of text.</span></span>

<span data-ttu-id="df074-181">A meno che non \_ venga utilizzato il formato DT noclip, questo metodo consente di ritagliare il testo in modo che non venga visualizzato all'esterno del rettangolo specificato.</span><span class="sxs-lookup"><span data-stu-id="df074-181">Unless the DT\_NOCLIP format is used, this method clips the text so that it does not appear outside the specified rectangle.</span></span> <span data-ttu-id="df074-182">Si presuppone che tutte le formattazioni abbiano più righe, a meno che non \_ sia specificato il formato DT Singleline.</span><span class="sxs-lookup"><span data-stu-id="df074-182">All formatting is assumed to have multiple lines unless the DT\_SINGLELINE format is specified.</span></span>

<span data-ttu-id="df074-183">Se il tipo di carattere selezionato è troppo grande per il rettangolo, questo metodo non tenta di sostituire un tipo di carattere più piccolo.</span><span class="sxs-lookup"><span data-stu-id="df074-183">If the selected font is too large for the rectangle, this method does not attempt to substitute a smaller font.</span></span>

<span data-ttu-id="df074-184">Questo metodo supporta solo i tipi di carattere il cui scappamento e l'orientamento sono entrambi zero.</span><span class="sxs-lookup"><span data-stu-id="df074-184">This method supports only fonts whose escapement and orientation are both zero.</span></span>

## <a name="requirements"></a><span data-ttu-id="df074-185">Requisiti</span><span class="sxs-lookup"><span data-stu-id="df074-185">Requirements</span></span>



| <span data-ttu-id="df074-186">Requisito</span><span class="sxs-lookup"><span data-stu-id="df074-186">Requirement</span></span> | <span data-ttu-id="df074-187">Valore</span><span class="sxs-lookup"><span data-stu-id="df074-187">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="df074-188">Intestazione</span><span class="sxs-lookup"><span data-stu-id="df074-188">Header</span></span><br/>  | <dl> <span data-ttu-id="df074-189"><dt>D3dx9core. h</dt></span><span class="sxs-lookup"><span data-stu-id="df074-189"><dt>D3dx9core.h</dt></span></span> </dl> |
| <span data-ttu-id="df074-190">Libreria</span><span class="sxs-lookup"><span data-stu-id="df074-190">Library</span></span><br/> | <dl> <span data-ttu-id="df074-191"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="df074-191"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="df074-192">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="df074-192">See also</span></span>

<dl> <dt>

[<span data-ttu-id="df074-193">ID3DXFont</span><span class="sxs-lookup"><span data-stu-id="df074-193">ID3DXFont</span></span>](id3dxfont.md)
</dt> </dl>

 

 
