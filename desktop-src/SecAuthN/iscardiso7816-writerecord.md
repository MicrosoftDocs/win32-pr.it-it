---
description: Costruisce un comando APDU che avvia una delle operazioni elencate.
ms.assetid: 2ce313b9-ccd7-4be0-a91f-d0747e35fab8
title: 'Metodo ISCardISO7816:: WriteRecord (scardssp. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardISO7816.WriteRecord
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 30bfdb9ff8779633d81da89bbf7ac8e69a617d04
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104128291"
---
# <a name="iscardiso7816writerecord-method"></a><span data-ttu-id="0b734-103">Metodo ISCardISO7816:: WriteRecord</span><span class="sxs-lookup"><span data-stu-id="0b734-103">ISCardISO7816::WriteRecord method</span></span>

<span data-ttu-id="0b734-104">\[Il metodo **WriteRecord** è disponibile per l'uso nei sistemi operativi specificati nella sezione requisiti.</span><span class="sxs-lookup"><span data-stu-id="0b734-104">\[The **WriteRecord** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="0b734-105">Non è disponibile per l'utilizzo in Windows Server 2003 con Service Pack 1 (SP1) e versioni successive, Windows Vista, Windows Server 2008 e versioni successive del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="0b734-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="0b734-106">I [moduli Smart Card](/previous-versions/windows/desktop/secsmart/smart-card-modules) offrono funzionalità simili.\]</span><span class="sxs-lookup"><span data-stu-id="0b734-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="0b734-107">Il metodo **WriteRecord** costruisce un comando APDU ( [*Application Protocol Data Unit*](../secgloss/a-gly.md) ) che avvia una delle operazioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="0b734-107">The **WriteRecord** method constructs an [*application protocol data unit*](../secgloss/a-gly.md) (APDU) command that initiates one of the following operations:</span></span>

-   <span data-ttu-id="0b734-108">Scrittura una volta di un record.</span><span class="sxs-lookup"><span data-stu-id="0b734-108">The write once of a record.</span></span>
-   <span data-ttu-id="0b734-109">L' **or** logico dei byte di dati di un record è già presente nella scheda con i byte di dati del record specificato nel comando APDU.</span><span class="sxs-lookup"><span data-stu-id="0b734-109">The logical **OR** of the data bytes of a record already present in the card with the data bytes of the record given in the command APDU.</span></span>
-   <span data-ttu-id="0b734-110">L'operatore AND logico dei byte di dati di un record è già presente nella scheda con i byte di dati del record specificato nel comando APDU.</span><span class="sxs-lookup"><span data-stu-id="0b734-110">The logical AND of the data bytes of a record already present in the card with the data bytes of the record given in the command APDU.</span></span>

<span data-ttu-id="0b734-111">Quando non viene specificata alcuna indicazione nel byte di codifica dei dati, viene applicato il comportamento logico OR.</span><span class="sxs-lookup"><span data-stu-id="0b734-111">When no indication is given in the data coding byte, the logical OR behavior applies.</span></span>

> [!Note]  
> <span data-ttu-id="0b734-112">Quando si usa l'indirizzamento dei record corrente, il comando imposta il puntatore del record sul record aggiornato correttamente.</span><span class="sxs-lookup"><span data-stu-id="0b734-112">When using current record addressing, the command sets the record pointer on the successfully updated record.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="0b734-113">Sintassi</span><span class="sxs-lookup"><span data-stu-id="0b734-113">Syntax</span></span>


```C++
HRESULT WriteRecord(
  [in]      BYTE         byRecordId,
  [in]      BYTE         byRefCtrl,
  [in]      LPBYTEBUFFER pData,
  [in, out] LPSCARDCMD   *ppCmd
);
```



## <a name="parameters"></a><span data-ttu-id="0b734-114">Parametri</span><span class="sxs-lookup"><span data-stu-id="0b734-114">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0b734-115">*byRecordId* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="0b734-115">*byRecordId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0b734-116">Identificazione del record.</span><span class="sxs-lookup"><span data-stu-id="0b734-116">Record identification.</span></span> <span data-ttu-id="0b734-117">Si tratta del valore P1:</span><span class="sxs-lookup"><span data-stu-id="0b734-117">This is the P1 value:</span></span>

<span data-ttu-id="0b734-118">P1 = "00" indica il record corrente.</span><span class="sxs-lookup"><span data-stu-id="0b734-118">P1 = '00' designates the current record.</span></span>

<span data-ttu-id="0b734-119">P1! = "00" è il numero del record specificato.</span><span class="sxs-lookup"><span data-stu-id="0b734-119">P1 != '00' is the number of the specified record.</span></span>

</dd> <dt>

<span data-ttu-id="0b734-120">*byRefCtrl* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="0b734-120">*byRefCtrl* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0b734-121">Codifica del controllo di riferimento P2.</span><span class="sxs-lookup"><span data-stu-id="0b734-121">Coding of the reference control P2.</span></span>



| <span data-ttu-id="0b734-122">Valore</span><span class="sxs-lookup"><span data-stu-id="0b734-122">Value</span></span>                                                                                                                                                                                                | <span data-ttu-id="0b734-123">Significato</span><span class="sxs-lookup"><span data-stu-id="0b734-123">Meaning</span></span>                                                             |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------|
| <span id="Current_EF"></span><span id="current_ef"></span><span id="CURRENT_EF"></span><dl> <span data-ttu-id="0b734-124"><dt>**EF corrente**</dt></span><span class="sxs-lookup"><span data-stu-id="0b734-124"><dt>**Current EF**</dt></span></span> </dl>                     | <span data-ttu-id="0b734-125">Posizione bit: 00000---</span><span class="sxs-lookup"><span data-stu-id="0b734-125">Bit position: 00000---</span></span><br/> <span data-ttu-id="0b734-126">Attualmente selezionato EF.</span><span class="sxs-lookup"><span data-stu-id="0b734-126">Currently selected EF.</span></span><br/> |
| <span id="Short_EF_ID"></span><span id="short_ef_id"></span><span id="SHORT_EF_ID"></span><dl> <span data-ttu-id="0b734-127"><dt>**ID EF breve**</dt></span><span class="sxs-lookup"><span data-stu-id="0b734-127"><dt>**Short EF ID**</dt></span></span> </dl>                 | <span data-ttu-id="0b734-128">Posizione bit: xxxxx---</span><span class="sxs-lookup"><span data-stu-id="0b734-128">Bit position: xxxxx---</span></span><br/> <span data-ttu-id="0b734-129">Identificatore EF breve.</span><span class="sxs-lookup"><span data-stu-id="0b734-129">Short EF identifier.</span></span><br/>   |
| <span id="First_Record"></span><span id="first_record"></span><span id="FIRST_RECORD"></span><dl> <span data-ttu-id="0b734-130"><dt>**Primo record**</dt></span><span class="sxs-lookup"><span data-stu-id="0b734-130"><dt>**First Record**</dt></span></span> </dl>             | <span data-ttu-id="0b734-131">Posizione bit:-----000</span><span class="sxs-lookup"><span data-stu-id="0b734-131">Bit position: -----000</span></span><br/>                                   |
| <span id="Last_Record"></span><span id="last_record"></span><span id="LAST_RECORD"></span><dl> <span data-ttu-id="0b734-132"><dt>**Ultimo record**</dt></span><span class="sxs-lookup"><span data-stu-id="0b734-132"><dt>**Last Record**</dt></span></span> </dl>                 | <span data-ttu-id="0b734-133">Posizione bit:-----001</span><span class="sxs-lookup"><span data-stu-id="0b734-133">Bit position: -----001</span></span><br/>                                   |
| <span id="Next_Record"></span><span id="next_record"></span><span id="NEXT_RECORD"></span><dl> <span data-ttu-id="0b734-134"><dt>**Record successivo**</dt></span><span class="sxs-lookup"><span data-stu-id="0b734-134"><dt>**Next Record**</dt></span></span> </dl>                 | <span data-ttu-id="0b734-135">Posizione bit:-----010</span><span class="sxs-lookup"><span data-stu-id="0b734-135">Bit position: -----010</span></span><br/>                                   |
| <span id="Previous_Record"></span><span id="previous_record"></span><span id="PREVIOUS_RECORD"></span><dl> <span data-ttu-id="0b734-136"><dt>**Record precedente**</dt></span><span class="sxs-lookup"><span data-stu-id="0b734-136"><dt>**Previous Record**</dt></span></span> </dl> | <span data-ttu-id="0b734-137">Posizione bit:-----011</span><span class="sxs-lookup"><span data-stu-id="0b734-137">Bit position: -----011</span></span><br/>                                   |
| <span id="Record___in_P1"></span><span id="record___in_p1"></span><span id="RECORD___IN_P1"></span><dl> <span data-ttu-id="0b734-138"><dt>**Record \# in P1**</dt></span><span class="sxs-lookup"><span data-stu-id="0b734-138"><dt>**Record \# in P1**</dt></span></span> </dl>    | <span data-ttu-id="0b734-139">Posizione bit:-----100</span><span class="sxs-lookup"><span data-stu-id="0b734-139">Bit position: -----100</span></span><br/>                                   |



 

</dd> <dt>

<span data-ttu-id="0b734-140">*pData* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="0b734-140">*pData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0b734-141">Puntatore al record da scrivere.</span><span class="sxs-lookup"><span data-stu-id="0b734-141">Pointer to the record to be written.</span></span>

</dd> <dt>

<span data-ttu-id="0b734-142">*ppCmd* \[ in uscita\]</span><span class="sxs-lookup"><span data-stu-id="0b734-142">*ppCmd* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="0b734-143">In input, un puntatore a un oggetto di interfaccia [**ISCardCmd**](iscardcmd.md) o **null**.</span><span class="sxs-lookup"><span data-stu-id="0b734-143">On input, a pointer to an [**ISCardCmd**](iscardcmd.md) interface object or **NULL**.</span></span>

<span data-ttu-id="0b734-144">Al ritorno, viene compilato con il comando APDU creato da questa operazione.</span><span class="sxs-lookup"><span data-stu-id="0b734-144">On return, it is filled with the APDU command constructed by this operation.</span></span> <span data-ttu-id="0b734-145">Se *ppCmd* è stato impostato su **null**, un oggetto [**ISCardCmd**](iscardcmd.md) della [*Smart Card*](../secgloss/s-gly.md) viene creato e restituito internamente tramite il puntatore *ppCmd* .</span><span class="sxs-lookup"><span data-stu-id="0b734-145">If *ppCmd* was set to **NULL**, a [*smart card*](../secgloss/s-gly.md) [**ISCardCmd**](iscardcmd.md) object is internally created and returned via the *ppCmd* pointer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0b734-146">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="0b734-146">Return value</span></span>

<span data-ttu-id="0b734-147">Il metodo restituisce uno dei valori possibili seguenti.</span><span class="sxs-lookup"><span data-stu-id="0b734-147">The method returns one of the following possible values.</span></span>



| <span data-ttu-id="0b734-148">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="0b734-148">Return code</span></span>                                                                                   | <span data-ttu-id="0b734-149">Descrizione</span><span class="sxs-lookup"><span data-stu-id="0b734-149">Description</span></span>                                  |
|-----------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="0b734-150"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="0b734-150"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="0b734-151">Operazione completata correttamente.</span><span class="sxs-lookup"><span data-stu-id="0b734-151">Operation completed successfully.</span></span><br/> |
| <dl> <span data-ttu-id="0b734-152"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="0b734-152"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="0b734-153">Parametro non valido.</span><span class="sxs-lookup"><span data-stu-id="0b734-153">Invalid parameter.</span></span><br/>                |
| <dl> <span data-ttu-id="0b734-154"><dt>**\_puntatore E**</dt></span><span class="sxs-lookup"><span data-stu-id="0b734-154"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="0b734-155">È stato passato un puntatore non valido.</span><span class="sxs-lookup"><span data-stu-id="0b734-155">A bad pointer was passed in.</span></span><br/>      |
| <dl> <span data-ttu-id="0b734-156"><dt>**E \_ OutOfMemory**</dt></span><span class="sxs-lookup"><span data-stu-id="0b734-156"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="0b734-157">Memoria insufficiente.</span><span class="sxs-lookup"><span data-stu-id="0b734-157">Out of memory.</span></span><br/>                    |



 

## <a name="remarks"></a><span data-ttu-id="0b734-158">Commenti</span><span class="sxs-lookup"><span data-stu-id="0b734-158">Remarks</span></span>

<span data-ttu-id="0b734-159">Il comando incapsulato può essere eseguito solo se lo stato di sicurezza della [*Smart Card*](../secgloss/s-gly.md) soddisfa gli attributi di sicurezza del file elementare elaborato.</span><span class="sxs-lookup"><span data-stu-id="0b734-159">The encapsulated command can only be performed if the security status of the [*smart card*](../secgloss/s-gly.md) satisfies the security attributes of the elementary file being processed.</span></span>

<span data-ttu-id="0b734-160">Quando il comando contiene un identificatore elementare breve valido, imposta il file come file elementare corrente.</span><span class="sxs-lookup"><span data-stu-id="0b734-160">When the command contains a valid short elementary identifier, it sets the file as current elementary file.</span></span> <span data-ttu-id="0b734-161">Se al momento dell'invio di questo comando è attualmente selezionato un altro file elementare, questo comando può essere elaborato senza l'identificazione del file attualmente selezionato.</span><span class="sxs-lookup"><span data-stu-id="0b734-161">If another elementary file is currently selected at the time of issuing this command, this command may be processed without identification of the currently selected file.</span></span>

<span data-ttu-id="0b734-162">Se il comando incapsulato si applica a un file elementare fisso o con struttura ciclica, verrà interrotto se la lunghezza del record è diversa dalla lunghezza del record esistente.</span><span class="sxs-lookup"><span data-stu-id="0b734-162">If the encapsulated command applies to a linear-fixed or cyclic-structured elementary file, it will abort if the record length is different from the length of the existing record.</span></span> <span data-ttu-id="0b734-163">Se si applica a un file elementare strutturato a variabile lineare, può essere eseguito quando la lunghezza del record è diversa dalla lunghezza del record esistente.</span><span class="sxs-lookup"><span data-stu-id="0b734-163">If it applies to a linear-variable structured elementary file, it may be carried out when the record length is different from the length of the existing record.</span></span>

<span data-ttu-id="0b734-164">Se P2 = xxxxx011 e il file Elementary è ciclico, questo comando ha lo stesso comportamento di un comando costruito usando [**AppendRecord**](iscardiso7816-appendrecord.md).</span><span class="sxs-lookup"><span data-stu-id="0b734-164">If P2=xxxxx011 and the elementary file is cyclic file, this command has the same behavior a command constructed using [**AppendRecord**](iscardiso7816-appendrecord.md).</span></span>

<span data-ttu-id="0b734-165">I file elementari senza una struttura di record non possono essere scritti in.</span><span class="sxs-lookup"><span data-stu-id="0b734-165">Elementary files without a record structure cannot be written to.</span></span> <span data-ttu-id="0b734-166">Il comando costruito viene interrotto se applicato a un file elementare senza una struttura di record.</span><span class="sxs-lookup"><span data-stu-id="0b734-166">The constructed command aborts if applied to an elementary file without a record structure.</span></span>

<span data-ttu-id="0b734-167">Per un elenco di tutti i metodi forniti da questa interfaccia, vedere [**ISCardISO7816**](iscardiso7816.md).</span><span class="sxs-lookup"><span data-stu-id="0b734-167">For a list of all the methods provided by this interface, see [**ISCardISO7816**](iscardiso7816.md).</span></span>

<span data-ttu-id="0b734-168">Oltre ai codici di errore COM elencati sopra, questa interfaccia può restituire un codice di errore della smart card se è stata chiamata una funzione Smart Card per completare la richiesta.</span><span class="sxs-lookup"><span data-stu-id="0b734-168">In addition to the COM error codes listed above, this interface may return a smart card error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="0b734-169">Per ulteriori informazioni, vedere [valori restituiti della smart card](authentication-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="0b734-169">For more information, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="0b734-170">Requisiti</span><span class="sxs-lookup"><span data-stu-id="0b734-170">Requirements</span></span>



| <span data-ttu-id="0b734-171">Requisito</span><span class="sxs-lookup"><span data-stu-id="0b734-171">Requirement</span></span> | <span data-ttu-id="0b734-172">Valore</span><span class="sxs-lookup"><span data-stu-id="0b734-172">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="0b734-173">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0b734-173">Minimum supported client</span></span><br/> | <span data-ttu-id="0b734-174">\[Solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="0b734-174">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="0b734-175">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0b734-175">Minimum supported server</span></span><br/> | <span data-ttu-id="0b734-176">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="0b734-176">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="0b734-177">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="0b734-177">End of client support</span></span><br/>    | <span data-ttu-id="0b734-178">Windows XP</span><span class="sxs-lookup"><span data-stu-id="0b734-178">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="0b734-179">Fine del supporto server</span><span class="sxs-lookup"><span data-stu-id="0b734-179">End of server support</span></span><br/>    | <span data-ttu-id="0b734-180">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="0b734-180">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="0b734-181">Intestazione</span><span class="sxs-lookup"><span data-stu-id="0b734-181">Header</span></span><br/>                   | <dl> <span data-ttu-id="0b734-182"><dt>Scardssp. h</dt></span><span class="sxs-lookup"><span data-stu-id="0b734-182"><dt>Scardssp.h</dt></span></span> </dl>   |
| <span data-ttu-id="0b734-183">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="0b734-183">Type library</span></span><br/>             | <dl> <span data-ttu-id="0b734-184"><dt>Scardsrv. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="0b734-184"><dt>Scardsrv.tlb</dt></span></span> </dl> |
| <span data-ttu-id="0b734-185">DLL</span><span class="sxs-lookup"><span data-stu-id="0b734-185">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0b734-186"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0b734-186"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="0b734-187">IID</span><span class="sxs-lookup"><span data-stu-id="0b734-187">IID</span></span><br/>                      | <span data-ttu-id="0b734-188">IID \_ ISCardISO7816 è definito come 53B6AA68-3F56-11D0-916B-00AA00C18068</span><span class="sxs-lookup"><span data-stu-id="0b734-188">IID\_ISCardISO7816 is defined as 53B6AA68-3F56-11D0-916B-00AA00C18068</span></span><br/>        |



## <a name="see-also"></a><span data-ttu-id="0b734-189">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="0b734-189">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0b734-190">**AppendRecord**</span><span class="sxs-lookup"><span data-stu-id="0b734-190">**AppendRecord**</span></span>](iscardiso7816-appendrecord.md)
</dt> <dt>

[<span data-ttu-id="0b734-191">**ISCardISO7816**</span><span class="sxs-lookup"><span data-stu-id="0b734-191">**ISCardISO7816**</span></span>](iscardiso7816.md)
</dt> <dt>

[<span data-ttu-id="0b734-192">**ReadRecord**</span><span class="sxs-lookup"><span data-stu-id="0b734-192">**ReadRecord**</span></span>](iscardiso7816-readrecord.md)
</dt> <dt>

[<span data-ttu-id="0b734-193">**UpdateRecord**</span><span class="sxs-lookup"><span data-stu-id="0b734-193">**UpdateRecord**</span></span>](iscardiso7816-updaterecord.md)
</dt> </dl>

 

 
