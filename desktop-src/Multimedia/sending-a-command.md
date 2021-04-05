---
title: Invio di un comando
description: Invio di un comando
ms.assetid: 28c38f36-b6a7-44da-95e2-25b3dccefc84
keywords:
- mciSendString (funzione)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e69536b167b8fde648c3f3743058542d74bd8647
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "103872402"
---
# <a name="sending-a-command"></a><span data-ttu-id="77a33-104">Invio di un comando</span><span class="sxs-lookup"><span data-stu-id="77a33-104">Sending a Command</span></span>

<span data-ttu-id="77a33-105">La funzione di esempio seguente invia il comando [**Play**](play.md) con i flag "from" e "to" usando la funzione [**mciSendString**](/previous-versions//dd757161(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="77a33-105">The following example function sends the [**play**](play.md) command with the "from" and "to" flags using the [**mciSendString**](/previous-versions//dd757161(v=vs.85)) function.</span></span>


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



 

 