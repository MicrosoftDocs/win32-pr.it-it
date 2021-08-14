---
title: Invio di un comando
description: Invio di un comando
ms.assetid: 28c38f36-b6a7-44da-95e2-25b3dccefc84
keywords:
- Funzione mciSendString
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aa2b5763ae93887da607cfba9e94f55a254d7bcd8b0413e40ab9dff45f922cf1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117801751"
---
# <a name="sending-a-command"></a>Invio di un comando

La funzione di esempio seguente invia [**il comando play**](play.md) con i flag "from" e "to" usando la funzione [**mciSendString.**](/previous-versions//dd757161(v=vs.85))


```C++
BOOL PlayFromTo(LPTSTR lpstrAlias, DWORD dwFrom, DWORD dwTo) 
{ 
    TCHAR achCommandBuff[128]; 
    int result;
    MCIERROR err;

    // Form the command string.
    result = _stprintf_s(
        achCommandBuff, 
        TEXT("play %s from %u to %u"), 
        lpstrAlias, dwFrom, dwTo); 

    if (result == -1)
    {
        return FALSE;
    }

    // Send the command string.
    err = mciSendString(achCommandBuff, NULL, 0, NULL); 
    if (err != 0)
    {
        return FALSE;
    }

    return TRUE;
} 
```



 

 