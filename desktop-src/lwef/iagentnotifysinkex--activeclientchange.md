---
title: IAgentNotifySinkEx ActiveClientChange
description: IAgentNotifySinkEx ActiveClientChange
ms.assetid: e953e803-c898-4c07-adc0-8b895b5e8473
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b96988f80d8a1799bf46f12bd38906e9357453f3
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106298331"
---
# <a name="iagentnotifysinkexactiveclientchange"></a><span data-ttu-id="c0c64-103">IAgentNotifySinkEx::ActiveClientChange</span><span class="sxs-lookup"><span data-stu-id="c0c64-103">IAgentNotifySinkEx::ActiveClientChange</span></span>

<span data-ttu-id="c0c64-104">\[Microsoft Agent è stato deprecato a partire da Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="c0c64-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT ActiveClientChange(
...long dwCharID,  // character ID
   long lStatus    // active state flag
);
```

<span data-ttu-id="c0c64-105">Notifica a un'applicazione client se il client attivo non è più il client attivo di un carattere.</span><span class="sxs-lookup"><span data-stu-id="c0c64-105">Notifies a client application if its active client is no longer the active client of a character.</span></span>

-   <span data-ttu-id="c0c64-106">Nessun valore restituito.</span><span class="sxs-lookup"><span data-stu-id="c0c64-106">No return value.</span></span>

<dl> <dt>

<span data-ttu-id="c0c64-107"><span id="dwCharID"></span><span id="dwcharid"></span><span id="DWCHARID"></span>*dwCharID*</span><span class="sxs-lookup"><span data-stu-id="c0c64-107"><span id="dwCharID"></span><span id="dwcharid"></span><span id="DWCHARID"></span>*dwCharID*</span></span>
</dt> <dd>

<span data-ttu-id="c0c64-108">Identificatore del carattere per il quale lo stato del client attivo è stato modificato.</span><span class="sxs-lookup"><span data-stu-id="c0c64-108">Identifier of the character for which active client status changed.</span></span>

</dd> <dt>

<span data-ttu-id="c0c64-109"><span id="lStatus"></span><span id="lstatus"></span><span id="LSTATUS"></span>*lStatus*</span><span class="sxs-lookup"><span data-stu-id="c0c64-109"><span id="lStatus"></span><span id="lstatus"></span><span id="LSTATUS"></span>*lStatus*</span></span>
</dt> <dd>

<span data-ttu-id="c0c64-110">Modifica dello stato attivo del client, che può essere una combinazione dei valori seguenti:</span><span class="sxs-lookup"><span data-stu-id="c0c64-110">Active state change of the client, which can be a combination of any of the following values:</span></span>



| <span data-ttu-id="c0c64-111">Valore</span><span class="sxs-lookup"><span data-stu-id="c0c64-111">Value</span></span>                                                              | <span data-ttu-id="c0c64-112">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c0c64-112">Description</span></span>                                                           |
|--------------------------------------------------------------------|-----------------------------------------------------------------------|
| <span data-ttu-id="c0c64-113">**const unsigned short** **Activate \_ notacty = 0;**</span><span class="sxs-lookup"><span data-stu-id="c0c64-113">**const unsigned short** **ACTIVATE\_NOTACTIVE = 0;**</span></span><br/>   | <span data-ttu-id="c0c64-114">Il client non è il client attivo del carattere.</span><span class="sxs-lookup"><span data-stu-id="c0c64-114">Your client is not the active client of the character.</span></span>                |
| <span data-ttu-id="c0c64-115">**const unsigned short** **Activate \_ attivo = 1;**</span><span class="sxs-lookup"><span data-stu-id="c0c64-115">**const unsigned short** **ACTIVATE\_ACTIVE = 1;**</span></span><br/>      | <span data-ttu-id="c0c64-116">Il client è il client attivo del carattere.</span><span class="sxs-lookup"><span data-stu-id="c0c64-116">Your client is the active client of the character.</span></span>                    |
| <span data-ttu-id="c0c64-117">**const unsigned short** **Activate \_ INPUTACTIVE = 2;**</span><span class="sxs-lookup"><span data-stu-id="c0c64-117">**const unsigned short** **ACTIVATE\_INPUTACTIVE = 2;**</span></span><br/> | <span data-ttu-id="c0c64-118">Il client è di input-attivo (client attivo del carattere superiore).</span><span class="sxs-lookup"><span data-stu-id="c0c64-118">Your client is input-active (active client of the topmost character).</span></span> |



 

</dd> </dl>

<span data-ttu-id="c0c64-119">Quando più applicazioni client condividono lo stesso carattere, il client attivo del carattere riceve l'input del mouse (ad esempio, gli eventi di clic o di trascinamento del controllo agente Microsoft).</span><span class="sxs-lookup"><span data-stu-id="c0c64-119">When multiple client applications share the same character, the active client of the character receives mouse input (for example, Microsoft Agent control click or drag events).</span></span> <span data-ttu-id="c0c64-120">Analogamente, quando vengono visualizzati più caratteri, il client attivo del carattere superiore (noto anche come client di input-attivo) riceve gli eventi [**IAgentNotifySink:: Command**](iagentnotifysink--command.md) .</span><span class="sxs-lookup"><span data-stu-id="c0c64-120">Similarly, when multiple characters are displayed, the active client of the topmost character (also known as the input-active client) receives [**IAgentNotifySink::Command**](iagentnotifysink--command.md) events.</span></span>

<span data-ttu-id="c0c64-121">Quando viene modificato il client attivo di un carattere, questo evento restituisce l'ID di tale carattere e **true** se l'applicazione è diventata il client attivo del carattere o **false** se non è più il client attivo del carattere.</span><span class="sxs-lookup"><span data-stu-id="c0c64-121">When the active client of a character changes, this event passes back the ID of that character and **True** if your application has become the active client of the character or **False** if it is no longer the active client of the character.</span></span>

<span data-ttu-id="c0c64-122">Un'applicazione client può ricevere questo evento quando l'utente seleziona la voce di un'altra applicazione client nel menu popup del carattere o tramite il comando vocale, l'applicazione client ne modifica lo stato attivo oppure un'altra applicazione client chiude la connessione a Microsoft Agent.</span><span class="sxs-lookup"><span data-stu-id="c0c64-122">A client application may receive this event when the user selects another client application's entry in character's pop-up menu or by voice command, the client application changes its active status, or another client application quits its connection to Microsoft Agent.</span></span> <span data-ttu-id="c0c64-123">Agent invia questo evento solo alle applicazioni client interessate direttamente, ovvero quelle che diventano il client attivo o smettono di essere il client attivo.</span><span class="sxs-lookup"><span data-stu-id="c0c64-123">Agent sends this event only to the client applications that are directly affected-those that either become the active client or stop being the active client.</span></span>

<span data-ttu-id="c0c64-124">È possibile usare il metodo [**Activate**](iagentcharacter--activate.md) per impostare se l'applicazione è il client attivo del carattere o per rendere l'applicazione il client di input-attivo (che rende anche il carattere in primo piano).</span><span class="sxs-lookup"><span data-stu-id="c0c64-124">You can use the [**Activate**](iagentcharacter--activate.md) method to set whether your application is the active client of the character or to make your application the input-active client (which also makes the character topmost).</span></span>

## <a name="see-also"></a><span data-ttu-id="c0c64-125">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="c0c64-125">See Also</span></span>

<span data-ttu-id="c0c64-126">[**IAgentCharacter:: Activate**](iagentcharacter--activate.md), [**IAgentCharacterEx:: getActive**](iagentcharacterex--getactive.md), [**IAgentNotifySink:: ActivateInputState**](iagentnotifysink--activateinputstate.md)</span><span class="sxs-lookup"><span data-stu-id="c0c64-126">[**IAgentCharacter::Activate**](iagentcharacter--activate.md), [**IAgentCharacterEx::GetActive**](iagentcharacterex--getactive.md), [**IAgentNotifySink::ActivateInputState**](iagentnotifysink--activateinputstate.md)</span></span>


 

 





