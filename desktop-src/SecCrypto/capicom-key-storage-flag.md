---
description: L' \_ enumerazione del flag di archiviazione della chiave CAPICOM definisce i flag di archiviazione delle \_ \_ chiavi.
ms.assetid: 326cef75-24a5-4dc9-a7e9-a63dd3d8de54
title: Enumerazione CAPICOM_KEY_STORAGE_FLAG (CAPICOM. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAPICOM_KEY_STORAGE_FLAG
api_type:
- HeaderDef
api_location:
- Capicom.h
ms.openlocfilehash: 9edbc3a5ac3396e528ebbb5390c4b07c24770e58
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327641"
---
# <a name="capicom_key_storage_flag-enumeration"></a><span data-ttu-id="b73e3-103">\_ \_ Enumerazione flag di archiviazione chiavi \_ CAPICOM</span><span class="sxs-lookup"><span data-stu-id="b73e3-103">CAPICOM\_KEY\_STORAGE\_FLAG enumeration</span></span>

<span data-ttu-id="b73e3-104">L'enumerazione del **\_ flag di \_ archiviazione \_ della chiave CAPICOM** definisce i flag di archiviazione delle chiavi.</span><span class="sxs-lookup"><span data-stu-id="b73e3-104">The **CAPICOM\_KEY\_STORAGE\_FLAG** enumeration defines key storage flags.</span></span>

## <a name="members"></a><span data-ttu-id="b73e3-105">Membri</span><span class="sxs-lookup"><span data-stu-id="b73e3-105">Members</span></span>



| <span data-ttu-id="b73e3-106">Membro</span><span class="sxs-lookup"><span data-stu-id="b73e3-106">Member</span></span>                                     | <span data-ttu-id="b73e3-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b73e3-107">Description</span></span>                           | <span data-ttu-id="b73e3-108">Valore</span><span class="sxs-lookup"><span data-stu-id="b73e3-108">Value</span></span> |
|--------------------------------------------|---------------------------------------|-------|
| <span data-ttu-id="b73e3-109">**archiviazione delle chiavi di CAPICOM \_ \_ \_ predefinite**</span><span class="sxs-lookup"><span data-stu-id="b73e3-109">**CAPICOM\_KEY\_STORAGE\_DEFAULT**</span></span>         | <span data-ttu-id="b73e3-110">Archiviazione chiavi predefinita.</span><span class="sxs-lookup"><span data-stu-id="b73e3-110">Default key storage.</span></span><br/>       | <span data-ttu-id="b73e3-111">0</span><span class="sxs-lookup"><span data-stu-id="b73e3-111">0</span></span>     |
| <span data-ttu-id="b73e3-112">**\_archiviazione chiavi CAPICOM \_ \_ esportabile**</span><span class="sxs-lookup"><span data-stu-id="b73e3-112">**CAPICOM\_KEY\_STORAGE\_EXPORTABLE**</span></span>      | <span data-ttu-id="b73e3-113">La chiave è esportabile.</span><span class="sxs-lookup"><span data-stu-id="b73e3-113">The key is exportable.</span></span><br/>     | <span data-ttu-id="b73e3-114">1</span><span class="sxs-lookup"><span data-stu-id="b73e3-114">1</span></span>     |
| <span data-ttu-id="b73e3-115">**archiviazione delle chiavi di CAPICOM \_ \_ \_ protetta dall'utente \_**</span><span class="sxs-lookup"><span data-stu-id="b73e3-115">**CAPICOM\_KEY\_STORAGE\_USER\_PROTECTED**</span></span> | <span data-ttu-id="b73e3-116">La chiave è protetta dall'utente.</span><span class="sxs-lookup"><span data-stu-id="b73e3-116">The key is user protected.</span></span><br/> | <span data-ttu-id="b73e3-117">2</span><span class="sxs-lookup"><span data-stu-id="b73e3-117">2</span></span>     |



## <a name="remarks"></a><span data-ttu-id="b73e3-118">Commenti</span><span class="sxs-lookup"><span data-stu-id="b73e3-118">Remarks</span></span>

<span data-ttu-id="b73e3-119">Questa enumerazione viene utilizzata dal metodo seguente:</span><span class="sxs-lookup"><span data-stu-id="b73e3-119">This enumeration is used by the following method:</span></span>

-   [<span data-ttu-id="b73e3-120">**Certificate. Load**</span><span class="sxs-lookup"><span data-stu-id="b73e3-120">**Certificate.Load**</span></span>](certificate-load.md)
-   [<span data-ttu-id="b73e3-121">**Store. Load**</span><span class="sxs-lookup"><span data-stu-id="b73e3-121">**Store.Load**</span></span>](store-load.md)

## <a name="requirements"></a><span data-ttu-id="b73e3-122">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b73e3-122">Requirements</span></span>



| <span data-ttu-id="b73e3-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="b73e3-123">Requirement</span></span> | <span data-ttu-id="b73e3-124">Valore</span><span class="sxs-lookup"><span data-stu-id="b73e3-124">Value</span></span> |
|----------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="b73e3-125">Componente ridistribuibile</span><span class="sxs-lookup"><span data-stu-id="b73e3-125">Redistributable</span></span><br/> | <span data-ttu-id="b73e3-126">CAPICOM 2,0 o versioni successive in Windows Server 2003 e Windows XP</span><span class="sxs-lookup"><span data-stu-id="b73e3-126">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                |
| <span data-ttu-id="b73e3-127">Intestazione</span><span class="sxs-lookup"><span data-stu-id="b73e3-127">Header</span></span><br/>          | <dl> <span data-ttu-id="b73e3-128"><dt>CAPICOM. h</dt></span><span class="sxs-lookup"><span data-stu-id="b73e3-128"><dt>Capicom.h</dt></span></span> </dl> |



 

 




