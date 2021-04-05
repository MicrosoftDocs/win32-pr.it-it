---
title: IAgentCommandWindow visibile
description: IAgentCommandWindow visibile
ms.assetid: 44f3fc2d-937a-4890-8dad-e0f29da4c6b5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a43ddff54f4869cbe36016f30d775eeea017ae6c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104044910"
---
# <a name="iagentcommandwindowsetvisible"></a><span data-ttu-id="26ade-103">IAgentCommandWindow:: sevisible</span><span class="sxs-lookup"><span data-stu-id="26ade-103">IAgentCommandWindow::SetVisible</span></span>

<span data-ttu-id="26ade-104">\[Microsoft Agent è stato deprecato a partire da Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="26ade-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT SetVisible(
   long bVisible  // Voice Commands Window Visible setting 
);
```

<span data-ttu-id="26ade-105">Impostare la proprietà [**Visible**](visible-property.md) per la finestra dei comandi vocali.</span><span class="sxs-lookup"><span data-stu-id="26ade-105">Set the [**Visible**](visible-property.md) property for the Voice Commands Window.</span></span>

-   <span data-ttu-id="26ade-106">Restituisce \_ OK per indicare che l'operazione è stata completata.</span><span class="sxs-lookup"><span data-stu-id="26ade-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="26ade-107"><span id="bVisible"></span><span id="bvisible"></span><span id="BVISIBLE"></span>*bVisible*</span><span class="sxs-lookup"><span data-stu-id="26ade-107"><span id="bVisible"></span><span id="bvisible"></span><span id="BVISIBLE"></span>*bVisible*</span></span>
</dt> <dd>

<span data-ttu-id="26ade-108">Impostazione della proprietà [**Visible**](visible-property.md) .</span><span class="sxs-lookup"><span data-stu-id="26ade-108">[**Visible**](visible-property.md) property setting.</span></span> <span data-ttu-id="26ade-109">Il valore **true** Visualizza la finestra comandi vocali; **False** lo nasconde.</span><span class="sxs-lookup"><span data-stu-id="26ade-109">A value of **True** displays the Voice Commands Window; **False** hides it.</span></span>

</dd> </dl>

<span data-ttu-id="26ade-110">L'utente può eseguire l'override di questa proprietà.</span><span class="sxs-lookup"><span data-stu-id="26ade-110">The user can override this property.</span></span>

## <a name="see-also"></a><span data-ttu-id="26ade-111">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="26ade-111">See Also</span></span>

[<span data-ttu-id="26ade-112">**IAgentCommandWindow:: GetVisible**</span><span class="sxs-lookup"><span data-stu-id="26ade-112">**IAgentCommandWindow::GetVisible**</span></span>](iagentcommandwindow--getvisible.md)


 

 




