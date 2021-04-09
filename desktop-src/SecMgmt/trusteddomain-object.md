---
description: L'oggetto TrustedDomain archivia le informazioni su una relazione di trust con un dominio.
ms.assetid: fab69367-2143-49ef-a1b9-9c1d846fd4e1
title: Oggetto TrustedDomain
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 837d8a9e56273a87b22b9697ef4e5917d73bcc81
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103878941"
---
# <a name="trusteddomain-object"></a><span data-ttu-id="baff7-103">Oggetto TrustedDomain</span><span class="sxs-lookup"><span data-stu-id="baff7-103">TrustedDomain Object</span></span>

<span data-ttu-id="baff7-104">L'oggetto **trustedDomain** archivia le informazioni su una relazione di trust con un dominio.</span><span class="sxs-lookup"><span data-stu-id="baff7-104">The **TrustedDomain** object stores information about a trust relationship with a domain.</span></span> <span data-ttu-id="baff7-105">Un oggetto **trustedDomain** viene creato nel sistema trusting per identificare un account all'interno del dominio trusted che può essere utilizzato per inviare richieste di autenticazione ed eseguire altre operazioni, ad esempio le conversioni di nome e [*ID di sicurezza*](/windows/desktop/SecGloss/s-gly) (SID).</span><span class="sxs-lookup"><span data-stu-id="baff7-105">A **TrustedDomain** object is created on the trusting system to identify an account within the trusted domain that can be used to submit authentication requests and to perform other operations, such as name and [*security identifier*](/windows/desktop/SecGloss/s-gly) (SID) translations.</span></span>

<span data-ttu-id="baff7-106">Le informazioni archiviate in un oggetto **trustedDomain** includono:</span><span class="sxs-lookup"><span data-stu-id="baff7-106">The information stored in a **TrustedDomain** object includes:</span></span>

-   <span data-ttu-id="baff7-107">SID del dominio attendibile.</span><span class="sxs-lookup"><span data-stu-id="baff7-107">The SID of the trusted domain.</span></span> <span data-ttu-id="baff7-108">Queste informazioni non sono modificabili e devono essere univoche tra tutti gli oggetti **trustedDomain** .</span><span class="sxs-lookup"><span data-stu-id="baff7-108">This information is not modifiable and must be unique among all **TrustedDomain** objects.</span></span>
-   <span data-ttu-id="baff7-109">Nome del dominio attendibile.</span><span class="sxs-lookup"><span data-stu-id="baff7-109">The name of the trusted domain.</span></span> <span data-ttu-id="baff7-110">Queste informazioni non sono modificabili e devono essere univoche tra tutti gli oggetti **trustedDomain** .</span><span class="sxs-lookup"><span data-stu-id="baff7-110">This information is not modifiable and must be unique among all **TrustedDomain** objects.</span></span>
-   <span data-ttu-id="baff7-111">Nome dell'account nel dominio trusted utilizzato per inviare le richieste di autenticazione e per eseguire traduzioni di nome e SID.</span><span class="sxs-lookup"><span data-stu-id="baff7-111">The name of the account in the trusted domain used to submit authentication requests and to perform name and SID translations.</span></span> <span data-ttu-id="baff7-112">Questo nome non è modificabile.</span><span class="sxs-lookup"><span data-stu-id="baff7-112">This name is not modifiable.</span></span>
-   <span data-ttu-id="baff7-113">Password utilizzata per inviare richieste di autenticazione ed eseguire traduzioni di nome e SID.</span><span class="sxs-lookup"><span data-stu-id="baff7-113">The password used to submit authentication requests and perform name and SID translations.</span></span>

<span data-ttu-id="baff7-114">Per ulteriori informazioni, vedere [il tipo di oggetto trustedDomain](the-trusteddomain-object-type.md).</span><span class="sxs-lookup"><span data-stu-id="baff7-114">For more information, see [The TrustedDomain Object Type](the-trusteddomain-object-type.md).</span></span>

 

 
