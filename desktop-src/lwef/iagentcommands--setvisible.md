---
title: IAgentCommands visibile
description: IAgentCommands visibile
ms.assetid: 4b99989a-29bb-4e0e-8155-cf734cc667fd
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 04a4bdb3c1a7f1e11c9548eb1e1af415d0f5d18f
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "106299608"
---
# <a name="iagentcommandssetvisible"></a><span data-ttu-id="d4ef2-103">IAgentCommands:: sevisible</span><span class="sxs-lookup"><span data-stu-id="d4ef2-103">IAgentCommands::SetVisible</span></span>

<span data-ttu-id="d4ef2-104">\[Microsoft Agent è stato deprecato a partire da Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="d4ef2-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT SetVisible(
   long bVisible  // the Visible setting for Commands collection
);
```

<span data-ttu-id="d4ef2-105">Imposta il valore della proprietà [**Visible**](visible-property.md) per una raccolta di [**comandi**](/windows/desktop/lwef/the-commands-collection-object) .</span><span class="sxs-lookup"><span data-stu-id="d4ef2-105">Sets the value of the [**Visible**](visible-property.md) property for a [**Commands**](/windows/desktop/lwef/the-commands-collection-object) collection.</span></span>

-   <span data-ttu-id="d4ef2-106">Restituisce \_ OK per indicare che l'operazione è stata completata.</span><span class="sxs-lookup"><span data-stu-id="d4ef2-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="d4ef2-107"><span id="bVisible"></span><span id="bvisible"></span><span id="BVISIBLE"></span>*bVisible*</span><span class="sxs-lookup"><span data-stu-id="d4ef2-107"><span id="bVisible"></span><span id="bvisible"></span><span id="BVISIBLE"></span>*bVisible*</span></span>
</dt> <dd>

<span data-ttu-id="d4ef2-108">Valore booleano che determina la proprietà [**Visible**](visible-property.md) di una raccolta di [**comandi**](/windows/desktop/lwef/the-commands-collection-object) .</span><span class="sxs-lookup"><span data-stu-id="d4ef2-108">A Boolean value that determines the [**Visible**](visible-property.md) property of a [**Commands**](/windows/desktop/lwef/the-commands-collection-object) collection.</span></span> <span data-ttu-id="d4ef2-109">**True** imposta la [**didascalia**](caption-property.md) della raccolta di **comandi** in modo che sia visibile quando viene visualizzato il menu popup del carattere; *False* non lo Visualizza.</span><span class="sxs-lookup"><span data-stu-id="d4ef2-109">**True** sets the **Commands** collection's [**Caption**](caption-property.md) to be visible when the character's pop-up menu is displayed; *False* does not display it.</span></span>

</dd> </dl>

<span data-ttu-id="d4ef2-110">Una raccolta di [**comandi**](/windows/desktop/lwef/the-commands-collection-object) deve avere la relativa proprietà [**Caption**](caption-property.md) impostata e la relativa proprietà [**Visible**](visible-property.md) impostata su **true** per essere visualizzata nel menu popup del carattere.</span><span class="sxs-lookup"><span data-stu-id="d4ef2-110">A [**Commands**](/windows/desktop/lwef/the-commands-collection-object) collection must have its [**Caption**](caption-property.md) property set and its [**Visible**](visible-property.md) property set to **True** to appear on the character's pop-up menu.</span></span> <span data-ttu-id="d4ef2-111">È inoltre necessario impostare la proprietà **Visible** su **true** per visualizzare i comandi della raccolta quando l'applicazione client è di input-Active.</span><span class="sxs-lookup"><span data-stu-id="d4ef2-111">The **Visible** property must also be set to **True** for commands in the collection to appear when your client application is input-active.</span></span>

## <a name="see-also"></a><span data-ttu-id="d4ef2-112">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="d4ef2-112">See Also</span></span>

<span data-ttu-id="d4ef2-113">[**IAgentCommands:: getVisible**](iagentcommands--getvisible.md), [ **IAgentCommand:: Caption**](iagentcommand--setcaption.md)</span><span class="sxs-lookup"><span data-stu-id="d4ef2-113">[**IAgentCommands::GetVisible**](iagentcommands--getvisible.md), [**IAgentCommand::SetCaption**](iagentcommand--setcaption.md)</span></span>


 

 