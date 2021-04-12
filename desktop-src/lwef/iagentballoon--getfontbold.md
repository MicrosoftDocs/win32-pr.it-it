---
title: IAgentBalloon GetFontBold
description: IAgentBalloon GetFontBold
ms.assetid: 5a55f771-d68e-4f66-8001-47c141661b06
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 858f6f42964db1bdd7ae548d308c6f6668b05631
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104221602"
---
# <a name="iagentballoongetfontbold"></a><span data-ttu-id="1dd7b-103">IAgentBalloon::GetFontBold</span><span class="sxs-lookup"><span data-stu-id="1dd7b-103">IAgentBalloon::GetFontBold</span></span>

<span data-ttu-id="1dd7b-104">\[Microsoft Agent è stato deprecato a partire da Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="1dd7b-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT GetFontBold(
   long * pbFontBold  // address of variable for bold setting for
);                    // font displayed in word balloon 
```

<span data-ttu-id="1dd7b-105">Indica se il tipo di carattere utilizzato in un fumetto di Word è in grassetto.</span><span class="sxs-lookup"><span data-stu-id="1dd7b-105">Indicates whether the font used in a word balloon is bold.</span></span>

-   <span data-ttu-id="1dd7b-106">Restituisce \_ OK per indicare che l'operazione è stata completata.</span><span class="sxs-lookup"><span data-stu-id="1dd7b-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="1dd7b-107"><span id="pbFontBold"></span><span id="pbfontbold"></span><span id="PBFONTBOLD"></span>*pbFontBold*</span><span class="sxs-lookup"><span data-stu-id="1dd7b-107"><span id="pbFontBold"></span><span id="pbfontbold"></span><span id="PBFONTBOLD"></span>*pbFontBold*</span></span>
</dt> <dd>

<span data-ttu-id="1dd7b-108">Indirizzo di un valore che riceve **true** se il tipo di carattere è grassetto e **false** se non è in grassetto.</span><span class="sxs-lookup"><span data-stu-id="1dd7b-108">The address of a value that receives **True** if the font is bold and **False** if not bold.</span></span>

</dd> </dl>

<span data-ttu-id="1dd7b-109">Lo stile del tipo di carattere utilizzato in un fumetto di parole è definito nell'editor dei caratteri di Microsoft Agent.</span><span class="sxs-lookup"><span data-stu-id="1dd7b-109">The font style used in a character word balloon is defined in the Microsoft Agent Character Editor.</span></span> <span data-ttu-id="1dd7b-110">Non può essere modificato da un'applicazione.</span><span class="sxs-lookup"><span data-stu-id="1dd7b-110">It cannot be changed by an application.</span></span> <span data-ttu-id="1dd7b-111">Tuttavia, l'utente può eseguire l'override delle impostazioni del tipo di carattere per tutti i caratteri tramite la finestra delle proprietà di Microsoft Agent.</span><span class="sxs-lookup"><span data-stu-id="1dd7b-111">However, the user can override the font settings for all characters through the Microsoft Agent property sheet.</span></span>

 

 




