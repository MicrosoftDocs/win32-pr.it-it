---
title: Struttura FONTDIRENTRY
description: Contiene informazioni su un singolo tipo di carattere in un gruppo di risorse dei tipi di carattere. La definizione della struttura fornita qui è solo per la spiegazione. non è presente in alcun file di intestazione standard.
ms.assetid: 0ada2afe-b299-4ef2-99b7-96da10ee218a
keywords:
- Menu struttura FONTDIRENTRY e altre risorse
topic_type:
- apiref
api_name:
- FONTDIRENTRY
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 1cee72a490fd2b94b1c810797f656d81418c0f71
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104475772"
---
# <a name="fontdirentry-structure"></a><span data-ttu-id="54ccb-105">Struttura FONTDIRENTRY</span><span class="sxs-lookup"><span data-stu-id="54ccb-105">FONTDIRENTRY structure</span></span>

<span data-ttu-id="54ccb-106">Contiene informazioni su un singolo tipo di carattere in un gruppo di risorse dei tipi di carattere.</span><span class="sxs-lookup"><span data-stu-id="54ccb-106">Contains information about an individual font in a font resource group.</span></span> <span data-ttu-id="54ccb-107">La definizione della struttura fornita qui è solo per la spiegazione. non è presente in alcun file di intestazione standard.</span><span class="sxs-lookup"><span data-stu-id="54ccb-107">The structure definition provided here is for explanation only; it is not present in any standard header file.</span></span>

## <a name="syntax"></a><span data-ttu-id="54ccb-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="54ccb-108">Syntax</span></span>


```C++
typedef struct {
  WORD  dfVersion;
  DWORD dfSize;
  CHAR  dfCopyright[60];
  WORD  dfType;
  WORD  dfPoints;
  WORD  dfVertRes;
  WORD  dfHorizRes;
  WORD  dfAscent;
  WORD  dfInternalLeading;
  WORD  dfExternalLeading;
  BYTE  dfItalic;
  BYTE  dfUnderline;
  BYTE  dfStrikeOut;
  WORD  dfWeight;
  BYTE  dfCharSet;
  WORD  dfPixWidth;
  WORD  dfPixHeight;
  BYTE  dfPitchAndFamily;
  WORD  dfAvgWidth;
  WORD  dfMaxWidth;
  BYTE  dfFirstChar;
  BYTE  dfLastChar;
  BYTE  dfDefaultChar;
  BYTE  dfBreakChar;
  WORD  dfWidthBytes;
  DWORD dfDevice;
  DWORD dfFace;
  DWORD dfReserved;
  CHAR  szDeviceName;
  CHAR  szFaceName;
} FONTDIRENTRY;
```



## <a name="members"></a><span data-ttu-id="54ccb-109">Members</span><span class="sxs-lookup"><span data-stu-id="54ccb-109">Members</span></span>

<dl> <dt>

<span data-ttu-id="54ccb-110">**dfVersion**</span><span class="sxs-lookup"><span data-stu-id="54ccb-110">**dfVersion**</span></span>
</dt> <dd>

<span data-ttu-id="54ccb-111">Tipo: **Word**</span><span class="sxs-lookup"><span data-stu-id="54ccb-111">Type: **WORD**</span></span>

</dd> <dd>

<span data-ttu-id="54ccb-112">Numero di versione definito dall'utente per i dati della risorsa che gli strumenti possono usare per leggere e scrivere i file di risorse.</span><span class="sxs-lookup"><span data-stu-id="54ccb-112">A user-defined version number for the resource data that tools can use to read and write resource files.</span></span>

</dd> <dt>

<span data-ttu-id="54ccb-113">**dfSize**</span><span class="sxs-lookup"><span data-stu-id="54ccb-113">**dfSize**</span></span>
</dt> <dd>

<span data-ttu-id="54ccb-114">Tipo: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="54ccb-114">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="54ccb-115">Dimensioni, in byte, del file.</span><span class="sxs-lookup"><span data-stu-id="54ccb-115">The size of the file, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="54ccb-116">**dfCopyright \[ 60\]**</span><span class="sxs-lookup"><span data-stu-id="54ccb-116">**dfCopyright\[60\]**</span></span>
</dt> <dd>

