---
description: Elenca e illustra i diritti di accesso dell'oggetto dati privato.
ms.assetid: 82be57d0-487c-4eb7-83d5-0dd2d53a452b
title: Diritti di accesso agli oggetti dati privati
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 142aecfe133a9c04237aacf58413e026c4cb3164
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104484580"
---
# <a name="private-data-object-access-rights"></a><span data-ttu-id="ca880-103">Diritti di accesso agli oggetti dati privati</span><span class="sxs-lookup"><span data-stu-id="ca880-103">Private Data Object Access Rights</span></span>

<span data-ttu-id="ca880-104">I tipi di accesso di questo tipo di oggetto sono:</span><span class="sxs-lookup"><span data-stu-id="ca880-104">The access types of this object type are:</span></span>



| <span data-ttu-id="ca880-105">Tipo di accesso</span><span class="sxs-lookup"><span data-stu-id="ca880-105">Access type</span></span>          | <span data-ttu-id="ca880-106">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ca880-106">Description</span></span>                                      |
|----------------------|--------------------------------------------------|
| <span data-ttu-id="ca880-107">\_valore query \_ Secret</span><span class="sxs-lookup"><span data-stu-id="ca880-107">SECRET\_QUERY\_VALUE</span></span> | <span data-ttu-id="ca880-108">Questo tipo di accesso è necessario per il recupero di un segreto.</span><span class="sxs-lookup"><span data-stu-id="ca880-108">This access type is needed to retrieve a secret.</span></span> |
| <span data-ttu-id="ca880-109">\_valore imposta \_ segreto</span><span class="sxs-lookup"><span data-stu-id="ca880-109">SECRET\_SET\_VALUE</span></span>   | <span data-ttu-id="ca880-110">Questo tipo di accesso è necessario per modificare un segreto.</span><span class="sxs-lookup"><span data-stu-id="ca880-110">This access type is needed to modify a secret.</span></span>   |



 

## <a name="generic-access-masks"></a><span data-ttu-id="ca880-111">Maschere di accesso generico</span><span class="sxs-lookup"><span data-stu-id="ca880-111">Generic Access Masks</span></span>

<span data-ttu-id="ca880-112">Questo tipo di oggetto ha i mapping di accesso generici seguenti:</span><span class="sxs-lookup"><span data-stu-id="ca880-112">This object type has the following generic access mappings:</span></span>

``` syntax
    GENERIC_READ    STANDARD_RIGHTS_READ |
                    SECRET_QUERY_VALUE

    GENERIC_WRITE   STANDARD_RIGHTS_WRITE |
                    SECRET_SET_VALUE

    GENERIC_EXECUTE STANDARD_RIGHTS_EXECUTE
```

## <a name="standard-access-types"></a><span data-ttu-id="ca880-113">Tipi di accesso standard:</span><span class="sxs-lookup"><span data-stu-id="ca880-113">Standard Access Types:</span></span>

<span data-ttu-id="ca880-114">Questo oggetto non supporta il tipo di accesso standard (facoltativo) SYNCHRONIZE.</span><span class="sxs-lookup"><span data-stu-id="ca880-114">This object does not support the (optional) SYNCHRONIZE standard access type.</span></span> <span data-ttu-id="ca880-115">Sono supportati tutti i tipi di accesso necessari.</span><span class="sxs-lookup"><span data-stu-id="ca880-115">All required access types are supported.</span></span> <span data-ttu-id="ca880-116">La maschera di tutti i tipi di accesso supportati per questo tipo di oggetto è:</span><span class="sxs-lookup"><span data-stu-id="ca880-116">The mask of all supported access types for this object type is:</span></span>

``` syntax
    SECRET_ALL_ACCESS    STANDARD_RIGHTS_REQUIRED |
                    SECRET_QUERY_VALUE |
                    SECRET_SET_VALUE
```

 

 



