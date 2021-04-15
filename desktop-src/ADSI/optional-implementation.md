---
title: Implementazione facoltativa
description: Le funzionalità seguenti sono facoltative, ma consigliate
ms.assetid: 6123bdda-06cf-4b8b-b2a8-89882b6341b4
ms.tgt_platform: multiple
keywords:
- Implementazione facoltativa di ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 043b07f3a9bcfaef4bde8e95458d64828d4e46be
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104515457"
---
# <a name="optional-implementation"></a><span data-ttu-id="76518-104">Implementazione facoltativa</span><span class="sxs-lookup"><span data-stu-id="76518-104">Optional Implementation</span></span>

<span data-ttu-id="76518-105">Le funzionalità seguenti sono facoltative, ma consigliate:</span><span class="sxs-lookup"><span data-stu-id="76518-105">The following features are optional, but recommended:</span></span>

-   <span data-ttu-id="76518-106">Interfaccia [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) per client non di automazione.</span><span class="sxs-lookup"><span data-stu-id="76518-106">The [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) interface for non-Automation clients.</span></span> <span data-ttu-id="76518-107">Poiché il provider di OLE DB ADSI utilizza **IDirectorySearch** per presentare le query e raccogliere i risultati dal servizio directory sottostante, i provider che implementano questa interfaccia forniscono automaticamente l'accesso ai database di OLE DB Style senza implementare interfacce aggiuntive.</span><span class="sxs-lookup"><span data-stu-id="76518-107">Because the ADSI OLE DB provider uses **IDirectorySearch** to present queries and collect results from the underlying directory service, providers that implement this interface automatically provide access to OLE DB style databases without having to implement any additional interfaces.</span></span>
-   <span data-ttu-id="76518-108">Interfacce [**IADsSecurityDescriptor**](/windows/desktop/api/Iads/nn-iads-iadssecuritydescriptor), [**IADsAccessControlList**](/windows/desktop/api/Iads/nn-iads-iadsaccesscontrollist)e [**IADsAccessControlEntry**](/windows/desktop/api/Iads/nn-iads-iadsaccesscontrolentry) .</span><span class="sxs-lookup"><span data-stu-id="76518-108">The [**IADsSecurityDescriptor**](/windows/desktop/api/Iads/nn-iads-iadssecuritydescriptor), [**IADsAccessControlList**](/windows/desktop/api/Iads/nn-iads-iadsaccesscontrollist), and [**IADsAccessControlEntry**](/windows/desktop/api/Iads/nn-iads-iadsaccesscontrolentry) interfaces.</span></span> <span data-ttu-id="76518-109">I provider per i servizi directory che supportano la sicurezza degli oggetti basata su ACL sono invitati a implementare queste funzionalità aggiuntive.</span><span class="sxs-lookup"><span data-stu-id="76518-109">Providers for directory services that support ACL-based object security are encouraged to implement these additional features.</span></span>

 

 




