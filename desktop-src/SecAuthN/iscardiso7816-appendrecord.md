---
description: Il metodo AppendRecord costruisce un comando APDU (Application Protocol Data Unit) che accoda un record alla fine di un file Elementary con struttura lineare o scrive il numero di record 1 in un file elementare con struttura ciclica.
ms.assetid: 4dd88661-41c4-4238-88c9-279b39afb206
title: 'Metodo ISCardISO7816:: AppendRecord (scardssp. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardISO7816.AppendRecord
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 28d1b6762e0a350bb87b673f21fa063ae2478e64
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104226602"
---
# <a name="iscardiso7816appendrecord-method"></a><span data-ttu-id="74666-103">Metodo ISCardISO7816:: AppendRecord</span><span class="sxs-lookup"><span data-stu-id="74666-103">ISCardISO7816::AppendRecord method</span></span>

<span data-ttu-id="74666-104">\[Il metodo **AppendRecord** è disponibile per l'uso nei sistemi operativi specificati nella sezione requisiti.</span><span class="sxs-lookup"><span data-stu-id="74666-104">\[The **AppendRecord** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="74666-105">Non è disponibile per l'utilizzo in Windows Server 2003 con Service Pack 1 (SP1) e versioni successive, Windows Vista, Windows Server 2008 e versioni successive del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="74666-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="74666-106">I [moduli Smart Card](/previous-versions/windows/desktop/secsmart/smart-card-modules) offrono funzionalità simili.\]</span><span class="sxs-lookup"><span data-stu-id="74666-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="74666-107">Il metodo **AppendRecord** costruisce un comando APDU ( [*Application Protocol Data Unit*](../secgloss/a-gly.md) ) che accoda un record alla fine di un file Elementary con struttura lineare o scrive il numero di record 1 in un file elementare con struttura ciclica.</span><span class="sxs-lookup"><span data-stu-id="74666-107">The **AppendRecord** method constructs an [*application protocol data unit*](../secgloss/a-gly.md) (APDU) command that either appends a record to the end of a linear-structured elementary file (EF) or writes record number 1 in a cyclic-structured elementary file.</span></span>

## <a name="syntax"></a><span data-ttu-id="74666-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="74666-108">Syntax</span></span>


```C++
HRESULT AppendRecord(
  [in]      BYTE         byRefCtrl,
  [in]      LPBYTEBUFFER pData,
  [in, out] LPSCARDCMD   *ppCmd
);
```



## <a name="parameters"></a><span data-ttu-id="74666-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="74666-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="74666-110">*byRefCtrl* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="74666-110">*byRefCtrl* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="74666-111">Identifica il file elementare da accodare.</span><span class="sxs-lookup"><span data-stu-id="74666-111">Identifies the elementary file to be appended.</span></span>



| <span data-ttu-id="74666-112">Valore</span><span class="sxs-lookup"><span data-stu-id="74666-112">Value</span></span>                                                                                                                                                                                | <span data-ttu-id="74666-113">Significato</span><span class="sxs-lookup"><span data-stu-id="74666-113">Meaning</span></span>                           |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------|
| <span id="Current_EF"></span><span id="current_ef"></span><span id="CURRENT_EF"></span><dl> <span data-ttu-id="74666-114"><dt>**EF corrente**</dt></span><span class="sxs-lookup"><span data-stu-id="74666-114"><dt>**Current EF**</dt></span></span> </dl>     | <span data-ttu-id="74666-115">Posizione bit: 00000000</span><span class="sxs-lookup"><span data-stu-id="74666-115">Bit position: 00000000</span></span><br/> |
| <span id="Short_EF_ID"></span><span id="short_ef_id"></span><span id="SHORT_EF_ID"></span><dl> <span data-ttu-id="74666-116"><dt>**ID EF breve**</dt></span><span class="sxs-lookup"><span data-stu-id="74666-116"><dt>**Short EF ID**</dt></span></span> </dl> | <span data-ttu-id="74666-117">Posizione bit: XXXXX000</span><span class="sxs-lookup"><span data-stu-id="74666-117">Bit position: xxxxx000</span></span><br/> |
| <span id="Reserved"></span><span id="reserved"></span><span id="RESERVED"></span><dl> <span data-ttu-id="74666-118"><dt>**Riservato**</dt></span><span class="sxs-lookup"><span data-stu-id="74666-118"><dt>**Reserved**</dt></span></span> </dl>             | <span data-ttu-id="74666-119">Posizione bit: xxxxxxxx</span><span class="sxs-lookup"><span data-stu-id="74666-119">Bit position: xxxxxxxx</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="74666-120">*pData* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="74666-120">*pData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="74666-121">Puntatore ai dati da accodare al file.</span><span class="sxs-lookup"><span data-stu-id="74666-121">A pointer to the data to be appended to the file.</span></span>



| <span data-ttu-id="74666-122">Valore</span><span class="sxs-lookup"><span data-stu-id="74666-122">Value</span></span>                                                                                                                                                | <span data-ttu-id="74666-123">Significato</span><span class="sxs-lookup"><span data-stu-id="74666-123">Meaning</span></span>                 |
|------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------|
| <span id="Tn"></span><span id="tn"></span><span id="TN"></span><dl> <span data-ttu-id="74666-124"><dt>**TN**</dt></span><span class="sxs-lookup"><span data-stu-id="74666-124"><dt>**Tn**</dt></span></span> </dl>     | <span data-ttu-id="74666-125">1 byte</span><span class="sxs-lookup"><span data-stu-id="74666-125">1 byte</span></span><br/>       |
| <span id="Ln_"></span><span id="ln_"></span><span id="LN_"></span><dl> <span data-ttu-id="74666-126"><dt>**LN**</dt></span><span class="sxs-lookup"><span data-stu-id="74666-126"><dt>**Ln** </dt></span></span> </dl> | <span data-ttu-id="74666-127">1 o 3 byte</span><span class="sxs-lookup"><span data-stu-id="74666-127">1 or 3 bytes</span></span><br/> |
| <span id="data"></span><span id="DATA"></span><dl> <span data-ttu-id="74666-128"><dt>**dati**</dt></span><span class="sxs-lookup"><span data-stu-id="74666-128"><dt>**data**</dt></span></span> </dl>                    | <span data-ttu-id="74666-129">Ln byte</span><span class="sxs-lookup"><span data-stu-id="74666-129">Ln bytes</span></span><br/>     |



 

</dd> <dt>

<span data-ttu-id="74666-130">*ppCmd* \[ in uscita\]</span><span class="sxs-lookup"><span data-stu-id="74666-130">*ppCmd* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="74666-131">In input, un puntatore a un oggetto di interfaccia [**ISCardCmd**](iscardcmd.md) o **null**.</span><span class="sxs-lookup"><span data-stu-id="74666-131">On input, a pointer to an [**ISCardCmd**](iscardcmd.md) interface object or **NULL**.</span></span>

<span data-ttu-id="74666-132">Al ritorno, viene compilato con il comando APDU creato da questa operazione.</span><span class="sxs-lookup"><span data-stu-id="74666-132">On return, it is filled with the APDU command constructed by this operation.</span></span> <span data-ttu-id="74666-133">Se *ppCmd* è stato impostato su **null**, un oggetto [**ISCardCmd**](iscardcmd.md) della [*Smart Card*](../secgloss/s-gly.md) viene creato e restituito internamente utilizzando il puntatore *ppCmd* .</span><span class="sxs-lookup"><span data-stu-id="74666-133">If *ppCmd* was set to **NULL**, a [*smart card*](../secgloss/s-gly.md) [**ISCardCmd**](iscardcmd.md) object is internally created and returned by using the *ppCmd* pointer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="74666-134">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="74666-134">Return value</span></span>

<span data-ttu-id="74666-135">Il metodo restituisce uno dei valori possibili seguenti.</span><span class="sxs-lookup"><span data-stu-id="74666-135">The method returns one of the following possible values.</span></span>



| <span data-ttu-id="74666-136">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="74666-136">Return code</span></span>                                                                                   | <span data-ttu-id="74666-137">Descrizione</span><span class="sxs-lookup"><span data-stu-id="74666-137">Description</span></span>                                  |
|-----------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="74666-138"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="74666-138"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="74666-139">Operazione completata correttamente.</span><span class="sxs-lookup"><span data-stu-id="74666-139">Operation completed successfully.</span></span><br/> |
| <dl> <span data-ttu-id="74666-140"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="74666-140"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="74666-141">Parametro non valido.</span><span class="sxs-lookup"><span data-stu-id="74666-141">Invalid parameter.</span></span><br/>                |
| <dl> <span data-ttu-id="74666-142"><dt>**\_puntatore E**</dt></span><span class="sxs-lookup"><span data-stu-id="74666-142"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="74666-143">È stato passato un puntatore non valido.</span><span class="sxs-lookup"><span data-stu-id="74666-143">A bad pointer was passed in.</span></span><br/>      |
| <dl> <span data-ttu-id="74666-144"><dt>**E \_ OutOfMemory**</dt></span><span class="sxs-lookup"><span data-stu-id="74666-144"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="74666-145">Memoria insufficiente.</span><span class="sxs-lookup"><span data-stu-id="74666-145">Out of memory.</span></span><br/>                    |



 

## <a name="remarks"></a><span data-ttu-id="74666-146">Commenti</span><span class="sxs-lookup"><span data-stu-id="74666-146">Remarks</span></span>

<span data-ttu-id="74666-147">Il comando incapsulato può essere eseguito solo se lo stato di sicurezza della [*Smart Card*](../secgloss/s-gly.md) soddisfa gli attributi di sicurezza del file elementare letto.</span><span class="sxs-lookup"><span data-stu-id="74666-147">The encapsulated command can only be performed if the security status of the [*smart card*](../secgloss/s-gly.md) satisfies the security attributes of the elementary file read.</span></span>

<span data-ttu-id="74666-148">Se al momento dell'invio di questo comando è selezionato un altro file elementare, è possibile che venga elaborato senza l'identificazione del file attualmente selezionato.</span><span class="sxs-lookup"><span data-stu-id="74666-148">If another elementary file is selected at the time of issuing this command, it may be processed without identification of the currently selected file.</span></span>

<span data-ttu-id="74666-149">Non è possibile leggere i file elementari senza una struttura di record.</span><span class="sxs-lookup"><span data-stu-id="74666-149">Elementary files without a record structure cannot be read.</span></span> <span data-ttu-id="74666-150">Il comando incapsulato viene interrotto se applicato a un file elementare senza una struttura di record.</span><span class="sxs-lookup"><span data-stu-id="74666-150">The encapsulated command aborts if applied to an elementary file without a record structure.</span></span>

<span data-ttu-id="74666-151">Per un elenco di tutti i metodi forniti da questa interfaccia, vedere [**ISCardISO7816**](iscardiso7816.md).</span><span class="sxs-lookup"><span data-stu-id="74666-151">For a list of all the methods provided by this interface, see [**ISCardISO7816**](iscardiso7816.md).</span></span>

<span data-ttu-id="74666-152">Oltre ai codici di errore COM elencati sopra, questa interfaccia può restituire un codice di errore della smart card se è stata chiamata una funzione Smart Card per completare la richiesta.</span><span class="sxs-lookup"><span data-stu-id="74666-152">In addition to the COM error codes listed above, this interface may return a smart card error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="74666-153">Per ulteriori informazioni, vedere [valori restituiti della smart card](authentication-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="74666-153">For more information, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="74666-154">Requisiti</span><span class="sxs-lookup"><span data-stu-id="74666-154">Requirements</span></span>



| <span data-ttu-id="74666-155">Requisito</span><span class="sxs-lookup"><span data-stu-id="74666-155">Requirement</span></span> | <span data-ttu-id="74666-156">Valore</span><span class="sxs-lookup"><span data-stu-id="74666-156">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="74666-157">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="74666-157">Minimum supported client</span></span><br/> | <span data-ttu-id="74666-158">\[Solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="74666-158">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="74666-159">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="74666-159">Minimum supported server</span></span><br/> | <span data-ttu-id="74666-160">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="74666-160">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="74666-161">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="74666-161">End of client support</span></span><br/>    | <span data-ttu-id="74666-162">Windows XP</span><span class="sxs-lookup"><span data-stu-id="74666-162">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="74666-163">Fine del supporto server</span><span class="sxs-lookup"><span data-stu-id="74666-163">End of server support</span></span><br/>    | <span data-ttu-id="74666-164">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="74666-164">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="74666-165">Intestazione</span><span class="sxs-lookup"><span data-stu-id="74666-165">Header</span></span><br/>                   | <dl> <span data-ttu-id="74666-166"><dt>Scardssp. h</dt></span><span class="sxs-lookup"><span data-stu-id="74666-166"><dt>Scardssp.h</dt></span></span> </dl>   |
| <span data-ttu-id="74666-167">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="74666-167">Type library</span></span><br/>             | <dl> <span data-ttu-id="74666-168"><dt>Scardsrv. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="74666-168"><dt>Scardsrv.tlb</dt></span></span> </dl> |
| <span data-ttu-id="74666-169">DLL</span><span class="sxs-lookup"><span data-stu-id="74666-169">DLL</span></span><br/>                      | <dl> <span data-ttu-id="74666-170"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="74666-170"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="74666-171">IID</span><span class="sxs-lookup"><span data-stu-id="74666-171">IID</span></span><br/>                      | <span data-ttu-id="74666-172">IID \_ ISCardISO7816 è definito come 53B6AA68-3F56-11D0-916B-00AA00C18068</span><span class="sxs-lookup"><span data-stu-id="74666-172">IID\_ISCardISO7816 is defined as 53B6AA68-3F56-11D0-916B-00AA00C18068</span></span><br/>        |



## <a name="see-also"></a><span data-ttu-id="74666-173">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="74666-173">See also</span></span>

<dl> <dt>

[<span data-ttu-id="74666-174">**ISCardISO7816**</span><span class="sxs-lookup"><span data-stu-id="74666-174">**ISCardISO7816**</span></span>](iscardiso7816.md)
</dt> <dt>

[<span data-ttu-id="74666-175">**ReadRecord**</span><span class="sxs-lookup"><span data-stu-id="74666-175">**ReadRecord**</span></span>](iscardiso7816-readrecord.md)
</dt> <dt>

[<span data-ttu-id="74666-176">**UpdateRecord**</span><span class="sxs-lookup"><span data-stu-id="74666-176">**UpdateRecord**</span></span>](iscardiso7816-updaterecord.md)
</dt> <dt>

[<span data-ttu-id="74666-177">**WriteRecord**</span><span class="sxs-lookup"><span data-stu-id="74666-177">**WriteRecord**</span></span>](iscardiso7816-writerecord.md)
</dt> </dl>

 

 
