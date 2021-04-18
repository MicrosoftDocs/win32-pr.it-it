---
title: IAgentBalloon GetFontItalic
description: IAgentBalloon GetFontItalic
ms.assetid: 03f40210-71b3-4488-9a44-5a9322db010a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e31c1a0e1e649e325e84d4a78eee087e102e8d1e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106298277"
---
# <a name="iagentballoongetfontitalic"></a><span data-ttu-id="35457-103">IAgentBalloon::GetFontItalic</span><span class="sxs-lookup"><span data-stu-id="35457-103">IAgentBalloon::GetFontItalic</span></span>

<span data-ttu-id="35457-104">\[Microsoft Agent è stato deprecato a partire da Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="35457-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT GetFontItalic(
   long * pbFontItalic  // address of variable for italic setting for 
);                      // font displayed in word balloon 
```

<span data-ttu-id="35457-105">Indica se il tipo di carattere utilizzato in un fumetto di Word è in corsivo.</span><span class="sxs-lookup"><span data-stu-id="35457-105">Indicates whether the font used in a word balloon is italic.</span></span>

-   <span data-ttu-id="35457-106">Restituisce \_ OK per indicare che l'operazione è stata completata.</span><span class="sxs-lookup"><span data-stu-id="35457-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="35457-107"><span id="pbFontItalic"></span><span id="pbfontitalic"></span><span id="PBFONTITALIC"></span>*pbFontItalic*</span><span class="sxs-lookup"><span data-stu-id="35457-107"><span id="pbFontItalic"></span><span id="pbfontitalic"></span><span id="PBFONTITALIC"></span>*pbFontItalic*</span></span>
</dt> <dd>

<span data-ttu-id="35457-108">Indirizzo di un valore che riceve **true** se il tipo di carattere è in corsivo e **false** se non è in corsivo.</span><span class="sxs-lookup"><span data-stu-id="35457-108">The address of a value that receives **True** if the font is italic and **False** if not italic.</span></span>

</dd> </dl>

<span data-ttu-id="35457-109">Lo stile del carattere utilizzato nella parola Balloon di un carattere viene definito nell'editor dei caratteri di Microsoft Agent.</span><span class="sxs-lookup"><span data-stu-id="35457-109">The font style used in a character's word balloon is defined in the Microsoft Agent Character Editor.</span></span> <span data-ttu-id="35457-110">Non può essere modificato da un'applicazione.</span><span class="sxs-lookup"><span data-stu-id="35457-110">It cannot be changed by an application.</span></span> <span data-ttu-id="35457-111">Tuttavia, l'utente può eseguire l'override delle impostazioni del tipo di carattere per tutti i caratteri tramite la finestra delle proprietà di Microsoft Agent.</span><span class="sxs-lookup"><span data-stu-id="35457-111">However, the user can override the font settings for all characters through the Microsoft Agent property sheet.</span></span>

 

 




