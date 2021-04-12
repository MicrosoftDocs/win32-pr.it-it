---
title: IAgentCharacterEx SetTTSModeID
description: IAgentCharacterEx SetTTSModeID
ms.assetid: 66ed792a-1693-45dc-b9a8-eebe772c5af9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 34392e65fcb8f3a46db6251f01f59ad76aba278d
ms.sourcegitcommit: 3e70ae762629e244028b437420ed50b5850db4e3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/20/2020
ms.locfileid: "104398682"
---
# <a name="iagentcharacterexsetttsmodeid"></a><span data-ttu-id="cad57-103">IAgentCharacterEx::SetTTSModeID</span><span class="sxs-lookup"><span data-stu-id="cad57-103">IAgentCharacterEx::SetTTSModeID</span></span>

<span data-ttu-id="cad57-104">\[Microsoft Agent è stato deprecato a partire da Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="cad57-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT SetTTSModeID(
   BSTR bszModeID  // TTS engine ID
);
```

<span data-ttu-id="cad57-105">Imposta l'ID modalità del set di motori TTS per il carattere.</span><span class="sxs-lookup"><span data-stu-id="cad57-105">Sets the mode ID of the TTS engine set for the character.</span></span>

-   <span data-ttu-id="cad57-106">Restituisce \_ OK per indicare che l'operazione è stata completata.</span><span class="sxs-lookup"><span data-stu-id="cad57-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="cad57-107"><span id="bszModeID"></span><span id="bszmodeid"></span><span id="BSZMODEID"></span>*bszModeID*</span><span class="sxs-lookup"><span data-stu-id="cad57-107"><span id="bszModeID"></span><span id="bszmodeid"></span><span id="BSZMODEID"></span>*bszModeID*</span></span>
</dt> <dd>

<span data-ttu-id="cad57-108">Impostazione dell'ID modalità del motore TTS per il carattere.</span><span class="sxs-lookup"><span data-stu-id="cad57-108">The mode ID setting of the TTS engine for the character.</span></span>

> [!Note]  
> <span data-ttu-id="cad57-109">**IAgentCharacterEx: SetTTSModeID** può avere esito negativo se Speech.dll non è installato e il motore specificato non corrisponde all'impostazione della modalità TTS compilata del carattere.</span><span class="sxs-lookup"><span data-stu-id="cad57-109">**IAgentCharacterEx:SetTTSModeID** can fail if Speech.dll is not installed and the engine you specify does not match the character's compiled TTS mode setting.</span></span>

 

</dd> </dl>

<span data-ttu-id="cad57-110">Questa impostazione determina la modalità del motore preferenziale per l'output TTS vocale di un carattere.</span><span class="sxs-lookup"><span data-stu-id="cad57-110">This setting determines the preferred engine mode for a character's spoken TTS output.</span></span> <span data-ttu-id="cad57-111">L'ID modalità per un motore di sintesi vocale è il GUID definito dal fornitore di riconoscimento vocale che identifica in modo univoco la modalità del motore (formattato con parentesi graffe e trattini).</span><span class="sxs-lookup"><span data-stu-id="cad57-111">The mode ID for a TTS (text-to-speech) engine is the GUID defined by the speech vendor that uniquely identifies the mode of the engine (formatted with braces and dashes).</span></span> <span data-ttu-id="cad57-112">Per ulteriori informazioni, vedere la [documentazione di Microsoft Speech SDK](https://msdn.microsoft.com/library/ee705648.aspx).</span><span class="sxs-lookup"><span data-stu-id="cad57-112">For more information, see the [Microsoft Speech SDK documentation](https://msdn.microsoft.com/library/ee705648.aspx).</span></span>

<span data-ttu-id="cad57-113">Se si imposta un ID modalità TTS, viene eseguito l'override del tentativo del server di trovare la corrispondenza con un motore di riconoscimento vocale basato sull'ID della modalità TTS compilata del carattere, sull'ID lingua del sistema corrente e sull'ID lingua corrente del carattere.</span><span class="sxs-lookup"><span data-stu-id="cad57-113">If you set a TTS mode ID, it overrides the server attempt to match a speech engine based on the character's compiled TTS mode ID, the current system language ID, and the character's current language ID.</span></span> <span data-ttu-id="cad57-114">Tuttavia, se si tenta di impostare un ID modalità quando l'utente ha disabilitato l'output vocale nella finestra delle proprietà dell'agente Microsoft o quando il motore associato non è installato, la chiamata avrà esito negativo.</span><span class="sxs-lookup"><span data-stu-id="cad57-114">However, if you attempt to set a mode ID when the user has disabled speech output in the Microsoft Agent property sheet or when the associated engine is not installed, this call will fail.</span></span>

<span data-ttu-id="cad57-115">Se non si imposta un ID modalità motore di TTS per il carattere, il server imposta un motore che corrisponde all'impostazione della lingua del carattere (mediante interfacce Speech API Microsoft).</span><span class="sxs-lookup"><span data-stu-id="cad57-115">If you do not set a TTS engine mode ID for the character, the server sets an engine that matches the character's language setting (using Microsoft Speech API interfaces).</span></span> <span data-ttu-id="cad57-116">Se si imposta questa proprietà, il motore associato verrà caricato se non è già caricato.</span><span class="sxs-lookup"><span data-stu-id="cad57-116">Setting this property will load the associated engine if it is not already loaded.</span></span>

<span data-ttu-id="cad57-117">Questa proprietà si applica solo all'utilizzo del carattere da parte dell'applicazione client. l'impostazione non influisce sugli altri client del carattere o di altri caratteri dell'applicazione client.</span><span class="sxs-lookup"><span data-stu-id="cad57-117">This property applies to only your client application's use of the character; the setting does not affect other clients of the character or other characters of your client application.</span></span>

<span data-ttu-id="cad57-118">I requisiti del motore vocale di Microsoft Agent sono basati sulla Speech API Microsoft.</span><span class="sxs-lookup"><span data-stu-id="cad57-118">Microsoft Agent's speech engine requirements are based on the Microsoft Speech API.</span></span> <span data-ttu-id="cad57-119">I motori che supportano i requisiti di SAPI di Microsoft Agent possono essere installati e usati con Agent.</span><span class="sxs-lookup"><span data-stu-id="cad57-119">Engines supporting Microsoft Agent's SAPI requirements can be installed and used with Agent.</span></span>

## <a name="see-also"></a><span data-ttu-id="cad57-120">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="cad57-120">See Also</span></span>

[<span data-ttu-id="cad57-121">**IAgentCharacterEx:GetTTSModeID**</span><span class="sxs-lookup"><span data-stu-id="cad57-121">**IAgentCharacterEx:GetTTSModeID**</span></span>](iagentcharacterex--getttsmodeid.md)


 

 




