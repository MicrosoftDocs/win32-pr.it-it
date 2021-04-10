---
description: Gestione delle notifiche degli eventi DVD
ms.assetid: 7a12aa36-f709-4ee2-aac6-45ab273ad3f9
title: Gestione delle notifiche degli eventi DVD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8212f3eb9f868c494aa008602713c1750a6c6dc9
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "103965819"
---
# <a name="handling-dvd-event-notifications"></a>Gestione delle notifiche degli eventi DVD

Il navigatore DVD invia notifiche a una finestra specificata dall'applicazione quando si verificano determinati eventi, ad esempio quando viene modificato il dominio DVD, quando viene rilevato un nuovo livello di gestione padre e quando il navigatore DVD sta per entrare in un blocco angolo. I parametri evento possono contenere informazioni aggiuntive correlate all'evento. Anche i messaggi di errore e gli avvisi vengono inviati in questo modo. L'applicazione specifica la finestra che gestirà le notifiche degli eventi usando il puntatore [**IMediaEventEx**](/windows/desktop/api/Control/nn-control-imediaeventex) per chiamare [**SetNotifyWindow**](/windows/desktop/api/Control/nf-control-imediaeventex-setnotifywindow), come indicato di seguito:


```C++
const DWORD WM_DVD_EVENT = WM_USER + 100;
hr = m_pIME->SetNotifyWindow(reinterpret_cast<OAHWND>(m_hWnd), WM_DVD_EVENT, 0);
```



Nell'esempio precedente m \_ hWnd è l'HWND della finestra per ricevere i messaggi e l' \_ evento WM DVD \_ è il messaggio definito dall'applicazione (maggiore di WM \_ User) che segnalerà che si è verificato un evento DVD. L'evento stesso viene recuperato dall'applicazione tramite una chiamata a [**IMediaEvent:: GetEvent**](/windows/desktop/api/Control/nf-control-imediaevent-getevent). Poiché più di un evento potrebbe trovarsi nella coda degli eventi in un determinato momento, l'applicazione deve chiamare **GetEvent** all'interno di un ciclo che si ripete fino a quando non vengono recuperati tutti gli eventi in coda, come illustrato nell'esempio di codice seguente.


```C++
while (SUCCEEDED(m_pIME->GetEvent(&lEvent, &lParam1, &lParam2, lTimeOut)))
{
    HRESULT hr;
    switch (lEvent)
    {

    case EC_DVD_CURRENT_HMSF_TIME:
        {
            DVD_HMSF_TIMECODE *pTC = reinterpret_cast<DVD_HMSF_TIMECODE *>(&lParam1);
            m_CurTime = *pTC;
            ...
        }
        break;
        ...
    } // switch
}
```



Gli eventi DVD possono contenere informazioni aggiuntive nei parametri *lParam1* o *lParam2* , come illustrato in precedenza, in cui l'ora corrente è inclusa in *lParam1*. L'esempio di codice precedente è riportato nell'applicazione di esempio DVD in Dvdcore. cpp. Per un elenco completo di tutti gli eventi DVD e dei relativi parametri, vedere la pagina relativa ai [codici di notifica degli eventi DVD](dvd-notification-codes.md).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Applicazioni DVD](dvd-applications.md)
</dt> </dl>

 

 