<span data-ttu-id="54ccb-117">Tipo: **char**</span><span class="sxs-lookup"><span data-stu-id="54ccb-117">Type: **CHAR**</span></span>

</dd> <dd>

<span data-ttu-id="54ccb-118">Informazioni sul copyright del fornitore di tipi di carattere.</span><span class="sxs-lookup"><span data-stu-id="54ccb-118">The font supplier's copyright information.</span></span>

</dd> <dt>

<span data-ttu-id="54ccb-119">**dfType**</span><span class="sxs-lookup"><span data-stu-id="54ccb-119">**dfType**</span></span>
</dt> <dd>

<span data-ttu-id="54ccb-120">Tipo: **Word**</span><span class="sxs-lookup"><span data-stu-id="54ccb-120">Type: **WORD**</span></span>

</dd> <dd>

<span data-ttu-id="54ccb-121">Tipo di file del tipo di carattere.</span><span class="sxs-lookup"><span data-stu-id="54ccb-121">The type of font file.</span></span>

</dd> <dt>

<span data-ttu-id="54ccb-122">**dfPoints**</span><span class="sxs-lookup"><span data-stu-id="54ccb-122">**dfPoints**</span></span>
</dt> <dd>

<span data-ttu-id="54ccb-123">Tipo: **Word**</span><span class="sxs-lookup"><span data-stu-id="54ccb-123">Type: **WORD**</span></span>

</dd> <dd>

<span data-ttu-id="54ccb-124">Dimensioni del punto in cui il set di caratteri è migliore.</span><span class="sxs-lookup"><span data-stu-id="54ccb-124">The point size at which this character set looks best.</span></span>

</dd> <dt>

<span data-ttu-id="54ccb-125">**dfVertRes**</span><span class="sxs-lookup"><span data-stu-id="54ccb-125">**dfVertRes**</span></span>
</dt> <dd>

<span data-ttu-id="54ccb-126">Tipo: **Word**</span><span class="sxs-lookup"><span data-stu-id="54ccb-126">Type: **WORD**</span></span>

</dd> <dd>

<span data-ttu-id="54ccb-127">Risoluzione verticale, espressa in punti per pollice, in cui il set di caratteri è stato digitato.</span><span class="sxs-lookup"><span data-stu-id="54ccb-127">The vertical resolution, in dots per inch, at which this character set was digitized.</span></span>

</dd> <dt>

<span data-ttu-id="54ccb-128">**dfHorizRes**</span><span class="sxs-lookup"><span data-stu-id="54ccb-128">**dfHorizRes**</span></span>
</dt> <dd>

<span data-ttu-id="54ccb-129">Tipo: **Word**</span><span class="sxs-lookup"><span data-stu-id="54ccb-129">Type: **WORD**</span></span>

</dd> <dd>

<span data-ttu-id="54ccb-130">Risoluzione orizzontale, espressa in punti per pollice, in cui il set di caratteri è stato digitato.</span><span class="sxs-lookup"><span data-stu-id="54ccb-130">The horizontal resolution, in dots per inch, at which this character set was digitized.</span></span>

</dd> <dt>

<span data-ttu-id="54ccb-131">**dfAscent**</span><span class="sxs-lookup"><span data-stu-id="54ccb-131">**dfAscent**</span></span>
</dt> <dd>

<span data-ttu-id="54ccb-132">Tipo: **Word**</span><span class="sxs-lookup"><span data-stu-id="54ccb-132">Type: **WORD**</span></span>

</dd> <dd>

<span data-ttu-id="54ccb-133">Distanza tra la parte superiore di una cella di definizione dei caratteri e la linea di base del tipo di carattere tipografico.</span><span class="sxs-lookup"><span data-stu-id="54ccb-133">The distance from the top of a character definition cell to the baseline of the typographical font.</span></span>

</dd> <dt>

<span data-ttu-id="54ccb-134">**dfInternalLeading**</span><span class="sxs-lookup"><span data-stu-id="54ccb-134">**dfInternalLeading**</span></span>
</dt> <dd>

<span data-ttu-id="54ccb-135">Tipo: **Word**</span><span class="sxs-lookup"><span data-stu-id="54ccb-135">Type: **WORD**</span></span>

