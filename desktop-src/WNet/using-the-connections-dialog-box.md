---
title: Utilizzo della finestra di dialogo connessioni
description: La funzione WNetConnectionDialog crea una finestra di dialogo che consente all'utente di esplorare e connettersi alle risorse di rete.
ms.assetid: ef375004-e426-4dee-b318-b470721116fa
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9f69d0f32772e614d60598853af620ae3c6452f5
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104338206"
---
# <a name="using-the-connections-dialog-box"></a><span data-ttu-id="1931c-103">Utilizzo della finestra di dialogo connessioni</span><span class="sxs-lookup"><span data-stu-id="1931c-103">Using the Connections Dialog Box</span></span>

<span data-ttu-id="1931c-104">La funzione [**WNetConnectionDialog**](/windows/win32/api/winnetwk/nf-winnetwk-wnetconnectiondialog) crea una finestra di dialogo che consente all'utente di esplorare e connettersi alle risorse di rete.</span><span class="sxs-lookup"><span data-stu-id="1931c-104">The [**WNetConnectionDialog**](/windows/win32/api/winnetwk/nf-winnetwk-wnetconnectiondialog) function creates a dialog box that allows the user to browse and connect to network resources.</span></span> <span data-ttu-id="1931c-105">È inoltre possibile chiamare la funzione [**WNetConnectionDialog1**](/windows/win32/api/winnetwk/nf-winnetwk-wnetconnectiondialog1a) per creare una finestra di dialogo connessioni.</span><span class="sxs-lookup"><span data-stu-id="1931c-105">You can also call the [**WNetConnectionDialog1**](/windows/win32/api/winnetwk/nf-winnetwk-wnetconnectiondialog1a) function to create a connections dialog box.</span></span> <span data-ttu-id="1931c-106">**WNetConnectionDialog1** richiede una struttura [**CONNECTDLGSTRUCT**](/windows/win32/api/winnetwk/ns-winnetwk-connectdlgstructa) .</span><span class="sxs-lookup"><span data-stu-id="1931c-106">**WNetConnectionDialog1** requires a [**CONNECTDLGSTRUCT**](/windows/win32/api/winnetwk/ns-winnetwk-connectdlgstructa) structure.</span></span>

<span data-ttu-id="1931c-107">La funzione [**WNetDisconnectDialog**](/windows/win32/api/winnetwk/nf-winnetwk-wnetdisconnectdialog) crea una finestra di dialogo che consente all'utente di disconnettersi dalle risorse di rete.</span><span class="sxs-lookup"><span data-stu-id="1931c-107">The [**WNetDisconnectDialog**](/windows/win32/api/winnetwk/nf-winnetwk-wnetdisconnectdialog) function creates a dialog box that allows the user to disconnect from network resources.</span></span>

<span data-ttu-id="1931c-108">Nell'esempio di codice seguente viene illustrato come chiamare la funzione **WNetConnectionDialog** per creare una finestra di dialogo in cui vengono visualizzate le risorse disco.</span><span class="sxs-lookup"><span data-stu-id="1931c-108">The following code sample demonstrates how to call the **WNetConnectionDialog** function to create a dialog box that displays disk resources.</span></span> <span data-ttu-id="1931c-109">Se la chiamata ha esito negativo, l'esempio chiama un gestore degli errori definito dall'applicazione.</span><span class="sxs-lookup"><span data-stu-id="1931c-109">If the call fails, the sample calls an application-defined error handler.</span></span>


```C++
DWORD dwResult; 
//
// Call the WNetConnectionDialog function.
//
dwResult = WNetConnectionDialog(hwnd, RESOURCETYPE_DISK);
//
// Call an application-defined error handler 
//  to process errors.
//
if(dwResult != NO_ERROR) 
{
    NetErrorHandler(hwnd, dwResult, (LPSTR)"WNetConnectionDialog"); 
    return FALSE; 
}
```



<span data-ttu-id="1931c-110">Per ulteriori informazioni sull'utilizzo di un gestore degli errori definito dall'applicazione, vedere [recupero degli errori di rete](retrieving-network-errors.md).</span><span class="sxs-lookup"><span data-stu-id="1931c-110">For more information about using an application-defined error handler, see [Retrieving Network Errors](retrieving-network-errors.md).</span></span>

 

 