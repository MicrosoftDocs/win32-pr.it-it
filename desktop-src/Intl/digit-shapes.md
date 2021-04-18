---
description: L'arabo e molti altri linguaggi hanno forme classiche per i numeri diversi dalle cifre occidentali convenzionali più spesso usate nei computer.
ms.assetid: 6b5267d8-b102-410c-bdc9-831555ca2f84
title: Forme cifre
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d6e6581b8b0eb87ae09b387c038c1ceba43125ac
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106317170"
---
# <a name="digit-shapes"></a><span data-ttu-id="6d665-103">Forme cifre</span><span class="sxs-lookup"><span data-stu-id="6d665-103">Digit Shapes</span></span>

<span data-ttu-id="6d665-104">L'arabo e molti altri linguaggi hanno forme classiche per i numeri diversi dalle cifre occidentali convenzionali più spesso usate nei computer.</span><span class="sxs-lookup"><span data-stu-id="6d665-104">Arabic and many other languages have classical shapes for numbers that are different from the conventional western digits most often used on computers.</span></span> <span data-ttu-id="6d665-105">Per evitare ambiguità nella denominazione di queste forme, in questo documento vengono utilizzati i nomi seguenti dello standard Unicode.</span><span class="sxs-lookup"><span data-stu-id="6d665-105">To avoid ambiguity in naming these shapes, this document uses the following names from the Unicode standard.</span></span>



| <span data-ttu-id="6d665-106">Nome Unicode delle cifre</span><span class="sxs-lookup"><span data-stu-id="6d665-106">Unicode name of the digits</span></span>                                     | <span data-ttu-id="6d665-107">Paese/area geografica in cui sono stati usati</span><span class="sxs-lookup"><span data-stu-id="6d665-107">Country/region where used</span></span>                                    |
|----------------------------------------------------------------|--------------------------------------------------------------|
| <span data-ttu-id="6d665-108">Cifre europee</span><span class="sxs-lookup"><span data-stu-id="6d665-108">European digits</span></span>                                                | <span data-ttu-id="6d665-109">Europa, Americhe e molti altri paesi/aree geografiche</span><span class="sxs-lookup"><span data-stu-id="6d665-109">Europe, the Americas, and many other countries/regions</span></span>       |
| <span data-ttu-id="6d665-110">Cifre Arabic-Indic</span><span class="sxs-lookup"><span data-stu-id="6d665-110">Arabic-Indic digits</span></span>                                            | <span data-ttu-id="6d665-111">Paesi/aree Arabi (sebbene molti usino cifre europee)</span><span class="sxs-lookup"><span data-stu-id="6d665-111">Arabic countries/regions (although many use European digits)</span></span> |
| <span data-ttu-id="6d665-112">Altre cifre nazionali: cifre indiane, cifre tailandesi e simili</span><span class="sxs-lookup"><span data-stu-id="6d665-112">Other national digits: Indic digits, Thai digits, and the like</span></span> | <span data-ttu-id="6d665-113">Diversi paesi/aree geografiche</span><span class="sxs-lookup"><span data-stu-id="6d665-113">Various countries/regions</span></span>                                    |



 

<span data-ttu-id="6d665-114">Unicode fornisce punti di codice separati per ogni forma di cifra.</span><span class="sxs-lookup"><span data-stu-id="6d665-114">Unicode provides separate code points for each digit shape.</span></span> <span data-ttu-id="6d665-115">Quindi, per accedere alle forme speciali di cifre della lingua, l'applicazione può usare i codici carattere Unicode pertinenti per le cifre precedenti, U + 0030 a U + 0039.</span><span class="sxs-lookup"><span data-stu-id="6d665-115">Thus, to access special language digit shapes, your application can use the relevant Unicode character codes for the digits above, U+0030 through U+0039.</span></span> <span data-ttu-id="6d665-116">Questi codici vengono sempre visualizzati con la forma appropriata, in base alla disponibilità dei tipi di carattere.</span><span class="sxs-lookup"><span data-stu-id="6d665-116">These codes are always displayed with the appropriate shape, subject to font availability.</span></span>