</dd> <dd>

<span data-ttu-id="54ccb-136">Quantità di iniziali all'interno dei limiti impostati dal membro **dfPixHeight** .</span><span class="sxs-lookup"><span data-stu-id="54ccb-136">The amount of leading inside the bounds set by the **dfPixHeight** member.</span></span> <span data-ttu-id="54ccb-137">In quest'area possono essere presenti contrassegni accentati e altri caratteri diacritici.</span><span class="sxs-lookup"><span data-stu-id="54ccb-137">Accent marks and other diacritical characters can occur in this area.</span></span>

</dd> <dt>

<span data-ttu-id="54ccb-138">**dfExternalLeading**</span><span class="sxs-lookup"><span data-stu-id="54ccb-138">**dfExternalLeading**</span></span>
</dt> <dd>

<span data-ttu-id="54ccb-139">Tipo: **Word**</span><span class="sxs-lookup"><span data-stu-id="54ccb-139">Type: **WORD**</span></span>

</dd> <dd>

<span data-ttu-id="54ccb-140">Quantità di porta aggiuntiva che l'applicazione aggiunge tra le righe.</span><span class="sxs-lookup"><span data-stu-id="54ccb-140">The amount of extra leading that the application adds between rows.</span></span>

</dd> <dt>

<span data-ttu-id="54ccb-141">**dfItalic**</span><span class="sxs-lookup"><span data-stu-id="54ccb-141">**dfItalic**</span></span>
</dt> <dd>

<span data-ttu-id="54ccb-142">Tipo: **byte**</span><span class="sxs-lookup"><span data-stu-id="54ccb-142">Type: **BYTE**</span></span>

</dd> <dd>

<span data-ttu-id="54ccb-143">Un tipo di carattere corsivo se non uguale a zero.</span><span class="sxs-lookup"><span data-stu-id="54ccb-143">An italic font if not equal to zero.</span></span>

</dd> <dt>

<span data-ttu-id="54ccb-144">**dfUnderline**</span><span class="sxs-lookup"><span data-stu-id="54ccb-144">**dfUnderline**</span></span>
</dt> <dd>

<span data-ttu-id="54ccb-145">Tipo: **byte**</span><span class="sxs-lookup"><span data-stu-id="54ccb-145">Type: **BYTE**</span></span>

</dd> <dd>

<span data-ttu-id="54ccb-146">Carattere sottolineato se non uguale a zero.</span><span class="sxs-lookup"><span data-stu-id="54ccb-146">An underlined font if not equal to zero.</span></span>

</dd> <dt>

<span data-ttu-id="54ccb-147">**dfStrikeOut**</span><span class="sxs-lookup"><span data-stu-id="54ccb-147">**dfStrikeOut**</span></span>
</dt> <dd>

<span data-ttu-id="54ccb-148">Tipo: **byte**</span><span class="sxs-lookup"><span data-stu-id="54ccb-148">Type: **BYTE**</span></span>

</dd> <dd>

<span data-ttu-id="54ccb-149">Un tipo di carattere di attacco se non è uguale a zero.</span><span class="sxs-lookup"><span data-stu-id="54ccb-149">A strikeout font if not equal to zero.</span></span>

</dd> <dt>

<span data-ttu-id="54ccb-150">**dfWeight**</span><span class="sxs-lookup"><span data-stu-id="54ccb-150">**dfWeight**</span></span>
</dt> <dd>

<span data-ttu-id="54ccb-151">Tipo: **Word**</span><span class="sxs-lookup"><span data-stu-id="54ccb-151">Type: **WORD**</span></span>

</dd> <dd>

