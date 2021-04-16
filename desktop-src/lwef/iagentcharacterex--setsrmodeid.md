---
title: IAgentCharacterEx SetSRModeID
description: IAgentCharacterEx SetSRModeID
ms.assetid: 8f9072ec-1f64-4f5c-972d-cd6799ce028c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 390d7e0126fe5ef62273cf6d7d23ada25c26bbdb
ms.sourcegitcommit: 3e70ae762629e244028b437420ed50b5850db4e3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/20/2020
ms.locfileid: "104472259"
---
# <a name="iagentcharacterexsetsrmodeid"></a><span data-ttu-id="c7ba3-103">IAgentCharacterEx::SetSRModeID</span><span class="sxs-lookup"><span data-stu-id="c7ba3-103">IAgentCharacterEx::SetSRModeID</span></span>

<span data-ttu-id="c7ba3-104">\[Microsoft Agent è stato deprecato a partire da Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="c7ba3-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT SetSRModeID(
   BSTR bszModeID  // speech recognition engine ID
);
```

<span data-ttu-id="c7ba3-105">Imposta l'ID modalità del motore di riconoscimento vocale impostato per il carattere.</span><span class="sxs-lookup"><span data-stu-id="c7ba3-105">Sets the mode ID of the speech recognition engine set for the character.</span></span>

-   <span data-ttu-id="c7ba3-106">Restituisce \_ OK per indicare che l'operazione è stata completata.</span><span class="sxs-lookup"><span data-stu-id="c7ba3-106">Returns S\_OK to indicate the operation was successful.</span></span>

<span data-ttu-id="c7ba3-107">bszModeID</span><span class="sxs-lookup"><span data-stu-id="c7ba3-107">bszModeID</span></span>

<span data-ttu-id="c7ba3-108">Impostazione dell'ID modalità del motore di riconoscimento vocale per il carattere.</span><span class="sxs-lookup"><span data-stu-id="c7ba3-108">The mode ID setting of the speech recognition engine for the character.</span></span>

<span data-ttu-id="c7ba3-109">Questa impostazione imposta il motore per l'input vocale di un carattere.</span><span class="sxs-lookup"><span data-stu-id="c7ba3-109">This setting sets the engine for a character's speech input.</span></span> <span data-ttu-id="c7ba3-110">L'ID modalità per un motore di riconoscimento vocale è il GUID definito dal fornitore vocale che identifica in modo univoco la modalità del motore (formattato con parentesi graffe e trattini).</span><span class="sxs-lookup"><span data-stu-id="c7ba3-110">The mode ID for a speech recognition engine is the GUID defined by the speech vendor that uniquely identifies the engine's mode (formatted with braces and dashes).</span></span> <span data-ttu-id="c7ba3-111">Per ulteriori informazioni, vedere la [documentazione di Microsoft Speech SDK](https://msdn.microsoft.com/library/ee705648.aspx).</span><span class="sxs-lookup"><span data-stu-id="c7ba3-111">For more information, see the [Microsoft Speech SDK documentation](https://msdn.microsoft.com/library/ee705648.aspx).</span></span>

<span data-ttu-id="c7ba3-112">Se si specifica un ID modalità che non corrisponde all'impostazione della lingua del carattere, se l'utente ha disabilitato il riconoscimento vocale (nella finestra delle proprietà di Microsoft Agent) o se il motore non è installato, la chiamata avrà esito negativo.</span><span class="sxs-lookup"><span data-stu-id="c7ba3-112">If you specify a mode ID that does not match the character's language setting, if the user has disabled speech recognition (in the Microsoft Agent property sheet), or the engine is not installed, this call will fail.</span></span> <span data-ttu-id="c7ba3-113">Se non si imposta un ID modalità del motore di riconoscimento vocale per il carattere, il server ne imposta uno che corrisponde all'impostazione della lingua del carattere (usando le interfacce Speech API Microsoft).</span><span class="sxs-lookup"><span data-stu-id="c7ba3-113">If you do not set a speech recognition engine mode ID for the character, the server sets one that matches the character's language setting (using Microsoft Speech API interfaces).</span></span>

<span data-ttu-id="c7ba3-114">Quando l'input vocale è abilitato nella finestra delle proprietà dell'agente (Opzioni carattere avanzate), l'impostazione di questa proprietà caricherà il motore associato (se non è già caricato) e avvierà servizi vocali.</span><span class="sxs-lookup"><span data-stu-id="c7ba3-114">When speech input is enabled in the Agent property sheet (Advanced Character Options), setting this property will load the associated engine (if it is not already loaded), and start speech services.</span></span> <span data-ttu-id="c7ba3-115">Ovvero, la chiave di ascolto è disponibile e il suggerimento di ascolto è visualizzabile.</span><span class="sxs-lookup"><span data-stu-id="c7ba3-115">That is, the Listening key is available, and the Listening Tip is displayable.</span></span> <span data-ttu-id="c7ba3-116">(Il tasto di attesa e il suggerimento di ascolto sono abilitati solo se sono abilitati anche nelle opzioni dei caratteri avanzati). Tuttavia, se si esegue una query sulla proprietà quando la voce Speech è disabilitata, il server non avvia i servizi di riconoscimento vocale.</span><span class="sxs-lookup"><span data-stu-id="c7ba3-116">(The Listening key and Listening tip are enabled only if they are also enabled in Advanced Character Options.) However, if you query the property when speech is disabled, the server does not start speech services.</span></span>

<span data-ttu-id="c7ba3-117">Questa proprietà si applica solo al client del carattere; l'impostazione non riflette l'impostazione per altri client del carattere o di altri caratteri del client.</span><span class="sxs-lookup"><span data-stu-id="c7ba3-117">This property applies to only the client of the character; the setting does not reflect the setting for other clients of the character or other characters of the client.</span></span>

<span data-ttu-id="c7ba3-118">I requisiti del motore vocale di Microsoft Agent sono basati sulla Speech API Microsoft.</span><span class="sxs-lookup"><span data-stu-id="c7ba3-118">Microsoft Agent's speech engine requirements are based on the Microsoft Speech API.</span></span> <span data-ttu-id="c7ba3-119">I motori che supportano i requisiti di SAPI di Microsoft Agent possono essere installati e usati con Agent.</span><span class="sxs-lookup"><span data-stu-id="c7ba3-119">Engines supporting Microsoft Agent's SAPI requirements can be installed and used with Agent.</span></span>

## <a name="see-also"></a><span data-ttu-id="c7ba3-120">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="c7ba3-120">See Also</span></span>

[<span data-ttu-id="c7ba3-121">**IAgentCharacterEx::GetSRModeID**</span><span class="sxs-lookup"><span data-stu-id="c7ba3-121">**IAgentCharacterEx::GetSRModeID**</span></span>](iagentcharacterex--getsrmodeid.md)


 

 




