---
description: Il metodo UpdateRecord costruisce un comando APDU (Application Protocol Data Unit) che aggiorna un record specifico con i bit specificati nel comando APDU.
ms.assetid: 66039afd-5d73-41b3-b87b-b5d598c6f3db
title: 'Metodo ISCardISO7816:: UpdateRecord (scardssp. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardISO7816.UpdateRecord
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 6bf810594e623d58944f58d3b7671664b3be175f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104231716"
---
# <a name="iscardiso7816updaterecord-method"></a><span data-ttu-id="af1c6-103">Metodo ISCardISO7816:: UpdateRecord</span><span class="sxs-lookup"><span data-stu-id="af1c6-103">ISCardISO7816::UpdateRecord method</span></span>

<span data-ttu-id="af1c6-104">\[Il metodo **UpdateRecord** è disponibile per l'uso nei sistemi operativi specificati nella sezione requisiti.</span><span class="sxs-lookup"><span data-stu-id="af1c6-104">\[The **UpdateRecord** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="af1c6-105">Non è disponibile per l'utilizzo in Windows Server 2003 con Service Pack 1 (SP1) e versioni successive, Windows Vista, Windows Server 2008 e versioni successive del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="af1c6-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="af1c6-106">I [moduli Smart Card](/previous-versions/windows/desktop/secsmart/smart-card-modules) offrono funzionalità simili.\]</span><span class="sxs-lookup"><span data-stu-id="af1c6-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="af1c6-107">Il metodo **UpdateRecord** costruisce un comando APDU ( [*Application Protocol Data Unit*](../secgloss/a-gly.md) ) che aggiorna un record specifico con i bit specificati nel comando APDU.</span><span class="sxs-lookup"><span data-stu-id="af1c6-107">The **UpdateRecord** method constructs an [*application protocol data unit*](../secgloss/a-gly.md) (APDU) command that updates a specific record with the bits given in the APDU command.</span></span>

> [!Note]  
> <span data-ttu-id="af1c6-108">Quando si usa l'indirizzamento dei record corrente, il comando imposta il puntatore del record sul record aggiornato correttamente.</span><span class="sxs-lookup"><span data-stu-id="af1c6-108">When using current record addressing, the command sets the record pointer on the successfully updated record.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="af1c6-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="af1c6-109">Syntax</span></span>


```C++
HRESULT UpdateRecord(
  [in]      BYTE         byRecordId,
  [in]      BYTE         byRefCtrl,
  [in]      LPBYTEBUFFER pData,
  [in, out] LPSCARDCMD   *ppCmd
);
```



## <a name="parameters"></a><span data-ttu-id="af1c6-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="af1c6-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="af1c6-111">*byRecordId* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="af1c6-111">*byRecordId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="af1c6-112">Valore P1:</span><span class="sxs-lookup"><span data-stu-id="af1c6-112">P1 value:</span></span>

<span data-ttu-id="af1c6-113">P1 = 00 indica il record corrente</span><span class="sxs-lookup"><span data-stu-id="af1c6-113">P1 = 00 designates the current record</span></span>

<span data-ttu-id="af1c6-114">P1! = "00" è il numero del record specificato</span><span class="sxs-lookup"><span data-stu-id="af1c6-114">P1 != '00' is the number of the specified record</span></span>

</dd> <dt>

<span data-ttu-id="af1c6-115">*byRefCtrl* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="af1c6-115">*byRefCtrl* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="af1c6-116">Codifica del controllo di riferimento P2:</span><span class="sxs-lookup"><span data-stu-id="af1c6-116">Coding of the reference control P2:</span></span>



| <span data-ttu-id="af1c6-117">Valore</span><span class="sxs-lookup"><span data-stu-id="af1c6-117">Value</span></span>                                                                                                                                                                                                | <span data-ttu-id="af1c6-118">Significato</span><span class="sxs-lookup"><span data-stu-id="af1c6-118">Meaning</span></span>                                                             |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------|
| <span id="Current_EF"></span><span id="current_ef"></span><span id="CURRENT_EF"></span><dl> <span data-ttu-id="af1c6-119"><dt>**EF corrente**</dt></span><span class="sxs-lookup"><span data-stu-id="af1c6-119"><dt>**Current EF**</dt></span></span> </dl>                     | <span data-ttu-id="af1c6-120">Posizione bit: 00000---</span><span class="sxs-lookup"><span data-stu-id="af1c6-120">Bit position: 00000---</span></span><br/> <span data-ttu-id="af1c6-121">Attualmente selezionato EF.</span><span class="sxs-lookup"><span data-stu-id="af1c6-121">Currently selected EF.</span></span><br/> |
| <span id="Short_EF_ID"></span><span id="short_ef_id"></span><span id="SHORT_EF_ID"></span><dl> <span data-ttu-id="af1c6-122"><dt>**ID EF breve**</dt></span><span class="sxs-lookup"><span data-stu-id="af1c6-122"><dt>**Short EF ID**</dt></span></span> </dl>                 | <span data-ttu-id="af1c6-123">Posizione bit: xxxxx---</span><span class="sxs-lookup"><span data-stu-id="af1c6-123">Bit position: xxxxx---</span></span><br/> <span data-ttu-id="af1c6-124">Identificatore EF breve.</span><span class="sxs-lookup"><span data-stu-id="af1c6-124">Short EF identifier.</span></span><br/>   |
| <span id="First_Record"></span><span id="first_record"></span><span id="FIRST_RECORD"></span><dl> <span data-ttu-id="af1c6-125"><dt>**Primo record**</dt></span><span class="sxs-lookup"><span data-stu-id="af1c6-125"><dt>**First Record**</dt></span></span> </dl>             | <span data-ttu-id="af1c6-126">Posizione bit:-----000</span><span class="sxs-lookup"><span data-stu-id="af1c6-126">Bit position: -----000</span></span><br/>                                   |
| <span id="Last_Record"></span><span id="last_record"></span><span id="LAST_RECORD"></span><dl> <span data-ttu-id="af1c6-127"><dt>**Ultimo record**</dt></span><span class="sxs-lookup"><span data-stu-id="af1c6-127"><dt>**Last Record**</dt></span></span> </dl>                 | <span data-ttu-id="af1c6-128">Posizione bit:-----001</span><span class="sxs-lookup"><span data-stu-id="af1c6-128">Bit position: -----001</span></span><br/>                                   |
| <span id="Next_Record"></span><span id="next_record"></span><span id="NEXT_RECORD"></span><dl> <span data-ttu-id="af1c6-129"><dt>**Record successivo**</dt></span><span class="sxs-lookup"><span data-stu-id="af1c6-129"><dt>**Next Record**</dt></span></span> </dl>                 | <span data-ttu-id="af1c6-130">Posizione bit:-----010</span><span class="sxs-lookup"><span data-stu-id="af1c6-130">Bit position: -----010</span></span><br/>                                   |
| <span id="Previous_Record"></span><span id="previous_record"></span><span id="PREVIOUS_RECORD"></span><dl> <span data-ttu-id="af1c6-131"><dt>**Record precedente**</dt></span><span class="sxs-lookup"><span data-stu-id="af1c6-131"><dt>**Previous Record**</dt></span></span> </dl> | <span data-ttu-id="af1c6-132">Posizione bit:-----011</span><span class="sxs-lookup"><span data-stu-id="af1c6-132">Bit position: -----011</span></span><br/>                                   |
| <span id="Record___in_P1"></span><span id="record___in_p1"></span><span id="RECORD___IN_P1"></span><dl> <span data-ttu-id="af1c6-133"><dt>**Record \# in P1**</dt></span><span class="sxs-lookup"><span data-stu-id="af1c6-133"><dt>**Record \# in P1**</dt></span></span> </dl>    | <span data-ttu-id="af1c6-134">Posizione bit:-----100</span><span class="sxs-lookup"><span data-stu-id="af1c6-134">Bit position: -----100</span></span><br/>                                   |



 

</dd> <dt>

<span data-ttu-id="af1c6-135">*pData* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="af1c6-135">*pData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="af1c6-136">Puntatore al record da aggiornare.</span><span class="sxs-lookup"><span data-stu-id="af1c6-136">Pointer to the record to be updated.</span></span>

</dd> <dt>

<span data-ttu-id="af1c6-137">*ppCmd* \[ in uscita\]</span><span class="sxs-lookup"><span data-stu-id="af1c6-137">*ppCmd* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="af1c6-138">In input, un puntatore a un oggetto di interfaccia [**ISCardCmd**](iscardcmd.md) o **null**.</span><span class="sxs-lookup"><span data-stu-id="af1c6-138">On input, a pointer to an [**ISCardCmd**](iscardcmd.md) interface object or **NULL**.</span></span>

<span data-ttu-id="af1c6-139">Al ritorno, viene compilato con il comando APDU creato da questa operazione.</span><span class="sxs-lookup"><span data-stu-id="af1c6-139">On return, it is filled with the APDU command constructed by this operation.</span></span> <span data-ttu-id="af1c6-140">Se *ppCmd* è stato impostato su **null**, un oggetto [**ISCardCmd**](iscardcmd.md) della [*Smart Card*](../secgloss/s-gly.md) viene creato e restituito internamente tramite il puntatore *ppCmd* .</span><span class="sxs-lookup"><span data-stu-id="af1c6-140">If *ppCmd* was set to **NULL**, a [*smart card*](../secgloss/s-gly.md) [**ISCardCmd**](iscardcmd.md) object is internally created and returned via the *ppCmd* pointer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="af1c6-141">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="af1c6-141">Return value</span></span>

<span data-ttu-id="af1c6-142">Il metodo restituisce uno dei valori possibili seguenti.</span><span class="sxs-lookup"><span data-stu-id="af1c6-142">The method returns one of the following possible values.</span></span>



| <span data-ttu-id="af1c6-143">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="af1c6-143">Return code</span></span>                                                                                   | <span data-ttu-id="af1c6-144">Descrizione</span><span class="sxs-lookup"><span data-stu-id="af1c6-144">Description</span></span>                                  |
|-----------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="af1c6-145"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="af1c6-145"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="af1c6-146">Operazione completata correttamente.</span><span class="sxs-lookup"><span data-stu-id="af1c6-146">Operation completed successfully.</span></span><br/> |
| <dl> <span data-ttu-id="af1c6-147"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="af1c6-147"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="af1c6-148">Parametro non valido.</span><span class="sxs-lookup"><span data-stu-id="af1c6-148">Invalid parameter.</span></span><br/>                |
| <dl> <span data-ttu-id="af1c6-149"><dt>**\_puntatore E**</dt></span><span class="sxs-lookup"><span data-stu-id="af1c6-149"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="af1c6-150">È stato passato un puntatore non valido.</span><span class="sxs-lookup"><span data-stu-id="af1c6-150">A bad pointer was passed in.</span></span><br/>      |
| <dl> <span data-ttu-id="af1c6-151"><dt>**E \_ OutOfMemory**</dt></span><span class="sxs-lookup"><span data-stu-id="af1c6-151"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="af1c6-152">Memoria insufficiente.</span><span class="sxs-lookup"><span data-stu-id="af1c6-152">Out of memory.</span></span><br/>                    |



 

## <a name="remarks"></a><span data-ttu-id="af1c6-153">Commenti</span><span class="sxs-lookup"><span data-stu-id="af1c6-153">Remarks</span></span>

<span data-ttu-id="af1c6-154">Il comando incapsulato può essere eseguito solo se lo stato di sicurezza della [*Smart Card*](../secgloss/s-gly.md) soddisfa gli attributi di sicurezza del file elementare elaborato.</span><span class="sxs-lookup"><span data-stu-id="af1c6-154">The encapsulated command can only be performed if the security status of the [*smart card*](../secgloss/s-gly.md) satisfies the security attributes of the elementary file being processed.</span></span>

<span data-ttu-id="af1c6-155">Quando il comando contiene un identificatore elementare breve valido, imposta il file come file elementare corrente.</span><span class="sxs-lookup"><span data-stu-id="af1c6-155">When the command contains a valid short elementary identifier, it sets the file as current elementary file.</span></span> <span data-ttu-id="af1c6-156">Se al momento dell'invio di questo comando è attualmente selezionato un altro file elementare, questo comando può essere elaborato senza l'identificazione del file attualmente selezionato.</span><span class="sxs-lookup"><span data-stu-id="af1c6-156">If another elementary file is currently selected at the time of issuing this command, this command may be processed without identification of the currently selected file.</span></span>

<span data-ttu-id="af1c6-157">Se il comando costruito si applica a un file elementare fisso o con struttura ciclica, verrà interrotto se la lunghezza del record è diversa dalla lunghezza del record esistente.</span><span class="sxs-lookup"><span data-stu-id="af1c6-157">If the constructed command applies to a linear-fixed or cyclic-structured elementary file, it will abort if the record length is different from the length of the existing record.</span></span>

<span data-ttu-id="af1c6-158">Se il comando si applica a un file elementare strutturato con variabile lineare, può essere eseguito quando la lunghezza del record è diversa dalla lunghezza del record esistente.</span><span class="sxs-lookup"><span data-stu-id="af1c6-158">If the command applies to a linear-variable structured elementary file, it may be carried out when the record length is different from the length of the existing record.</span></span>

<span data-ttu-id="af1c6-159">L'opzione "Previous" del comando (P2 = xxxxx011), applicata a un file ciclico, ha lo stesso comportamento di un comando costruito da [**AppendRecord**](iscardiso7816-appendrecord.md).</span><span class="sxs-lookup"><span data-stu-id="af1c6-159">The "previous" option of the command (P2=xxxxx011), applied to a cyclic file, has the same behavior as a command constructed by [**AppendRecord**](iscardiso7816-appendrecord.md).</span></span>

<span data-ttu-id="af1c6-160">Non è possibile leggere i file elementari senza una struttura di record.</span><span class="sxs-lookup"><span data-stu-id="af1c6-160">Elementary files without a record structure cannot be read.</span></span> <span data-ttu-id="af1c6-161">Il comando costruito viene interrotto se applicato a un file elementare senza struttura di record.</span><span class="sxs-lookup"><span data-stu-id="af1c6-161">The constructed command aborts if applied to an elementary file without record structure.</span></span>

<span data-ttu-id="af1c6-162">Per un elenco di tutti i metodi forniti da questa interfaccia, vedere [**ISCardISO7816**](iscardiso7816.md).</span><span class="sxs-lookup"><span data-stu-id="af1c6-162">For a list of all the methods provided by this interface, see [**ISCardISO7816**](iscardiso7816.md).</span></span>

<span data-ttu-id="af1c6-163">Oltre ai codici di errore COM elencati sopra, questa interfaccia può restituire un codice di errore della smart card se è stata chiamata una funzione Smart Card per completare la richiesta.</span><span class="sxs-lookup"><span data-stu-id="af1c6-163">In addition to the COM error codes listed above, this interface may return a smart card error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="af1c6-164">Per ulteriori informazioni, vedere [valori restituiti della smart card](authentication-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="af1c6-164">For more information, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="af1c6-165">Requisiti</span><span class="sxs-lookup"><span data-stu-id="af1c6-165">Requirements</span></span>



| <span data-ttu-id="af1c6-166">Requisito</span><span class="sxs-lookup"><span data-stu-id="af1c6-166">Requirement</span></span> | <span data-ttu-id="af1c6-167">Valore</span><span class="sxs-lookup"><span data-stu-id="af1c6-167">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="af1c6-168">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="af1c6-168">Minimum supported client</span></span><br/> | <span data-ttu-id="af1c6-169">\[Solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="af1c6-169">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="af1c6-170">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="af1c6-170">Minimum supported server</span></span><br/> | <span data-ttu-id="af1c6-171">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="af1c6-171">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="af1c6-172">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="af1c6-172">End of client support</span></span><br/>    | <span data-ttu-id="af1c6-173">Windows XP</span><span class="sxs-lookup"><span data-stu-id="af1c6-173">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="af1c6-174">Fine del supporto server</span><span class="sxs-lookup"><span data-stu-id="af1c6-174">End of server support</span></span><br/>    | <span data-ttu-id="af1c6-175">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="af1c6-175">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="af1c6-176">Intestazione</span><span class="sxs-lookup"><span data-stu-id="af1c6-176">Header</span></span><br/>                   | <dl> <span data-ttu-id="af1c6-177"><dt>Scardssp. h</dt></span><span class="sxs-lookup"><span data-stu-id="af1c6-177"><dt>Scardssp.h</dt></span></span> </dl>   |
| <span data-ttu-id="af1c6-178">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="af1c6-178">Type library</span></span><br/>             | <dl> <span data-ttu-id="af1c6-179"><dt>Scardsrv. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="af1c6-179"><dt>Scardsrv.tlb</dt></span></span> </dl> |
| <span data-ttu-id="af1c6-180">DLL</span><span class="sxs-lookup"><span data-stu-id="af1c6-180">DLL</span></span><br/>                      | <dl> <span data-ttu-id="af1c6-181"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="af1c6-181"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="af1c6-182">IID</span><span class="sxs-lookup"><span data-stu-id="af1c6-182">IID</span></span><br/>                      | <span data-ttu-id="af1c6-183">IID \_ ISCardISO7816 è definito come 53B6AA68-3F56-11D0-916B-00AA00C18068</span><span class="sxs-lookup"><span data-stu-id="af1c6-183">IID\_ISCardISO7816 is defined as 53B6AA68-3F56-11D0-916B-00AA00C18068</span></span><br/>        |



## <a name="see-also"></a><span data-ttu-id="af1c6-184">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="af1c6-184">See also</span></span>

<dl> <dt>

[<span data-ttu-id="af1c6-185">**AppendRecord**</span><span class="sxs-lookup"><span data-stu-id="af1c6-185">**AppendRecord**</span></span>](iscardiso7816-appendrecord.md)
</dt> <dt>

[<span data-ttu-id="af1c6-186">**ISCardISO7816**</span><span class="sxs-lookup"><span data-stu-id="af1c6-186">**ISCardISO7816**</span></span>](iscardiso7816.md)
</dt> <dt>

[<span data-ttu-id="af1c6-187">**ReadRecord**</span><span class="sxs-lookup"><span data-stu-id="af1c6-187">**ReadRecord**</span></span>](iscardiso7816-readrecord.md)
</dt> <dt>

[<span data-ttu-id="af1c6-188">**WriteRecord**</span><span class="sxs-lookup"><span data-stu-id="af1c6-188">**WriteRecord**</span></span>](iscardiso7816-writerecord.md)
</dt> </dl>

 

 
