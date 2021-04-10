---
title: Conversione di stringhe
description: Conversione di stringhe
ms.assetid: 40621c71-4264-40bc-b6c3-6b639d2f28fa
keywords:
- mciSendString (funzione)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7d1db4cb4b3d02a93adecc82d6ce95de436fb2e7
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "103956368"
---
# <a name="converting-strings"></a>Conversione di stringhe

Quando si usa la funzione [**mciSendString**](/previous-versions//dd757161(v=vs.85)) , tutti i valori passati con il comando e tutti i valori restituiti sono stringhe di testo, quindi l'applicazione deve avere le routine di conversione per tradurre le variabili in stringhe o viceversa. Nell'esempio seguente viene recuperato il rettangolo di origine e la stringa restituita viene convertita in coordinate del rettangolo.


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
> Le strutture **Rect** sono gestite in modo diverso in MCI rispetto ad altre parti di Windows; in MCI il membro **destro** contiene la larghezza del rettangolo e il membro **inferiore** ne contiene l'altezza. Nell'interfaccia di stringa, un rettangolo viene specificato come *X1*, *Y1*, *X2* e *Y2*. Le coordinate *X1* e *Y1* specificano l'angolo superiore sinistro del rettangolo e le coordinate *X2* e *Y2* specificano la larghezza e l'altezza.

 

 

 