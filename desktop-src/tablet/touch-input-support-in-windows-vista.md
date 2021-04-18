---
description: A partire da Windows Vista, la tecnologia Tablet PC supporta l'input touch su Tablet PC con digitalizzatori compatibili con touch. Questo supporto include un'interfaccia utente avanzata per semplificare la destinazione e la riga di comando di Windows quando si usa un dito per l'input.
ms.assetid: 63f1d71f-03d8-4d83-a174-e3dc7c57bad0
title: Supporto per input touch in Windows Vista
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1b623630c93c33b846ab1bb491fc56fe46dfe825
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106313910"
---
# <a name="touch-input-support-in-windows-vista"></a>Supporto per input touch in Windows Vista

A partire da Windows Vista, la tecnologia Tablet PC supporta l'input touch su Tablet PC con digitalizzatori compatibili con touch. Questo supporto include un'interfaccia utente avanzata per semplificare la destinazione e la riga di comando di Windows quando si usa un dito per l'input.

## <a name="touch-digitizer-support"></a>Supporto per il digitalizzatore Touch

### <a name="pen-and-touch-input-not-exclusive"></a>Input penna e tocco non esclusivo

Non presupporre che input penna e tocco si escludono a vicenda nelle applicazioni [**InkCollector**](inkcollector-class.md), [**InkOverlay**](inkoverlay-class.md)e [**RealTimeStylus**](realtimestylus-class.md) .

In Windows Vista, quando il sistema riconosce una penna, ignora l'input tocco. Ovvero, il tratto di tocco termina e viene avviato il tratto della penna. Poiché questo potrebbe cambiare in futuro, il codice non deve presumere che l'input penna e tocco si escludono a vicenda.

### <a name="other-mouse-message-sources"></a>Altre origini messaggi del mouse

Sono presenti altre origini dei messaggi del mouse anche quando l'utente sta interagendo solo con un dito o con una penna. Le origini includono i touchpad, nonché lo spostamento per consentire a un'applicazione dietro una finestra a più livelli di tenere presente che il mouse è in movimento sopra l'applicazione.

### <a name="enabling-and-disabling-the-touch-input-user-interface"></a>Abilitazione e disabilitazione dell'interfaccia utente di input tocco

È possibile abilitare o disabilitare l'interfaccia utente di input tocco in base ai requisiti dell'applicazione. A tale scopo, intercettare i messaggi della finestra del sistema operativo in una routine della finestra e modificare il messaggio di Windows. Eseguire l'override di [WndProc](/dotnet/api/system.windows.forms.control.wndproc?view=netcore-3.1) nell'applicazione per intercettare questi messaggi. Nel seguente \# pseudo-codice C viene illustrato come abilitare e disabilitare l'interfaccia utente di input tocco. Il codice mostra anche l'uso della stessa tecnica per disabilitare il movimento di stampa e di attesa. Questo metodo funziona anche per disabilitare lo stilo.


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

[Windows Touch](../wintouch/windows-touch-portal.md)
</dt> </dl>

 

 