<span data-ttu-id="54ccb-152">Spessore del tipo di carattere nell'intervallo compreso tra 0 e 1000.</span><span class="sxs-lookup"><span data-stu-id="54ccb-152">The weight of the font in the range 0 through 1000.</span></span> <span data-ttu-id="54ccb-153">400, ad esempio, è Roman e 700 è in grassetto.</span><span class="sxs-lookup"><span data-stu-id="54ccb-153">For example, 400 is roman and 700 is bold.</span></span> <span data-ttu-id="54ccb-154">Se questo valore è zero, viene utilizzato un peso predefinito.</span><span class="sxs-lookup"><span data-stu-id="54ccb-154">If this value is zero, a default weight is used.</span></span> <span data-ttu-id="54ccb-155">Per altri valori definiti, vedere la descrizione della struttura [**LOGFONT**](/windows/win32/api/wingdi/ns-wingdi-logfonta) .</span><span class="sxs-lookup"><span data-stu-id="54ccb-155">For additional defined values, see the description of the [**LOGFONT**](/windows/win32/api/wingdi/ns-wingdi-logfonta) structure.</span></span>

</dd> <dt>

<span data-ttu-id="54ccb-156">**dfCharSet**</span><span class="sxs-lookup"><span data-stu-id="54ccb-156">**dfCharSet**</span></span>
</dt> <dd>

<span data-ttu-id="54ccb-157">Tipo: **byte**</span><span class="sxs-lookup"><span data-stu-id="54ccb-157">Type: **BYTE**</span></span>

</dd> <dd>

<span data-ttu-id="54ccb-158">Set di caratteri del tipo di carattere.</span><span class="sxs-lookup"><span data-stu-id="54ccb-158">The character set of the font.</span></span> <span data-ttu-id="54ccb-159">Per i valori predefiniti, vedere la descrizione della struttura [**LOGFONT**](/windows/win32/api/wingdi/ns-wingdi-logfonta) .</span><span class="sxs-lookup"><span data-stu-id="54ccb-159">For predefined values, see the description of the [**LOGFONT**](/windows/win32/api/wingdi/ns-wingdi-logfonta) structure.</span></span>

</dd> <dt>

<span data-ttu-id="54ccb-160">**dfPixWidth**</span><span class="sxs-lookup"><span data-stu-id="54ccb-160">**dfPixWidth**</span></span>
</dt> <dd>

<span data-ttu-id="54ccb-161">Tipo: **Word**</span><span class="sxs-lookup"><span data-stu-id="54ccb-161">Type: **WORD**</span></span>

</dd> <dd>

<span data-ttu-id="54ccb-162">Larghezza della griglia in cui è stato digitato un tipo di carattere vettoriale.</span><span class="sxs-lookup"><span data-stu-id="54ccb-162">The width of the grid on which a vector font was digitized.</span></span> <span data-ttu-id="54ccb-163">Per i tipi di carattere raster, se il membro non è uguale a zero, rappresenta la larghezza per tutti i caratteri nella bitmap.</span><span class="sxs-lookup"><span data-stu-id="54ccb-163">For raster fonts, if the member is not equal to zero, it represents the width for all the characters in the bitmap.</span></span> <span data-ttu-id="54ccb-164">Se il membro è uguale a zero, il tipo di carattere ha caratteri a larghezza variabile.</span><span class="sxs-lookup"><span data-stu-id="54ccb-164">If the member is equal to zero, the font has variable-width characters.</span></span>

</dd> <dt>

<span data-ttu-id="54ccb-165">**dfPixHeight**</span><span class="sxs-lookup"><span data-stu-id="54ccb-165">**dfPixHeight**</span></span>
</dt> <dd>

<span data-ttu-id="54ccb-166">Tipo: **Word**</span><span class="sxs-lookup"><span data-stu-id="54ccb-166">Type: **WORD**</span></span>

</dd> <dd>

<span data-ttu-id="54ccb-167">Altezza della bitmap dei caratteri per i tipi di carattere raster o l'altezza della griglia in cui è stato digitalizzato un tipo di carattere vettoriale.</span><span class="sxs-lookup"><span data-stu-id="54ccb-167">The height of the character bitmap for raster fonts or the height of the grid on which a vector font was digitized.</span></span>

</dd> <dt>

<span data-ttu-id="54ccb-168">**dfPitchAndFamily**</span><span class="sxs-lookup"><span data-stu-id="54ccb-168">**dfPitchAndFamily**</span></span>
</dt> <dd>

<span data-ttu-id="54ccb-169">Tipo: **byte**</span><span class="sxs-lookup"><span data-stu-id="54ccb-169">Type: **BYTE**</span></span>

