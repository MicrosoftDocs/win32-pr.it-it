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
# <a name="handling-dvd-event-notifications"></a><span data-ttu-id="c433a-103">Gestione delle notifiche degli eventi DVD</span><span class="sxs-lookup"><span data-stu-id="c433a-103">Handling DVD Event Notifications</span></span>

<span data-ttu-id="c433a-104">Il navigatore DVD invia notifiche a una finestra specificata dall'applicazione quando si verificano determinati eventi, ad esempio quando viene modificato il dominio DVD, quando viene rilevato un nuovo livello di gestione padre e quando il navigatore DVD sta per entrare in un blocco angolo.</span><span class="sxs-lookup"><span data-stu-id="c433a-104">The DVD Navigator sends notifications to an application-specified window when certain events take place, such as when the DVD domain changes, when a new parental management level is encountered, and when the DVD Navigator is about to enter an angle block.</span></span> <span data-ttu-id="c433a-105">I parametri evento possono contenere informazioni aggiuntive correlate all'evento.</span><span class="sxs-lookup"><span data-stu-id="c433a-105">The event parameters can contain additional information related to the event.</span></span> <span data-ttu-id="c433a-106">Anche i messaggi di errore e gli avvisi vengono inviati in questo modo.</span><span class="sxs-lookup"><span data-stu-id="c433a-106">Error messages and warnings are also sent in this way.</span></span> <span data-ttu-id="c433a-107">L'applicazione specifica la finestra che gestirà le notifiche degli eventi usando il puntatore [**IMediaEventEx**](/windows/desktop/api/Control/nn-control-imediaeventex) per chiamare [**SetNotifyWindow**](/windows/desktop/api/Control/nf-control-imediaeventex-setnotifywindow), come indicato di seguito:</span><span class="sxs-lookup"><span data-stu-id="c433a-107">The application specifies the window that will handle the event notifications by using the [**IMediaEventEx**](/windows/desktop/api/Control/nn-control-imediaeventex) pointer to call [**SetNotifyWindow**](/windows/desktop/api/Control/nf-control-imediaeventex-setnotifywindow), as follows:</span></span>


```C++
const DWORD WM_DVD_EVENT = WM_USER + 100;
hr = m_pIME->SetNotifyWindow(reinterpret_cast<OAHWND>(m_hWnd), WM_DVD_EVENT, 0);
```



<span data-ttu-id="c433a-108">Nell'esempio precedente m \_ hWnd è l'HWND della finestra per ricevere i messaggi e l' \_ evento WM DVD \_ è il messaggio definito dall'applicazione (maggiore di WM \_ User) che segnalerà che si è verificato un evento DVD.</span><span class="sxs-lookup"><span data-stu-id="c433a-108">In the preceding example, m\_hWnd is the HWND of the window to receive the messages and WM\_DVD\_EVENT is the application-defined message (greater than WM\_USER) that will signal that a DVD event has taken place.</span></span> <span data-ttu-id="c433a-109">L'evento stesso viene recuperato dall'applicazione tramite una chiamata a [**IMediaEvent:: GetEvent**](/windows/desktop/api/Control/nf-control-imediaevent-getevent).</span><span class="sxs-lookup"><span data-stu-id="c433a-109">The event itself is retrieved by the application through a call to [**IMediaEvent::GetEvent**](/windows/desktop/api/Control/nf-control-imediaevent-getevent).</span></span> <span data-ttu-id="c433a-110">Poiché più di un evento potrebbe trovarsi nella coda degli eventi in un determinato momento, l'applicazione deve chiamare **GetEvent** all'interno di un ciclo che si ripete fino a quando non vengono recuperati tutti gli eventi in coda, come illustrato nell'esempio di codice seguente.</span><span class="sxs-lookup"><span data-stu-id="c433a-110">Because more than one event might be in the event queue at any given time, the application must call **GetEvent** within a loop that repeats until all queued events have been retrieved, as shown in the following code example.</span></span>


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



<span data-ttu-id="c433a-111">Gli eventi DVD possono contenere informazioni aggiuntive nei parametri *lParam1* o *lParam2* , come illustrato in precedenza, in cui l'ora corrente è inclusa in *lParam1*.</span><span class="sxs-lookup"><span data-stu-id="c433a-111">DVD events might contain additional information in the *lParam1* or *lParam2* parameters, as illustrated above where the current time is contained in *lParam1*.</span></span> <span data-ttu-id="c433a-112">L'esempio di codice precedente è riportato nell'applicazione di esempio DVD in Dvdcore. cpp.</span><span class="sxs-lookup"><span data-stu-id="c433a-112">The preceding code example is from the DVD sample application in Dvdcore.cpp.</span></span> <span data-ttu-id="c433a-113">Per un elenco completo di tutti gli eventi DVD e dei relativi parametri, vedere la pagina relativa ai [codici di notifica degli eventi DVD](dvd-notification-codes.md).</span><span class="sxs-lookup"><span data-stu-id="c433a-113">For a complete list of all DVD events and their parameters, see [DVD Event Notification Codes](dvd-notification-codes.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="c433a-114">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="c433a-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c433a-115">Applicazioni DVD</span><span class="sxs-lookup"><span data-stu-id="c433a-115">DVD Applications</span></span>](dvd-applications.md)
</dt> </dl>

 

 



