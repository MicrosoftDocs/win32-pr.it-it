---
description: Il metodo SelectFile costruisce un comando APDU (Application Protocol Data Unit) che imposta un file elementare corrente all'interno di un canale logico. I comandi successivi possono fare riferimento in modo implicito al file corrente tramite il canale logico.
ms.assetid: cb6231b3-fb1c-4350-8797-9efaa663c21b
title: 'Metodo ISCardISO7816:: SelectFile (scardssp. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardISO7816.SelectFile
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 9bab499d32a65a2e6b4348458ec42328029760ce
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104231715"
---
# <a name="iscardiso7816selectfile-method"></a><span data-ttu-id="a3e87-104">Metodo ISCardISO7816:: SelectFile</span><span class="sxs-lookup"><span data-stu-id="a3e87-104">ISCardISO7816::SelectFile method</span></span>

<span data-ttu-id="a3e87-105">\[Il metodo **SelectFile** è disponibile per l'uso nei sistemi operativi specificati nella sezione requisiti.</span><span class="sxs-lookup"><span data-stu-id="a3e87-105">\[The **SelectFile** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="a3e87-106">Non è disponibile per l'utilizzo in Windows Server 2003 con Service Pack 1 (SP1) e versioni successive, Windows Vista, Windows Server 2008 e versioni successive del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="a3e87-106">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="a3e87-107">I [moduli Smart Card](/previous-versions/windows/desktop/secsmart/smart-card-modules) offrono funzionalità simili.\]</span><span class="sxs-lookup"><span data-stu-id="a3e87-107">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="a3e87-108">Il metodo **SelectFile** costruisce un comando APDU ( [*Application Protocol Data Unit*](../secgloss/a-gly.md) ) che imposta un file elementare corrente all'interno di un canale logico.</span><span class="sxs-lookup"><span data-stu-id="a3e87-108">The **SelectFile** method constructs an [*application protocol data unit*](../secgloss/a-gly.md) (APDU) command that sets a current elementary file within a logical channel.</span></span> <span data-ttu-id="a3e87-109">I comandi successivi possono fare riferimento in modo implicito al file corrente tramite il canale logico.</span><span class="sxs-lookup"><span data-stu-id="a3e87-109">Subsequent commands may implicitly refer to the current file through the logical channel.</span></span>

<span data-ttu-id="a3e87-110">La selezione di una directory (DF) nell'archivio file delle schede, che può essere la radice (MF) del file Store, lo rende il valore DF corrente.</span><span class="sxs-lookup"><span data-stu-id="a3e87-110">Selecting a directory (DF) within the card filestore — which may be the root (MF) of the filestore — makes it the current DF.</span></span> <span data-ttu-id="a3e87-111">Dopo questa selezione, è possibile fare riferimento a un file elementare corrente implicito tramite il canale logico.</span><span class="sxs-lookup"><span data-stu-id="a3e87-111">After such a selection, an implicit current elementary file may be referred to through that logical channel.</span></span>

<span data-ttu-id="a3e87-112">Selezionando un file elementare, il file selezionato e il relativo padre vengono impostati come file correnti.</span><span class="sxs-lookup"><span data-stu-id="a3e87-112">Selecting an elementary file sets the selected file and its parent as current files.</span></span>

<span data-ttu-id="a3e87-113">Dopo la reimpostazione della risposta, MF viene selezionato in modo implicito tramite il canale logico di base, a meno che non venga specificato diversamente nei byte cronologici o nella stringa di dati iniziale.</span><span class="sxs-lookup"><span data-stu-id="a3e87-113">After the answer to reset, the MF is implicitly selected through the basic logical channel, unless specified differently in the historical bytes or in the initial data string.</span></span>

## <a name="syntax"></a><span data-ttu-id="a3e87-114">Sintassi</span><span class="sxs-lookup"><span data-stu-id="a3e87-114">Syntax</span></span>


