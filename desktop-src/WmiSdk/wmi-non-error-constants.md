---
description: Codici restituiti WMI che indicano lo stato e non indicano un errore.
ms.assetid: 36faa3fb-9496-47ca-bdba-f8eb52a06ff7
ms.tgt_platform: multiple
title: Costanti non di errore WMI (WbemCli. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0880c9fda00f03c1fa8b174242bfc84ed9d75ad8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104226939"
---
# <a name="wmi-non-error-constants"></a><span data-ttu-id="a43a4-103">Costanti non di errore WMI</span><span class="sxs-lookup"><span data-stu-id="a43a4-103">WMI Non-Error Constants</span></span>

<span data-ttu-id="a43a4-104">Codici restituiti WMI che indicano lo stato e non indicano un errore.</span><span class="sxs-lookup"><span data-stu-id="a43a4-104">WMI return codes that indicate status and do not indicate an error.</span></span>

<span data-ttu-id="a43a4-105">Se un'operazione non genera un errore, WMI restituisce uno dei seguenti codici come **HRESULT** che indica lo stato dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="a43a4-105">If an operation does not result in an error, WMI returns one of the following codes as an **HRESULT** that indicates the status of the operation.</span></span>

> [!Note]  
> <span data-ttu-id="a43a4-106">Alcuni metodi delle classi WMI possono restituire codici di errore di sistema e di rete (ad esempio, 64).</span><span class="sxs-lookup"><span data-stu-id="a43a4-106">Some methods in WMI classes can return system and network error codes (64 for example).</span></span> <span data-ttu-id="a43a4-107">È possibile controllare la definizione di questi tipi di codici di errore usando il comando **net helpmsg** nella finestra del prompt dei comandi.</span><span class="sxs-lookup"><span data-stu-id="a43a4-107">You can check the definition of these types of error codes by using the **net helpmsg** command in the command prompt window.</span></span> <span data-ttu-id="a43a4-108">Ad esempio, il comando **net helpmsg 64** restituisce il messaggio: il nome di rete specificato non è più disponibile.</span><span class="sxs-lookup"><span data-stu-id="a43a4-108">For example, the command **net helpmsg 64** returns the message: The specified network name is no longer available.</span></span>

 

<span data-ttu-id="a43a4-109">In C++ è possibile chiamare [**FormatMessage**](/windows/desktop/api/winbase/nf-winbase-formatmessage) e specificare **C: \\ Windows \\ system32 \\ WBEM \\wmiutils.dll** come modulo Message.</span><span class="sxs-lookup"><span data-stu-id="a43a4-109">In C++, you can call [**FormatMessage**](/windows/desktop/api/winbase/nf-winbase-formatmessage) and specify **C:\\Windows\\System32\\wbem\\wmiutils.dll** as the message module.</span></span>

<dl> <dt>

<span data-ttu-id="a43a4-110"><span id="WBEM_S_NO_ERROR"></span><span id="wbem_s_no_error"></span>**\_non è \_ disponibile alcun \_ errore in WBEM**</span><span class="sxs-lookup"><span data-stu-id="a43a4-110"><span id="WBEM_S_NO_ERROR"></span><span id="wbem_s_no_error"></span>**WBEM\_S\_NO\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a43a4-111">0 (0x0)</span><span class="sxs-lookup"><span data-stu-id="a43a4-111">0 (0x0)</span></span>
</dt> <dt>



<span data-ttu-id="a43a4-112">L'operazione è stata completata.</span><span class="sxs-lookup"><span data-stu-id="a43a4-112">The operation was successful.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a43a4-113"><span id="WBEM_S_FALSE"></span><span id="wbem_s_false"></span>**WBEM \_ S \_ false**</span><span class="sxs-lookup"><span data-stu-id="a43a4-113"><span id="WBEM_S_FALSE"></span><span id="wbem_s_false"></span>**WBEM\_S\_FALSE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a43a4-114">1 (0x1)</span><span class="sxs-lookup"><span data-stu-id="a43a4-114">1 (0x1)</span></span>
</dt> <dt>



<span data-ttu-id="a43a4-115">Non sono disponibili altri oggetti, il numero di oggetti restituiti è inferiore al numero richiesto oppure è la fine di un'enumerazione.</span><span class="sxs-lookup"><span data-stu-id="a43a4-115">No more objects are available, the number of objects returned is less than the number requested, or this is the end of an enumeration.</span></span> <span data-ttu-id="a43a4-116">Questo valore viene restituito anche quando questo metodo viene chiamato con un valore pari a 0 per il parametro *uCount* .</span><span class="sxs-lookup"><span data-stu-id="a43a4-116">This value is also returned when this method is called with a value of 0 for the *uCount* parameter.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a43a4-117"><span id="WBEM_S_ALREADY_EXISTS"></span><span id="wbem_s_already_exists"></span>**WBEM \_ S \_ \_ esiste già**</span><span class="sxs-lookup"><span data-stu-id="a43a4-117"><span id="WBEM_S_ALREADY_EXISTS"></span><span id="wbem_s_already_exists"></span>**WBEM\_S\_ALREADY\_EXISTS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a43a4-118">262145 (0x40001)</span><span class="sxs-lookup"><span data-stu-id="a43a4-118">262145 (0x40001)</span></span>
</dt> <dt>



<span data-ttu-id="a43a4-119">È stato effettuato un tentativo di creare un oggetto o una classe già esistente.</span><span class="sxs-lookup"><span data-stu-id="a43a4-119">An attempt was made to create an object or class that already exists.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a43a4-120"><span id="WBEM_S_RESET_TO_DEFAULT"></span><span id="wbem_s_reset_to_default"></span>**il \_ ripristino di WBEM S è \_ \_ \_ predefinito**</span><span class="sxs-lookup"><span data-stu-id="a43a4-120"><span id="WBEM_S_RESET_TO_DEFAULT"></span><span id="wbem_s_reset_to_default"></span>**WBEM\_S\_RESET\_TO\_DEFAULT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a43a4-121">262146 (0x40002)</span><span class="sxs-lookup"><span data-stu-id="a43a4-121">262146 (0x40002)</span></span>
</dt> <dt>



<span data-ttu-id="a43a4-122">Una proprietà sottoposta a override è stata eliminata.</span><span class="sxs-lookup"><span data-stu-id="a43a4-122">An overridden property was deleted.</span></span> <span data-ttu-id="a43a4-123">Questo valore viene restituito per segnalare che il valore originale non sottoposto a override è stato ripristinato in seguito all'eliminazione.</span><span class="sxs-lookup"><span data-stu-id="a43a4-123">This value is returned to signal that the original non-overridden value has been restored as a result of the deletion.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a43a4-124"><span id="WBEM_S_DIFFERENT"></span><span id="wbem_s_different"></span>**WBEM \_ S \_ diverso**</span><span class="sxs-lookup"><span data-stu-id="a43a4-124"><span id="WBEM_S_DIFFERENT"></span><span id="wbem_s_different"></span>**WBEM\_S\_DIFFERENT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a43a4-125">262147 (0x40003)</span><span class="sxs-lookup"><span data-stu-id="a43a4-125">262147 (0x40003)</span></span>
</dt> <dt>



<span data-ttu-id="a43a4-126">Gli elementi (oggetti, classi e così via) che vengono confrontati non sono identici.</span><span class="sxs-lookup"><span data-stu-id="a43a4-126">The items (objects, classes, and so on) that are being compared are not identical.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a43a4-127"><span id="WBEM_S_TIMEDOUT"></span><span id="wbem_s_timedout"></span>**timeout di WBEM \_ S \_**</span><span class="sxs-lookup"><span data-stu-id="a43a4-127"><span id="WBEM_S_TIMEDOUT"></span><span id="wbem_s_timedout"></span>**WBEM\_S\_TIMEDOUT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a43a4-128">262148 (0x40004)</span><span class="sxs-lookup"><span data-stu-id="a43a4-128">262148 (0x40004)</span></span>
</dt> <dt>



<span data-ttu-id="a43a4-129">Si è verificato il timeout di una chiamata. Non si tratta di una condizione di errore.</span><span class="sxs-lookup"><span data-stu-id="a43a4-129">A call timed out. This is not an error condition.</span></span> <span data-ttu-id="a43a4-130">È pertanto possibile che vengano restituiti anche alcuni risultati.</span><span class="sxs-lookup"><span data-stu-id="a43a4-130">Therefore, some results may have also been returned.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a43a4-131"><span id="WBEM_S_NO_MORE_DATA"></span><span id="wbem_s_no_more_data"></span>**\_ \_ non sono disponibili \_ altri \_ dati per WBEM**</span><span class="sxs-lookup"><span data-stu-id="a43a4-131"><span id="WBEM_S_NO_MORE_DATA"></span><span id="wbem_s_no_more_data"></span>**WBEM\_S\_NO\_MORE\_DATA**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a43a4-132">262149 (0x40005)</span><span class="sxs-lookup"><span data-stu-id="a43a4-132">262149 (0x40005)</span></span>
</dt> <dt>



<span data-ttu-id="a43a4-133">Non sono disponibili altri dati dall'enumerazione e l'utente deve terminare l'enumerazione.</span><span class="sxs-lookup"><span data-stu-id="a43a4-133">No more data is available from the enumeration, and the user must terminate the enumeration.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a43a4-134"><span id="WBEM_S_OPERATION_CANCELLED"></span><span id="wbem_s_operation_cancelled"></span>**\_operazione WBEM \_ \_ annullata**</span><span class="sxs-lookup"><span data-stu-id="a43a4-134"><span id="WBEM_S_OPERATION_CANCELLED"></span><span id="wbem_s_operation_cancelled"></span>**WBEM\_S\_OPERATION\_CANCELLED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a43a4-135">262150 (0x40006)</span><span class="sxs-lookup"><span data-stu-id="a43a4-135">262150 (0x40006)</span></span>
</dt> <dt>



<span data-ttu-id="a43a4-136">L'operazione è stata annullata intenzionalmente o involontariamente.</span><span class="sxs-lookup"><span data-stu-id="a43a4-136">The operation was intentionally or unintentionally canceled.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a43a4-137"><span id="WBEM_S_PENDING"></span><span id="wbem_s_pending"></span>**WBEM \_ S \_ in sospeso**</span><span class="sxs-lookup"><span data-stu-id="a43a4-137"><span id="WBEM_S_PENDING"></span><span id="wbem_s_pending"></span>**WBEM\_S\_PENDING**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a43a4-138">262151 (0x40007)</span><span class="sxs-lookup"><span data-stu-id="a43a4-138">262151 (0x40007)</span></span>
</dt> <dt>



<span data-ttu-id="a43a4-139">Una richiesta è ancora in corso e i risultati non sono ancora disponibili.</span><span class="sxs-lookup"><span data-stu-id="a43a4-139">A request is still in progress, and the results are not yet available.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a43a4-140"><span id="WBEM_S_DUPLICATE_OBJECTS"></span><span id="wbem_s_duplicate_objects"></span>**\_ \_ oggetti duplicati WBEM S \_**</span><span class="sxs-lookup"><span data-stu-id="a43a4-140"><span id="WBEM_S_DUPLICATE_OBJECTS"></span><span id="wbem_s_duplicate_objects"></span>**WBEM\_S\_DUPLICATE\_OBJECTS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a43a4-141">262152 (0x40008)</span><span class="sxs-lookup"><span data-stu-id="a43a4-141">262152 (0x40008)</span></span>
</dt> <dt>



<span data-ttu-id="a43a4-142">Sono state individuate più copie dello stesso oggetto nel gruppo di risultati di un'enumerazione.</span><span class="sxs-lookup"><span data-stu-id="a43a4-142">More than one copy of the same object was detected in the result set of an enumeration.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a43a4-143"><span id="WBEM_S_ACCESS_DENIED"></span><span id="wbem_s_access_denied"></span>**accesso a WBEM \_ S \_ \_ negato**</span><span class="sxs-lookup"><span data-stu-id="a43a4-143"><span id="WBEM_S_ACCESS_DENIED"></span><span id="wbem_s_access_denied"></span>**WBEM\_S\_ACCESS\_DENIED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a43a4-144">262153 (0x40009)</span><span class="sxs-lookup"><span data-stu-id="a43a4-144">262153 (0x40009)</span></span>
</dt> <dt>



<span data-ttu-id="a43a4-145">All'utente è stato negato l'accesso ad alcune risorse, ma non a tutte.</span><span class="sxs-lookup"><span data-stu-id="a43a4-145">The user was denied access to some but not all resources.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a43a4-146"><span id="WBEM_S_PARTIAL_RESULTS"></span><span id="wbem_s_partial_results"></span>**\_ \_ risultati parziali di WBEM \_**</span><span class="sxs-lookup"><span data-stu-id="a43a4-146"><span id="WBEM_S_PARTIAL_RESULTS"></span><span id="wbem_s_partial_results"></span>**WBEM\_S\_PARTIAL\_RESULTS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a43a4-147">262160 (0x40010)</span><span class="sxs-lookup"><span data-stu-id="a43a4-147">262160 (0x40010)</span></span>
</dt> <dt>



<span data-ttu-id="a43a4-148">L'utente non ha ricevuto tutti gli oggetti richiesti a causa di risorse inaccessibili (ad eccezione delle violazioni della sicurezza).</span><span class="sxs-lookup"><span data-stu-id="a43a4-148">The user did not receive all of the objects requested due to inaccessible resources (other than security violations).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a43a4-149"><span id="WBEM_S_LIMITED_SERVICE"></span><span id="wbem_s_limited_service"></span>**servizio con limitazioni per WBEM \_ S \_ \_**</span><span class="sxs-lookup"><span data-stu-id="a43a4-149"><span id="WBEM_S_LIMITED_SERVICE"></span><span id="wbem_s_limited_service"></span>**WBEM\_S\_LIMITED\_SERVICE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a43a4-150">274433 (0x43001)</span><span class="sxs-lookup"><span data-stu-id="a43a4-150">274433 (0x43001)</span></span>
</dt> <dt>



<span data-ttu-id="a43a4-151">Il provider è in grado di limitare il servizio.</span><span class="sxs-lookup"><span data-stu-id="a43a4-151">The provider is capable of limited service.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a43a4-152"><span id="WBEM_S_INDIRECTLY_UPDATED"></span><span id="wbem_s_indirectly_updated"></span>**WBEM \_ è \_ stato \_ aggiornato indirettamente**</span><span class="sxs-lookup"><span data-stu-id="a43a4-152"><span id="WBEM_S_INDIRECTLY_UPDATED"></span><span id="wbem_s_indirectly_updated"></span>**WBEM\_S\_INDIRECTLY\_UPDATED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a43a4-153">274434 (0x43002)</span><span class="sxs-lookup"><span data-stu-id="a43a4-153">274434 (0x43002)</span></span>
</dt> <dt>



<span data-ttu-id="a43a4-154">Riservato per utilizzi futuri.</span><span class="sxs-lookup"><span data-stu-id="a43a4-154">Reserved for future use.</span></span>


</dt> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="a43a4-155">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a43a4-155">Requirements</span></span>



| <span data-ttu-id="a43a4-156">Requisito</span><span class="sxs-lookup"><span data-stu-id="a43a4-156">Requirement</span></span> | <span data-ttu-id="a43a4-157">Valore</span><span class="sxs-lookup"><span data-stu-id="a43a4-157">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="a43a4-158">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a43a4-158">Minimum supported client</span></span><br/> | <span data-ttu-id="a43a4-159">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="a43a4-159">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="a43a4-160">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a43a4-160">Minimum supported server</span></span><br/> | <span data-ttu-id="a43a4-161">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="a43a4-161">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="a43a4-162">Intestazione</span><span class="sxs-lookup"><span data-stu-id="a43a4-162">Header</span></span><br/>                   | <dl> <span data-ttu-id="a43a4-163"><dt>WbemCli. h</dt></span><span class="sxs-lookup"><span data-stu-id="a43a4-163"><dt>WbemCli.h</dt></span></span> </dl>   |
| <span data-ttu-id="a43a4-164">IDL</span><span class="sxs-lookup"><span data-stu-id="a43a4-164">IDL</span></span><br/>                      | <dl> <span data-ttu-id="a43a4-165"><dt>WbemCli. idl</dt></span><span class="sxs-lookup"><span data-stu-id="a43a4-165"><dt>WbemCli.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a43a4-166">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a43a4-166">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a43a4-167">Codici restituiti WMI</span><span class="sxs-lookup"><span data-stu-id="a43a4-167">WMI Return Codes</span></span>](wmi-return-codes.md)
</dt> </dl>

 

