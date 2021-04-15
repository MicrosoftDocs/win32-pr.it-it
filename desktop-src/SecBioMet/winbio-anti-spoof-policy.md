---
title: Struttura WINBIO_ANTI_SPOOF_POLICY ( \_ tipi WINBIO. h)
description: Rappresenta i criteri di antispoofing per un utente.
ms.assetid: 2B433AE8-21A0-4AF1-853C-9074527DB2E4
keywords:
- Struttura di WINBIO_ANTI_SPOOF_POLICY Windows Biometric Framework API
- API Windows Biometric Framework puntatore alla struttura PWINBIO_ANTI_SPOOF_POLICY
topic_type:
- apiref
api_name:
- WINBIO_ANTI_SPOOF_POLICY
api_location:
- winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3da8b7811afb1de1ad464675125f125ef0ceab73
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104477500"
---
# <a name="winbio_anti_spoof_policy-structure"></a><span data-ttu-id="7533e-105">\_Struttura dei criteri anti- \_ spoofing WINBIO \_</span><span class="sxs-lookup"><span data-stu-id="7533e-105">WINBIO\_ANTI\_SPOOF\_POLICY structure</span></span>

<span data-ttu-id="7533e-106">Rappresenta i criteri di antispoofing per un utente.</span><span class="sxs-lookup"><span data-stu-id="7533e-106">Represents the antispoofing policy for a user.</span></span>

## <a name="syntax"></a><span data-ttu-id="7533e-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="7533e-107">Syntax</span></span>


```C++
typedef struct _WINBIO_ANTI_SPOOF_POLICY {
  WINBIO_ANTI_SPOOF_POLICY_ACTION Action;
  WINBIO_POLICY_SOURCE            Source;
} WINBIO_ANTI_SPOOF_POLICY, *PWINBIO_ANTI_SPOOF_POLICY;
```



## <a name="members"></a><span data-ttu-id="7533e-108">Members</span><span class="sxs-lookup"><span data-stu-id="7533e-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="7533e-109">**Azione**</span><span class="sxs-lookup"><span data-stu-id="7533e-109">**Action**</span></span>
</dt> <dd>

<span data-ttu-id="7533e-110">Tipo di azione da eseguire per i criteri di antispoofing.</span><span class="sxs-lookup"><span data-stu-id="7533e-110">The type of action to take for the antispoofing policy.</span></span>

</dd> <dt>

<span data-ttu-id="7533e-111">**Origine**</span><span class="sxs-lookup"><span data-stu-id="7533e-111">**Source**</span></span>
</dt> <dd>

<span data-ttu-id="7533e-112">Origine per i criteri di antispoofing.</span><span class="sxs-lookup"><span data-stu-id="7533e-112">The source for the antispoofing policy.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="7533e-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="7533e-113">Requirements</span></span>



| <span data-ttu-id="7533e-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="7533e-114">Requirement</span></span> | <span data-ttu-id="7533e-115">Valore</span><span class="sxs-lookup"><span data-stu-id="7533e-115">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7533e-116">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="7533e-116">Minimum supported client</span></span><br/> | <span data-ttu-id="7533e-117">\[Solo app desktop Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="7533e-117">Windows 10 \[desktop apps only\]</span></span><br/>                                                                                                                              |
| <span data-ttu-id="7533e-118">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="7533e-118">Minimum supported server</span></span><br/> | <span data-ttu-id="7533e-119">\[Solo app desktop Windows Server 2016\]</span><span class="sxs-lookup"><span data-stu-id="7533e-119">Windows Server 2016 \[desktop apps only\]</span></span><br/>                                                                                                                     |
| <span data-ttu-id="7533e-120">Intestazione</span><span class="sxs-lookup"><span data-stu-id="7533e-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="7533e-121"><dt>WinBio \_ types. h (includere WinBio. h per le applicazioni client o WinBio \_ Adapters. h per gli adapter)</dt></span><span class="sxs-lookup"><span data-stu-id="7533e-121"><dt>Winbio\_types.h (include Winbio.h for client applications or Winbio\_adapters.h for adapters)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7533e-122">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="7533e-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7533e-123">**\_ \_ \_ Azione criterio anti-spoofing WINBIO \_**</span><span class="sxs-lookup"><span data-stu-id="7533e-123">**WINBIO\_ANTI\_SPOOF\_POLICY\_ACTION**</span></span>](winbio-anti-spoof-policy-action.md)
</dt> <dt>

[<span data-ttu-id="7533e-124">**\_origine criteri \_ WINBIO**</span><span class="sxs-lookup"><span data-stu-id="7533e-124">**WINBIO\_POLICY\_SOURCE**</span></span>](winbio-policy-source.md)
</dt> <dt>

[<span data-ttu-id="7533e-125">**\_risultato asincrono \_ WINBIO**</span><span class="sxs-lookup"><span data-stu-id="7533e-125">**WINBIO\_ASYNC\_RESULT**</span></span>](/windows/desktop/api/Winbio/ns-winbio-winbio_async_result)
</dt> <dt>

[<span data-ttu-id="7533e-126">**WinBioGetProperty**</span><span class="sxs-lookup"><span data-stu-id="7533e-126">**WinBioGetProperty**</span></span>](/windows/desktop/api/Winbio/nf-winbio-winbiogetproperty)
</dt> <dt>

[<span data-ttu-id="7533e-127">**WinBioSetProperty**</span><span class="sxs-lookup"><span data-stu-id="7533e-127">**WinBioSetProperty**</span></span>](/windows/desktop/api/winbio/nf-winbio-winbiosetproperty)
</dt> </dl>

 

 





