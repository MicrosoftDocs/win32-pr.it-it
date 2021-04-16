---
title: Sezione Marquee di esempio
description: Sezione Marquee di esempio
ms.assetid: 44ed3257-2e1a-4b8d-9d55-a13b0400422d
keywords:
- Interfacce di Windows Media Player Mobile, Marquees
- interfacce, Marquee
- riferimento per Skin, Marquees
- Marquees in Skins, sezione Marquee
- file di definizione dell'interfaccia, sezione Marquee
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0f66588d81b22051a9289a80c8733d5cfe154bed
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104471603"
---
# <a name="sample-marquee-section"></a><span data-ttu-id="b3db0-108">Sezione Marquee di esempio</span><span class="sxs-lookup"><span data-stu-id="b3db0-108">Sample Marquee Section</span></span>

<span data-ttu-id="b3db0-109">Le righe seguenti mostrano una sezione di selezione tipica di un file di definizione dell'interfaccia personalizzata:</span><span class="sxs-lookup"><span data-stu-id="b3db0-109">The following lines show a typical Marquee section of a skin definition file:</span></span>


```C++
//  <Location>   <Font>       <Color>      <Text item combinations>

//  ----------   ------       -------      ------------------------

    3,2,234,20   Tahoma,12,N  255,0,0    Title+Author, Title, Author


```



<span data-ttu-id="b3db0-110">Definisce una casella di visualizzazione Marquee che mostra il titolo e l'autore se sono definiti entrambi, il titolo se è stato definito solo il titolo o il nome dell'autore se è definito solo l'autore.</span><span class="sxs-lookup"><span data-stu-id="b3db0-110">This defines a marquee display box that shows the title and author if both are defined, the title if only Title is defined, or the name of the author if only Author is defined.</span></span> <span data-ttu-id="b3db0-111">Se non viene definito alcun elemento, non verrà visualizzato nulla.</span><span class="sxs-lookup"><span data-stu-id="b3db0-111">If neither is defined, nothing will be displayed.</span></span>

## <a name="related-topics"></a><span data-ttu-id="b3db0-112">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="b3db0-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b3db0-113">**Testo scorrevole**</span><span class="sxs-lookup"><span data-stu-id="b3db0-113">**Marquee**</span></span>](marquee.md)
</dt> </dl>

 

 




