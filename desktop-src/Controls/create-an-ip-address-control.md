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
# <a name="how-to-create-an-ip-address-control"></a>Come creare un controllo degli indirizzi IP

In questo argomento viene illustrato come creare un'istanza di un controllo degli indirizzi IP.

## <a name="what-you-need-to-know"></a>Informazioni importanti

### <a name="technologies"></a>Tecnologie

-   [Controlli Windows](window-controls.md)

### <a name="prerequisites"></a>Prerequisiti

-   C/C++
-   Programmazione dell'interfaccia utente di Windows

## <a name="instructions"></a>Istruzioni


Prima di creare un controllo degli indirizzi IP, caricare la DLL dei controlli comuni chiamando [**InitCommonControlsEx**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrolsex). Usare quindi la funzione [**CreateWindow**](/windows/desktop/api/winuser/nf-winuser-createwindowa) o [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) per creare un controllo dell'indirizzo IP dell'istanza. Il nome della classe per il controllo è il [**WC \_ IPAddress**](common-control-window-classes.md). Utilizzare lo stile [**WS \_ child**](/windows/desktop/winmsg/window-styles) , perché non è presente alcuna costante di stile associata al controllo degli indirizzi IP.

Nell'esempio di codice C++ riportato di seguito, la funzione definita dall'applicazione chiama prima [**InitCommonControlsEx**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrolsex) e imposta il membro **DwICC** della struttura [**InitCommonControlsEx**](/windows/win32/api/commctrl/ns-commctrl-initcommoncontrolsex) sulle [**\_ \_ classi Internet ICC**](/windows/win32/api/commctrl/ns-commctrl-initcommoncontrolsex), che specifica la classe dell'indirizzo IP. Chiama quindi [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) per creare un'istanza del controllo degli indirizzi IP.


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



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Riferimento al controllo degli indirizzi IP](bumper-ip-address-control-ip-address-control-reference.md)
</dt> <dt>

[Informazioni sui controlli degli indirizzi IP](ip-address-controls.md)
</dt> <dt>

[Uso di controlli degli indirizzi IP](using-ip-address-controls.md)
</dt> </dl>

 

 