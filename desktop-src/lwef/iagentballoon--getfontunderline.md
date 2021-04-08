---
title: IAgentBalloon GetFontUnderline
description: IAgentBalloon GetFontUnderline
ms.assetid: 19886e94-8095-4650-bd88-34ea9d96ddaa
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d5acf35453209679dc96c85b3017fbe76b19d53b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104045301"
---
# <a name="iagentballoongetfontunderline"></a><span data-ttu-id="85dcd-103">IAgentBalloon::GetFontUnderline</span><span class="sxs-lookup"><span data-stu-id="85dcd-103">IAgentBalloon::GetFontUnderline</span></span>

<span data-ttu-id="85dcd-104">\[Microsoft Agent è stato deprecato a partire da Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="85dcd-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT GetFontUnderline(
   long * pbFontUnderline  // address of variable for underline setting
);                         // for font displayed in word balloon 
```

<span data-ttu-id="85dcd-105">Indica se il tipo di carattere utilizzato in un fumetto di Word dispone del set di stili di sottolineatura.</span><span class="sxs-lookup"><span data-stu-id="85dcd-105">Indicates whether the font used in a word balloon has the underline style set.</span></span>

-   <span data-ttu-id="85dcd-106">Restituisce \_ OK per indicare che l'operazione è stata completata.</span><span class="sxs-lookup"><span data-stu-id="85dcd-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="85dcd-107"><span id="pbFontUnderline"></span><span id="pbfontunderline"></span><span id="PBFONTUNDERLINE"></span>*pbFontUnderline*</span><span class="sxs-lookup"><span data-stu-id="85dcd-107"><span id="pbFontUnderline"></span><span id="pbfontunderline"></span><span id="PBFONTUNDERLINE"></span>*pbFontUnderline*</span></span>
</dt> <dd>

<span data-ttu-id="85dcd-108">Indirizzo di un valore che riceve **true** se lo stile di sottolineatura del tipo di carattere è impostato e **false** in caso contrario.</span><span class="sxs-lookup"><span data-stu-id="85dcd-108">The address of a value that receives **True** if the font underline style is set and **False** if not.</span></span>

</dd> </dl>

<span data-ttu-id="85dcd-109">Lo stile del tipo di carattere utilizzato in un fumetto di parole è definito nell'editor dei caratteri di Microsoft Agent.</span><span class="sxs-lookup"><span data-stu-id="85dcd-109">The font style used in a character word balloon is defined in the Microsoft Agent Character Editor.</span></span> <span data-ttu-id="85dcd-110">Non può essere modificato da un'applicazione.</span><span class="sxs-lookup"><span data-stu-id="85dcd-110">It cannot be changed by an application.</span></span> <span data-ttu-id="85dcd-111">Tuttavia, l'utente può eseguire l'override delle impostazioni del tipo di carattere per tutti i caratteri utilizzando la finestra delle proprietà di Microsoft Agent.</span><span class="sxs-lookup"><span data-stu-id="85dcd-111">However, the user can override the font settings for all characters using the Microsoft Agent property sheet.</span></span>

 

 




