---
title: Enumerazione WINBIO_POLICY_SOURCE ( \_ tipi WINBIO. h)
description: Elenca le possibili origini delle informazioni sui criteri per il rilevamento dello spoofing per i fattori biometrici.
ms.assetid: 3DC3BB0B-1FD7-473C-8E0B-B7E0A4A44E9E
keywords:
- WINBIO_POLICY_SOURCE enumerazione Windows Biometric Framework API
- Puntatore di enumerazione PWINBIO_POLICY_SOURCE Windows Biometric Framework API
topic_type:
- apiref
api_name:
- WINBIO_POLICY_SOURCE
api_location:
- winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 866d1d82d939f143c4385caa5d94c68ffe3758f9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104341263"
---
# <a name="winbio_policy_source-enumeration"></a><span data-ttu-id="bbca6-105">Enumerazione dell'origine dei \_ criteri WINBIO \_</span><span class="sxs-lookup"><span data-stu-id="bbca6-105">WINBIO\_POLICY\_SOURCE enumeration</span></span>

<span data-ttu-id="bbca6-106">Elenca le possibili origini delle informazioni sui criteri per il rilevamento dello spoofing per i fattori biometrici.</span><span class="sxs-lookup"><span data-stu-id="bbca6-106">Lists the possible sources of policy information for the detection of spoofing for biometric factors.</span></span>

## <a name="syntax"></a><span data-ttu-id="bbca6-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="bbca6-107">Syntax</span></span>


```C++
typedef enum _WINBIO_POLICY_SOURCE { 
  WINBIO_POLICY_UNKNOWN  = 0x00000000,
  WINBIO_POLICY_DEFAULT  = 0x00000001,
  WINBIO_POLICY_LOCAL    = 0x00000002,
  WINBIO_POLICY_ADMIN    = 0x00000003
} WINBIO_POLICY_SOURCE, *PWINBIO_POLICY_SOURCE;
```



## <a name="constants"></a><span data-ttu-id="bbca6-108">Costanti</span><span class="sxs-lookup"><span data-stu-id="bbca6-108">Constants</span></span>

<dl> <dt>

<span data-ttu-id="bbca6-109"><span id="WINBIO_POLICY_UNKNOWN"></span><span id="winbio_policy_unknown"></span>**\_criterio WINBIO \_ sconosciuto**</span><span class="sxs-lookup"><span data-stu-id="bbca6-109"><span id="WINBIO_POLICY_UNKNOWN"></span><span id="winbio_policy_unknown"></span>**WINBIO\_POLICY\_UNKNOWN**</span></span>
</dt> <dd>

<span data-ttu-id="bbca6-110">L'origine del criterio è sconosciuta.</span><span class="sxs-lookup"><span data-stu-id="bbca6-110">The source of the policy is unknown.</span></span>

</dd> <dt>

<span data-ttu-id="bbca6-111"><span id="WINBIO_POLICY_DEFAULT"></span><span id="winbio_policy_default"></span>**\_impostazione predefinita dei criteri di WINBIO \_**</span><span class="sxs-lookup"><span data-stu-id="bbca6-111"><span id="WINBIO_POLICY_DEFAULT"></span><span id="winbio_policy_default"></span>**WINBIO\_POLICY\_DEFAULT**</span></span>
</dt> <dd>

<span data-ttu-id="bbca6-112">Il criterio è il criterio predefinito fornito dal Windows Biometric Framework.</span><span class="sxs-lookup"><span data-stu-id="bbca6-112">The policy is the default policy that the Windows Biometric Framework provides.</span></span>

</dd> <dt>

<span data-ttu-id="bbca6-113"><span id="WINBIO_POLICY_LOCAL"></span><span id="winbio_policy_local"></span>**\_criteri WINBIO \_ locale**</span><span class="sxs-lookup"><span data-stu-id="bbca6-113"><span id="WINBIO_POLICY_LOCAL"></span><span id="winbio_policy_local"></span>**WINBIO\_POLICY\_LOCAL**</span></span>
</dt> <dd>

<span data-ttu-id="bbca6-114">Criteri impostati dall'utente singolo per il proprio account tramite l'app **Impostazioni** .</span><span class="sxs-lookup"><span data-stu-id="bbca6-114">The policy that the individual user set for their account by using the **Settings** app.</span></span> <span data-ttu-id="bbca6-115">Questo criterio sostituisce i criteri predefiniti.</span><span class="sxs-lookup"><span data-stu-id="bbca6-115">This policy overrides the default policy.</span></span>

</dd> <dt>

<span data-ttu-id="bbca6-116"><span id="WINBIO_POLICY_ADMIN"></span><span id="winbio_policy_admin"></span>**\_amministrazione dei criteri di WINBIO \_**</span><span class="sxs-lookup"><span data-stu-id="bbca6-116"><span id="WINBIO_POLICY_ADMIN"></span><span id="winbio_policy_admin"></span>**WINBIO\_POLICY\_ADMIN**</span></span>
</dt> <dd>

<span data-ttu-id="bbca6-117">Criteri di gruppo impostati dall'amministratore IT per l'organizzazione.</span><span class="sxs-lookup"><span data-stu-id="bbca6-117">A group policy that the IT administrator set for the enterprise.</span></span> <span data-ttu-id="bbca6-118">I singoli utenti non possono eseguire l'override di questo criterio.</span><span class="sxs-lookup"><span data-stu-id="bbca6-118">Individual users cannot override this policy.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="bbca6-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="bbca6-119">Requirements</span></span>



| <span data-ttu-id="bbca6-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="bbca6-120">Requirement</span></span> | <span data-ttu-id="bbca6-121">Valore</span><span class="sxs-lookup"><span data-stu-id="bbca6-121">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bbca6-122">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="bbca6-122">Minimum supported client</span></span><br/> | <span data-ttu-id="bbca6-123">\[Solo app desktop Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="bbca6-123">Windows 10 \[desktop apps only\]</span></span><br/>                                                                                                                              |
| <span data-ttu-id="bbca6-124">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="bbca6-124">Minimum supported server</span></span><br/> | <span data-ttu-id="bbca6-125">\[Solo app desktop Windows Server 2016\]</span><span class="sxs-lookup"><span data-stu-id="bbca6-125">Windows Server 2016 \[desktop apps only\]</span></span><br/>                                                                                                                     |
| <span data-ttu-id="bbca6-126">Intestazione</span><span class="sxs-lookup"><span data-stu-id="bbca6-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="bbca6-127"><dt>WinBio \_ types. h (includere WinBio. h per le applicazioni client o WinBio \_ Adapters. h per gli adapter)</dt></span><span class="sxs-lookup"><span data-stu-id="bbca6-127"><dt>Winbio\_types.h (include Winbio.h for client applications or Winbio\_adapters.h for adapters)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bbca6-128">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="bbca6-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bbca6-129">**\_ \_ \_ Azione criterio anti-spoofing WINBIO \_**</span><span class="sxs-lookup"><span data-stu-id="bbca6-129">**WINBIO\_ANTI\_SPOOF\_POLICY\_ACTION**</span></span>](winbio-anti-spoof-policy-action.md)
</dt> </dl>

 

 





