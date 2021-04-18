---
description: Costruisce un comando APDU (Application Protocol Data Unit) che avvia il confronto (nella scheda) dei dati di verifica inviati dal dispositivo di interfaccia con i dati di riferimento archiviati nella scheda (ad esempio, la password).
ms.assetid: a0837c39-d741-42eb-88b2-87c4e043e64f
title: 'Metodo ISCardISO7816:: Verify (scardssp. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardISO7816.Verify
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: c44bf65bfcebe6e76ce1ee955205b9c9163efcee
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106313736"
---
# <a name="iscardiso7816verify-method"></a><span data-ttu-id="069ca-103">Metodo ISCardISO7816:: Verify</span><span class="sxs-lookup"><span data-stu-id="069ca-103">ISCardISO7816::Verify method</span></span>

<span data-ttu-id="069ca-104">\[Il metodo **Verify** è disponibile per l'uso nei sistemi operativi specificati nella sezione requisiti.</span><span class="sxs-lookup"><span data-stu-id="069ca-104">\[The **Verify** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="069ca-105">Non è disponibile per l'utilizzo in Windows Server 2003 con Service Pack 1 (SP1) e versioni successive, Windows Vista, Windows Server 2008 e versioni successive del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="069ca-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="069ca-106">I [moduli Smart Card](/previous-versions/windows/desktop/secsmart/smart-card-modules) offrono funzionalità simili.\]</span><span class="sxs-lookup"><span data-stu-id="069ca-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="069ca-107">Il metodo **Verify** costruisce un comando APDU ( [*Application Protocol Data Unit*](../secgloss/a-gly.md) ) che avvia il confronto (nella scheda) dei dati di verifica inviati dal dispositivo di interfaccia con i dati di riferimento archiviati nella scheda (ad esempio, password).</span><span class="sxs-lookup"><span data-stu-id="069ca-107">The **Verify** method constructs an [*application protocol data unit*](../secgloss/a-gly.md) (APDU) command that initiates the comparison (in the card) of the verification data sent from the interface device with the reference data stored in the card (for example, password).</span></span>

## <a name="syntax"></a><span data-ttu-id="069ca-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="069ca-108">Syntax</span></span>


```C++
HRESULT Verify(
  [in]      BYTE         byRefCtrl,
  [in]      LPBYTEBUFFER pData,
  [in, out] LPSCARDCMD   *ppCmd
);
```



## <a name="parameters"></a><span data-ttu-id="069ca-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="069ca-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="069ca-110">*byRefCtrl* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="069ca-110">*byRefCtrl* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="069ca-111">Quantificatore dei dati di riferimento.</span><span class="sxs-lookup"><span data-stu-id="069ca-111">A quantifier of the reference data.</span></span> <span data-ttu-id="069ca-112">Segue la codifica del controllo di riferimento P2.</span><span class="sxs-lookup"><span data-stu-id="069ca-112">Coding of the reference control P2 follows.</span></span>

<span data-ttu-id="069ca-113">Quando il corpo è vuoto, il comando può essere usato per recuperare il numero "X" di nuovi tentativi consentiti (SW1-SW2 = 63CX) o per verificare se la verifica non è necessaria (SW1-SW2 = 9000).</span><span class="sxs-lookup"><span data-stu-id="069ca-113">When the body is empty, the command may be used either to retrieve the number 'X' of further allowed retries (SW1-SW2=63CX) or to check whether the verification is not required (SW1-SW2=9000).</span></span>



| <span data-ttu-id="069ca-114">Valore</span><span class="sxs-lookup"><span data-stu-id="069ca-114">Value</span></span>                                                                                                                                                                                    | <span data-ttu-id="069ca-115">Significato</span><span class="sxs-lookup"><span data-stu-id="069ca-115">Meaning</span></span>                                                                                                                                                                                           |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="No_Info"></span><span id="no_info"></span><span id="NO_INFO"></span><dl> <span data-ttu-id="069ca-116"><dt>**Nessuna informazione**</dt></span><span class="sxs-lookup"><span data-stu-id="069ca-116"><dt>**No Info**</dt></span></span> </dl>                     | <span data-ttu-id="069ca-117">Posizione bit: 00000000</span><span class="sxs-lookup"><span data-stu-id="069ca-117">Bit position: 00000000</span></span><br/> <span data-ttu-id="069ca-118">P2 = 00 è riservata per indicare che non viene usato alcun qualificatore particolare nelle schede in cui il comando Verify fa riferimento ai dati del segreto in modo non ambiguo.</span><span class="sxs-lookup"><span data-stu-id="069ca-118">P2=00 is reserved to indicate that no particular qualifier is used in those cards where the verify command references the secret data unambiguously.</span></span><br/> |
| <span id="Global_Ref"></span><span id="global_ref"></span><span id="GLOBAL_REF"></span><dl> <span data-ttu-id="069ca-119"><dt>**Riferimento globale**</dt></span><span class="sxs-lookup"><span data-stu-id="069ca-119"><dt>**Global Ref**</dt></span></span> </dl>         | <span data-ttu-id="069ca-120">Posizione bit: 0-------</span><span class="sxs-lookup"><span data-stu-id="069ca-120">Bit position: 0-------</span></span><br/> <span data-ttu-id="069ca-121">Un esempio di riferimento globale è costituito da una password.</span><span class="sxs-lookup"><span data-stu-id="069ca-121">An example of Global Ref would be a password.</span></span><br/>                                                                                                        |
| <span id="Specific_Ref"></span><span id="specific_ref"></span><span id="SPECIFIC_REF"></span><dl> <span data-ttu-id="069ca-122"><dt>**Riferimento specifico**</dt></span><span class="sxs-lookup"><span data-stu-id="069ca-122"><dt>**Specific Ref**</dt></span></span> </dl> | <span data-ttu-id="069ca-123">Posizione bit: 1-------</span><span class="sxs-lookup"><span data-stu-id="069ca-123">Bit position: 1-------</span></span><br/> <span data-ttu-id="069ca-124">Un esempio di riferimento specifico è la password specifica di DF.</span><span class="sxs-lookup"><span data-stu-id="069ca-124">An example of Specific Ref is DF specific password.</span></span><br/>                                                                                                  |
| <span id="RFU"></span><span id="rfu"></span><dl> <span data-ttu-id="069ca-125"><dt>**RFU**</dt></span><span class="sxs-lookup"><span data-stu-id="069ca-125"><dt>**RFU**</dt></span></span> </dl>                                                           | <span data-ttu-id="069ca-126">Posizione bit:-XX-----</span><span class="sxs-lookup"><span data-stu-id="069ca-126">Bit position: -xx-----</span></span><br/>                                                                                                                                                                 |
| <span id="Ref_Data__"></span><span id="ref_data__"></span><span id="REF_DATA__"></span><dl> <span data-ttu-id="069ca-127"><dt>**Dati di riferimento \#**</dt></span><span class="sxs-lookup"><span data-stu-id="069ca-127"><dt>**Ref Data \#**</dt></span></span> </dl>        | <span data-ttu-id="069ca-128">Posizione bit:---xxxxx</span><span class="sxs-lookup"><span data-stu-id="069ca-128">Bit position: ---xxxxx</span></span><br/> <span data-ttu-id="069ca-129">Il numero di dati di riferimento può essere, ad esempio, un numero di password o un identificatore EF breve.</span><span class="sxs-lookup"><span data-stu-id="069ca-129">The reference data number may be, for example, a password number or a short EF identifier.</span></span><br/>                                                           |



 

</dd> <dt>

<span data-ttu-id="069ca-130">*pData* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="069ca-130">*pData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="069ca-131">Puntatore ai dati di verifica.</span><span class="sxs-lookup"><span data-stu-id="069ca-131">A pointer to the verification data.</span></span> <span data-ttu-id="069ca-132">Questo parametro può essere **NULL**.</span><span class="sxs-lookup"><span data-stu-id="069ca-132">This parameter can be **NULL**.</span></span> <span data-ttu-id="069ca-133">Il valore predefinito è **NULL**.</span><span class="sxs-lookup"><span data-stu-id="069ca-133">The default value is **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="069ca-134">*ppCmd* \[ in uscita\]</span><span class="sxs-lookup"><span data-stu-id="069ca-134">*ppCmd* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="069ca-135">In input, un puntatore a un oggetto di interfaccia [**ISCardCmd**](iscardcmd.md) o **null**.</span><span class="sxs-lookup"><span data-stu-id="069ca-135">On input, a pointer to an [**ISCardCmd**](iscardcmd.md) interface object or **NULL**.</span></span>

<span data-ttu-id="069ca-136">Al ritorno, viene compilato con il comando APDU creato da questa operazione.</span><span class="sxs-lookup"><span data-stu-id="069ca-136">On return, it is filled with the APDU command constructed by this operation.</span></span> <span data-ttu-id="069ca-137">Se *ppCmd* è stato impostato su **null**, un oggetto [**ISCardCmd**](iscardcmd.md) della [*Smart Card*](../secgloss/s-gly.md) viene creato e restituito internamente utilizzando il puntatore *ppCmd* .</span><span class="sxs-lookup"><span data-stu-id="069ca-137">If *ppCmd* was set to **NULL**, a [*smart card*](../secgloss/s-gly.md) [**ISCardCmd**](iscardcmd.md) object is internally created and returned by using the *ppCmd* pointer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="069ca-138">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="069ca-138">Return value</span></span>

<span data-ttu-id="069ca-139">Il metodo restituisce uno dei valori possibili seguenti.</span><span class="sxs-lookup"><span data-stu-id="069ca-139">The method returns one of the following possible values.</span></span>



| <span data-ttu-id="069ca-140">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="069ca-140">Return code</span></span>                                                                                   | <span data-ttu-id="069ca-141">Descrizione</span><span class="sxs-lookup"><span data-stu-id="069ca-141">Description</span></span>                                        |
|-----------------------------------------------------------------------------------------------|----------------------------------------------------|
| <dl> <span data-ttu-id="069ca-142"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="069ca-142"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="069ca-143">Operazione riuscita.</span><span class="sxs-lookup"><span data-stu-id="069ca-143">The operation completed successfully.</span></span><br/>   |
| <dl> <span data-ttu-id="069ca-144"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="069ca-144"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="069ca-145">È stato usato un parametro non valido.</span><span class="sxs-lookup"><span data-stu-id="069ca-145">A parameter that is not valid was used.</span></span><br/> |
| <dl> <span data-ttu-id="069ca-146"><dt>**\_puntatore E**</dt></span><span class="sxs-lookup"><span data-stu-id="069ca-146"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="069ca-147">È stato passato un puntatore non valido.</span><span class="sxs-lookup"><span data-stu-id="069ca-147">A bad pointer was passed in.</span></span><br/>            |
| <dl> <span data-ttu-id="069ca-148"><dt>**E \_ OutOfMemory**</dt></span><span class="sxs-lookup"><span data-stu-id="069ca-148"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="069ca-149">Memoria insufficiente.</span><span class="sxs-lookup"><span data-stu-id="069ca-149">Out of memory.</span></span><br/>                          |



 

## <a name="remarks"></a><span data-ttu-id="069ca-150">Commenti</span><span class="sxs-lookup"><span data-stu-id="069ca-150">Remarks</span></span>

<span data-ttu-id="069ca-151">Lo stato di sicurezza può essere modificato in seguito a un confronto.</span><span class="sxs-lookup"><span data-stu-id="069ca-151">The security status may be modified as a result of a comparison.</span></span> <span data-ttu-id="069ca-152">I confronti non riusciti possono essere registrati nella scheda, ad esempio per limitare il numero di ulteriori tentativi di utilizzo dei dati di riferimento.</span><span class="sxs-lookup"><span data-stu-id="069ca-152">Unsuccessful comparisons may be recorded in the card (for example, to limit the number of further attempts of the use of the reference data).</span></span>

<span data-ttu-id="069ca-153">Per un elenco di tutti i metodi forniti da questa interfaccia, vedere [**ISCardISO7816**](iscardiso7816.md).</span><span class="sxs-lookup"><span data-stu-id="069ca-153">For a list of all the methods provided by this interface, see [**ISCardISO7816**](iscardiso7816.md).</span></span>

<span data-ttu-id="069ca-154">Oltre ai codici di errore COM elencati sopra, questa interfaccia può restituire un codice di errore della smart card se è stata chiamata una funzione Smart Card per completare la richiesta.</span><span class="sxs-lookup"><span data-stu-id="069ca-154">In addition to the COM error codes listed above, this interface may return a smart card error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="069ca-155">Per ulteriori informazioni, vedere [valori restituiti della smart card](authentication-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="069ca-155">For more information, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="069ca-156">Requisiti</span><span class="sxs-lookup"><span data-stu-id="069ca-156">Requirements</span></span>



| <span data-ttu-id="069ca-157">Requisito</span><span class="sxs-lookup"><span data-stu-id="069ca-157">Requirement</span></span> | <span data-ttu-id="069ca-158">Valore</span><span class="sxs-lookup"><span data-stu-id="069ca-158">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="069ca-159">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="069ca-159">Minimum supported client</span></span><br/> | <span data-ttu-id="069ca-160">\[Solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="069ca-160">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="069ca-161">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="069ca-161">Minimum supported server</span></span><br/> | <span data-ttu-id="069ca-162">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="069ca-162">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="069ca-163">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="069ca-163">End of client support</span></span><br/>    | <span data-ttu-id="069ca-164">Windows XP</span><span class="sxs-lookup"><span data-stu-id="069ca-164">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="069ca-165">Fine del supporto server</span><span class="sxs-lookup"><span data-stu-id="069ca-165">End of server support</span></span><br/>    | <span data-ttu-id="069ca-166">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="069ca-166">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="069ca-167">Intestazione</span><span class="sxs-lookup"><span data-stu-id="069ca-167">Header</span></span><br/>                   | <dl> <span data-ttu-id="069ca-168"><dt>Scardssp. h</dt></span><span class="sxs-lookup"><span data-stu-id="069ca-168"><dt>Scardssp.h</dt></span></span> </dl>   |
| <span data-ttu-id="069ca-169">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="069ca-169">Type library</span></span><br/>             | <dl> <span data-ttu-id="069ca-170"><dt>Scardsrv. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="069ca-170"><dt>Scardsrv.tlb</dt></span></span> </dl> |
| <span data-ttu-id="069ca-171">DLL</span><span class="sxs-lookup"><span data-stu-id="069ca-171">DLL</span></span><br/>                      | <dl> <span data-ttu-id="069ca-172"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="069ca-172"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="069ca-173">IID</span><span class="sxs-lookup"><span data-stu-id="069ca-173">IID</span></span><br/>                      | <span data-ttu-id="069ca-174">IID \_ ISCardISO7816 è definito come 53B6AA68-3F56-11D0-916B-00AA00C18068</span><span class="sxs-lookup"><span data-stu-id="069ca-174">IID\_ISCardISO7816 is defined as 53B6AA68-3F56-11D0-916B-00AA00C18068</span></span><br/>        |



## <a name="see-also"></a><span data-ttu-id="069ca-175">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="069ca-175">See also</span></span>

<dl> <dt>

[<span data-ttu-id="069ca-176">**ISCardISO7816**</span><span class="sxs-lookup"><span data-stu-id="069ca-176">**ISCardISO7816**</span></span>](iscardiso7816.md)
</dt> </dl>

 

 
