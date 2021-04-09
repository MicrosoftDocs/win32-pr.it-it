---
description: L'API di Identity Manager consente di creare un'identità peer da usare in una rete peer.
ms.assetid: 44b85bbc-9594-4f68-b930-51a28422b571
title: Creazione di un'identità peer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2ab240b9fa1265ba03bfb1ce584dabed92988620
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103967541"
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



 

 



