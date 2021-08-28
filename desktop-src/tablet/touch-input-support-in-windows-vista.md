---
description: A partire da Windows Vista, la tecnologia Tablet PC supporta l'input tocco nei Tablet PC con digitalizzatori che supportano il tocco. Questo supporto include un'interfaccia utente avanzata per facilitare la destinazione e l'esecuzione di Windows quando si usa un dito per l'input.
ms.assetid: 63f1d71f-03d8-4d83-a174-e3dc7c57bad0
title: Supporto dell'input tocco in Windows Vista
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e81b22130a7c731d49556db263d5c1d5565ef51aa103925969b35c98548a32d2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119335071"
---
# <a name="touch-input-support-in-windows-vista"></a>Supporto dell'input tocco in Windows Vista

A partire da Windows Vista, la tecnologia Tablet PC supporta l'input tocco nei Tablet PC con digitalizzatori che supportano il tocco. Questo supporto include un'interfaccia utente avanzata per facilitare la destinazione e l'esecuzione di Windows quando si usa un dito per l'input.

## <a name="touch-digitizer-support"></a>Supporto del digitalizzatore tocco

### <a name="pen-and-touch-input-not-exclusive"></a>Input penna e tocco non esclusivo

Non presupporre che l'input penna e tocco si escludono a vicenda nelle applicazioni [**InkCollector**](inkcollector-class.md), [**InkOverlay**](inkoverlay-class.md)e [**RealTimeStylus.**](realtimestylus-class.md)

In Windows Vista, quando il sistema riconosce una penna, ignora l'input tocco. In altri termini, il tratto tocco termina e inizia il tratto della penna. Poiché questo potrebbe cambiare in futuro, il codice non deve presupporre che l'input penna e tocco si escludono a vicenda.

### <a name="other-mouse-message-sources"></a>Altre origini dei messaggi del mouse

Esistono altre origini di messaggi del mouse anche quando l'utente interagisce solo usando un dito o una penna. Le origini includono i touchpad, nonché lo spostamento destinato a consentire a un'applicazione dietro una finestra su più livelli di tenere presente che il mouse si sta spostando sopra l'applicazione.

### <a name="enabling-and-disabling-the-touch-input-user-interface"></a>Abilitazione e disabilitazione dell'input tocco Interfaccia utente

È possibile abilitare o disabilitare l'interfaccia utente di input tocco a seconda dei requisiti dell'applicazione. A tale scopo, intercettare i messaggi della finestra del sistema operativo in una routine della finestra e modificare il Windows messaggio. Eseguire [l'override di WndProc](/dotnet/api/system.windows.forms.control.wndproc?view=netcore-3.1) nell'applicazione per intercettare questi messaggi. Lo \# pseudocodice C seguente illustra come abilitare e disabilitare l'interfaccia utente di input tocco. Il codice mostra anche l'uso della stessa tecnica per disabilitare il movimento di pressione e pressione. Questo metodo funziona anche per disabilitare lo stilo.


```C++
const int WM_TABLET_QUERY_SYSTEM_GESTURE_STATUS = 716;

const uint SYSTEM_GESTURE_STATUS_NOHOLD           = 0x00000001;
const uint SYSTEM_GESTURE_STATUS_TOUCHUI_FORCEON  = 0x00000100;
const uint SYSTEM_GESTURE_STATUS_TOUCHUI_FORCEOFF = 0x00000200;

protected override void WndProc(ref Message msg)
{
    switch (msg.Msg)
    {
        case WM_TABLET_QUERY_SYSTEM_GESTURE_STATUS:
        {
            uint result = 0;
            if (...)
            {
                result |= SYSTEM_GESTURE_STATUS_NOHOLD;
            }

            if (...)
            {
                result |= SYSTEM_GESTURE_STATUS_TOUCHUI_FORCEON;
            }

            if (...)
            {
                result |= SYSTEM_GESTURE_STATUS_TOUCHUI_FORCEOFF;
            }

            msg.Result = (IntPtr)result;
        }
        break;

        default:
            base.WndProc(ref msg);
            break;
    }
}
```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Windows tocco](../wintouch/windows-touch-portal.md)
</dt> </dl>

 

 
