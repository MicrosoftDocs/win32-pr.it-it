---
title: IAgentCommands getvoice
description: IAgentCommands getvoice
ms.assetid: ef8983bc-c70c-48c7-9c5f-1dae61028d90
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6b1915512c89611267df3788e5dcaa84fb0874a4
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "104399025"
---
# <a name="iagentcommandsgetvoice"></a><span data-ttu-id="ed992-103">IAgentCommands:: getvoice</span><span class="sxs-lookup"><span data-stu-id="ed992-103">IAgentCommands::GetVoice</span></span>

<span data-ttu-id="ed992-104">\[Microsoft Agent è stato deprecato a partire da Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="ed992-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT GetVoice(
   BSTR * pbszVoice  // address of Voice setting for Commands collection
);
```

<span data-ttu-id="ed992-105">Recupera il valore della proprietà [**Voice**](voice-property.md) per una raccolta di [**comandi**](/windows/desktop/lwef/the-commands-collection-object) .</span><span class="sxs-lookup"><span data-stu-id="ed992-105">Retrieves the value of the [**Voice**](voice-property.md) property for a [**Commands**](/windows/desktop/lwef/the-commands-collection-object) collection.</span></span>

-   <span data-ttu-id="ed992-106">Restituisce \_ OK per indicare che l'operazione è stata completata.</span><span class="sxs-lookup"><span data-stu-id="ed992-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="ed992-107"><span id="pbszVoice"></span><span id="pbszvoice"></span><span id="PBSZVOICE"></span>*pbszVoice*</span><span class="sxs-lookup"><span data-stu-id="ed992-107"><span id="pbszVoice"></span><span id="pbszvoice"></span><span id="PBSZVOICE"></span>*pbszVoice*</span></span>
</dt> <dd>

<span data-ttu-id="ed992-108">Indirizzo di un BSTR che riceve il valore dell'impostazione del testo [**vocale**](voice-property.md) per una raccolta di [**comandi**](/windows/desktop/lwef/the-commands-collection-object) .</span><span class="sxs-lookup"><span data-stu-id="ed992-108">The address of a BSTR that receives the value of the [**Voice**](voice-property.md) text setting for a [**Commands**](/windows/desktop/lwef/the-commands-collection-object) collection.</span></span>

</dd> </dl>

## <a name="see-also"></a><span data-ttu-id="ed992-109">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="ed992-109">See Also</span></span>

<span data-ttu-id="ed992-110">[**IAgentCommands:: sevoice**](iagentcommands--setvoice.md), [**IAgentCommands:: GetCaption**](iagentcommands--getcaption.md), [**IAgentCommands:: getVisible**](iagentcommands--getvisible.md)</span><span class="sxs-lookup"><span data-stu-id="ed992-110">[**IAgentCommands::SetVoice**](iagentcommands--setvoice.md), [**IAgentCommands::GetCaption**](iagentcommands--getcaption.md), [**IAgentCommands::GetVisible**](iagentcommands--getvisible.md)</span></span>


 

 