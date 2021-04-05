---
title: IAgentCharacterEx getActive
description: IAgentCharacterEx getActive
ms.assetid: b14ae69a-a50e-4488-b5a7-33702e6555eb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d1dab89ee9ba89c5982e34844917334d97169b9f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103856657"
---
# <a name="iagentcharacterexgetactive"></a><span data-ttu-id="3c588-103">IAgentCharacterEx:: getActive</span><span class="sxs-lookup"><span data-stu-id="3c588-103">IAgentCharacterEx::GetActive</span></span>

<span data-ttu-id="3c588-104">\[Microsoft Agent è stato deprecato a partire da Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="3c588-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT GetActive(
   short * psState  // address of active state setting
);
```

<span data-ttu-id="3c588-105">Recupera un valore che indica se l'applicazione client è il client attivo del carattere e se il carattere è in primo piano.</span><span class="sxs-lookup"><span data-stu-id="3c588-105">Retrieves whether your client application is the active client of the character and whether the character is topmost.</span></span>

-   <span data-ttu-id="3c588-106">Restituisce \_ OK per indicare che l'operazione è stata completata.</span><span class="sxs-lookup"><span data-stu-id="3c588-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="3c588-107"><span id="psState"></span><span id="psstate"></span><span id="PSSTATE"></span>*psState*</span><span class="sxs-lookup"><span data-stu-id="3c588-107"><span id="psState"></span><span id="psstate"></span><span id="PSSTATE"></span>*psState*</span></span>
</dt> <dd>

<span data-ttu-id="3c588-108">Indirizzo di una variabile che riceve uno dei valori seguenti per l'impostazione dello stato:</span><span class="sxs-lookup"><span data-stu-id="3c588-108">Address of a variable that receives one of the following values for the state setting:</span></span>



| <span data-ttu-id="3c588-109">Valore</span><span class="sxs-lookup"><span data-stu-id="3c588-109">Value</span></span>                                                              | <span data-ttu-id="3c588-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="3c588-110">Description</span></span>                                                           |
|--------------------------------------------------------------------|-----------------------------------------------------------------------|
| <span data-ttu-id="3c588-111">**const unsigned short** **Activate \_ notacty = 0;**</span><span class="sxs-lookup"><span data-stu-id="3c588-111">**const unsigned short** **ACTIVATE\_NOTACTIVE = 0;**</span></span><br/>   | <span data-ttu-id="3c588-112">Il client non è il client attivo del carattere.</span><span class="sxs-lookup"><span data-stu-id="3c588-112">Your client is not the active client of the character.</span></span>                |
| <span data-ttu-id="3c588-113">**const unsigned short** **Activate \_ attivo = 1;**</span><span class="sxs-lookup"><span data-stu-id="3c588-113">**const unsigned short** **ACTIVATE\_ACTIVE = 1;**</span></span><br/>      | <span data-ttu-id="3c588-114">Il client è il client attivo del carattere.</span><span class="sxs-lookup"><span data-stu-id="3c588-114">Your client is the active client of the character.</span></span>                    |
| <span data-ttu-id="3c588-115">**const unsigned short** **Activate \_ INPUTACTIVE = 2;**</span><span class="sxs-lookup"><span data-stu-id="3c588-115">**const unsigned short** **ACTIVATE\_INPUTACTIVE = 2;**</span></span><br/> | <span data-ttu-id="3c588-116">Il client è di input-attivo (client attivo del carattere superiore).</span><span class="sxs-lookup"><span data-stu-id="3c588-116">Your client is input-active (active client of the topmost character).</span></span> |



 

</dd> </dl>

<span data-ttu-id="3c588-117">Questa impostazione consente di sapere se si è il client attivo del carattere o se il carattere è il carattere attivo di input.</span><span class="sxs-lookup"><span data-stu-id="3c588-117">This setting lets you know whether you are the active client of the character or whether your character is the input active character.</span></span> <span data-ttu-id="3c588-118">Quando più applicazioni client condividono lo stesso carattere, il client attivo del carattere riceve l'input del mouse (ad esempio, gli eventi di clic o di trascinamento del controllo agente Microsoft).</span><span class="sxs-lookup"><span data-stu-id="3c588-118">When multiple client applications share the same character, the active client of the character receives mouse input (for example, Microsoft Agent control click or drag events).</span></span> <span data-ttu-id="3c588-119">Analogamente, quando vengono visualizzati più caratteri, il client attivo del carattere superiore (noto anche come client di input-attivo) riceve gli eventi [**IAgentNotifySink:: Command**](iagentnotifysink--command.md) .</span><span class="sxs-lookup"><span data-stu-id="3c588-119">Similarly, when multiple characters are displayed, the active client of the topmost character (also known as the input-active client) receives [**IAgentNotifySink::Command**](iagentnotifysink--command.md) events.</span></span>

<span data-ttu-id="3c588-120">Usare il metodo [**Activate**](iagentcharacter--activate.md) per impostare se l'applicazione è il client attivo del carattere o per rendere l'applicazione il client attivo di input (che rende anche il carattere in primo piano).</span><span class="sxs-lookup"><span data-stu-id="3c588-120">Use the [**Activate**](iagentcharacter--activate.md) method to set whether your application is the active client of the character or to make your application the input active client (which also makes the character topmost).</span></span>

## <a name="see-also"></a><span data-ttu-id="3c588-121">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="3c588-121">See Also</span></span>

<span data-ttu-id="3c588-122">[**IAgentCharacter:: Activate**](iagentcharacter--activate.md), [ **IAgentNotifySinkEx:: ActiveClientChange**](iagentnotifysinkex--activeclientchange.md)</span><span class="sxs-lookup"><span data-stu-id="3c588-122">[**IAgentCharacter::Activate**](iagentcharacter--activate.md), [**IAgentNotifySinkEx::ActiveClientChange**](iagentnotifysinkex--activeclientchange.md)</span></span>


 

 





