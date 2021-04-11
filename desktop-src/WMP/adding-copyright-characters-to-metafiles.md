---
title: Aggiunta di caratteri di copyright a metafile
description: I caratteri per il copyright e i simboli di registrazione dei marchi (\ 169; o \ 174;) potrebbero non essere visualizzati correttamente se il metafile non è codificato con lo schema di codifica UTF-8.
ms.assetid: 9124c8d4-1fc1-4163-ada9-d96af58f8b98
keywords:
- Aggiunta di caratteri di copyright a file di Windows Media Player
topic_type:
- apiref
api_name:
- Adding Copyright Characters to Metafiles
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 6e71b116a3500fdb4217613c81bd4f041af75a66
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/25/2019
ms.locfileid: "104333967"
---
# <a name="adding-copyright-characters-to-metafiles"></a><span data-ttu-id="fc112-104">Aggiunta di caratteri di copyright a metafile</span><span class="sxs-lookup"><span data-stu-id="fc112-104">Adding Copyright Characters to Metafiles</span></span>

<span data-ttu-id="fc112-105">I caratteri per il copyright e i simboli di registrazione dei marchi (© o®) potrebbero non essere visualizzati correttamente se il metafile non è codificato con lo schema di codifica UTF-8.</span><span class="sxs-lookup"><span data-stu-id="fc112-105">The characters for copyright and trademark registration symbols ( © or ® ) may not display correctly if the metafile is not encoded using the UTF-8 encoding scheme.</span></span> <span data-ttu-id="fc112-106">In questo caso, per visualizzare correttamente uno di questi simboli per tutti gli utenti, è possibile usare gli equivalenti ASCII (c) e (r) all'interno dell'elemento **Copyright** , come illustrato nel codice seguente.</span><span class="sxs-lookup"><span data-stu-id="fc112-106">In this case, to display either of these symbols properly for all users, you can use the ASCII equivalents (c) and (r) inside the **COPYRIGHT** element, as shown in the following code.</span></span>


```
<COPYRIGHT>Copyright (c) 1998, Microsoft Corporation</COPYRIGHT>
```



<span data-ttu-id="fc112-107">Se il metafile è codificato con UTF-8, i simboli del copyright e dei marchi vengono visualizzati correttamente.</span><span class="sxs-lookup"><span data-stu-id="fc112-107">If the metafile is encoded using UTF-8, copyright and trademark symbols will display correctly.</span></span>

## <a name="see-also"></a><span data-ttu-id="fc112-108">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="fc112-108">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fc112-109">**Riferimento agli elementi metafile di Windows Media**</span><span class="sxs-lookup"><span data-stu-id="fc112-109">**Windows Media Metafile Elements Reference**</span></span>](windows-media-metafile-elements-reference.md)
</dt> </dl>

 

 




