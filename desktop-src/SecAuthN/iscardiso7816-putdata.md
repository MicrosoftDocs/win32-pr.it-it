---
description: Il metodo PutData costruisce un comando APDU (Application Protocol Data Unit) che archivia un singolo oggetto dati primitivo o il set di oggetti dati contenuti in un oggetto dati costruito, a seconda del file selezionato.
ms.assetid: 6bad45fb-b202-4eb0-b2f4-fe0a6af64330
title: Metodo ISCardISO7816::P utData (scardssp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardISO7816.PutData
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 3c15239943a92067011011b6cedca191fa78c3a8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103883641"
---
# <a name="iscardiso7816putdata-method"></a><span data-ttu-id="42caf-103">ISCardISO7816::P metodo utData</span><span class="sxs-lookup"><span data-stu-id="42caf-103">ISCardISO7816::PutData method</span></span>

<span data-ttu-id="42caf-104">\[Il metodo **PutData** è disponibile per l'uso nei sistemi operativi specificati nella sezione requisiti.</span><span class="sxs-lookup"><span data-stu-id="42caf-104">\[The **PutData** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="42caf-105">Non è disponibile per l'utilizzo in Windows Server 2003 con Service Pack 1 (SP1) e versioni successive, Windows Vista, Windows Server 2008 e versioni successive del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="42caf-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="42caf-106">I [moduli Smart Card](/previous-versions/windows/desktop/secsmart/smart-card-modules) offrono funzionalità simili.\]</span><span class="sxs-lookup"><span data-stu-id="42caf-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="42caf-107">Il metodo **PutData** costruisce un comando APDU ( [*Application Protocol Data Unit*](../secgloss/a-gly.md) ) che archivia un singolo oggetto dati primitivo o il set di oggetti dati contenuti in un oggetto dati costruito, a seconda del file selezionato.</span><span class="sxs-lookup"><span data-stu-id="42caf-107">The **PutData** method constructs an [*application protocol data unit*](../secgloss/a-gly.md) (APDU) command that stores a single primitive data object or the set of data objects contained in a constructed data object, depending on the file selected.</span></span>

<span data-ttu-id="42caf-108">La modalità di archiviazione degli oggetti, ovvero la scrittura di una sola volta e/o l'aggiornamento e/o l'accodamento, dipende dalla definizione o dalla natura degli oggetti dati.</span><span class="sxs-lookup"><span data-stu-id="42caf-108">How the objects are stored (writing once and/or updating and/or appending) depends on the definition or the nature of the data objects.</span></span>

## <a name="syntax"></a><span data-ttu-id="42caf-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="42caf-109">Syntax</span></span>


```C++
HRESULT PutData(
  [in]      BYTE         byP1,
  [in]      BYTE         byP2,
  [in]      LPBYTEBUFFER pData,
  [in, out] LPSCARDCMD   *ppCmd
);
```



## <a name="parameters"></a><span data-ttu-id="42caf-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="42caf-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="42caf-111">*byP1* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="42caf-111">*byP1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="42caf-112">Codifica di P1-P2.</span><span class="sxs-lookup"><span data-stu-id="42caf-112">Coding of P1-P2.</span></span>



| <span data-ttu-id="42caf-113">Valore</span><span class="sxs-lookup"><span data-stu-id="42caf-113">Value</span></span>                                                                                  | <span data-ttu-id="42caf-114">Significato</span><span class="sxs-lookup"><span data-stu-id="42caf-114">Meaning</span></span>                                          |
|----------------------------------------------------------------------------------------|--------------------------------------------------|
| <dl> <span data-ttu-id="42caf-115"><dt>0000-003F</dt></span><span class="sxs-lookup"><span data-stu-id="42caf-115"><dt>0000 - 003F</dt></span></span> </dl> | <span data-ttu-id="42caf-116">RFU</span><span class="sxs-lookup"><span data-stu-id="42caf-116">RFU</span></span><br/>                                   |
| <dl> <span data-ttu-id="42caf-117"><dt>0040-00FF</dt></span><span class="sxs-lookup"><span data-stu-id="42caf-117"><dt>0040 - 00FF</dt></span></span> </dl> | <span data-ttu-id="42caf-118">Tag BER-TLV (1 byte) in P2</span><span class="sxs-lookup"><span data-stu-id="42caf-118">BER-TLV tag (1 byte) in P2</span></span><br/>            |
| <dl> <span data-ttu-id="42caf-119"><dt>0100-01FF</dt></span><span class="sxs-lookup"><span data-stu-id="42caf-119"><dt>0100 - 01FF</dt></span></span> </dl> | <span data-ttu-id="42caf-120">Dati applicazione (codifica proprietaria)</span><span class="sxs-lookup"><span data-stu-id="42caf-120">Application data (proprietary coding)</span></span><br/> |
| <dl> <span data-ttu-id="42caf-121"><dt>0200-02FF</dt></span><span class="sxs-lookup"><span data-stu-id="42caf-121"><dt>0200 - 02FF</dt></span></span> </dl> | <span data-ttu-id="42caf-122">SEMPLICE tag TLV in P2</span><span class="sxs-lookup"><span data-stu-id="42caf-122">SIMPLE-TLV tag in P2</span></span><br/>                  |
| <dl> <span data-ttu-id="42caf-123"><dt>0300-03FF</dt></span><span class="sxs-lookup"><span data-stu-id="42caf-123"><dt>0300 - 03FF</dt></span></span> </dl> | <span data-ttu-id="42caf-124">RFU</span><span class="sxs-lookup"><span data-stu-id="42caf-124">RFU</span></span><br/>                                   |
| <dl> <span data-ttu-id="42caf-125"><dt>0400 - 04FF</dt></span><span class="sxs-lookup"><span data-stu-id="42caf-125"><dt>0400 - 04FF</dt></span></span> </dl> | <span data-ttu-id="42caf-126">Tag BER-TLV (2 byte) in P1-P2</span><span class="sxs-lookup"><span data-stu-id="42caf-126">BER-TLV tag (2 bytes) in P1-P2</span></span><br/>        |



 

</dd> <dt>

<span data-ttu-id="42caf-127">*byP2* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="42caf-127">*byP2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="42caf-128">Codifica di P1-P2.</span><span class="sxs-lookup"><span data-stu-id="42caf-128">Coding of P1-P2.</span></span>



| <span data-ttu-id="42caf-129">Valore</span><span class="sxs-lookup"><span data-stu-id="42caf-129">Value</span></span>                                                                                  | <span data-ttu-id="42caf-130">Significato</span><span class="sxs-lookup"><span data-stu-id="42caf-130">Meaning</span></span>                                          |
|----------------------------------------------------------------------------------------|--------------------------------------------------|
| <dl> <span data-ttu-id="42caf-131"><dt>0000-003F</dt></span><span class="sxs-lookup"><span data-stu-id="42caf-131"><dt>0000 - 003F</dt></span></span> </dl> | <span data-ttu-id="42caf-132">RFU</span><span class="sxs-lookup"><span data-stu-id="42caf-132">RFU</span></span><br/>                                   |
| <dl> <span data-ttu-id="42caf-133"><dt>0040-00FF</dt></span><span class="sxs-lookup"><span data-stu-id="42caf-133"><dt>0040 - 00FF</dt></span></span> </dl> | <span data-ttu-id="42caf-134">Tag BER-TLV (1 byte) in P2</span><span class="sxs-lookup"><span data-stu-id="42caf-134">BER-TLV tag (1 byte) in P2</span></span><br/>            |
| <dl> <span data-ttu-id="42caf-135"><dt>0100-01FF</dt></span><span class="sxs-lookup"><span data-stu-id="42caf-135"><dt>0100 - 01FF</dt></span></span> </dl> | <span data-ttu-id="42caf-136">Dati applicazione (codifica proprietaria)</span><span class="sxs-lookup"><span data-stu-id="42caf-136">Application data (proprietary coding)</span></span><br/> |
| <dl> <span data-ttu-id="42caf-137"><dt>0200-02FF</dt></span><span class="sxs-lookup"><span data-stu-id="42caf-137"><dt>0200 - 02FF</dt></span></span> </dl> | <span data-ttu-id="42caf-138">SEMPLICE tag TLV in P2</span><span class="sxs-lookup"><span data-stu-id="42caf-138">SIMPLE-TLV tag in P2</span></span><br/>                  |
| <dl> <span data-ttu-id="42caf-139"><dt>0300-03FF</dt></span><span class="sxs-lookup"><span data-stu-id="42caf-139"><dt>0300 - 03FF</dt></span></span> </dl> | <span data-ttu-id="42caf-140">RFU</span><span class="sxs-lookup"><span data-stu-id="42caf-140">RFU</span></span><br/>                                   |
| <dl> <span data-ttu-id="42caf-141"><dt>0400 - 04FF</dt></span><span class="sxs-lookup"><span data-stu-id="42caf-141"><dt>0400 - 04FF</dt></span></span> </dl> | <span data-ttu-id="42caf-142">Tag BER-TLV (2 byte) in P1-P2</span><span class="sxs-lookup"><span data-stu-id="42caf-142">BER-TLV tag (2 bytes) in P1-P2</span></span><br/>        |



 

</dd> <dt>

<span data-ttu-id="42caf-143">*pData* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="42caf-143">*pData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="42caf-144">Puntatore a un buffer di byte che contiene i parametri e i dati da scrivere.</span><span class="sxs-lookup"><span data-stu-id="42caf-144">Pointer to a byte buffer that contains the parameters and data to be written.</span></span>

</dd> <dt>

<span data-ttu-id="42caf-145">*ppCmd* \[ in uscita\]</span><span class="sxs-lookup"><span data-stu-id="42caf-145">*ppCmd* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="42caf-146">In input, un puntatore a un oggetto di interfaccia [**ISCardCmd**](iscardcmd.md) o **null**.</span><span class="sxs-lookup"><span data-stu-id="42caf-146">On input, a pointer to an [**ISCardCmd**](iscardcmd.md) interface object or **NULL**.</span></span>

<span data-ttu-id="42caf-147">Al ritorno, viene compilato con il comando APDU creato da questa operazione.</span><span class="sxs-lookup"><span data-stu-id="42caf-147">On return, it is filled with the APDU command constructed by this operation.</span></span> <span data-ttu-id="42caf-148">Se *ppCmd* è stato impostato su **null**, un oggetto [**ISCardCmd**](iscardcmd.md) della [*Smart Card*](../secgloss/s-gly.md) viene creato e restituito internamente utilizzando il puntatore *ppCmd* .</span><span class="sxs-lookup"><span data-stu-id="42caf-148">If *ppCmd* was set to **NULL**, a [*smart card*](../secgloss/s-gly.md) [**ISCardCmd**](iscardcmd.md) object is internally created and returned using the *ppCmd* pointer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="42caf-149">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="42caf-149">Return value</span></span>

<span data-ttu-id="42caf-150">Il metodo restituisce uno dei valori possibili seguenti.</span><span class="sxs-lookup"><span data-stu-id="42caf-150">The method returns one of the following possible values.</span></span>



| <span data-ttu-id="42caf-151">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="42caf-151">Return code</span></span>                                                                                   | <span data-ttu-id="42caf-152">Descrizione</span><span class="sxs-lookup"><span data-stu-id="42caf-152">Description</span></span>                                  |
|-----------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="42caf-153"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="42caf-153"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="42caf-154">Operazione completata correttamente.</span><span class="sxs-lookup"><span data-stu-id="42caf-154">Operation completed successfully.</span></span><br/> |
| <dl> <span data-ttu-id="42caf-155"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="42caf-155"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="42caf-156">Parametro non valido.</span><span class="sxs-lookup"><span data-stu-id="42caf-156">Invalid parameter.</span></span><br/>                |
| <dl> <span data-ttu-id="42caf-157"><dt>**\_puntatore E**</dt></span><span class="sxs-lookup"><span data-stu-id="42caf-157"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="42caf-158">È stato passato un puntatore non valido.</span><span class="sxs-lookup"><span data-stu-id="42caf-158">A bad pointer was passed in.</span></span><br/>      |
| <dl> <span data-ttu-id="42caf-159"><dt>**E \_ OutOfMemory**</dt></span><span class="sxs-lookup"><span data-stu-id="42caf-159"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="42caf-160">Memoria insufficiente.</span><span class="sxs-lookup"><span data-stu-id="42caf-160">Out of memory.</span></span><br/>                    |



 

## <a name="remarks"></a><span data-ttu-id="42caf-161">Commenti</span><span class="sxs-lookup"><span data-stu-id="42caf-161">Remarks</span></span>

<span data-ttu-id="42caf-162">Il comando può essere eseguito solo se lo stato di sicurezza soddisfa le condizioni di sicurezza definite dall'applicazione nel [*contesto*](../secgloss/c-gly.md) per la funzione.</span><span class="sxs-lookup"><span data-stu-id="42caf-162">The command can be performed only if the security status satisfies the security conditions defined by the application within the [*context*](../secgloss/c-gly.md) for the function.</span></span>

<dl> <dt>

<span data-ttu-id="42caf-163"><span id="Store_Application_Data"></span><span id="store_application_data"></span><span id="STORE_APPLICATION_DATA"></span>Archiviare i dati dell'applicazione</span><span class="sxs-lookup"><span data-stu-id="42caf-163"><span id="Store_Application_Data"></span><span id="store_application_data"></span><span id="STORE_APPLICATION_DATA"></span>Store Application Data</span></span>
</dt> <dd>

<span data-ttu-id="42caf-164">Quando il valore di P1-P2 si trova nell'intervallo compreso tra 0100 e 01FF, il valore di P1-P2 deve essere un identificatore riservato per i test interni delle schede e per i servizi proprietari significativi all'interno di un determinato contesto dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="42caf-164">When the value of P1-P2 lies in the range from 0100 to 01FF, the value of P1-P2 shall be an identifier reserved for card internal tests and for proprietary services meaningful within a given application context.</span></span>

</dd> <dt>

<span data-ttu-id="42caf-165"><span id="Store_Data_Objects"></span><span id="store_data_objects"></span><span id="STORE_DATA_OBJECTS"></span>Archiviare oggetti dati</span><span class="sxs-lookup"><span data-stu-id="42caf-165"><span id="Store_Data_Objects"></span><span id="store_data_objects"></span><span id="STORE_DATA_OBJECTS"></span>Store Data Objects</span></span>
</dt> <dd>

<span data-ttu-id="42caf-166">Quando il valore P1-P2 si trova nell'intervallo compreso tra 0040 e 00FF, il valore di P2 deve essere un tag BER-TLV su un solo byte.</span><span class="sxs-lookup"><span data-stu-id="42caf-166">When the value P1-P2 lies in the range from 0040 to 00FF, the value of P2 shall be a BER-TLV tag on a single byte.</span></span> <span data-ttu-id="42caf-167">Il valore di 00FF è riservato per indicare che il campo dati contiene oggetti dati BER-TLV.</span><span class="sxs-lookup"><span data-stu-id="42caf-167">The value of 00FF is reserved for indicating that the data field carries BER-TLV data objects.</span></span>

<span data-ttu-id="42caf-168">Quando il valore di P1-P2 si trova nell'intervallo compreso tra 0200 e 02FF, il valore di P2 sarà un tag SIMPLE-TLV.</span><span class="sxs-lookup"><span data-stu-id="42caf-168">When the value of P1-P2 lies in the range 0200 to 02FF, the value of P2 shall be a SIMPLE-TLV tag.</span></span> <span data-ttu-id="42caf-169">Il valore 0200 è RFU.</span><span class="sxs-lookup"><span data-stu-id="42caf-169">The value 0200 is RFU.</span></span> <span data-ttu-id="42caf-170">Il valore 02FF è riservato per indicare che il campo dati contiene oggetti dati SIMPLE-TLV.</span><span class="sxs-lookup"><span data-stu-id="42caf-170">The value 02FF is reserved for indicating that the data field carries SIMPLE-TLV data objects.</span></span>

<span data-ttu-id="42caf-171">Quando il valore di P1-P2 si trova nell'intervallo compreso tra 4000 e FFFF, il valore di P1-P2 deve essere un tag BER-TLV su due byte.</span><span class="sxs-lookup"><span data-stu-id="42caf-171">When the value of P1-P2 lies in the range from 4000 to FFFF, the value of P1-P2 shall be a BER-TLV tag on two bytes.</span></span> <span data-ttu-id="42caf-172">I valori da 4000 a FFFF sono RFU.</span><span class="sxs-lookup"><span data-stu-id="42caf-172">The values 4000 to FFFF are RFU.</span></span>

<span data-ttu-id="42caf-173">Quando viene fornito un oggetto dati primitivo, il campo dati del messaggio di comando deve contenere il valore dell'oggetto dati primitivo corrispondente.</span><span class="sxs-lookup"><span data-stu-id="42caf-173">When a primitive data object is provided, the data field of the command message shall contain the value of the corresponding primitive data object.</span></span>

<span data-ttu-id="42caf-174">Quando viene fornito un oggetto dati costruito, il campo dati del messaggio di comando deve contenere il valore dell'oggetto dati costruito, ovvero gli oggetti dati, inclusi il tag, la lunghezza e il valore.</span><span class="sxs-lookup"><span data-stu-id="42caf-174">When a constructed data object is provided, the data field of the command message shall contain the value of the constructed data object (that is, data objects including their tag, length, and value).</span></span>

</dd> </dl>

<span data-ttu-id="42caf-175">Per un elenco di tutti i metodi forniti da questa interfaccia, vedere [**ISCardISO7816**](iscardiso7816.md).</span><span class="sxs-lookup"><span data-stu-id="42caf-175">For a list of all the methods provided by this interface, see [**ISCardISO7816**](iscardiso7816.md).</span></span>

<span data-ttu-id="42caf-176">Oltre ai codici di errore COM elencati sopra, questa interfaccia può restituire un codice di errore della smart card se è stata chiamata una funzione Smart Card per completare la richiesta.</span><span class="sxs-lookup"><span data-stu-id="42caf-176">In addition to the COM error codes listed above, this interface may return a smart card error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="42caf-177">Per ulteriori informazioni, vedere [valori restituiti della smart card](authentication-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="42caf-177">For more information, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="42caf-178">Requisiti</span><span class="sxs-lookup"><span data-stu-id="42caf-178">Requirements</span></span>



| <span data-ttu-id="42caf-179">Requisito</span><span class="sxs-lookup"><span data-stu-id="42caf-179">Requirement</span></span> | <span data-ttu-id="42caf-180">Valore</span><span class="sxs-lookup"><span data-stu-id="42caf-180">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="42caf-181">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="42caf-181">Minimum supported client</span></span><br/> | <span data-ttu-id="42caf-182">\[Solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="42caf-182">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="42caf-183">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="42caf-183">Minimum supported server</span></span><br/> | <span data-ttu-id="42caf-184">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="42caf-184">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="42caf-185">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="42caf-185">End of client support</span></span><br/>    | <span data-ttu-id="42caf-186">Windows XP</span><span class="sxs-lookup"><span data-stu-id="42caf-186">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="42caf-187">Fine del supporto server</span><span class="sxs-lookup"><span data-stu-id="42caf-187">End of server support</span></span><br/>    | <span data-ttu-id="42caf-188">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="42caf-188">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="42caf-189">Intestazione</span><span class="sxs-lookup"><span data-stu-id="42caf-189">Header</span></span><br/>                   | <dl> <span data-ttu-id="42caf-190"><dt>Scardssp. h</dt></span><span class="sxs-lookup"><span data-stu-id="42caf-190"><dt>Scardssp.h</dt></span></span> </dl>   |
| <span data-ttu-id="42caf-191">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="42caf-191">Type library</span></span><br/>             | <dl> <span data-ttu-id="42caf-192"><dt>Scardsrv. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="42caf-192"><dt>Scardsrv.tlb</dt></span></span> </dl> |
| <span data-ttu-id="42caf-193">DLL</span><span class="sxs-lookup"><span data-stu-id="42caf-193">DLL</span></span><br/>                      | <dl> <span data-ttu-id="42caf-194"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="42caf-194"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="42caf-195">IID</span><span class="sxs-lookup"><span data-stu-id="42caf-195">IID</span></span><br/>                      | <span data-ttu-id="42caf-196">IID \_ ISCardISO7816 è definito come 53B6AA68-3F56-11D0-916B-00AA00C18068</span><span class="sxs-lookup"><span data-stu-id="42caf-196">IID\_ISCardISO7816 is defined as 53B6AA68-3F56-11D0-916B-00AA00C18068</span></span><br/>        |



## <a name="see-also"></a><span data-ttu-id="42caf-197">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="42caf-197">See also</span></span>

<dl> <dt>

[<span data-ttu-id="42caf-198">**GetData**</span><span class="sxs-lookup"><span data-stu-id="42caf-198">**GetData**</span></span>](iscardiso7816-getdata.md)
</dt> <dt>

[<span data-ttu-id="42caf-199">**ISCardISO7816**</span><span class="sxs-lookup"><span data-stu-id="42caf-199">**ISCardISO7816**</span></span>](iscardiso7816.md)
</dt> </dl>

 

 