</dd> <dd>

<span data-ttu-id="54ccb-170">Il pitch e la famiglia del tipo di carattere.</span><span class="sxs-lookup"><span data-stu-id="54ccb-170">The pitch and the family of the font.</span></span> <span data-ttu-id="54ccb-171">Per ulteriori informazioni, vedere la descrizione della struttura [**LOGFONT**](/windows/win32/api/wingdi/ns-wingdi-logfonta) .</span><span class="sxs-lookup"><span data-stu-id="54ccb-171">For additional information, see the description of the [**LOGFONT**](/windows/win32/api/wingdi/ns-wingdi-logfonta) structure.</span></span>

</dd> <dt>

<span data-ttu-id="54ccb-172">**dfAvgWidth**</span><span class="sxs-lookup"><span data-stu-id="54ccb-172">**dfAvgWidth**</span></span>
</dt> <dd>

<span data-ttu-id="54ccb-173">Tipo: **Word**</span><span class="sxs-lookup"><span data-stu-id="54ccb-173">Type: **WORD**</span></span>

</dd> <dd>

<span data-ttu-id="54ccb-174">Larghezza media dei caratteri nel tipo di carattere, generalmente definita come larghezza della lettera x.</span><span class="sxs-lookup"><span data-stu-id="54ccb-174">The average width of characters in the font (generally defined as the width of the letter x).</span></span> <span data-ttu-id="54ccb-175">Questo valore non include la sporgenza richiesta per i caratteri in grassetto o in corsivo.</span><span class="sxs-lookup"><span data-stu-id="54ccb-175">This value does not include the overhang required for bold or italic characters.</span></span>

</dd> <dt>

<span data-ttu-id="54ccb-176">**dfMaxWidth**</span><span class="sxs-lookup"><span data-stu-id="54ccb-176">**dfMaxWidth**</span></span>
</dt> <dd>

<span data-ttu-id="54ccb-177">Tipo: **Word**</span><span class="sxs-lookup"><span data-stu-id="54ccb-177">Type: **WORD**</span></span>

</dd> <dd>

<span data-ttu-id="54ccb-178">Larghezza del carattere più largo nel tipo di carattere.</span><span class="sxs-lookup"><span data-stu-id="54ccb-178">The width of the widest character in the font.</span></span>

</dd> <dt>

<span data-ttu-id="54ccb-179">**dfFirstChar**</span><span class="sxs-lookup"><span data-stu-id="54ccb-179">**dfFirstChar**</span></span>
</dt> <dd>

<span data-ttu-id="54ccb-180">Tipo: **byte**</span><span class="sxs-lookup"><span data-stu-id="54ccb-180">Type: **BYTE**</span></span>

</dd> <dd>

<span data-ttu-id="54ccb-181">Primo codice carattere definito nel tipo di carattere.</span><span class="sxs-lookup"><span data-stu-id="54ccb-181">The first character code defined in the font.</span></span>

</dd> <dt>

<span data-ttu-id="54ccb-182">**dfLastChar**</span><span class="sxs-lookup"><span data-stu-id="54ccb-182">**dfLastChar**</span></span>
</dt> <dd>

<span data-ttu-id="54ccb-183">Tipo: **byte**</span><span class="sxs-lookup"><span data-stu-id="54ccb-183">Type: **BYTE**</span></span>

</dd> <dd>

<span data-ttu-id="54ccb-184">Ultimo codice carattere definito nel tipo di carattere.</span><span class="sxs-lookup"><span data-stu-id="54ccb-184">The last character code defined in the font.</span></span>

</dd> <dt>

<span data-ttu-id="54ccb-185">**dfDefaultChar**</span><span class="sxs-lookup"><span data-stu-id="54ccb-185">**dfDefaultChar**</span></span>
</dt> <dd>

<span data-ttu-id="54ccb-186">Tipo: **byte**</span><span class="sxs-lookup"><span data-stu-id="54ccb-186">Type: **BYTE**</span></span>

</dd> <dd>

<span data-ttu-id="54ccb-187">Carattere da sostituire per i caratteri non presenti nel tipo di carattere.</span><span class="sxs-lookup"><span data-stu-id="54ccb-187">The character to substitute for characters not in the font.</span></span>

