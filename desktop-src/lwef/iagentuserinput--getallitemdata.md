---
title: IAgentUserInput GetAllItemData
description: IAgentUserInput GetAllItemData
ms.assetid: d1857b28-c745-4ed2-b49e-774f247e7348
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ced6a618d4fbbc093bf54c19fc393b7e195f2069
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104470742"
---
# <a name="iagentuserinputgetallitemdata"></a><span data-ttu-id="b354a-103">IAgentUserInput::GetAllItemData</span><span class="sxs-lookup"><span data-stu-id="b354a-103">IAgentUserInput::GetAllItemData</span></span>

<span data-ttu-id="b354a-104">\[Microsoft Agent è stato deprecato a partire da Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="b354a-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT GetAllItemData(
   VARIANT * pdwItemIndices,  // address of variable for alternative IDs
   VARIANT * plConfidences,   // address of variable for confidence scores
   VARIANT * pbszText         // address of variable for voice text
);
```

<span data-ttu-id="b354a-105">Recupera i dati per tutte le alternative di [**comando**](command-event.md) passate a un callback [**IAgentNotifySink:: Command**](iagentnotifysink--command.md) .</span><span class="sxs-lookup"><span data-stu-id="b354a-105">Retrieves the data for all [**Command**](command-event.md) alternatives passed to an [**IAgentNotifySink::Command**](iagentnotifysink--command.md) callback.</span></span>

-   <span data-ttu-id="b354a-106">Restituisce \_ OK per indicare che l'operazione è stata completata.</span><span class="sxs-lookup"><span data-stu-id="b354a-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="b354a-107"><span id="pdwItemIndices"></span><span id="pdwitemindices"></span><span id="PDWITEMINDICES"></span>*pdwItemIndices*</span><span class="sxs-lookup"><span data-stu-id="b354a-107"><span id="pdwItemIndices"></span><span id="pdwitemindices"></span><span id="PDWITEMINDICES"></span>*pdwItemIndices*</span></span>
</dt> <dd>

<span data-ttu-id="b354a-108">Indirizzo di una variabile che riceve gli ID dei [**comandi**](command-event.md) passati al callback [**IAgentNotifySink:: Command**](iagentnotifysink--command.md) .</span><span class="sxs-lookup"><span data-stu-id="b354a-108">Address of a variable that receives the IDs of [**Commands**](command-event.md) passed to the [**IAgentNotifySink::Command**](iagentnotifysink--command.md) callback.</span></span>

</dd> <dt>

<span data-ttu-id="b354a-109"><span id="plConfidences"></span><span id="plconfidences"></span><span id="PLCONFIDENCES"></span>*plConfidences*</span><span class="sxs-lookup"><span data-stu-id="b354a-109"><span id="plConfidences"></span><span id="plconfidences"></span><span id="PLCONFIDENCES"></span>*plConfidences*</span></span>
</dt> <dd>

<span data-ttu-id="b354a-110">Indirizzo di una variabile che riceve i punteggi di confidenza per le alternative del [**comando**](command-event.md) passate al callback [**IAgentNotifySink:: Command**](iagentnotifysink--command.md) .</span><span class="sxs-lookup"><span data-stu-id="b354a-110">Address of a variable that receives the confidence scores for [**Command**](command-event.md) alternatives passed to the [**IAgentNotifySink::Command**](iagentnotifysink--command.md) callback.</span></span>

</dd> <dt>

<span data-ttu-id="b354a-111"><span id="pbszText"></span><span id="pbsztext"></span><span id="PBSZTEXT"></span>*pbszText*</span><span class="sxs-lookup"><span data-stu-id="b354a-111"><span id="pbszText"></span><span id="pbsztext"></span><span id="PBSZTEXT"></span>*pbszText*</span></span>
</dt> <dd>

<span data-ttu-id="b354a-112">Indirizzo di una variabile che riceve il testo vocale per le alternative del [**comando**](command-event.md) passate al callback [**IAgentNotifySink:: Command**](iagentnotifysink--command.md) .</span><span class="sxs-lookup"><span data-stu-id="b354a-112">Address of a variable that receives the voice text for [**Command**](command-event.md) alternatives passed to the [**IAgentNotifySink::Command**](iagentnotifysink--command.md) callback.</span></span>

</dd> </dl>

<span data-ttu-id="b354a-113">Se l'input vocale attiva [**IAgentNotifySink:: Command**](iagentnotifysink--command.md), il server restituisce la migliore corrispondenza, la seconda corrispondenza migliore e la terza corrispondenza migliore, se vengono fornite dal motore di riconoscimento vocale.</span><span class="sxs-lookup"><span data-stu-id="b354a-113">If speech input triggers [**IAgentNotifySink::Command**](iagentnotifysink--command.md), the server returns the best match, the second-best match, and the third-best match, if these are provided by the speech engine.</span></span> <span data-ttu-id="b354a-114">Fornisce i punteggi di confidenza relativi, nell'intervallo da-100 a 100 e il testo effettivo "sentito" dal motore di riconoscimento vocale.</span><span class="sxs-lookup"><span data-stu-id="b354a-114">It provides the relative confidence scores, in the range of -100 to 100, and actual text "heard" by the speech engine.</span></span> <span data-ttu-id="b354a-115">Se la corrispondenza migliore era un comando fornito dal server, il server invia un ID NULL, ma invia comunque un punteggio di confidenza e il testo [**vocale**](voice-property.md) .</span><span class="sxs-lookup"><span data-stu-id="b354a-115">If the best match was a server-supplied command, the server sends a NULL ID, but still sends a confidence score and the [**Voice**](voice-property.md) text.</span></span>

<span data-ttu-id="b354a-116">Se l'input vocale non è l'origine dell'evento. Se, ad esempio, l'utente ha selezionato il comando dal menu popup del carattere, il server Microsoft Agent restituisce l'ID del [**comando**](command-event.md) selezionato, con un punteggio di confidenza pari a 100 e il testo vocale come null.</span><span class="sxs-lookup"><span data-stu-id="b354a-116">If speech input was not the source for the event; for example, if the user selected the command from the character's pop-up menu, the Microsoft Agent server returns the ID of the [**Command**](command-event.md) selected, with a confidence score of 100 and voice text as NULL.</span></span> <span data-ttu-id="b354a-117">Le altre alternative restituiscono come NULL con i punteggi di confidenza pari a zero (0) e il testo vocale come NULL.</span><span class="sxs-lookup"><span data-stu-id="b354a-117">The other alternatives return as NULL with confidence scores of zero (0) and voice text as NULL.</span></span>

> [!Note]  
> <span data-ttu-id="b354a-118">Non tutti i motori di riconoscimento vocale possono restituire tutti i valori per tutti i parametri di questo evento.</span><span class="sxs-lookup"><span data-stu-id="b354a-118">Not all speech recognition engines may return all the values for all the parameters of this event.</span></span> <span data-ttu-id="b354a-119">Rivolgersi al fornitore del motore per determinare se il motore supporta l'interfaccia di Microsoft Speech API per la restituzione di alternative e punteggi di confidenza.</span><span class="sxs-lookup"><span data-stu-id="b354a-119">Check with your engine vendor to determine whether the engine supports the Microsoft Speech API interface for returning alternatives and confidence scores.</span></span>

 

## <a name="see-also"></a><span data-ttu-id="b354a-120">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="b354a-120">See Also</span></span>

<span data-ttu-id="b354a-121">[**IAgentUserInput:: GetItemConfidence**](iagentuserinput--getitemconfidence.md), [**IAgentUserInput:: GetItemText**](iagentuserinput--getitemtext.md), [**IAgentUserInput:: GetItemID**](iagentuserinput--getitemid.md)</span><span class="sxs-lookup"><span data-stu-id="b354a-121">[**IAgentUserInput::GetItemConfidence**](iagentuserinput--getitemconfidence.md), [**IAgentUserInput::GetItemText**](iagentuserinput--getitemtext.md), [**IAgentUserInput::GetItemID**](iagentuserinput--getitemid.md)</span></span>


 

 




