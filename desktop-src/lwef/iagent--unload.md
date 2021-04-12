---
title: Scaricamento IAgent
description: Scaricamento IAgent
ms.assetid: 560301b3-c038-4c6e-b3f1-1203b618b67d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bc30d6c4c06c1d292a26a2f503477dcca651dd18
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "104337359"
---
# <a name="iagentunload"></a><span data-ttu-id="b3021-103">IAgent:: UnLoad</span><span class="sxs-lookup"><span data-stu-id="b3021-103">IAgent::UnLoad</span></span>

<span data-ttu-id="b3021-104">\[Microsoft Agent è stato deprecato a partire da Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="b3021-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT UnLoad(
   long * dwCharID  //character ID
);
```

<span data-ttu-id="b3021-105">Scarica i dati di tipo carattere per il carattere specificato dalla raccolta di [**caratteri**](/windows/desktop/lwef/the-characters-object) .</span><span class="sxs-lookup"><span data-stu-id="b3021-105">Unloads the character data for the specified character from the [**Characters**](/windows/desktop/lwef/the-characters-object) collection.</span></span>

-   <span data-ttu-id="b3021-106">Restituisce \_ OK per indicare che l'operazione è stata completata.</span><span class="sxs-lookup"><span data-stu-id="b3021-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="b3021-107"><span id="dwCharID"></span><span id="dwcharid"></span><span id="DWCHARID"></span>*dwCharID*</span><span class="sxs-lookup"><span data-stu-id="b3021-107"><span id="dwCharID"></span><span id="dwcharid"></span><span id="DWCHARID"></span>*dwCharID*</span></span>
</dt> <dd>

<span data-ttu-id="b3021-108">ID del carattere.</span><span class="sxs-lookup"><span data-stu-id="b3021-108">The character's ID.</span></span>

</dd> </dl>

<span data-ttu-id="b3021-109">Utilizzare questo metodo quando non è più necessario un carattere, per liberare memoria utilizzata per archiviare le informazioni sul carattere.</span><span class="sxs-lookup"><span data-stu-id="b3021-109">Use this method when you no longer need a character, to free up memory used to store information about the character.</span></span> <span data-ttu-id="b3021-110">Se si accede di nuovo al carattere, utilizzare il metodo [**Load**](load-method.md) .</span><span class="sxs-lookup"><span data-stu-id="b3021-110">If you access the character again, use the [**Load**](load-method.md) method.</span></span>

## <a name="see-also"></a><span data-ttu-id="b3021-111">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="b3021-111">See Also</span></span>

[<span data-ttu-id="b3021-112">**IAgent:: Load**</span><span class="sxs-lookup"><span data-stu-id="b3021-112">**IAgent::Load**</span></span>](iagent--load.md)


 

 