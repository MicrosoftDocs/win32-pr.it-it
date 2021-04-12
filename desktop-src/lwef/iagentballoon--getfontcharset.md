---
title: IAgentBalloon GetFontCharSet
description: IAgentBalloon GetFontCharSet
ms.assetid: 1ab5767a-31e3-449c-b242-f20b11336ca0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 54f544df6c09fb00d346015b610751dd23738820
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104221603"
---
# <a name="iagentballoongetfontcharset"></a><span data-ttu-id="d7d49-103">IAgentBalloon::GetFontCharSet</span><span class="sxs-lookup"><span data-stu-id="d7d49-103">IAgentBalloon::GetFontCharSet</span></span>

<span data-ttu-id="d7d49-104">\[Microsoft Agent è stato deprecato a partire da Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="d7d49-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT GetFontCharSet(
   short * psFontCharSet  // character set displayed in word balloon
); 
```

<span data-ttu-id="d7d49-105">Indica il set di caratteri del tipo di carattere visualizzato in un fumetto di Word.</span><span class="sxs-lookup"><span data-stu-id="d7d49-105">Indicates the character set of the font displayed in a word balloon.</span></span>

-   <span data-ttu-id="d7d49-106">Restituisce \_ OK per indicare che l'operazione è stata completata.</span><span class="sxs-lookup"><span data-stu-id="d7d49-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="d7d49-107"><span id="psFontCharSet"></span><span id="psfontcharset"></span><span id="PSFONTCHARSET"></span>*psFontCharSet*</span><span class="sxs-lookup"><span data-stu-id="d7d49-107"><span id="psFontCharSet"></span><span id="psfontcharset"></span><span id="PSFONTCHARSET"></span>*psFontCharSet*</span></span>
</dt> <dd>

<span data-ttu-id="d7d49-108">Indirizzo di un valore che riceve il set di caratteri del tipo di carattere.</span><span class="sxs-lookup"><span data-stu-id="d7d49-108">The address of a value that receives the font's character set.</span></span> <span data-ttu-id="d7d49-109">Di seguito sono riportate alcune impostazioni comuni per value:</span><span class="sxs-lookup"><span data-stu-id="d7d49-109">The following are some common settings for value:</span></span>



|     |                                                                                        |
|-----|----------------------------------------------------------------------------------------|
| <span data-ttu-id="d7d49-110">0</span><span class="sxs-lookup"><span data-stu-id="d7d49-110">0</span></span>   | <span data-ttu-id="d7d49-111">Caratteri Windows standard (ANSI).</span><span class="sxs-lookup"><span data-stu-id="d7d49-111">Standard Windows characters (ANSI).</span></span>                                                    |
| <span data-ttu-id="d7d49-112">1</span><span class="sxs-lookup"><span data-stu-id="d7d49-112">1</span></span>   | <span data-ttu-id="d7d49-113">Set di caratteri predefinito.</span><span class="sxs-lookup"><span data-stu-id="d7d49-113">Default character set.</span></span>                                                                 |
| <span data-ttu-id="d7d49-114">2</span><span class="sxs-lookup"><span data-stu-id="d7d49-114">2</span></span>   | <span data-ttu-id="d7d49-115">Set di caratteri del simbolo.</span><span class="sxs-lookup"><span data-stu-id="d7d49-115">The symbol character set.</span></span>                                                              |
| <span data-ttu-id="d7d49-116">128</span><span class="sxs-lookup"><span data-stu-id="d7d49-116">128</span></span> | <span data-ttu-id="d7d49-117">Set di caratteri a doppio byte (DBCS) univoco per la versione giapponese di Windows.</span><span class="sxs-lookup"><span data-stu-id="d7d49-117">Double-byte character set (DBCS) unique to the Japanese version of Windows.</span></span>            |
| <span data-ttu-id="d7d49-118">129</span><span class="sxs-lookup"><span data-stu-id="d7d49-118">129</span></span> | <span data-ttu-id="d7d49-119">Set di caratteri a doppio byte (DBCS) univoco per la versione coreana di Windows.</span><span class="sxs-lookup"><span data-stu-id="d7d49-119">Double-byte character set (DBCS) unique to the Korean version of Windows.</span></span>              |
| <span data-ttu-id="d7d49-120">134</span><span class="sxs-lookup"><span data-stu-id="d7d49-120">134</span></span> | <span data-ttu-id="d7d49-121">Set di caratteri a doppio byte (DBCS) univoco per la versione in cinese semplificato di Windows.</span><span class="sxs-lookup"><span data-stu-id="d7d49-121">Double-byte character set (DBCS) unique to the Simplified Chinese version of Windows.</span></span>  |
| <span data-ttu-id="d7d49-122">136</span><span class="sxs-lookup"><span data-stu-id="d7d49-122">136</span></span> | <span data-ttu-id="d7d49-123">Set di caratteri a doppio byte (DBCS) univoco per la versione cinese tradizionale di Windows.</span><span class="sxs-lookup"><span data-stu-id="d7d49-123">Double-byte character set (DBCS) unique to the Traditional Chinese version of Windows.</span></span> |
| <span data-ttu-id="d7d49-124">255</span><span class="sxs-lookup"><span data-stu-id="d7d49-124">255</span></span> | <span data-ttu-id="d7d49-125">Caratteri estesi generalmente visualizzati dalle applicazioni MS-DOS.</span><span class="sxs-lookup"><span data-stu-id="d7d49-125">Extended characters usually displayed by MS-DOS applications.</span></span>                          |



 

</dd> </dl>

<span data-ttu-id="d7d49-126">Per altri valori del set di caratteri, vedere la documentazione di Platform SDK.</span><span class="sxs-lookup"><span data-stu-id="d7d49-126">For other character set values, consult the Platform SDK documentation.</span></span>

<span data-ttu-id="d7d49-127">Il set di caratteri predefinito utilizzato nella parola Balloon di un carattere viene definito nell'editor dei caratteri di Microsoft Agent.</span><span class="sxs-lookup"><span data-stu-id="d7d49-127">The default character set used in a character's word balloon is defined in the Microsoft Agent Character Editor.</span></span> <span data-ttu-id="d7d49-128">È possibile modificarlo utilizzando [**IAgentBalloon:: SetFontCharSet**](iagentballoon--setfontcharset.md).</span><span class="sxs-lookup"><span data-stu-id="d7d49-128">You can change it using [**IAgentBalloon::SetFontCharSet**](iagentballoon--setfontcharset.md).</span></span> <span data-ttu-id="d7d49-129">Tuttavia, l'utente può eseguire l'override dell'impostazione del set di caratteri per tutti i caratteri utilizzando la finestra delle proprietà di Microsoft Agent.</span><span class="sxs-lookup"><span data-stu-id="d7d49-129">However, the user can override the character set setting for all characters using the Microsoft Agent property sheet.</span></span>

## <a name="see-also"></a><span data-ttu-id="d7d49-130">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="d7d49-130">See Also</span></span>

[<span data-ttu-id="d7d49-131">**IAgentBalloon::SetFontCharSet**</span><span class="sxs-lookup"><span data-stu-id="d7d49-131">**IAgentBalloon::SetFontCharSet**</span></span>](iagentballoon--setfontcharset.md)


 

 




