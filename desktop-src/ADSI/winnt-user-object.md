---
title: Oggetto utente WinNT
description: L'oggetto utente WinNT rappresenta un account utente in un dominio Windows NT 4,0.
ms.assetid: c57016e2-538b-4f37-a1bb-699fcf3c080d
ms.tgt_platform: multiple
keywords:
- Oggetto utente WinNT ADSI
- ADSI del provider WinNT, oggetto utente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2448fbc7cd77be9c76290777b16e23b2f7e97e61
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103955070"
---
# <a name="winnt-user-object"></a><span data-ttu-id="3eb13-105">Oggetto utente WinNT</span><span class="sxs-lookup"><span data-stu-id="3eb13-105">WinNT User Object</span></span>

<span data-ttu-id="3eb13-106">L'oggetto utente WinNT rappresenta un account utente in un dominio Windows NT 4,0.</span><span class="sxs-lookup"><span data-stu-id="3eb13-106">The WinNT User object represents a user account in a Windows NT 4.0 domain.</span></span> <span data-ttu-id="3eb13-107">L'oggetto presenta funzionalità speciali.</span><span class="sxs-lookup"><span data-stu-id="3eb13-107">The object exhibits special features.</span></span> <span data-ttu-id="3eb13-108">In un'istanza di non sono supportati tutti i metodi di proprietà dell'interfaccia [**IADsUser**](/windows/desktop/api/Iads/nn-iads-iadsuser) .</span><span class="sxs-lookup"><span data-stu-id="3eb13-108">In one instance, it does not support all the property methods of the [**IADsUser**](/windows/desktop/api/Iads/nn-iads-iadsuser) interface.</span></span> <span data-ttu-id="3eb13-109">In una seconda istanza, supporta alcune proprietà personalizzate a cui è possibile accedere solo con il metodo [**IADs. Get**](/windows/desktop/api/Iads/nf-iads-iads-get) o [**IADs. Put**](/windows/desktop/api/Iads/nf-iads-iads-put) .</span><span class="sxs-lookup"><span data-stu-id="3eb13-109">In a second instance, it supports some custom properties that can be accessed only with the [**IADs.Get**](/windows/desktop/api/Iads/nf-iads-iads-get) or [**IADs.Put**](/windows/desktop/api/Iads/nf-iads-iads-put) method.</span></span>

<span data-ttu-id="3eb13-110">Per ulteriori informazioni sugli oggetti utente WinNT, vedere:</span><span class="sxs-lookup"><span data-stu-id="3eb13-110">For more information about WinNT user objects, see:</span></span>

-   [<span data-ttu-id="3eb13-111">Proprietà IADsUser non supportate</span><span class="sxs-lookup"><span data-stu-id="3eb13-111">Unsupported IADsUser Properties</span></span>](unsupported-iadsuser-properties.md)
-   [<span data-ttu-id="3eb13-112">Proprietà utente personalizzate WinNT</span><span class="sxs-lookup"><span data-stu-id="3eb13-112">WinNT Custom User Properties</span></span>](winnt-custom-user-properties.md)
-   [<span data-ttu-id="3eb13-113">Esempi di gestione degli account utente WinNT</span><span class="sxs-lookup"><span data-stu-id="3eb13-113">WinNT User Account Management Examples</span></span>](winnt-user-account-management-examples.md)

 

 




