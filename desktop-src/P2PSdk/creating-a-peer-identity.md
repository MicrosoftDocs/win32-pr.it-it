---
description: L'API di Identity Manager consente di creare un'identità peer da usare in una rete peer.
ms.assetid: 44b85bbc-9594-4f68-b930-51a28422b571
title: Creazione di un'identità peer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: de7d7e2a1bfba386ede4bf3f10e8b009794c3e17676abc65d797d42e203f214f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119887821"
---
# <a name="creating-a-peer-identity"></a>Creazione di un'identità peer

L'API di Identity Manager consente di creare un'identità peer da usare in una rete peer.

Quando si crea un'identità peer, è possibile fornire le informazioni facoltative seguenti:

-   [Classificatore](peer-names.md)
-   Nome descrittivo
-   Provider del servizio di crittografia

> [!Note]  
> Quando possibile, usare nuovamente un'identità peer.

 

## <a name="example-of-creating-and-deleting-a-peer-identity"></a>Esempio di creazione ed eliminazione di un'identità peer

Il frammento di codice seguente illustra come creare ed eliminare un'identità peer usando un classificatore e un nome descrittivo.


```C++
#define UNICODE
#include <p2p.h>
#include <stdio.h>

#pragma comment(lib, "p2p.lib")

//-----------------------------------------------------------------------------
// Function: CreateIdentity
//
// Purpose:  Creates a new Identity.
//
// Returns:  HRESULT
//
HRESULT CreateIdentity(PWSTR pwzFriendlyName)
{
    HRESULT     hr              = S_OK;   
    PWSTR       pwzClassifier   = L"GroupMember";
    PWSTR       pwzIdentity     = NULL;

    hr = PeerIdentityCreate(pwzClassifier, pwzFriendlyName, 0, &pwzIdentity);
    if (FAILED(hr))
    {            
        printf("Failed to create identity.");
    }
    else
    {
        printf("Identity: %s", pwzFriendlyName);
    }
       
    PeerFreeData(pwzIdentity);    

    return hr;
}


//-----------------------------------------------------------------------------
// Function: DeleteIdentity
//
// Purpose:  Delete the identity created by CreateIdentity
//
// Returns:  HRESULT
//
HRESULT DeleteIdentity()
{
    HRESULT hr = S_OK;

    if (g_pwzIdentity)
    {
        hr = PeerIdentityDelete(g_pwzIdentity);
        g_pwzIdentity = NULL;
    }

    return hr;
}
```



 

 



