---
description: Sospensione
ms.assetid: 945e1b1a-2557-4be2-bfdb-bb11ac7c3fe8
title: Sospensione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 15f113bdaa41709055202886112d678c2a1fbb172d99e880ceaafc997817412a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119997281"
---
# <a name="pausing"></a>Sospensione

Tutte le modifiche dello stato del filtro devono contenere il blocco del filtro. Nel metodo **Pause** creare le risorse necessarie per il filtro:


```C++
HRESULT CMyFilter::Pause()
{
    CAutoLock lock_it(m_pLock);

    /* Create filter resources. */

    return CBaseFilter::Pause();
}
```



Il [**metodo CBaseFilter::P ause**](cbasefilter-pause.md) imposta lo stato corretto sul filtro (Stato sospeso) e chiama il metodo \_ [**CBasePin::Active**](cbasepin-active.md) su ogni pin connesso nel filtro. Il **metodo Active** informa il pin che il filtro è diventato attivo. Se il segnaposto crea risorse, eseguire l'override **del metodo Active,** come indicato di seguito:


```C++
HRESULT CMyInputPin::Active()
{
    // You do not need to hold the filter lock here. It is already held in Pause.

    /* Create pin resources. */

    return CBaseInputPin::Active()
}
```



 

 



