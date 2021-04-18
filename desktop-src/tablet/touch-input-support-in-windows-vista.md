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
# <a name="touch-input-support-in-windows-vista"></a><span data-ttu-id="f52e7-104">Supporto per input touch in Windows Vista</span><span class="sxs-lookup"><span data-stu-id="f52e7-104">Touch Input Support in Windows Vista</span></span>

<span data-ttu-id="f52e7-105">A partire da Windows Vista, la tecnologia Tablet PC supporta l'input touch su Tablet PC con digitalizzatori compatibili con touch.</span><span class="sxs-lookup"><span data-stu-id="f52e7-105">Starting with Windows Vista, Tablet PC Technology has support for touch input on Tablet PC's with touch capable digitizers.</span></span> <span data-ttu-id="f52e7-106">Questo supporto include un'interfaccia utente avanzata per semplificare la destinazione e la riga di comando di Windows quando si usa un dito per l'input.</span><span class="sxs-lookup"><span data-stu-id="f52e7-106">This support includes an enhanced user interface to aid in targeting and commanding Windows when using a finger for input.</span></span>

## <a name="touch-digitizer-support"></a><span data-ttu-id="f52e7-107">Supporto per il digitalizzatore Touch</span><span class="sxs-lookup"><span data-stu-id="f52e7-107">Touch Digitizer Support</span></span>

### <a name="pen-and-touch-input-not-exclusive"></a><span data-ttu-id="f52e7-108">Input penna e tocco non esclusivo</span><span class="sxs-lookup"><span data-stu-id="f52e7-108">Pen and Touch Input Not Exclusive</span></span>

<span data-ttu-id="f52e7-109">Non presupporre che input penna e tocco si escludono a vicenda nelle applicazioni [**InkCollector**](inkcollector-class.md), [**InkOverlay**](inkoverlay-class.md)e [**RealTimeStylus**](realtimestylus-class.md) .</span><span class="sxs-lookup"><span data-stu-id="f52e7-109">Do not assume pen and touch input are mutually exclusive in [**InkCollector**](inkcollector-class.md), [**InkOverlay**](inkoverlay-class.md), and [**RealTimeStylus**](realtimestylus-class.md) applications.</span></span>

<span data-ttu-id="f52e7-110">In Windows Vista, quando il sistema riconosce una penna, ignora l'input tocco.</span><span class="sxs-lookup"><span data-stu-id="f52e7-110">In Windows Vista, when the system recognizes a pen it ignores touch input.</span></span> <span data-ttu-id="f52e7-111">Ovvero, il tratto di tocco termina e viene avviato il tratto della penna.</span><span class="sxs-lookup"><span data-stu-id="f52e7-111">That is, the touch stroke ends and the pen stroke begins.</span></span> <span data-ttu-id="f52e7-112">Poiché questo potrebbe cambiare in futuro, il codice non deve presumere che l'input penna e tocco si escludono a vicenda.</span><span class="sxs-lookup"><span data-stu-id="f52e7-112">Because this could possibly change in the future, your code should not assume pen and touch input are mutually exclusive.</span></span>

### <a name="other-mouse-message-sources"></a><span data-ttu-id="f52e7-113">Altre origini messaggi del mouse</span><span class="sxs-lookup"><span data-stu-id="f52e7-113">Other Mouse Message Sources</span></span>

<span data-ttu-id="f52e7-114">Sono presenti altre origini dei messaggi del mouse anche quando l'utente sta interagendo solo con un dito o con una penna.</span><span class="sxs-lookup"><span data-stu-id="f52e7-114">There are other sources of mouse messages even when the user is only interacting using finger or pen.</span></span> <span data-ttu-id="f52e7-115">Le origini includono i touchpad, nonché lo spostamento per consentire a un'applicazione dietro una finestra a più livelli di tenere presente che il mouse è in movimento sopra l'applicazione.</span><span class="sxs-lookup"><span data-stu-id="f52e7-115">Sources include touchpads, as well as movement intended to let an application behind a layered window be aware that the mouse is moving above the application.</span></span>

### <a name="enabling-and-disabling-the-touch-input-user-interface"></a><span data-ttu-id="f52e7-116">Abilitazione e disabilitazione dell'interfaccia utente di input tocco</span><span class="sxs-lookup"><span data-stu-id="f52e7-116">Enabling and Disabling the Touch Input User Interface</span></span>

<span data-ttu-id="f52e7-117">È possibile abilitare o disabilitare l'interfaccia utente di input tocco in base ai requisiti dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="f52e7-117">You may wish to enable or disable the touch input user interface depending on the requirements of your application.</span></span> <span data-ttu-id="f52e7-118">A tale scopo, intercettare i messaggi della finestra del sistema operativo in una routine della finestra e modificare il messaggio di Windows.</span><span class="sxs-lookup"><span data-stu-id="f52e7-118">To accomplish this, intercept operating system window messages in a window procedure and modify the Windows message.</span></span> <span data-ttu-id="f52e7-119">Eseguire l'override di [WndProc](/dotnet/api/system.windows.forms.control.wndproc?view=netcore-3.1) nell'applicazione per intercettare questi messaggi.</span><span class="sxs-lookup"><span data-stu-id="f52e7-119">Override [WndProc](/dotnet/api/system.windows.forms.control.wndproc?view=netcore-3.1) in your application to intercept these messages.</span></span> <span data-ttu-id="f52e7-120">Nel seguente \# pseudo-codice C viene illustrato come abilitare e disabilitare l'interfaccia utente di input tocco.</span><span class="sxs-lookup"><span data-stu-id="f52e7-120">The following C\# pseudo-code shows how to enable and disable the touch input user interface.</span></span> <span data-ttu-id="f52e7-121">Il codice mostra anche l'uso della stessa tecnica per disabilitare il movimento di stampa e di attesa.</span><span class="sxs-lookup"><span data-stu-id="f52e7-121">The code also shows using the same technique to disable the press-and-hold gesture.</span></span> <span data-ttu-id="f52e7-122">Questo metodo funziona anche per disabilitare lo stilo.</span><span class="sxs-lookup"><span data-stu-id="f52e7-122">This method also works for disabling the stylus.</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="f52e7-123">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="f52e7-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f52e7-124">Windows Touch</span><span class="sxs-lookup"><span data-stu-id="f52e7-124">Windows Touch</span></span>](../wintouch/windows-touch-portal.md)
</dt> </dl>

 

 
