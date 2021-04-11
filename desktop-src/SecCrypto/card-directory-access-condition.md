---
description: Specifica le autorizzazioni di controllo di accesso per una directory in una smart card.
ms.assetid: 361d9fa0-286e-4d2c-8452-3b5f48e77779
title: Enumerazione CARD_DIRECTORY_ACCESS_CONDITION (cardmod. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CARD_DIRECTORY_ACCESS_CONDITION
api_type:
- HeaderDef
api_location:
- Cardmod.h
ms.openlocfilehash: 9879fa73f6bb45b56f433d7bca7765ab5fc0daef
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104226022"
---
# <a name="card_directory_access_condition-enumeration"></a><span data-ttu-id="0ac43-103">\_Enumerazione della \_ condizione di accesso alla directory della scheda \_</span><span class="sxs-lookup"><span data-stu-id="0ac43-103">CARD\_DIRECTORY\_ACCESS\_CONDITION enumeration</span></span>

<span data-ttu-id="0ac43-104">L'enumerazione della condizione di accesso alla directory delle schede specifica le autorizzazioni di controllo di accesso per una directory in una [*Smart Card*](../secgloss/s-gly.md). **\_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="0ac43-104">The **CARD\_DIRECTORY\_ACCESS\_CONDITION** enumeration specifies access control permissions for a directory on a [*smart card*](../secgloss/s-gly.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="0ac43-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="0ac43-105">Syntax</span></span>


```C++
typedef enum  { 
  InvalidAc               = 0,
  UserCreateDeleteDirAc   = 1,
  AdminCreateDeleteDirAc  = 2
} CARD_DIRECTORY_ACCESS_CONDITION;
```



## <a name="constants"></a><span data-ttu-id="0ac43-106">Costanti</span><span class="sxs-lookup"><span data-stu-id="0ac43-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="0ac43-107"><span id="InvalidAc"></span><span id="invalidac"></span><span id="INVALIDAC"></span>**InvalidAc**</span><span class="sxs-lookup"><span data-stu-id="0ac43-107"><span id="InvalidAc"></span><span id="invalidac"></span><span id="INVALIDAC"></span>**InvalidAc**</span></span>
</dt> <dd>

<span data-ttu-id="0ac43-108">Questo valore non è valido.</span><span class="sxs-lookup"><span data-stu-id="0ac43-108">This value is not valid.</span></span>

</dd> <dt>

<span data-ttu-id="0ac43-109"><span id="UserCreateDeleteDirAc"></span><span id="usercreatedeletedirac"></span><span id="USERCREATEDELETEDIRAC"></span>**UserCreateDeleteDirAc**</span><span class="sxs-lookup"><span data-stu-id="0ac43-109"><span id="UserCreateDeleteDirAc"></span><span id="usercreatedeletedirac"></span><span id="USERCREATEDELETEDIRAC"></span>**UserCreateDeleteDirAc**</span></span>
</dt> <dd>

<span data-ttu-id="0ac43-110">Utenti specifici possono leggere, scrivere ed eliminare la directory.</span><span class="sxs-lookup"><span data-stu-id="0ac43-110">Specific users can read, write, and delete the directory.</span></span>

</dd> <dt>

<span data-ttu-id="0ac43-111"><span id="AdminCreateDeleteDirAc"></span><span id="admincreatedeletedirac"></span><span id="ADMINCREATEDELETEDIRAC"></span>**AdminCreateDeleteDirAc**</span><span class="sxs-lookup"><span data-stu-id="0ac43-111"><span id="AdminCreateDeleteDirAc"></span><span id="admincreatedeletedirac"></span><span id="ADMINCREATEDELETEDIRAC"></span>**AdminCreateDeleteDirAc**</span></span>
</dt> <dd>

<span data-ttu-id="0ac43-112">Gli amministratori possono leggere, scrivere ed eliminare la directory.</span><span class="sxs-lookup"><span data-stu-id="0ac43-112">Administrators can read, write, and delete the directory.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="0ac43-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="0ac43-113">Requirements</span></span>



| <span data-ttu-id="0ac43-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="0ac43-114">Requirement</span></span> | <span data-ttu-id="0ac43-115">Valore</span><span class="sxs-lookup"><span data-stu-id="0ac43-115">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="0ac43-116">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0ac43-116">Minimum supported client</span></span><br/> | <span data-ttu-id="0ac43-117">Windows XP, \[ solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="0ac43-117">Windows XP, Windows XP \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="0ac43-118">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0ac43-118">Minimum supported server</span></span><br/> | <span data-ttu-id="0ac43-119">Solo app desktop Windows Server 2003, Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="0ac43-119">Windows Server 2003, Windows Server 2003 \[desktop apps only\]</span></span><br/>            |
| <span data-ttu-id="0ac43-120">Intestazione</span><span class="sxs-lookup"><span data-stu-id="0ac43-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="0ac43-121"><dt>Cardmod. h</dt></span><span class="sxs-lookup"><span data-stu-id="0ac43-121"><dt>Cardmod.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0ac43-122">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="0ac43-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0ac43-123">Provider del servizio di crittografia Smart Card di Microsoft base</span><span class="sxs-lookup"><span data-stu-id="0ac43-123">Microsoft Base Smart Card Cryptographic Service Provider</span></span>](/previous-versions/windows/desktop/secsmart/microsoft-base-smart-card-cryptographic-service-provider)
</dt> <dt>

[<span data-ttu-id="0ac43-124">**CardCreateDirectory**</span><span class="sxs-lookup"><span data-stu-id="0ac43-124">**CardCreateDirectory**</span></span>](/previous-versions/windows/desktop/secsmart/cardcreatedirectory)
</dt> <dt>

[<span data-ttu-id="0ac43-125">**CardDeleteDirectory**</span><span class="sxs-lookup"><span data-stu-id="0ac43-125">**CardDeleteDirectory**</span></span>](/previous-versions/windows/desktop/secsmart/carddeletedirectory)
</dt> </dl>

 

 
