---
description: Elenca e illustra i diritti di accesso dell'oggetto TrustedDomain.
ms.assetid: eb82864c-7e69-4ed5-a55d-d6792670bcd1
title: Diritti di accesso agli oggetti TrustedDomain
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4f79dc44b54ff907cbe3d1f700cc673f75a40d57
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106306414"
---
# <a name="trusteddomain-object-access-rights"></a><span data-ttu-id="29cac-103">Diritti di accesso agli oggetti TrustedDomain</span><span class="sxs-lookup"><span data-stu-id="29cac-103">TrustedDomain Object Access Rights</span></span>

<span data-ttu-id="29cac-104">Il tipo di oggetto [**trustedDomain**](trusteddomain-object.md) presenta i tipi di accesso seguenti:</span><span class="sxs-lookup"><span data-stu-id="29cac-104">The [**TrustedDomain**](trusteddomain-object.md) object type has the following access types:</span></span>



| <span data-ttu-id="29cac-105">Tipo di accesso</span><span class="sxs-lookup"><span data-stu-id="29cac-105">Access type</span></span>                  | <span data-ttu-id="29cac-106">Descrizione</span><span class="sxs-lookup"><span data-stu-id="29cac-106">Description</span></span>                                                                      |
|------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="29cac-107">\_nome di \_ dominio di query attendibile \_</span><span class="sxs-lookup"><span data-stu-id="29cac-107">TRUSTED\_QUERY\_DOMAIN\_NAME</span></span> | <span data-ttu-id="29cac-108">Questo tipo di accesso è necessario per eseguire una query sul nome del dominio attendibile.</span><span class="sxs-lookup"><span data-stu-id="29cac-108">This access type is needed to query the name of the trusted domain.</span></span>              |
| <span data-ttu-id="29cac-109">\_Controller Set attendibili \_</span><span class="sxs-lookup"><span data-stu-id="29cac-109">TRUSTED\_SET\_CONTROLLERS</span></span>    | <span data-ttu-id="29cac-110">Questo tipo di accesso è necessario per impostare l'elenco dei controller del dominio trusted.</span><span class="sxs-lookup"><span data-stu-id="29cac-110">This access type is needed to set the list of controllers of the trusted domain.</span></span> |
| <span data-ttu-id="29cac-111">QUERY ATTENDIBILe \_ \_ POSIX</span><span class="sxs-lookup"><span data-stu-id="29cac-111">TRUSTED\_QUERY\_POSIX</span></span>        | <span data-ttu-id="29cac-112">Questo tipo di accesso è necessario per recuperare l'offset dell'ID POSIX di un dominio trusted.</span><span class="sxs-lookup"><span data-stu-id="29cac-112">This access type is needed to retrieve the Posix ID offset of a trusted domain.</span></span>  |
| <span data-ttu-id="29cac-113">SET ATTENDIBILe \_ \_ POSIX</span><span class="sxs-lookup"><span data-stu-id="29cac-113">TRUSTED\_SET\_POSIX</span></span>          | <span data-ttu-id="29cac-114">Questo tipo di accesso è necessario per impostare l'offset dell'ID POSIX di un dominio trusted.</span><span class="sxs-lookup"><span data-stu-id="29cac-114">This access type is needed to set the Posix ID offset of a trusted domain.</span></span>       |



 

## <a name="generic-access-masks"></a><span data-ttu-id="29cac-115">Maschere di accesso generico</span><span class="sxs-lookup"><span data-stu-id="29cac-115">Generic Access Masks</span></span>

<span data-ttu-id="29cac-116">Questo tipo di oggetto ha i mapping di accesso generici seguenti:</span><span class="sxs-lookup"><span data-stu-id="29cac-116">This object type has the following generic access mappings:</span></span>

``` syntax
    GENERIC_READ        STANDARD_RIGHTS_READ |
                    TRUSTED_QUERY_DOMAIN_NAME

    GENERIC_WRITE        STANDARD_RIGHTS_WRITE |
                    TRUSTED_SET_POSIX

    GENERIC_EXECUTE    STANDARD_RIGHTS_EXECUTE |
                    TRUSTED_QUERY_POSIX
```

## <a name="standard-access-types"></a><span data-ttu-id="29cac-117">Tipi di accesso standard</span><span class="sxs-lookup"><span data-stu-id="29cac-117">Standard Access Types</span></span>

<span data-ttu-id="29cac-118">Questo oggetto non supporta il tipo di accesso standard (facoltativo) SYNCHRONIZE.</span><span class="sxs-lookup"><span data-stu-id="29cac-118">This object does not support the (optional) SYNCHRONIZE standard access type.</span></span> <span data-ttu-id="29cac-119">Sono supportati tutti i tipi di accesso necessari.</span><span class="sxs-lookup"><span data-stu-id="29cac-119">All required access types are supported.</span></span> <span data-ttu-id="29cac-120">La maschera di tutti i tipi di accesso supportati per questo tipo di oggetto è:</span><span class="sxs-lookup"><span data-stu-id="29cac-120">The mask of all supported access types for this object type is:</span></span>

``` syntax
    TRUSTED_ALL_ACCESS    STANDARD_RIGHTS_REQUIRED |
                    TRUSTED_QUERY_DOMAIN_NAME |
                    TRUSTED_QUERY_CONTROLLERS |
                    TRUSTED_SET_CONTROLLERS
```

 

 