```C++
HRESULT SelectFile(
  [in]      BYTE         byP1,
  [in]      BYTE         byP2,
  [in]      LPBYTEBUFFER pData,
  [in]      LONG         lBytesToRead,
  [in, out] LPSCARDCMD   *ppCmd
);
```



## <a name="parameters"></a><span data-ttu-id="a3e87-115">Parametri</span><span class="sxs-lookup"><span data-stu-id="a3e87-115">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a3e87-116">*byP1* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a3e87-116">*byP1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a3e87-117">Controllo di selezione.</span><span class="sxs-lookup"><span data-stu-id="a3e87-117">Selection control.</span></span>



| <span data-ttu-id="a3e87-118">P1 (byte superiore in Word): 8 7 6 5 4 3 2 1</span><span class="sxs-lookup"><span data-stu-id="a3e87-118">P1 (upper byte in word): 8 7 6 5 4 3 2 1</span></span>                                                                                                                                                            | <span data-ttu-id="a3e87-119">Significato</span><span class="sxs-lookup"><span data-stu-id="a3e87-119">Meaning</span></span>                            |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------|
| <span id="000000xx"></span><span id="000000XX"></span><dl> <span data-ttu-id="a3e87-120"><dt>**000000XX**</dt><dt></dt></span><span class="sxs-lookup"><span data-stu-id="a3e87-120"><dt>**000000xx**</dt> <dt></dt></span></span> </dl> | <span data-ttu-id="a3e87-121">Seleziona ID file</span><span class="sxs-lookup"><span data-stu-id="a3e87-121">Select File ID</span></span><br/>          |
| <span id="00000000"></span><dl> <span data-ttu-id="a3e87-122"><dt>**00000000**</dt><dt></dt></span><span class="sxs-lookup"><span data-stu-id="a3e87-122"><dt>**00000000**</dt> <dt></dt></span></span> </dl>                            | <span data-ttu-id="a3e87-123">EF, DF o MF</span><span class="sxs-lookup"><span data-stu-id="a3e87-123">EF, DF, or MF</span></span><br/>           |
| <span id="00000001"></span><dl> <span data-ttu-id="a3e87-124"><dt>**00000001**</dt><dt></dt></span><span class="sxs-lookup"><span data-stu-id="a3e87-124"><dt>**00000001**</dt> <dt></dt></span></span> </dl>                            | <span data-ttu-id="a3e87-125">DF figlio</span><span class="sxs-lookup"><span data-stu-id="a3e87-125">Child DF</span></span><br/>                |
| <span id="00000010"></span><dl> <span data-ttu-id="a3e87-126"><dt>**00000010**</dt><dt></dt></span><span class="sxs-lookup"><span data-stu-id="a3e87-126"><dt>**00000010**</dt> <dt></dt></span></span> </dl>                            | <span data-ttu-id="a3e87-127">EF in DF</span><span class="sxs-lookup"><span data-stu-id="a3e87-127">EF under DF</span></span><br/>             |
| <span id="00000011"></span><dl> <span data-ttu-id="a3e87-128"><dt>**00000011**</dt><dt></dt></span><span class="sxs-lookup"><span data-stu-id="a3e87-128"><dt>**00000011**</dt> <dt></dt></span></span> </dl>                            | <span data-ttu-id="a3e87-129">DF padre del DF corrente</span><span class="sxs-lookup"><span data-stu-id="a3e87-129">Parent DF of current DF</span></span><br/> |



 

<span data-ttu-id="a3e87-130">Quando P1 = 00, la scheda è nota a causa di una specifica codifica dell'ID file o a causa del contesto di esecuzione del comando se il file da selezionare è MF, DF o EF.</span><span class="sxs-lookup"><span data-stu-id="a3e87-130">When P1=00, the card knows either because of a specific coding of the file ID or because of the context of execution of the command if the file to select is the MF, a DF, or an EF.</span></span>

<span data-ttu-id="a3e87-131">Quando P1-P2 = 0000, se viene fornito un ID file, deve essere univoco negli ambienti seguenti:</span><span class="sxs-lookup"><span data-stu-id="a3e87-131">When P1-P2=0000, if a file ID is provided, then it shall be unique in the following environments:</span></span>

