---
title: IAgentCommandsEx GetFontName
description: IAgentCommandsEx GetFontName
ms.assetid: cd0d0d93-839e-471c-9cfa-9f47dcce841b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 215f08cbe1e5e97b218f9279baff5e3affd74956
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104396195"
---
# <a name="iagentcommandsexgetfontname"></a><span data-ttu-id="307a4-103">IAgentCommandsEx:: GetFontName</span><span class="sxs-lookup"><span data-stu-id="307a4-103">IAgentCommandsEx::GetFontName</span></span>

<span data-ttu-id="307a4-104">\[Microsoft Agent è stato deprecato a partire da Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="307a4-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT GetFontName(
   BSTR * pbszFontName  // address of variable for font displayed 
);                      // in character's pop-up menu
```

<span data-ttu-id="307a4-105">Recupera il valore per il tipo di carattere visualizzato nel menu di scelta rapida del carattere.</span><span class="sxs-lookup"><span data-stu-id="307a4-105">Retrieves the value for the font displayed in the character's pop-up menu.</span></span>

-   <span data-ttu-id="307a4-106">Restituisce \_ OK per indicare che l'operazione è stata completata.</span><span class="sxs-lookup"><span data-stu-id="307a4-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="307a4-107"><span id="pbszFontName"></span><span id="pbszfontname"></span><span id="PBSZFONTNAME"></span>*pbszFontName*</span><span class="sxs-lookup"><span data-stu-id="307a4-107"><span id="pbszFontName"></span><span id="pbszfontname"></span><span id="PBSZFONTNAME"></span>*pbszFontName*</span></span>
</dt> <dd>

<span data-ttu-id="307a4-108">Indirizzo di un BSTR che riceve il nome del tipo di carattere visualizzato nel menu di scelta rapida del carattere.</span><span class="sxs-lookup"><span data-stu-id="307a4-108">The address of a BSTR that receives the font name displayed in the character's pop-up menu.</span></span>

</dd> </dl>

<span data-ttu-id="307a4-109">Il nome del tipo di carattere restituito corrisponde al tipo di carattere utilizzato per visualizzare il testo nel menu popup del carattere quando l'applicazione client è di input-attivo.</span><span class="sxs-lookup"><span data-stu-id="307a4-109">The font name returned corresponds to the font used to display text in the character's pop-up menu when your client application is input-active.</span></span> <span data-ttu-id="307a4-110">Il valore predefinito per l'impostazione del tipo di carattere è basato sull'impostazione del tipo di carattere del menu per l'impostazione dell'ID lingua del carattere oppure, se non è impostato, l'impostazione dell'ID lingua predefinita dell'utente.</span><span class="sxs-lookup"><span data-stu-id="307a4-110">The default value for the font setting is based on the menu font setting for the character's language ID setting, or if not set, the user default language ID setting.</span></span>

<span data-ttu-id="307a4-111">Questa proprietà si applica solo all'utilizzo del carattere da parte dell'applicazione client. l'impostazione non influisce sugli altri client del carattere o di altri caratteri dell'applicazione client.</span><span class="sxs-lookup"><span data-stu-id="307a4-111">This property applies only to your client application's use of the character; the setting does not affect other clients of the character or other characters of your client application.</span></span>

## <a name="see-also"></a><span data-ttu-id="307a4-112">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="307a4-112">See Also</span></span>

<span data-ttu-id="307a4-113">[**IAgentCommandsEx:: sefontname**](iagentcommandsex--setfontname.md), [ **IAgentCommandsEx:: sefontsize**](iagentcommandsex--setfontsize.md)</span><span class="sxs-lookup"><span data-stu-id="307a4-113">[**IAgentCommandsEx::SetFontName**](iagentcommandsex--setfontname.md), [**IAgentCommandsEx::SetFontSize**](iagentcommandsex--setfontsize.md)</span></span>


 

 




