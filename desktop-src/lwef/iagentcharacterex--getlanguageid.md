---
title: IAgentCharacterEx GetLanguageID
description: IAgentCharacterEx GetLanguageID
ms.assetid: 4e4e5342-edf9-480b-a9c3-e2626fd89e76
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9679538f93d779acc6272dccada824585c4449f5
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104045071"
---
# <a name="iagentcharacterexgetlanguageid"></a><span data-ttu-id="5bb2a-103">IAgentCharacterEx::GetLanguageID</span><span class="sxs-lookup"><span data-stu-id="5bb2a-103">IAgentCharacterEx::GetLanguageID</span></span>

<span data-ttu-id="5bb2a-104">\[Microsoft Agent è stato deprecato a partire da Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="5bb2a-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT GetLanguageID(
   long * plangID  // address of language ID setting
);
```

<span data-ttu-id="5bb2a-105">Recupera l'ID lingua impostato per il carattere.</span><span class="sxs-lookup"><span data-stu-id="5bb2a-105">Retrieves the language ID set for the character.</span></span>

-   <span data-ttu-id="5bb2a-106">Restituisce \_ OK per indicare che l'operazione è stata completata.</span><span class="sxs-lookup"><span data-stu-id="5bb2a-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="5bb2a-107"><span id="plangID"></span><span id="plangid"></span><span id="PLANGID"></span>*plangID*</span><span class="sxs-lookup"><span data-stu-id="5bb2a-107"><span id="plangID"></span><span id="plangid"></span><span id="PLANGID"></span>*plangID*</span></span>
</dt> <dd>

<span data-ttu-id="5bb2a-108">Indirizzo di una variabile che riceve l'impostazione dell'ID lingua per il carattere.</span><span class="sxs-lookup"><span data-stu-id="5bb2a-108">Address of a variable that receives the language ID setting for the character.</span></span>

</dd> </dl>

<span data-ttu-id="5bb2a-109">Valore long integer che specifica l'ID lingua per il carattere.</span><span class="sxs-lookup"><span data-stu-id="5bb2a-109">A Long integer specifying the language ID for the character.</span></span> <span data-ttu-id="5bb2a-110">L'ID lingua (LANGID) per un carattere è un valore a 16 bit definito da Windows, costituito da un ID di lingua primario e da un ID di lingua secondaria.</span><span class="sxs-lookup"><span data-stu-id="5bb2a-110">The language ID (LANGID) for a character is a 16-bit value defined by Windows, consisting of a primary language ID and a secondary language ID.</span></span> <span data-ttu-id="5bb2a-111">Gli esempi seguenti sono valori per alcune lingue.</span><span class="sxs-lookup"><span data-stu-id="5bb2a-111">The following examples are values for some languages.</span></span> <span data-ttu-id="5bb2a-112">Per determinare i valori in altre lingue, vedere la documentazione di Platform SDK.</span><span class="sxs-lookup"><span data-stu-id="5bb2a-112">To determine the values other languages, see the Platform SDK documentation.</span></span>



|                       |        |                       |        |
|-----------------------|--------|-----------------------|--------|
| <span data-ttu-id="5bb2a-113">Arabo (Arabia Saudita)</span><span class="sxs-lookup"><span data-stu-id="5bb2a-113">Arabic (Saudi)</span></span>        | <span data-ttu-id="5bb2a-114">0x0401</span><span class="sxs-lookup"><span data-stu-id="5bb2a-114">0x0401</span></span> | <span data-ttu-id="5bb2a-115">Italiano</span><span class="sxs-lookup"><span data-stu-id="5bb2a-115">Italian</span></span>               | <span data-ttu-id="5bb2a-116">0x0410</span><span class="sxs-lookup"><span data-stu-id="5bb2a-116">0x0410</span></span> |
| <span data-ttu-id="5bb2a-117">Basco</span><span class="sxs-lookup"><span data-stu-id="5bb2a-117">Basque</span></span>                | <span data-ttu-id="5bb2a-118">0x042d</span><span class="sxs-lookup"><span data-stu-id="5bb2a-118">0x042d</span></span> | <span data-ttu-id="5bb2a-119">Giapponese</span><span class="sxs-lookup"><span data-stu-id="5bb2a-119">Japanese</span></span>              | <span data-ttu-id="5bb2a-120">0x0411</span><span class="sxs-lookup"><span data-stu-id="5bb2a-120">0x0411</span></span> |
| <span data-ttu-id="5bb2a-121">Cinese (semplificato)</span><span class="sxs-lookup"><span data-stu-id="5bb2a-121">Chinese (Simplified)</span></span>  | <span data-ttu-id="5bb2a-122">0x0804</span><span class="sxs-lookup"><span data-stu-id="5bb2a-122">0x0804</span></span> | <span data-ttu-id="5bb2a-123">Coreano</span><span class="sxs-lookup"><span data-stu-id="5bb2a-123">Korean</span></span>                | <span data-ttu-id="5bb2a-124">0x0412</span><span class="sxs-lookup"><span data-stu-id="5bb2a-124">0x0412</span></span> |
| <span data-ttu-id="5bb2a-125">Cinese (tradizionale)</span><span class="sxs-lookup"><span data-stu-id="5bb2a-125">Chinese (Traditional)</span></span> | <span data-ttu-id="5bb2a-126">0x0404</span><span class="sxs-lookup"><span data-stu-id="5bb2a-126">0x0404</span></span> | <span data-ttu-id="5bb2a-127">Norvegese</span><span class="sxs-lookup"><span data-stu-id="5bb2a-127">Norwegian</span></span>             | <span data-ttu-id="5bb2a-128">0x0414</span><span class="sxs-lookup"><span data-stu-id="5bb2a-128">0x0414</span></span> |
| <span data-ttu-id="5bb2a-129">Croato</span><span class="sxs-lookup"><span data-stu-id="5bb2a-129">Croatian</span></span>              | <span data-ttu-id="5bb2a-130">0x041A</span><span class="sxs-lookup"><span data-stu-id="5bb2a-130">0x041A</span></span> | <span data-ttu-id="5bb2a-131">Polacco</span><span class="sxs-lookup"><span data-stu-id="5bb2a-131">Polish</span></span>                | <span data-ttu-id="5bb2a-132">0x0415</span><span class="sxs-lookup"><span data-stu-id="5bb2a-132">0x0415</span></span> |
| <span data-ttu-id="5bb2a-133">Ceco</span><span class="sxs-lookup"><span data-stu-id="5bb2a-133">Czech</span></span>                 | <span data-ttu-id="5bb2a-134">0x0405</span><span class="sxs-lookup"><span data-stu-id="5bb2a-134">0x0405</span></span> | <span data-ttu-id="5bb2a-135">Portoghese (Portogallo)</span><span class="sxs-lookup"><span data-stu-id="5bb2a-135">Portuguese (Portugal)</span></span> | <span data-ttu-id="5bb2a-136">0x0816</span><span class="sxs-lookup"><span data-stu-id="5bb2a-136">0x0816</span></span> |
| <span data-ttu-id="5bb2a-137">Danese</span><span class="sxs-lookup"><span data-stu-id="5bb2a-137">Danish</span></span>                | <span data-ttu-id="5bb2a-138">0x0406</span><span class="sxs-lookup"><span data-stu-id="5bb2a-138">0x0406</span></span> | <span data-ttu-id="5bb2a-139">Portoghese (Brasile)</span><span class="sxs-lookup"><span data-stu-id="5bb2a-139">Portuguese (Brazil)</span></span>   | <span data-ttu-id="5bb2a-140">0x0416</span><span class="sxs-lookup"><span data-stu-id="5bb2a-140">0x0416</span></span> |
| <span data-ttu-id="5bb2a-141">Olandese</span><span class="sxs-lookup"><span data-stu-id="5bb2a-141">Dutch</span></span>                 | <span data-ttu-id="5bb2a-142">0x0413</span><span class="sxs-lookup"><span data-stu-id="5bb2a-142">0x0413</span></span> | <span data-ttu-id="5bb2a-143">Romeno</span><span class="sxs-lookup"><span data-stu-id="5bb2a-143">Romanian</span></span>              | <span data-ttu-id="5bb2a-144">0x0418</span><span class="sxs-lookup"><span data-stu-id="5bb2a-144">0x0418</span></span> |
| <span data-ttu-id="5bb2a-145">Inglese (Regno Unito)</span><span class="sxs-lookup"><span data-stu-id="5bb2a-145">English (British)</span></span>     | <span data-ttu-id="5bb2a-146">0x0809</span><span class="sxs-lookup"><span data-stu-id="5bb2a-146">0x0809</span></span> | <span data-ttu-id="5bb2a-147">Russo</span><span class="sxs-lookup"><span data-stu-id="5bb2a-147">Russian</span></span>               | <span data-ttu-id="5bb2a-148">0x0419</span><span class="sxs-lookup"><span data-stu-id="5bb2a-148">0x0419</span></span> |
| <span data-ttu-id="5bb2a-149">Inglese (Stati Uniti)</span><span class="sxs-lookup"><span data-stu-id="5bb2a-149">English (US)</span></span>          | <span data-ttu-id="5bb2a-150">0x0409</span><span class="sxs-lookup"><span data-stu-id="5bb2a-150">0x0409</span></span> | <span data-ttu-id="5bb2a-151">Slovacco</span><span class="sxs-lookup"><span data-stu-id="5bb2a-151">Slovakian</span></span>             | <span data-ttu-id="5bb2a-152">0x041B</span><span class="sxs-lookup"><span data-stu-id="5bb2a-152">0x041B</span></span> |
| <span data-ttu-id="5bb2a-153">Finlandese</span><span class="sxs-lookup"><span data-stu-id="5bb2a-153">Finnish</span></span>               | <span data-ttu-id="5bb2a-154">0x040B</span><span class="sxs-lookup"><span data-stu-id="5bb2a-154">0x040B</span></span> | <span data-ttu-id="5bb2a-155">Sloveno</span><span class="sxs-lookup"><span data-stu-id="5bb2a-155">Slovenian</span></span>             | <span data-ttu-id="5bb2a-156">0x0424</span><span class="sxs-lookup"><span data-stu-id="5bb2a-156">0x0424</span></span> |
| <span data-ttu-id="5bb2a-157">Francese</span><span class="sxs-lookup"><span data-stu-id="5bb2a-157">French</span></span>                | <span data-ttu-id="5bb2a-158">0x040C</span><span class="sxs-lookup"><span data-stu-id="5bb2a-158">0x040C</span></span> | <span data-ttu-id="5bb2a-159">Spagnolo</span><span class="sxs-lookup"><span data-stu-id="5bb2a-159">Spanish</span></span>               | <span data-ttu-id="5bb2a-160">0x0C0A</span><span class="sxs-lookup"><span data-stu-id="5bb2a-160">0x0C0A</span></span> |
| <span data-ttu-id="5bb2a-161">Tedesco</span><span class="sxs-lookup"><span data-stu-id="5bb2a-161">German</span></span>                | <span data-ttu-id="5bb2a-162">0x0407</span><span class="sxs-lookup"><span data-stu-id="5bb2a-162">0x0407</span></span> | <span data-ttu-id="5bb2a-163">Svedese</span><span class="sxs-lookup"><span data-stu-id="5bb2a-163">Swedish</span></span>               | <span data-ttu-id="5bb2a-164">0x041D</span><span class="sxs-lookup"><span data-stu-id="5bb2a-164">0x041D</span></span> |
| <span data-ttu-id="5bb2a-165">Greco</span><span class="sxs-lookup"><span data-stu-id="5bb2a-165">Greek</span></span>                 | <span data-ttu-id="5bb2a-166">0x0408</span><span class="sxs-lookup"><span data-stu-id="5bb2a-166">0x0408</span></span> | <span data-ttu-id="5bb2a-167">Thai</span><span class="sxs-lookup"><span data-stu-id="5bb2a-167">Thai</span></span>                  | <span data-ttu-id="5bb2a-168">0x041E</span><span class="sxs-lookup"><span data-stu-id="5bb2a-168">0x041E</span></span> |
| <span data-ttu-id="5bb2a-169">Ebraico</span><span class="sxs-lookup"><span data-stu-id="5bb2a-169">Hebrew</span></span>                | <span data-ttu-id="5bb2a-170">0x040D</span><span class="sxs-lookup"><span data-stu-id="5bb2a-170">0x040D</span></span> | <span data-ttu-id="5bb2a-171">Turco</span><span class="sxs-lookup"><span data-stu-id="5bb2a-171">Turkish</span></span>               | <span data-ttu-id="5bb2a-172">0x041F</span><span class="sxs-lookup"><span data-stu-id="5bb2a-172">0x041F</span></span> |
| <span data-ttu-id="5bb2a-173">Ungherese</span><span class="sxs-lookup"><span data-stu-id="5bb2a-173">Hungarian</span></span>             | <span data-ttu-id="5bb2a-174">0x040E</span><span class="sxs-lookup"><span data-stu-id="5bb2a-174">0x040E</span></span> |                       |        |



 

<span data-ttu-id="5bb2a-175">Se non si imposta questo ID lingua per il carattere, l'ID lingua del carattere sarà l'ID della lingua di sistema corrente.</span><span class="sxs-lookup"><span data-stu-id="5bb2a-175">If you do not set this language ID for the character, the character's language ID will be the current system language ID.</span></span>

<span data-ttu-id="5bb2a-176">Questa impostazione determina anche la lingua per l'output TTS, il testo del fumetto di parole, i comandi nel menu a comparsa del carattere e il motore di riconoscimento vocale.</span><span class="sxs-lookup"><span data-stu-id="5bb2a-176">This setting also determines the language for TTS output, word balloon text, the commands in the character's pop-up menu, and speech recognition engine.</span></span> <span data-ttu-id="5bb2a-177">Per determinare se è disponibile un motore di riconoscimento vocale compatibile per la lingua del carattere, usare [**IAgentCharacterEx:: GetSRModeID**](iagentcharacterex--getsrmodeid.md) o [**IAgentCharacterEx:: GetTTSModeID**](iagentcharacterex--getttsmodeid.md).</span><span class="sxs-lookup"><span data-stu-id="5bb2a-177">To determine if there is a compatible speech recognition engine available for the character's language, use [**IAgentCharacterEx::GetSRModeID**](iagentcharacterex--getsrmodeid.md) or [**IAgentCharacterEx::GetTTSModeID**](iagentcharacterex--getttsmodeid.md).</span></span>

<span data-ttu-id="5bb2a-178">Questa proprietà si applica solo all'utilizzo del carattere da parte dell'applicazione client. l'impostazione non influisce sugli altri client del carattere o di altri caratteri dell'applicazione client.</span><span class="sxs-lookup"><span data-stu-id="5bb2a-178">This property applies only to your client application's use of the character; the setting does not affect other clients of the character or other characters of your client application.</span></span>

> [!Note]  
> <span data-ttu-id="5bb2a-179">Se l'ID lingua è impostato su una lingua che supporta il testo bidirezionale, ad esempio l'arabo o l'ebraico, ma nel sistema in cui è in esecuzione l'applicazione non è installato il supporto bidirezionale, il testo verrà visualizzato nella parola fumetto nell'ordine logico anziché in quello visualizzato.</span><span class="sxs-lookup"><span data-stu-id="5bb2a-179">If the language ID is set to a language that supports bidirectional text (such as Arabic or Hebrew), but the system running your application does not have bidirectional support installed, text will appear in the word balloon in logical rather than display order.</span></span>

 

## <a name="see-also"></a><span data-ttu-id="5bb2a-180">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="5bb2a-180">See Also</span></span>

<span data-ttu-id="5bb2a-181">[**IAgentCharacterEx: SetLanguageID**](iagentcharacterex--setlanguageid.md), [**IAgentCharacterEx:: GetSRModeID**](iagentcharacterex--getsrmodeid.md), [**IAgentCharacterEx:: GetTTSModeID**](iagentcharacterex--getttsmodeid.md)</span><span class="sxs-lookup"><span data-stu-id="5bb2a-181">[**IAgentCharacterEx:SetLanguageID**](iagentcharacterex--setlanguageid.md), [**IAgentCharacterEx::GetSRModeID**](iagentcharacterex--getsrmodeid.md), [**IAgentCharacterEx::GetTTSModeID**](iagentcharacterex--getttsmodeid.md)</span></span>


 

 




