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
# <a name="handling-mci-errors"></a>Gestione degli errori di MCI

Controllare sempre il valore restituito della funzione [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) . Se viene indicato un errore, è possibile utilizzare [**mciGetErrorString**](/previous-versions//dd757158(v=vs.85)) per ottenere una descrizione testuale dell'errore.

Nell'esempio seguente il codice di errore MCI specificato da *dwError* viene passato a **mciGetErrorString** e quindi viene visualizzata la descrizione dell'errore testuale risultante utilizzando la funzione [MessageBox](/windows/win32/api/winuser/nf-winuser-messagebox) .


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
> Per interpretare autonomamente un valore restituito da un errore [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) , mascherare la parola più ordinata (la parola di basso livello contiene il codice di errore). Se si passa il valore di errore restituito a [**mciGetErrorString**](/previous-versions//dd757158(v=vs.85)), tuttavia, è necessario passare l'intero valore di parola doppia.

 

 

 