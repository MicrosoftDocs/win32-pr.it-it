---
title: IAgentCommandsEx GetFontSize
description: IAgentCommandsEx GetFontSize
ms.assetid: 8173e026-d28f-43d8-a8b4-96d1d97a8b68
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 48a2450d94e89dd9dddc00a11af7f37bf4837558
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104396194"
---
# <a name="iagentcommandsexgetfontsize"></a><span data-ttu-id="72c3a-103">IAgentCommandsEx:: GetFontSize</span><span class="sxs-lookup"><span data-stu-id="72c3a-103">IAgentCommandsEx::GetFontSize</span></span>

<span data-ttu-id="72c3a-104">\[Microsoft Agent è stato deprecato a partire da Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="72c3a-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT GetFontSize(
   long * plFontSize  // address of variable for font size 
);                    // for font displayed in character's pop-up menu
```

<span data-ttu-id="72c3a-105">Recupera il valore per la dimensione del tipo di carattere visualizzato nel menu di scelta rapida del carattere.</span><span class="sxs-lookup"><span data-stu-id="72c3a-105">Retrieves the value for the size of the font displayed in the character's pop-up menu.</span></span>

-   <span data-ttu-id="72c3a-106">Restituisce \_ OK per indicare che l'operazione è stata completata.</span><span class="sxs-lookup"><span data-stu-id="72c3a-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="72c3a-107"><span id="plFontSize"></span><span id="plfontsize"></span><span id="PLFONTSIZE"></span>*plFontSize*</span><span class="sxs-lookup"><span data-stu-id="72c3a-107"><span id="plFontSize"></span><span id="plfontsize"></span><span id="PLFONTSIZE"></span>*plFontSize*</span></span>
</dt> <dd>

<span data-ttu-id="72c3a-108">Indirizzo di un valore che riceve la dimensione del tipo di carattere.</span><span class="sxs-lookup"><span data-stu-id="72c3a-108">The address of a value that receives the size of the font.</span></span>

</dd> </dl>

<span data-ttu-id="72c3a-109">La dimensione in punti del tipo di carattere restituito corrisponde alla dimensione definita per visualizzare il testo nel menu popup del carattere quando il client è di input-attivo.</span><span class="sxs-lookup"><span data-stu-id="72c3a-109">The point size of the font returned corresponds to the size defined to display text in the character's pop-up menu when your client is input-active.</span></span> <span data-ttu-id="72c3a-110">Il valore predefinito per l'impostazione del tipo di carattere è basato sull'impostazione del tipo di carattere del menu per l'impostazione dell'ID lingua del carattere oppure, se non è impostato, l'impostazione della lingua predefinita dell'utente.</span><span class="sxs-lookup"><span data-stu-id="72c3a-110">The default value for the font setting is based on the menu font setting for the character's language ID setting, or if not set, the user default language setting.</span></span>

<span data-ttu-id="72c3a-111">Questa proprietà si applica solo all'utilizzo del carattere da parte dell'applicazione client. l'impostazione non influisce sugli altri client del carattere o di altri caratteri dell'applicazione client.</span><span class="sxs-lookup"><span data-stu-id="72c3a-111">This property applies only to your client application's use of the character; the setting does not affect other clients of the character or other characters of your client application.</span></span>

## <a name="see-also"></a><span data-ttu-id="72c3a-112">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="72c3a-112">See Also</span></span>

<span data-ttu-id="72c3a-113">[**IAgentCommandsEx:: sefontsize**](iagentcommandsex--setfontsize.md), [ **IAgentCommandsEx:: sefontname**](iagentcommandsex--setfontname.md)</span><span class="sxs-lookup"><span data-stu-id="72c3a-113">[**IAgentCommandsEx::SetFontSize**](iagentcommandsex--setfontsize.md), [**IAgentCommandsEx::SetFontName**](iagentcommandsex--setfontname.md)</span></span>


 

 




