---
title: IAgentBalloon SetFontCharSet
description: IAgentBalloon SetFontCharSet
ms.assetid: ce1b152d-c8af-47ec-9e6b-5768dbcf3566
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e6202aa144d13c3c7435be03721a3f8fd4878b93
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106298869"
---
# <a name="iagentballoonsetfontcharset"></a><span data-ttu-id="aad4f-103">IAgentBalloon::SetFontCharSet</span><span class="sxs-lookup"><span data-stu-id="aad4f-103">IAgentBalloon::SetFontCharSet</span></span>

<span data-ttu-id="aad4f-104">\[Microsoft Agent è stato deprecato a partire da Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="aad4f-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT SetFontCharSet(
   short sFontCharSet  // character set displayed in word balloon
); 
```

<span data-ttu-id="aad4f-105">Imposta il set di caratteri del tipo di carattere visualizzato nella parola Balloon.</span><span class="sxs-lookup"><span data-stu-id="aad4f-105">Sets the character set of the font displayed in the word balloon.</span></span>

-   <span data-ttu-id="aad4f-106">Restituisce \_ OK per indicare che l'operazione è stata completata.</span><span class="sxs-lookup"><span data-stu-id="aad4f-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="aad4f-107"><span id="sFontCharSet"></span><span id="sfontcharset"></span><span id="SFONTCHARSET"></span>*sFontCharSet*</span><span class="sxs-lookup"><span data-stu-id="aad4f-107"><span id="sFontCharSet"></span><span id="sfontcharset"></span><span id="SFONTCHARSET"></span>*sFontCharSet*</span></span>
</dt> <dd>

<span data-ttu-id="aad4f-108">Set di caratteri del tipo di carattere.</span><span class="sxs-lookup"><span data-stu-id="aad4f-108">The character set of the font.</span></span> <span data-ttu-id="aad4f-109">Di seguito sono riportate alcune impostazioni comuni per value:</span><span class="sxs-lookup"><span data-stu-id="aad4f-109">The following are some common settings for value:</span></span>



|     |                                                                                        |
|-----|----------------------------------------------------------------------------------------|
| <span data-ttu-id="aad4f-110">0</span><span class="sxs-lookup"><span data-stu-id="aad4f-110">0</span></span>   | <span data-ttu-id="aad4f-111">Caratteri Windows standard (ANSI).</span><span class="sxs-lookup"><span data-stu-id="aad4f-111">Standard Windows characters (ANSI).</span></span>                                                    |
| <span data-ttu-id="aad4f-112">1</span><span class="sxs-lookup"><span data-stu-id="aad4f-112">1</span></span>   | <span data-ttu-id="aad4f-113">Set di caratteri predefinito.</span><span class="sxs-lookup"><span data-stu-id="aad4f-113">Default character set.</span></span>                                                                 |
| <span data-ttu-id="aad4f-114">2</span><span class="sxs-lookup"><span data-stu-id="aad4f-114">2</span></span>   | <span data-ttu-id="aad4f-115">Set di caratteri del simbolo.</span><span class="sxs-lookup"><span data-stu-id="aad4f-115">The symbol character set.</span></span>                                                              |
| <span data-ttu-id="aad4f-116">128</span><span class="sxs-lookup"><span data-stu-id="aad4f-116">128</span></span> | <span data-ttu-id="aad4f-117">Set di caratteri a doppio byte (DBCS) univoco per la versione giapponese di Windows.</span><span class="sxs-lookup"><span data-stu-id="aad4f-117">Double-byte character set (DBCS) unique to the Japanese version of Windows.</span></span>            |
| <span data-ttu-id="aad4f-118">129</span><span class="sxs-lookup"><span data-stu-id="aad4f-118">129</span></span> | <span data-ttu-id="aad4f-119">Set di caratteri a doppio byte (DBCS) univoco per la versione coreana di Windows.</span><span class="sxs-lookup"><span data-stu-id="aad4f-119">Double-byte character set (DBCS) unique to the Korean version of Windows.</span></span>              |
| <span data-ttu-id="aad4f-120">134</span><span class="sxs-lookup"><span data-stu-id="aad4f-120">134</span></span> | <span data-ttu-id="aad4f-121">Set di caratteri a doppio byte (DBCS) univoco per la versione in cinese semplificato di Windows.</span><span class="sxs-lookup"><span data-stu-id="aad4f-121">Double-byte character set (DBCS) unique to the Simplified Chinese version of Windows.</span></span>  |
| <span data-ttu-id="aad4f-122">136</span><span class="sxs-lookup"><span data-stu-id="aad4f-122">136</span></span> | <span data-ttu-id="aad4f-123">Set di caratteri a doppio byte (DBCS) univoco per la versione cinese tradizionale di Windows.</span><span class="sxs-lookup"><span data-stu-id="aad4f-123">Double-byte character set (DBCS) unique to the Traditional Chinese version of Windows.</span></span> |
| <span data-ttu-id="aad4f-124">255</span><span class="sxs-lookup"><span data-stu-id="aad4f-124">255</span></span> | <span data-ttu-id="aad4f-125">Caratteri estesi generalmente visualizzati dalle applicazioni MS-DOS.</span><span class="sxs-lookup"><span data-stu-id="aad4f-125">Extended characters usually displayed by MS-DOS applications.</span></span>                          |



 

</dd> </dl>

<span data-ttu-id="aad4f-126">Per altri valori del set di caratteri, vedere la documentazione di Platform SDK.</span><span class="sxs-lookup"><span data-stu-id="aad4f-126">For other character set values, consult the Platform SDK documentation.</span></span>

<span data-ttu-id="aad4f-127">Il set di caratteri predefinito utilizzato nella parola Balloon di un carattere viene definito nell'editor dei caratteri di Microsoft Agent.</span><span class="sxs-lookup"><span data-stu-id="aad4f-127">The default character set used in a character's word balloon is defined in the Microsoft Agent Character Editor.</span></span> <span data-ttu-id="aad4f-128">È possibile modificarlo con [**IAgentBalloon:: SetFontCharSet**](https://www.bing.com/search?q=**IAgentBalloon::SetFontCharSet**).</span><span class="sxs-lookup"><span data-stu-id="aad4f-128">You can change it with [**IAgentBalloon::SetFontCharSet**](https://www.bing.com/search?q=**IAgentBalloon::SetFontCharSet**).</span></span> <span data-ttu-id="aad4f-129">Tuttavia, l'utente può eseguire l'override dell'impostazione del set di caratteri per tutti i caratteri utilizzando la finestra delle proprietà di Microsoft Agent.</span><span class="sxs-lookup"><span data-stu-id="aad4f-129">However, the user can override the character set setting for all characters using the Microsoft Agent property sheet.</span></span> <span data-ttu-id="aad4f-130">Questa proprietà si applica solo all'utilizzo del carattere da parte dell'applicazione client. l'impostazione non influisce sugli altri client del carattere o di altri caratteri dell'applicazione client.</span><span class="sxs-lookup"><span data-stu-id="aad4f-130">This property applies only to your client application's use of the character; the setting does not affect other clients of the character or other characters of your client application.</span></span>

## <a name="see-also"></a><span data-ttu-id="aad4f-131">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="aad4f-131">See Also</span></span>

[<span data-ttu-id="aad4f-132">**IAgentBalloon::GetFontCharSet**</span><span class="sxs-lookup"><span data-stu-id="aad4f-132">**IAgentBalloon::GetFontCharSet**</span></span>](iagentballoon--getfontcharset.md)


 

 




