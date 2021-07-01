---
title: IAgentCharacterEx GetLanguageID
description: IAgentCharacterEx GetLanguageID
ms.assetid: 4e4e5342-edf9-480b-a9c3-e2626fd89e76
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3d847bf392709b2433b045a357a703173e2de454
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/30/2021
ms.locfileid: "113120647"
---
# <a name="iagentcharacterexgetlanguageid"></a><span data-ttu-id="ae24d-103">IAgentCharacterEx::GetLanguageID</span><span class="sxs-lookup"><span data-stu-id="ae24d-103">IAgentCharacterEx::GetLanguageID</span></span>

<span data-ttu-id="ae24d-104">\[Microsoft Agent è deprecato a livello di Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="ae24d-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT GetLanguageID(
   long * plangID  // address of language ID setting
);
```

<span data-ttu-id="ae24d-105">Recupera l'ID lingua impostato per il carattere.</span><span class="sxs-lookup"><span data-stu-id="ae24d-105">Retrieves the language ID set for the character.</span></span>

-   <span data-ttu-id="ae24d-106">Restituisce S \_ OK per indicare che l'operazione è riuscita.</span><span class="sxs-lookup"><span data-stu-id="ae24d-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="ae24d-107"><span id="plangID"></span><span id="plangid"></span><span id="PLANGID"></span>*plangID*</span><span class="sxs-lookup"><span data-stu-id="ae24d-107"><span id="plangID"></span><span id="plangid"></span><span id="PLANGID"></span>*plangID*</span></span>
</dt> <dd>

<span data-ttu-id="ae24d-108">Indirizzo di una variabile che riceve l'impostazione dell'ID lingua per il carattere.</span><span class="sxs-lookup"><span data-stu-id="ae24d-108">Address of a variable that receives the language ID setting for the character.</span></span>

</dd> </dl>

<span data-ttu-id="ae24d-109">Valore Long integer che specifica l'ID lingua per il carattere.</span><span class="sxs-lookup"><span data-stu-id="ae24d-109">A Long integer specifying the language ID for the character.</span></span> <span data-ttu-id="ae24d-110">L'ID lingua (LANGID) per un carattere è un valore a 16 bit definito da Windows, costituito da un ID lingua primaria e un ID lingua secondaria.</span><span class="sxs-lookup"><span data-stu-id="ae24d-110">The language ID (LANGID) for a character is a 16-bit value defined by Windows, consisting of a primary language ID and a secondary language ID.</span></span> <span data-ttu-id="ae24d-111">Gli esempi seguenti sono valori per alcuni linguaggi.</span><span class="sxs-lookup"><span data-stu-id="ae24d-111">The following examples are values for some languages.</span></span> <span data-ttu-id="ae24d-112">Per determinare i valori di altri linguaggi, vedere la documentazione di Platform SDK.</span><span class="sxs-lookup"><span data-stu-id="ae24d-112">To determine the values other languages, see the Platform SDK documentation.</span></span>



| <span data-ttu-id="ae24d-113">Lingua</span><span class="sxs-lookup"><span data-stu-id="ae24d-113">Language</span></span>              | <span data-ttu-id="ae24d-114">ID</span><span class="sxs-lookup"><span data-stu-id="ae24d-114">ID</span></span>     | <span data-ttu-id="ae24d-115">Lingua</span><span class="sxs-lookup"><span data-stu-id="ae24d-115">Language</span></span>              | <span data-ttu-id="ae24d-116">ID</span><span class="sxs-lookup"><span data-stu-id="ae24d-116">ID</span></span>     |
|-----------------------|--------|-----------------------|--------|
| <span data-ttu-id="ae24d-117">Arabo (Saudita)</span><span class="sxs-lookup"><span data-stu-id="ae24d-117">Arabic (Saudi)</span></span>        | <span data-ttu-id="ae24d-118">0x0401</span><span class="sxs-lookup"><span data-stu-id="ae24d-118">0x0401</span></span> | <span data-ttu-id="ae24d-119">Italiano</span><span class="sxs-lookup"><span data-stu-id="ae24d-119">Italian</span></span>               | <span data-ttu-id="ae24d-120">0x0410</span><span class="sxs-lookup"><span data-stu-id="ae24d-120">0x0410</span></span> |
| <span data-ttu-id="ae24d-121">Basco</span><span class="sxs-lookup"><span data-stu-id="ae24d-121">Basque</span></span>                | <span data-ttu-id="ae24d-122">0x042d</span><span class="sxs-lookup"><span data-stu-id="ae24d-122">0x042d</span></span> | <span data-ttu-id="ae24d-123">Giapponese</span><span class="sxs-lookup"><span data-stu-id="ae24d-123">Japanese</span></span>              | <span data-ttu-id="ae24d-124">0x0411</span><span class="sxs-lookup"><span data-stu-id="ae24d-124">0x0411</span></span> |
| <span data-ttu-id="ae24d-125">Cinese (semplificato)</span><span class="sxs-lookup"><span data-stu-id="ae24d-125">Chinese (Simplified)</span></span>  | <span data-ttu-id="ae24d-126">0x0804</span><span class="sxs-lookup"><span data-stu-id="ae24d-126">0x0804</span></span> | <span data-ttu-id="ae24d-127">Coreano</span><span class="sxs-lookup"><span data-stu-id="ae24d-127">Korean</span></span>                | <span data-ttu-id="ae24d-128">0x0412</span><span class="sxs-lookup"><span data-stu-id="ae24d-128">0x0412</span></span> |
| <span data-ttu-id="ae24d-129">Cinese (tradizionale)</span><span class="sxs-lookup"><span data-stu-id="ae24d-129">Chinese (Traditional)</span></span> | <span data-ttu-id="ae24d-130">0x0404</span><span class="sxs-lookup"><span data-stu-id="ae24d-130">0x0404</span></span> | <span data-ttu-id="ae24d-131">Norvegese</span><span class="sxs-lookup"><span data-stu-id="ae24d-131">Norwegian</span></span>             | <span data-ttu-id="ae24d-132">0x0414</span><span class="sxs-lookup"><span data-stu-id="ae24d-132">0x0414</span></span> |
| <span data-ttu-id="ae24d-133">Croato</span><span class="sxs-lookup"><span data-stu-id="ae24d-133">Croatian</span></span>              | <span data-ttu-id="ae24d-134">0x041A</span><span class="sxs-lookup"><span data-stu-id="ae24d-134">0x041A</span></span> | <span data-ttu-id="ae24d-135">Polacco</span><span class="sxs-lookup"><span data-stu-id="ae24d-135">Polish</span></span>                | <span data-ttu-id="ae24d-136">0x0415</span><span class="sxs-lookup"><span data-stu-id="ae24d-136">0x0415</span></span> |
| <span data-ttu-id="ae24d-137">Ceco</span><span class="sxs-lookup"><span data-stu-id="ae24d-137">Czech</span></span>                 | <span data-ttu-id="ae24d-138">0x0405</span><span class="sxs-lookup"><span data-stu-id="ae24d-138">0x0405</span></span> | <span data-ttu-id="ae24d-139">Portoghese (Portogallo)</span><span class="sxs-lookup"><span data-stu-id="ae24d-139">Portuguese (Portugal)</span></span> | <span data-ttu-id="ae24d-140">0x0816</span><span class="sxs-lookup"><span data-stu-id="ae24d-140">0x0816</span></span> |
| <span data-ttu-id="ae24d-141">Danese</span><span class="sxs-lookup"><span data-stu-id="ae24d-141">Danish</span></span>                | <span data-ttu-id="ae24d-142">0x0406</span><span class="sxs-lookup"><span data-stu-id="ae24d-142">0x0406</span></span> | <span data-ttu-id="ae24d-143">Portoghese (Brasile)</span><span class="sxs-lookup"><span data-stu-id="ae24d-143">Portuguese (Brazil)</span></span>   | <span data-ttu-id="ae24d-144">0x0416</span><span class="sxs-lookup"><span data-stu-id="ae24d-144">0x0416</span></span> |
| <span data-ttu-id="ae24d-145">Olandese</span><span class="sxs-lookup"><span data-stu-id="ae24d-145">Dutch</span></span>                 | <span data-ttu-id="ae24d-146">0x0413</span><span class="sxs-lookup"><span data-stu-id="ae24d-146">0x0413</span></span> | <span data-ttu-id="ae24d-147">Romeno</span><span class="sxs-lookup"><span data-stu-id="ae24d-147">Romanian</span></span>              | <span data-ttu-id="ae24d-148">0x0418</span><span class="sxs-lookup"><span data-stu-id="ae24d-148">0x0418</span></span> |
| <span data-ttu-id="ae24d-149">Inglese (Regno Unito)</span><span class="sxs-lookup"><span data-stu-id="ae24d-149">English (British)</span></span>     | <span data-ttu-id="ae24d-150">0x0809</span><span class="sxs-lookup"><span data-stu-id="ae24d-150">0x0809</span></span> | <span data-ttu-id="ae24d-151">Russo</span><span class="sxs-lookup"><span data-stu-id="ae24d-151">Russian</span></span>               | <span data-ttu-id="ae24d-152">0x0419</span><span class="sxs-lookup"><span data-stu-id="ae24d-152">0x0419</span></span> |
| <span data-ttu-id="ae24d-153">Inglese (Stati Uniti)</span><span class="sxs-lookup"><span data-stu-id="ae24d-153">English (US)</span></span>          | <span data-ttu-id="ae24d-154">0x0409</span><span class="sxs-lookup"><span data-stu-id="ae24d-154">0x0409</span></span> | <span data-ttu-id="ae24d-155">Slovacco</span><span class="sxs-lookup"><span data-stu-id="ae24d-155">Slovakian</span></span>             | <span data-ttu-id="ae24d-156">0x041B</span><span class="sxs-lookup"><span data-stu-id="ae24d-156">0x041B</span></span> |
| <span data-ttu-id="ae24d-157">Finlandese</span><span class="sxs-lookup"><span data-stu-id="ae24d-157">Finnish</span></span>               | <span data-ttu-id="ae24d-158">0x040B</span><span class="sxs-lookup"><span data-stu-id="ae24d-158">0x040B</span></span> | <span data-ttu-id="ae24d-159">Sloveno</span><span class="sxs-lookup"><span data-stu-id="ae24d-159">Slovenian</span></span>             | <span data-ttu-id="ae24d-160">0x0424</span><span class="sxs-lookup"><span data-stu-id="ae24d-160">0x0424</span></span> |
| <span data-ttu-id="ae24d-161">Francese</span><span class="sxs-lookup"><span data-stu-id="ae24d-161">French</span></span>                | <span data-ttu-id="ae24d-162">0x040C</span><span class="sxs-lookup"><span data-stu-id="ae24d-162">0x040C</span></span> | <span data-ttu-id="ae24d-163">Spagnolo</span><span class="sxs-lookup"><span data-stu-id="ae24d-163">Spanish</span></span>               | <span data-ttu-id="ae24d-164">0x0C0A</span><span class="sxs-lookup"><span data-stu-id="ae24d-164">0x0C0A</span></span> |
| <span data-ttu-id="ae24d-165">Tedesco</span><span class="sxs-lookup"><span data-stu-id="ae24d-165">German</span></span>                | <span data-ttu-id="ae24d-166">0x0407</span><span class="sxs-lookup"><span data-stu-id="ae24d-166">0x0407</span></span> | <span data-ttu-id="ae24d-167">Svedese</span><span class="sxs-lookup"><span data-stu-id="ae24d-167">Swedish</span></span>               | <span data-ttu-id="ae24d-168">0x041D</span><span class="sxs-lookup"><span data-stu-id="ae24d-168">0x041D</span></span> |
| <span data-ttu-id="ae24d-169">Greco</span><span class="sxs-lookup"><span data-stu-id="ae24d-169">Greek</span></span>                 | <span data-ttu-id="ae24d-170">0x0408</span><span class="sxs-lookup"><span data-stu-id="ae24d-170">0x0408</span></span> | <span data-ttu-id="ae24d-171">Thai</span><span class="sxs-lookup"><span data-stu-id="ae24d-171">Thai</span></span>                  | <span data-ttu-id="ae24d-172">0x041E</span><span class="sxs-lookup"><span data-stu-id="ae24d-172">0x041E</span></span> |
| <span data-ttu-id="ae24d-173">Ebraico</span><span class="sxs-lookup"><span data-stu-id="ae24d-173">Hebrew</span></span>                | <span data-ttu-id="ae24d-174">0x040D</span><span class="sxs-lookup"><span data-stu-id="ae24d-174">0x040D</span></span> | <span data-ttu-id="ae24d-175">Turco</span><span class="sxs-lookup"><span data-stu-id="ae24d-175">Turkish</span></span>               | <span data-ttu-id="ae24d-176">0x041F</span><span class="sxs-lookup"><span data-stu-id="ae24d-176">0x041F</span></span> |
| <span data-ttu-id="ae24d-177">Ungherese</span><span class="sxs-lookup"><span data-stu-id="ae24d-177">Hungarian</span></span>             | <span data-ttu-id="ae24d-178">0x040E</span><span class="sxs-lookup"><span data-stu-id="ae24d-178">0x040E</span></span> |                       |        |



 

<span data-ttu-id="ae24d-179">Se non si imposta questo ID lingua per il carattere, l'ID lingua del carattere sarà l'ID lingua di sistema corrente.</span><span class="sxs-lookup"><span data-stu-id="ae24d-179">If you do not set this language ID for the character, the character's language ID will be the current system language ID.</span></span>

<span data-ttu-id="ae24d-180">Questa impostazione determina anche la lingua per l'output TTS, il testo del fumetto, i comandi nel menu a comparsa del carattere e il motore di riconoscimento vocale.</span><span class="sxs-lookup"><span data-stu-id="ae24d-180">This setting also determines the language for TTS output, word balloon text, the commands in the character's pop-up menu, and speech recognition engine.</span></span> <span data-ttu-id="ae24d-181">Per determinare se è disponibile un motore di riconoscimento vocale compatibile per la lingua del carattere, usare [**IAgentCharacterEx::GetSRModeID**](iagentcharacterex--getsrmodeid.md) o [**IAgentCharacterEx::GetTTSModeID**](iagentcharacterex--getttsmodeid.md).</span><span class="sxs-lookup"><span data-stu-id="ae24d-181">To determine if there is a compatible speech recognition engine available for the character's language, use [**IAgentCharacterEx::GetSRModeID**](iagentcharacterex--getsrmodeid.md) or [**IAgentCharacterEx::GetTTSModeID**](iagentcharacterex--getttsmodeid.md).</span></span>

<span data-ttu-id="ae24d-182">Questa proprietà si applica solo all'uso del carattere da parte dell'applicazione client. l'impostazione non influisce sugli altri client del carattere o di altri caratteri dell'applicazione client.</span><span class="sxs-lookup"><span data-stu-id="ae24d-182">This property applies only to your client application's use of the character; the setting does not affect other clients of the character or other characters of your client application.</span></span>

> [!Note]  
> <span data-ttu-id="ae24d-183">Se l'ID lingua è impostato su una lingua che supporta il testo bidirezionale (ad esempio arabo o ebraico), ma nel sistema che esegue l'applicazione non è installato il supporto bidirezionale, il testo verrà visualizzato nel fumetto della parola in ordine logico anziché di visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="ae24d-183">If the language ID is set to a language that supports bidirectional text (such as Arabic or Hebrew), but the system running your application does not have bidirectional support installed, text will appear in the word balloon in logical rather than display order.</span></span>

 

## <a name="see-also"></a><span data-ttu-id="ae24d-184">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="ae24d-184">See Also</span></span>

<span data-ttu-id="ae24d-185">[**IAgentCharacterEx:SetLanguageID,**](iagentcharacterex--setlanguageid.md) [**IAgentCharacterEx::GetSRModeID,**](iagentcharacterex--getsrmodeid.md) [**IAgentCharacterEx::GetTTSModeID**](iagentcharacterex--getttsmodeid.md)</span><span class="sxs-lookup"><span data-stu-id="ae24d-185">[**IAgentCharacterEx:SetLanguageID**](iagentcharacterex--setlanguageid.md), [**IAgentCharacterEx::GetSRModeID**](iagentcharacterex--getsrmodeid.md), [**IAgentCharacterEx::GetTTSModeID**](iagentcharacterex--getttsmodeid.md)</span></span>


 

 




