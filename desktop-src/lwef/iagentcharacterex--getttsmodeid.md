---
title: IAgentCharacterEx GetTTSModeID
description: IAgentCharacterEx GetTTSModeID
ms.assetid: e7b3c576-dc3c-40de-8d09-8e7f4b79250b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 62a77e78755345c0993ed5723080b0b3f4b8297a
ms.sourcegitcommit: 3e70ae762629e244028b437420ed50b5850db4e3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/20/2020
ms.locfileid: "104046385"
---
# <a name="iagentcharacterexgetttsmodeid"></a><span data-ttu-id="3199e-103">IAgentCharacterEx::GetTTSModeID</span><span class="sxs-lookup"><span data-stu-id="3199e-103">IAgentCharacterEx::GetTTSModeID</span></span>

<span data-ttu-id="3199e-104">\[Microsoft Agent è stato deprecato a partire da Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="3199e-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT GetTTSModeID(
   BSTR * pbszModeID  // address of TTS engine ID
);
```

<span data-ttu-id="3199e-105">Recupera l'ID modalità del set di motori TTS per il carattere.</span><span class="sxs-lookup"><span data-stu-id="3199e-105">Retrieves the mode ID of the TTS engine set for the character.</span></span>

-   <span data-ttu-id="3199e-106">Restituisce \_ OK per indicare che l'operazione è stata completata.</span><span class="sxs-lookup"><span data-stu-id="3199e-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="3199e-107"><span id="pbszModeID"></span><span id="pbszmodeid"></span><span id="PBSZMODEID"></span>*pbszModeID*</span><span class="sxs-lookup"><span data-stu-id="3199e-107"><span id="pbszModeID"></span><span id="pbszmodeid"></span><span id="PBSZMODEID"></span>*pbszModeID*</span></span>
</dt> <dd>

<span data-ttu-id="3199e-108">Indirizzo di un BSTR che riceve l'impostazione dell'ID modalità del motore TTS per il carattere.</span><span class="sxs-lookup"><span data-stu-id="3199e-108">Address of a BSTR that receives the mode ID setting of the TTS engine for the character.</span></span>

</dd> </dl>

<span data-ttu-id="3199e-109">Questa impostazione restituisce l'ID della modalità del motore TTS (sintesi vocale) per l'output parlato di un carattere.</span><span class="sxs-lookup"><span data-stu-id="3199e-109">This setting returns the TTS (text-to-speech) engine mode ID for a character's spoken output.</span></span> <span data-ttu-id="3199e-110">L'ID modalità per un motore TTS è una rappresentazione di stringa del GUID (formattato con parentesi graffe e trattini) definita dal fornitore di riconoscimento vocale che identifica in modo univoco il motore.</span><span class="sxs-lookup"><span data-stu-id="3199e-110">The mode ID for a TTS engine is a string representation of the GUID (formatted with braces and dashes) defined by the speech vendor uniquely identifying the engine.</span></span> <span data-ttu-id="3199e-111">Per ulteriori informazioni, vedere la [documentazione di Microsoft Speech SDK](https://msdn.microsoft.com/library/ee705648.aspx).</span><span class="sxs-lookup"><span data-stu-id="3199e-111">For more information, see the [Microsoft Speech SDK documentation](https://msdn.microsoft.com/library/ee705648.aspx).</span></span> <span data-ttu-id="3199e-112">Se si esegue una query su questa proprietà, il motore associato verrà caricato se non è già caricato.</span><span class="sxs-lookup"><span data-stu-id="3199e-112">Querying this property will load the associated engine if it is not already loaded.</span></span>

<span data-ttu-id="3199e-113">Se non si imposta un ID modalità motore di TTS per il carattere, il server tenta di restituire un motore che corrisponde a (usando le interfacce di Microsoft Speech API) l'impostazione TTS compilata del carattere e l'impostazione della lingua corrente del carattere.</span><span class="sxs-lookup"><span data-stu-id="3199e-113">If you do not set a TTS engine mode ID for the character, the server attempts to return an engine that matches (using Microsoft Speech API interfaces) the character's compiled TTS setting and the character's current language setting.</span></span> <span data-ttu-id="3199e-114">Se sono diversi, l'impostazione della lingua del carattere sostituisce la relativa impostazione della modalità di creazione.</span><span class="sxs-lookup"><span data-stu-id="3199e-114">If these are different, then the character's language setting overrides its authored mode setting.</span></span> <span data-ttu-id="3199e-115">Se l'impostazione della lingua del carattere non è stata impostata, la lingua del carattere è l'ID della lingua predefinita dell'utente e il server tenta la corrispondenza in base a tale ID lingua.</span><span class="sxs-lookup"><span data-stu-id="3199e-115">If you have not set the character's language setting, the character's language is the user default language ID, and the server attempts the match based on that language ID.</span></span>

<span data-ttu-id="3199e-116">Questa funzione non ha esito negativo se [**IAgentAudioObjectProperties:: GetEnabled**](https://www.bing.com/search?q=**IAgentAudioObjectProperties::GetEnabled**) restituisce **false**.</span><span class="sxs-lookup"><span data-stu-id="3199e-116">This function does not fail if the [**IAgentAudioObjectProperties::GetEnabled**](https://www.bing.com/search?q=**IAgentAudioObjectProperties::GetEnabled**) returns **False**.</span></span>

<span data-ttu-id="3199e-117">Questa proprietà si applica solo all'utilizzo del carattere da parte dell'applicazione client. l'impostazione non influisce sugli altri client del carattere o di altri caratteri dell'applicazione client.</span><span class="sxs-lookup"><span data-stu-id="3199e-117">This property applies only to your client application's use of the character; the setting does not affect other clients of the character or other characters of your client application.</span></span>

<span data-ttu-id="3199e-118">I requisiti del motore vocale di Microsoft Agent sono basati sulla Speech API Microsoft.</span><span class="sxs-lookup"><span data-stu-id="3199e-118">Microsoft Agent's speech engine requirements are based on the Microsoft Speech API.</span></span> <span data-ttu-id="3199e-119">I motori che supportano i requisiti di SAPI di Microsoft Agent possono essere installati e usati con Agent.</span><span class="sxs-lookup"><span data-stu-id="3199e-119">Engines supporting Microsoft Agent's SAPI requirements can be installed and used with Agent.</span></span>

## <a name="see-also"></a><span data-ttu-id="3199e-120">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="3199e-120">See Also</span></span>

[<span data-ttu-id="3199e-121">**IAgentCharacterEx::SetTTSModeID**</span><span class="sxs-lookup"><span data-stu-id="3199e-121">**IAgentCharacterEx::SetTTSModeID**</span></span>](iagentcharacterex--setttsmodeid.md)


 

 




