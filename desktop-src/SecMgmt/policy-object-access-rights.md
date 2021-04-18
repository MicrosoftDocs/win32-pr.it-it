---
description: Elenca e descrive i tipi di accesso dell'oggetto criteri.
ms.assetid: 592dea65-9da1-4e49-82e4-8e08c451e026
title: Diritti di accesso agli oggetti Criteri
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e2e5c762955a4c53015241086b2249c5edbc4f12
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106306434"
---
# <a name="policy-object-access-rights"></a><span data-ttu-id="74446-103">Diritti di accesso agli oggetti Criteri</span><span class="sxs-lookup"><span data-stu-id="74446-103">Policy Object Access Rights</span></span>

<span data-ttu-id="74446-104">L'oggetto [**policy**](policy-object.md) dispone dei seguenti tipi di accesso specifici per gli oggetti:</span><span class="sxs-lookup"><span data-stu-id="74446-104">The [**Policy**](policy-object.md) object has the following object-specific access types:</span></span>



| <span data-ttu-id="74446-105">Tipo di accesso</span><span class="sxs-lookup"><span data-stu-id="74446-105">Access type</span></span>                         | <span data-ttu-id="74446-106">Descrizione</span><span class="sxs-lookup"><span data-stu-id="74446-106">Description</span></span>                                                                                                                                                                                                                                                                                                                                                        |
|-------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="74446-107">\_ \_ informazioni locali visualizzazione \_ criteri</span><span class="sxs-lookup"><span data-stu-id="74446-107">POLICY\_VIEW\_LOCAL\_INFORMATION</span></span>    | <span data-ttu-id="74446-108">Questo tipo di accesso è necessario per leggere le varie informazioni sui criteri di sicurezza del sistema di destinazione.</span><span class="sxs-lookup"><span data-stu-id="74446-108">This access type is needed to read the target system's miscellaneous security policy information.</span></span> <span data-ttu-id="74446-109">Sono incluse la quota predefinita, il controllo, lo stato del server e le informazioni sui ruoli e le informazioni sull'attendibilità.</span><span class="sxs-lookup"><span data-stu-id="74446-109">This includes the default quota, auditing, server state and role information, and trust information.</span></span> <span data-ttu-id="74446-110">Questo tipo di accesso è necessario anche per enumerare domini, account e [*privilegi*](/windows/desktop/SecGloss/p-gly)attendibili.</span><span class="sxs-lookup"><span data-stu-id="74446-110">This access type is also needed to enumerate trusted domains, accounts, and [*privileges*](/windows/desktop/SecGloss/p-gly).</span></span> |
| <span data-ttu-id="74446-111">\_ottenere \_ informazioni private \_ sui criteri</span><span class="sxs-lookup"><span data-stu-id="74446-111">POLICY\_GET\_PRIVATE\_INFORMATION</span></span>   | <span data-ttu-id="74446-112">Questo tipo di accesso è necessario per visualizzare informazioni riservate, ad esempio i nomi degli account stabiliti per le relazioni di dominio trusted.</span><span class="sxs-lookup"><span data-stu-id="74446-112">This access type is needed to view sensitive information, such as the names of accounts established for trusted domain relationships.</span></span>                                                                                                                                                                                                                              |
| <span data-ttu-id="74446-113">\_amministratore attendibilità criteri \_</span><span class="sxs-lookup"><span data-stu-id="74446-113">POLICY\_TRUST\_ADMIN</span></span>                | <span data-ttu-id="74446-114">Questo tipo di accesso è necessario per modificare le informazioni sul dominio dell'account o sul dominio primario.</span><span class="sxs-lookup"><span data-stu-id="74446-114">This access type is needed to change the account domain or primary domain information.</span></span>                                                                                                                                                                                                                                                                             |
| <span data-ttu-id="74446-115">\_limiti di \_ \_ quota predefiniti impostati dal \_ criterio</span><span class="sxs-lookup"><span data-stu-id="74446-115">POLICY\_SET\_DEFAULT\_QUOTA\_LIMITS</span></span> | <span data-ttu-id="74446-116">Impostare le quote di sistema predefinite che vengono applicate agli account utente.</span><span class="sxs-lookup"><span data-stu-id="74446-116">Set the default system quotas that are applied to user accounts.</span></span>                                                                                                                                                                                                                                                                                                   |
| <span data-ttu-id="74446-117">creazione di un \_ \_ segreto criterio</span><span class="sxs-lookup"><span data-stu-id="74446-117">POLICY\_CREATE\_SECRET</span></span>              | <span data-ttu-id="74446-118">Questo tipo di accesso è necessario per creare un nuovo oggetto dati privato.</span><span class="sxs-lookup"><span data-stu-id="74446-118">This access type is needed to create a new Private Data object.</span></span>                                                                                                                                                                                                                                                                                                    |
| <span data-ttu-id="74446-119">\_account creazione \_ criteri</span><span class="sxs-lookup"><span data-stu-id="74446-119">POLICY\_CREATE\_ACCOUNT</span></span>             | <span data-ttu-id="74446-120">Questo tipo di accesso è necessario per creare un nuovo oggetto [**account**](account-object.md) .</span><span class="sxs-lookup"><span data-stu-id="74446-120">This access type is needed to create a new [**Account**](account-object.md) object.</span></span>                                                                                                                                                                                                                                                                               |
| <span data-ttu-id="74446-121">\_requisiti di \_ controllo per set di criteri \_</span><span class="sxs-lookup"><span data-stu-id="74446-121">POLICY\_SET\_AUDIT\_REQUIREMENTS</span></span>    | <span data-ttu-id="74446-122">Questo tipo di accesso è necessario per aggiornare i requisiti di controllo del sistema.</span><span class="sxs-lookup"><span data-stu-id="74446-122">This access type is needed to update the auditing requirements of the system.</span></span>                                                                                                                                                                                                                                                                                      |
| <span data-ttu-id="74446-123">\_ \_ Amministrazione log di controllo dei criteri \_</span><span class="sxs-lookup"><span data-stu-id="74446-123">POLICY\_AUDIT\_LOG\_ADMIN</span></span>           | <span data-ttu-id="74446-124">Questo tipo di accesso è necessario per modificare le caratteristiche del audit trail, ad esempio le dimensioni massime o il periodo di conservazione per i record di controllo, oppure per cancellare il log.</span><span class="sxs-lookup"><span data-stu-id="74446-124">This access type is needed to change the characteristics of the audit trail such as its maximum size or the retention period for audit records, or to clear the log.</span></span>                                                                                                                                                                                               |
| <span data-ttu-id="74446-125">\_informazioni di \_ controllo \_ visualizzazione criteri</span><span class="sxs-lookup"><span data-stu-id="74446-125">POLICY\_VIEW\_AUDIT\_INFORMATION</span></span>    | <span data-ttu-id="74446-126">Questo tipo di accesso è necessario per visualizzare le informazioni sui requisiti di audit trail o controllo.</span><span class="sxs-lookup"><span data-stu-id="74446-126">This access type is needed to view audit trail or audit requirements information.</span></span>                                                                                                                                                                                                                                                                                  |
| <span data-ttu-id="74446-127">\_amministratore server dei criteri \_</span><span class="sxs-lookup"><span data-stu-id="74446-127">POLICY\_SERVER\_ADMIN</span></span>               | <span data-ttu-id="74446-128">Questo tipo di accesso è necessario per modificare le informazioni sullo stato del server o sul ruolo (Master/replica).</span><span class="sxs-lookup"><span data-stu-id="74446-128">This access type is needed to modify the server state or role (master/replica) information.</span></span> <span data-ttu-id="74446-129">È anche necessario modificare le informazioni relative all'origine e al nome dell'account di replica.</span><span class="sxs-lookup"><span data-stu-id="74446-129">It is also needed to change the replica source and account name information.</span></span>                                                                                                                                                                                           |
| <span data-ttu-id="74446-130">\_nomi di ricerca criteri \_</span><span class="sxs-lookup"><span data-stu-id="74446-130">POLICY\_LOOKUP\_NAMES</span></span>               | <span data-ttu-id="74446-131">Questo tipo di accesso è necessario per la conversione tra nomi e SID.</span><span class="sxs-lookup"><span data-stu-id="74446-131">This access type is needed to translate between names and SIDs.</span></span>                                                                                                                                                                                                                                                                                                    |
| <span data-ttu-id="74446-132">\_privilegio Creazione \_ criteri</span><span class="sxs-lookup"><span data-stu-id="74446-132">POLICY\_CREATE\_PRIVILEGE</span></span>           | <span data-ttu-id="74446-133">Non ancora supportato.</span><span class="sxs-lookup"><span data-stu-id="74446-133">Not yet supported.</span></span>                                                                                                                                                                                                                                                                                                                                                 |



 