</dd> <dt>

<span data-ttu-id="54ccb-188">**dfBreakChar**</span><span class="sxs-lookup"><span data-stu-id="54ccb-188">**dfBreakChar**</span></span>
</dt> <dd>

<span data-ttu-id="54ccb-189">Tipo: **byte**</span><span class="sxs-lookup"><span data-stu-id="54ccb-189">Type: **BYTE**</span></span>

</dd> <dd>

<span data-ttu-id="54ccb-190">Carattere che verrà utilizzato per definire le interruzioni di parola per la giustificazione del testo.</span><span class="sxs-lookup"><span data-stu-id="54ccb-190">The character that will be used to define word breaks for text justification.</span></span>

</dd> <dt>

<span data-ttu-id="54ccb-191">**dfWidthBytes**</span><span class="sxs-lookup"><span data-stu-id="54ccb-191">**dfWidthBytes**</span></span>
</dt> <dd>

<span data-ttu-id="54ccb-192">Tipo: **Word**</span><span class="sxs-lookup"><span data-stu-id="54ccb-192">Type: **WORD**</span></span>

</dd> <dd>

<span data-ttu-id="54ccb-193">Numero di byte in ogni riga della bitmap.</span><span class="sxs-lookup"><span data-stu-id="54ccb-193">The number of bytes in each row of the bitmap.</span></span> <span data-ttu-id="54ccb-194">Questo valore è sempre pari, in modo che le righe vengano avviate sui limiti di parola.</span><span class="sxs-lookup"><span data-stu-id="54ccb-194">This value is always even so that the rows start on word boundaries.</span></span> <span data-ttu-id="54ccb-195">Per i tipi di carattere vettoriali, questo membro non ha alcun significato.</span><span class="sxs-lookup"><span data-stu-id="54ccb-195">For vector fonts, this member has no meaning.</span></span>

</dd> <dt>

<span data-ttu-id="54ccb-196">**dfDevice**</span><span class="sxs-lookup"><span data-stu-id="54ccb-196">**dfDevice**</span></span>
</dt> <dd>

<span data-ttu-id="54ccb-197">Tipo: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="54ccb-197">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="54ccb-198">Offset nel file a una stringa con terminazione null che specifica il nome di un dispositivo.</span><span class="sxs-lookup"><span data-stu-id="54ccb-198">The offset in the file to a null-terminated string that specifies a device name.</span></span> <span data-ttu-id="54ccb-199">Per un tipo di carattere generico, questo valore è zero.</span><span class="sxs-lookup"><span data-stu-id="54ccb-199">For a generic font, this value is zero.</span></span>

</dd> <dt>

<span data-ttu-id="54ccb-200">**dfFace**</span><span class="sxs-lookup"><span data-stu-id="54ccb-200">**dfFace**</span></span>
</dt> <dd>

<span data-ttu-id="54ccb-201">Tipo: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="54ccb-201">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="54ccb-202">Offset nel file a una stringa con terminazione null che denomina il carattere tipografico.</span><span class="sxs-lookup"><span data-stu-id="54ccb-202">The offset in the file to a null-terminated string that names the typeface.</span></span>

</dd> <dt>

<span data-ttu-id="54ccb-203">**dfReserved**</span><span class="sxs-lookup"><span data-stu-id="54ccb-203">**dfReserved**</span></span>
</dt> <dd>

<span data-ttu-id="54ccb-204">Tipo: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="54ccb-204">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="54ccb-205">Questo membro è riservato.</span><span class="sxs-lookup"><span data-stu-id="54ccb-205">This member is reserved.</span></span>

</dd> <dt>

<span data-ttu-id="54ccb-206">**szDeviceName**</span><span class="sxs-lookup"><span data-stu-id="54ccb-206">**szDeviceName**</span></span>
</dt> <dd>

<span data-ttu-id="54ccb-207">Tipo: **char**</span><span class="sxs-lookup"><span data-stu-id="54ccb-207">Type: **CHAR**</span></span>

</dd> <dd>

<span data-ttu-id="54ccb-208">Nome del dispositivo se il file del tipo di carattere è designato per un dispositivo specifico.</span><span class="sxs-lookup"><span data-stu-id="54ccb-208">The name of the device if this font file is designated for a specific device.</span></span>

