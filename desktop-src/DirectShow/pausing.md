---
description: Sospensione
ms.assetid: 945e1b1a-2557-4be2-bfdb-bb11ac7c3fe8
title: Sospensione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a07f6f610c3cfac9361e1db40c0fcd37b90645b2
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104125013"
---
# <a name="pausing"></a><span data-ttu-id="cfc94-103">Sospensione</span><span class="sxs-lookup"><span data-stu-id="cfc94-103">Pausing</span></span>

<span data-ttu-id="cfc94-104">Tutte le modifiche dello stato del filtro devono mantenere il blocco del filtro.</span><span class="sxs-lookup"><span data-stu-id="cfc94-104">All filter state changes must hold the filter lock.</span></span> <span data-ttu-id="cfc94-105">Nel metodo **pause** creare le risorse necessarie per il filtro:</span><span class="sxs-lookup"><span data-stu-id="cfc94-105">In the **Pause** method, create any resources the filter needs:</span></span>


```C++
HRESULT CMyFilter::Pause()
{
    CAutoLock lock_it(m_pLock);

    /* Create filter resources. */

    return CBaseFilter::Pause();
}
```



<span data-ttu-id="cfc94-106">Il metodo [**CBaseFilter::P ause**](cbasefilter-pause.md) imposta lo stato corretto sul filtro (stato in \_ pausa) e chiama il metodo [**CBasePin:: Active**](cbasepin-active.md) su ogni pin connesso nel filtro.</span><span class="sxs-lookup"><span data-stu-id="cfc94-106">The [**CBaseFilter::Pause**](cbasefilter-pause.md) method sets the correct state on the filter (State\_Paused) and calls the [**CBasePin::Active**](cbasepin-active.md) method on every connected pin in the filter.</span></span> <span data-ttu-id="cfc94-107">Il metodo **attivo** informa il pin che il filtro è diventato attivo.</span><span class="sxs-lookup"><span data-stu-id="cfc94-107">The **Active** method informs the pin that the filter has become active.</span></span> <span data-ttu-id="cfc94-108">Se il pin crea risorse, eseguire l'override del metodo **attivo** , come indicato di seguito:</span><span class="sxs-lookup"><span data-stu-id="cfc94-108">If the pin creates resources, override the **Active** method, as follows:</span></span>


```C++
HRESULT CMyInputPin::Active()
{
    // You do not need to hold the filter lock here. It is already held in Pause.

    /* Create pin resources. */

    return CBaseInputPin::Active()
}
```



 

 



