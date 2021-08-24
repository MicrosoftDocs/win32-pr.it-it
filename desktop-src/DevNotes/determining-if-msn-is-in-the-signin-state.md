---
description: Nell'esempio di codice seguente viene illustrato l'utilizzo di un oggetto mutex per determinare se MSN Explorer è connesso.
ms.assetid: ec52a61c-9d2c-4327-977b-fb13d042bc37
title: Determinare se MSN è nello stato di accesso
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5da0abffc1735d2bf7af6ee6f9a68bf0d71ca1a2fda44176a0905c3e8faec6d3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119654192"
---
# <a name="determining-if-msn-is-in-the-sign-in-state"></a>Determinare se MSN è nello stato di accesso

Nell'esempio di codice seguente viene illustrato l'utilizzo di un oggetto mutex per determinare se MSN Explorer è connesso. Al termine dell'uso dell'handle, assicurarsi di chiamare la [**funzione CloseHandle.**](/windows/win32/api/handleapi/nf-handleapi-closehandle)

> [!Note]  
> Questo oggetto mutex è disponibile per l'uso nel controllo di MSN Explorer 7. Stato di accesso *x.* Potrebbe non essere disponibile nelle versioni successive.

 


```C++
    HANDLE hMSNSignedInMutex;

    hMSNSignedInMutex = OpenMutex(SYNCHRONIZE, FALSE, 
        "{ECCC50B5-064B-4693-B104-925714A4C74B}");

    if (hMSNSignedInMutex != NULL)
    {
        // MSN Explorer is signed in
    }
```



 

 
