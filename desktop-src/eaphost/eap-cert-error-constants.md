---
title: '\_Costanti di errore del certificato EAP (Eaphosterror. h)'
description: Definire gli errori correlati ai certificati comuni a tutte le tecnologie API EAPHost.
ms.assetid: 12f626e1-520a-4aba-954b-769c3062a38c
topic_type:
- apiref
api_name:
- _EAP_CERT_FIRST
- _EAP_CERT_LAST
- _EAP_CERT_NOT_FOUND
- _EAP_CERT_INVALID
- _EAP_CERT_EXPIRED
- _EAP_CERT_REVOKED
- _EAP_CERT_OTHER_ERROR
- _EAP_CERT_REJECTED
- _EAP_CERT_NAME_REQUIRED
- _EAP_GENERAL_FIRST
- _EAP_GENERAL_LAST
api_location:
- eaphosterror.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0543636f36d823b5557ad2f5a5f7cb000d93259a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104517517"
---
# <a name="eap_cert-error-constants"></a><span data-ttu-id="b1294-103">\_Costanti di errore del certificato EAP</span><span class="sxs-lookup"><span data-stu-id="b1294-103">EAP\_CERT Error Constants</span></span>

<span data-ttu-id="b1294-104">Queste costanti definiscono gli errori correlati ai certificati comuni a tutte le tecnologie API EAPHost.</span><span class="sxs-lookup"><span data-stu-id="b1294-104">These constants define certificate-related errors common to all EAPHost API technologies.</span></span>

<dl> <dt>

<span data-ttu-id="b1294-105"><span id="_EAP_CERT_FIRST"></span><span id="_eap_cert_first"></span>**\_\_certificato EAP \_ prima**</span><span class="sxs-lookup"><span data-stu-id="b1294-105"><span id="_EAP_CERT_FIRST"></span><span id="_eap_cert_first"></span>**\_EAP\_CERT\_FIRST**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b1294-106">0x0</span><span class="sxs-lookup"><span data-stu-id="b1294-106">0x0</span></span>
</dt> <dt>



<span data-ttu-id="b1294-107">Definisce il limite dei report di errore. si verificherà un errore di certificato tra i certificati **\_ EAP \_ \_ prima** e il certificato **\_ EAP per \_ \_ ultimo**.</span><span class="sxs-lookup"><span data-stu-id="b1294-107">Defines the boundary of error reports; any certificate error will occur between **\_EAP\_CERT\_FIRST** and **\_EAP\_CERT\_LAST**.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b1294-108"><span id="_EAP_CERT_LAST"></span><span id="_eap_cert_last"></span>**\_\_ultimo certificato \_ EAP**</span><span class="sxs-lookup"><span data-stu-id="b1294-108"><span id="_EAP_CERT_LAST"></span><span id="_eap_cert_last"></span>**\_EAP\_CERT\_LAST**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b1294-109">0xF</span><span class="sxs-lookup"><span data-stu-id="b1294-109">0xF</span></span>
</dt> <dt>



<span data-ttu-id="b1294-110">Definisce il limite dei report di errore. si verificherà un errore di certificato tra i certificati **\_ EAP \_ \_ prima** e il certificato **\_ EAP per \_ \_ ultimo**.</span><span class="sxs-lookup"><span data-stu-id="b1294-110">Defines the boundary of error reports; any certificate error will occur between **\_EAP\_CERT\_FIRST** and **\_EAP\_CERT\_LAST**.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b1294-111"><span id="_EAP_CERT_NOT_FOUND"></span><span id="_eap_cert_not_found"></span>**\_\_certificato EAP \_ non \_ trovato**</span><span class="sxs-lookup"><span data-stu-id="b1294-111"><span id="_EAP_CERT_NOT_FOUND"></span><span id="_eap_cert_not_found"></span>**\_EAP\_CERT\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b1294-112">0x1</span><span class="sxs-lookup"><span data-stu-id="b1294-112">0x1</span></span>
</dt> <dt>



<span data-ttu-id="b1294-113">Non è stato trovato alcun certificato utente.</span><span class="sxs-lookup"><span data-stu-id="b1294-113">No user certificate was found.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b1294-114"><span id="_EAP_CERT_INVALID"></span><span id="_eap_cert_invalid"></span>**\_\_certificato EAP \_ non valido**</span><span class="sxs-lookup"><span data-stu-id="b1294-114"><span id="_EAP_CERT_INVALID"></span><span id="_eap_cert_invalid"></span>**\_EAP\_CERT\_INVALID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b1294-115">0x2</span><span class="sxs-lookup"><span data-stu-id="b1294-115">0x2</span></span>
</dt> <dt>



<span data-ttu-id="b1294-116">Il certificato utente non è valido.</span><span class="sxs-lookup"><span data-stu-id="b1294-116">The user certificate is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b1294-117"><span id="_EAP_CERT_EXPIRED"></span><span id="_eap_cert_expired"></span>**\_\_certificato EAP \_ scaduto**</span><span class="sxs-lookup"><span data-stu-id="b1294-117"><span id="_EAP_CERT_EXPIRED"></span><span id="_eap_cert_expired"></span>**\_EAP\_CERT\_EXPIRED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b1294-118">0x3</span><span class="sxs-lookup"><span data-stu-id="b1294-118">0x3</span></span>
</dt> <dt>



<span data-ttu-id="b1294-119">Il certificato utente è scaduto.</span><span class="sxs-lookup"><span data-stu-id="b1294-119">The user certificate has expired.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b1294-120"><span id="_EAP_CERT_REVOKED"></span><span id="_eap_cert_revoked"></span>**\_\_certificato EAP \_ revocato**</span><span class="sxs-lookup"><span data-stu-id="b1294-120"><span id="_EAP_CERT_REVOKED"></span><span id="_eap_cert_revoked"></span>**\_EAP\_CERT\_REVOKED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b1294-121">0x4</span><span class="sxs-lookup"><span data-stu-id="b1294-121">0x4</span></span>
</dt> <dt>



