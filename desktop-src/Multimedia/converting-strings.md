---
title: Conversione di stringhe
description: Conversione di stringhe
ms.assetid: 40621c71-4264-40bc-b6c3-6b639d2f28fa
keywords:
- Funzione mciSendString
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4efeb5801c46d89686ed3fe9fcf25b311d57d4d553c220902907ac0e70a5b7e1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119144794"
---
# <a name="converting-strings"></a>Conversione di stringhe

Quando si usa la funzione [**mciSendString,**](/previous-versions//dd757161(v=vs.85)) tutti i valori passati con il comando e tutti i valori restituiti sono stringhe di testo, quindi l'applicazione necessita di routine di conversione per la conversione da variabili a stringhe o di nuovo. Nell'esempio seguente viene recuperato il rettangolo di origine e la stringa restituita viene convertita in coordinate di rettangolo.


```C++
BOOL GetSourceRect(LPTSTR lpstrAlias, LPRECT lprc) 
{ 
    TCHAR achRetBuff[128]; 
    TCHAR achCommandBuff[128]; 

    int result;
    MCIERROR err;
 
    // Build the command string. 
    result = _stprintf_s(
        achCommandBuff, 
        TEXT("where %s source"), 
        lpstrAlias); 

    if (result == -1)
    {
        return FALSE;
    }
    
    // Clear the RECT.
    SetRectEmpty(lprc);
 
    // Send the MCI command. 
    err = mciSendString(
        achCommandBuff, 
        achRetBuff, 
        sizeof(achRetBuff), 
        NULL);

    if (err != 0)
    {
        return FALSE;
    }
        
    // The rectangle is returned as "x y dx dy". 
    // Translate the string into the RECT structure. 

    // Warning: This example omits error checking
    // for the _tcstok_s and _tstoi functions.
    TCHAR *p; 
    TCHAR *context;

    // Left.
    p = _tcstok_s(achRetBuff, TEXT(" "), &context);
    lprc->left = _tstoi(p);

    // Top.
    p = _tcstok_s(NULL, TEXT(" "), &context);
    lprc->top = _tstoi(p);

    // Right.
    p = _tcstok_s(NULL, TEXT(" "), &context);
    lprc->right = _tstoi(p);
    
    // Bottom.
    p = _tcstok_s(NULL, TEXT(" "), &context);
    lprc->bottom = _tstoi(p);

    return TRUE;
}
 
```



> [!Note]  
> **Le** strutture RECT vengono gestite in modo diverso in MCI rispetto ad altre parti del Windows; In MCI, il **membro destro** contiene la larghezza del rettangolo e il **membro** inferiore contiene l'altezza. Nell'interfaccia di stringa un rettangolo viene specificato *come X1*, *Y1*, *X2* e *Y2*. Le coordinate *X1* e *Y1* specificano l'angolo superiore sinistro del rettangolo e le coordinate *X2* *e Y2* specificano la larghezza e l'altezza.

 

 

 