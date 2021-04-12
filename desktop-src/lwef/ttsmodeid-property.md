---
title: Proprietà TTSModeID
description: Proprietà TTSModeID
ms.assetid: 9205c37e-e006-466a-9b33-b98408c01ed7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c6852f203f5df716df6cfc5962f9cfa911d8fc1a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104221893"
---
# <a name="ttsmodeid-property"></a><span data-ttu-id="1fe33-103">Proprietà TTSModeID</span><span class="sxs-lookup"><span data-stu-id="1fe33-103">TTSModeID Property</span></span>

<span data-ttu-id="1fe33-104">\[Microsoft Agent è stato deprecato a partire da Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="1fe33-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="1fe33-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descrizione**</span><span class="sxs-lookup"><span data-stu-id="1fe33-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="1fe33-106">Restituisce o imposta la modalità del motore di TTS utilizzata per il carattere.</span><span class="sxs-lookup"><span data-stu-id="1fe33-106">Returns or sets the TTS engine mode used for the character.</span></span>

</dd> <dt>

<span data-ttu-id="1fe33-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintassi**</span><span class="sxs-lookup"><span data-stu-id="1fe33-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="1fe33-108">\*agente ***. Caratteri ("*** CharacterID \* \* *").* \*  \[  =  *ModeID* TTSModeID\]</span><span class="sxs-lookup"><span data-stu-id="1fe33-108">*agent ***.Characters ("*** CharacterID\*\*\*").TTSModeID*\* \[ = *ModeID*\]</span></span>



| <span data-ttu-id="1fe33-109">Parte</span><span class="sxs-lookup"><span data-stu-id="1fe33-109">Part</span></span>     | <span data-ttu-id="1fe33-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="1fe33-110">Description</span></span>                                                             |
|----------|-------------------------------------------------------------------------|
| <span data-ttu-id="1fe33-111">*ModeID*</span><span class="sxs-lookup"><span data-stu-id="1fe33-111">*ModeID*</span></span> | <span data-ttu-id="1fe33-112">Espressione stringa che corrisponde all'ID modalità di un motore vocale.</span><span class="sxs-lookup"><span data-stu-id="1fe33-112">A string expression that corresponds to the mode ID of a speech engine.</span></span> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="1fe33-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="1fe33-113">Remarks</span></span>

<span data-ttu-id="1fe33-114">Questa proprietà determina l'ID della modalità del motore TTS (sintesi vocale) per l'output parlato di un carattere.</span><span class="sxs-lookup"><span data-stu-id="1fe33-114">This property determines the TTS (text-to-speech) engine mode ID for a character's spoken output.</span></span> <span data-ttu-id="1fe33-115">L'ID modalità per un motore TTS è una stringa formattata definita dal fornitore vocale che identifica in modo univoco la modalità del motore.</span><span class="sxs-lookup"><span data-stu-id="1fe33-115">The mode ID for a TTS engine is a formatted string defined by the speech vendor that uniquely identifies the engine's mode.</span></span> <span data-ttu-id="1fe33-116">Per altre informazioni, vedere [accesso a un motore di riconoscimento vocale nel codice](accessing-a-speech-engine-in-your-code.md).</span><span class="sxs-lookup"><span data-stu-id="1fe33-116">For more information, see [Accessing a Speech Engine in Your Code](accessing-a-speech-engine-in-your-code.md).</span></span>

<span data-ttu-id="1fe33-117">L'impostazione di questa proprietà esegue l'override del tentativo del server di caricare un motore in base all'impostazione TTS compilata del carattere e all'impostazione [**LanguageID**](languageid-property.md) corrente del carattere.</span><span class="sxs-lookup"><span data-stu-id="1fe33-117">Setting this property overrides the server's attempt to load an engine based on the character's compiled TTS setting and the character's current [**LanguageID**](languageid-property.md) setting.</span></span> <span data-ttu-id="1fe33-118">Tuttavia, se si specifica un ID modalità per un motore che non è installato o se l'utente ha disabilitato l'output vocale nella finestra delle proprietà dell'agente Microsoft (**AudioOutput. Enabled = false**), il server genera un errore.</span><span class="sxs-lookup"><span data-stu-id="1fe33-118">However, if you specify a mode ID for an engine that isn't installed or if the user has disabled speech output in the Microsoft Agent property sheet (**AudioOutput.Enabled = False**), the server raises an error.</span></span>

<span data-ttu-id="1fe33-119">In caso contrario, impostare un ID modalità TTS per il carattere, il server verificherà se l'impostazione della modalità TTS compilata del carattere corrisponde all'impostazione [**LanguageID**](languageid-property.md) del carattere e che il motore TTS associato sia installato.</span><span class="sxs-lookup"><span data-stu-id="1fe33-119">If you do not (or have not successfully) set a TTS mode ID for the character, the server checks to see if the character's compiled TTS mode setting matches the character's [**LanguageID**](languageid-property.md) setting, and that the associated TTS engine is installed.</span></span> <span data-ttu-id="1fe33-120">In tal caso, la modalità TTS utilizzata dal carattere per l'output parlato e questa proprietà restituisce tale ID modalità.</span><span class="sxs-lookup"><span data-stu-id="1fe33-120">If so, the TTS mode used by the character for spoken output and this property returns that mode ID.</span></span> <span data-ttu-id="1fe33-121">In caso contrario, il server richiede un motore di riconoscimento vocale SAPI compatibile che corrisponde al **LanguageID** del carattere, nonché il genere e l'età impostati per l'ID modalità compilata del carattere.</span><span class="sxs-lookup"><span data-stu-id="1fe33-121">If not, the server requests a compatible SAPI speech engine that matches the **LanguageID** of the character, as well as the gender and age set for the character's compiled mode ID.</span></span> <span data-ttu-id="1fe33-122">Se il **LanguageID** del carattere non è stato impostato, il relativo **LanguageID** è la lingua dell'utente corrente.</span><span class="sxs-lookup"><span data-stu-id="1fe33-122">If you have not set the character's **LanguageID**, its **LanguageID** is the current user language.</span></span> <span data-ttu-id="1fe33-123">Se non è possibile trovare alcun motore corrispondente, l'esecuzione di una query per questa proprietà restituisce una stringa vuota per l'ID modalità del motore.</span><span class="sxs-lookup"><span data-stu-id="1fe33-123">If no matching engine can be found, querying for this property returns an empty string for the engine's mode ID.</span></span> <span data-ttu-id="1fe33-124">Analogamente, se si esegue una query su questa proprietà quando l'utente ha disabilitato l'output vocale nella finestra delle proprietà dell'agente Microsoft (**AudioOutput. Enabled = false**), il valore sarà una stringa vuota.</span><span class="sxs-lookup"><span data-stu-id="1fe33-124">Similarly, if you query this property when the user has disabled speech output in the Microsoft Agent property sheet (**AudioOutput.Enabled = False**), the value will be an empty string.</span></span>

<span data-ttu-id="1fe33-125">Se si esegue una query o si imposta questa proprietà, il motore associato verrà caricato (se non è già stato caricato).</span><span class="sxs-lookup"><span data-stu-id="1fe33-125">Querying or setting this property will load the associated engine (if it is not already loaded).</span></span> <span data-ttu-id="1fe33-126">Tuttavia, se il motore specificato nell'impostazione di TTS compilata del carattere è installato e corrisponde all'impostazione dell'ID lingua del carattere, il motore verrà caricato quando viene caricato il carattere.</span><span class="sxs-lookup"><span data-stu-id="1fe33-126">However, if the engine specified in the character's compiled TTS setting is installed and matches the character's language ID setting, the engine will be loaded when the character loads.</span></span>

<span data-ttu-id="1fe33-127">Questa proprietà si applica solo all'utilizzo del carattere da parte dell'applicazione client. l'impostazione non influisce sugli altri client del carattere o di altri caratteri dell'applicazione client.</span><span class="sxs-lookup"><span data-stu-id="1fe33-127">This property applies only to your client application's use of the character; the setting does not affect other clients of the character or other characters of your client application.</span></span>

<span data-ttu-id="1fe33-128">I requisiti del motore vocale di Microsoft Agent sono basati sulla Speech API Microsoft.</span><span class="sxs-lookup"><span data-stu-id="1fe33-128">Microsoft Agent's speech engine requirements are based on the Microsoft Speech API.</span></span> <span data-ttu-id="1fe33-129">I motori che supportano i requisiti di SAPI di Microsoft Agent possono essere installati e usati con Agent.</span><span class="sxs-lookup"><span data-stu-id="1fe33-129">Engines supporting Microsoft Agent's SAPI requirements can be installed and used with Agent.</span></span>

> [!Note]  
> <span data-ttu-id="1fe33-130">Questa proprietà restituisce anche la stringa vuota se nel sistema non è installato alcun supporto audio compatibile.</span><span class="sxs-lookup"><span data-stu-id="1fe33-130">This property also returns the empty string if you have no compatible sound support installed on your system.</span></span>

 

> [!Note]  
> <span data-ttu-id="1fe33-131">L'impostazione di **TTSModeID** può avere esito negativo se Speech.dll non è installato e il motore specificato non corrisponde all'impostazione della modalità TTS compilata del carattere.</span><span class="sxs-lookup"><span data-stu-id="1fe33-131">Setting the **TTSModeID** can fail if Speech.dll is not installed and the engine you specify does not match the character's compiled TTS mode setting.</span></span>

 

> [!Note]  
> <span data-ttu-id="1fe33-132">L'esecuzione di query su questa proprietà in genere non restituisce un errore.</span><span class="sxs-lookup"><span data-stu-id="1fe33-132">Querying this property does not typically return an error.</span></span> <span data-ttu-id="1fe33-133">Tuttavia, se il tempo di caricamento del motore vocale richiede un tempo insolitamente lungo, potrebbe essere presente un errore che indica che si è verificato il timeout della query.</span><span class="sxs-lookup"><span data-stu-id="1fe33-133">However, if the speech engine takes an abnormally long time to load, you may get an error indicating that the query timed out.</span></span>

 

## <a name="see-also"></a><span data-ttu-id="1fe33-134">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="1fe33-134">See Also</span></span>

[<span data-ttu-id="1fe33-135">**Proprietà LanguageID**</span><span class="sxs-lookup"><span data-stu-id="1fe33-135">**LanguageID property**</span></span>](languageid-property.md)


 

 




