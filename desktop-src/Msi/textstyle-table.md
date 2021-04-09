---
description: La tabella TextStyle elenca diversi stili di carattere usati nei controlli con testo.
ms.assetid: a351e67a-8f51-41bf-9202-56488b870fa7
title: Tabella TextStyle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9c9993362228e37f01c0e53683755f7bd1310eaa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103966824"
---
# <a name="textstyle-table"></a><span data-ttu-id="3fb50-103">Tabella TextStyle</span><span class="sxs-lookup"><span data-stu-id="3fb50-103">TextStyle Table</span></span>

<span data-ttu-id="3fb50-104">La tabella TextStyle elenca diversi stili di carattere usati nei controlli con testo.</span><span class="sxs-lookup"><span data-stu-id="3fb50-104">The TextStyle table lists different font styles used in controls having text.</span></span>

<span data-ttu-id="3fb50-105">La tabella TextStyle include le colonne seguenti.</span><span class="sxs-lookup"><span data-stu-id="3fb50-105">The TextStyle table has the following columns.</span></span>



| <span data-ttu-id="3fb50-106">Colonna</span><span class="sxs-lookup"><span data-stu-id="3fb50-106">Column</span></span>    | <span data-ttu-id="3fb50-107">Tipo</span><span class="sxs-lookup"><span data-stu-id="3fb50-107">Type</span></span>                               | <span data-ttu-id="3fb50-108">Chiave</span><span class="sxs-lookup"><span data-stu-id="3fb50-108">Key</span></span> | <span data-ttu-id="3fb50-109">Nullable</span><span class="sxs-lookup"><span data-stu-id="3fb50-109">Nullable</span></span> |
|-----------|------------------------------------|-----|----------|
| <span data-ttu-id="3fb50-110">TextStyle</span><span class="sxs-lookup"><span data-stu-id="3fb50-110">TextStyle</span></span> | [<span data-ttu-id="3fb50-111">Identificatore</span><span class="sxs-lookup"><span data-stu-id="3fb50-111">Identifier</span></span>](identifier.md)       | <span data-ttu-id="3fb50-112">S</span><span class="sxs-lookup"><span data-stu-id="3fb50-112">Y</span></span>   | <span data-ttu-id="3fb50-113">N</span><span class="sxs-lookup"><span data-stu-id="3fb50-113">N</span></span>        |
| <span data-ttu-id="3fb50-114">Contemplato</span><span class="sxs-lookup"><span data-stu-id="3fb50-114">FaceName</span></span>  | [<span data-ttu-id="3fb50-115">Text</span><span class="sxs-lookup"><span data-stu-id="3fb50-115">Text</span></span>](text.md)                   | <span data-ttu-id="3fb50-116">N</span><span class="sxs-lookup"><span data-stu-id="3fb50-116">N</span></span>   | <span data-ttu-id="3fb50-117">N</span><span class="sxs-lookup"><span data-stu-id="3fb50-117">N</span></span>        |
| <span data-ttu-id="3fb50-118">Dimensione</span><span class="sxs-lookup"><span data-stu-id="3fb50-118">Size</span></span>      | [<span data-ttu-id="3fb50-119">Integer</span><span class="sxs-lookup"><span data-stu-id="3fb50-119">Integer</span></span>](integer.md)             | <span data-ttu-id="3fb50-120">N</span><span class="sxs-lookup"><span data-stu-id="3fb50-120">N</span></span>   | <span data-ttu-id="3fb50-121">N</span><span class="sxs-lookup"><span data-stu-id="3fb50-121">N</span></span>        |
| <span data-ttu-id="3fb50-122">Colore</span><span class="sxs-lookup"><span data-stu-id="3fb50-122">Color</span></span>     | [<span data-ttu-id="3fb50-123">DoubleInteger</span><span class="sxs-lookup"><span data-stu-id="3fb50-123">DoubleInteger</span></span>](doubleinteger.md) | <span data-ttu-id="3fb50-124">N</span><span class="sxs-lookup"><span data-stu-id="3fb50-124">N</span></span>   | <span data-ttu-id="3fb50-125">S</span><span class="sxs-lookup"><span data-stu-id="3fb50-125">Y</span></span>        |
| <span data-ttu-id="3fb50-126">StyleBits</span><span class="sxs-lookup"><span data-stu-id="3fb50-126">StyleBits</span></span> | [<span data-ttu-id="3fb50-127">Integer</span><span class="sxs-lookup"><span data-stu-id="3fb50-127">Integer</span></span>](integer.md)             | <span data-ttu-id="3fb50-128">N</span><span class="sxs-lookup"><span data-stu-id="3fb50-128">N</span></span>   | <span data-ttu-id="3fb50-129">S</span><span class="sxs-lookup"><span data-stu-id="3fb50-129">Y</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="3fb50-130">Colonne</span><span class="sxs-lookup"><span data-stu-id="3fb50-130">Columns</span></span>

