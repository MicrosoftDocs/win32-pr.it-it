---
title: Funzioni modali utente
description: Le funzioni modali utente Gestione rete ottengono e impostano parametri a livello di sistema correlati al comportamento del sistema di sicurezza.
ms.assetid: e655b9f6-2808-4bd4-998c-c8a2e980920b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c65595f78a412196b9fd54030ec1ac1f1fb8ae59
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "103963390"
---
# <a name="user-modal-functions"></a><span data-ttu-id="6ef7d-103">Funzioni modali utente</span><span class="sxs-lookup"><span data-stu-id="6ef7d-103">User Modal Functions</span></span>

<span data-ttu-id="6ef7d-104">Le funzioni modali utente Gestione rete ottengono e impostano parametri a livello di sistema correlati al comportamento del sistema di sicurezza.</span><span class="sxs-lookup"><span data-stu-id="6ef7d-104">The network management user modal functions get and set system-wide parameters related to security system behavior.</span></span>

<span data-ttu-id="6ef7d-105">Le funzioni modali utente sono elencate di seguito.</span><span class="sxs-lookup"><span data-stu-id="6ef7d-105">The user modal functions are listed following.</span></span>



| <span data-ttu-id="6ef7d-106">Funzione</span><span class="sxs-lookup"><span data-stu-id="6ef7d-106">Function</span></span>                                     | <span data-ttu-id="6ef7d-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="6ef7d-107">Description</span></span>                                                                                                                                                                                             |
|----------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="6ef7d-108">**NetUserModalsGet**</span><span class="sxs-lookup"><span data-stu-id="6ef7d-108">**NetUserModalsGet**</span></span>](/windows/desktop/api/Lmaccess/nf-lmaccess-netusermodalsget) | <span data-ttu-id="6ef7d-109">Restituisce informazioni globali per tutti gli utenti e i gruppi globali nel database di sicurezza, ovvero il database di gestione degli account di sicurezza (SAM) o, nel caso di controller di dominio, il Active Directory.</span><span class="sxs-lookup"><span data-stu-id="6ef7d-109">Returns global information for all users and global groups in the security database, which is the security accounts manager (SAM) database or, in the case of domain controllers, the Active Directory.</span></span> |
| [<span data-ttu-id="6ef7d-110">**NetUserModalsSet**</span><span class="sxs-lookup"><span data-stu-id="6ef7d-110">**NetUserModalsSet**</span></span>](/windows/desktop/api/Lmaccess/nf-lmaccess-netusermodalsset) | <span data-ttu-id="6ef7d-111">Imposta le informazioni globali per tutti gli utenti e i gruppi globali nel database di sicurezza.</span><span class="sxs-lookup"><span data-stu-id="6ef7d-111">Sets global information for all users and global groups in the security database.</span></span>                                                                                                                       |



 

<span data-ttu-id="6ef7d-112">Le funzioni **NetUserModalsGet** e **NetUserModalsSet** esaminano e modificano le impostazioni modali, che sono parametri globali che interessano ogni account nel database di sicurezza, ad esempio la lunghezza minima consentita per la password.</span><span class="sxs-lookup"><span data-stu-id="6ef7d-112">The **NetUserModalsGet** and **NetUserModalsSet** functions examine and modify the modal settings, which are global parameters that affect every account in the security database (for example, the minimum allowable password length).</span></span> <span data-ttu-id="6ef7d-113">Tutte le impostazioni modali possono essere modificate chiamando **NetUserModalsSet**.</span><span class="sxs-lookup"><span data-stu-id="6ef7d-113">All modal settings can be altered by calling **NetUserModalsSet**.</span></span> <span data-ttu-id="6ef7d-114">La maggior parte dei modale può essere modificata anche usando il comando **net accounts** .</span><span class="sxs-lookup"><span data-stu-id="6ef7d-114">Most of the modals can also be altered by using the **net accounts** command.</span></span> <span data-ttu-id="6ef7d-115">Per le funzioni modali utente di gestione di rete non è necessario che il server disponga di sicurezza a livello di utente.</span><span class="sxs-lookup"><span data-stu-id="6ef7d-115">The network management user modal functions do not require the server to have user-level security.</span></span>

<span data-ttu-id="6ef7d-116">Le informazioni modali dell'utente sono disponibili ai livelli seguenti:</span><span class="sxs-lookup"><span data-stu-id="6ef7d-116">User modal information is available at the following levels:</span></span>

