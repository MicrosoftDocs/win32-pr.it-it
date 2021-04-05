---
title: IAgentCommands RemoveAll
description: IAgentCommands RemoveAll
ms.assetid: fab43363-6325-4566-b7bb-599591f67321
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e8bd374b7c5767c416d2c3bb2281e651ba71acd8
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "103727039"
---
# <a name="iagentcommandsremoveall"></a><span data-ttu-id="fc580-103">IAgentCommands:: RemoveAll</span><span class="sxs-lookup"><span data-stu-id="fc580-103">IAgentCommands::RemoveAll</span></span>

<span data-ttu-id="fc580-104">\[Microsoft Agent è stato deprecato a partire da Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="fc580-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT Remove();
```

<span data-ttu-id="fc580-105">Rimuove tutti i [**comandi**](/windows/desktop/lwef/the-command-object) da una raccolta di [**comandi**](/windows/desktop/lwef/the-commands-collection-object) .</span><span class="sxs-lookup"><span data-stu-id="fc580-105">Removes all [**Commands**](/windows/desktop/lwef/the-command-object) from a [**Commands**](/windows/desktop/lwef/the-commands-collection-object) collection.</span></span>

-   <span data-ttu-id="fc580-106">Restituisce \_ OK per indicare che l'operazione è stata completata.</span><span class="sxs-lookup"><span data-stu-id="fc580-106">Returns S\_OK to indicate the operation was successful.</span></span>

<span data-ttu-id="fc580-107">La rimozione di tutti i [**comandi**](/windows/desktop/lwef/the-command-object) da una raccolta di [**comandi**](/windows/desktop/lwef/the-commands-collection-object) li rimuove anche dal menu a comparsa e dalla **finestra comandi vocali** quando l'applicazione è di input-attivo.</span><span class="sxs-lookup"><span data-stu-id="fc580-107">Removing all [**Commands**](/windows/desktop/lwef/the-command-object) from a [**Commands**](/windows/desktop/lwef/the-commands-collection-object) collection also removes them from the pop-up menu and the **Voice Commands Window** when your application is input-active.</span></span> <span data-ttu-id="fc580-108">**RemoveAll** non rimuove le voci del server o di altri client.</span><span class="sxs-lookup"><span data-stu-id="fc580-108">**RemoveAll** does not remove server or other client's entries.</span></span>

## <a name="see-also"></a><span data-ttu-id="fc580-109">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="fc580-109">See Also</span></span>

<span data-ttu-id="fc580-110">[**IAgentCommands:: Add**](iagentcommands--add.md), [**IAgentCommands:: Insert**](iagentcommands--insert.md), [**IAgentCommands:: Remove**](iagentcommands--remove.md)</span><span class="sxs-lookup"><span data-stu-id="fc580-110">[**IAgentCommands::Add**](iagentcommands--add.md), [**IAgentCommands::Insert**](iagentcommands--insert.md), [**IAgentCommands::Remove**](iagentcommands--remove.md)</span></span>


 

 