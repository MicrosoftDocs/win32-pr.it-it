---
description: Stopping
ms.assetid: e2796b69-05e5-4ced-b238-257952d81211
title: Stopping
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5a93bde3b504400eed59190bf1651828f2f4509a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103884142"
---
# <a name="stopping"></a>Stopping

Il metodo **Stop** deve sbloccare il metodo **Receive** ed eseguire il decommit degli allocatori del filtro. Il commit di un allocatore impone la restituzione di tutte le chiamate a **GetBuffer** in sospeso, che sbloccano i filtri upstream in attesa di campioni. Il metodo **Stop** include il blocco del filtro e quindi chiama il metodo [**CBaseFilter:: Stop**](cbasefilter-stop.md) , che chiama [**CBasePin:: inactive**](cbasepin-inactive.md) su tutti i pin del filtro:


```C++
HRESULT CMyFilter::Stop()
{
    CAutoLock lock_it(m_pLock);
    // Inactivate all the pins, to protect the filter resources.
    hr = CBaseFilter::Stop();

    /* Safe to destroy filter resources used by the streaming thread. */

    return hr;
}
```



Eseguire l'override del metodo **inattivo** del PIN di input come indicato di seguito:


```C++
HRESULT CMyInputPin::Inactive()
{
    // You do not need to hold the filter lock here. 
    // It is already locked in Stop.

    // Unblock Receive.
    SetEvent(m_hSomeEventThatReceiveNeedsToWaitOn);

    // Make sure Receive will fail. 
    // This also decommits the allocator.
    HRESULT hr = CBaseInputPin::Inactive();

    // Make sure Receive has completed, and is not using resources.
    {
        CAutoLock c(&m_csReceive);

        /* It is now safe to destroy filter resources used by the
           streaming thread. */
    }
    return hr;
}
```



 

 



