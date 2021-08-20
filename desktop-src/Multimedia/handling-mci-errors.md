---
title: Gestione degli errori MCI
description: Gestione degli errori MCI
ms.assetid: 01a2ff95-34a2-434f-9c7e-d0cdac826c02
keywords:
- MciSendCommand - funzione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f8e2f3a9cc3e711db0d26f28c9ac7e3fd0a8c94eec96117a732f8024372bf9de
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118141023"
---
# <a name="handling-mci-errors"></a>Gestione degli errori MCI

È necessario controllare sempre il valore restituito della [**funzione mciSendCommand.**](/previous-versions//dd757160(v=vs.85)) Se indica un errore, è possibile usare [**mciGetErrorString**](/previous-versions//dd757158(v=vs.85)) per ottenere una descrizione testuale dell'errore.

L'esempio seguente passa il codice di errore MCI specificato da *dwError* a **mciGetErrorString** e quindi visualizza la descrizione dell'errore testuale risultante usando la [funzione MessageBox.](/windows/win32/api/winuser/nf-winuser-messagebox)


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
> Per interpretare manualmente un valore restituito di errore [**mciSendCommand,**](/previous-versions//dd757160(v=vs.85)) mascherare la parola più alta (la parola di ordine più basso contiene il codice di errore). Se tuttavia si passa il valore restituito dell'errore [**a mciGetErrorString,**](/previous-versions//dd757158(v=vs.85))è necessario passare l'intero valore doubleword.

 

 

 