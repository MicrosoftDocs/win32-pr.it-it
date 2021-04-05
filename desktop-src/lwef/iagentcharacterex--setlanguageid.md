---
title: IAgentCharacterEx SetLanguageID
description: IAgentCharacterEx SetLanguageID
ms.assetid: 064f4c3c-1871-4372-9796-5b53f05c6d9a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9ec8a396c174fd251b1cc7ac8d7e9696c9b9f2d1
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103708878"
---
# <a name="iagentcharacterexsetlanguageid"></a><span data-ttu-id="81ae6-103">IAgentCharacterEx::SetLanguageID</span><span class="sxs-lookup"><span data-stu-id="81ae6-103">IAgentCharacterEx::SetLanguageID</span></span>

<span data-ttu-id="81ae6-104">\[Microsoft Agent è stato deprecato a partire da Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="81ae6-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT SetLanguageID(
   long langID  // language ID setting of character
); 
```

<span data-ttu-id="81ae6-105">Imposta l'ID lingua impostato per il carattere.</span><span class="sxs-lookup"><span data-stu-id="81ae6-105">Sets the language ID set for the character.</span></span>

-   <span data-ttu-id="81ae6-106">Restituisce \_ OK per indicare che l'operazione è stata completata.</span><span class="sxs-lookup"><span data-stu-id="81ae6-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="81ae6-107"><span id="langID"></span><span id="langid"></span><span id="LANGID"></span>*langID*</span><span class="sxs-lookup"><span data-stu-id="81ae6-107"><span id="langID"></span><span id="langid"></span><span id="LANGID"></span>*langID*</span></span>
</dt> <dd>

<span data-ttu-id="81ae6-108">Impostazione dell'ID lingua per il carattere.</span><span class="sxs-lookup"><span data-stu-id="81ae6-108">The language ID setting for the character.</span></span>

</dd> </dl>

<span data-ttu-id="81ae6-109">Valore long integer che specifica l'ID lingua per il carattere.</span><span class="sxs-lookup"><span data-stu-id="81ae6-109">A Long integer specifying the language ID for the character.</span></span> <span data-ttu-id="81ae6-110">L'ID lingua (LANGID) per un carattere è un valore a 16 bit definito da Windows, costituito da un ID di lingua primario e da un ID di lingua secondaria.</span><span class="sxs-lookup"><span data-stu-id="81ae6-110">The language ID (LANGID) for a character is a 16-bit value defined by Windows, consisting of a primary language ID and a secondary language ID.</span></span> <span data-ttu-id="81ae6-111">È possibile usare i valori seguenti per le lingue specificate.</span><span class="sxs-lookup"><span data-stu-id="81ae6-111">You can use the following values for the specified languages.</span></span> <span data-ttu-id="81ae6-112">Per ulteriori informazioni, vedere la documentazione di Platform SDK.</span><span class="sxs-lookup"><span data-stu-id="81ae6-112">For more information, see the Platform SDK documentation.</span></span>



|                       |        |                       |        |
|-----------------------|--------|-----------------------|--------|
| <span data-ttu-id="81ae6-113">Arabo (Arabia Saudita)</span><span class="sxs-lookup"><span data-stu-id="81ae6-113">Arabic (Saudi)</span></span>        | <span data-ttu-id="81ae6-114">0x0401</span><span class="sxs-lookup"><span data-stu-id="81ae6-114">0x0401</span></span> | <span data-ttu-id="81ae6-115">Italiano</span><span class="sxs-lookup"><span data-stu-id="81ae6-115">Italian</span></span>               | <span data-ttu-id="81ae6-116">0x0410</span><span class="sxs-lookup"><span data-stu-id="81ae6-116">0x0410</span></span> |
| <span data-ttu-id="81ae6-117">Basco</span><span class="sxs-lookup"><span data-stu-id="81ae6-117">Basque</span></span>                | <span data-ttu-id="81ae6-118">0x042d</span><span class="sxs-lookup"><span data-stu-id="81ae6-118">0x042d</span></span> | <span data-ttu-id="81ae6-119">Giapponese</span><span class="sxs-lookup"><span data-stu-id="81ae6-119">Japanese</span></span>              | <span data-ttu-id="81ae6-120">0x0411</span><span class="sxs-lookup"><span data-stu-id="81ae6-120">0x0411</span></span> |
| <span data-ttu-id="81ae6-121">Cinese (semplificato)</span><span class="sxs-lookup"><span data-stu-id="81ae6-121">Chinese (Simplified)</span></span>  | <span data-ttu-id="81ae6-122">0x0804</span><span class="sxs-lookup"><span data-stu-id="81ae6-122">0x0804</span></span> | <span data-ttu-id="81ae6-123">Coreano</span><span class="sxs-lookup"><span data-stu-id="81ae6-123">Korean</span></span>                | <span data-ttu-id="81ae6-124">0x0412</span><span class="sxs-lookup"><span data-stu-id="81ae6-124">0x0412</span></span> |
| <span data-ttu-id="81ae6-125">Cinese (tradizionale)</span><span class="sxs-lookup"><span data-stu-id="81ae6-125">Chinese (Traditional)</span></span> | <span data-ttu-id="81ae6-126">0x0404</span><span class="sxs-lookup"><span data-stu-id="81ae6-126">0x0404</span></span> | <span data-ttu-id="81ae6-127">Norvegese</span><span class="sxs-lookup"><span data-stu-id="81ae6-127">Norwegian</span></span>             | <span data-ttu-id="81ae6-128">0x0414</span><span class="sxs-lookup"><span data-stu-id="81ae6-128">0x0414</span></span> |
| <span data-ttu-id="81ae6-129">Croato</span><span class="sxs-lookup"><span data-stu-id="81ae6-129">Croatian</span></span>              | <span data-ttu-id="81ae6-130">0x041A</span><span class="sxs-lookup"><span data-stu-id="81ae6-130">0x041A</span></span> | <span data-ttu-id="81ae6-131">Polacco</span><span class="sxs-lookup"><span data-stu-id="81ae6-131">Polish</span></span>                | <span data-ttu-id="81ae6-132">0x0415</span><span class="sxs-lookup"><span data-stu-id="81ae6-132">0x0415</span></span> |
| <span data-ttu-id="81ae6-133">Ceco</span><span class="sxs-lookup"><span data-stu-id="81ae6-133">Czech</span></span>                 | <span data-ttu-id="81ae6-134">0x0405</span><span class="sxs-lookup"><span data-stu-id="81ae6-134">0x0405</span></span> | <span data-ttu-id="81ae6-135">Portoghese (Portogallo)</span><span class="sxs-lookup"><span data-stu-id="81ae6-135">Portuguese (Portugal)</span></span> | <span data-ttu-id="81ae6-136">0x0816</span><span class="sxs-lookup"><span data-stu-id="81ae6-136">0x0816</span></span> |
| <span data-ttu-id="81ae6-137">Danese</span><span class="sxs-lookup"><span data-stu-id="81ae6-137">Danish</span></span>                | <span data-ttu-id="81ae6-138">0x0406</span><span class="sxs-lookup"><span data-stu-id="81ae6-138">0x0406</span></span> | <span data-ttu-id="81ae6-139">Portoghese (Brasile)</span><span class="sxs-lookup"><span data-stu-id="81ae6-139">Portuguese (Brazil)</span></span>   | <span data-ttu-id="81ae6-140">0x0416</span><span class="sxs-lookup"><span data-stu-id="81ae6-140">0x0416</span></span> |
| <span data-ttu-id="81ae6-141">Olandese</span><span class="sxs-lookup"><span data-stu-id="81ae6-141">Dutch</span></span>                 | <span data-ttu-id="81ae6-142">0x0413</span><span class="sxs-lookup"><span data-stu-id="81ae6-142">0x0413</span></span> | <span data-ttu-id="81ae6-143">Romeno</span><span class="sxs-lookup"><span data-stu-id="81ae6-143">Romanian</span></span>              | <span data-ttu-id="81ae6-144">0x0418</span><span class="sxs-lookup"><span data-stu-id="81ae6-144">0x0418</span></span> |
| <span data-ttu-id="81ae6-145">Inglese (Regno Unito)</span><span class="sxs-lookup"><span data-stu-id="81ae6-145">English (British)</span></span>     | <span data-ttu-id="81ae6-146">0x0809</span><span class="sxs-lookup"><span data-stu-id="81ae6-146">0x0809</span></span> | <span data-ttu-id="81ae6-147">Russo</span><span class="sxs-lookup"><span data-stu-id="81ae6-147">Russian</span></span>               | <span data-ttu-id="81ae6-148">0x0419</span><span class="sxs-lookup"><span data-stu-id="81ae6-148">0x0419</span></span> |
| <span data-ttu-id="81ae6-149">Inglese (Stati Uniti)</span><span class="sxs-lookup"><span data-stu-id="81ae6-149">English (US)</span></span>          | <span data-ttu-id="81ae6-150">0x0409</span><span class="sxs-lookup"><span data-stu-id="81ae6-150">0x0409</span></span> | <span data-ttu-id="81ae6-151">Slovacco</span><span class="sxs-lookup"><span data-stu-id="81ae6-151">Slovakian</span></span>             | <span data-ttu-id="81ae6-152">0x041B</span><span class="sxs-lookup"><span data-stu-id="81ae6-152">0x041B</span></span> |
| <span data-ttu-id="81ae6-153">Finlandese</span><span class="sxs-lookup"><span data-stu-id="81ae6-153">Finnish</span></span>               | <span data-ttu-id="81ae6-154">0x040B</span><span class="sxs-lookup"><span data-stu-id="81ae6-154">0x040B</span></span> | <span data-ttu-id="81ae6-155">Sloveno</span><span class="sxs-lookup"><span data-stu-id="81ae6-155">Slovenian</span></span>             | <span data-ttu-id="81ae6-156">0x0424</span><span class="sxs-lookup"><span data-stu-id="81ae6-156">0x0424</span></span> |
| <span data-ttu-id="81ae6-157">Francese</span><span class="sxs-lookup"><span data-stu-id="81ae6-157">French</span></span>                | <span data-ttu-id="81ae6-158">0x040C</span><span class="sxs-lookup"><span data-stu-id="81ae6-158">0x040C</span></span> | <span data-ttu-id="81ae6-159">Spagnolo</span><span class="sxs-lookup"><span data-stu-id="81ae6-159">Spanish</span></span>               | <span data-ttu-id="81ae6-160">0x0C0A</span><span class="sxs-lookup"><span data-stu-id="81ae6-160">0x0C0A</span></span> |
| <span data-ttu-id="81ae6-161">Tedesco</span><span class="sxs-lookup"><span data-stu-id="81ae6-161">German</span></span>                | <span data-ttu-id="81ae6-162">0x0407</span><span class="sxs-lookup"><span data-stu-id="81ae6-162">0x0407</span></span> | <span data-ttu-id="81ae6-163">Svedese</span><span class="sxs-lookup"><span data-stu-id="81ae6-163">Swedish</span></span>               | <span data-ttu-id="81ae6-164">0x041D</span><span class="sxs-lookup"><span data-stu-id="81ae6-164">0x041D</span></span> |
| <span data-ttu-id="81ae6-165">Greco</span><span class="sxs-lookup"><span data-stu-id="81ae6-165">Greek</span></span>                 | <span data-ttu-id="81ae6-166">0x0408</span><span class="sxs-lookup"><span data-stu-id="81ae6-166">0x0408</span></span> | <span data-ttu-id="81ae6-167">Thai</span><span class="sxs-lookup"><span data-stu-id="81ae6-167">Thai</span></span>                  | <span data-ttu-id="81ae6-168">0x041E</span><span class="sxs-lookup"><span data-stu-id="81ae6-168">0x041E</span></span> |
| <span data-ttu-id="81ae6-169">Ebraico</span><span class="sxs-lookup"><span data-stu-id="81ae6-169">Hebrew</span></span>                | <span data-ttu-id="81ae6-170">0x040D</span><span class="sxs-lookup"><span data-stu-id="81ae6-170">0x040D</span></span> | <span data-ttu-id="81ae6-171">Turco</span><span class="sxs-lookup"><span data-stu-id="81ae6-171">Turkish</span></span>               | <span data-ttu-id="81ae6-172">0x041F</span><span class="sxs-lookup"><span data-stu-id="81ae6-172">0x041F</span></span> |
| <span data-ttu-id="81ae6-173">Ungherese</span><span class="sxs-lookup"><span data-stu-id="81ae6-173">Hungarian</span></span>             | <span data-ttu-id="81ae6-174">0x040E</span><span class="sxs-lookup"><span data-stu-id="81ae6-174">0x040E</span></span> |                       |        |



 

<span data-ttu-id="81ae6-175">Se non si imposta l'ID lingua per il carattere, il relativo ID lingua sarà l'ID della lingua di sistema corrente se è installata la DLL della lingua dell'agente corrispondente. in caso contrario, la lingua del carattere sarà inglese (Stati Uniti).</span><span class="sxs-lookup"><span data-stu-id="81ae6-175">If you do not set the language ID for the character, its language ID will be the current system language ID if the corresponding Agent language DLL is installed; otherwise, the character's language will be English (US).</span></span>

<span data-ttu-id="81ae6-176">Questa proprietà determina anche la lingua del testo del fumetto di parole, i comandi nel menu a comparsa del carattere e il motore di riconoscimento vocale.</span><span class="sxs-lookup"><span data-stu-id="81ae6-176">This property also determines the language for the word balloon text, the commands in the character's pop-up menu, and the speech recognition engine.</span></span> <span data-ttu-id="81ae6-177">Consente inoltre di determinare la lingua predefinita per l'output TTS.</span><span class="sxs-lookup"><span data-stu-id="81ae6-177">It also determines the default language for TTS output.</span></span> <span data-ttu-id="81ae6-178">Per determinare se è disponibile un motore di riconoscimento vocale compatibile per la lingua del carattere, usare [**IAgentCharacterEx:: GetSRModeID**](iagentcharacterex--getsrmodeid.md) o [**IAgentCharacterEx:: GetTTSModeID**](iagentcharacterex--getttsmodeid.md).</span><span class="sxs-lookup"><span data-stu-id="81ae6-178">To determine if there is a compatible speech engine available for the character's language, use [**IAgentCharacterEx::GetSRModeID**](iagentcharacterex--getsrmodeid.md) or [**IAgentCharacterEx::GetTTSModeID**](iagentcharacterex--getttsmodeid.md).</span></span>

<span data-ttu-id="81ae6-179">Se si tenta di impostare l'ID lingua per un carattere e le risorse della lingua dell'agente, la tabella codici o un tipo di carattere visualizzato per l'ID lingua non è disponibile, Agent restituisce un errore e l'ID lingua del carattere rimane all'ultima impostazione.</span><span class="sxs-lookup"><span data-stu-id="81ae6-179">If you try to set the language ID for a character and the Agent language resources, the code page, or a display font for the language ID is not available, Agent returns an error and the character's language ID remains at its last setting.</span></span> <span data-ttu-id="81ae6-180">L'impostazione di questa proprietà non restituisce un errore se non sono presenti motori di riconoscimento vocale corrispondenti per la lingua.</span><span class="sxs-lookup"><span data-stu-id="81ae6-180">Setting this property does not return an error if there are no matching speech engines for the language.</span></span>

<span data-ttu-id="81ae6-181">Questa proprietà si applica solo all'utilizzo del carattere da parte dell'applicazione client. l'impostazione non influisce sugli altri client del carattere o di altri caratteri dell'applicazione client.</span><span class="sxs-lookup"><span data-stu-id="81ae6-181">This property applies only to your client application's use of the character; the setting does not affect other clients of the character or other characters of your client application.</span></span>

> [!Note]  
> <span data-ttu-id="81ae6-182">Se si imposta l'ID lingua del carattere su una lingua che supporta il testo bidirezionale, ad esempio l'arabo o l'ebraico, ma nel sistema in cui è in esecuzione l'applicazione non è installato il supporto bidirezionale, il testo verrà visualizzato nella parola fumetto nell'ordine logico anziché in quello di visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="81ae6-182">If you set the character's language ID to a language that supports bidirectional text (such as Arabic or Hebrew), but the system running your application does not have bidirectional support installed, text will appear in the word balloon in logical rather than display order.</span></span>

 

## <a name="see-also"></a><span data-ttu-id="81ae6-183">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="81ae6-183">See Also</span></span>

<span data-ttu-id="81ae6-184">[**IAgentCharacterEx: GetLanguageID**](iagentcharacterex--getlanguageid.md), [**IAgentCharacterEx:: GetSRModeID**](iagentcharacterex--getsrmodeid.md), [**IAgentCharacterEx:: GetTTSModeID**](iagentcharacterex--getttsmodeid.md)</span><span class="sxs-lookup"><span data-stu-id="81ae6-184">[**IAgentCharacterEx:GetLanguageID**](iagentcharacterex--getlanguageid.md), [**IAgentCharacterEx::GetSRModeID**](iagentcharacterex--getsrmodeid.md), [**IAgentCharacterEx::GetTTSModeID**](iagentcharacterex--getttsmodeid.md)</span></span>


 

 