</dd> <dt>

<span data-ttu-id="54ccb-209">**szFaceName**</span><span class="sxs-lookup"><span data-stu-id="54ccb-209">**szFaceName**</span></span>
</dt> <dd>

<span data-ttu-id="54ccb-210">Tipo: **char**</span><span class="sxs-lookup"><span data-stu-id="54ccb-210">Type: **CHAR**</span></span>

</dd> <dd>

<span data-ttu-id="54ccb-211">Nome tipografico del tipo di carattere.</span><span class="sxs-lookup"><span data-stu-id="54ccb-211">The typeface name of the font.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="54ccb-212">Commenti</span><span class="sxs-lookup"><span data-stu-id="54ccb-212">Remarks</span></span>

<span data-ttu-id="54ccb-213">Esiste una struttura **FONTDIRENTRY** per ogni tipo di carattere nel file res.</span><span class="sxs-lookup"><span data-stu-id="54ccb-213">There is one **FONTDIRENTRY** structure for every font in the .res file.</span></span> <span data-ttu-id="54ccb-214">Le applicazioni che generano file con estensione res con le risorse del tipo di carattere devono anche aggiungere al file una struttura **FONTDIRENTRY** per ogni tipo di carattere.</span><span class="sxs-lookup"><span data-stu-id="54ccb-214">Applications that generate .res files with font resources must also add to the file a **FONTDIRENTRY** structure for each font.</span></span>

<span data-ttu-id="54ccb-215">Le dichiarazioni dei tipi di carattere possono essere combinate con altre dichiarazioni di risorse in. File RC perché non è necessario che i tipi di carattere siano contigui nel file res.</span><span class="sxs-lookup"><span data-stu-id="54ccb-215">Font declarations can be mixed with other resource declarations in the .RC file because fonts do not need to be contiguous in the .res file.</span></span>

## <a name="requirements"></a><span data-ttu-id="54ccb-216">Requisiti</span><span class="sxs-lookup"><span data-stu-id="54ccb-216">Requirements</span></span>



| <span data-ttu-id="54ccb-217">Requisito</span><span class="sxs-lookup"><span data-stu-id="54ccb-217">Requirement</span></span> | <span data-ttu-id="54ccb-218">Valore</span><span class="sxs-lookup"><span data-stu-id="54ccb-218">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="54ccb-219">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="54ccb-219">Minimum supported client</span></span><br/> | <span data-ttu-id="54ccb-220">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="54ccb-220">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="54ccb-221">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="54ccb-221">Minimum supported server</span></span><br/> | <span data-ttu-id="54ccb-222">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="54ccb-222">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="54ccb-223">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="54ccb-223">See also</span></span>

<dl> <dt>

<span data-ttu-id="54ccb-224">**Riferimento**</span><span class="sxs-lookup"><span data-stu-id="54ccb-224">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="54ccb-225">**Diaffitto**</span><span class="sxs-lookup"><span data-stu-id="54ccb-225">**DIRENTRY**</span></span>](direntry.md)
</dt> <dt>

[<span data-ttu-id="54ccb-226">**FONTGROUPHDR**</span><span class="sxs-lookup"><span data-stu-id="54ccb-226">**FONTGROUPHDR**</span></span>](fontgrouphdr.md)
</dt> <dt>

<span data-ttu-id="54ccb-227">**Informazioni concettuali**</span><span class="sxs-lookup"><span data-stu-id="54ccb-227">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="54ccb-228">Risorse</span><span class="sxs-lookup"><span data-stu-id="54ccb-228">Resources</span></span>](resources.md)
</dt> <dt>

<span data-ttu-id="54ccb-229">**Altre risorse**</span><span class="sxs-lookup"><span data-stu-id="54ccb-229">**Other Resources**</span></span>
</dt> <dt>

[<span data-ttu-id="54ccb-230">**LOGFONT**</span><span class="sxs-lookup"><span data-stu-id="54ccb-230">**LOGFONT**</span></span>](/windows/win32/api/wingdi/ns-wingdi-logfonta)
</dt> </dl>

 

