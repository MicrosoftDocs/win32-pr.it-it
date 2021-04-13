---
title: IAgentCommandsEx GetDefaultID
description: IAgentCommandsEx GetDefaultID
ms.assetid: 14079ae0-ad2c-4f38-9371-9914f8402e49
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3e4380eca62a65758979a94fb23511348b11acdf
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "104399024"
---
# <a name="iagentcommandsexgetdefaultid"></a><span data-ttu-id="2ca61-103">IAgentCommandsEx::GetDefaultID</span><span class="sxs-lookup"><span data-stu-id="2ca61-103">IAgentCommandsEx::GetDefaultID</span></span>

<span data-ttu-id="2ca61-104">\[Microsoft Agent è stato deprecato a partire da Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="2ca61-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT GetDefaultID(
   long * pdwID  // address of default command's ID
);
```

<span data-ttu-id="2ca61-105">Recupera l'ID del comando predefinito in una raccolta di [**comandi**](/windows/desktop/lwef/the-commands-collection-object) .</span><span class="sxs-lookup"><span data-stu-id="2ca61-105">Retrieves the ID of the default command in a [**Commands**](/windows/desktop/lwef/the-commands-collection-object) collection.</span></span>

-   <span data-ttu-id="2ca61-106">Restituisce \_ OK per indicare che l'operazione è stata completata.</span><span class="sxs-lookup"><span data-stu-id="2ca61-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="2ca61-107"><span id="pdwID"></span><span id="pdwid"></span><span id="PDWID"></span>*pdwID*</span><span class="sxs-lookup"><span data-stu-id="2ca61-107"><span id="pdwID"></span><span id="pdwid"></span><span id="PDWID"></span>*pdwID*</span></span>
</dt> <dd>

<span data-ttu-id="2ca61-108">Indirizzo di una variabile che riceve l'ID del set di [**comandi**](/windows/desktop/lwef/the-command-object) come predefinito.</span><span class="sxs-lookup"><span data-stu-id="2ca61-108">Address of a variable that receives the ID of the [**Command**](/windows/desktop/lwef/the-command-object) set as the default.</span></span>

</dd> </dl>

<span data-ttu-id="2ca61-109">Questa proprietà restituisce l'oggetto [**comando**](/windows/desktop/lwef/the-command-object) predefinito corrente nella raccolta di [**comandi**](/windows/desktop/lwef/the-commands-collection-object) .</span><span class="sxs-lookup"><span data-stu-id="2ca61-109">This property returns the current default [**Command**](/windows/desktop/lwef/the-command-object) object in your [**Commands**](/windows/desktop/lwef/the-commands-collection-object) collection.</span></span> <span data-ttu-id="2ca61-110">Il comando predefinito è in grassetto nel menu a comparsa del carattere.</span><span class="sxs-lookup"><span data-stu-id="2ca61-110">The default command is bold in the character's pop-up menu.</span></span> <span data-ttu-id="2ca61-111">Tuttavia, l'impostazione del comando predefinito non comporta la modifica della gestione dei comandi o degli eventi di doppio clic.</span><span class="sxs-lookup"><span data-stu-id="2ca61-111">However, setting the default command does not change command handling or double-click events.</span></span>

<span data-ttu-id="2ca61-112">Questa proprietà si applica solo all'utilizzo del carattere da parte dell'applicazione client. l'impostazione non influisce sugli altri client del carattere o di altri caratteri dell'applicazione client.</span><span class="sxs-lookup"><span data-stu-id="2ca61-112">This property applies only to your client application's use of the character; the setting does not affect other clients of the character or other characters of your client application.</span></span>

## <a name="see-also"></a><span data-ttu-id="2ca61-113">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="2ca61-113">See Also</span></span>

[<span data-ttu-id="2ca61-114">**IAgentCommandsEx::SetDefaultID**</span><span class="sxs-lookup"><span data-stu-id="2ca61-114">**IAgentCommandsEx::SetDefaultID**</span></span>](iagentcommandsex--setdefaultid.md)


 

 