-   <span data-ttu-id="a3e87-132">Elementi figlio immediati del DF corrente</span><span class="sxs-lookup"><span data-stu-id="a3e87-132">Immediate children of the current DF</span></span>
-   <span data-ttu-id="a3e87-133">DF padre</span><span class="sxs-lookup"><span data-stu-id="a3e87-133">Parent DF</span></span>
-   <span data-ttu-id="a3e87-134">Elementi figlio immediati del DF padre</span><span class="sxs-lookup"><span data-stu-id="a3e87-134">Immediate children of the parent DF</span></span>

<span data-ttu-id="a3e87-135">Se P1-P2 = 0000 e il campo dati è vuoto o uguale a 3F00, selezionare MF.</span><span class="sxs-lookup"><span data-stu-id="a3e87-135">If P1-P2=0000 and if the data field is empty or equal to 3F00, then select the MF.</span></span>

<span data-ttu-id="a3e87-136">Quando P1 = 04, il campo dati è un nome DF, probabilmente troncato a destra.</span><span class="sxs-lookup"><span data-stu-id="a3e87-136">When P1=04, the data field is a DF name, possibly right truncated.</span></span>

<span data-ttu-id="a3e87-137">Se supportato, i comandi successivi con lo stesso campo dati dovranno selezionare DFs i cui nomi corrispondono a quelli del campo dati, ovvero iniziano con il campo dati del comando.</span><span class="sxs-lookup"><span data-stu-id="a3e87-137">When supported, successive such commands with the same data field shall select DFs whose names match with the data field (that is, start with the command data field).</span></span> <span data-ttu-id="a3e87-138">Se la scheda accetta il comando con un campo dati vuoto, è possibile selezionare in successione tutti o un subset del DFs.</span><span class="sxs-lookup"><span data-stu-id="a3e87-138">If the card accepts the command with an empty data field, then all or a subset of the DFs can be successively selected.</span></span>

</dd> <dt>

<span data-ttu-id="a3e87-139">*byP2* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a3e87-139">*byP2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a3e87-140">Controllo di selezione.</span><span class="sxs-lookup"><span data-stu-id="a3e87-140">Selection control.</span></span>

</dd> <dt>

<span data-ttu-id="a3e87-141">*pData* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a3e87-141">*pData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a3e87-142">Dati per l'operazione, se necessario; altrimenti, **null**.</span><span class="sxs-lookup"><span data-stu-id="a3e87-142">Data for operation if needed; else, **NULL**.</span></span> <span data-ttu-id="a3e87-143">I tipi di dati passati in questo parametro includono:</span><span class="sxs-lookup"><span data-stu-id="a3e87-143">Types of data that are passed in this parameter include:</span></span>

-   <span data-ttu-id="a3e87-144">ID file</span><span class="sxs-lookup"><span data-stu-id="a3e87-144">file ID</span></span>
-   <span data-ttu-id="a3e87-145">percorso da MF</span><span class="sxs-lookup"><span data-stu-id="a3e87-145">path from the MF</span></span>
-   <span data-ttu-id="a3e87-146">percorso dal DF corrente</span><span class="sxs-lookup"><span data-stu-id="a3e87-146">path from the current DF</span></span>
-   <span data-ttu-id="a3e87-147">Nome DF</span><span class="sxs-lookup"><span data-stu-id="a3e87-147">DF name</span></span>

</dd> <dt>

<span data-ttu-id="a3e87-148">*lBytesToRead* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a3e87-148">*lBytesToRead* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a3e87-149">Vuoto (ovvero 0) o lunghezza massima dei dati previsti nella risposta.</span><span class="sxs-lookup"><span data-stu-id="a3e87-149">Empty (that is, 0) or maximum length of data expected in response.</span></span>

</dd> <dt>