<span data-ttu-id="6d665-117">I codici carattere Unicode U + 0030 a U + 0039 rappresentano nominalmente i numeri europei da 0 a 9, ma la relativa forma digit può essere modificata.</span><span class="sxs-lookup"><span data-stu-id="6d665-117">The Unicode character codes U+0030 through U+0039 nominally represent the European digits 0 through 9, but their digit shape can be altered.</span></span> <span data-ttu-id="6d665-118">Le API di testo GDI e DirectWrite forniscono meccanismi che consentono alle applicazioni di controllare questo comportamento.</span><span class="sxs-lookup"><span data-stu-id="6d665-118">GDI and DirectWrite text APIs provide mechanisms for applications to control this behavior.</span></span> <span data-ttu-id="6d665-119">Vedere, ad esempio, [**ScriptApplyDigitSubstitution**](/windows/desktop/api/Usp10/nf-usp10-scriptapplydigitsubstitution) o [**IDWriteTextAnalysisSink:: SetNumberSubstitution**](/windows/win32/api/dwrite/nf-dwrite-idwritetextanalysissink-setnumbersubstitution). Il comportamento in alcuni controlli della shell e nei framework dell'interfaccia utente può rispondere alle impostazioni locali dell'utente per la sostituzione delle cifre. le impostazioni [locali \_ IDIGITSUBSTITUTION](locale-idigitsubstitution.md) LCType possono essere usate per ottenere le impostazioni di sostituzione cifre predefinite per le diverse impostazioni locali o le impostazioni desktop dell'utente corrente per la sostituzione delle cifre.</span><span class="sxs-lookup"><span data-stu-id="6d665-119">(See, for instance, [**ScriptApplyDigitSubstitution**](/windows/desktop/api/Usp10/nf-usp10-scriptapplydigitsubstitution) or [**IDWriteTextAnalysisSink::SetNumberSubstitution**](/windows/win32/api/dwrite/nf-dwrite-idwritetextanalysissink-setnumbersubstitution).) The behavior in some shell controls and user interface frameworks may respond to user locale settings for digit substitution; the [LOCALE\_IDIGITSUBSTITUTION](locale-idigitsubstitution.md) LCTYPE can be used to obtain default digit substitution settings for different locales or the current user's desktop settings for digit substitution.</span></span>

## <a name="native-digits"></a><span data-ttu-id="6d665-120">Cifre native</span><span class="sxs-lookup"><span data-stu-id="6d665-120">Native Digits</span></span>

<span data-ttu-id="6d665-121">Le cifre native sono le forme cifra scelte dall'utente nella finestra delle proprietà **numero** nella parte opzioni internazionali e della lingua del pannello di controllo.</span><span class="sxs-lookup"><span data-stu-id="6d665-121">Native digits are the digit shapes chosen by the user in the **Number** property sheet in the regional and language options portion of the Control Panel.</span></span> <span data-ttu-id="6d665-122">Per trovare la presentazione dei numeri preferita dall'utente, l'applicazione usa la funzione [**GetLocaleInfo**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoa) o [**GetLocaleInfoEx**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoex) con la costante [ \_ SNATIVEDIGITS delle impostazioni](locale-snative-constants.md) locali che rappresenta le informazioni sulle impostazioni locali.</span><span class="sxs-lookup"><span data-stu-id="6d665-122">To find the digit presentation preferred by the user, your application uses the [**GetLocaleInfo**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoa) or [**GetLocaleInfoEx**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoex) function with the [LOCALE\_SNATIVEDIGITS](locale-snative-constants.md) constant representing the locale information.</span></span>

> [!Note]  
> <span data-ttu-id="6d665-123">In genere, i codici cifra Unicode vengono generati nelle routine del sistema operativo in fase di esecuzione.</span><span class="sxs-lookup"><span data-stu-id="6d665-123">Typically, Unicode digit codes are generated in runtime operating system routines.</span></span> <span data-ttu-id="6d665-124">Pertanto, è necessario aggiornare i sistemi operativi di runtime comuni affinché l'applicazione esamini le [impostazioni locali \_ SNATIVEDIGITS](locale-snative-constants.md) in modo appropriato.</span><span class="sxs-lookup"><span data-stu-id="6d665-124">Therefore, common runtime operating systems must be upgraded for the application to inspect [LOCALE\_SNATIVEDIGITS](locale-snative-constants.md) appropriately.</span></span>

 

