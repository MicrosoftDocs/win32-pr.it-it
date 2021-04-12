---
title: IAgentCommandsEx sefontsize
description: IAgentCommandsEx sefontsize
ms.assetid: 095f78d2-ef91-4880-ad49-dd9a94f02891
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 19bb9a638141dc3cebe683748500510ea848a664
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "104472859"
---
# <a name="iagentcommandsexsetfontsize"></a><span data-ttu-id="4693f-103">IAgentCommandsEx:: sefontsize</span><span class="sxs-lookup"><span data-stu-id="4693f-103">IAgentCommandsEx::SetFontSize</span></span>

<span data-ttu-id="4693f-104">\[Microsoft Agent è stato deprecato a partire da Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="4693f-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT SetFontSize(
   long lFontSize  // font size displayed in character's pop-up menu
);
```

<span data-ttu-id="4693f-105">Imposta la dimensione del tipo di carattere visualizzato nel menu di scelta rapida del carattere.</span><span class="sxs-lookup"><span data-stu-id="4693f-105">Sets the size of the font displayed in the character's pop-up menu.</span></span>

-   <span data-ttu-id="4693f-106">Restituisce \_ OK per indicare che l'operazione è stata completata.</span><span class="sxs-lookup"><span data-stu-id="4693f-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="4693f-107"><span id="lFontSize"></span><span id="lfontsize"></span><span id="LFONTSIZE"></span>*lFontSize*</span><span class="sxs-lookup"><span data-stu-id="4693f-107"><span id="lFontSize"></span><span id="lfontsize"></span><span id="LFONTSIZE"></span>*lFontSize*</span></span>
</dt> <dd>

<span data-ttu-id="4693f-108">Dimensione del carattere.</span><span class="sxs-lookup"><span data-stu-id="4693f-108">The size of the font.</span></span>

</dd> </dl>

<span data-ttu-id="4693f-109">Questa proprietà determina la dimensione in punti del tipo di carattere utilizzato per visualizzare il testo nel menu popup del carattere quando l'applicazione client è di input-attivo.</span><span class="sxs-lookup"><span data-stu-id="4693f-109">This property determines the point size of the font used to display text in the character's pop-up menu when your client application is input-active.</span></span> <span data-ttu-id="4693f-110">Il valore predefinito per l'impostazione del tipo di carattere è basato sull'impostazione del tipo di carattere del menu per l'impostazione dell'ID lingua del carattere, o se non è impostato, l'impostazione della lingua predefinita dell'utente.</span><span class="sxs-lookup"><span data-stu-id="4693f-110">The default value for the font setting is based on the menu font setting for the character's language ID setting-or if that's not set-the user default language setting.</span></span> <span data-ttu-id="4693f-111">Se l'opzione non è attiva, il testo della [](/windows/desktop/lwef/the-command-object) [**didascalia**](caption-property.md) del comando dell'applicazione client viene visualizzato nelle dimensioni dei punti specificate per il client attivo di input.</span><span class="sxs-lookup"><span data-stu-id="4693f-111">If not input-active, your client application's [**Command**](/windows/desktop/lwef/the-command-object) [**Caption**](caption-property.md) text appears in the point size specified for the input-active client.</span></span>

<span data-ttu-id="4693f-112">Questa proprietà si applica solo all'utilizzo del carattere da parte dell'applicazione client. l'impostazione non influisce sugli altri client del carattere o di altri caratteri dell'applicazione client.</span><span class="sxs-lookup"><span data-stu-id="4693f-112">This property applies only to your client application's use of the character; the setting does not affect other clients of the character or other characters of your client application.</span></span>

## <a name="see-also"></a><span data-ttu-id="4693f-113">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="4693f-113">See Also</span></span>

<span data-ttu-id="4693f-114">[**IAgentCommandsEx:: GetFontSize**](iagentcommandsex--getfontsize.md), [**IAgentCommandsEx:: GetFontName**](iagentcommandsex--getfontname.md), [**IAgentCommandsEx:: sefontname**](iagentcommandsex--setfontname.md)</span><span class="sxs-lookup"><span data-stu-id="4693f-114">[**IAgentCommandsEx::GetFontSize**](iagentcommandsex--getfontsize.md), [**IAgentCommandsEx::GetFontName**](iagentcommandsex--getfontname.md), [**IAgentCommandsEx::SetFontName**](iagentcommandsex--setfontname.md)</span></span>


 

 