<span data-ttu-id="a3e87-150">*ppCmd* \[ in uscita\]</span><span class="sxs-lookup"><span data-stu-id="a3e87-150">*ppCmd* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="a3e87-151">In input, un puntatore a un oggetto di interfaccia [**ISCardCmd**](iscardcmd.md) o **null**.</span><span class="sxs-lookup"><span data-stu-id="a3e87-151">On input, a pointer to an [**ISCardCmd**](iscardcmd.md) interface object or **NULL**.</span></span>

<span data-ttu-id="a3e87-152">Al ritorno, viene compilato con il comando APDU creato da questa operazione.</span><span class="sxs-lookup"><span data-stu-id="a3e87-152">On return, it is filled with the APDU command constructed by this operation.</span></span> <span data-ttu-id="a3e87-153">Se *ppCmd* è stato impostato su **null**, un oggetto [**ISCardCmd**](iscardcmd.md) della [*Smart Card*](../secgloss/s-gly.md) viene creato e restituito internamente tramite il puntatore *ppCmd* .</span><span class="sxs-lookup"><span data-stu-id="a3e87-153">If *ppCmd* was set to **NULL**, a [*smart card*](../secgloss/s-gly.md) [**ISCardCmd**](iscardcmd.md) object is internally created and returned via the *ppCmd* pointer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a3e87-154">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="a3e87-154">Return value</span></span>

<span data-ttu-id="a3e87-155">Il metodo restituisce uno dei valori possibili seguenti.</span><span class="sxs-lookup"><span data-stu-id="a3e87-155">The method returns one of the following possible values.</span></span>



| <span data-ttu-id="a3e87-156">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="a3e87-156">Return code</span></span>                                                                                   | <span data-ttu-id="a3e87-157">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a3e87-157">Description</span></span>                                  |
|-----------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="a3e87-158"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="a3e87-158"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="a3e87-159">Operazione completata correttamente.</span><span class="sxs-lookup"><span data-stu-id="a3e87-159">Operation completed successfully.</span></span><br/> |
| <dl> <span data-ttu-id="a3e87-160"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="a3e87-160"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="a3e87-161">Parametro non valido.</span><span class="sxs-lookup"><span data-stu-id="a3e87-161">Invalid parameter.</span></span><br/>                |
| <dl> <span data-ttu-id="a3e87-162"><dt>**\_puntatore E**</dt></span><span class="sxs-lookup"><span data-stu-id="a3e87-162"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="a3e87-163">È stato passato un puntatore non valido.</span><span class="sxs-lookup"><span data-stu-id="a3e87-163">A bad pointer was passed in.</span></span><br/>      |
| <dl> <span data-ttu-id="a3e87-164"><dt>**E \_ OutOfMemory**</dt></span><span class="sxs-lookup"><span data-stu-id="a3e87-164"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="a3e87-165">Memoria insufficiente.</span><span class="sxs-lookup"><span data-stu-id="a3e87-165">Out of memory.</span></span><br/>                    |



 

## <a name="remarks"></a><span data-ttu-id="a3e87-166">Commenti</span><span class="sxs-lookup"><span data-stu-id="a3e87-166">Remarks</span></span>

<span data-ttu-id="a3e87-167">Se non diversamente specificato, l'esecuzione corretta del comando incapsulato modifica lo stato di sicurezza in base alle regole seguenti:</span><span class="sxs-lookup"><span data-stu-id="a3e87-167">Unless otherwise specified, the correct execution of the encapsulated command modifies the security status according to the following rules:</span></span>

-   <span data-ttu-id="a3e87-168">Quando il file elementare corrente viene modificato o quando non è presente alcun file elementare corrente, lo stato di sicurezza specifico di un precedente file elementare corrente viene perso.</span><span class="sxs-lookup"><span data-stu-id="a3e87-168">When the current elementary file is changed, or when there is no current elementary file, the security status specific to a former current elementary file is lost.</span></span>
-   <span data-ttu-id="a3e87-169">Quando la directory FileStore corrente (DF) è discendente di o identica alla precedente DF corrente, lo stato di sicurezza specifico del DF corrente viene perso.</span><span class="sxs-lookup"><span data-stu-id="a3e87-169">When the current filestore directory (DF) is descendant of, or identical to the former current DF, the security status specific to the former current DF is lost.</span></span> <span data-ttu-id="a3e87-170">Viene mantenuto lo stato di sicurezza comune a tutti i predecessori comuni del nuovo DF corrente.</span><span class="sxs-lookup"><span data-stu-id="a3e87-170">The security status common to all common ancestors of the previous and new current DF is maintained.</span></span>