## <a name="digit-substitution"></a><span data-ttu-id="6d665-125">Sostituzione cifre</span><span class="sxs-lookup"><span data-stu-id="6d665-125">Digit Substitution</span></span>

<span data-ttu-id="6d665-126">L'applicazione può usare la sostituzione dei numeri per indicare al sistema operativo come stampare le cifre U + 0030 fino a U + 0039.</span><span class="sxs-lookup"><span data-stu-id="6d665-126">The application can use digit substitution to tell the operating system how to print digits U+0030 through U+0039.</span></span> <span data-ttu-id="6d665-127">La costante [ \_ IDIGITSUBSTITUTION delle impostazioni locali](locale-idigitsubstitution.md) controlla questa operazione.</span><span class="sxs-lookup"><span data-stu-id="6d665-127">The [LOCALE\_IDIGITSUBSTITUTION](locale-idigitsubstitution.md) constant controls this operation.</span></span>

## <a name="digit-shaping-for-a-single-function"></a><span data-ttu-id="6d665-128">Shaping dei numeri per una singola funzione</span><span class="sxs-lookup"><span data-stu-id="6d665-128">Digit Shaping for a Single Function</span></span>

<span data-ttu-id="6d665-129">Le funzioni [ExtTextOut](/windows/win32/api/wingdi/nf-wingdi-exttextouta), [GetCharacterPlacement](/windows/win32/api/wingdi/nf-wingdi-getcharacterplacementa)e [GCP \_ results](/windows/win32/api/wingdi/ns-wingdi-gcp_resultsa) hanno flag che regolano la sostituzione dei codici Unicode U + 0030 fino a u + 0039 per la durata della chiamata di funzione.</span><span class="sxs-lookup"><span data-stu-id="6d665-129">The [ExtTextOut](/windows/win32/api/wingdi/nf-wingdi-exttextouta), [GetCharacterPlacement](/windows/win32/api/wingdi/nf-wingdi-getcharacterplacementa), and [GCP\_RESULTS](/windows/win32/api/wingdi/ns-wingdi-gcp_resultsa) functions have flags that govern the substitution of Unicode codes U+0030 through U+0039 for the duration of the function call.</span></span> <span data-ttu-id="6d665-130">Questi flag sostituiscono le impostazioni internazionali nel pannello di controllo, ma non reimpostano le impostazioni.</span><span class="sxs-lookup"><span data-stu-id="6d665-130">These flags override regional settings in the Control Panel, but do not reset the settings.</span></span> <span data-ttu-id="6d665-131">Inoltre, non eseguono l'override dei codici Unicode e dei relativi nodi.</span><span class="sxs-lookup"><span data-stu-id="6d665-131">Also, they do not override the Unicode codes NADS and NODS.</span></span> <span data-ttu-id="6d665-132">Sono disponibili i flag seguenti.</span><span class="sxs-lookup"><span data-stu-id="6d665-132">The following flags are available.</span></span>



