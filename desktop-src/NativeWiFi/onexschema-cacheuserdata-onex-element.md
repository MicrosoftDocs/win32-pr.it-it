---
description: Specifica se le credenziali utente vengono memorizzate nella cache per le connessioni successive.
ms.assetid: 65ed03f1-f61e-46f8-a666-91b393618de3
title: Elemento cacheUserData (OneX)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- cacheUserData
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 8650bb2e5899e96f921d57460c8ba49ffab0ea66
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103967404"
---
# <a name="cacheuserdata-onex-element"></a><span data-ttu-id="25de6-103">Elemento cacheUserData (OneX)</span><span class="sxs-lookup"><span data-stu-id="25de6-103">cacheUserData (OneX) Element</span></span>

<span data-ttu-id="25de6-104">L'elemento cacheUserData (OneX) specifica se le credenziali utente vengono memorizzate nella cache per le connessioni successive.</span><span class="sxs-lookup"><span data-stu-id="25de6-104">The cacheUserData (OneX) element specifies whether the user credentials are cached for subsequent connections.</span></span> <span data-ttu-id="25de6-105">Quando cacheUserData è TRUE, le credenziali vengono memorizzate nella cache.</span><span class="sxs-lookup"><span data-stu-id="25de6-105">When cacheUserData is TRUE, the credentials are cached.</span></span> <span data-ttu-id="25de6-106">Quando cacheUserData è FALSE, le credenziali non vengono memorizzate nella cache e all'utente potrebbero essere richieste le credenziali per i successivi tentativi di connessione.</span><span class="sxs-lookup"><span data-stu-id="25de6-106">When cacheUserData is FALSE, the credentials are not cached and the user may be prompted for credentials on subsequent connection attempts.</span></span>

<span data-ttu-id="25de6-107">Questo elemento è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="25de6-107">This element is optional.</span></span> <span data-ttu-id="25de6-108">Quando cacheUserData non viene specificato in un profilo, le credenziali utente vengono memorizzate nella cache.</span><span class="sxs-lookup"><span data-stu-id="25de6-108">When cacheUserData is not specified in a profile, the user credentials are cached.</span></span>

<span data-ttu-id="25de6-109">**Windows XP con SP3 e l'API LAN wireless per Windows XP con SP2:** Questo elemento verrà ignorato se è presente in un profilo.</span><span class="sxs-lookup"><span data-stu-id="25de6-109">**Windows XP with SP3 and Wireless LAN API for Windows XP with SP2:** This element will be ignored if it is present in a profile.</span></span>

``` syntax
<xs:element name="cacheUserData"
    type="boolean"
 />
```

<span data-ttu-id="25de6-110">L'elemento **cacheUserData** è definito dall'elemento [**Onex**](onexschema-onex-element.md) .</span><span class="sxs-lookup"><span data-stu-id="25de6-110">The **cacheUserData** element is defined by the [**OneX**](onexschema-onex-element.md) element.</span></span>

## <a name="requirements"></a><span data-ttu-id="25de6-111">Requisiti</span><span class="sxs-lookup"><span data-stu-id="25de6-111">Requirements</span></span>



| <span data-ttu-id="25de6-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="25de6-112">Requirement</span></span> | <span data-ttu-id="25de6-113">Valore</span><span class="sxs-lookup"><span data-stu-id="25de6-113">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="25de6-114">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="25de6-114">Minimum supported client</span></span><br/> | <span data-ttu-id="25de6-115">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="25de6-115">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="25de6-116">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="25de6-116">Minimum supported server</span></span><br/> | <span data-ttu-id="25de6-117">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="25de6-117">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="25de6-118">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="25de6-118">See also</span></span>

<dl> <dt>

<span data-ttu-id="25de6-119">**Contesto di definizione dell'elemento nello schema**</span><span class="sxs-lookup"><span data-stu-id="25de6-119">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="25de6-120">**OneX**</span><span class="sxs-lookup"><span data-stu-id="25de6-120">**OneX**</span></span>](onexschema-onex-element.md)
</dt> <dt>

<span data-ttu-id="25de6-121">**Possibile elemento padre immediato nell'istanza dello schema**</span><span class="sxs-lookup"><span data-stu-id="25de6-121">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="25de6-122">**OneX**</span><span class="sxs-lookup"><span data-stu-id="25de6-122">**OneX**</span></span>](onexschema-onex-element.md)
</dt> </dl>

 

 




