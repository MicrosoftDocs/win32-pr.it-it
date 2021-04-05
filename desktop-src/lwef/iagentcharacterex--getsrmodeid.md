---
title: IAgentCharacterEx GetSRModeID
description: IAgentCharacterEx GetSRModeID
ms.assetid: 28049680-8245-49f3-9ecd-13c7605f10ed
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e0bba237fb1bc1b5d769f7e8ecf983b58718c18e
ms.sourcegitcommit: 3e70ae762629e244028b437420ed50b5850db4e3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/20/2020
ms.locfileid: "103723814"
---
# <a name="iagentcharacterexgetsrmodeid"></a><span data-ttu-id="0d30d-103">IAgentCharacterEx::GetSRModeID</span><span class="sxs-lookup"><span data-stu-id="0d30d-103">IAgentCharacterEx::GetSRModeID</span></span>

<span data-ttu-id="0d30d-104">\[Microsoft Agent è stato deprecato a partire da Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="0d30d-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT GetSRModeID(
   BSTR * pbszModeID  // address of speech recognition engine ID
);
```

<span data-ttu-id="0d30d-105">Recupera l'ID modalità del motore di riconoscimento vocale impostato per il carattere.</span><span class="sxs-lookup"><span data-stu-id="0d30d-105">Retrieves the mode ID of the speech recognition engine set for the character.</span></span>

-   <span data-ttu-id="0d30d-106">Restituisce \_ OK per indicare che l'operazione è stata completata.</span><span class="sxs-lookup"><span data-stu-id="0d30d-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="0d30d-107"><span id="pbszModeID"></span><span id="pbszmodeid"></span><span id="PBSZMODEID"></span>*pbszModeID*</span><span class="sxs-lookup"><span data-stu-id="0d30d-107"><span id="pbszModeID"></span><span id="pbszmodeid"></span><span id="PBSZMODEID"></span>*pbszModeID*</span></span>
</dt> <dd>

<span data-ttu-id="0d30d-108">Indirizzo di un BSTR che riceve l'impostazione dell'ID modalità del motore di riconoscimento vocale per il carattere.</span><span class="sxs-lookup"><span data-stu-id="0d30d-108">Address of a BSTR that receives the mode ID setting of the speech recognition engine for the character.</span></span>

</dd> </dl>

<span data-ttu-id="0d30d-109">Questa impostazione restituisce il motore impostato per l'input vocale di un carattere.</span><span class="sxs-lookup"><span data-stu-id="0d30d-109">This setting returns the engine set for a character's speech input.</span></span> <span data-ttu-id="0d30d-110">L'ID modalità per un motore di riconoscimento vocale è una rappresentazione in forma di stringa del GUID (formattato con parentesi graffe e trattini) dal fornitore di sintesi vocale che identifica in modo univoco il motore.</span><span class="sxs-lookup"><span data-stu-id="0d30d-110">The mode ID for a speech recognition engine is a string representation of the GUID (formatted with braces and dashes) by the speech vendor uniquely identifying the engine.</span></span> <span data-ttu-id="0d30d-111">Per ulteriori informazioni, vedere la [documentazione di Microsoft Speech SDK](https://msdn.microsoft.com/library/ee705648.aspx).</span><span class="sxs-lookup"><span data-stu-id="0d30d-111">For more information, see the [Microsoft Speech SDK documentation](https://msdn.microsoft.com/library/ee705648.aspx).</span></span>

<span data-ttu-id="0d30d-112">Se non si imposta un ID modalità del motore di riconoscimento vocale per il carattere, il server restituisce un motore che corrisponde all'impostazione della lingua del carattere (usando le interfacce Speech API Microsoft).</span><span class="sxs-lookup"><span data-stu-id="0d30d-112">If you do not set a speech recognition engine mode ID for the character, the server returns an engine that matches the character's language setting (using Microsoft Speech API interfaces).</span></span> <span data-ttu-id="0d30d-113">Se non è disponibile alcun motore di riconoscimento vocale corrispondente per il carattere, il server restituisce una stringa null (vuota).</span><span class="sxs-lookup"><span data-stu-id="0d30d-113">If there is no matching speech recognition engine available for the character, the server returns a null (empty) string.</span></span>

<span data-ttu-id="0d30d-114">Quando l'input vocale è abilitato (nella finestra Opzioni carattere avanzato), l'esecuzione di una query o l'impostazione di questa proprietà caricherà il motore associato (se non è già caricato) e avvierà servizi vocali.</span><span class="sxs-lookup"><span data-stu-id="0d30d-114">When speech input is enabled (in the Advanced Character Options window), querying or setting this property will load the associated engine (if it is not already loaded), and start speech services.</span></span> <span data-ttu-id="0d30d-115">Ovvero, la chiave di ascolto è disponibile e il suggerimento di ascolto è visualizzabile.</span><span class="sxs-lookup"><span data-stu-id="0d30d-115">That is, the Listening key is available, and the Listening Tip is displayable.</span></span> <span data-ttu-id="0d30d-116">(Il tasto di attesa e il suggerimento di ascolto sono abilitati solo se sono abilitati anche nelle opzioni dei caratteri avanzati). Tuttavia, se si esegue una query sulla proprietà quando la voce Speech è disabilitata, il server non avvia servizi vocali e restituisce una stringa null (stringa vuota).</span><span class="sxs-lookup"><span data-stu-id="0d30d-116">(The Listening key and Listening Tip are enabled only if they are also enabled in Advanced Character Options.) However, if you query the property when speech is disabled, the server does not start speech services and it returns a null string (empty string).</span></span>

<span data-ttu-id="0d30d-117">Questa funzione restituisce solo l'impostazione per l'uso del carattere da parte dell'applicazione client. l'impostazione non riflette altri client del carattere o di altri caratteri dell'applicazione client.</span><span class="sxs-lookup"><span data-stu-id="0d30d-117">This function returns only the setting for your client application's use of the character; the setting does not reflect other clients of the character or other characters of your client application.</span></span>

<span data-ttu-id="0d30d-118">Questa funzione non ha esito negativo se [**IAgentSpeechInputProperties:: GetEnabled**](iagentspeechinputproperties--getenabled.md) restituisce **false**.</span><span class="sxs-lookup"><span data-stu-id="0d30d-118">This function does not fail if the [**IAgentSpeechInputProperties::GetEnabled**](iagentspeechinputproperties--getenabled.md) returns **False**.</span></span>

<span data-ttu-id="0d30d-119">I requisiti del motore vocale di Microsoft Agent sono basati sulla Speech API Microsoft.</span><span class="sxs-lookup"><span data-stu-id="0d30d-119">Microsoft Agent's speech engine requirements are based on the Microsoft Speech API.</span></span> <span data-ttu-id="0d30d-120">I motori che supportano i requisiti di SAPI di Microsoft Agent possono essere installati e usati con Agent.</span><span class="sxs-lookup"><span data-stu-id="0d30d-120">Engines supporting Microsoft Agent's SAPI requirements can be installed and used with Agent.</span></span>

## <a name="see-also"></a><span data-ttu-id="0d30d-121">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="0d30d-121">See Also</span></span>

[<span data-ttu-id="0d30d-122">**IAgentCharacterEx::SetSRModeID**</span><span class="sxs-lookup"><span data-stu-id="0d30d-122">**IAgentCharacterEx::SetSRModeID**</span></span>](iagentcharacterex--setsrmodeid.md)


 

 




