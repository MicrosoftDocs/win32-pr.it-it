---
description: Nell'esempio di codice seguente viene illustrato l'utilizzo di un oggetto mutex per determinare se è stato eseguito l'accesso a MSN Explorer.
ms.assetid: ec52a61c-9d2c-4327-977b-fb13d042bc37
title: Determinare se MSN è nello stato di accesso
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ba2d7af3511035c997493f0439a8635c1a928a75
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104523961"
---
# <a name="determining-if-msn-is-in-the-sign-in-state"></a>Determinare se MSN è nello stato di accesso

Nell'esempio di codice seguente viene illustrato l'utilizzo di un oggetto mutex per determinare se è stato eseguito l'accesso a MSN Explorer. Al termine dell'utilizzo dell'handle, assicurarsi di chiamare la funzione [**CloseHandle**](/windows/win32/api/handleapi/nf-handleapi-closehandle) .

> [!Note]  
> Questo oggetto mutex è disponibile per l'utilizzo nel controllo di MSN Explorer 7. stato di accesso *x* . Potrebbe non essere disponibile nelle versioni successive.

 


```C++
    HANDLE hMSNSignedInMutex;

    hMSNSignedInMutex = OpenMutex(SYNCHRONIZE, FALSE, 
        "{ECCC50B5-064B-4693-B104-925714A4C74B}");

    if (hMSNSignedInMutex != NULL)
    {
        // MSN Explorer is signed in
    }
```



 

 
