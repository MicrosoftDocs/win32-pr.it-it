---
title: Messaggi di errore estesi ADSI
description: Questo argomento contiene un elenco di argomenti che illustrano come usare i messaggi di errore ADSI restituiti da IADs, IADsContainer, IDirectoryObject e IDirectorySearch.
ms.assetid: cfec86cb-fe90-4e2b-8c9d-06e175253fa4
ms.tgt_platform: multiple
keywords:
- Messaggi di errore estesi ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ab374f18892c0ff336ef588dce477db60405ab19
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104044081"
---
# <a name="adsi-extended-error-messages"></a><span data-ttu-id="9c823-104">Messaggi di errore estesi ADSI</span><span class="sxs-lookup"><span data-stu-id="9c823-104">ADSI Extended Error Messages</span></span>

<span data-ttu-id="9c823-105">Oltre ai valori **HRESULT** , diversi provider di sistema ADSI (per lo più LDAP) restituiscono dati di errore aggiuntivi per le operazioni eseguite dalle interfacce seguenti:</span><span class="sxs-lookup"><span data-stu-id="9c823-105">Apart from the **HRESULT** values, several ADSI system providers (mostly LDAP) return additional error data for operations performed by the following interfaces:</span></span>

-   [<span data-ttu-id="9c823-106">**IADs**</span><span class="sxs-lookup"><span data-stu-id="9c823-106">**IADs**</span></span>](/windows/desktop/api/Iads/nn-iads-iads)
-   [<span data-ttu-id="9c823-107">**IADsContainer**</span><span class="sxs-lookup"><span data-stu-id="9c823-107">**IADsContainer**</span></span>](/windows/desktop/api/Iads/nn-iads-iadscontainer)
-   [<span data-ttu-id="9c823-108">**IDirectoryObject**</span><span class="sxs-lookup"><span data-stu-id="9c823-108">**IDirectoryObject**</span></span>](/windows/desktop/api/Iads/nn-iads-idirectoryobject)
-   [<span data-ttu-id="9c823-109">**IDirectorySearch**</span><span class="sxs-lookup"><span data-stu-id="9c823-109">**IDirectorySearch**</span></span>](/windows/desktop/api/Iads/nn-iads-idirectorysearch)

<span data-ttu-id="9c823-110">Una parte di tali dati degli errori estesi è la stringa inviata dal server come parte del risultato del messaggio.</span><span class="sxs-lookup"><span data-stu-id="9c823-110">A part of such extended error data is the string sent by the server as a part of the message result.</span></span>

<span data-ttu-id="9c823-111">Chiamare [**ADsGetLastError**](/windows/desktop/api/Adshlp/nf-adshlp-adsgetlasterror) per recuperare tali messaggi di errore estesi.</span><span class="sxs-lookup"><span data-stu-id="9c823-111">Call [**ADsGetLastError**](/windows/desktop/api/Adshlp/nf-adshlp-adsgetlasterror) to retrieve such extended error messages.</span></span> <span data-ttu-id="9c823-112">Il primo parametro di questa funzione, *lpError*, è un valore **DWORD** .</span><span class="sxs-lookup"><span data-stu-id="9c823-112">The first parameter of this function, *lpError*, is a **DWORD** value.</span></span> <span data-ttu-id="9c823-113">Per un server di Active Directory, ADSI tenta di eseguire il mapping di un messaggio di errore LDAP a un codice di errore Win32 appropriato e assegna il valore del codice di errore Win32 a *lpError*.</span><span class="sxs-lookup"><span data-stu-id="9c823-113">For an Active Directory server, ADSI attempts to map an LDAP error message to an appropriate Win32 error code and assigns the Win32 error code value to *lpError*.</span></span> <span data-ttu-id="9c823-114">Se non si riesce a risolvere il mapping, ADSI assegna i **dati di errore \_ non validi \_** a *lpError*, come per qualsiasi altro server di directory.</span><span class="sxs-lookup"><span data-stu-id="9c823-114">Failing to resolve the mapping, ADSI assigns **ERROR\_INVALID\_DATA** to *lpError*, as it does for any other directory server.</span></span> <span data-ttu-id="9c823-115">In tutti i casi, ADSI inoltra in modo fedele la stringa della descrizione dell'errore dal server al client tramite *lpErrorBuf*, il secondo parametro della funzione **ADsGetLastError** .</span><span class="sxs-lookup"><span data-stu-id="9c823-115">In all cases, ADSI faithfully relays the string of the error description from the server to the client through *lpErrorBuf*, the second parameter of the **ADsGetLastError** function.</span></span>

 

 




