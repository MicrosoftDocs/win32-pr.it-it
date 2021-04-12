---
title: Come creare un controllo degli indirizzi IP
description: In questo argomento viene illustrato come creare un'istanza di un controllo degli indirizzi IP.
ms.assetid: E4DBECA6-B3F2-405F-8D95-32FA2334114D
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d8427a5695c0b9c79c19d328f4abc2ab0ffb2e5a
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/04/2020
ms.locfileid: "104118678"
---
# <a name="how-to-create-an-ip-address-control"></a><span data-ttu-id="72609-103">Come creare un controllo degli indirizzi IP</span><span class="sxs-lookup"><span data-stu-id="72609-103">How to Create an IP Address Control</span></span>

<span data-ttu-id="72609-104">In questo argomento viene illustrato come creare un'istanza di un controllo degli indirizzi IP.</span><span class="sxs-lookup"><span data-stu-id="72609-104">This topic demonstrates how to create an instance of an IP address control.</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="72609-105">Informazioni importanti</span><span class="sxs-lookup"><span data-stu-id="72609-105">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="72609-106">Tecnologie</span><span class="sxs-lookup"><span data-stu-id="72609-106">Technologies</span></span>

-   [<span data-ttu-id="72609-107">Controlli Windows</span><span class="sxs-lookup"><span data-stu-id="72609-107">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="72609-108">Prerequisiti</span><span class="sxs-lookup"><span data-stu-id="72609-108">Prerequisites</span></span>

-   <span data-ttu-id="72609-109">C/C++</span><span class="sxs-lookup"><span data-stu-id="72609-109">C/C++</span></span>
-   <span data-ttu-id="72609-110">Programmazione dell'interfaccia utente di Windows</span><span class="sxs-lookup"><span data-stu-id="72609-110">Windows User Interface Programming</span></span>

## <a name="instructions"></a><span data-ttu-id="72609-111">Istruzioni</span><span class="sxs-lookup"><span data-stu-id="72609-111">Instructions</span></span>


<span data-ttu-id="72609-112">Prima di creare un controllo degli indirizzi IP, caricare la DLL dei controlli comuni chiamando [**InitCommonControlsEx**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrolsex).</span><span class="sxs-lookup"><span data-stu-id="72609-112">Before creating an IP address control, load the common controls DLL by calling [**InitCommonControlsEx**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrolsex).</span></span> <span data-ttu-id="72609-113">Usare quindi la funzione [**CreateWindow**](/windows/desktop/api/winuser/nf-winuser-createwindowa) o [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) per creare un controllo dell'indirizzo IP dell'istanza.</span><span class="sxs-lookup"><span data-stu-id="72609-113">Then use the [**CreateWindow**](/windows/desktop/api/winuser/nf-winuser-createwindowa) or the [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) function to create an instance IP address control.</span></span> <span data-ttu-id="72609-114">Il nome della classe per il controllo è il [**WC \_ IPAddress**](common-control-window-classes.md).</span><span class="sxs-lookup"><span data-stu-id="72609-114">The class name for the control is [**WC\_IPADDRESS**](common-control-window-classes.md).</span></span> <span data-ttu-id="72609-115">Utilizzare lo stile [**WS \_ child**](/windows/desktop/winmsg/window-styles) , perché non è presente alcuna costante di stile associata al controllo degli indirizzi IP.</span><span class="sxs-lookup"><span data-stu-id="72609-115">Use the [**WS\_CHILD**](/windows/desktop/winmsg/window-styles) style, because there is no specific style constant associated with the IP address control.</span></span>

<span data-ttu-id="72609-116">Nell'esempio di codice C++ riportato di seguito, la funzione definita dall'applicazione chiama prima [**InitCommonControlsEx**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrolsex) e imposta il membro **DwICC** della struttura [**InitCommonControlsEx**](/windows/win32/api/commctrl/ns-commctrl-initcommoncontrolsex) sulle [**\_ \_ classi Internet ICC**](/windows/win32/api/commctrl/ns-commctrl-initcommoncontrolsex), che specifica la classe dell'indirizzo IP.</span><span class="sxs-lookup"><span data-stu-id="72609-116">In the following C++ code example, the application-defined function first calls [**InitCommonControlsEx**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrolsex) and sets the **dwICC** member of the [**INITCOMMONCONTROLSEX**](/windows/win32/api/commctrl/ns-commctrl-initcommoncontrolsex) structure to [**ICC\_INTERNET\_CLASSES**](/windows/win32/api/commctrl/ns-commctrl-initcommoncontrolsex), which specifies the IP address class.</span></span> <span data-ttu-id="72609-117">Chiama quindi [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) per creare un'istanza del controllo degli indirizzi IP.</span><span class="sxs-lookup"><span data-stu-id="72609-117">It then calls [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) to create an instance of the IP address control.</span></span>


```C++
// CreateIPAdressFld - creates a IPAddress control.
// Returns the handle to the new control
// TO DO:  calling procedure needs to check whether the handle is NULL, in case 
// of an error in creation.
// int xcoord, ycoord the coordinates of location of the control in the parent window
// HINST hInst is the global handle to the application instance.
// HWND  hWndParent is the handle to the control's parent window. 
//
//
HWND CreateIPAddressFld (HWND hwndParent, int xcoord, int ycoord) 
{     
     
    INITCOMMONCONTROLSEX icex;
    
    // Ensure that the common control DLL is loaded. 
    icex.dwSize = sizeof(INITCOMMONCONTROLSEX);
    icex.dwICC  = ICC_INTERNET_CLASSES ;
    InitCommonControlsEx(&icex); 
    
    // Create the IPAddress control.        
    HWND hWndIPAddressFld = CreateWindow(WC_IPADDRESS, 
                                L"", 
                                WS_CHILD | WS_OVERLAPPED | WS_VISIBLE, 
                                xcoord, 
                                ycoord,
                                150, 
                                20,  
                                hwndParent, 
                                NULL, 
                                hInst, 
                                NULL); 
                                
    return (hWndIPAddressFld);
}
```



## <a name="related-topics"></a><span data-ttu-id="72609-118">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="72609-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="72609-119">Riferimento al controllo degli indirizzi IP</span><span class="sxs-lookup"><span data-stu-id="72609-119">IP Address Control Reference</span></span>](bumper-ip-address-control-ip-address-control-reference.md)
</dt> <dt>

[<span data-ttu-id="72609-120">Informazioni sui controlli degli indirizzi IP</span><span class="sxs-lookup"><span data-stu-id="72609-120">About IP Address Controls</span></span>](ip-address-controls.md)
</dt> <dt>

[<span data-ttu-id="72609-121">Uso di controlli degli indirizzi IP</span><span class="sxs-lookup"><span data-stu-id="72609-121">Using IP Address Controls</span></span>](using-ip-address-controls.md)
</dt> </dl>

 

 