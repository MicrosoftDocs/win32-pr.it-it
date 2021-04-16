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
# <a name="determining-if-msn-is-in-the-sign-in-state"></a><span data-ttu-id="de988-103">Determinare se MSN è nello stato di accesso</span><span class="sxs-lookup"><span data-stu-id="de988-103">Determining if MSN Is in the Sign-in State</span></span>

<span data-ttu-id="de988-104">Nell'esempio di codice seguente viene illustrato l'utilizzo di un oggetto mutex per determinare se è stato eseguito l'accesso a MSN Explorer.</span><span class="sxs-lookup"><span data-stu-id="de988-104">The following code example shows the usage of a mutex object to determine if MSN Explorer is signed in.</span></span> <span data-ttu-id="de988-105">Al termine dell'utilizzo dell'handle, assicurarsi di chiamare la funzione [**CloseHandle**](/windows/win32/api/handleapi/nf-handleapi-closehandle) .</span><span class="sxs-lookup"><span data-stu-id="de988-105">When you have finished using the handle, be sure to call the [**CloseHandle**](/windows/win32/api/handleapi/nf-handleapi-closehandle) function.</span></span>

> [!Note]  
> <span data-ttu-id="de988-106">Questo oggetto mutex è disponibile per l'utilizzo nel controllo di MSN Explorer 7. stato di accesso *x* .</span><span class="sxs-lookup"><span data-stu-id="de988-106">This mutex object is available for use in checking MSN Explorer 7.*x* sign-in status.</span></span> <span data-ttu-id="de988-107">Potrebbe non essere disponibile nelle versioni successive.</span><span class="sxs-lookup"><span data-stu-id="de988-107">It may be unavailable in subsequent versions.</span></span>

 


```C++
    HANDLE hMSNSignedInMutex;

    hMSNSignedInMutex = OpenMutex(SYNCHRONIZE, FALSE, 
        "{ECCC50B5-064B-4693-B104-925714A4C74B}");

    if (hMSNSignedInMutex != NULL)
    {
        // MSN Explorer is signed in
    }
```



 

 
