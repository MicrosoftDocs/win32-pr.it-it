---
title: IAgentBalloon SetFontCharSet
description: IAgentBalloon SetFontCharSet
ms.assetid: ce1b152d-c8af-47ec-9e6b-5768dbcf3566
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 18cc462895ff9f19f7e722660608a268af13446f
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/30/2021
ms.locfileid: "113120206"
---
# <a name="iagentballoonsetfontcharset"></a><span data-ttu-id="5a38f-103">IAgentBalloon::SetFontCharSet</span><span class="sxs-lookup"><span data-stu-id="5a38f-103">IAgentBalloon::SetFontCharSet</span></span>

<span data-ttu-id="5a38f-104">\[Microsoft Agent è deprecato a livello di Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="5a38f-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT SetFontCharSet(
   short sFontCharSet  // character set displayed in word balloon
); 
```

<span data-ttu-id="5a38f-105">Imposta il set di caratteri del tipo di carattere visualizzato nel fumetto.</span><span class="sxs-lookup"><span data-stu-id="5a38f-105">Sets the character set of the font displayed in the word balloon.</span></span>

-   <span data-ttu-id="5a38f-106">Restituisce S \_ OK per indicare che l'operazione è riuscita.</span><span class="sxs-lookup"><span data-stu-id="5a38f-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="5a38f-107"><span id="sFontCharSet"></span><span id="sfontcharset"></span><span id="SFONTCHARSET"></span>*sFontCharSet*</span><span class="sxs-lookup"><span data-stu-id="5a38f-107"><span id="sFontCharSet"></span><span id="sfontcharset"></span><span id="SFONTCHARSET"></span>*sFontCharSet*</span></span>
</dt> <dd>

<span data-ttu-id="5a38f-108">Set di caratteri del tipo di carattere.</span><span class="sxs-lookup"><span data-stu-id="5a38f-108">The character set of the font.</span></span> <span data-ttu-id="5a38f-109">Di seguito sono riportate alcune impostazioni comuni per value:</span><span class="sxs-lookup"><span data-stu-id="5a38f-109">The following are some common settings for value:</span></span>



| <span data-ttu-id="5a38f-110">Valore</span><span class="sxs-lookup"><span data-stu-id="5a38f-110">Value</span></span>    | <span data-ttu-id="5a38f-111">Set di caratteri</span><span class="sxs-lookup"><span data-stu-id="5a38f-111">Character set</span></span>                                                                                       |
|-----|----------------------------------------------------------------------------------------|
| <span data-ttu-id="5a38f-112">0</span><span class="sxs-lookup"><span data-stu-id="5a38f-112">0</span></span>   | <span data-ttu-id="5a38f-113">Caratteri Windows standard (ANSI).</span><span class="sxs-lookup"><span data-stu-id="5a38f-113">Standard Windows characters (ANSI).</span></span>                                                    |
| <span data-ttu-id="5a38f-114">1</span><span class="sxs-lookup"><span data-stu-id="5a38f-114">1</span></span>   | <span data-ttu-id="5a38f-115">Set di caratteri predefinito.</span><span class="sxs-lookup"><span data-stu-id="5a38f-115">Default character set.</span></span>                                                                 |
| <span data-ttu-id="5a38f-116">2</span><span class="sxs-lookup"><span data-stu-id="5a38f-116">2</span></span>   | <span data-ttu-id="5a38f-117">Set di caratteri dei simboli.</span><span class="sxs-lookup"><span data-stu-id="5a38f-117">The symbol character set.</span></span>                                                              |
| <span data-ttu-id="5a38f-118">128</span><span class="sxs-lookup"><span data-stu-id="5a38f-118">128</span></span> | <span data-ttu-id="5a38f-119">Set di caratteri a byte doppio (DBCS) univoco per la versione giapponese di Windows.</span><span class="sxs-lookup"><span data-stu-id="5a38f-119">Double-byte character set (DBCS) unique to the Japanese version of Windows.</span></span>            |
| <span data-ttu-id="5a38f-120">129</span><span class="sxs-lookup"><span data-stu-id="5a38f-120">129</span></span> | <span data-ttu-id="5a38f-121">Set di caratteri a byte doppio (DBCS) univoco per la versione coreana di Windows.</span><span class="sxs-lookup"><span data-stu-id="5a38f-121">Double-byte character set (DBCS) unique to the Korean version of Windows.</span></span>              |
| <span data-ttu-id="5a38f-122">134</span><span class="sxs-lookup"><span data-stu-id="5a38f-122">134</span></span> | <span data-ttu-id="5a38f-123">Set di caratteri a byte doppio (DBCS) univoco per la versione in cinese semplificato di Windows.</span><span class="sxs-lookup"><span data-stu-id="5a38f-123">Double-byte character set (DBCS) unique to the Simplified Chinese version of Windows.</span></span>  |
| <span data-ttu-id="5a38f-124">136</span><span class="sxs-lookup"><span data-stu-id="5a38f-124">136</span></span> | <span data-ttu-id="5a38f-125">Set di caratteri a byte doppio (DBCS) univoco per la versione in cinese tradizionale di Windows.</span><span class="sxs-lookup"><span data-stu-id="5a38f-125">Double-byte character set (DBCS) unique to the Traditional Chinese version of Windows.</span></span> |
| <span data-ttu-id="5a38f-126">255</span><span class="sxs-lookup"><span data-stu-id="5a38f-126">255</span></span> | <span data-ttu-id="5a38f-127">Caratteri estesi in genere visualizzati dalle applicazioni MS-DOS.</span><span class="sxs-lookup"><span data-stu-id="5a38f-127">Extended characters usually displayed by MS-DOS applications.</span></span>                          |



 

</dd> </dl>

<span data-ttu-id="5a38f-128">Per altri valori del set di caratteri, vedere la documentazione di Platform SDK.</span><span class="sxs-lookup"><span data-stu-id="5a38f-128">For other character set values, consult the Platform SDK documentation.</span></span>

<span data-ttu-id="5a38f-129">Il set di caratteri predefinito usato nel fumetto delle parole di un carattere è definito nell'editor di caratteri di Microsoft Agent.</span><span class="sxs-lookup"><span data-stu-id="5a38f-129">The default character set used in a character's word balloon is defined in the Microsoft Agent Character Editor.</span></span> <span data-ttu-id="5a38f-130">È possibile modificarlo con [**IAgentBalloon::SetFontCharSet**](https://www.bing.com/search?q=**IAgentBalloon::SetFontCharSet**).</span><span class="sxs-lookup"><span data-stu-id="5a38f-130">You can change it with [**IAgentBalloon::SetFontCharSet**](https://www.bing.com/search?q=**IAgentBalloon::SetFontCharSet**).</span></span> <span data-ttu-id="5a38f-131">Tuttavia, l'utente può eseguire l'override dell'impostazione del set di caratteri per tutti i caratteri usando la finestra delle proprietà di Microsoft Agent.</span><span class="sxs-lookup"><span data-stu-id="5a38f-131">However, the user can override the character set setting for all characters using the Microsoft Agent property sheet.</span></span> <span data-ttu-id="5a38f-132">Questa proprietà si applica solo all'uso del carattere da parte dell'applicazione client. L'impostazione non influisce su altri client del carattere o di altri caratteri dell'applicazione client.</span><span class="sxs-lookup"><span data-stu-id="5a38f-132">This property applies only to your client application's use of the character; the setting does not affect other clients of the character or other characters of your client application.</span></span>

## <a name="see-also"></a><span data-ttu-id="5a38f-133">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="5a38f-133">See Also</span></span>

[<span data-ttu-id="5a38f-134">**IAgentBalloon::GetFontCharSet**</span><span class="sxs-lookup"><span data-stu-id="5a38f-134">**IAgentBalloon::GetFontCharSet**</span></span>](iagentballoon--getfontcharset.md)


 

 




