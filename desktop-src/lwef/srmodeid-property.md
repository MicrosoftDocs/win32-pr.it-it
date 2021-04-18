---
title: Proprietà SRModeID
description: Proprietà SRModeID
ms.assetid: 4c784fc5-d2c2-4e5b-ba5f-f59b4507f40f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 898f90a70c29d409eaa12df3d3fde845e35bd5ff
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106298955"
---
# <a name="srmodeid-property"></a><span data-ttu-id="177f2-103">Proprietà SRModeID</span><span class="sxs-lookup"><span data-stu-id="177f2-103">SRModeID Property</span></span>

<span data-ttu-id="177f2-104">\[Microsoft Agent è stato deprecato a partire da Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="177f2-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="177f2-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descrizione**</span><span class="sxs-lookup"><span data-stu-id="177f2-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="177f2-106">Restituisce o imposta il motore di riconoscimento vocale utilizzato dal carattere.</span><span class="sxs-lookup"><span data-stu-id="177f2-106">Returns or sets the speech recognition engine the character uses.</span></span>

</dd> <dt>

<span data-ttu-id="177f2-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintassi**</span><span class="sxs-lookup"><span data-stu-id="177f2-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="177f2-108">\*agente ***. Caratteri ("*** CharacterID \* \* *").* \*  \[  =  *ModeID* SRModeID\]</span><span class="sxs-lookup"><span data-stu-id="177f2-108">*agent ***.Characters("*** CharacterID\*\*\*").SRModeID*\* \[ = *ModeID*\]</span></span>



| <span data-ttu-id="177f2-109">Parte</span><span class="sxs-lookup"><span data-stu-id="177f2-109">Part</span></span>     | <span data-ttu-id="177f2-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="177f2-110">Description</span></span>                                                             |
|----------|-------------------------------------------------------------------------|
| <span data-ttu-id="177f2-111">*ModeID*</span><span class="sxs-lookup"><span data-stu-id="177f2-111">*ModeID*</span></span> | <span data-ttu-id="177f2-112">Espressione stringa che corrisponde all'ID modalità di un motore vocale.</span><span class="sxs-lookup"><span data-stu-id="177f2-112">A string expression that corresponds to the mode ID of a speech engine.</span></span> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="177f2-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="177f2-113">Remarks</span></span>

<span data-ttu-id="177f2-114">La proprietà determina il motore di riconoscimento vocale usato dal carattere per l'input vocale.</span><span class="sxs-lookup"><span data-stu-id="177f2-114">The property determines the speech recognition engine used by the character for speech input.</span></span> <span data-ttu-id="177f2-115">L'ID modalità per un motore di riconoscimento vocale è una stringa formattata definita dal fornitore di sintesi vocale che identifica in modo univoco il motore.</span><span class="sxs-lookup"><span data-stu-id="177f2-115">The mode ID for a speech recognition engine is a formatted string defined by the speech vendor that uniquely identifies the engine.</span></span> <span data-ttu-id="177f2-116">Per altre informazioni, vedere [accesso a un motore di riconoscimento vocale nel codice](accessing-a-speech-engine-in-your-code.md).</span><span class="sxs-lookup"><span data-stu-id="177f2-116">For more information, see [Accessing a Speech Engine In Your Code](accessing-a-speech-engine-in-your-code.md).</span></span>

<span data-ttu-id="177f2-117">Se si specifica un ID modalità per un motore vocale non installato, se l'utente ha disabilitato il riconoscimento vocale (nella finestra delle proprietà di Microsoft Agent) o se la lingua del motore di riconoscimento vocale specificato non corrisponde all'impostazione [**LanguageID**](languageid-property.md) del carattere, il server genera un errore.</span><span class="sxs-lookup"><span data-stu-id="177f2-117">If you specify a mode ID for a speech engine that isn't installed, if the user has disabled speech recognition (in the Microsoft Agent property sheet), or if the language of the specified speech engine doesn't match the character's [**LanguageID**](languageid-property.md) setting, the server raises an error.</span></span>

<span data-ttu-id="177f2-118">Se si esegue una query su questa proprietà e non è stato ancora impostato il motore di riconoscimento vocale, il server restituisce l'ID modalità del motore restituito da SAPI in base all'impostazione [**LanguageID**](languageid-property.md) del carattere.</span><span class="sxs-lookup"><span data-stu-id="177f2-118">If you query this property and haven't already (successfully) set the speech recognition engine, the server returns the mode ID of the engine that SAPI returns based on the character's [**LanguageID**](languageid-property.md) setting.</span></span> <span data-ttu-id="177f2-119">Se il **LanguageID** del carattere non è stato impostato, Agent restituisce l'ID modalità del motore restituito da SAPI in base all'impostazione dell'ID lingua predefinita dell'utente.</span><span class="sxs-lookup"><span data-stu-id="177f2-119">If you haven't set the character's **LanguageID**, then Agent returns the mode ID of the engine that SAPI returns based on the user's default language ID setting.</span></span> <span data-ttu-id="177f2-120">Se non è presente alcun motore corrispondente, il server restituisce una stringa vuota ("").</span><span class="sxs-lookup"><span data-stu-id="177f2-120">If there is no matching engine, the server returns an empty string ("").</span></span> <span data-ttu-id="177f2-121">Per eseguire una query su questa proprietà non è necessario che [**SpeechInput. Enabled**](https://www.bing.com/search?q=**SpeechInput.Enabled**) sia impostato su **true**.</span><span class="sxs-lookup"><span data-stu-id="177f2-121">Querying this property does not require that [**SpeechInput.Enabled**](https://www.bing.com/search?q=**SpeechInput.Enabled**) be set to **True**.</span></span> <span data-ttu-id="177f2-122">Tuttavia, se si esegue una query sulla proprietà quando l'input vocale è disabilitato, il server restituisce una stringa vuota.</span><span class="sxs-lookup"><span data-stu-id="177f2-122">However, if you query the property when speech input is disabled, the server returns an empty string.</span></span>

<span data-ttu-id="177f2-123">Quando l'input vocale è abilitato (nella finestra Opzioni carattere avanzato), l'esecuzione di una query o l'impostazione di questa proprietà caricherà il motore associato (se non è già caricato) e avvierà servizi vocali.</span><span class="sxs-lookup"><span data-stu-id="177f2-123">When speech input is enabled (in the Advanced Character Options window), querying or setting this property will load the associated engine (if it is not already loaded), and start speech services.</span></span> <span data-ttu-id="177f2-124">Ovvero, la chiave di ascolto è disponibile e il suggerimento di ascolto è visualizzabile.</span><span class="sxs-lookup"><span data-stu-id="177f2-124">That is, the Listening key is available, and the Listening Tip is displayable.</span></span> <span data-ttu-id="177f2-125">(Il tasto di attesa e il suggerimento di ascolto sono abilitati solo se sono abilitati anche nelle opzioni dei caratteri avanzati). Tuttavia, se si esegue una query sulla proprietà quando la voce Speech è disabilitata, il server non avvia i servizi di riconoscimento vocale.</span><span class="sxs-lookup"><span data-stu-id="177f2-125">(The Listening key and Listening Tip are enabled only if they are also enabled in Advanced Character Options.) However, if you query the property when speech is disabled, the server does not start speech services.</span></span>

<span data-ttu-id="177f2-126">Questa proprietà si applica solo all'utilizzo del carattere da parte dell'applicazione client. l'impostazione non influisce sugli altri client del carattere o di altri caratteri dell'applicazione client.</span><span class="sxs-lookup"><span data-stu-id="177f2-126">This property applies only to your client application's use of the character; the setting does not affect other clients of the character or other characters of your client application.</span></span>

<span data-ttu-id="177f2-127">I requisiti del motore vocale di Microsoft Agent sono basati sulla Speech API Microsoft.</span><span class="sxs-lookup"><span data-stu-id="177f2-127">Microsoft Agent's speech engine requirements are based on the Microsoft Speech API.</span></span> <span data-ttu-id="177f2-128">I motori che supportano i requisiti di SAPI di Microsoft Agent possono essere installati e usati con Agent.</span><span class="sxs-lookup"><span data-stu-id="177f2-128">Engines supporting Microsoft Agent's SAPI requirements can be installed and used with Agent.</span></span>

> [!Note]  
> <span data-ttu-id="177f2-129">Questa proprietà restituisce anche la stringa vuota se nel sistema non è installato alcun supporto audio compatibile.</span><span class="sxs-lookup"><span data-stu-id="177f2-129">This property also returns the empty string if you have no compatible sound support installed on your system.</span></span>

 

> [!Note]  
> <span data-ttu-id="177f2-130">L'esecuzione di query su questa proprietà in genere non restituisce un errore.</span><span class="sxs-lookup"><span data-stu-id="177f2-130">Querying this property does not typically return an error.</span></span> <span data-ttu-id="177f2-131">Tuttavia, se il tempo di caricamento del motore vocale richiede un tempo insolitamente lungo, potrebbe essere presente un errore che indica che si è verificato il timeout della query.</span><span class="sxs-lookup"><span data-stu-id="177f2-131">However, if the speech engine takes an abnormally long time to load, you may get an error indicating that the query timed out.</span></span>

 

## <a name="see-also"></a><span data-ttu-id="177f2-132">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="177f2-132">See Also</span></span>

[<span data-ttu-id="177f2-133">**Proprietà LanguageID**</span><span class="sxs-lookup"><span data-stu-id="177f2-133">**LanguageID property**</span></span>](languageid-property.md)


 

 