-   [<span data-ttu-id="6ef7d-117">**\_Informazioni sulle modalità \_ utente \_ 0**</span><span class="sxs-lookup"><span data-stu-id="6ef7d-117">**USER\_MODALS\_INFO\_0**</span></span>](/windows/desktop/api/Lmaccess/ns-lmaccess-user_modals_info_0)
-   [<span data-ttu-id="6ef7d-118">**\_Informazioni sulle modalità \_ utente \_ 1**</span><span class="sxs-lookup"><span data-stu-id="6ef7d-118">**USER\_MODALS\_INFO\_1**</span></span>](/windows/desktop/api/Lmaccess/ns-lmaccess-user_modals_info_1)
-   [<span data-ttu-id="6ef7d-119">**\_Informazioni sulle modalità \_ utente \_ 2**</span><span class="sxs-lookup"><span data-stu-id="6ef7d-119">**USER\_MODALS\_INFO\_2**</span></span>](/windows/desktop/api/Lmaccess/ns-lmaccess-user_modals_info_2)
-   [<span data-ttu-id="6ef7d-120">**\_Informazioni sulle modalità \_ utente \_ 3**</span><span class="sxs-lookup"><span data-stu-id="6ef7d-120">**USER\_MODALS\_INFO\_3**</span></span>](/windows/desktop/api/Lmaccess/ns-lmaccess-user_modals_info_3)

<span data-ttu-id="6ef7d-121">I livelli di informazioni seguenti sono validi solo per [**NetUserModalsSet**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusermodalsset) e sostituiscono il modo precedente di passare un *Parmnum* per impostare un campo specifico:</span><span class="sxs-lookup"><span data-stu-id="6ef7d-121">The following information levels are valid only for [**NetUserModalsSet**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusermodalsset) and replace the older way of passing in a *Parmnum* to set a specific field:</span></span>

-   [<span data-ttu-id="6ef7d-122">**\_Informazioni sulle modalità \_ utente \_ 1001**</span><span class="sxs-lookup"><span data-stu-id="6ef7d-122">**USER\_MODALS\_INFO\_1001**</span></span>](/windows/desktop/api/Lmaccess/ns-lmaccess-user_modals_info_1001)
-   [<span data-ttu-id="6ef7d-123">**\_Informazioni sulle modalità \_ utente \_ 1002**</span><span class="sxs-lookup"><span data-stu-id="6ef7d-123">**USER\_MODALS\_INFO\_1002**</span></span>](/windows/desktop/api/Lmaccess/ns-lmaccess-user_modals_info_1002)
-   [<span data-ttu-id="6ef7d-124">**\_Informazioni sulle modalità \_ utente \_ 1003**</span><span class="sxs-lookup"><span data-stu-id="6ef7d-124">**USER\_MODALS\_INFO\_1003**</span></span>](/windows/desktop/api/Lmaccess/ns-lmaccess-user_modals_info_1003)
-   [<span data-ttu-id="6ef7d-125">**\_Informazioni sulle modalità \_ utente \_ 1004**</span><span class="sxs-lookup"><span data-stu-id="6ef7d-125">**USER\_MODALS\_INFO\_1004**</span></span>](/windows/desktop/api/Lmaccess/ns-lmaccess-user_modals_info_1004)
-   [<span data-ttu-id="6ef7d-126">**\_Informazioni sulle modalità \_ utente \_ 1005**</span><span class="sxs-lookup"><span data-stu-id="6ef7d-126">**USER\_MODALS\_INFO\_1005**</span></span>](/windows/desktop/api/Lmaccess/ns-lmaccess-user_modals_info_1005)
-   [<span data-ttu-id="6ef7d-127">**\_Informazioni sulle modalità \_ utente \_ 1006**</span><span class="sxs-lookup"><span data-stu-id="6ef7d-127">**USER\_MODALS\_INFO\_1006**</span></span>](/windows/desktop/api/Lmaccess/ns-lmaccess-user_modals_info_1006)
-   [<span data-ttu-id="6ef7d-128">**\_Informazioni sulle modalità \_ utente \_ 1007**</span><span class="sxs-lookup"><span data-stu-id="6ef7d-128">**USER\_MODALS\_INFO\_1007**</span></span>](/windows/desktop/api/Lmaccess/ns-lmaccess-user_modals_info_1007)

<span data-ttu-id="6ef7d-129">Se si sta programmando per Active Directory, è possibile chiamare determinati metodi di Active Directory Service Interface (ADSI) per ottenere la stessa funzionalità che è possibile ottenere chiamando le funzioni modali dell'utente di gestione della rete.</span><span class="sxs-lookup"><span data-stu-id="6ef7d-129">If you are programming for Active Directory, you may be able to call certain Active Directory Service Interface (ADSI) methods to achieve the same functionality you can achieve by calling the network management user modal functions.</span></span> <span data-ttu-id="6ef7d-130">Per ulteriori informazioni, vedere [**IADsDomain**](/windows/desktop/api/iads/nn-iads-iadsdomain).</span><span class="sxs-lookup"><span data-stu-id="6ef7d-130">For more information, see [**IADsDomain**](/windows/desktop/api/iads/nn-iads-iadsdomain).</span></span>

 

 