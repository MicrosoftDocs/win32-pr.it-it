---
description: Il metodo ReadRecord costruisce un comando APDU (Application Protocol Data Unit) che legge il contenuto dei record specificati o la parte iniziale di un record di un file elementare.
ms.assetid: b00a3242-93bc-4779-8c62-89157fbcb5d1
title: 'Metodo ISCardISO7816:: ReadRecord (scardssp. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardISO7816.ReadRecord
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 0cb9697315a6f9dd2436cd7a64d54fa6b44e00f4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104049980"
---
# <a name="iscardiso7816readrecord-method"></a><span data-ttu-id="1403f-103">Metodo ISCardISO7816:: ReadRecord</span><span class="sxs-lookup"><span data-stu-id="1403f-103">ISCardISO7816::ReadRecord method</span></span>

<span data-ttu-id="1403f-104">\[Il metodo **ReadRecord** è disponibile per l'uso nei sistemi operativi specificati nella sezione requisiti.</span><span class="sxs-lookup"><span data-stu-id="1403f-104">\[The **ReadRecord** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="1403f-105">Non è disponibile per l'utilizzo in Windows Server 2003 con Service Pack 1 (SP1) e versioni successive, Windows Vista, Windows Server 2008 e versioni successive del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="1403f-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="1403f-106">I [moduli Smart Card](/previous-versions/windows/desktop/secsmart/smart-card-modules) offrono funzionalità simili.\]</span><span class="sxs-lookup"><span data-stu-id="1403f-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="1403f-107">Il metodo **ReadRecord** costruisce un comando APDU ( [*Application Protocol Data Unit*](../secgloss/a-gly.md) ) che legge il contenuto dei record specificati o la parte iniziale di un record di un file elementare.</span><span class="sxs-lookup"><span data-stu-id="1403f-107">The **ReadRecord** method constructs an [*application protocol data unit*](../secgloss/a-gly.md) (APDU) command that reads either the contents of the specified records or the beginning part of one record of an elementary file.</span></span>

## <a name="syntax"></a><span data-ttu-id="1403f-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="1403f-108">Syntax</span></span>


```C++
HRESULT ReadRecord(
  [in]      BYTE       byRecordId,
  [in]      BYTE       byRefCtrl,
  [in]      LONG       lBytesToRead,
  [in, out] LPSCARDCMD *ppCmd
);
```



## <a name="parameters"></a><span data-ttu-id="1403f-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="1403f-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1403f-110">*byRecordId* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="1403f-110">*byRecordId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1403f-111">Numero di record o ID del primo record da leggere (00 indica il record corrente).</span><span class="sxs-lookup"><span data-stu-id="1403f-111">Record number or ID of the first record to be read (00 indicates the current record).</span></span>

</dd> <dt>

<span data-ttu-id="1403f-112">*byRefCtrl* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="1403f-112">*byRefCtrl* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1403f-113">Codifica del controllo di riferimento.</span><span class="sxs-lookup"><span data-stu-id="1403f-113">Coding of the reference control.</span></span>



| <span data-ttu-id="1403f-114">Valore</span><span class="sxs-lookup"><span data-stu-id="1403f-114">Value</span></span>                                                                                                                                                                                | <span data-ttu-id="1403f-115">Significato</span><span class="sxs-lookup"><span data-stu-id="1403f-115">Meaning</span></span>                                                                                |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| <span id="Current_EF"></span><span id="current_ef"></span><span id="CURRENT_EF"></span><dl> <span data-ttu-id="1403f-116"><dt>**EF corrente**</dt></span><span class="sxs-lookup"><span data-stu-id="1403f-116"><dt>**Current EF**</dt></span></span> </dl>     | <span data-ttu-id="1403f-117">Posizione bit: 00000---</span><span class="sxs-lookup"><span data-stu-id="1403f-117">Bit position: 00000---</span></span><br/> <span data-ttu-id="1403f-118">Attualmente selezionato EF.</span><span class="sxs-lookup"><span data-stu-id="1403f-118">Currently selected EF.</span></span><br/>                    |
| <span id="Short_EF_ID"></span><span id="short_ef_id"></span><span id="SHORT_EF_ID"></span><dl> <span data-ttu-id="1403f-119"><dt>**ID EF breve**</dt></span><span class="sxs-lookup"><span data-stu-id="1403f-119"><dt>**Short EF ID**</dt></span></span> </dl> | <span data-ttu-id="1403f-120">Posizione bit: xxxxx---</span><span class="sxs-lookup"><span data-stu-id="1403f-120">Bit position: xxxxx---</span></span><br/> <span data-ttu-id="1403f-121">Identificatore EF breve.</span><span class="sxs-lookup"><span data-stu-id="1403f-121">Short EF identifier.</span></span><br/>                      |
| <span id="RFU"></span><span id="rfu"></span><dl> <span data-ttu-id="1403f-122"><dt>**RFU**</dt></span><span class="sxs-lookup"><span data-stu-id="1403f-122"><dt>**RFU**</dt></span></span> </dl>                                                       | <span data-ttu-id="1403f-123">Posizione bit: 11111---</span><span class="sxs-lookup"><span data-stu-id="1403f-123">Bit position: 11111---</span></span><br/>                                                      |
| <span id="Record__"></span><span id="record__"></span><span id="RECORD__"></span><dl> <span data-ttu-id="1403f-124"><dt>**Record \#**</dt></span><span class="sxs-lookup"><span data-stu-id="1403f-124"><dt>**Record \#**</dt></span></span> </dl>            | <span data-ttu-id="1403f-125">Posizione bit:-----1xx</span><span class="sxs-lookup"><span data-stu-id="1403f-125">Bit position: -----1xx</span></span><br/> <span data-ttu-id="1403f-126">Utilizzo del numero di record in P1.</span><span class="sxs-lookup"><span data-stu-id="1403f-126">Usage of record number in P1.</span></span><br/>             |
| <span id="Read_Record"></span><span id="read_record"></span><span id="READ_RECORD"></span><dl> <span data-ttu-id="1403f-127"><dt>**Leggi record**</dt></span><span class="sxs-lookup"><span data-stu-id="1403f-127"><dt>**Read Record**</dt></span></span> </dl> | <span data-ttu-id="1403f-128">Posizione bit:-----100</span><span class="sxs-lookup"><span data-stu-id="1403f-128">Bit position: -----100</span></span><br/> <span data-ttu-id="1403f-129">Leggere il record P1.</span><span class="sxs-lookup"><span data-stu-id="1403f-129">Read record P1.</span></span><br/>                           |
| <span id="Up_to_Last"></span><span id="up_to_last"></span><span id="UP_TO_LAST"></span><dl> <span data-ttu-id="1403f-130"><dt>**Fino alla fine**</dt></span><span class="sxs-lookup"><span data-stu-id="1403f-130"><dt>**Up to Last**</dt></span></span> </dl>     | <span data-ttu-id="1403f-131">Posizione bit:-----101</span><span class="sxs-lookup"><span data-stu-id="1403f-131">Bit position: -----101</span></span><br/> <span data-ttu-id="1403f-132">Leggere tutti i record da P1 fino alla fine.</span><span class="sxs-lookup"><span data-stu-id="1403f-132">Read all records from P1 up to the last.</span></span> <br/> |
| <span id="Up_to_P1"></span><span id="up_to_p1"></span><span id="UP_TO_P1"></span><dl> <span data-ttu-id="1403f-133"><dt>**Fino a P1**</dt></span><span class="sxs-lookup"><span data-stu-id="1403f-133"><dt>**Up to P1**</dt></span></span> </dl>             | <span data-ttu-id="1403f-134">Posizione bit:-----110</span><span class="sxs-lookup"><span data-stu-id="1403f-134">Bit position: -----110</span></span><br/> <span data-ttu-id="1403f-135">Leggere tutti i record dall'ultimo fino a P1.</span><span class="sxs-lookup"><span data-stu-id="1403f-135">Read all records from the last up to P1.</span></span> <br/> |
| <span id="RFU"></span><span id="rfu"></span><dl> <span data-ttu-id="1403f-136"><dt>**RFU**</dt></span><span class="sxs-lookup"><span data-stu-id="1403f-136"><dt>**RFU**</dt></span></span> </dl>                                                       | <span data-ttu-id="1403f-137">Posizione bit:-----111</span><span class="sxs-lookup"><span data-stu-id="1403f-137">Bit position: -----111</span></span><br/>                                                      |
| <span id="Record_ID"></span><span id="record_id"></span><span id="RECORD_ID"></span><dl> <span data-ttu-id="1403f-138"><dt>**ID record**</dt></span><span class="sxs-lookup"><span data-stu-id="1403f-138"><dt>**Record ID**</dt></span></span> </dl>         | <span data-ttu-id="1403f-139">Posizione bit:-----0xx</span><span class="sxs-lookup"><span data-stu-id="1403f-139">Bit position: -----0xx</span></span><br/> <span data-ttu-id="1403f-140">Utilizzo del numero di record in P1.</span><span class="sxs-lookup"><span data-stu-id="1403f-140">Usage of record number in P1.</span></span><br/>             |
| <span id="First_Occur"></span><span id="first_occur"></span><span id="FIRST_OCCUR"></span><dl> <span data-ttu-id="1403f-141"><dt>**Prima occorrenza**</dt></span><span class="sxs-lookup"><span data-stu-id="1403f-141"><dt>**First Occur**</dt></span></span> </dl> | <span data-ttu-id="1403f-142">Posizione bit:-----000</span><span class="sxs-lookup"><span data-stu-id="1403f-142">Bit position: -----000</span></span><br/> <span data-ttu-id="1403f-143">Lettura prima occorrenza.</span><span class="sxs-lookup"><span data-stu-id="1403f-143">Read first occurrence.</span></span> <br/>                   |
| <span id="Last_Occur"></span><span id="last_occur"></span><span id="LAST_OCCUR"></span><dl> <span data-ttu-id="1403f-144"><dt>**Ultima occorrenza**</dt></span><span class="sxs-lookup"><span data-stu-id="1403f-144"><dt>**Last Occur**</dt></span></span> </dl>     | <span data-ttu-id="1403f-145">Posizione bit:-----001</span><span class="sxs-lookup"><span data-stu-id="1403f-145">Bit position: -----001</span></span><br/> <span data-ttu-id="1403f-146">Leggere l'ultima occorrenza.</span><span class="sxs-lookup"><span data-stu-id="1403f-146">Read last occurrence.</span></span> <br/>                    |
| <span id="Next_Occur"></span><span id="next_occur"></span><span id="NEXT_OCCUR"></span><dl> <span data-ttu-id="1403f-147"><dt>**Prossima esecuzione**</dt></span><span class="sxs-lookup"><span data-stu-id="1403f-147"><dt>**Next Occur**</dt></span></span> </dl>     | <span data-ttu-id="1403f-148">Posizione bit:-----010</span><span class="sxs-lookup"><span data-stu-id="1403f-148">Bit position: -----010</span></span><br/> <span data-ttu-id="1403f-149">Leggere l'occorrenza successiva.</span><span class="sxs-lookup"><span data-stu-id="1403f-149">Read next occurrence.</span></span> <br/>                    |
| <span id="Previous"></span><span id="previous"></span><span id="PREVIOUS"></span><dl> <span data-ttu-id="1403f-150"><dt>**Indietro**</dt></span><span class="sxs-lookup"><span data-stu-id="1403f-150"><dt>**Previous**</dt></span></span> </dl>             | <span data-ttu-id="1403f-151">Posizione bit:-----011</span><span class="sxs-lookup"><span data-stu-id="1403f-151">Bit position: -----011</span></span><br/> <span data-ttu-id="1403f-152">Leggere l'occorrenza precedente.</span><span class="sxs-lookup"><span data-stu-id="1403f-152">Read previous occurrence.</span></span> <br/>                |
| <span id="Secret"></span><span id="secret"></span><span id="SECRET"></span><dl> <span data-ttu-id="1403f-153"><dt>**Segreto**</dt></span><span class="sxs-lookup"><span data-stu-id="1403f-153"><dt>**Secret**</dt></span></span> </dl>                     | <span data-ttu-id="1403f-154">Posizione bit:---xxxxx</span><span class="sxs-lookup"><span data-stu-id="1403f-154">Bit position: ---xxxxx</span></span><br/>                                                      |



 

</dd> <dt>

<span data-ttu-id="1403f-155">*lBytesToRead* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="1403f-155">*lBytesToRead* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1403f-156">Numero di byte da leggere dall'EF trasparente.</span><span class="sxs-lookup"><span data-stu-id="1403f-156">Number of bytes to read from the transparent EF.</span></span>

<span data-ttu-id="1403f-157">Se il campo le contiene solo zeri, a seconda del valore di b3b2b1 P2 e del limite di 256 per la lunghezza breve o 65536 per la lunghezza prolungata, il comando deve leggere completamente il singolo record richiesto o la sequenza di record richiesta.</span><span class="sxs-lookup"><span data-stu-id="1403f-157">If the Le field contains only zeros, then depending on b3b2b1 of P2 and within the limit of 256 for short length or 65536 for extended length, the command should read completely either the single requested record or the requested sequence of records.</span></span>

</dd> <dt>

<span data-ttu-id="1403f-158">*ppCmd* \[ in uscita\]</span><span class="sxs-lookup"><span data-stu-id="1403f-158">*ppCmd* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="1403f-159">In input, un puntatore a un oggetto di interfaccia [**ISCardCmd**](iscardcmd.md) o **null**.</span><span class="sxs-lookup"><span data-stu-id="1403f-159">On input, a pointer to an [**ISCardCmd**](iscardcmd.md) interface object or **NULL**.</span></span>

<span data-ttu-id="1403f-160">Al ritorno, viene compilato con il comando APDU creato da questa operazione.</span><span class="sxs-lookup"><span data-stu-id="1403f-160">On return, it is filled with the APDU command constructed by this operation.</span></span> <span data-ttu-id="1403f-161">Se *ppCmd* è stato impostato su **null**, un oggetto [**ISCardCmd**](iscardcmd.md) della [*Smart Card*](../secgloss/s-gly.md) viene creato e restituito internamente tramite il puntatore *ppCmd* .</span><span class="sxs-lookup"><span data-stu-id="1403f-161">If *ppCmd* was set to **NULL**, a [*smart card*](../secgloss/s-gly.md) [**ISCardCmd**](iscardcmd.md) object is internally created and returned via the *ppCmd* pointer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1403f-162">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="1403f-162">Return value</span></span>

<span data-ttu-id="1403f-163">Il metodo restituisce uno dei valori possibili seguenti.</span><span class="sxs-lookup"><span data-stu-id="1403f-163">The method returns one of the following possible values.</span></span>



| <span data-ttu-id="1403f-164">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="1403f-164">Return code</span></span>                                                                                   | <span data-ttu-id="1403f-165">Descrizione</span><span class="sxs-lookup"><span data-stu-id="1403f-165">Description</span></span>                                  |
|-----------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="1403f-166"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="1403f-166"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="1403f-167">Operazione completata correttamente.</span><span class="sxs-lookup"><span data-stu-id="1403f-167">Operation completed successfully.</span></span><br/> |
| <dl> <span data-ttu-id="1403f-168"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="1403f-168"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="1403f-169">Parametro non valido.</span><span class="sxs-lookup"><span data-stu-id="1403f-169">Invalid parameter.</span></span><br/>                |
| <dl> <span data-ttu-id="1403f-170"><dt>**\_puntatore E**</dt></span><span class="sxs-lookup"><span data-stu-id="1403f-170"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="1403f-171">È stato passato un puntatore non valido.</span><span class="sxs-lookup"><span data-stu-id="1403f-171">A bad pointer was passed in.</span></span><br/>      |
| <dl> <span data-ttu-id="1403f-172"><dt>**E \_ OutOfMemory**</dt></span><span class="sxs-lookup"><span data-stu-id="1403f-172"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="1403f-173">Memoria insufficiente.</span><span class="sxs-lookup"><span data-stu-id="1403f-173">Out of memory.</span></span><br/>                    |



 

## <a name="remarks"></a><span data-ttu-id="1403f-174">Commenti</span><span class="sxs-lookup"><span data-stu-id="1403f-174">Remarks</span></span>

<span data-ttu-id="1403f-175">Il comando incapsulato può essere eseguito solo se lo stato di sicurezza della [*Smart Card*](../secgloss/s-gly.md) soddisfa gli attributi di sicurezza del file elementare letto.</span><span class="sxs-lookup"><span data-stu-id="1403f-175">The encapsulated command can only be performed if the security status of the [*smart card*](../secgloss/s-gly.md) satisfies the security attributes of the elementary file being read.</span></span>

<span data-ttu-id="1403f-176">Se al momento dell'invio di questo comando è attualmente selezionato un altro file elementare, è possibile che venga elaborato senza l'identificazione del file attualmente selezionato.</span><span class="sxs-lookup"><span data-stu-id="1403f-176">If another elementary file is currently selected at the time of issuing this command, it may be processed without identification of the currently selected file.</span></span>

<span data-ttu-id="1403f-177">Quando il comando contiene un identificatore elementare breve valido, imposta il file come file elementare corrente.</span><span class="sxs-lookup"><span data-stu-id="1403f-177">When the command contains a valid short elementary identifier, it sets the file as current elementary file.</span></span>

<span data-ttu-id="1403f-178">Non è possibile leggere i file elementari senza una struttura di record.</span><span class="sxs-lookup"><span data-stu-id="1403f-178">Elementary files without a record structure cannot be read.</span></span> <span data-ttu-id="1403f-179">Il comando incapsulato viene interrotto se applicato a un file elementare senza una struttura di record.</span><span class="sxs-lookup"><span data-stu-id="1403f-179">The encapsulated command aborts if applied to an elementary file without a record structure.</span></span>

<span data-ttu-id="1403f-180">Per un elenco di tutti i metodi forniti da questa interfaccia, vedere [**ISCardISO7816**](iscardiso7816.md).</span><span class="sxs-lookup"><span data-stu-id="1403f-180">For a list of all the methods provided by this interface, see [**ISCardISO7816**](iscardiso7816.md).</span></span>

<span data-ttu-id="1403f-181">Oltre ai codici di errore COM elencati sopra, questa interfaccia può restituire un codice di errore della smart card se è stata chiamata una funzione Smart Card per completare la richiesta.</span><span class="sxs-lookup"><span data-stu-id="1403f-181">In addition to the COM error codes listed above, this interface may return a smart card error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="1403f-182">Per ulteriori informazioni, vedere [valori restituiti della smart card](authentication-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="1403f-182">For more information, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="1403f-183">Requisiti</span><span class="sxs-lookup"><span data-stu-id="1403f-183">Requirements</span></span>



| <span data-ttu-id="1403f-184">Requisito</span><span class="sxs-lookup"><span data-stu-id="1403f-184">Requirement</span></span> | <span data-ttu-id="1403f-185">Valore</span><span class="sxs-lookup"><span data-stu-id="1403f-185">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="1403f-186">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="1403f-186">Minimum supported client</span></span><br/> | <span data-ttu-id="1403f-187">\[Solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="1403f-187">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="1403f-188">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="1403f-188">Minimum supported server</span></span><br/> | <span data-ttu-id="1403f-189">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="1403f-189">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="1403f-190">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="1403f-190">End of client support</span></span><br/>    | <span data-ttu-id="1403f-191">Windows XP</span><span class="sxs-lookup"><span data-stu-id="1403f-191">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="1403f-192">Fine del supporto server</span><span class="sxs-lookup"><span data-stu-id="1403f-192">End of server support</span></span><br/>    | <span data-ttu-id="1403f-193">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="1403f-193">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="1403f-194">Intestazione</span><span class="sxs-lookup"><span data-stu-id="1403f-194">Header</span></span><br/>                   | <dl> <span data-ttu-id="1403f-195"><dt>Scardssp. h</dt></span><span class="sxs-lookup"><span data-stu-id="1403f-195"><dt>Scardssp.h</dt></span></span> </dl>   |
| <span data-ttu-id="1403f-196">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="1403f-196">Type library</span></span><br/>             | <dl> <span data-ttu-id="1403f-197"><dt>Scardsrv. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="1403f-197"><dt>Scardsrv.tlb</dt></span></span> </dl> |
| <span data-ttu-id="1403f-198">DLL</span><span class="sxs-lookup"><span data-stu-id="1403f-198">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1403f-199"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1403f-199"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="1403f-200">IID</span><span class="sxs-lookup"><span data-stu-id="1403f-200">IID</span></span><br/>                      | <span data-ttu-id="1403f-201">IID \_ ISCardISO7816 è definito come 53B6AA68-3F56-11D0-916B-00AA00C18068</span><span class="sxs-lookup"><span data-stu-id="1403f-201">IID\_ISCardISO7816 is defined as 53B6AA68-3F56-11D0-916B-00AA00C18068</span></span><br/>        |



## <a name="see-also"></a><span data-ttu-id="1403f-202">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="1403f-202">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1403f-203">**AppendRecord**</span><span class="sxs-lookup"><span data-stu-id="1403f-203">**AppendRecord**</span></span>](iscardiso7816-appendrecord.md)
</dt> <dt>

[<span data-ttu-id="1403f-204">**ISCardISO7816**</span><span class="sxs-lookup"><span data-stu-id="1403f-204">**ISCardISO7816**</span></span>](iscardiso7816.md)
</dt> <dt>

[<span data-ttu-id="1403f-205">**UpdateRecord**</span><span class="sxs-lookup"><span data-stu-id="1403f-205">**UpdateRecord**</span></span>](iscardiso7816-updaterecord.md)
</dt> <dt>

[<span data-ttu-id="1403f-206">**WriteRecord**</span><span class="sxs-lookup"><span data-stu-id="1403f-206">**WriteRecord**</span></span>](iscardiso7816-writerecord.md)
</dt> </dl>

 

 
