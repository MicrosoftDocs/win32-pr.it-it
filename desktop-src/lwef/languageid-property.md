---
title: Proprietà LanguageID
description: Proprietà LanguageID
ms.assetid: f57b0fa1-b3b8-49c8-b441-2a40e564d6ea
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7a7a10e6b16f9e35b223bada728871d253685538
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104331996"
---
# <a name="languageid-property"></a><span data-ttu-id="d1117-103">Proprietà LanguageID</span><span class="sxs-lookup"><span data-stu-id="d1117-103">LanguageID Property</span></span>

<span data-ttu-id="d1117-104">\[Microsoft Agent è stato deprecato a partire da Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="d1117-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="d1117-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descrizione**</span><span class="sxs-lookup"><span data-stu-id="d1117-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="d1117-106">Restituisce o imposta l'ID lingua per il carattere.</span><span class="sxs-lookup"><span data-stu-id="d1117-106">Returns or sets the language ID for the character.</span></span>

</dd> <dt>

<span data-ttu-id="d1117-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintassi**</span><span class="sxs-lookup"><span data-stu-id="d1117-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="d1117-108">*Agent. \* \* \* caratteri* \*  **("***CharacterID***").** \[  =  *LanguageID* LanguageID\]</span><span class="sxs-lookup"><span data-stu-id="d1117-108">*agent.\*\*\*Characters*\* **("***CharacterID***").LanguageID** \[ = *LanguageID*\]</span></span>



<span data-ttu-id="d1117-109">Parte</span><span class="sxs-lookup"><span data-stu-id="d1117-109">Part</span></span>

<span data-ttu-id="d1117-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d1117-110">Description</span></span>

<span data-ttu-id="d1117-111">LanguageID</span><span class="sxs-lookup"><span data-stu-id="d1117-111">LanguageID</span></span>

<span data-ttu-id="d1117-112">Valore long integer che specifica l'ID lingua per il carattere.</span><span class="sxs-lookup"><span data-stu-id="d1117-112">A Long integer specifying the language ID for the character.</span></span> <span data-ttu-id="d1117-113">L'ID lingua (LANGID) per un carattere è un valore a 16 bit definito da Windows, costituito da un ID di lingua primario e da un ID di lingua secondaria.</span><span class="sxs-lookup"><span data-stu-id="d1117-113">The language ID (LANGID) for a character is a 16-bit value defined by Windows, consisting of a primary language ID and a secondary language ID.</span></span> <span data-ttu-id="d1117-114">Gli esempi seguenti sono valori per le lingue supportate da Microsoft Agent.</span><span class="sxs-lookup"><span data-stu-id="d1117-114">The following examples are values for languages supported by Microsoft Agent.</span></span> <span data-ttu-id="d1117-115">Per determinare il valore per altre lingue, vedere la *documentazione di Platform SDK*.</span><span class="sxs-lookup"><span data-stu-id="d1117-115">To determine the value for other languages, see the *Platform SDK documentation*.</span></span>

 

<span data-ttu-id="d1117-116">Arabo</span><span class="sxs-lookup"><span data-stu-id="d1117-116">Arabic</span></span>

<span data-ttu-id="d1117-117">&H0401</span><span class="sxs-lookup"><span data-stu-id="d1117-117">&H0401</span></span>

<span data-ttu-id="d1117-118">Italiano</span><span class="sxs-lookup"><span data-stu-id="d1117-118">Italian</span></span>

<span data-ttu-id="d1117-119">&H0410</span><span class="sxs-lookup"><span data-stu-id="d1117-119">&H0410</span></span>

 

<span data-ttu-id="d1117-120">Basco</span><span class="sxs-lookup"><span data-stu-id="d1117-120">Basque</span></span>

<span data-ttu-id="d1117-121">&H042D</span><span class="sxs-lookup"><span data-stu-id="d1117-121">&H042D</span></span>

<span data-ttu-id="d1117-122">Giapponese</span><span class="sxs-lookup"><span data-stu-id="d1117-122">Japanese</span></span>

<span data-ttu-id="d1117-123">&H0411</span><span class="sxs-lookup"><span data-stu-id="d1117-123">&H0411</span></span>

 

<span data-ttu-id="d1117-124">Cinese (semplificato)</span><span class="sxs-lookup"><span data-stu-id="d1117-124">Chinese (Simplified)</span></span>

<span data-ttu-id="d1117-125">&H0804</span><span class="sxs-lookup"><span data-stu-id="d1117-125">&H0804</span></span>

<span data-ttu-id="d1117-126">Coreano</span><span class="sxs-lookup"><span data-stu-id="d1117-126">Korean</span></span>

<span data-ttu-id="d1117-127">&H0412</span><span class="sxs-lookup"><span data-stu-id="d1117-127">&H0412</span></span>

 

<span data-ttu-id="d1117-128">Cinese (tradizionale)</span><span class="sxs-lookup"><span data-stu-id="d1117-128">Chinese (Traditional)</span></span>

<span data-ttu-id="d1117-129">&H0404</span><span class="sxs-lookup"><span data-stu-id="d1117-129">&H0404</span></span>

<span data-ttu-id="d1117-130">Norvegese</span><span class="sxs-lookup"><span data-stu-id="d1117-130">Norwegian</span></span>

<span data-ttu-id="d1117-131">&H0414</span><span class="sxs-lookup"><span data-stu-id="d1117-131">&H0414</span></span>

 

<span data-ttu-id="d1117-132">Croato</span><span class="sxs-lookup"><span data-stu-id="d1117-132">Croatian</span></span>

<span data-ttu-id="d1117-133">&H041A</span><span class="sxs-lookup"><span data-stu-id="d1117-133">&H041A</span></span>

<span data-ttu-id="d1117-134">Polacco</span><span class="sxs-lookup"><span data-stu-id="d1117-134">Polish</span></span>

<span data-ttu-id="d1117-135">&H0415</span><span class="sxs-lookup"><span data-stu-id="d1117-135">&H0415</span></span>

 

<span data-ttu-id="d1117-136">Ceco</span><span class="sxs-lookup"><span data-stu-id="d1117-136">Czech</span></span>

<span data-ttu-id="d1117-137">&H0405</span><span class="sxs-lookup"><span data-stu-id="d1117-137">&H0405</span></span>

<span data-ttu-id="d1117-138">Portoghese (Portogallo)</span><span class="sxs-lookup"><span data-stu-id="d1117-138">Portuguese (Portugal)</span></span>

<span data-ttu-id="d1117-139">&H0816</span><span class="sxs-lookup"><span data-stu-id="d1117-139">&H0816</span></span>

 

<span data-ttu-id="d1117-140">Danese</span><span class="sxs-lookup"><span data-stu-id="d1117-140">Danish</span></span>

<span data-ttu-id="d1117-141">&H0406</span><span class="sxs-lookup"><span data-stu-id="d1117-141">&H0406</span></span>

<span data-ttu-id="d1117-142">Portoghese (Brasile)</span><span class="sxs-lookup"><span data-stu-id="d1117-142">Portuguese (Brazil)</span></span>

<span data-ttu-id="d1117-143">&H0416</span><span class="sxs-lookup"><span data-stu-id="d1117-143">&H0416</span></span>

 

<span data-ttu-id="d1117-144">Olandese</span><span class="sxs-lookup"><span data-stu-id="d1117-144">Dutch</span></span>

<span data-ttu-id="d1117-145">&H0413</span><span class="sxs-lookup"><span data-stu-id="d1117-145">&H0413</span></span>

<span data-ttu-id="d1117-146">Romeno</span><span class="sxs-lookup"><span data-stu-id="d1117-146">Romanian</span></span>

<span data-ttu-id="d1117-147">&H0418</span><span class="sxs-lookup"><span data-stu-id="d1117-147">&H0418</span></span>

 

<span data-ttu-id="d1117-148">Inglese (Regno Unito)</span><span class="sxs-lookup"><span data-stu-id="d1117-148">English (British)</span></span>

<span data-ttu-id="d1117-149">&H0809</span><span class="sxs-lookup"><span data-stu-id="d1117-149">&H0809</span></span>

<span data-ttu-id="d1117-150">Russo</span><span class="sxs-lookup"><span data-stu-id="d1117-150">Russian</span></span>

<span data-ttu-id="d1117-151">&H0419</span><span class="sxs-lookup"><span data-stu-id="d1117-151">&H0419</span></span>

 

<span data-ttu-id="d1117-152">Inglese (Stati Uniti)</span><span class="sxs-lookup"><span data-stu-id="d1117-152">English (US)</span></span>

<span data-ttu-id="d1117-153">&H0409</span><span class="sxs-lookup"><span data-stu-id="d1117-153">&H0409</span></span>

<span data-ttu-id="d1117-154">Slovacco</span><span class="sxs-lookup"><span data-stu-id="d1117-154">Slovakian</span></span>

<span data-ttu-id="d1117-155">&H041B</span><span class="sxs-lookup"><span data-stu-id="d1117-155">&H041B</span></span>

 

<span data-ttu-id="d1117-156">Finlandese</span><span class="sxs-lookup"><span data-stu-id="d1117-156">Finnish</span></span>

<span data-ttu-id="d1117-157">&H040B</span><span class="sxs-lookup"><span data-stu-id="d1117-157">&H040B</span></span>

<span data-ttu-id="d1117-158">Sloveno</span><span class="sxs-lookup"><span data-stu-id="d1117-158">Slovenian</span></span>

<span data-ttu-id="d1117-159">&H0424</span><span class="sxs-lookup"><span data-stu-id="d1117-159">&H0424</span></span>

 

<span data-ttu-id="d1117-160">Francese</span><span class="sxs-lookup"><span data-stu-id="d1117-160">French</span></span>

<span data-ttu-id="d1117-161">&H040C</span><span class="sxs-lookup"><span data-stu-id="d1117-161">&H040C</span></span>

<span data-ttu-id="d1117-162">Spagnolo</span><span class="sxs-lookup"><span data-stu-id="d1117-162">Spanish</span></span>

<span data-ttu-id="d1117-163">&H0C0A</span><span class="sxs-lookup"><span data-stu-id="d1117-163">&H0C0A</span></span>

 

<span data-ttu-id="d1117-164">Tedesco</span><span class="sxs-lookup"><span data-stu-id="d1117-164">German</span></span>

<span data-ttu-id="d1117-165">&H0407</span><span class="sxs-lookup"><span data-stu-id="d1117-165">&H0407</span></span>

<span data-ttu-id="d1117-166">Svedese</span><span class="sxs-lookup"><span data-stu-id="d1117-166">Swedish</span></span>

<span data-ttu-id="d1117-167">&H041D</span><span class="sxs-lookup"><span data-stu-id="d1117-167">&H041D</span></span>

 

<span data-ttu-id="d1117-168">Greco</span><span class="sxs-lookup"><span data-stu-id="d1117-168">Greek</span></span>

<span data-ttu-id="d1117-169">&H0408</span><span class="sxs-lookup"><span data-stu-id="d1117-169">&H0408</span></span>

<span data-ttu-id="d1117-170">Thai</span><span class="sxs-lookup"><span data-stu-id="d1117-170">Thai</span></span>

<span data-ttu-id="d1117-171">&H041E</span><span class="sxs-lookup"><span data-stu-id="d1117-171">&H041E</span></span>

 

<span data-ttu-id="d1117-172">Ebraico</span><span class="sxs-lookup"><span data-stu-id="d1117-172">Hebrew</span></span>

<span data-ttu-id="d1117-173">&H040D</span><span class="sxs-lookup"><span data-stu-id="d1117-173">&H040D</span></span>

<span data-ttu-id="d1117-174">Turco</span><span class="sxs-lookup"><span data-stu-id="d1117-174">Turkish</span></span>

<span data-ttu-id="d1117-175">&H041F</span><span class="sxs-lookup"><span data-stu-id="d1117-175">&H041F</span></span>

 

<span data-ttu-id="d1117-176">Ungherese</span><span class="sxs-lookup"><span data-stu-id="d1117-176">Hungarian</span></span>

<span data-ttu-id="d1117-177">&H040E</span><span class="sxs-lookup"><span data-stu-id="d1117-177">&H040E</span></span>

 

 



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="d1117-178">Commenti</span><span class="sxs-lookup"><span data-stu-id="d1117-178">Remarks</span></span>

<span data-ttu-id="d1117-179">Se non si imposta **LanguageID** per il carattere, il relativo ID lingua sarà l'ID della lingua di sistema corrente se è installata la dll della lingua dell'agente corrispondente. in caso contrario, la lingua del carattere sarà inglese (Stati Uniti).</span><span class="sxs-lookup"><span data-stu-id="d1117-179">If you do not set the **LanguageID** for the character, its language ID will be the current system language ID if the corresponding Agent language DLL is installed, otherwise, the character's language will be English (US).</span></span>

<span data-ttu-id="d1117-180">Questa proprietà determina anche la lingua del testo del fumetto di parole, i comandi nel menu a comparsa del carattere e il motore di riconoscimento vocale.</span><span class="sxs-lookup"><span data-stu-id="d1117-180">This property also determines the language for word balloon text, the commands in the character's pop-up menu, and the speech recognition engine.</span></span> <span data-ttu-id="d1117-181">Consente inoltre di determinare la lingua predefinita per l'output TTS.</span><span class="sxs-lookup"><span data-stu-id="d1117-181">It also determines the default language for TTS output.</span></span>

<span data-ttu-id="d1117-182">Se si tenta di impostare **LanguageID** per un carattere e la dll della lingua dell'agente per tale lingua non è installata o non è disponibile un tipo di carattere visualizzato per l'ID lingua, Agent genera un errore e **LanguageID** rimane all'ultima impostazione.</span><span class="sxs-lookup"><span data-stu-id="d1117-182">If you try to set the **LanguageID** for a character and the Agent language DLL for that language is not installed or a display font for the language ID is not available, Agent raises an error and **LanguageID** remains at its last setting.</span></span>

<span data-ttu-id="d1117-183">L'impostazione di questa proprietà non genera un errore se non sono presenti motori di riconoscimento vocale corrispondenti per la lingua.</span><span class="sxs-lookup"><span data-stu-id="d1117-183">Setting this property does not raise an error if there are no matching speech engines for the language.</span></span> <span data-ttu-id="d1117-184">Per determinare se è disponibile un motore vocale compatibile per **LanguageID**, controllare [**SRModeID**](srmodeid-property.md) o [**TTSModeID**](ttsmodeid-property.md).</span><span class="sxs-lookup"><span data-stu-id="d1117-184">To determine if there is a compatible speech engine available for the **LanguageID**, check [**SRModeID**](srmodeid-property.md) or [**TTSModeID**](ttsmodeid-property.md).</span></span> <span data-ttu-id="d1117-185">Se non si imposta **LanguageID**, questo verrà impostato sull'impostazione ID lingua predefinita dell'utente.</span><span class="sxs-lookup"><span data-stu-id="d1117-185">If you do not set **LanguageID**, it will be set to the user default language ID setting.</span></span>

<span data-ttu-id="d1117-186">Questa proprietà si applica solo all'utilizzo del carattere da parte dell'applicazione client. l'impostazione non influisce sugli altri client del carattere o di altri caratteri dell'applicazione client.</span><span class="sxs-lookup"><span data-stu-id="d1117-186">This property applies only to your client application's use of the character; the setting does not affect other clients of the character or other characters of your client application.</span></span>

> [!Note]  
> <span data-ttu-id="d1117-187">Se si imposta **LanguageID** su una lingua che supporta il testo bidirezionale, ad esempio l'arabo o l'ebraico, ma nel sistema in cui è in esecuzione l'applicazione non è installato il supporto bidirezionale, il testo nella parola Balloon verrà visualizzato nell'ordine logico anziché in quello di visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="d1117-187">If you set **LanguageID** to a language that supports bidirectional text (such as Arabic or Hebrew), but the system running your application does not have bidirectional support installed, text in the word balloon will appear in logical rather than display order.</span></span>

 

## <a name="see-also"></a><span data-ttu-id="d1117-188">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="d1117-188">See Also</span></span>

<span data-ttu-id="d1117-189">[**Proprietà SRModeID**](srmodeid-property.md), [ **Proprietà TTSModeID**](ttsmodeid-property.md)</span><span class="sxs-lookup"><span data-stu-id="d1117-189">[**SRModeID property**](srmodeid-property.md), [**TTSModeID property**](ttsmodeid-property.md)</span></span>


 

 




