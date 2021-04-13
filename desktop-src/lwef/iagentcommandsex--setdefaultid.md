---
title: IAgentCommandsEx SetDefaultID
description: IAgentCommandsEx SetDefaultID
ms.assetid: 056ec518-bf0b-403f-adc6-9b53b0c044a7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 37754eb61df7879511a03dde705936d36f905376
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "104398927"
---
# <a name="iagentcommandsexsetdefaultid"></a><span data-ttu-id="fb143-103">IAgentCommandsEx::SetDefaultID</span><span class="sxs-lookup"><span data-stu-id="fb143-103">IAgentCommandsEx::SetDefaultID</span></span>

<span data-ttu-id="fb143-104">\[Microsoft Agent è stato deprecato a partire da Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="fb143-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT SetDefaultID(
   long dwID,  // default command's ID
);
```

<span data-ttu-id="fb143-105">Imposta l'ID del comando predefinito in una raccolta di [**comandi**](/windows/desktop/lwef/the-commands-collection-object) .</span><span class="sxs-lookup"><span data-stu-id="fb143-105">Sets the ID of the default command in a [**Commands**](/windows/desktop/lwef/the-commands-collection-object) collection.</span></span>

-   <span data-ttu-id="fb143-106">Restituisce \_ OK per indicare che l'operazione è stata completata.</span><span class="sxs-lookup"><span data-stu-id="fb143-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="fb143-107"><span id="dwID"></span><span id="dwid"></span><span id="DWID"></span>*dwID*</span><span class="sxs-lookup"><span data-stu-id="fb143-107"><span id="dwID"></span><span id="dwid"></span><span id="DWID"></span>*dwID*</span></span>
</dt> <dd>

<span data-ttu-id="fb143-108">ID del [**comando**](/windows/desktop/lwef/the-command-object) da impostare come valore predefinito.</span><span class="sxs-lookup"><span data-stu-id="fb143-108">The ID for the [**Command**](/windows/desktop/lwef/the-command-object) to be set as the default.</span></span>

</dd> </dl>

<span data-ttu-id="fb143-109">Questa proprietà imposta il set di oggetti [**comando**](/windows/desktop/lwef/the-command-object) predefinito nella raccolta di [**comandi**](/windows/desktop/lwef/the-commands-collection-object) .</span><span class="sxs-lookup"><span data-stu-id="fb143-109">This property sets the default [**Command**](/windows/desktop/lwef/the-command-object) object set in your [**Commands**](/windows/desktop/lwef/the-commands-collection-object) collection.</span></span> <span data-ttu-id="fb143-110">Il comando predefinito è in grassetto nel menu a comparsa del carattere.</span><span class="sxs-lookup"><span data-stu-id="fb143-110">The default command is bold in the character's pop-up menu.</span></span> <span data-ttu-id="fb143-111">Tuttavia, l'impostazione del comando predefinito non modifica effettivamente la gestione dei comandi o gli eventi di doppio clic.</span><span class="sxs-lookup"><span data-stu-id="fb143-111">However, setting the default command does not actually change command handling or double-click events.</span></span>

<span data-ttu-id="fb143-112">Questa proprietà si applica solo all'utilizzo del carattere da parte dell'applicazione client. l'impostazione non influisce sugli altri client del carattere o di altri caratteri dell'applicazione client.</span><span class="sxs-lookup"><span data-stu-id="fb143-112">This property applies only to your client application's use of the character; the setting does not affect other clients of the character or other characters of your client application.</span></span>

## <a name="see-also"></a><span data-ttu-id="fb143-113">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="fb143-113">See Also</span></span>

[<span data-ttu-id="fb143-114">**IAgentCommandsEx::GetDefaultID**</span><span class="sxs-lookup"><span data-stu-id="fb143-114">**IAgentCommandsEx::GetDefaultID**</span></span>](iagentcommandsex--getdefaultid.md)


 

 