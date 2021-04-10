---
title: Controllo del diritto di accesso a un controllo nell'elenco ACL di un oggetto
description: Per controllare l'accesso a un controllo direttamente nell'ACL di un oggetto, usare la funzione AccessCheckByTypeResultList.
ms.assetid: 5a609622-6a1a-46ae-a336-afec504225c7
ms.tgt_platform: multiple
keywords:
- Controllo di un diritto di accesso a un controllo in un annuncio ACL di oggetti
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 10170bd496da14657356a2334015975da1cc02ff
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/17/2020
ms.locfileid: "104046551"
---
# <a name="checking-a-control-access-right-in-an-objects-acl"></a><span data-ttu-id="ae982-104">Controllo del diritto di accesso a un controllo nell'elenco ACL di un oggetto</span><span class="sxs-lookup"><span data-stu-id="ae982-104">Checking a Control Access Right in an Object's ACL</span></span>

<span data-ttu-id="ae982-105">Per controllare l'accesso a un controllo direttamente nell'ACL di un oggetto, usare la funzione [**AccessCheckByTypeResultList**](/windows/desktop/api/securitybaseapi/nf-securitybaseapi-accesscheckbytyperesultlist) .</span><span class="sxs-lookup"><span data-stu-id="ae982-105">To check a control access right on an object's ACL, use the [**AccessCheckByTypeResultList**](/windows/desktop/api/securitybaseapi/nf-securitybaseapi-accesscheckbytyperesultlist) function.</span></span> <span data-ttu-id="ae982-106">Per utilizzare questa funzione, un'applicazione richiede un puntatore al [**\_ descrittore di sicurezza**](/windows/desktop/api/winnt/ns-winnt-security_descriptor) per l'oggetto anziché un'interfaccia [**IADSSECURITYDESCRIPTOR**](/windows/desktop/api/iads/nn-iads-iadssecuritydescriptor) a un oggetto com del descrittore di sicurezza ADSI.</span><span class="sxs-lookup"><span data-stu-id="ae982-106">To use this function, an application requires a pointer to the [**SECURITY\_DESCRIPTOR**](/windows/desktop/api/winnt/ns-winnt-security_descriptor) for the object instead of an [**IADsSecurityDescriptor**](/windows/desktop/api/iads/nn-iads-iadssecuritydescriptor) interface to an ADSI security descriptor COM object.</span></span>

<span data-ttu-id="ae982-107">Usare la procedura seguente per controllare l'accesso per un diritto di accesso controllato su un oggetto:</span><span class="sxs-lookup"><span data-stu-id="ae982-107">Use the following steps to check access for an controlled access right on an object:</span></span>

1.  <span data-ttu-id="ae982-108">Ottiene un puntatore di interfaccia [**IDirectoryObject**](/windows/desktop/api/iads/nn-iads-idirectoryobject) all'oggetto.</span><span class="sxs-lookup"><span data-stu-id="ae982-108">Get an [**IDirectoryObject**](/windows/desktop/api/iads/nn-iads-idirectoryobject) interface pointer to the object.</span></span>
2.  <span data-ttu-id="ae982-109">Usare il metodo [**IDirectoryObject:: GetObjectAttributes**](/windows/desktop/api/iads/nf-iads-idirectoryobject-getobjectattributes) per ottenere il descrittore di sicurezza dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="ae982-109">Use the [**IDirectoryObject::GetObjectAttributes**](/windows/desktop/api/iads/nf-iads-idirectoryobject-getobjectattributes) method to get the security descriptor of the object.</span></span> <span data-ttu-id="ae982-110">Il nome della proprietà che contiene il descrittore di sicurezza è [**ntSecurityDescriptor**](/windows/desktop/ADSchema/a-ntsecuritydescriptor).</span><span class="sxs-lookup"><span data-stu-id="ae982-110">The name of the property containing the security descriptor is [**nTSecurityDescriptor**](/windows/desktop/ADSchema/a-ntsecuritydescriptor).</span></span> <span data-ttu-id="ae982-111">La proprietà viene restituita come puntatore a una struttura di [**\_ descrittori di sicurezza**](/windows/desktop/api/winnt/ns-winnt-security_descriptor) .</span><span class="sxs-lookup"><span data-stu-id="ae982-111">The property is returned as a pointer to a [**SECURITY\_DESCRIPTOR**](/windows/desktop/api/winnt/ns-winnt-security_descriptor) structure.</span></span>
3.  <span data-ttu-id="ae982-112">Utilizzare la struttura del [**\_ descrittore di sicurezza**](/windows/desktop/api/winnt/ns-winnt-security_descriptor) con la funzione [**AccessCheckByTypeResultList**](/windows/desktop/api/securitybaseapi/nf-securitybaseapi-accesscheckbytyperesultlist) per controllare le autorizzazioni per il diritto di accesso al controllo specificato per il client specificato.</span><span class="sxs-lookup"><span data-stu-id="ae982-112">Use the [**SECURITY\_DESCRIPTOR**](/windows/desktop/api/winnt/ns-winnt-security_descriptor) structure with the [**AccessCheckByTypeResultList**](/windows/desktop/api/securitybaseapi/nf-securitybaseapi-accesscheckbytyperesultlist) function to check the permissions for the specified control access right for the specified client.</span></span>

<span data-ttu-id="ae982-113">Il codice di esempio nel [codice di esempio per verificare un diritto di accesso al controllo nell'elenco ACL di un oggetto](example-code-for-checking-a-control-access-right-in-an-objectampaposs-acl.md) Mostra in dettaglio come eseguire questa operazione.</span><span class="sxs-lookup"><span data-stu-id="ae982-113">The example code in [Example Code for Checking a Control Access Right in an Object's ACL](example-code-for-checking-a-control-access-right-in-an-objectampaposs-acl.md) shows, in detail, how to do this.</span></span>

 

 