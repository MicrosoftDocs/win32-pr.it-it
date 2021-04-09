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
# <a name="creating-a-peer-identity"></a><span data-ttu-id="7f748-103">Creazione di un'identità peer</span><span class="sxs-lookup"><span data-stu-id="7f748-103">Creating a Peer Identity</span></span>

<span data-ttu-id="7f748-104">L'API di Identity Manager consente di creare un'identità peer da usare in una rete peer.</span><span class="sxs-lookup"><span data-stu-id="7f748-104">The Identity Manager API allows you to create a peer identity to use in a peer network.</span></span>

<span data-ttu-id="7f748-105">Quando si crea un'identità peer, è possibile fornire le informazioni facoltative seguenti:</span><span class="sxs-lookup"><span data-stu-id="7f748-105">When you create a peer identity, you can provide the following optional information:</span></span>

-   [<span data-ttu-id="7f748-106">Classificatore</span><span class="sxs-lookup"><span data-stu-id="7f748-106">Classifier</span></span>](peer-names.md)
-   <span data-ttu-id="7f748-107">Nome descrittivo</span><span class="sxs-lookup"><span data-stu-id="7f748-107">Friendly name</span></span>
-   <span data-ttu-id="7f748-108">Provider del servizio di crittografia</span><span class="sxs-lookup"><span data-stu-id="7f748-108">Cryptographic service provider</span></span>

> [!Note]  
> <span data-ttu-id="7f748-109">Quando possibile, usare nuovamente un'identità peer.</span><span class="sxs-lookup"><span data-stu-id="7f748-109">Whenever possible, re-use a peer identity.</span></span>

 

## <a name="example-of-creating-and-deleting-a-peer-identity"></a><span data-ttu-id="7f748-110">Esempio di creazione ed eliminazione di un'identità peer</span><span class="sxs-lookup"><span data-stu-id="7f748-110">Example of Creating and Deleting a Peer Identity</span></span>

<span data-ttu-id="7f748-111">Il frammento di codice seguente illustra come creare ed eliminare un'identità peer usando un classificatore e un nome descrittivo.</span><span class="sxs-lookup"><span data-stu-id="7f748-111">The following code snippet shows you how to create and delete a peer identity by using a classifier and friendly name.</span></span>


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



 

 



