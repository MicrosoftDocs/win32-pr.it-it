---
description: Viene illustrata la chiave del registro di sistema da impostare per impedire AutoPlay.
ms.assetid: E0A25DC2-0991-45D6-9185-019DB4C040AD
title: Come impedire AutoPlay per un componente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2ebe03473ce7c5eb441ec428cbe4d060dc62f042
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104979530"
---
# <a name="how-to-prevent-autoplay-for-a-component"></a><span data-ttu-id="402b3-103">Come impedire AutoPlay per un componente</span><span class="sxs-lookup"><span data-stu-id="402b3-103">How to Prevent AutoPlay for a Component</span></span>

<span data-ttu-id="402b3-104">Viene illustrata la chiave del registro di sistema da impostare per impedire AutoPlay.</span><span class="sxs-lookup"><span data-stu-id="402b3-104">Illustrates which registry key must be set to prevent AutoPlay.</span></span>

## <a name="instructions"></a><span data-ttu-id="402b3-105">Istruzioni</span><span class="sxs-lookup"><span data-stu-id="402b3-105">Instructions</span></span>


<span data-ttu-id="402b3-106">Per impedire l'avvio di AutoPlay in risposta a un evento, aggiungere il seguente valore **reg \_ SZ** , come illustrato in questo esempio.</span><span class="sxs-lookup"><span data-stu-id="402b3-106">To prevent AutoPlay from launching in response to an event, add the following **REG\_SZ** value, as shown in this example.</span></span>

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Microsoft
         Windows
            CurrentVersion
               Explorer
                  AutoplayHandlers
                     CancelAutoplay
                        CLSID
                           00000000-0000-0000-0000-000000000000
```

<span data-ttu-id="402b3-107">Il valore è l'identificatore di classe (CLSID) in base al quale il componente che genera l'evento è noto nella tabella degli oggetti in esecuzione (ROT).</span><span class="sxs-lookup"><span data-stu-id="402b3-107">The value is the class identifier (CLSID) that the component that is generating the event is known by in the running object table (ROT).</span></span> <span data-ttu-id="402b3-108">Il valore non contiene dati.</span><span class="sxs-lookup"><span data-stu-id="402b3-108">The value has no data.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="402b3-109">Sotto questa chiave, i CLSID non sono racchiusi tra parentesi graffe ( {} ).</span><span class="sxs-lookup"><span data-stu-id="402b3-109">Under this key, the CLSIDs are not enclosed in braces ( {} ).</span></span>

 

 

 



