---
description: Specifica le autorizzazioni di controllo di accesso per un file in una smart card.
ms.assetid: 995d959f-30dc-4e5c-be2d-6b447499415a
title: Enumerazione CARD_FILE_ACCESS_CONDITION (cardmod. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CARD_FILE_ACCESS_CONDITION
api_type:
- HeaderDef
api_location:
- Cardmod.h
ms.openlocfilehash: d3ef9fc81c9ab3bff5f3992c3aedeb3f923648ea
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106306546"
---
# <a name="card_file_access_condition-enumeration"></a><span data-ttu-id="56338-103">\_Enumerazione della \_ condizione di accesso ai file delle schede \_</span><span class="sxs-lookup"><span data-stu-id="56338-103">CARD\_FILE\_ACCESS\_CONDITION enumeration</span></span>

<span data-ttu-id="56338-104">L'enumerazione della condizione di accesso ai file di scheda specifica le autorizzazioni di controllo di accesso per un file in una [*Smart Card*](../secgloss/s-gly.md). **\_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="56338-104">The **CARD\_FILE\_ACCESS\_CONDITION** enumeration specifies access control permissions for a file on a [*smart card*](../secgloss/s-gly.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="56338-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="56338-105">Syntax</span></span>


```C++
typedef enum  { 
  InvalidAc                 = 0,
  EveryoneReadUserWriteAc   = 1,
  UserWriteExecuteAc        = 2,
  EveryoneReadAdminWriteAc  = 3,
  UnknownAc                 = 4
} CARD_FILE_ACCESS_CONDITION;
```



## <a name="constants"></a><span data-ttu-id="56338-106">Costanti</span><span class="sxs-lookup"><span data-stu-id="56338-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="56338-107"><span id="InvalidAc"></span><span id="invalidac"></span><span id="INVALIDAC"></span>**InvalidAc**</span><span class="sxs-lookup"><span data-stu-id="56338-107"><span id="InvalidAc"></span><span id="invalidac"></span><span id="INVALIDAC"></span>**InvalidAc**</span></span>
</dt> <dd>

<span data-ttu-id="56338-108">Questo valore non è valido.</span><span class="sxs-lookup"><span data-stu-id="56338-108">This value is not valid.</span></span>

</dd> <dt>

<span data-ttu-id="56338-109"><span id="EveryoneReadUserWriteAc"></span><span id="everyonereaduserwriteac"></span><span id="EVERYONEREADUSERWRITEAC"></span>**EveryoneReadUserWriteAc**</span><span class="sxs-lookup"><span data-stu-id="56338-109"><span id="EveryoneReadUserWriteAc"></span><span id="everyonereaduserwriteac"></span><span id="EVERYONEREADUSERWRITEAC"></span>**EveryoneReadUserWriteAc**</span></span>
</dt> <dd>

<span data-ttu-id="56338-110">Tutti possono leggere il file.</span><span class="sxs-lookup"><span data-stu-id="56338-110">Everyone can read the file.</span></span> <span data-ttu-id="56338-111">Utenti specifici possono scrivere nel file.</span><span class="sxs-lookup"><span data-stu-id="56338-111">Specific users can write to the file.</span></span>

</dd> <dt>

<span data-ttu-id="56338-112"><span id="UserWriteExecuteAc"></span><span id="userwriteexecuteac"></span><span id="USERWRITEEXECUTEAC"></span>**UserWriteExecuteAc**</span><span class="sxs-lookup"><span data-stu-id="56338-112"><span id="UserWriteExecuteAc"></span><span id="userwriteexecuteac"></span><span id="USERWRITEEXECUTEAC"></span>**UserWriteExecuteAc**</span></span>
</dt> <dd>

<span data-ttu-id="56338-113">Solo utenti specifici possono leggere o scrivere nel file.</span><span class="sxs-lookup"><span data-stu-id="56338-113">Only specific users can read or write to the file.</span></span>

</dd> <dt>

<span data-ttu-id="56338-114"><span id="EveryoneReadAdminWriteAc"></span><span id="everyonereadadminwriteac"></span><span id="EVERYONEREADADMINWRITEAC"></span>**EveryoneReadAdminWriteAc**</span><span class="sxs-lookup"><span data-stu-id="56338-114"><span id="EveryoneReadAdminWriteAc"></span><span id="everyonereadadminwriteac"></span><span id="EVERYONEREADADMINWRITEAC"></span>**EveryoneReadAdminWriteAc**</span></span>
</dt> <dd>

<span data-ttu-id="56338-115">Tutti possono leggere il file.</span><span class="sxs-lookup"><span data-stu-id="56338-115">Everyone can read the file.</span></span> <span data-ttu-id="56338-116">Gli amministratori possono scrivere nel file.</span><span class="sxs-lookup"><span data-stu-id="56338-116">Administrators can write to the file.</span></span>

</dd> <dt>

<span data-ttu-id="56338-117"><span id="UnknownAc"></span><span id="unknownac"></span><span id="UNKNOWNAC"></span>**UnknownAc**</span><span class="sxs-lookup"><span data-stu-id="56338-117"><span id="UnknownAc"></span><span id="unknownac"></span><span id="UNKNOWNAC"></span>**UnknownAc**</span></span>
</dt> <dd>

<span data-ttu-id="56338-118">Le autorizzazioni di accesso per il file sono sconosciute.</span><span class="sxs-lookup"><span data-stu-id="56338-118">Access permissions for the file are unknown.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="56338-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="56338-119">Requirements</span></span>



| <span data-ttu-id="56338-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="56338-120">Requirement</span></span> | <span data-ttu-id="56338-121">Valore</span><span class="sxs-lookup"><span data-stu-id="56338-121">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="56338-122">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="56338-122">Minimum supported client</span></span><br/> | <span data-ttu-id="56338-123">Windows XP, \[ solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="56338-123">Windows XP, Windows XP \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="56338-124">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="56338-124">Minimum supported server</span></span><br/> | <span data-ttu-id="56338-125">Solo app desktop Windows Server 2003, Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="56338-125">Windows Server 2003, Windows Server 2003 \[desktop apps only\]</span></span><br/>            |
| <span data-ttu-id="56338-126">Intestazione</span><span class="sxs-lookup"><span data-stu-id="56338-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="56338-127"><dt>Cardmod. h</dt></span><span class="sxs-lookup"><span data-stu-id="56338-127"><dt>Cardmod.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="56338-128">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="56338-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="56338-129">Provider del servizio di crittografia Smart Card di Microsoft base</span><span class="sxs-lookup"><span data-stu-id="56338-129">Microsoft Base Smart Card Cryptographic Service Provider</span></span>](/previous-versions/windows/desktop/secsmart/microsoft-base-smart-card-cryptographic-service-provider)
</dt> <dt>

[<span data-ttu-id="56338-130">**\_informazioni sul file di scheda \_**</span><span class="sxs-lookup"><span data-stu-id="56338-130">**CARD\_FILE\_INFO**</span></span>](/previous-versions/windows/desktop/secsmart/card-file-info)
</dt> <dt>

[<span data-ttu-id="56338-131">**CardCreateFile**</span><span class="sxs-lookup"><span data-stu-id="56338-131">**CardCreateFile**</span></span>](/previous-versions/windows/desktop/secsmart/cardcreatefile)
</dt> </dl>

 

 
