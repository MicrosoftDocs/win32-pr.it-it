---
title: IAgentBalloon GetFontCharSet
description: IAgentBalloon GetFontCharSet
ms.assetid: 1ab5767a-31e3-449c-b242-f20b11336ca0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f809fbd83e44259c96184c9f364a85151ec9ddde
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/30/2021
ms.locfileid: "113120406"
---
# <a name="iagentballoongetfontcharset"></a><span data-ttu-id="91517-103">IAgentBalloon::GetFontCharSet</span><span class="sxs-lookup"><span data-stu-id="91517-103">IAgentBalloon::GetFontCharSet</span></span>

<span data-ttu-id="91517-104">\[Microsoft Agent è deprecato a livello di Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="91517-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT GetFontCharSet(
   short * psFontCharSet  // character set displayed in word balloon
); 
```

<span data-ttu-id="91517-105">Indica il set di caratteri del tipo di carattere visualizzato in un fumetto di parole.</span><span class="sxs-lookup"><span data-stu-id="91517-105">Indicates the character set of the font displayed in a word balloon.</span></span>

-   <span data-ttu-id="91517-106">Restituisce S \_ OK per indicare che l'operazione è riuscita.</span><span class="sxs-lookup"><span data-stu-id="91517-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="91517-107"><span id="psFontCharSet"></span><span id="psfontcharset"></span><span id="PSFONTCHARSET"></span>*psFontCharSet*</span><span class="sxs-lookup"><span data-stu-id="91517-107"><span id="psFontCharSet"></span><span id="psfontcharset"></span><span id="PSFONTCHARSET"></span>*psFontCharSet*</span></span>
</dt> <dd>

<span data-ttu-id="91517-108">Indirizzo di un valore che riceve il set di caratteri del tipo di carattere.</span><span class="sxs-lookup"><span data-stu-id="91517-108">The address of a value that receives the font's character set.</span></span> <span data-ttu-id="91517-109">Di seguito sono riportate alcune impostazioni comuni per value:</span><span class="sxs-lookup"><span data-stu-id="91517-109">The following are some common settings for value:</span></span>



| <span data-ttu-id="91517-110">Valore</span><span class="sxs-lookup"><span data-stu-id="91517-110">Value</span></span>    | <span data-ttu-id="91517-111">Set di caratteri</span><span class="sxs-lookup"><span data-stu-id="91517-111">Character set</span></span>                                                                                       |
|-----|----------------------------------------------------------------------------------------|
| <span data-ttu-id="91517-112">0</span><span class="sxs-lookup"><span data-stu-id="91517-112">0</span></span>   | <span data-ttu-id="91517-113">Caratteri Windows standard (ANSI).</span><span class="sxs-lookup"><span data-stu-id="91517-113">Standard Windows characters (ANSI).</span></span>                                                    |
| <span data-ttu-id="91517-114">1</span><span class="sxs-lookup"><span data-stu-id="91517-114">1</span></span>   | <span data-ttu-id="91517-115">Set di caratteri predefinito.</span><span class="sxs-lookup"><span data-stu-id="91517-115">Default character set.</span></span>                                                                 |
| <span data-ttu-id="91517-116">2</span><span class="sxs-lookup"><span data-stu-id="91517-116">2</span></span>   | <span data-ttu-id="91517-117">Set di caratteri del simbolo.</span><span class="sxs-lookup"><span data-stu-id="91517-117">The symbol character set.</span></span>                                                              |
| <span data-ttu-id="91517-118">128</span><span class="sxs-lookup"><span data-stu-id="91517-118">128</span></span> | <span data-ttu-id="91517-119">Set di caratteri a byte doppio (DBCS) univoco per la versione giapponese di Windows.</span><span class="sxs-lookup"><span data-stu-id="91517-119">Double-byte character set (DBCS) unique to the Japanese version of Windows.</span></span>            |
| <span data-ttu-id="91517-120">129</span><span class="sxs-lookup"><span data-stu-id="91517-120">129</span></span> | <span data-ttu-id="91517-121">Set di caratteri a byte doppio (DBCS) univoco per la versione coreana di Windows.</span><span class="sxs-lookup"><span data-stu-id="91517-121">Double-byte character set (DBCS) unique to the Korean version of Windows.</span></span>              |
| <span data-ttu-id="91517-122">134</span><span class="sxs-lookup"><span data-stu-id="91517-122">134</span></span> | <span data-ttu-id="91517-123">Set di caratteri a byte doppio (DBCS) univoco per la versione in cinese semplificato di Windows.</span><span class="sxs-lookup"><span data-stu-id="91517-123">Double-byte character set (DBCS) unique to the Simplified Chinese version of Windows.</span></span>  |
| <span data-ttu-id="91517-124">136</span><span class="sxs-lookup"><span data-stu-id="91517-124">136</span></span> | <span data-ttu-id="91517-125">Set di caratteri a byte doppio (DBCS) univoco per la versione in cinese tradizionale di Windows.</span><span class="sxs-lookup"><span data-stu-id="91517-125">Double-byte character set (DBCS) unique to the Traditional Chinese version of Windows.</span></span> |
| <span data-ttu-id="91517-126">255</span><span class="sxs-lookup"><span data-stu-id="91517-126">255</span></span> | <span data-ttu-id="91517-127">Caratteri estesi in genere visualizzati dalle applicazioni MS-DOS.</span><span class="sxs-lookup"><span data-stu-id="91517-127">Extended characters usually displayed by MS-DOS applications.</span></span>                          |



 

</dd> </dl>

<span data-ttu-id="91517-128">Per altri valori del set di caratteri, vedere la documentazione di Platform SDK.</span><span class="sxs-lookup"><span data-stu-id="91517-128">For other character set values, consult the Platform SDK documentation.</span></span>

<span data-ttu-id="91517-129">Il set di caratteri predefinito usato nel fumetto di un carattere è definito nell'editor di caratteri di Microsoft Agent.</span><span class="sxs-lookup"><span data-stu-id="91517-129">The default character set used in a character's word balloon is defined in the Microsoft Agent Character Editor.</span></span> <span data-ttu-id="91517-130">È possibile modificarlo [**usando IAgentBalloon::SetFontCharSet**](iagentballoon--setfontcharset.md).</span><span class="sxs-lookup"><span data-stu-id="91517-130">You can change it using [**IAgentBalloon::SetFontCharSet**](iagentballoon--setfontcharset.md).</span></span> <span data-ttu-id="91517-131">Tuttavia, l'utente può eseguire l'override dell'impostazione del set di caratteri per tutti i caratteri usando la finestra delle proprietà di Microsoft Agent.</span><span class="sxs-lookup"><span data-stu-id="91517-131">However, the user can override the character set setting for all characters using the Microsoft Agent property sheet.</span></span>

## <a name="see-also"></a><span data-ttu-id="91517-132">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="91517-132">See Also</span></span>

[<span data-ttu-id="91517-133">**IAgentBalloon::SetFontCharSet**</span><span class="sxs-lookup"><span data-stu-id="91517-133">**IAgentBalloon::SetFontCharSet**</span></span>](iagentballoon--setfontcharset.md)


 

 




