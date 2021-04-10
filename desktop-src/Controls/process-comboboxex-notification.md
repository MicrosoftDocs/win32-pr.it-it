---
title: Come elaborare le notifiche ComboBoxEx
description: In questo argomento viene illustrato come elaborare i messaggi di notifica ComboBoxEx.
ms.assetid: 375634BC-CDD6-4D72-A41E-FCBFCBFE7F03
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7a9787e22aa01d51478ca55f0dde5d7ac944decb
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/04/2020
ms.locfileid: "103963604"
---
# <a name="how-to-process-comboboxex-notifications"></a><span data-ttu-id="c4c05-103">Come elaborare le notifiche ComboBoxEx</span><span class="sxs-lookup"><span data-stu-id="c4c05-103">How to Process ComboBoxEx Notifications</span></span>

<span data-ttu-id="c4c05-104">In questo argomento viene illustrato come elaborare i messaggi di notifica ComboBoxEx.</span><span class="sxs-lookup"><span data-stu-id="c4c05-104">This topic demonstrates how to process ComboBoxEx notification messages.</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="c4c05-105">Informazioni importanti</span><span class="sxs-lookup"><span data-stu-id="c4c05-105">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="c4c05-106">Tecnologie</span><span class="sxs-lookup"><span data-stu-id="c4c05-106">Technologies</span></span>

-   [<span data-ttu-id="c4c05-107">Controlli Windows</span><span class="sxs-lookup"><span data-stu-id="c4c05-107">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="c4c05-108">Prerequisiti</span><span class="sxs-lookup"><span data-stu-id="c4c05-108">Prerequisites</span></span>

-   <span data-ttu-id="c4c05-109">C/C++</span><span class="sxs-lookup"><span data-stu-id="c4c05-109">C/C++</span></span>
-   <span data-ttu-id="c4c05-110">Programmazione dell'interfaccia utente di Windows</span><span class="sxs-lookup"><span data-stu-id="c4c05-110">Windows User Interface Programming</span></span>

## <a name="instructions"></a><span data-ttu-id="c4c05-111">Istruzioni</span><span class="sxs-lookup"><span data-stu-id="c4c05-111">Instructions</span></span>


<span data-ttu-id="c4c05-112">Un controllo ComboBoxEx notifica la finestra padre degli eventi inviando i messaggi di [**\_ notifica WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="c4c05-112">A ComboBoxEx control notifies its parent window of events by sending [**WM\_NOTIFY**](wm-notify.md) messages.</span></span> <span data-ttu-id="c4c05-113">Passa inoltre i messaggi di notifica dei [**\_ comandi WM**](/windows/desktop/menurc/wm-command) ricevuti dalla casella combinata contenuta al suo interno alla finestra padre da elaborare.</span><span class="sxs-lookup"><span data-stu-id="c4c05-113">It also passes the [**WM\_COMMAND**](/windows/desktop/menurc/wm-command) notification messages that it receives from the combo box contained within it to the parent window to be processed.</span></span> <span data-ttu-id="c4c05-114">Pertanto, l'applicazione deve essere preparata per l'elaborazione dei messaggi di **\_ notifica WM** dai messaggi di **\_ comando** ComboBoxEx e WM che vengono inviati dal controllo casella combinata figlio ComboBoxEx.</span><span class="sxs-lookup"><span data-stu-id="c4c05-114">Therefore, your application must be prepared to process **WM\_NOTIFY** messages from the ComboBoxEx and **WM\_COMMAND** messages that are forwarded from the ComboBoxEx child combo box control.</span></span>

<span data-ttu-id="c4c05-115">Nell'esempio riportato in questa sezione vengono gestiti i messaggi [**WM \_ Notify**](wm-notify.md) e [**WM \_ Command**](/windows/desktop/menurc/wm-command) da un controllo ComboBoxEx tramite una chiamata a una funzione definita dall'applicazione corrispondente per elaborare questi messaggi.</span><span class="sxs-lookup"><span data-stu-id="c4c05-115">The example in this section handles the [**WM\_NOTIFY**](wm-notify.md) and [**WM\_COMMAND**](/windows/desktop/menurc/wm-command) messages from a ComboBoxEx control by calling a corresponding application-defined function to process these messages.</span></span>

## <a name="complete-example"></a><span data-ttu-id="c4c05-116">Esempio completo</span><span class="sxs-lookup"><span data-stu-id="c4c05-116">Complete example</span></span>


```C++
LRESULT CALLBACK WndProc (HWND hwnd, UINT msg, WPARAM wParam, LPARAM lParam)
{
    switch(msg){

        case WM_COMMAND: // notification from the child ComboBox within the ComboBoxEx control.
            if((HWND)lParam == g_hwndCB)
                DoOldNotify(hwnd,  wParam);  
            break;

        case WM_NOTIFY: // notification from the ComboBoxEx control
            return (DoCBEXNotify(hwnd, lParam));

        case WM_PAINT:
            hdc = BeginPaint(hwnd, &ps);
            EndPaint(hwnd, &ps);
            break;

        case WM_DESTROY:
            PostQuitMessage(0);
            break;

        default:
            return DefWindowProc(hwnd, msg, wParam, lParam);
            break;
    }

    return FALSE;
}
```



## <a name="related-topics"></a><span data-ttu-id="c4c05-117">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="c4c05-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c4c05-118">Informazioni sui controlli ComboBoxEx</span><span class="sxs-lookup"><span data-stu-id="c4c05-118">About ComboBoxEx Controls</span></span>](comboboxex-controls.md)
</dt> <dt>

[<span data-ttu-id="c4c05-119">Riferimento al controllo ComboBoxEx</span><span class="sxs-lookup"><span data-stu-id="c4c05-119">ComboBoxEx Control Reference</span></span>](bumper-comboboxex-comboboxex-control-reference.md)
</dt> <dt>

[<span data-ttu-id="c4c05-120">Uso di controlli ComboBoxEx</span><span class="sxs-lookup"><span data-stu-id="c4c05-120">Using ComboBoxEx Controls</span></span>](/windows/desktop/Controls/using-comboboxex)
</dt> <dt>

[<span data-ttu-id="c4c05-121">ComboBoxEx</span><span class="sxs-lookup"><span data-stu-id="c4c05-121">ComboBoxEx</span></span>](comboboxex-control-reference.md)
</dt> </dl>

 

 