<dl> <dt>

<span data-ttu-id="3fb50-131"><span id="TextStyle"></span><span id="textstyle"></span><span id="TEXTSTYLE"></span>TextStyle</span><span class="sxs-lookup"><span data-stu-id="3fb50-131"><span id="TextStyle"></span><span id="textstyle"></span><span id="TEXTSTYLE"></span>TextStyle</span></span>
</dt> <dd>

<span data-ttu-id="3fb50-132">Questa colonna è il nome dello stile del tipo di carattere.</span><span class="sxs-lookup"><span data-stu-id="3fb50-132">This column is the name of the font style.</span></span> <span data-ttu-id="3fb50-133">Questo nome può essere incorporato nella stringa di testo per indicare una modifica dello stile.</span><span class="sxs-lookup"><span data-stu-id="3fb50-133">This name can be embedded in the text string to indicate a style change.</span></span> <span data-ttu-id="3fb50-134">Si noti che il nome dello stile del tipo di carattere usato in questo campo non deve terminare con i caratteri: \_ ul.</span><span class="sxs-lookup"><span data-stu-id="3fb50-134">Note that the font style name used in this field must not end with the characters: \_UL.</span></span> <span data-ttu-id="3fb50-135">Vedere [aggiunta di controlli e testo](adding-controls-and-text.md).</span><span class="sxs-lookup"><span data-stu-id="3fb50-135">See [Adding Controls and Text](adding-controls-and-text.md).</span></span>

</dd> <dt>

<span data-ttu-id="3fb50-136"><span id="FaceName"></span><span id="facename"></span><span id="FACENAME"></span>Contemplato</span><span class="sxs-lookup"><span data-stu-id="3fb50-136"><span id="FaceName"></span><span id="facename"></span><span id="FACENAME"></span>FaceName</span></span>
</dt> <dd>

<span data-ttu-id="3fb50-137">Stringa che indica il nome del tipo di carattere.</span><span class="sxs-lookup"><span data-stu-id="3fb50-137">A string indicating the name of the font.</span></span> <span data-ttu-id="3fb50-138">La lunghezza della stringa non deve superare i 31 caratteri.</span><span class="sxs-lookup"><span data-stu-id="3fb50-138">The string must be no more than 31 characters long.</span></span>

</dd> <dt>

<span data-ttu-id="3fb50-139"><span id="Size"></span><span id="size"></span><span id="SIZE"></span>Dimensioni</span><span class="sxs-lookup"><span data-stu-id="3fb50-139"><span id="Size"></span><span id="size"></span><span id="SIZE"></span>Size</span></span>
</dt> <dd>

<span data-ttu-id="3fb50-140">Dimensione del carattere misurata in punti.</span><span class="sxs-lookup"><span data-stu-id="3fb50-140">The font size measured in points.</span></span> <span data-ttu-id="3fb50-141">Deve essere un numero non negativo.</span><span class="sxs-lookup"><span data-stu-id="3fb50-141">This must be a non-negative number.</span></span>

</dd> <dt>

