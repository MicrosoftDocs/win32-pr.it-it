---
description: Il metodo GetData costruisce un comando APDU (Application Protocol Data Unit) che recupera un singolo oggetto dati primitivo o un set di oggetti dati (contenuto in un oggetto dati costruito), a seconda del tipo di file selezionato.
ms.assetid: d764a765-f451-4bf7-9d06-f5901062dcac
title: 'Metodo ISCardISO7816:: GetData (scardssp. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardISO7816.GetData
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 93dca04daa50e068a68dc62cf11a580eb8e3b1c6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103758096"
---
# <a name="iscardiso7816getdata-method"></a><span data-ttu-id="55f56-103">Metodo ISCardISO7816:: GetData</span><span class="sxs-lookup"><span data-stu-id="55f56-103">ISCardISO7816::GetData method</span></span>

<span data-ttu-id="55f56-104">\[Il metodo **GetData** è disponibile per l'uso nei sistemi operativi specificati nella sezione requisiti.</span><span class="sxs-lookup"><span data-stu-id="55f56-104">\[The **GetData** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="55f56-105">Non è disponibile per l'utilizzo in Windows Server 2003 con Service Pack 1 (SP1) e versioni successive, Windows Vista, Windows Server 2008 e versioni successive del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="55f56-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="55f56-106">I [moduli Smart Card](/previous-versions/windows/desktop/secsmart/smart-card-modules) offrono funzionalità simili.\]</span><span class="sxs-lookup"><span data-stu-id="55f56-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="55f56-107">Il metodo **GetData** costruisce un comando APDU ( [*Application Protocol Data Unit*](../secgloss/a-gly.md) ) che recupera un singolo oggetto dati primitivo o un set di oggetti dati (contenuto in un oggetto dati costruito), a seconda del tipo di file selezionato.</span><span class="sxs-lookup"><span data-stu-id="55f56-107">The **GetData** method constructs an [*application protocol data unit*](../secgloss/a-gly.md) (APDU) command that retrieves either a single primitive data object or a set of data objects (contained in a constructed data object), depending on the type of file selected.</span></span>

## <a name="syntax"></a><span data-ttu-id="55f56-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="55f56-108">Syntax</span></span>


```C++
HRESULT GetData(
  [in]      BYTE       byP1,
  [in]      BYTE       byP2,
  [in]      LONG       lBytesToGet,
  [in, out] LPSCARDCMD *ppCmd
);
```



## <a name="parameters"></a><span data-ttu-id="55f56-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="55f56-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="55f56-110">*byP1* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="55f56-110">*byP1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="55f56-111">Parametri.</span><span class="sxs-lookup"><span data-stu-id="55f56-111">Parameters.</span></span>



| <span data-ttu-id="55f56-112">Valore</span><span class="sxs-lookup"><span data-stu-id="55f56-112">Value</span></span>                                                                                  | <span data-ttu-id="55f56-113">Significato</span><span class="sxs-lookup"><span data-stu-id="55f56-113">Meaning</span></span>                                          |
|----------------------------------------------------------------------------------------|--------------------------------------------------|
| <dl> <span data-ttu-id="55f56-114"><dt>0000-003F</dt></span><span class="sxs-lookup"><span data-stu-id="55f56-114"><dt>0000 - 003F</dt></span></span> </dl> | <span data-ttu-id="55f56-115">RFU</span><span class="sxs-lookup"><span data-stu-id="55f56-115">RFU</span></span><br/>                                   |
| <dl> <span data-ttu-id="55f56-116"><dt>0040-00FF</dt></span><span class="sxs-lookup"><span data-stu-id="55f56-116"><dt>0040 - 00FF</dt></span></span> </dl> | <span data-ttu-id="55f56-117">Tag BER-TLV (1 byte) in P2</span><span class="sxs-lookup"><span data-stu-id="55f56-117">BER-TLV tag (1 byte) in P2</span></span><br/>            |
| <dl> <span data-ttu-id="55f56-118"><dt>0100-01FF</dt></span><span class="sxs-lookup"><span data-stu-id="55f56-118"><dt>0100 - 01FF</dt></span></span> </dl> | <span data-ttu-id="55f56-119">Dati applicazione (codifica proprietaria)</span><span class="sxs-lookup"><span data-stu-id="55f56-119">Application data (proprietary coding)</span></span><br/> |
| <dl> <span data-ttu-id="55f56-120"><dt>0200-02FF</dt></span><span class="sxs-lookup"><span data-stu-id="55f56-120"><dt>0200 - 02FF</dt></span></span> </dl> | <span data-ttu-id="55f56-121">SEMPLICE tag TLV in P2</span><span class="sxs-lookup"><span data-stu-id="55f56-121">SIMPLE-TLV tag in P2</span></span><br/>                  |
| <dl> <span data-ttu-id="55f56-122"><dt>0300-03FF</dt></span><span class="sxs-lookup"><span data-stu-id="55f56-122"><dt>0300 - 03FF</dt></span></span> </dl> | <span data-ttu-id="55f56-123">RFU</span><span class="sxs-lookup"><span data-stu-id="55f56-123">RFU</span></span><br/>                                   |
| <dl> <span data-ttu-id="55f56-124"><dt>0400 - 04FF</dt></span><span class="sxs-lookup"><span data-stu-id="55f56-124"><dt>0400 - 04FF</dt></span></span> </dl> | <span data-ttu-id="55f56-125">Tag BER-TLV (2 byte) in P1-P2</span><span class="sxs-lookup"><span data-stu-id="55f56-125">BER-TLV tag (2 bytes) in P1-P2</span></span><br/>        |



 

</dd> <dt>

<span data-ttu-id="55f56-126">*byP2* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="55f56-126">*byP2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="55f56-127">Parametri.</span><span class="sxs-lookup"><span data-stu-id="55f56-127">Parameters.</span></span>



| <span data-ttu-id="55f56-128">Valore</span><span class="sxs-lookup"><span data-stu-id="55f56-128">Value</span></span>                                                                                  | <span data-ttu-id="55f56-129">Significato</span><span class="sxs-lookup"><span data-stu-id="55f56-129">Meaning</span></span>                                          |
|----------------------------------------------------------------------------------------|--------------------------------------------------|
| <dl> <span data-ttu-id="55f56-130"><dt>0000-003F</dt></span><span class="sxs-lookup"><span data-stu-id="55f56-130"><dt>0000 - 003F</dt></span></span> </dl> | <span data-ttu-id="55f56-131">RFU</span><span class="sxs-lookup"><span data-stu-id="55f56-131">RFU</span></span><br/>                                   |
| <dl> <span data-ttu-id="55f56-132"><dt>0040-00FF</dt></span><span class="sxs-lookup"><span data-stu-id="55f56-132"><dt>0040 - 00FF</dt></span></span> </dl> | <span data-ttu-id="55f56-133">Tag BER-TLV (1 byte) in P2</span><span class="sxs-lookup"><span data-stu-id="55f56-133">BER-TLV tag (1 byte) in P2</span></span><br/>            |
| <dl> <span data-ttu-id="55f56-134"><dt>0100-01FF</dt></span><span class="sxs-lookup"><span data-stu-id="55f56-134"><dt>0100 - 01FF</dt></span></span> </dl> | <span data-ttu-id="55f56-135">Dati applicazione (codifica proprietaria)</span><span class="sxs-lookup"><span data-stu-id="55f56-135">Application data (proprietary coding)</span></span><br/> |
| <dl> <span data-ttu-id="55f56-136"><dt>0200-02FF</dt></span><span class="sxs-lookup"><span data-stu-id="55f56-136"><dt>0200 - 02FF</dt></span></span> </dl> | <span data-ttu-id="55f56-137">SEMPLICE tag TLV in P2</span><span class="sxs-lookup"><span data-stu-id="55f56-137">SIMPLE-TLV tag in P2</span></span><br/>                  |
| <dl> <span data-ttu-id="55f56-138"><dt>0300-03FF</dt></span><span class="sxs-lookup"><span data-stu-id="55f56-138"><dt>0300 - 03FF</dt></span></span> </dl> | <span data-ttu-id="55f56-139">RFU</span><span class="sxs-lookup"><span data-stu-id="55f56-139">RFU</span></span><br/>                                   |
| <dl> <span data-ttu-id="55f56-140"><dt>0400 - 04FF</dt></span><span class="sxs-lookup"><span data-stu-id="55f56-140"><dt>0400 - 04FF</dt></span></span> </dl> | <span data-ttu-id="55f56-141">Tag BER-TLV (2 byte) in P1-P2</span><span class="sxs-lookup"><span data-stu-id="55f56-141">BER-TLV tag (2 bytes) in P1-P2</span></span><br/>        |



 

</dd> <dt>

<span data-ttu-id="55f56-142">*lBytesToGet* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="55f56-142">*lBytesToGet* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="55f56-143">Numero di byte previsti nella risposta.</span><span class="sxs-lookup"><span data-stu-id="55f56-143">Number of bytes expected in the response.</span></span>

</dd> <dt>

<span data-ttu-id="55f56-144">*ppCmd* \[ in uscita\]</span><span class="sxs-lookup"><span data-stu-id="55f56-144">*ppCmd* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="55f56-145">In input, un puntatore a un oggetto di interfaccia [**ISCardCmd**](iscardcmd.md) o **null**.</span><span class="sxs-lookup"><span data-stu-id="55f56-145">On input, a pointer to an [**ISCardCmd**](iscardcmd.md) interface object or **NULL**.</span></span>

<span data-ttu-id="55f56-146">Al ritorno, viene compilato con il comando APDU creato da questa operazione.</span><span class="sxs-lookup"><span data-stu-id="55f56-146">On return, it is filled with the APDU command constructed by this operation.</span></span> <span data-ttu-id="55f56-147">Se *ppCmd* è stato impostato su **null**, un oggetto [**ISCardCmd**](iscardcmd.md) della [*Smart Card*](../secgloss/s-gly.md) viene creato e restituito internamente utilizzando il puntatore *ppCmd* .</span><span class="sxs-lookup"><span data-stu-id="55f56-147">If *ppCmd* was set to **NULL**, a [*smart card*](../secgloss/s-gly.md) [**ISCardCmd**](iscardcmd.md) object is internally created and returned using the *ppCmd* pointer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="55f56-148">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="55f56-148">Return value</span></span>

<span data-ttu-id="55f56-149">Il metodo restituisce uno dei valori possibili seguenti.</span><span class="sxs-lookup"><span data-stu-id="55f56-149">The method returns one of the following possible values.</span></span>



| <span data-ttu-id="55f56-150">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="55f56-150">Return code</span></span>                                                                                   | <span data-ttu-id="55f56-151">Descrizione</span><span class="sxs-lookup"><span data-stu-id="55f56-151">Description</span></span>                                  |
|-----------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="55f56-152"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="55f56-152"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="55f56-153">Operazione completata correttamente.</span><span class="sxs-lookup"><span data-stu-id="55f56-153">Operation completed successfully.</span></span><br/> |
| <dl> <span data-ttu-id="55f56-154"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="55f56-154"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="55f56-155">Parametro non valido.</span><span class="sxs-lookup"><span data-stu-id="55f56-155">Invalid parameter.</span></span><br/>                |
| <dl> <span data-ttu-id="55f56-156"><dt>**\_puntatore E**</dt></span><span class="sxs-lookup"><span data-stu-id="55f56-156"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="55f56-157">È stato passato un puntatore non valido.</span><span class="sxs-lookup"><span data-stu-id="55f56-157">A bad pointer was passed in.</span></span><br/>      |
| <dl> <span data-ttu-id="55f56-158"><dt>**E \_ OutOfMemory**</dt></span><span class="sxs-lookup"><span data-stu-id="55f56-158"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="55f56-159">Memoria insufficiente.</span><span class="sxs-lookup"><span data-stu-id="55f56-159">Out of memory.</span></span><br/>                    |



 

## <a name="remarks"></a><span data-ttu-id="55f56-160">Commenti</span><span class="sxs-lookup"><span data-stu-id="55f56-160">Remarks</span></span>

<span data-ttu-id="55f56-161">Il comando incapsulato può essere eseguito solo se lo stato di sicurezza della [*Smart Card*](../secgloss/s-gly.md) soddisfa gli attributi di sicurezza del file elementare letto.</span><span class="sxs-lookup"><span data-stu-id="55f56-161">The encapsulated command can only be performed if the security status of the [*smart card*](../secgloss/s-gly.md) satisfies the security attributes of the elementary file being read.</span></span> <span data-ttu-id="55f56-162">Le condizioni di sicurezza dipendono dai criteri della scheda e possono essere modificate tramite [**ExternalAuthenticate**](iscardiso7816-externalauthenticate.md), [**InternalAuthenticate**](iscardiso7816-internalauthenticate.md), [**ISCardAuth**](iscardauth.md)e così via.</span><span class="sxs-lookup"><span data-stu-id="55f56-162">Security conditions are dependent on the policy of the card, and may be manipulated through [**ExternalAuthenticate**](iscardiso7816-externalauthenticate.md), [**InternalAuthenticate**](iscardiso7816-internalauthenticate.md), [**ISCardAuth**](iscardauth.md), and so on.</span></span>

<span data-ttu-id="55f56-163">Per selezionare un file, chiamare [**SelectFile**](iscardiso7816-selectfile.md).</span><span class="sxs-lookup"><span data-stu-id="55f56-163">To select a file, call [**SelectFile**](iscardiso7816-selectfile.md).</span></span>

<span data-ttu-id="55f56-164">Per un elenco di tutti i metodi forniti da questa interfaccia, vedere [**ISCardISO7816**](iscardiso7816.md).</span><span class="sxs-lookup"><span data-stu-id="55f56-164">For a list of all the methods provided by this interface, see [**ISCardISO7816**](iscardiso7816.md).</span></span>

<span data-ttu-id="55f56-165">Oltre ai codici di errore COM elencati sopra, questa interfaccia può restituire un codice di errore della smart card se è stata chiamata una funzione Smart Card per completare la richiesta.</span><span class="sxs-lookup"><span data-stu-id="55f56-165">In addition to the COM error codes listed above, this interface may return a smart card error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="55f56-166">Per ulteriori informazioni, vedere [valori restituiti della smart card](authentication-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="55f56-166">For more information, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="55f56-167">Requisiti</span><span class="sxs-lookup"><span data-stu-id="55f56-167">Requirements</span></span>



| <span data-ttu-id="55f56-168">Requisito</span><span class="sxs-lookup"><span data-stu-id="55f56-168">Requirement</span></span> | <span data-ttu-id="55f56-169">Valore</span><span class="sxs-lookup"><span data-stu-id="55f56-169">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="55f56-170">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="55f56-170">Minimum supported client</span></span><br/> | <span data-ttu-id="55f56-171">\[Solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="55f56-171">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="55f56-172">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="55f56-172">Minimum supported server</span></span><br/> | <span data-ttu-id="55f56-173">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="55f56-173">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="55f56-174">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="55f56-174">End of client support</span></span><br/>    | <span data-ttu-id="55f56-175">Windows XP</span><span class="sxs-lookup"><span data-stu-id="55f56-175">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="55f56-176">Fine del supporto server</span><span class="sxs-lookup"><span data-stu-id="55f56-176">End of server support</span></span><br/>    | <span data-ttu-id="55f56-177">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="55f56-177">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="55f56-178">Intestazione</span><span class="sxs-lookup"><span data-stu-id="55f56-178">Header</span></span><br/>                   | <dl> <span data-ttu-id="55f56-179"><dt>Scardssp. h</dt></span><span class="sxs-lookup"><span data-stu-id="55f56-179"><dt>Scardssp.h</dt></span></span> </dl>   |
| <span data-ttu-id="55f56-180">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="55f56-180">Type library</span></span><br/>             | <dl> <span data-ttu-id="55f56-181"><dt>Scardsrv. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="55f56-181"><dt>Scardsrv.tlb</dt></span></span> </dl> |
| <span data-ttu-id="55f56-182">DLL</span><span class="sxs-lookup"><span data-stu-id="55f56-182">DLL</span></span><br/>                      | <dl> <span data-ttu-id="55f56-183"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="55f56-183"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="55f56-184">IID</span><span class="sxs-lookup"><span data-stu-id="55f56-184">IID</span></span><br/>                      | <span data-ttu-id="55f56-185">IID \_ ISCardISO7816 è definito come 53B6AA68-3F56-11D0-916B-00AA00C18068</span><span class="sxs-lookup"><span data-stu-id="55f56-185">IID\_ISCardISO7816 is defined as 53B6AA68-3F56-11D0-916B-00AA00C18068</span></span><br/>        |



## <a name="see-also"></a><span data-ttu-id="55f56-186">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="55f56-186">See also</span></span>

<dl> <dt>

[<span data-ttu-id="55f56-187">**ExternalAuthenticate**</span><span class="sxs-lookup"><span data-stu-id="55f56-187">**ExternalAuthenticate**</span></span>](iscardiso7816-externalauthenticate.md)
</dt> <dt>

[<span data-ttu-id="55f56-188">**InternalAuthenticate**</span><span class="sxs-lookup"><span data-stu-id="55f56-188">**InternalAuthenticate**</span></span>](iscardiso7816-internalauthenticate.md)
</dt> <dt>

[<span data-ttu-id="55f56-189">**ISCardAuth**</span><span class="sxs-lookup"><span data-stu-id="55f56-189">**ISCardAuth**</span></span>](iscardauth.md)
</dt> <dt>

[<span data-ttu-id="55f56-190">**ISCardISO7816**</span><span class="sxs-lookup"><span data-stu-id="55f56-190">**ISCardISO7816**</span></span>](iscardiso7816.md)
</dt> <dt>

[<span data-ttu-id="55f56-191">**PutData**</span><span class="sxs-lookup"><span data-stu-id="55f56-191">**PutData**</span></span>](iscardiso7816-putdata.md)
</dt> <dt>

[<span data-ttu-id="55f56-192">**SelectFile**</span><span class="sxs-lookup"><span data-stu-id="55f56-192">**SelectFile**</span></span>](iscardiso7816-selectfile.md)
</dt> </dl>

 

 
