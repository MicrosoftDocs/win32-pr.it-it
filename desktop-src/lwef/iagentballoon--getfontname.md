---
title: IAgentBalloon GetFontName
description: IAgentBalloon GetFontName
ms.assetid: 7d057571-bb6e-4b79-bc4a-5691779ace51
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 73f29ad981fb4b10249b17e55c92fb286552eedc
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104396803"
---
# <a name="iagentballoongetfontname"></a><span data-ttu-id="8473e-103">IAgentBalloon:: GetFontName</span><span class="sxs-lookup"><span data-stu-id="8473e-103">IAgentBalloon::GetFontName</span></span>

<span data-ttu-id="8473e-104">\[Microsoft Agent è stato deprecato a partire da Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="8473e-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT GetFontName(
   BSTR * pbszFontName  // address of variable for font displayed 
);                      // in word balloon
```

<span data-ttu-id="8473e-105">Recupera il valore per il tipo di carattere visualizzato in un fumetto di Word.</span><span class="sxs-lookup"><span data-stu-id="8473e-105">Retrieves the value for the font displayed in a word balloon.</span></span>

-   <span data-ttu-id="8473e-106">Restituisce \_ OK per indicare che l'operazione è stata completata.</span><span class="sxs-lookup"><span data-stu-id="8473e-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="8473e-107"><span id="pbszFontName"></span><span id="pbszfontname"></span><span id="PBSZFONTNAME"></span>*pbszFontName*</span><span class="sxs-lookup"><span data-stu-id="8473e-107"><span id="pbszFontName"></span><span id="pbszfontname"></span><span id="PBSZFONTNAME"></span>*pbszFontName*</span></span>
</dt> <dd>

<span data-ttu-id="8473e-108">Indirizzo di un BSTR che riceve il nome del tipo di carattere visualizzato in un fumetto di Word.</span><span class="sxs-lookup"><span data-stu-id="8473e-108">The address of a BSTR that receives the font name displayed in a word balloon.</span></span>

</dd> </dl>

<span data-ttu-id="8473e-109">Il tipo di carattere predefinito utilizzato in un fumetto di parole è definito nell'editor dei caratteri di Microsoft Agent.</span><span class="sxs-lookup"><span data-stu-id="8473e-109">The default font used in a character word balloon is defined in the Microsoft Agent Character Editor.</span></span> <span data-ttu-id="8473e-110">È possibile modificarlo con [**IAgentBalloon:: Sefontname**](https://www.bing.com/search?q=**IAgentBalloon::SetFontName**).</span><span class="sxs-lookup"><span data-stu-id="8473e-110">You can change it with [**IAgentBalloon::SetFontName**](https://www.bing.com/search?q=**IAgentBalloon::SetFontName**).</span></span> <span data-ttu-id="8473e-111">L'utente può eseguire l'override dell'impostazione del tipo di carattere per tutti i caratteri utilizzando la finestra delle proprietà di Microsoft Agent.</span><span class="sxs-lookup"><span data-stu-id="8473e-111">The user can override the font setting for all characters using the Microsoft Agent property sheet.</span></span>

 

 




