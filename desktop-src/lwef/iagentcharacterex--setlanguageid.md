---
title: IAgentCharacterEx SetLanguageID
description: IAgentCharacterEx SetLanguageID
ms.assetid: 064f4c3c-1871-4372-9796-5b53f05c6d9a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 036e1d41878adaae878a5961b45d190971d790af
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/30/2021
ms.locfileid: "113119006"
---
# <a name="iagentcharacterexsetlanguageid"></a><span data-ttu-id="ebd28-103">IAgentCharacterEx::SetLanguageID</span><span class="sxs-lookup"><span data-stu-id="ebd28-103">IAgentCharacterEx::SetLanguageID</span></span>

<span data-ttu-id="ebd28-104">\[Microsoft Agent è deprecato a livello di Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="ebd28-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT SetLanguageID(
   long langID  // language ID setting of character
); 
```

<span data-ttu-id="ebd28-105">Imposta l'ID lingua impostato per il carattere.</span><span class="sxs-lookup"><span data-stu-id="ebd28-105">Sets the language ID set for the character.</span></span>

-   <span data-ttu-id="ebd28-106">Restituisce S \_ OK per indicare che l'operazione è riuscita.</span><span class="sxs-lookup"><span data-stu-id="ebd28-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="ebd28-107"><span id="langID"></span><span id="langid"></span><span id="LANGID"></span>*langID*</span><span class="sxs-lookup"><span data-stu-id="ebd28-107"><span id="langID"></span><span id="langid"></span><span id="LANGID"></span>*langID*</span></span>
</dt> <dd>

<span data-ttu-id="ebd28-108">Impostazione dell'ID lingua per il carattere.</span><span class="sxs-lookup"><span data-stu-id="ebd28-108">The language ID setting for the character.</span></span>

</dd> </dl>

<span data-ttu-id="ebd28-109">Intero lungo che specifica l'ID lingua per il carattere.</span><span class="sxs-lookup"><span data-stu-id="ebd28-109">A Long integer specifying the language ID for the character.</span></span> <span data-ttu-id="ebd28-110">L'ID lingua (LANGID) per un carattere è un valore a 16 bit definito da Windows, costituito da un ID lingua primaria e un ID lingua secondaria.</span><span class="sxs-lookup"><span data-stu-id="ebd28-110">The language ID (LANGID) for a character is a 16-bit value defined by Windows, consisting of a primary language ID and a secondary language ID.</span></span> <span data-ttu-id="ebd28-111">È possibile usare i valori seguenti per le lingue specificate.</span><span class="sxs-lookup"><span data-stu-id="ebd28-111">You can use the following values for the specified languages.</span></span> <span data-ttu-id="ebd28-112">Per altre informazioni, vedere la documentazione di Platform SDK.</span><span class="sxs-lookup"><span data-stu-id="ebd28-112">For more information, see the Platform SDK documentation.</span></span>



| <span data-ttu-id="ebd28-113">Lingua</span><span class="sxs-lookup"><span data-stu-id="ebd28-113">Language</span></span>              | <span data-ttu-id="ebd28-114">ID</span><span class="sxs-lookup"><span data-stu-id="ebd28-114">ID</span></span>     |  <span data-ttu-id="ebd28-115">Lingua</span><span class="sxs-lookup"><span data-stu-id="ebd28-115">Language</span></span>             | <span data-ttu-id="ebd28-116">ID</span><span class="sxs-lookup"><span data-stu-id="ebd28-116">ID</span></span>     |
|-----------------------|--------|-----------------------|--------|
| <span data-ttu-id="ebd28-117">Arabo (Saudita)</span><span class="sxs-lookup"><span data-stu-id="ebd28-117">Arabic (Saudi)</span></span>        | <span data-ttu-id="ebd28-118">0x0401</span><span class="sxs-lookup"><span data-stu-id="ebd28-118">0x0401</span></span> | <span data-ttu-id="ebd28-119">Italiano</span><span class="sxs-lookup"><span data-stu-id="ebd28-119">Italian</span></span>               | <span data-ttu-id="ebd28-120">0x0410</span><span class="sxs-lookup"><span data-stu-id="ebd28-120">0x0410</span></span> |
| <span data-ttu-id="ebd28-121">Basco</span><span class="sxs-lookup"><span data-stu-id="ebd28-121">Basque</span></span>                | <span data-ttu-id="ebd28-122">0x042d</span><span class="sxs-lookup"><span data-stu-id="ebd28-122">0x042d</span></span> | <span data-ttu-id="ebd28-123">Giapponese</span><span class="sxs-lookup"><span data-stu-id="ebd28-123">Japanese</span></span>              | <span data-ttu-id="ebd28-124">0x0411</span><span class="sxs-lookup"><span data-stu-id="ebd28-124">0x0411</span></span> |
| <span data-ttu-id="ebd28-125">Cinese (semplificato)</span><span class="sxs-lookup"><span data-stu-id="ebd28-125">Chinese (Simplified)</span></span>  | <span data-ttu-id="ebd28-126">0x0804</span><span class="sxs-lookup"><span data-stu-id="ebd28-126">0x0804</span></span> | <span data-ttu-id="ebd28-127">Coreano</span><span class="sxs-lookup"><span data-stu-id="ebd28-127">Korean</span></span>                | <span data-ttu-id="ebd28-128">0x0412</span><span class="sxs-lookup"><span data-stu-id="ebd28-128">0x0412</span></span> |
| <span data-ttu-id="ebd28-129">Cinese (tradizionale)</span><span class="sxs-lookup"><span data-stu-id="ebd28-129">Chinese (Traditional)</span></span> | <span data-ttu-id="ebd28-130">0x0404</span><span class="sxs-lookup"><span data-stu-id="ebd28-130">0x0404</span></span> | <span data-ttu-id="ebd28-131">Norvegese</span><span class="sxs-lookup"><span data-stu-id="ebd28-131">Norwegian</span></span>             | <span data-ttu-id="ebd28-132">0x0414</span><span class="sxs-lookup"><span data-stu-id="ebd28-132">0x0414</span></span> |
| <span data-ttu-id="ebd28-133">Croato</span><span class="sxs-lookup"><span data-stu-id="ebd28-133">Croatian</span></span>              | <span data-ttu-id="ebd28-134">0x041A</span><span class="sxs-lookup"><span data-stu-id="ebd28-134">0x041A</span></span> | <span data-ttu-id="ebd28-135">Polacco</span><span class="sxs-lookup"><span data-stu-id="ebd28-135">Polish</span></span>                | <span data-ttu-id="ebd28-136">0x0415</span><span class="sxs-lookup"><span data-stu-id="ebd28-136">0x0415</span></span> |
| <span data-ttu-id="ebd28-137">Ceco</span><span class="sxs-lookup"><span data-stu-id="ebd28-137">Czech</span></span>                 | <span data-ttu-id="ebd28-138">0x0405</span><span class="sxs-lookup"><span data-stu-id="ebd28-138">0x0405</span></span> | <span data-ttu-id="ebd28-139">Portoghese (Portogallo)</span><span class="sxs-lookup"><span data-stu-id="ebd28-139">Portuguese (Portugal)</span></span> | <span data-ttu-id="ebd28-140">0x0816</span><span class="sxs-lookup"><span data-stu-id="ebd28-140">0x0816</span></span> |
| <span data-ttu-id="ebd28-141">Danese</span><span class="sxs-lookup"><span data-stu-id="ebd28-141">Danish</span></span>                | <span data-ttu-id="ebd28-142">0x0406</span><span class="sxs-lookup"><span data-stu-id="ebd28-142">0x0406</span></span> | <span data-ttu-id="ebd28-143">Portoghese (Brasile)</span><span class="sxs-lookup"><span data-stu-id="ebd28-143">Portuguese (Brazil)</span></span>   | <span data-ttu-id="ebd28-144">0x0416</span><span class="sxs-lookup"><span data-stu-id="ebd28-144">0x0416</span></span> |
| <span data-ttu-id="ebd28-145">Olandese</span><span class="sxs-lookup"><span data-stu-id="ebd28-145">Dutch</span></span>                 | <span data-ttu-id="ebd28-146">0x0413</span><span class="sxs-lookup"><span data-stu-id="ebd28-146">0x0413</span></span> | <span data-ttu-id="ebd28-147">Romeno</span><span class="sxs-lookup"><span data-stu-id="ebd28-147">Romanian</span></span>              | <span data-ttu-id="ebd28-148">0x0418</span><span class="sxs-lookup"><span data-stu-id="ebd28-148">0x0418</span></span> |
| <span data-ttu-id="ebd28-149">Inglese (Regno Unito)</span><span class="sxs-lookup"><span data-stu-id="ebd28-149">English (British)</span></span>     | <span data-ttu-id="ebd28-150">0x0809</span><span class="sxs-lookup"><span data-stu-id="ebd28-150">0x0809</span></span> | <span data-ttu-id="ebd28-151">Russo</span><span class="sxs-lookup"><span data-stu-id="ebd28-151">Russian</span></span>               | <span data-ttu-id="ebd28-152">0x0419</span><span class="sxs-lookup"><span data-stu-id="ebd28-152">0x0419</span></span> |
| <span data-ttu-id="ebd28-153">Inglese (Stati Uniti)</span><span class="sxs-lookup"><span data-stu-id="ebd28-153">English (US)</span></span>          | <span data-ttu-id="ebd28-154">0x0409</span><span class="sxs-lookup"><span data-stu-id="ebd28-154">0x0409</span></span> | <span data-ttu-id="ebd28-155">Slovacco</span><span class="sxs-lookup"><span data-stu-id="ebd28-155">Slovakian</span></span>             | <span data-ttu-id="ebd28-156">0x041B</span><span class="sxs-lookup"><span data-stu-id="ebd28-156">0x041B</span></span> |
| <span data-ttu-id="ebd28-157">Finlandese</span><span class="sxs-lookup"><span data-stu-id="ebd28-157">Finnish</span></span>               | <span data-ttu-id="ebd28-158">0x040B</span><span class="sxs-lookup"><span data-stu-id="ebd28-158">0x040B</span></span> | <span data-ttu-id="ebd28-159">Sloveno</span><span class="sxs-lookup"><span data-stu-id="ebd28-159">Slovenian</span></span>             | <span data-ttu-id="ebd28-160">0x0424</span><span class="sxs-lookup"><span data-stu-id="ebd28-160">0x0424</span></span> |
| <span data-ttu-id="ebd28-161">Francese</span><span class="sxs-lookup"><span data-stu-id="ebd28-161">French</span></span>                | <span data-ttu-id="ebd28-162">0x040C</span><span class="sxs-lookup"><span data-stu-id="ebd28-162">0x040C</span></span> | <span data-ttu-id="ebd28-163">Spagnolo</span><span class="sxs-lookup"><span data-stu-id="ebd28-163">Spanish</span></span>               | <span data-ttu-id="ebd28-164">0x0C0A</span><span class="sxs-lookup"><span data-stu-id="ebd28-164">0x0C0A</span></span> |
| <span data-ttu-id="ebd28-165">Tedesco</span><span class="sxs-lookup"><span data-stu-id="ebd28-165">German</span></span>                | <span data-ttu-id="ebd28-166">0x0407</span><span class="sxs-lookup"><span data-stu-id="ebd28-166">0x0407</span></span> | <span data-ttu-id="ebd28-167">Svedese</span><span class="sxs-lookup"><span data-stu-id="ebd28-167">Swedish</span></span>               | <span data-ttu-id="ebd28-168">0x041D</span><span class="sxs-lookup"><span data-stu-id="ebd28-168">0x041D</span></span> |
| <span data-ttu-id="ebd28-169">Greco</span><span class="sxs-lookup"><span data-stu-id="ebd28-169">Greek</span></span>                 | <span data-ttu-id="ebd28-170">0x0408</span><span class="sxs-lookup"><span data-stu-id="ebd28-170">0x0408</span></span> | <span data-ttu-id="ebd28-171">Thai</span><span class="sxs-lookup"><span data-stu-id="ebd28-171">Thai</span></span>                  | <span data-ttu-id="ebd28-172">0x041E</span><span class="sxs-lookup"><span data-stu-id="ebd28-172">0x041E</span></span> |
| <span data-ttu-id="ebd28-173">Ebraico</span><span class="sxs-lookup"><span data-stu-id="ebd28-173">Hebrew</span></span>                | <span data-ttu-id="ebd28-174">0x040D</span><span class="sxs-lookup"><span data-stu-id="ebd28-174">0x040D</span></span> | <span data-ttu-id="ebd28-175">Turco</span><span class="sxs-lookup"><span data-stu-id="ebd28-175">Turkish</span></span>               | <span data-ttu-id="ebd28-176">0x041F</span><span class="sxs-lookup"><span data-stu-id="ebd28-176">0x041F</span></span> |
| <span data-ttu-id="ebd28-177">Ungherese</span><span class="sxs-lookup"><span data-stu-id="ebd28-177">Hungarian</span></span>             | <span data-ttu-id="ebd28-178">0x040E</span><span class="sxs-lookup"><span data-stu-id="ebd28-178">0x040E</span></span> |                       |        |



 

<span data-ttu-id="ebd28-179">Se non si imposta l'ID lingua per il carattere, il relativo ID lingua sarà l'ID lingua di sistema corrente se è installata la DLL della lingua dell'agente corrispondente. In caso contrario, la lingua del carattere sarà Inglese (Stati Uniti).</span><span class="sxs-lookup"><span data-stu-id="ebd28-179">If you do not set the language ID for the character, its language ID will be the current system language ID if the corresponding Agent language DLL is installed; otherwise, the character's language will be English (US).</span></span>

<span data-ttu-id="ebd28-180">Questa proprietà determina anche la lingua per il testo del fumetto delle parole, i comandi nel menu a comparsa del carattere e il motore di riconoscimento vocale.</span><span class="sxs-lookup"><span data-stu-id="ebd28-180">This property also determines the language for the word balloon text, the commands in the character's pop-up menu, and the speech recognition engine.</span></span> <span data-ttu-id="ebd28-181">Determina anche la lingua predefinita per l'output TTS.</span><span class="sxs-lookup"><span data-stu-id="ebd28-181">It also determines the default language for TTS output.</span></span> <span data-ttu-id="ebd28-182">Per determinare se è disponibile un motore di riconoscimento vocale compatibile per la lingua del carattere, usare [**IAgentCharacterEx::GetSRModeID**](iagentcharacterex--getsrmodeid.md) o [**IAgentCharacterEx::GetTTSModeID**](iagentcharacterex--getttsmodeid.md).</span><span class="sxs-lookup"><span data-stu-id="ebd28-182">To determine if there is a compatible speech engine available for the character's language, use [**IAgentCharacterEx::GetSRModeID**](iagentcharacterex--getsrmodeid.md) or [**IAgentCharacterEx::GetTTSModeID**](iagentcharacterex--getttsmodeid.md).</span></span>

<span data-ttu-id="ebd28-183">Se si tenta di impostare l'ID lingua per un carattere e le risorse della lingua dell'agente, la tabella codici o un tipo di carattere visualizzato per l'ID lingua non sono disponibili, Agent restituisce un errore e l'ID lingua del carattere rimane all'ultima impostazione.</span><span class="sxs-lookup"><span data-stu-id="ebd28-183">If you try to set the language ID for a character and the Agent language resources, the code page, or a display font for the language ID is not available, Agent returns an error and the character's language ID remains at its last setting.</span></span> <span data-ttu-id="ebd28-184">L'impostazione di questa proprietà non restituisce un errore se non sono presenti motori di riconoscimento vocale corrispondenti per la lingua.</span><span class="sxs-lookup"><span data-stu-id="ebd28-184">Setting this property does not return an error if there are no matching speech engines for the language.</span></span>

<span data-ttu-id="ebd28-185">Questa proprietà si applica solo all'uso del carattere da parte dell'applicazione client. l'impostazione non influisce sugli altri client del carattere o di altri caratteri dell'applicazione client.</span><span class="sxs-lookup"><span data-stu-id="ebd28-185">This property applies only to your client application's use of the character; the setting does not affect other clients of the character or other characters of your client application.</span></span>

> [!Note]  
> <span data-ttu-id="ebd28-186">Se si imposta l'ID lingua del carattere su una lingua che supporta il testo bidirezionale (ad esempio arabo o ebraico), ma nel sistema che esegue l'applicazione non è installato il supporto bidirezionale, il testo verrà visualizzato nel fumetto delle parole in ordine logico anziché di visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="ebd28-186">If you set the character's language ID to a language that supports bidirectional text (such as Arabic or Hebrew), but the system running your application does not have bidirectional support installed, text will appear in the word balloon in logical rather than display order.</span></span>

 

## <a name="see-also"></a><span data-ttu-id="ebd28-187">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="ebd28-187">See Also</span></span>

<span data-ttu-id="ebd28-188">[**IAgentCharacterEx:GetLanguageID,**](iagentcharacterex--getlanguageid.md) [**IAgentCharacterEx::GetSRModeID,**](iagentcharacterex--getsrmodeid.md) [**IAgentCharacterEx::GetTTSModeID**](iagentcharacterex--getttsmodeid.md)</span><span class="sxs-lookup"><span data-stu-id="ebd28-188">[**IAgentCharacterEx:GetLanguageID**](iagentcharacterex--getlanguageid.md), [**IAgentCharacterEx::GetSRModeID**](iagentcharacterex--getsrmodeid.md), [**IAgentCharacterEx::GetTTSModeID**](iagentcharacterex--getttsmodeid.md)</span></span>


 

 




