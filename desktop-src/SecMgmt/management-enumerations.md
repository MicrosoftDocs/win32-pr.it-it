---
description: Elenca le enumerazioni utilizzate dalle funzioni di gestione dei criteri LSA.
ms.assetid: f4fd2a61-61bc-44d2-b01f-3ca07699bcb8
title: Enumerazioni di gestione della sicurezza
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 39bec2cdd731e2a3befe75e543f692d93bc5d9ad
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104231697"
---
# <a name="security-management-enumerations"></a><span data-ttu-id="e3984-103">Enumerazioni di gestione della sicurezza</span><span class="sxs-lookup"><span data-stu-id="e3984-103">Security Management Enumerations</span></span>

<span data-ttu-id="e3984-104">Di seguito sono riportate le enumerazioni di gestione della sicurezza:</span><span class="sxs-lookup"><span data-stu-id="e3984-104">The security management enumerations include the following:</span></span>

-   [<span data-ttu-id="e3984-105">Enumerazioni dei criteri LSA</span><span class="sxs-lookup"><span data-stu-id="e3984-105">LSA Policy Enumerations</span></span>](#lsa-policy-enumerations)
-   [<span data-ttu-id="e3984-106">Enumerazioni più sicure</span><span class="sxs-lookup"><span data-stu-id="e3984-106">Safer Enumerations</span></span>](#safer-enumerations)

## <a name="lsa-policy-enumerations"></a><span data-ttu-id="e3984-107">Enumerazioni dei criteri LSA</span><span class="sxs-lookup"><span data-stu-id="e3984-107">LSA Policy Enumerations</span></span>

<span data-ttu-id="e3984-108">I tipi di enumerazione seguenti vengono utilizzati dalle funzioni di gestione dei criteri LSA.</span><span class="sxs-lookup"><span data-stu-id="e3984-108">The following enumeration types are used by the LSA policy management functions.</span></span>



| <span data-ttu-id="e3984-109">Enumerazione</span><span class="sxs-lookup"><span data-stu-id="e3984-109">Enumeration</span></span>                                                                               | <span data-ttu-id="e3984-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e3984-110">Description</span></span>                                                                                                                           |
|-------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="e3984-111">**\_tipo di \_ evento di controllo dei criteri \_**</span><span class="sxs-lookup"><span data-stu-id="e3984-111">**POLICY\_AUDIT\_EVENT\_TYPE**</span></span>](/windows/desktop/api/Ntsecapi/ne-ntsecapi-policy_audit_event_type)                             | <span data-ttu-id="e3984-112">Definisce i tipi di eventi che il sistema è in grado di controllare.</span><span class="sxs-lookup"><span data-stu-id="e3984-112">Defines the types of events the system can audit.</span></span>                                                                                     |
| [<span data-ttu-id="e3984-113">**\_classe di informazioni sui criteri \_**</span><span class="sxs-lookup"><span data-stu-id="e3984-113">**POLICY\_INFORMATION\_CLASS**</span></span>](/windows/desktop/api/Ntsecapi/ne-ntsecapi-policy_information_class)                            | <span data-ttu-id="e3984-114">Definisce i tipi di informazioni che è possibile impostare o sottoporre a query per un oggetto [**criteri**](policy-object.md) .</span><span class="sxs-lookup"><span data-stu-id="e3984-114">Defines the types of information that can be set or queried for a [**Policy**](policy-object.md) object.</span></span>                             |
| [<span data-ttu-id="e3984-115">**\_ruolo del \_ server \_ LSA del criterio**</span><span class="sxs-lookup"><span data-stu-id="e3984-115">**POLICY\_LSA\_SERVER\_ROLE**</span></span>](/windows/desktop/api/Ntsecapi/ne-ntsecapi-policy_lsa_server_role)                               | <span data-ttu-id="e3984-116">Indica il ruolo di un server LSA.</span><span class="sxs-lookup"><span data-stu-id="e3984-116">Indicate the role of an LSA server.</span></span>                                                                                                   |
| [<span data-ttu-id="e3984-117">**\_classe di \_ informazioni di notifica dei criteri \_**</span><span class="sxs-lookup"><span data-stu-id="e3984-117">**POLICY\_NOTIFICATION\_INFORMATION\_CLASS**</span></span>](/windows/desktop/api/Ntsecapi/ne-ntsecapi-policy_notification_information_class) | <span data-ttu-id="e3984-118">Definisce i tipi di informazioni sui criteri e informazioni sul dominio dei criteri per cui l'applicazione può richiedere la notifica delle modifiche.</span><span class="sxs-lookup"><span data-stu-id="e3984-118">Defines the types of policy information and policy domain information for which your application can request notification of changes.</span></span> |
| [<span data-ttu-id="e3984-119">**\_stato di \_ Abilitazione del server dei criteri \_**</span><span class="sxs-lookup"><span data-stu-id="e3984-119">**POLICY\_SERVER\_ENABLE\_STATE**</span></span>](/windows/desktop/api/Ntsecapi/ne-ntsecapi-policy_server_enable_state)                       | <span data-ttu-id="e3984-120">Rappresenta lo stato del server LSA, ovvero se è abilitato o disabilitato.</span><span class="sxs-lookup"><span data-stu-id="e3984-120">Represents the state of the LSA server, that is, whether it is enabled or disabled.</span></span>                                                   |
| [<span data-ttu-id="e3984-121">**\_classe di informazioni attendibili \_**</span><span class="sxs-lookup"><span data-stu-id="e3984-121">**TRUSTED\_INFORMATION\_CLASS**</span></span>](/windows/desktop/api/Ntsecapi/ne-ntsecapi-trusted_information_class)                          | <span data-ttu-id="e3984-122">Definisce i tipi di informazioni che è possibile impostare o sottoporre a query per un dominio trusted.</span><span class="sxs-lookup"><span data-stu-id="e3984-122">Defines the types of information that can be set or queried for a trusted domain.</span></span>                                                     |



 

## <a name="safer-enumerations"></a><span data-ttu-id="e3984-123">Enumerazioni più sicure</span><span class="sxs-lookup"><span data-stu-id="e3984-123">Safer Enumerations</span></span>

<span data-ttu-id="e3984-124">[Safer](safer.md) utilizza i seguenti tipi enumerati.</span><span class="sxs-lookup"><span data-stu-id="e3984-124">[Safer](safer.md) uses the following enumerated types.</span></span>



| <span data-ttu-id="e3984-125">Nome</span><span class="sxs-lookup"><span data-stu-id="e3984-125">Name</span></span>                                                               | <span data-ttu-id="e3984-126">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e3984-126">Description</span></span>                                                                                                                                                                                      |
|--------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="e3984-127">**\_tipi di identificazione più sicuri \_**</span><span class="sxs-lookup"><span data-stu-id="e3984-127">**SAFER\_IDENTIFICATION\_TYPES**</span></span>](/windows/desktop/api/WinSafer/ne-winsafer-safer_identification_types) | <span data-ttu-id="e3984-128">Tipo di enumerazione che definisce i possibili tipi di strutture della regola di identificazione che possono essere identificati dalla struttura dell' [**\_ \_ intestazione di identificazione più sicura**](/windows/desktop/api/WinSafer/ns-winsafer-safer_identification_header) .</span><span class="sxs-lookup"><span data-stu-id="e3984-128">Enumeration type that defines the possible types of identification rule structures that can be identified by the [**SAFER\_IDENTIFICATION\_HEADER**](/windows/desktop/api/WinSafer/ns-winsafer-safer_identification_header) structure.</span></span> |
| [<span data-ttu-id="e3984-129">**\_ \_ classe informazioni sugli oggetti più sicure \_**</span><span class="sxs-lookup"><span data-stu-id="e3984-129">**SAFER\_OBJECT\_INFO\_CLASS**</span></span>](/windows/desktop/api/WinSafer/ne-winsafer-safer_object_info_class)      | <span data-ttu-id="e3984-130">Tipo di enumerazione che definisce il tipo di informazioni richieste su un oggetto più sicuro.</span><span class="sxs-lookup"><span data-stu-id="e3984-130">Enumeration type that defines the type of information requested about a Safer object.</span></span>                                                                                                            |
| [<span data-ttu-id="e3984-131">**\_ \_ classe informazioni dei criteri più sicure \_**</span><span class="sxs-lookup"><span data-stu-id="e3984-131">**SAFER\_POLICY\_INFO\_CLASS**</span></span>](/windows/desktop/api/WinSafer/ne-winsafer-safer_policy_info_class)      | <span data-ttu-id="e3984-132">Tipo di enumerazione che definisce i modi in cui è possibile eseguire una query su un criterio.</span><span class="sxs-lookup"><span data-stu-id="e3984-132">Enumeration type that defines the ways in which a policy may be queried.</span></span>                                                                                                                         |



 

 

 



