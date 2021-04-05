---
title: Riferimento a interfacce in URL
description: Riferimento a interfacce in URL
ms.assetid: 9ae30c12-2dee-46b2-90e2-c101a83856fb
keywords:
- Windows Media Player Skin, riferimenti URL
- interfacce, riferimenti URL
- Riferimenti URL nelle interfacce
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 75b33ac9a5f37dce242797ae93dc4e85b973c76b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103714047"
---
# <a name="referencing-skins-in-urls"></a><span data-ttu-id="9b18d-106">Riferimento a interfacce in URL</span><span class="sxs-lookup"><span data-stu-id="9b18d-106">Referencing Skins in URLs</span></span>

<span data-ttu-id="9b18d-107">Se si utilizza un URL per caricare un file multimediale che verrà riprodotto da Windows Media Player, è possibile richiedere l'utilizzo di una particolare interfaccia con tale file.</span><span class="sxs-lookup"><span data-stu-id="9b18d-107">If you use a URL to load a media file that will be played by Windows Media Player, you can request that a particular skin be used with that file.</span></span> <span data-ttu-id="9b18d-108">Se l'interfaccia è già installata nel computer dell'utente, verrà utilizzata. in caso contrario, verrà utilizzata l'interfaccia precedente.</span><span class="sxs-lookup"><span data-stu-id="9b18d-108">If the skin is already installed on the user's machine, it will be used; otherwise the previous skin will be used.</span></span>

<span data-ttu-id="9b18d-109">Per richiedere un'interfaccia personalizzata, aggiungere quanto segue alla fine dell'URL:</span><span class="sxs-lookup"><span data-stu-id="9b18d-109">To request a skin, add the following to the end of the URL:</span></span>


```C++
?WMPSkin=skinname
```



<span data-ttu-id="9b18d-110">*SkinName* è il nome dell'interfaccia che si vuole richiedere.</span><span class="sxs-lookup"><span data-stu-id="9b18d-110">*skinname* is the name of the skin you want to request.</span></span> <span data-ttu-id="9b18d-111">Non usare le virgolette intorno al nome dell'interfaccia.</span><span class="sxs-lookup"><span data-stu-id="9b18d-111">Do not use quotes around the name of the skin.</span></span>

<span data-ttu-id="9b18d-112">Per richiedere, ad esempio, l'utilizzo dell'interfaccia Headspace, digitare l'URL http seguente:</span><span class="sxs-lookup"><span data-stu-id="9b18d-112">For example, to request the headspace skin be used, type the following http URL:</span></span>


```C++
https://www.proseware.com/mymedia.wma?WMPSkin=headspace

```



## <a name="related-topics"></a><span data-ttu-id="9b18d-113">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="9b18d-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9b18d-114">**Informazioni sulle interfacce**</span><span class="sxs-lookup"><span data-stu-id="9b18d-114">**About Skins**</span></span>](about-skins.md)
</dt> </dl>

 

 