<span data-ttu-id="b1294-122">Il certificato utente è stato revocato.</span><span class="sxs-lookup"><span data-stu-id="b1294-122">The user certificate was revoked.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b1294-123"><span id="_EAP_CERT_OTHER_ERROR"></span><span id="_eap_cert_other_error"></span>**\_\_ \_ altro errore del certificato EAP \_**</span><span class="sxs-lookup"><span data-stu-id="b1294-123"><span id="_EAP_CERT_OTHER_ERROR"></span><span id="_eap_cert_other_error"></span>**\_EAP\_CERT\_OTHER\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b1294-124">0x5</span><span class="sxs-lookup"><span data-stu-id="b1294-124">0x5</span></span>
</dt> <dt>



<span data-ttu-id="b1294-125">Errore sconosciuto relativo al certificato.</span><span class="sxs-lookup"><span data-stu-id="b1294-125">There is an unknown certificate related error.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b1294-126"><span id="_EAP_CERT_REJECTED"></span><span id="_eap_cert_rejected"></span>**\_\_certificato EAP \_ rifiutato**</span><span class="sxs-lookup"><span data-stu-id="b1294-126"><span id="_EAP_CERT_REJECTED"></span><span id="_eap_cert_rejected"></span>**\_EAP\_CERT\_REJECTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b1294-127">0x6</span><span class="sxs-lookup"><span data-stu-id="b1294-127">0x6</span></span>
</dt> <dt>



<span data-ttu-id="b1294-128">Il certificato utente è stato rifiutato.</span><span class="sxs-lookup"><span data-stu-id="b1294-128">The user certificate was rejected.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b1294-129"><span id="_EAP_CERT_NAME_REQUIRED"></span><span id="_eap_cert_name_required"></span>**\_il \_ nome del certificato EAP è \_ \_ obbligatorio**</span><span class="sxs-lookup"><span data-stu-id="b1294-129"><span id="_EAP_CERT_NAME_REQUIRED"></span><span id="_eap_cert_name_required"></span>**\_EAP\_CERT\_NAME\_REQUIRED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b1294-130">0x7</span><span class="sxs-lookup"><span data-stu-id="b1294-130">0x7</span></span>
</dt> <dt>



<span data-ttu-id="b1294-131">Il certificato utente richiede un nome.</span><span class="sxs-lookup"><span data-stu-id="b1294-131">The user certificate requires a name.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b1294-132"><span id="_EAP_GENERAL_FIRST"></span><span id="_eap_general_first"></span>**\_\_prima EAP generale \_**</span><span class="sxs-lookup"><span data-stu-id="b1294-132"><span id="_EAP_GENERAL_FIRST"></span><span id="_eap_general_first"></span>**\_EAP\_GENERAL\_FIRST**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b1294-133">0x10</span><span class="sxs-lookup"><span data-stu-id="b1294-133">0x10</span></span>
</dt> <dt>



<span data-ttu-id="b1294-134">Definisce il limite dei report di errore. qualsiasi errore EAP generale si verificherà tra il **\_ \_ \_ primo** e **\_ \_ \_ l'ultimo** generale EAP.</span><span class="sxs-lookup"><span data-stu-id="b1294-134">Defines the boundary of error reports; any general EAP error will occur between **\_EAP\_GENERAL\_FIRST** and **\_EAP\_GENERAL\_LAST**.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b1294-135"><span id="_EAP_GENERAL_LAST"></span><span id="_eap_general_last"></span>**\_\_ultimo generale \_ EAP**</span><span class="sxs-lookup"><span data-stu-id="b1294-135"><span id="_EAP_GENERAL_LAST"></span><span id="_eap_general_last"></span>**\_EAP\_GENERAL\_LAST**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b1294-136">0x3F</span><span class="sxs-lookup"><span data-stu-id="b1294-136">0x3F</span></span>
</dt> <dt>



<span data-ttu-id="b1294-137">Definisce il limite dei report di errore. qualsiasi errore EAP generale si verificherà tra il **\_ \_ \_ primo** e **\_ \_ \_ l'ultimo** generale EAP.</span><span class="sxs-lookup"><span data-stu-id="b1294-137">Defines the boundary of error reports; any general EAP error will occur between **\_EAP\_GENERAL\_FIRST** and **\_EAP\_GENERAL\_LAST**.</span></span>


</dt> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="b1294-138">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b1294-138">Requirements</span></span>



| <span data-ttu-id="b1294-139">Requisito</span><span class="sxs-lookup"><span data-stu-id="b1294-139">Requirement</span></span> | <span data-ttu-id="b1294-140">Valore</span><span class="sxs-lookup"><span data-stu-id="b1294-140">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="b1294-141">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b1294-141">Minimum supported client</span></span><br/> | <span data-ttu-id="b1294-142">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="b1294-142">Windows Vista \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="b1294-143">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b1294-143">Minimum supported server</span></span><br/> | <span data-ttu-id="b1294-144">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="b1294-144">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="b1294-145">Intestazione</span><span class="sxs-lookup"><span data-stu-id="b1294-145">Header</span></span><br/>                   | <dl> <span data-ttu-id="b1294-146"><dt>Eaphosterror. h</dt></span><span class="sxs-lookup"><span data-stu-id="b1294-146"><dt>Eaphosterror.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b1294-147">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="b1294-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b1294-148">Costanti EAPHost comuni</span><span class="sxs-lookup"><span data-stu-id="b1294-148">Common EAPHost Constants</span></span>](common-eap-host-error-constants.md)
</dt> </dl>

 

 





