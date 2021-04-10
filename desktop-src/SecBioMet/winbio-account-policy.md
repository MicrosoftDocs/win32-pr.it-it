---
title: Struttura WINBIO_ACCOUNT_POLICY (WinBio \_ Adapter. h)
description: Contiene criteri di antispoofing predefiniti o specifici dell'account.
ms.assetid: 7098FC53-E487-42B2-8B4B-EB7E2D296CB6
keywords:
- Struttura di WINBIO_ACCOUNT_POLICY Windows Biometric Framework API
- API Windows Biometric Framework puntatore alla struttura PWINBIO_ACCOUNT_POLICY
topic_type:
- apiref
api_name:
- WINBIO_ACCOUNT_POLICY
api_location:
- Winbio_adapter.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c734fa6d98615b7708a65ebad1dddc47cdc77cc2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964215"
---
# <a name="winbio_account_policy-structure"></a><span data-ttu-id="4f287-105">Struttura dei criteri dell' \_ account WINBIO \_</span><span class="sxs-lookup"><span data-stu-id="4f287-105">WINBIO\_ACCOUNT\_POLICY structure</span></span>

<span data-ttu-id="4f287-106">La struttura dei **\_ \_ criteri dell'account WINBIO** contiene un criterio di antispoofing predefinito o specifico per l'account.</span><span class="sxs-lookup"><span data-stu-id="4f287-106">The **WINBIO\_ACCOUNT\_POLICY** structure contains either a default or account-specific antispoofing policy.</span></span>

## <a name="syntax"></a><span data-ttu-id="4f287-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="4f287-107">Syntax</span></span>


```C++
typedef struct _WINBIO_ACCOUNT_POLICY {
  WINBIO_IDENTITY                 Identity;
  WINBIO_ANTI_SPOOF_POLICY_ACTION AntiSpoofBehavior;
} WINBIO_ACCOUNT_POLICY, *PWINBIO_ACCOUNT_POLICY;
```



## <a name="members"></a><span data-ttu-id="4f287-108">Members</span><span class="sxs-lookup"><span data-stu-id="4f287-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="4f287-109">**Identità**</span><span class="sxs-lookup"><span data-stu-id="4f287-109">**Identity**</span></span>
</dt> <dd>

<span data-ttu-id="4f287-110">Struttura [**di \_ identità WINBIO**](winbio-identity.md) che specifica le informazioni sull'account.</span><span class="sxs-lookup"><span data-stu-id="4f287-110">A [**WINBIO\_IDENTITY**](winbio-identity.md) structure that specifies the account information.</span></span>

</dd> <dt>

<span data-ttu-id="4f287-111">**AntiSpoofBehavior**</span><span class="sxs-lookup"><span data-stu-id="4f287-111">**AntiSpoofBehavior**</span></span>
</dt> <dd>

<span data-ttu-id="4f287-112">Uno dei valori di enumerazione dell' [**\_ \_ azione del \_ criterio \_ anti spoofing di WINBIO**](winbio-anti-spoof-policy-action.md) che specifica l'azione del criterio di antispoofing da usare per l'account.</span><span class="sxs-lookup"><span data-stu-id="4f287-112">One of the [**WINBIO\_ANTI\_SPOOF\_POLICY\_ACTION**](winbio-anti-spoof-policy-action.md) enumeration values that specifies what antispoofing policy action to use for the account.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="4f287-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="4f287-113">Remarks</span></span>

<span data-ttu-id="4f287-114">Per una descrizione della modalità di utilizzo di questa struttura, vedere la discussione sul metodo [**EngineAdapterSetAccountPolicy**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_set_account_policy_fn) .</span><span class="sxs-lookup"><span data-stu-id="4f287-114">See the discussion of the [**EngineAdapterSetAccountPolicy**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_set_account_policy_fn) method for a description of how this structure is used.</span></span>

## <a name="requirements"></a><span data-ttu-id="4f287-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="4f287-115">Requirements</span></span>



| <span data-ttu-id="4f287-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="4f287-116">Requirement</span></span> | <span data-ttu-id="4f287-117">Valore</span><span class="sxs-lookup"><span data-stu-id="4f287-117">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4f287-118">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4f287-118">Minimum supported client</span></span><br/> | <span data-ttu-id="4f287-119">\[Solo app desktop Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="4f287-119">Windows 10 \[desktop apps only\]</span></span><br/>                                                                              |
| <span data-ttu-id="4f287-120">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4f287-120">Minimum supported server</span></span><br/> | <span data-ttu-id="4f287-121">\[Solo app desktop Windows Server 2016\]</span><span class="sxs-lookup"><span data-stu-id="4f287-121">Windows Server 2016 \[desktop apps only\]</span></span><br/>                                                                     |
| <span data-ttu-id="4f287-122">Intestazione</span><span class="sxs-lookup"><span data-stu-id="4f287-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="4f287-123"><dt>WinBio \_ Adapter. h (include WinBio \_ Adapter. h)</dt></span><span class="sxs-lookup"><span data-stu-id="4f287-123"><dt>Winbio\_adapter.h (include Winbio\_adapter.h)</dt></span></span> </dl> |



 

 





