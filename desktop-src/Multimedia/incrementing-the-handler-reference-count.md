---
title: Incremento del conteggio dei riferimenti del gestore
description: Incremento del conteggio dei riferimenti del gestore
ms.assetid: 9e71ce1f-5805-4240-9dcc-7e71fbabfe7e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5a990f2570fca0057156a39a955930cca2d71858
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104045202"
---
# <a name="incrementing-the-handler-reference-count"></a><span data-ttu-id="d2010-103">Incremento del conteggio dei riferimenti del gestore</span><span class="sxs-lookup"><span data-stu-id="d2010-103">Incrementing the Handler Reference Count</span></span>

<span data-ttu-id="d2010-104">Il metodo **AddRef** incrementa il conteggio dei riferimenti del gestore di flusso o del gestore di file.</span><span class="sxs-lookup"><span data-stu-id="d2010-104">The **AddRef** method increments the stream-hander or file-handler reference count.</span></span>


```C++
STDMETHODIMP_(ULONG) CAVIFileCF::AddRef() 
{ 
    return ++m_refs; 
} 

```



 

 