<span data-ttu-id="3fb50-142"><span id="Color"></span><span id="color"></span><span id="COLOR"></span>Colore</span><span class="sxs-lookup"><span data-stu-id="3fb50-142"><span id="Color"></span><span id="color"></span><span id="COLOR"></span>Color</span></span>
</dt> <dd>

<span data-ttu-id="3fb50-143">In questa colonna viene specificato il colore del testo visualizzato da un [controllo di testo](text-control.md).</span><span class="sxs-lookup"><span data-stu-id="3fb50-143">This column specifies the text color displayed by a [Text Control](text-control.md).</span></span> <span data-ttu-id="3fb50-144">Tutti gli altri tipi di controlli utilizzano sempre il colore predefinito del testo.</span><span class="sxs-lookup"><span data-stu-id="3fb50-144">All other types of controls always use the default text color.</span></span> <span data-ttu-id="3fb50-145">Il valore inserito in questa colonna deve essere calcolato utilizzando la formula seguente: 65536 \* blu + 256 \* verde + rosso, dove rosso, verde e blu sono ciascuno nell'intervallo 0-255.</span><span class="sxs-lookup"><span data-stu-id="3fb50-145">The value put in this column should be computed using the following formula: 65536 \* blue + 256 \* green + red, where red, green, and blue are each in the range of 0-255.</span></span> <span data-ttu-id="3fb50-146">Il valore non deve superare 16777215, ovvero il valore per il bianco.</span><span class="sxs-lookup"><span data-stu-id="3fb50-146">The value must not exceed 16777215, which is the value for white.</span></span> <span data-ttu-id="3fb50-147">Il valore è 0 per il nero, 255 per il rosso, 65280 per il verde, 16711680 per il blu e 8421504 per il grigio.</span><span class="sxs-lookup"><span data-stu-id="3fb50-147">The value is 0 for black, 255 for red, 65280 for green, 16711680 for blue and 8421504 for grey.</span></span> <span data-ttu-id="3fb50-148">Se si lascia vuoto il campo, viene specificato il colore predefinito.</span><span class="sxs-lookup"><span data-stu-id="3fb50-148">Leaving the field empty specifies the default color.</span></span>

<span data-ttu-id="3fb50-149">Non posizionare [controlli testo](text-control.md) trasparenti su bitmap colorate.</span><span class="sxs-lookup"><span data-stu-id="3fb50-149">Do not place transparent [Text controls](text-control.md) on top of colored bitmaps.</span></span> <span data-ttu-id="3fb50-150">Il testo potrebbe non essere visibile se l'utente modifica la combinazione di colori di visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="3fb50-150">The text may not be visible if the user changes the display color scheme.</span></span> <span data-ttu-id="3fb50-151">Ad esempio, il testo potrebbe diventare invisibile se l'utente imposta il parametro a contrasto elevato per l'accessibilità.</span><span class="sxs-lookup"><span data-stu-id="3fb50-151">For example, text may become invisible if the user sets the high contrast parameter for accessibility.</span></span>

</dd> <dt>

<span data-ttu-id="3fb50-152"><span id="StyleBits"></span><span id="stylebits"></span><span id="STYLEBITS"></span>StyleBits</span><span class="sxs-lookup"><span data-stu-id="3fb50-152"><span id="StyleBits"></span><span id="stylebits"></span><span id="STYLEBITS"></span>StyleBits</span></span>
</dt> <dd>

<span data-ttu-id="3fb50-153">Combinazione di bit che indica la formattazione del testo.</span><span class="sxs-lookup"><span data-stu-id="3fb50-153">A combination of bits indicating the formatting for the text.</span></span>

<span data-ttu-id="3fb50-154">I singoli bit di stile hanno i valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="3fb50-154">The individual style bits have the following values.</span></span>



