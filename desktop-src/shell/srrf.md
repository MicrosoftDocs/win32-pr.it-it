---
description: Flag che limitano l'impostazione o la restituzione dei dati.
title: SRRF (Shlwapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: c9dbffd1-3b3e-4a25-89ee-1666e2812a62
api_name:
- SRRF_RT_REG_NONE
- SRRF_RT_REG_SZ
- SRRF_RT_REG_EXPAND_SZ
- SRRF_RT_REG_BINARY
- SRRF_RT_REG_DWORD
- SRRF_RT_REG_MULTI_SZ
- SRRF_RT_REG_QWORD
- SRRF_RT_DWORD
- SRRF_RT_QWORD
- SRRF_RT_ANY
- SRRF_RM_ANY
- SRRF_RM_NORMAL
- SRRF_RM_SAFE
- SRRF_RM_SAFENETWORK
- SRRF_NOEXPAND
- SRRF_ZEROONFAILURE
- SRRF_NOVIRT
api_type:
- HeaderDef
api_location:
- Shlwapi.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 3ba36b64496413a54e6d8b8b96c16c265367d05c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104050172"
---
# <a name="srrf"></a><span data-ttu-id="70e85-103">SRRF</span><span class="sxs-lookup"><span data-stu-id="70e85-103">SRRF</span></span>

<span data-ttu-id="70e85-104">Flag che limitano l'impostazione o la restituzione dei dati.</span><span class="sxs-lookup"><span data-stu-id="70e85-104">Flags that restrict the data to be set or returned.</span></span>



| <span data-ttu-id="70e85-105">Costante/valore</span><span class="sxs-lookup"><span data-stu-id="70e85-105">Constant/value</span></span>                                                                                                                                                                                                                                           | <span data-ttu-id="70e85-106">Descrizione</span><span class="sxs-lookup"><span data-stu-id="70e85-106">Description</span></span>                                                                                                                                                                                                            |
|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="SRRF_RT_REG_NONE"></span><span id="srrf_rt_reg_none"></span><dl> <span data-ttu-id="70e85-107"><dt>**SRRF \_ RT \_ reg \_ None**</dt> <dt>0x00000001</dt></span><span class="sxs-lookup"><span data-stu-id="70e85-107"><dt>**SRRF\_RT\_REG\_NONE**</dt> <dt>0x00000001</dt></span></span> </dl>                 | <span data-ttu-id="70e85-108">Digitare REG \_ None.</span><span class="sxs-lookup"><span data-stu-id="70e85-108">Type REG\_NONE.</span></span><br/>                                                                                                                                                                                             |
| <span id="SRRF_RT_REG_SZ"></span><span id="srrf_rt_reg_sz"></span><dl> <span data-ttu-id="70e85-109"><dt>**SRRF \_ RT \_ reg \_ SZ**</dt> <dt>0x00000002</dt></span><span class="sxs-lookup"><span data-stu-id="70e85-109"><dt>**SRRF\_RT\_REG\_SZ**</dt> <dt>0x00000002</dt></span></span> </dl>                       | <span data-ttu-id="70e85-110">Digitare REG \_ SZ.</span><span class="sxs-lookup"><span data-stu-id="70e85-110">Type REG\_SZ.</span></span> <span data-ttu-id="70e85-111">\_ \_ I tipi reg Expand SZ vengono convertiti automaticamente in reg \_ SZ a meno che non \_ sia specificato il flag SRRF NOEXPAND.</span><span class="sxs-lookup"><span data-stu-id="70e85-111">REG\_EXPAND\_SZ types are automatically converted to REG\_SZ unless the SRRF\_NOEXPAND flag is specified.</span></span><br/>                                                                                     |
| <span id="SRRF_RT_REG_EXPAND_SZ"></span><span id="srrf_rt_reg_expand_sz"></span><dl> <span data-ttu-id="70e85-112"><dt>**SRRF \_ RT \_ reg \_ expand \_ SZ**</dt> <dt>0x00000004</dt></span><span class="sxs-lookup"><span data-stu-id="70e85-112"><dt>**SRRF\_RT\_REG\_EXPAND\_SZ**</dt> <dt>0x00000004</dt></span></span> </dl> | <span data-ttu-id="70e85-113">Digitare REG \_ expand \_ SZ.</span><span class="sxs-lookup"><span data-stu-id="70e85-113">Type REG\_EXPAND\_SZ.</span></span> <span data-ttu-id="70e85-114">Se si recupera un valore, è necessario ottenere anche il \_ flag SRRF NOEXPAND oppure [**SHRegGetValue**](/windows/desktop/api/Shlwapi/nf-shlwapi-shreggetvaluea) ha esito negativo con un \_ parametro error non valido \_ .</span><span class="sxs-lookup"><span data-stu-id="70e85-114">If retrieving a value, you must also get the SRRF\_NOEXPAND flag, or [**SHRegGetValue**](/windows/desktop/api/Shlwapi/nf-shlwapi-shreggetvaluea) fails with ERROR\_INVALID\_PARAMETER.</span></span><br/>                                     |
| <span id="SRRF_RT_REG_BINARY"></span><span id="srrf_rt_reg_binary"></span><dl> <span data-ttu-id="70e85-115"><dt>**SRRF \_ RT \_ reg \_ binario**</dt> <dt>0x00000008</dt></span><span class="sxs-lookup"><span data-stu-id="70e85-115"><dt>**SRRF\_RT\_REG\_BINARY**</dt> <dt>0x00000008</dt></span></span> </dl>           | <span data-ttu-id="70e85-116">Digitare REG \_ Binary.</span><span class="sxs-lookup"><span data-stu-id="70e85-116">Type REG\_BINARY.</span></span><br/>                                                                                                                                                                                           |
| <span id="SRRF_RT_REG_DWORD"></span><span id="srrf_rt_reg_dword"></span><dl> <span data-ttu-id="70e85-117"><dt>**SRRF \_ RT \_ reg \_ DWORD**</dt> <dt>0x00000010</dt></span><span class="sxs-lookup"><span data-stu-id="70e85-117"><dt>**SRRF\_RT\_REG\_DWORD**</dt> <dt>0x00000010</dt></span></span> </dl>              | <span data-ttu-id="70e85-118">Digitare REG \_ DWORD.</span><span class="sxs-lookup"><span data-stu-id="70e85-118">Type REG\_DWORD.</span></span><br/>                                                                                                                                                                                            |
| <span id="SRRF_RT_REG_MULTI_SZ"></span><span id="srrf_rt_reg_multi_sz"></span><dl> <span data-ttu-id="70e85-119"><dt>**SRRF \_ RT \_ reg \_ \_ multisz**</dt> <dt>0x00000020</dt></span><span class="sxs-lookup"><span data-stu-id="70e85-119"><dt>**SRRF\_RT\_REG\_MULTI\_SZ**</dt> <dt>0x00000020</dt></span></span> </dl>    | <span data-ttu-id="70e85-120">Digitare REG \_ \_ multisz.</span><span class="sxs-lookup"><span data-stu-id="70e85-120">Type REG\_MULTI\_SZ.</span></span><br/>                                                                                                                                                                                        |
| <span id="SRRF_RT_REG_QWORD"></span><span id="srrf_rt_reg_qword"></span><dl> <span data-ttu-id="70e85-121"><dt>**SRRF \_ RT \_ reg \_ QWORD**</dt> <dt>0x00000040</dt></span><span class="sxs-lookup"><span data-stu-id="70e85-121"><dt>**SRRF\_RT\_REG\_QWORD**</dt> <dt>0x00000040</dt></span></span> </dl>              | <span data-ttu-id="70e85-122">Digitare REG \_ QWORD.</span><span class="sxs-lookup"><span data-stu-id="70e85-122">Type REG\_QWORD.</span></span><br/>                                                                                                                                                                                            |
| <span id="SRRF_RT_DWORD"></span><span id="srrf_rt_dword"></span><dl> <span data-ttu-id="70e85-123"><dt>**SRRF \_ RT \_ DWORD**</dt> <dt>0x00000018</dt></span><span class="sxs-lookup"><span data-stu-id="70e85-123"><dt>**SRRF\_RT\_DWORD**</dt> <dt>0x00000018</dt></span></span> </dl>                           | <span data-ttu-id="70e85-124">REG \_ DWORD e i tipi binari reg a 32 bit \_ .</span><span class="sxs-lookup"><span data-stu-id="70e85-124">REG\_DWORD and 32-bit REG\_BINARY types.</span></span> <span data-ttu-id="70e85-125">Equivale a SRRF \_ RT \_ reg \_ Binary \| SRRF \_ RT \_ reg reg \_ DWORD.</span><span class="sxs-lookup"><span data-stu-id="70e85-125">This is equivalent to SRRF\_RT\_REG\_BINARY \| SRRF\_RT\_REG\_DWORD.</span></span> <span data-ttu-id="70e85-126">Se si recupera un valore, se i dati binari del valore sono maggiori di 32 bit, non vengono restituiti.</span><span class="sxs-lookup"><span data-stu-id="70e85-126">If retrieving a value, if the value's binary data is larger than 32 bits, it is not returned.</span></span><br/> |
| <span id="SRRF_RT_QWORD"></span><span id="srrf_rt_qword"></span><dl> <span data-ttu-id="70e85-127"><dt>**SRRF \_ RT \_ QWORD**</dt> <dt>0x00000048</dt></span><span class="sxs-lookup"><span data-stu-id="70e85-127"><dt>**SRRF\_RT\_QWORD**</dt> <dt>0x00000048</dt></span></span> </dl>                           | <span data-ttu-id="70e85-128">REG \_ QWORD e i tipi binari reg a 64 bit \_ .</span><span class="sxs-lookup"><span data-stu-id="70e85-128">REG\_QWORD and 64-bit REG\_BINARY types.</span></span> <span data-ttu-id="70e85-129">Equivale a SRRF \_ RT \_ reg \_ Binary \| SRRF \_ RT \_ reg \_ QWORD.</span><span class="sxs-lookup"><span data-stu-id="70e85-129">This is equivalent to SRRF\_RT\_REG\_BINARY \| SRRF\_RT\_REG\_QWORD.</span></span> <span data-ttu-id="70e85-130">Se si recupera un valore, se i dati binari del valore sono maggiori di 64 bit, non vengono restituiti.</span><span class="sxs-lookup"><span data-stu-id="70e85-130">If retrieving a value, if the value's binary data is larger than 64 bits, it is not returned.</span></span><br/> |
| <span id="SRRF_RT_ANY"></span><span id="srrf_rt_any"></span><dl> <span data-ttu-id="70e85-131"><dt>**SRRF \_ RT \_ qualsiasi**</dt> <dt>0x0000FFFF</dt></span><span class="sxs-lookup"><span data-stu-id="70e85-131"><dt>**SRRF\_RT\_ANY**</dt> <dt>0x0000FFFF</dt></span></span> </dl>                                 | <span data-ttu-id="70e85-132">Tutti i tipi.</span><span class="sxs-lookup"><span data-stu-id="70e85-132">All types.</span></span> <span data-ttu-id="70e85-133">Impostare questo flag se non \_ è impostato alcun altro valore RT SRRF.</span><span class="sxs-lookup"><span data-stu-id="70e85-133">Set this flag if no other SRRF\_RT value is set.</span></span><br/>                                                                                                                                                 |
| <span id="SRRF_RM_ANY"></span><span id="srrf_rm_any"></span><dl> <span data-ttu-id="70e85-134"><dt>**SRRF \_ RM \_ any**</dt> <dt>0x00000000</dt></span><span class="sxs-lookup"><span data-stu-id="70e85-134"><dt>**SRRF\_RM\_ANY**</dt> <dt>0x00000000</dt></span></span> </dl>                                 | <span data-ttu-id="70e85-135">Nessuna restrizione in modalità.</span><span class="sxs-lookup"><span data-stu-id="70e85-135">No mode restriction.</span></span> <span data-ttu-id="70e85-136">Si tratta del valore predefinito.</span><span class="sxs-lookup"><span data-stu-id="70e85-136">This is the default value.</span></span><br/>                                                                                                                                                             |
| <span id="SRRF_RM_NORMAL"></span><span id="srrf_rm_normal"></span><dl> <span data-ttu-id="70e85-137"><dt>**SRRF \_ 0x00010000 \_ normale RM**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="70e85-137"><dt>**SRRF\_RM\_NORMAL**</dt> <dt>0x00010000</dt></span></span> </dl>                        | <span data-ttu-id="70e85-138">Limitare la modalità di avvio del sistema a "avvio normale".</span><span class="sxs-lookup"><span data-stu-id="70e85-138">Restrict system startup mode to "normal boot".</span></span><br/>                                                                                                                                                              |
| <span id="SRRF_RM_SAFE"></span><span id="srrf_rm_safe"></span><dl> <span data-ttu-id="70e85-139"><dt>**SRRF \_ 0x00020000 \_ Safe RM**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="70e85-139"><dt>**SRRF\_RM\_SAFE**</dt> <dt>0x00020000</dt></span></span> </dl>                              | <span data-ttu-id="70e85-140">Limitare la modalità di avvio del sistema alla "modalità provvisoria".</span><span class="sxs-lookup"><span data-stu-id="70e85-140">Restrict system startup mode to "safe mode".</span></span><br/>                                                                                                                                                                |
| <span id="SRRF_RM_SAFENETWORK"></span><span id="srrf_rm_safenetwork"></span><dl> <span data-ttu-id="70e85-141"><dt>**SRRF \_ 0x00040000 \_ SAFENETWORK RM**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="70e85-141"><dt>**SRRF\_RM\_SAFENETWORK**</dt> <dt>0x00040000</dt></span></span> </dl>         | <span data-ttu-id="70e85-142">Limitare la modalità di avvio del sistema alla "modalità provvisoria con rete".</span><span class="sxs-lookup"><span data-stu-id="70e85-142">Restrict system startup mode to "safe mode with networking".</span></span><br/>                                                                                                                                                |
| <span id="SRRF_NOEXPAND"></span><span id="srrf_noexpand"></span><dl> <span data-ttu-id="70e85-143"><dt>**SRRF \_ NOEXPAND**</dt> <dt>0x10000000</dt></span><span class="sxs-lookup"><span data-stu-id="70e85-143"><dt>**SRRF\_NOEXPAND**</dt> <dt>0x10000000</dt></span></span> </dl>                            | <span data-ttu-id="70e85-144">Non espandere automaticamente le \_ stringhe di ambiente reg Expand \_ SZ.</span><span class="sxs-lookup"><span data-stu-id="70e85-144">Do not automatically expand REG\_EXPAND\_SZ environment strings.</span></span><br/>                                                                                                                                            |
| <span id="SRRF_ZEROONFAILURE"></span><span id="srrf_zeroonfailure"></span><dl> <span data-ttu-id="70e85-145"><dt>**SRRF \_**</dt> <dt>0x20000000</dt> ZEROONFAILURE</span><span class="sxs-lookup"><span data-stu-id="70e85-145"><dt>**SRRF\_ZEROONFAILURE**</dt> <dt>0x20000000</dt></span></span> </dl>             | <span data-ttu-id="70e85-146">Se si recupera un valore, se *pvData* non è **null**, impostare il contenuto del buffer *pvData* su tutti gli zeri in caso di errore.</span><span class="sxs-lookup"><span data-stu-id="70e85-146">If retrieving a value, if *pvData* is not **NULL**, set the contents of the *pvData* buffer to all zeros on failure.</span></span><br/>                                                                                        |
| <span id="SRRF_NOVIRT"></span><span id="srrf_novirt"></span><dl> <span data-ttu-id="70e85-147"><dt>**SRRF \_**</dt> <dt>0x40000000</dt> NOVIRT</span><span class="sxs-lookup"><span data-stu-id="70e85-147"><dt>**SRRF\_NOVIRT**</dt> <dt>0x40000000</dt></span></span> </dl>                                  | <span data-ttu-id="70e85-148">Quando si recupera un valore, se la chiave richiesta è virtualizzata, non riesce e il file di errore non è stato \_ \_ \_ trovato.</span><span class="sxs-lookup"><span data-stu-id="70e85-148">When retrieving a value, if the requested key is virtualized, fail with ERROR\_FILE\_NOT\_FOUND.</span></span><br/>                                                                                                            |



## <a name="remarks"></a><span data-ttu-id="70e85-149">Commenti</span><span class="sxs-lookup"><span data-stu-id="70e85-149">Remarks</span></span>

<span data-ttu-id="70e85-150">Questi valori sono definiti in Shlwapi. h.</span><span class="sxs-lookup"><span data-stu-id="70e85-150">These values are defined in Shlwapi.h.</span></span>

## <a name="requirements"></a><span data-ttu-id="70e85-151">Requisiti</span><span class="sxs-lookup"><span data-stu-id="70e85-151">Requirements</span></span>



| <span data-ttu-id="70e85-152">Requisito</span><span class="sxs-lookup"><span data-stu-id="70e85-152">Requirement</span></span> | <span data-ttu-id="70e85-153">Valore</span><span class="sxs-lookup"><span data-stu-id="70e85-153">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="70e85-154">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="70e85-154">Minimum supported client</span></span><br/> | <span data-ttu-id="70e85-155">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="70e85-155">Windows Vista \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="70e85-156">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="70e85-156">Minimum supported server</span></span><br/> | <span data-ttu-id="70e85-157">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="70e85-157">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="70e85-158">Intestazione</span><span class="sxs-lookup"><span data-stu-id="70e85-158">Header</span></span><br/>                   | <dl> <span data-ttu-id="70e85-159"><dt>Shlwapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="70e85-159"><dt>Shlwapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="70e85-160">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="70e85-160">See also</span></span>

<dl> <dt>

[<span data-ttu-id="70e85-161">**SHRegSetValue**</span><span class="sxs-lookup"><span data-stu-id="70e85-161">**SHRegSetValue**</span></span>](/windows/desktop/api/shlwapi/nf-shlwapi-shregsetvalue)
</dt> <dt>

[<span data-ttu-id="70e85-162">**SHRegGetValue**</span><span class="sxs-lookup"><span data-stu-id="70e85-162">**SHRegGetValue**</span></span>](/windows/desktop/api/Shlwapi/nf-shlwapi-shreggetvaluea)
</dt> </dl>

 

 




