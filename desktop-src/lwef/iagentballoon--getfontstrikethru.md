---
title: IAgentBalloon GetFontStrikethru
description: IAgentBalloon GetFontStrikethru
ms.assetid: b5c253e8-dca7-44a6-b63b-a33e6e793a40
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2001ec0125949144843d500f125b3502e94723db
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104396799"
---
# <a name="iagentballoongetfontstrikethru"></a><span data-ttu-id="0d106-103">IAgentBalloon::GetFontStrikethru</span><span class="sxs-lookup"><span data-stu-id="0d106-103">IAgentBalloon::GetFontStrikethru</span></span>

<span data-ttu-id="0d106-104">\[Microsoft Agent è stato deprecato a partire da Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="0d106-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT GetFontStrikethru(
   long * pbFontStrikethru  // address of variable for strikethrough setting 
);                          // for font displayed in word balloon 
```

<span data-ttu-id="0d106-105">Indica se il tipo di carattere utilizzato in un fumetto di Word dispone del set di stili barrato.</span><span class="sxs-lookup"><span data-stu-id="0d106-105">Indicates whether the font used in a word balloon has the strikethrough style set.</span></span>

-   <span data-ttu-id="0d106-106">Restituisce \_ OK per indicare che l'operazione è stata completata.</span><span class="sxs-lookup"><span data-stu-id="0d106-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="0d106-107"><span id="pbFontStrikethru"></span><span id="pbfontstrikethru"></span><span id="PBFONTSTRIKETHRU"></span>*pbFontStrikethru*</span><span class="sxs-lookup"><span data-stu-id="0d106-107"><span id="pbFontStrikethru"></span><span id="pbfontstrikethru"></span><span id="PBFONTSTRIKETHRU"></span>*pbFontStrikethru*</span></span>
</dt> <dd>

<span data-ttu-id="0d106-108">Indirizzo di un valore che riceve **true** se lo stile barrato del carattere è impostato e **false** in caso contrario.</span><span class="sxs-lookup"><span data-stu-id="0d106-108">The address of a value that receives **True** if the font strikethrough style is set and **False** if not.</span></span>

</dd> </dl>

<span data-ttu-id="0d106-109">Lo stile del tipo di carattere utilizzato in un fumetto di parole è definito nell'editor dei caratteri di Microsoft Agent.</span><span class="sxs-lookup"><span data-stu-id="0d106-109">The font style used in a character word balloon is defined in the Microsoft Agent Character Editor.</span></span> <span data-ttu-id="0d106-110">Non può essere modificato da un'applicazione.</span><span class="sxs-lookup"><span data-stu-id="0d106-110">It cannot be changed by an application.</span></span> <span data-ttu-id="0d106-111">Tuttavia, l'utente può eseguire l'override delle impostazioni del tipo di carattere per tutti i caratteri utilizzando la finestra delle proprietà di Microsoft Agent.</span><span class="sxs-lookup"><span data-stu-id="0d106-111">However, the user can override the font settings for all characters using the Microsoft Agent property sheet.</span></span>

 

 




