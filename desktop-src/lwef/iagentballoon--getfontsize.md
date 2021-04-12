---
title: IAgentBalloon GetFontSize
description: IAgentBalloon GetFontSize
ms.assetid: 4d342ee9-abb4-431b-bd28-f62ab76705ec
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d14b1a921f1f5c9927f58ab9e561569ba3bc98fa
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104222071"
---
# <a name="iagentballoongetfontsize"></a><span data-ttu-id="adf18-103">IAgentBalloon:: GetFontSize</span><span class="sxs-lookup"><span data-stu-id="adf18-103">IAgentBalloon::GetFontSize</span></span>

<span data-ttu-id="adf18-104">\[Microsoft Agent è stato deprecato a partire da Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="adf18-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT GetFontSize(
   long * plFontSize  // address of variable for font size 
);                    // for font displayed in word balloon 
```

<span data-ttu-id="adf18-105">Recupera il valore per la dimensione del tipo di carattere visualizzato in un fumetto di Word.</span><span class="sxs-lookup"><span data-stu-id="adf18-105">Retrieves the value for the size of the font displayed in a word balloon.</span></span>

-   <span data-ttu-id="adf18-106">Restituisce \_ OK per indicare che l'operazione è stata completata.</span><span class="sxs-lookup"><span data-stu-id="adf18-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="adf18-107"><span id="plFontSize"></span><span id="plfontsize"></span><span id="PLFONTSIZE"></span>*plFontSize*</span><span class="sxs-lookup"><span data-stu-id="adf18-107"><span id="plFontSize"></span><span id="plfontsize"></span><span id="PLFONTSIZE"></span>*plFontSize*</span></span>
</dt> <dd>

<span data-ttu-id="adf18-108">Indirizzo di un valore che riceve la dimensione del tipo di carattere.</span><span class="sxs-lookup"><span data-stu-id="adf18-108">The address of a value that receives the size of the font.</span></span>

</dd> </dl>

<span data-ttu-id="adf18-109">Le dimensioni predefinite del tipo di carattere utilizzate in un fumetto di parole sono definite nell'editor dei caratteri di Microsoft Agent.</span><span class="sxs-lookup"><span data-stu-id="adf18-109">The default font size used in a character word balloon is defined in the Microsoft Agent Character Editor.</span></span> <span data-ttu-id="adf18-110">È possibile modificarlo con [**IAgentBalloon:: sefontsize**](https://www.bing.com/search?q=**IAgentBalloon::SetFontSize**).</span><span class="sxs-lookup"><span data-stu-id="adf18-110">You can change it with [**IAgentBalloon::SetFontSize**](https://www.bing.com/search?q=**IAgentBalloon::SetFontSize**).</span></span> <span data-ttu-id="adf18-111">Tuttavia, l'utente può eseguire l'override delle impostazioni relative alle dimensioni del carattere per tutti i caratteri utilizzando la finestra delle proprietà di Microsoft Agent.</span><span class="sxs-lookup"><span data-stu-id="adf18-111">However, the user can override the font size settings for all characters using the Microsoft Agent property sheet.</span></span>

 

 




