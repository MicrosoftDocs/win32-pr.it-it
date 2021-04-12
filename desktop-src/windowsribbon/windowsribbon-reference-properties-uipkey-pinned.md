---
title: UI_PKEY_Pinned
description: Identifica la proprietà bloccata dell'interfaccia utente \_ pkey \_ .
ms.assetid: 906b2ab9-1ed7-46a6-88bc-e8f9160ab60c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8637f11404090313751647058ee41acbad3d9bf8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104221738"
---
# <a name="ui_pkey_pinned"></a><span data-ttu-id="5c64d-103">Interfaccia utente \_ pkey \_ bloccata</span><span class="sxs-lookup"><span data-stu-id="5c64d-103">UI\_PKEY\_Pinned</span></span>

<span data-ttu-id="5c64d-104">Identifica la proprietà bloccata dell'interfaccia utente \_ pkey \_ .</span><span class="sxs-lookup"><span data-stu-id="5c64d-104">Identifies the UI\_PKEY\_Pinned property.</span></span>

```
propertyDescription
   name = UI_PKEY_Pinned
   shellPKey = UI_PKEY_Pinned
   formatID = 00000351-7363-696e-8441798acf5aebb7
   propID = 351
   typeInfo
      type = VT_BOOL
   booleanFormat
      formatAs = VARIANT_TRUE=-1, VARIANT_FALSE=0
```

## <a name="remarks"></a><span data-ttu-id="5c64d-105">Commenti</span><span class="sxs-lookup"><span data-stu-id="5c64d-105">Remarks</span></span>

<span data-ttu-id="5c64d-106">L'interfaccia utente \_ pkey aggiunta \_ viene usata da un'applicazione per eseguire una query per verificare se un elemento nel [menu dell'applicazione](windowsribbon-controls-applicationmenu.md) è "bloccato" o persistente tra le istanze dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="5c64d-106">UI\_PKEY\_Pinned is used by an application to query whether an item in the [Application Menu](windowsribbon-controls-applicationmenu.md) is "pinned", or persistent, across application instances.</span></span> <span data-ttu-id="5c64d-107">Ad esempio, un elemento nell'elenco degli elementi usati di recente (MRU) è accessibile e non rilascia l'elenco di elementi MRU finché non è "sbloccato".</span><span class="sxs-lookup"><span data-stu-id="5c64d-107">For example, an item in the most recently used (MRU) items list is accessible and does not drop off the MRU items list until it is "unpinned".</span></span>

## <a name="related-topics"></a><span data-ttu-id="5c64d-108">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="5c64d-108">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5c64d-109">Proprietà stato</span><span class="sxs-lookup"><span data-stu-id="5c64d-109">State Properties</span></span>](windowsribbon-reference-properties-state.md)
</dt> <dt>

[<span data-ttu-id="5c64d-110">Interfaccia utente \_ pkey \_ RecentItems</span><span class="sxs-lookup"><span data-stu-id="5c64d-110">UI\_PKEY\_RecentItems</span></span>](windowsribbon-reference-properties-uipkey-recentitems.md)
</dt> <dt>

[<span data-ttu-id="5c64d-111">Elementi recenti</span><span class="sxs-lookup"><span data-stu-id="5c64d-111">Recent Items</span></span>](windowsribbon-controls-recentitems.md)
</dt> </dl>

 

 




