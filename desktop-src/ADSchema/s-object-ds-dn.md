---
title: Sintassi dell'oggetto (DS-DN)
description: Stringa che contiene un nome distinto (DN).
ms.assetid: 089104c4-ff82-49ea-a8db-a6dadc3a18bc
ms.tgt_platform: multiple
keywords:
- Oggetto (DS-DN) sintassi di AD schema
topic_type:
- apiref
api_name:
- Object(DS-DN)
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 45154985fa7fbfc4d95d563196357d43eac2ea72
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/14/2020
ms.locfileid: "104519350"
---
# <a name="objectds-dn-syntax"></a><span data-ttu-id="c2e4f-104">Sintassi dell'oggetto (DS-DN)</span><span class="sxs-lookup"><span data-stu-id="c2e4f-104">Object(DS-DN) syntax</span></span>

<span data-ttu-id="c2e4f-105">Stringa che contiene un nome distinto (DN).</span><span class="sxs-lookup"><span data-stu-id="c2e4f-105">String that contains a distinguished name (DN).</span></span> <span data-ttu-id="c2e4f-106">Per gli attributi con questa sintassi, Active Directory gestisce i valori di attributo come riferimenti all'oggetto identificato dal DN e aggiorna automaticamente il valore se l'oggetto viene spostato o rinominato.</span><span class="sxs-lookup"><span data-stu-id="c2e4f-106">For attributes with this syntax, Active Directory handles attribute values as references to the object identified by the DN and automatically updates the value if the object is moved or renamed.</span></span> <span data-ttu-id="c2e4f-107">Per le query che includono attributi della sintassi DN in un filtro, specificare nomi distinti completi.</span><span class="sxs-lookup"><span data-stu-id="c2e4f-107">For queries that include attributes of DN syntax in a filter, specify full distinguished names.</span></span> <span data-ttu-id="c2e4f-108">I caratteri jolly (ad esempio, CN = John \* ) non sono supportati.</span><span class="sxs-lookup"><span data-stu-id="c2e4f-108">Wildcards (for example, cn=John\*) are not supported.</span></span>



| <span data-ttu-id="c2e4f-109">Voce</span><span class="sxs-lookup"><span data-stu-id="c2e4f-109">Entry</span></span> | <span data-ttu-id="c2e4f-110">Valore</span><span class="sxs-lookup"><span data-stu-id="c2e4f-110">Value</span></span> |
|--------------|------------------------------------------------------------------------|
| <span data-ttu-id="c2e4f-111">Nome</span><span class="sxs-lookup"><span data-stu-id="c2e4f-111">Name</span></span>         | <span data-ttu-id="c2e4f-112">Object(DS-DN) </span><span class="sxs-lookup"><span data-stu-id="c2e4f-112">Object(DS-DN)</span></span>                                                          |
| <span data-ttu-id="c2e4f-113">ID sintassi</span><span class="sxs-lookup"><span data-stu-id="c2e4f-113">Syntax ID</span></span>    | <span data-ttu-id="c2e4f-114">2.5.5.1</span><span class="sxs-lookup"><span data-stu-id="c2e4f-114">2.5.5.1</span></span>                                                                |
| <span data-ttu-id="c2e4f-115">ID OM</span><span class="sxs-lookup"><span data-stu-id="c2e4f-115">OM ID</span></span>        | <span data-ttu-id="c2e4f-116">127</span><span class="sxs-lookup"><span data-stu-id="c2e4f-116">127</span></span>                                                                    |
| <span data-ttu-id="c2e4f-117">Tipo MAPI</span><span class="sxs-lookup"><span data-stu-id="c2e4f-117">MAPI Type</span></span>    | <span data-ttu-id="c2e4f-118">OBJECT</span><span class="sxs-lookup"><span data-stu-id="c2e4f-118">OBJECT</span></span>                                                                 |
| <span data-ttu-id="c2e4f-119">Tipo di annunci</span><span class="sxs-lookup"><span data-stu-id="c2e4f-119">ADS Type</span></span>     | <span data-ttu-id="c2e4f-120">\_stringa DN \_ ADSTYPE</span><span class="sxs-lookup"><span data-stu-id="c2e4f-120">ADSTYPE\_DN\_STRING</span></span>                                                    |
| <span data-ttu-id="c2e4f-121">Tipo Variant</span><span class="sxs-lookup"><span data-stu-id="c2e4f-121">Variant Type</span></span> | <span data-ttu-id="c2e4f-122">\_BSTR VT</span><span class="sxs-lookup"><span data-stu-id="c2e4f-122">VT\_BSTR</span></span>                                                               |
| <span data-ttu-id="c2e4f-123">Tipo SDS</span><span class="sxs-lookup"><span data-stu-id="c2e4f-123">SDS Type</span></span>     | [<span data-ttu-id="c2e4f-124">System.String</span><span class="sxs-lookup"><span data-stu-id="c2e4f-124">System.String</span></span>](/dotnet/api/system.string) |



## <a name="see-also"></a><span data-ttu-id="c2e4f-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="c2e4f-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c2e4f-126">System.String</span><span class="sxs-lookup"><span data-stu-id="c2e4f-126">System.String</span></span>](/dotnet/api/system.string)
</dt> </dl>

 

 
