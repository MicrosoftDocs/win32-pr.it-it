---
title: Gestione degli errori di MCI
description: Gestione degli errori di MCI
ms.assetid: 01a2ff95-34a2-434f-9c7e-d0cdac826c02
keywords:
- mciSendCommand (funzione)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ab8412c74153d5ddfb03a3aff895f9f2e0e73798
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "106299618"
---
# <a name="handling-mci-errors"></a><span data-ttu-id="e0ede-104">Gestione degli errori di MCI</span><span class="sxs-lookup"><span data-stu-id="e0ede-104">Handling MCI Errors</span></span>

<span data-ttu-id="e0ede-105">Controllare sempre il valore restituito della funzione [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="e0ede-105">You should always check the return value of the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function.</span></span> <span data-ttu-id="e0ede-106">Se viene indicato un errore, è possibile utilizzare [**mciGetErrorString**](/previous-versions//dd757158(v=vs.85)) per ottenere una descrizione testuale dell'errore.</span><span class="sxs-lookup"><span data-stu-id="e0ede-106">If it indicates an error, you can use [**mciGetErrorString**](/previous-versions//dd757158(v=vs.85)) to get a textual description of the error.</span></span>

<span data-ttu-id="e0ede-107">Nell'esempio seguente il codice di errore MCI specificato da *dwError* viene passato a **mciGetErrorString** e quindi viene visualizzata la descrizione dell'errore testuale risultante utilizzando la funzione [MessageBox](/windows/win32/api/winuser/nf-winuser-messagebox) .</span><span class="sxs-lookup"><span data-stu-id="e0ede-107">The following example passes the MCI error code specified by *dwError* to **mciGetErrorString**, and then displays the resulting textual error description using the [MessageBox](/windows/win32/api/winuser/nf-winuser-messagebox) function.</span></span>


```C++
// Use mciGetErrorString to get a textual description of an MCI error.
// Display the error description using MessageBox.

void showError(DWORD dwError)
{
    char szErrorBuf[MAXERRORLENGTH];
    MessageBeep(MB_ICONEXCLAMATION);
    if(mciGetErrorString(dwError, (LPSTR) szErrorBuf, MAXERRORLENGTH))
    {
        MessageBox(hMainWnd, szErrorBuf, "MCI Error",
        MB_ICONEXCLAMATION);
    }
    else
    {
        MessageBox(hMainWnd, "Unknown Error", "MCI Error",
            MB_ICONEXCLAMATION);
    }
}
 
```



> [!Note]  
> <span data-ttu-id="e0ede-108">Per interpretare autonomamente un valore restituito da un errore [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) , mascherare la parola più ordinata (la parola di basso livello contiene il codice di errore).</span><span class="sxs-lookup"><span data-stu-id="e0ede-108">To interpret an [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) error return value yourself, mask the high-order word (the low-order word contains the error code).</span></span> <span data-ttu-id="e0ede-109">Se si passa il valore di errore restituito a [**mciGetErrorString**](/previous-versions//dd757158(v=vs.85)), tuttavia, è necessario passare l'intero valore di parola doppia.</span><span class="sxs-lookup"><span data-stu-id="e0ede-109">If you pass the error return value to [**mciGetErrorString**](/previous-versions//dd757158(v=vs.85)), however, you must pass the entire doubleword value.</span></span>

 

 

 