---
description: Il tipo di diritti di accesso agli oggetti account ha i seguenti tipi di accesso.
ms.assetid: 42fb22bb-8135-4a8f-bce6-e767d6c5aaea
title: Diritti di accesso agli oggetti account
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d69ba0939286564517c7293da136e88aa0367a60
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104529647"
---
# <a name="account-object-access-rights"></a><span data-ttu-id="fa9d7-103">Diritti di accesso agli oggetti account</span><span class="sxs-lookup"><span data-stu-id="fa9d7-103">Account Object Access Rights</span></span>

<span data-ttu-id="fa9d7-104">Il tipo di diritti di accesso agli oggetti account ha i seguenti tipi di accesso.</span><span class="sxs-lookup"><span data-stu-id="fa9d7-104">The Account Object Access Rights type has the following access types.</span></span>



| <span data-ttu-id="fa9d7-105">Tipo di accesso</span><span class="sxs-lookup"><span data-stu-id="fa9d7-105">Access type</span></span>                     | <span data-ttu-id="fa9d7-106">Descrizione</span><span class="sxs-lookup"><span data-stu-id="fa9d7-106">Description</span></span>                                                                                                                                                                                                                                           |
|---------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fa9d7-107">\_visualizzazione account</span><span class="sxs-lookup"><span data-stu-id="fa9d7-107">ACCOUNT\_VIEW</span></span>                   | <span data-ttu-id="fa9d7-108">Questo tipo di accesso è necessario per leggere le informazioni sull'account.</span><span class="sxs-lookup"><span data-stu-id="fa9d7-108">This access type is required to read the account information.</span></span> <span data-ttu-id="fa9d7-109">Sono inclusi i [*privilegi*](/windows/desktop/SecGloss/p-gly) assegnati all'account, le quote di memoria assegnate e tutti i tipi di accesso speciali concessi.</span><span class="sxs-lookup"><span data-stu-id="fa9d7-109">This includes the [*privileges*](/windows/desktop/SecGloss/p-gly) assigned to the account, memory quotas assigned, and any special access types granted.</span></span> |
| <span data-ttu-id="fa9d7-110">privilegi per la modifica dell'ACCOUNT \_ \_</span><span class="sxs-lookup"><span data-stu-id="fa9d7-110">ACCOUNT\_ADJUST\_PRIVILEGES</span></span>     | <span data-ttu-id="fa9d7-111">Questo tipo di accesso è necessario per assegnare o rimuovere privilegi da un account.</span><span class="sxs-lookup"><span data-stu-id="fa9d7-111">This access type is required to assign privileges to or remove privileges from an account.</span></span>                                                                                                                                                            |
| <span data-ttu-id="fa9d7-112">\_quote di regolazione dell'account \_</span><span class="sxs-lookup"><span data-stu-id="fa9d7-112">ACCOUNT\_ADJUST\_QUOTAS</span></span>         | <span data-ttu-id="fa9d7-113">Questo tipo di accesso è necessario per modificare le quote di sistema assegnate a un account.</span><span class="sxs-lookup"><span data-stu-id="fa9d7-113">This access type is required to change the system quotas assigned to an account.</span></span>                                                                                                                                                                      |
| <span data-ttu-id="fa9d7-114">ACCOUNT \_ per \_ regolare \_ l'accesso al sistema</span><span class="sxs-lookup"><span data-stu-id="fa9d7-114">ACCOUNT\_ADJUST\_SYSTEM\_ACCESS</span></span> | <span data-ttu-id="fa9d7-115">Questo tipo di accesso è necessario per aggiornare i flag di accesso al sistema per l'account.</span><span class="sxs-lookup"><span data-stu-id="fa9d7-115">This access type is required to update the system access flags for the account.</span></span>                                                                                                                                                                       |



 

## <a name="generic-access-masks"></a><span data-ttu-id="fa9d7-116">Maschere di accesso generico</span><span class="sxs-lookup"><span data-stu-id="fa9d7-116">Generic Access Masks</span></span>

<span data-ttu-id="fa9d7-117">L'oggetto [**account**](account-object.md) pubblica i mapping seguenti dai tipi di accesso generici ai tipi di accesso specifici.</span><span class="sxs-lookup"><span data-stu-id="fa9d7-117">The [**Account**](account-object.md) object publishes the following mappings from generic access types to specific access types.</span></span>

``` syntax
    GENERIC_READ        STANDARD_RIGHTS_READ |
                        ACCOUNT_VIEW 
            
    GENERIC_WRITE       STANDARD_RIGHTS_WRITE |
                        ACCOUNT_ADJUST_PRIVILEGES |
                        ACCOUNT_ADJUST_QUOTAS |
                        ACCOUNT_ADJUST_SYSTEM_ACCESS

    GENERIC_EXECUTE        STANDARD_RIGHTS_EXECUTE
```

## <a name="standard-access-types"></a><span data-ttu-id="fa9d7-118">Tipi di accesso standard</span><span class="sxs-lookup"><span data-stu-id="fa9d7-118">Standard Access Types</span></span>

<span data-ttu-id="fa9d7-119">Questo oggetto non supporta il tipo di accesso standard (facoltativo) SYNCHRONIZE.</span><span class="sxs-lookup"><span data-stu-id="fa9d7-119">This object does not support the (optional) SYNCHRONIZE standard access type.</span></span> <span data-ttu-id="fa9d7-120">Sono supportati tutti i tipi di accesso necessari.</span><span class="sxs-lookup"><span data-stu-id="fa9d7-120">All required access types are supported.</span></span> <span data-ttu-id="fa9d7-121">Di seguito è riportata la maschera di tutti i tipi di accesso supportati per questo tipo di oggetto.</span><span class="sxs-lookup"><span data-stu-id="fa9d7-121">The mask of all supported access types for this object type is as follows.</span></span>

``` syntax
    ACCOUNT_ALL_ACCESS  STANDARD_RIGHTS_REQUIRED |
                        ACCOUNT_VIEW |
                        ACCOUNT_ADJUST_PRIVILEGES |    
                        ACCOUNT_ADJUST_QUOTAS |
                        ACCOUNT_ADJUST_SYSTEM_ACCESS
```

 

 