<span data-ttu-id="a3e87-171">Per un elenco di tutti i metodi forniti da questa interfaccia, vedere [**ISCardISO7816**](iscardiso7816.md).</span><span class="sxs-lookup"><span data-stu-id="a3e87-171">For a list of all the methods provided by this interface, see [**ISCardISO7816**](iscardiso7816.md).</span></span>

<span data-ttu-id="a3e87-172">Oltre ai codici di errore COM elencati sopra, questa interfaccia può restituire un codice di errore della smart card se è stata chiamata una funzione Smart Card per completare la richiesta.</span><span class="sxs-lookup"><span data-stu-id="a3e87-172">In addition to the COM error codes listed above, this interface may return a smart card error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="a3e87-173">Per ulteriori informazioni, vedere [valori restituiti della smart card](authentication-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="a3e87-173">For more information, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="a3e87-174">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a3e87-174">Requirements</span></span>



| <span data-ttu-id="a3e87-175">Requisito</span><span class="sxs-lookup"><span data-stu-id="a3e87-175">Requirement</span></span> | <span data-ttu-id="a3e87-176">Valore</span><span class="sxs-lookup"><span data-stu-id="a3e87-176">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a3e87-177">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a3e87-177">Minimum supported client</span></span><br/> | <span data-ttu-id="a3e87-178">\[Solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="a3e87-178">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="a3e87-179">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a3e87-179">Minimum supported server</span></span><br/> | <span data-ttu-id="a3e87-180">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="a3e87-180">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="a3e87-181">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="a3e87-181">End of client support</span></span><br/>    | <span data-ttu-id="a3e87-182">Windows XP</span><span class="sxs-lookup"><span data-stu-id="a3e87-182">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="a3e87-183">Fine del supporto server</span><span class="sxs-lookup"><span data-stu-id="a3e87-183">End of server support</span></span><br/>    | <span data-ttu-id="a3e87-184">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="a3e87-184">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="a3e87-185">Intestazione</span><span class="sxs-lookup"><span data-stu-id="a3e87-185">Header</span></span><br/>                   | <dl> <span data-ttu-id="a3e87-186"><dt>Scardssp. h</dt></span><span class="sxs-lookup"><span data-stu-id="a3e87-186"><dt>Scardssp.h</dt></span></span> </dl>   |
| <span data-ttu-id="a3e87-187">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="a3e87-187">Type library</span></span><br/>             | <dl> <span data-ttu-id="a3e87-188"><dt>Scardsrv. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="a3e87-188"><dt>Scardsrv.tlb</dt></span></span> </dl> |
| <span data-ttu-id="a3e87-189">DLL</span><span class="sxs-lookup"><span data-stu-id="a3e87-189">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a3e87-190"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a3e87-190"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="a3e87-191">IID</span><span class="sxs-lookup"><span data-stu-id="a3e87-191">IID</span></span><br/>                      | <span data-ttu-id="a3e87-192">IID \_ ISCardISO7816 è definito come 53B6AA68-3F56-11D0-916B-00AA00C18068</span><span class="sxs-lookup"><span data-stu-id="a3e87-192">IID\_ISCardISO7816 is defined as 53B6AA68-3F56-11D0-916B-00AA00C18068</span></span><br/>        |



## <a name="see-also"></a><span data-ttu-id="a3e87-193">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a3e87-193">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a3e87-194">**ISCardISO7816**</span><span class="sxs-lookup"><span data-stu-id="a3e87-194">**ISCardISO7816**</span></span>](iscardiso7816.md)
</dt> </dl>

 

 