## <a name="generic-access-masks"></a><span data-ttu-id="74446-134">Maschere di accesso generico</span><span class="sxs-lookup"><span data-stu-id="74446-134">Generic Access Masks</span></span>

<span data-ttu-id="74446-135">L'oggetto [**policy**](policy-object.md) pubblica i mapping seguenti dai tipi di accesso generici ai tipi di accesso specifici:</span><span class="sxs-lookup"><span data-stu-id="74446-135">The [**Policy**](policy-object.md) object publishes the following mappings from generic access types to specific access types:</span></span>

``` syntax
    GENERIC_READ    STANDARD_RIGHTS_READ |
                    POLICY_VIEW_AUDIT_INFORMATION |
                    POLICY_GET_PRIVATE_INFORMATION

    GENERIC_WRITE   STANDARD_RIGHTS_WRITE |
                    POLICY_TRUST_ADMIN |
                    POLICY_CREATE_ACCOUNT |
                    POLICY_CREATE_SECRET |
                    POLICY_CREATE_PRIVILEGE |
                    POLICY_SET_DEFAULT_QUOTA_LIMITS |
                    POLICY_SET_AUDIT_REQUIREMENTS |
                    POLICY_AUDIT_LOG_ADMIN |
                                        POLICY_SERVER_ADMIN

    GENERIC_EXECUTE STANDARD_RIGHTS_EXECUTE |
                    POLICY_VIEW_LOCAL_INFORMATION |
                    POLICY_LOOKUP_NAMES
```