| <span data-ttu-id="6d665-133">Flags</span><span class="sxs-lookup"><span data-stu-id="6d665-133">Flags</span></span>                 | <span data-ttu-id="6d665-134">Cifre utilizzate</span><span class="sxs-lookup"><span data-stu-id="6d665-134">Digits used</span></span>                      | <span data-ttu-id="6d665-135">Campo di utilizzo</span><span class="sxs-lookup"><span data-stu-id="6d665-135">Used in</span></span>                   |
|-----------------------|----------------------------------|---------------------------|
| <span data-ttu-id="6d665-136">\_NUMERICSLATIN Eto</span><span class="sxs-lookup"><span data-stu-id="6d665-136">ETO\_NUMERICSLATIN</span></span>    | <span data-ttu-id="6d665-137">Cifre europee</span><span class="sxs-lookup"><span data-stu-id="6d665-137">European digits</span></span>                  | <span data-ttu-id="6d665-138">**ExtTextOut**</span><span class="sxs-lookup"><span data-stu-id="6d665-138">**ExtTextOut**</span></span>            |
| <span data-ttu-id="6d665-139">\_NUMERICSLOCAL Eto</span><span class="sxs-lookup"><span data-stu-id="6d665-139">ETO\_NUMERICSLOCAL</span></span>    | <span data-ttu-id="6d665-140">Cifre appropriate per le impostazioni locali</span><span class="sxs-lookup"><span data-stu-id="6d665-140">Digits appropriate to the locale</span></span> | <span data-ttu-id="6d665-141">**ExtTextOut**</span><span class="sxs-lookup"><span data-stu-id="6d665-141">**ExtTextOut**</span></span>            |
| <span data-ttu-id="6d665-142">\_NUMERICSLATIN GCP</span><span class="sxs-lookup"><span data-stu-id="6d665-142">GCP\_NUMERICSLATIN</span></span>    | <span data-ttu-id="6d665-143">Cifre europee</span><span class="sxs-lookup"><span data-stu-id="6d665-143">European digits</span></span>                  | <span data-ttu-id="6d665-144">**GetCharacterPlacement**</span><span class="sxs-lookup"><span data-stu-id="6d665-144">**GetCharacterPlacement**</span></span> |
| <span data-ttu-id="6d665-145">\_NUMERICSLOCAL GCP</span><span class="sxs-lookup"><span data-stu-id="6d665-145">GCP\_NUMERICSLOCAL</span></span>    | <span data-ttu-id="6d665-146">Cifre appropriate per le impostazioni locali</span><span class="sxs-lookup"><span data-stu-id="6d665-146">Digits appropriate to the locale</span></span> | <span data-ttu-id="6d665-147">**GetCharacterPlacement**</span><span class="sxs-lookup"><span data-stu-id="6d665-147">**GetCharacterPlacement**</span></span> |
| <span data-ttu-id="6d665-148">\_LATINNUMBER GCPCLASS</span><span class="sxs-lookup"><span data-stu-id="6d665-148">GCPCLASS\_LATINNUMBER</span></span> | <span data-ttu-id="6d665-149">Cifre europee</span><span class="sxs-lookup"><span data-stu-id="6d665-149">European digits</span></span>                  | <span data-ttu-id="6d665-150">**risultati di GCP \_**</span><span class="sxs-lookup"><span data-stu-id="6d665-150">**GCP\_RESULTS**</span></span>          |
| <span data-ttu-id="6d665-151">\_LOCALNUMBER GCPCLASS</span><span class="sxs-lookup"><span data-stu-id="6d665-151">GCPCLASS\_LOCALNUMBER</span></span> | <span data-ttu-id="6d665-152">Cifre appropriate per le impostazioni locali</span><span class="sxs-lookup"><span data-stu-id="6d665-152">Digits appropriate to the locale</span></span> | <span data-ttu-id="6d665-153">**risultati di GCP \_**</span><span class="sxs-lookup"><span data-stu-id="6d665-153">**GCP\_RESULTS**</span></span>          |



 

## <a name="related-topics"></a><span data-ttu-id="6d665-154">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="6d665-154">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6d665-155">Informazioni sul supporto linguistico nazionale</span><span class="sxs-lookup"><span data-stu-id="6d665-155">About National Language Support</span></span>](about-national-language-support.md)
</dt> <dt>

[<span data-ttu-id="6d665-156">**GetLocaleInfo**</span><span class="sxs-lookup"><span data-stu-id="6d665-156">**GetLocaleInfo**</span></span>](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoa)
</dt> <dt>

[<span data-ttu-id="6d665-157">**GetLocaleInfoEx**</span><span class="sxs-lookup"><span data-stu-id="6d665-157">**GetLocaleInfoEx**</span></span>](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoex)
</dt> </dl>

 

 