| <span data-ttu-id="3fb50-155">Costante</span><span class="sxs-lookup"><span data-stu-id="3fb50-155">Constant</span></span>                             | <span data-ttu-id="3fb50-156">Valore esadecimale</span><span class="sxs-lookup"><span data-stu-id="3fb50-156">Hexadecimal</span></span> | <span data-ttu-id="3fb50-157">Decimal</span><span class="sxs-lookup"><span data-stu-id="3fb50-157">Decimal</span></span> | <span data-ttu-id="3fb50-158">Stile</span><span class="sxs-lookup"><span data-stu-id="3fb50-158">Style</span></span>      |
|--------------------------------------|-------------|---------|------------|
| <span data-ttu-id="3fb50-159">**msidbTextStyleStyleBitsBold**</span><span class="sxs-lookup"><span data-stu-id="3fb50-159">**msidbTextStyleStyleBitsBold**</span></span>      | <span data-ttu-id="3fb50-160">0x001</span><span class="sxs-lookup"><span data-stu-id="3fb50-160">0x001</span></span>       | <span data-ttu-id="3fb50-161">1</span><span class="sxs-lookup"><span data-stu-id="3fb50-161">1</span></span>       | <span data-ttu-id="3fb50-162">Grassetto</span><span class="sxs-lookup"><span data-stu-id="3fb50-162">Bold</span></span>       |
| <span data-ttu-id="3fb50-163">**msidbTextStyleStyleBitsItalic**</span><span class="sxs-lookup"><span data-stu-id="3fb50-163">**msidbTextStyleStyleBitsItalic**</span></span>    | <span data-ttu-id="3fb50-164">0x002</span><span class="sxs-lookup"><span data-stu-id="3fb50-164">0x002</span></span>       | <span data-ttu-id="3fb50-165">2</span><span class="sxs-lookup"><span data-stu-id="3fb50-165">2</span></span>       | <span data-ttu-id="3fb50-166">Corsivo</span><span class="sxs-lookup"><span data-stu-id="3fb50-166">Italic</span></span>     |
| <span data-ttu-id="3fb50-167">**msidbTextStyleStyleBitsUnderline**</span><span class="sxs-lookup"><span data-stu-id="3fb50-167">**msidbTextStyleStyleBitsUnderline**</span></span> | <span data-ttu-id="3fb50-168">0x004</span><span class="sxs-lookup"><span data-stu-id="3fb50-168">0x004</span></span>       | <span data-ttu-id="3fb50-169">4</span><span class="sxs-lookup"><span data-stu-id="3fb50-169">4</span></span>       | <span data-ttu-id="3fb50-170">Sottolineato</span><span class="sxs-lookup"><span data-stu-id="3fb50-170">Underline</span></span>  |
| <span data-ttu-id="3fb50-171">**msidbTextStyleStyleBitsStrike**</span><span class="sxs-lookup"><span data-stu-id="3fb50-171">**msidbTextStyleStyleBitsStrike**</span></span>    | <span data-ttu-id="3fb50-172">0x008</span><span class="sxs-lookup"><span data-stu-id="3fb50-172">0x008</span></span>       | <span data-ttu-id="3fb50-173">8</span><span class="sxs-lookup"><span data-stu-id="3fb50-173">8</span></span>       | <span data-ttu-id="3fb50-174">Sciopero</span><span class="sxs-lookup"><span data-stu-id="3fb50-174">Strike out</span></span> |



 

</dd> </dl>

## <a name="validation"></a><span data-ttu-id="3fb50-175">Convalida</span><span class="sxs-lookup"><span data-stu-id="3fb50-175">Validation</span></span>

<dl>

[<span data-ttu-id="3fb50-176">ICE03</span><span class="sxs-lookup"><span data-stu-id="3fb50-176">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="3fb50-177">ICE06</span><span class="sxs-lookup"><span data-stu-id="3fb50-177">ICE06</span></span>](ice06.md)  
[<span data-ttu-id="3fb50-178">ICE31</span><span class="sxs-lookup"><span data-stu-id="3fb50-178">ICE31</span></span>](ice31.md)  
[<span data-ttu-id="3fb50-179">ICE45</span><span class="sxs-lookup"><span data-stu-id="3fb50-179">ICE45</span></span>](ice45.md)  
</dl>

 

 