## <a name="standard-access-types"></a><span data-ttu-id="74446-136">Tipi di accesso standard</span><span class="sxs-lookup"><span data-stu-id="74446-136">Standard Access Types</span></span>

<span data-ttu-id="74446-137">Questo oggetto non supporta il tipo di accesso standard (facoltativo) SYNCHRONIZE.</span><span class="sxs-lookup"><span data-stu-id="74446-137">This object does not support the (optional) SYNCHRONIZE standard access type.</span></span> <span data-ttu-id="74446-138">Sono supportati tutti i tipi di accesso necessari.</span><span class="sxs-lookup"><span data-stu-id="74446-138">All required access types are supported.</span></span> <span data-ttu-id="74446-139">La maschera di tutti i tipi di accesso supportati per questo tipo di oggetto è:</span><span class="sxs-lookup"><span data-stu-id="74446-139">The mask of all supported access types for this object type is:</span></span>

``` syntax
    POLICY_ALL_ACCESS STANDARD_RIGHTS_REQUIRED |
                    POLICY_VIEW_LOCAL_INFORMATION |
                    POLICY_VIEW_AUDIT_INFORMATION |
                    POLICY_GET_PRIVATE_INFORMATION |
                    POLICY_TRUST_ADMIN |
                    POLICY_CREATE_ACCOUNT |
                    POLICY_CREATE_SECRET |
                    POLICY_CREATE_PRIVILEGE |
                    POLICY_SET_DEFAULT_QUOTA_LIMITS |
                    POLICY_SET_AUDIT_REQUIREMENTS |
                    POLICY_AUDIT_LOG_ADMIN |
                    POLICY_SERVER_ADMIN
                    POLICY_LOOKUP_NAMES
```

 

 
