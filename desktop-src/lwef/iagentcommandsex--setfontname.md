---
title: IAgentCommandsEx sefontname
description: IAgentCommandsEx sefontname
ms.assetid: c676ceb6-c098-4ac0-9103-ece469317ad6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3e9a4b76a58fc3651c02bedc43f8d372f607c2df
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103708158"
---
# <a name="iagentcommandsexsetfontname"></a><span data-ttu-id="43e79-103">IAgentCommandsEx:: sefontname</span><span class="sxs-lookup"><span data-stu-id="43e79-103">IAgentCommandsEx::SetFontName</span></span>

<span data-ttu-id="43e79-104">\[Microsoft Agent è stato deprecato a partire da Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="43e79-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT SetFontName(
   BSTR bszFontName  // font to be displayed in character's pop-up menu
);
```

<span data-ttu-id="43e79-105">Imposta il tipo di carattere visualizzato nel menu di scelta rapida del carattere.</span><span class="sxs-lookup"><span data-stu-id="43e79-105">Sets the font displayed in the character's pop-up menu.</span></span>

-   <span data-ttu-id="43e79-106">Restituisce \_ OK per indicare che l'operazione è stata completata.</span><span class="sxs-lookup"><span data-stu-id="43e79-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="43e79-107"><span id="bszFontName"></span><span id="bszfontname"></span><span id="BSZFONTNAME"></span>*bszFontName*</span><span class="sxs-lookup"><span data-stu-id="43e79-107"><span id="bszFontName"></span><span id="bszfontname"></span><span id="BSZFONTNAME"></span>*bszFontName*</span></span>
</dt> <dd>

<span data-ttu-id="43e79-108">BSTR che imposta il tipo di carattere visualizzato nel menu di scelta rapida del carattere.</span><span class="sxs-lookup"><span data-stu-id="43e79-108">A BSTR that sets the font displayed in the character's pop-up menu.</span></span>

</dd> </dl>

<span data-ttu-id="43e79-109">Questa proprietà determina il tipo di carattere utilizzato per visualizzare il testo nel menu popup del carattere.</span><span class="sxs-lookup"><span data-stu-id="43e79-109">This property determines the font used to display text in the character's pop-up menu.</span></span> <span data-ttu-id="43e79-110">Il valore predefinito per l'impostazione del tipo di carattere è basato sull'impostazione del tipo di carattere del menu per l'impostazione dell'ID lingua del carattere, o se non è impostato, l'impostazione dell'ID lingua predefinita dell'utente.</span><span class="sxs-lookup"><span data-stu-id="43e79-110">The default value for the font setting is based on the menu font setting for the character's language ID setting-or if that's not set-the user default language ID setting.</span></span>

<span data-ttu-id="43e79-111">Questa proprietà si applica solo all'utilizzo del carattere da parte dell'applicazione client. l'impostazione non influisce sugli altri client del carattere o di altri caratteri dell'applicazione client.</span><span class="sxs-lookup"><span data-stu-id="43e79-111">This property applies only to your client application's use of the character; the setting does not affect other clients of the character or other characters of your client application.</span></span>

## <a name="see-also"></a><span data-ttu-id="43e79-112">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="43e79-112">See Also</span></span>

<span data-ttu-id="43e79-113">[**IAgentCommandsEx:: GetFontName**](iagentcommandsex--getfontname.md), [**IAgentCommandsEx:: GetFontSize**](iagentcommandsex--getfontsize.md), [**IAgentCommandsEx:: sefontsize**](iagentcommandsex--setfontsize.md)</span><span class="sxs-lookup"><span data-stu-id="43e79-113">[**IAgentCommandsEx::GetFontName**](iagentcommandsex--getfontname.md), [**IAgentCommandsEx::GetFontSize**](iagentcommandsex--getfontsize.md), [**IAgentCommandsEx::SetFontSize**](iagentcommandsex--setfontsize.md)</span></span>


 

 




