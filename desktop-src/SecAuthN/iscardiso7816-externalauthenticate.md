---
description: Costruisce un comando APDU (Application Protocol Data Unit) che aggiorna in modo condizionale lo stato di sicurezza, verificando l'identità del computer quando la smart card non lo considera attendibile.
ms.assetid: 6db063d5-48a7-4c8b-ae84-cbcf34edc79d
title: 'Metodo ISCardISO7816:: ExternalAuthenticate (scardssp. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardISO7816.ExternalAuthenticate
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 1c8d56b6f2210974bd86dbecea06f16b68548659
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104401674"
---
# <a name="iscardiso7816externalauthenticate-method"></a><span data-ttu-id="698e2-103">Metodo ISCardISO7816:: ExternalAuthenticate</span><span class="sxs-lookup"><span data-stu-id="698e2-103">ISCardISO7816::ExternalAuthenticate method</span></span>

<span data-ttu-id="698e2-104">\[Il metodo **ExternalAuthenticate** è disponibile per l'uso nei sistemi operativi specificati nella sezione requisiti.</span><span class="sxs-lookup"><span data-stu-id="698e2-104">\[The **ExternalAuthenticate** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="698e2-105">Non è disponibile per l'utilizzo in Windows Server 2003 con Service Pack 1 (SP1) e versioni successive, Windows Vista, Windows Server 2008 e versioni successive del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="698e2-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="698e2-106">I [moduli Smart Card](/previous-versions/windows/desktop/secsmart/smart-card-modules) offrono funzionalità simili.\]</span><span class="sxs-lookup"><span data-stu-id="698e2-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="698e2-107">Il metodo **ExternalAuthenticate** costruisce un comando APDU ( [*Application Protocol Data Unit*](../secgloss/a-gly.md) ) che aggiorna in modo condizionale lo stato di sicurezza, verificando l'identità del computer quando la [*Smart Card*](../secgloss/s-gly.md) non lo considera attendibile.</span><span class="sxs-lookup"><span data-stu-id="698e2-107">The **ExternalAuthenticate** method constructs an [*application protocol data unit*](../secgloss/a-gly.md) (APDU) command that conditionally updates security status, verifying the identity of the computer when the [*smart card*](../secgloss/s-gly.md) does not trust it.</span></span>

<span data-ttu-id="698e2-108">Il comando usa il risultato (Sì o no) del calcolo per la scheda (in base a una richiesta di verifica rilasciata in precedenza dalla scheda, ad esempio \_ dal \_ comando ins get Challenge), una chiave (possibilmente segreta) archiviata nella scheda e i dati di autenticazione trasmessi dal dispositivo di interfaccia.</span><span class="sxs-lookup"><span data-stu-id="698e2-108">The command uses the result (yes or no) of the computation by the card (based on a challenge previously issued by the card, for example, by the INS\_GET\_CHALLENGE command), a key (possibly secret) stored in the card, and authentication data transmitted by the interface device.</span></span>

## <a name="syntax"></a><span data-ttu-id="698e2-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="698e2-109">Syntax</span></span>


```C++
HRESULT ExternalAuthenticate(
  [in]      BYTE         byAlgorithmRef,
  [in]      BYTE         bySecretRef,
  [in]      LPBYTEBUFFER pChallenge,
  [in, out] LPSCARDCMD   *ppCmd
);
```



## <a name="parameters"></a><span data-ttu-id="698e2-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="698e2-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="698e2-111">*byAlgorithmRef* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="698e2-111">*byAlgorithmRef* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="698e2-112">Riferimento dell'algoritmo nella scheda.</span><span class="sxs-lookup"><span data-stu-id="698e2-112">The reference of the algorithm in the card.</span></span>

<span data-ttu-id="698e2-113">Se questo valore è zero, indica che non viene fornita alcuna informazione.</span><span class="sxs-lookup"><span data-stu-id="698e2-113">If this value is zero, this indicates that no information is given.</span></span> <span data-ttu-id="698e2-114">Il riferimento dell'algoritmo è noto prima di emettere il comando o viene fornito nel campo dati.</span><span class="sxs-lookup"><span data-stu-id="698e2-114">The reference of the algorithm is known either before issuing the command or is provided in the data field.</span></span>

</dd> <dt>

<span data-ttu-id="698e2-115">*bySecretRef* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="698e2-115">*bySecretRef* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="698e2-116">Riferimento del segreto.</span><span class="sxs-lookup"><span data-stu-id="698e2-116">The reference of the secret.</span></span>



| <span data-ttu-id="698e2-117">Valore</span><span class="sxs-lookup"><span data-stu-id="698e2-117">Value</span></span>                                                                                                                                                                                    | <span data-ttu-id="698e2-118">Significato</span><span class="sxs-lookup"><span data-stu-id="698e2-118">Meaning</span></span>                                                                                                                                                                        |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="No_Info"></span><span id="no_info"></span><span id="NO_INFO"></span><dl> <span data-ttu-id="698e2-119"><dt>**Nessuna informazione**</dt></span><span class="sxs-lookup"><span data-stu-id="698e2-119"><dt>**No Info**</dt></span></span> </dl>                     | <span data-ttu-id="698e2-120">Posizione bit: 00000000</span><span class="sxs-lookup"><span data-stu-id="698e2-120">Bit position: 00000000</span></span><br/> <span data-ttu-id="698e2-121">Non viene fornita alcuna informazione.</span><span class="sxs-lookup"><span data-stu-id="698e2-121">No information is given.</span></span> <span data-ttu-id="698e2-122">Il riferimento del segreto è noto prima di emettere il comando o viene fornito nel campo dati.</span><span class="sxs-lookup"><span data-stu-id="698e2-122">The reference of the secret is known either before issuing the command or is provided in the data field.</span></span><br/> |
| <span id="Global_ref"></span><span id="global_ref"></span><span id="GLOBAL_REF"></span><dl> <span data-ttu-id="698e2-123"><dt>**Riferimento globale**</dt></span><span class="sxs-lookup"><span data-stu-id="698e2-123"><dt>**Global ref**</dt></span></span> </dl>         | <span data-ttu-id="698e2-124">Posizione bit: 0-------</span><span class="sxs-lookup"><span data-stu-id="698e2-124">Bit position: 0-------</span></span><br/> <span data-ttu-id="698e2-125">Dati di riferimento globali (chiave specifica MF).</span><span class="sxs-lookup"><span data-stu-id="698e2-125">Global reference data (an MF specific key).</span></span><br/>                                                                                       |
| <span id="Specific_ref"></span><span id="specific_ref"></span><span id="SPECIFIC_REF"></span><dl> <span data-ttu-id="698e2-126"><dt>**Riferimento specifico**</dt></span><span class="sxs-lookup"><span data-stu-id="698e2-126"><dt>**Specific ref**</dt></span></span> </dl> | <span data-ttu-id="698e2-127">Posizione bit: 1-------</span><span class="sxs-lookup"><span data-stu-id="698e2-127">Bit position: 1-------</span></span><br/> <span data-ttu-id="698e2-128">Dati di riferimento specifici (chiave specifica DF).</span><span class="sxs-lookup"><span data-stu-id="698e2-128">Specific reference data (a DF specific key).</span></span><br/>                                                                                      |
| <span id="RFU"></span><span id="rfu"></span><dl> <span data-ttu-id="698e2-129"><dt>**RFU**</dt></span><span class="sxs-lookup"><span data-stu-id="698e2-129"><dt>**RFU**</dt></span></span> </dl>                                                           | <span data-ttu-id="698e2-130">Posizione bit:-XX-----</span><span class="sxs-lookup"><span data-stu-id="698e2-130">Bit position: -xx-----</span></span><br/> <span data-ttu-id="698e2-131">00 (gli altri valori sono RFU).</span><span class="sxs-lookup"><span data-stu-id="698e2-131">00 (other values are RFU).</span></span><br/>                                                                                                        |
| <span id="Secret"></span><span id="secret"></span><span id="SECRET"></span><dl> <span data-ttu-id="698e2-132"><dt>**Segreto**</dt></span><span class="sxs-lookup"><span data-stu-id="698e2-132"><dt>**Secret**</dt></span></span> </dl>                         | <span data-ttu-id="698e2-133">Posizione bit:---xxxxx</span><span class="sxs-lookup"><span data-stu-id="698e2-133">Bit position: ---xxxxx</span></span><br/> <span data-ttu-id="698e2-134">Numero del segreto.</span><span class="sxs-lookup"><span data-stu-id="698e2-134">Number of the secret.</span></span><br/>                                                                                                             |



 

</dd> <dt>

<span data-ttu-id="698e2-135">*pChallenge* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="698e2-135">*pChallenge* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="698e2-136">Puntatore ai dati correlati all'autenticazione.</span><span class="sxs-lookup"><span data-stu-id="698e2-136">A pointer to the authentication-related data.</span></span> <span data-ttu-id="698e2-137">Questo parametro può essere **null**.</span><span class="sxs-lookup"><span data-stu-id="698e2-137">This parameter may be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="698e2-138">*ppCmd* \[ in uscita\]</span><span class="sxs-lookup"><span data-stu-id="698e2-138">*ppCmd* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="698e2-139">In input, un puntatore a un oggetto di interfaccia [**ISCardCmd**](iscardcmd.md) o **null**.</span><span class="sxs-lookup"><span data-stu-id="698e2-139">On input, a pointer to an [**ISCardCmd**](iscardcmd.md) interface object or **NULL**.</span></span>

<span data-ttu-id="698e2-140">Al ritorno, viene compilato con il comando APDU creato da questa operazione.</span><span class="sxs-lookup"><span data-stu-id="698e2-140">On return, it is filled with the APDU command constructed by this operation.</span></span> <span data-ttu-id="698e2-141">Se *ppCmd* è stato impostato su **null**, un oggetto [**ISCardCmd**](iscardcmd.md) della [*Smart Card*](../secgloss/s-gly.md) viene creato e restituito internamente utilizzando il puntatore *ppCmd* .</span><span class="sxs-lookup"><span data-stu-id="698e2-141">If *ppCmd* was set to **NULL**, a [*smart card*](../secgloss/s-gly.md) [**ISCardCmd**](iscardcmd.md) object is internally created and returned by using the *ppCmd* pointer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="698e2-142">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="698e2-142">Return value</span></span>

<span data-ttu-id="698e2-143">Il metodo restituisce uno dei valori possibili seguenti.</span><span class="sxs-lookup"><span data-stu-id="698e2-143">The method returns one of the following possible values.</span></span>



| <span data-ttu-id="698e2-144">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="698e2-144">Return code</span></span>                                                                                   | <span data-ttu-id="698e2-145">Descrizione</span><span class="sxs-lookup"><span data-stu-id="698e2-145">Description</span></span>                                          |
|-----------------------------------------------------------------------------------------------|------------------------------------------------------|
| <dl> <span data-ttu-id="698e2-146"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="698e2-146"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="698e2-147">Operazione riuscita.</span><span class="sxs-lookup"><span data-stu-id="698e2-147">The operation completed successfully.</span></span><br/>     |
| <dl> <span data-ttu-id="698e2-148"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="698e2-148"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="698e2-149">È stato passato un parametro non valido.</span><span class="sxs-lookup"><span data-stu-id="698e2-149">A parameter that is not valid was passed.</span></span><br/> |
| <dl> <span data-ttu-id="698e2-150"><dt>**\_puntatore E**</dt></span><span class="sxs-lookup"><span data-stu-id="698e2-150"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="698e2-151">È stato passato un puntatore non valido.</span><span class="sxs-lookup"><span data-stu-id="698e2-151">A bad pointer was passed in.</span></span><br/>              |
| <dl> <span data-ttu-id="698e2-152"><dt>**E \_ OutOfMemory**</dt></span><span class="sxs-lookup"><span data-stu-id="698e2-152"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="698e2-153">Memoria insufficiente.</span><span class="sxs-lookup"><span data-stu-id="698e2-153">Out of memory.</span></span><br/>                            |



 

## <a name="remarks"></a><span data-ttu-id="698e2-154">Commenti</span><span class="sxs-lookup"><span data-stu-id="698e2-154">Remarks</span></span>

<span data-ttu-id="698e2-155">Per il corretto completamento del comando incapsulato, è necessario che l'ultima richiesta ottenuta dalla scheda sia valida.</span><span class="sxs-lookup"><span data-stu-id="698e2-155">For the encapsulated command to be successful, the last challenge obtained from the card must be valid.</span></span>

<span data-ttu-id="698e2-156">I confronti non riusciti possono essere registrati nella scheda, ad esempio per limitare il numero di ulteriori tentativi di utilizzo dei dati di riferimento.</span><span class="sxs-lookup"><span data-stu-id="698e2-156">Unsuccessful comparisons may be recorded in the card (for example, to limit the number of further attempts of the use of the reference data).</span></span>

<span data-ttu-id="698e2-157">Per un elenco di tutti i metodi forniti da questa interfaccia, vedere [**ISCardISO7816**](iscardiso7816.md).</span><span class="sxs-lookup"><span data-stu-id="698e2-157">For a list of all the methods provided by this interface, see [**ISCardISO7816**](iscardiso7816.md).</span></span>

<span data-ttu-id="698e2-158">Oltre ai codici di errore COM elencati sopra, questa interfaccia può restituire un codice di errore della smart card se è stata chiamata una funzione Smart Card per completare la richiesta.</span><span class="sxs-lookup"><span data-stu-id="698e2-158">In addition to the COM error codes listed above, this interface may return a smart card error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="698e2-159">Per ulteriori informazioni, vedere [valori restituiti della smart card](authentication-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="698e2-159">For more information, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="698e2-160">Requisiti</span><span class="sxs-lookup"><span data-stu-id="698e2-160">Requirements</span></span>



| <span data-ttu-id="698e2-161">Requisito</span><span class="sxs-lookup"><span data-stu-id="698e2-161">Requirement</span></span> | <span data-ttu-id="698e2-162">Valore</span><span class="sxs-lookup"><span data-stu-id="698e2-162">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="698e2-163">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="698e2-163">Minimum supported client</span></span><br/> | <span data-ttu-id="698e2-164">\[Solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="698e2-164">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="698e2-165">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="698e2-165">Minimum supported server</span></span><br/> | <span data-ttu-id="698e2-166">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="698e2-166">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="698e2-167">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="698e2-167">End of client support</span></span><br/>    | <span data-ttu-id="698e2-168">Windows XP</span><span class="sxs-lookup"><span data-stu-id="698e2-168">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="698e2-169">Fine del supporto server</span><span class="sxs-lookup"><span data-stu-id="698e2-169">End of server support</span></span><br/>    | <span data-ttu-id="698e2-170">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="698e2-170">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="698e2-171">Intestazione</span><span class="sxs-lookup"><span data-stu-id="698e2-171">Header</span></span><br/>                   | <dl> <span data-ttu-id="698e2-172"><dt>Scardssp. h</dt></span><span class="sxs-lookup"><span data-stu-id="698e2-172"><dt>Scardssp.h</dt></span></span> </dl>   |
| <span data-ttu-id="698e2-173">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="698e2-173">Type library</span></span><br/>             | <dl> <span data-ttu-id="698e2-174"><dt>Scardsrv. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="698e2-174"><dt>Scardsrv.tlb</dt></span></span> </dl> |
| <span data-ttu-id="698e2-175">DLL</span><span class="sxs-lookup"><span data-stu-id="698e2-175">DLL</span></span><br/>                      | <dl> <span data-ttu-id="698e2-176"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="698e2-176"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="698e2-177">IID</span><span class="sxs-lookup"><span data-stu-id="698e2-177">IID</span></span><br/>                      | <span data-ttu-id="698e2-178">IID \_ ISCardISO7816 è definito come 53B6AA68-3F56-11D0-916B-00AA00C18068</span><span class="sxs-lookup"><span data-stu-id="698e2-178">IID\_ISCardISO7816 is defined as 53B6AA68-3F56-11D0-916B-00AA00C18068</span></span><br/>        |



## <a name="see-also"></a><span data-ttu-id="698e2-179">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="698e2-179">See also</span></span>

<dl> <dt>

[<span data-ttu-id="698e2-180">**InternalAuthenticate**</span><span class="sxs-lookup"><span data-stu-id="698e2-180">**InternalAuthenticate**</span></span>](iscardiso7816-internalauthenticate.md)
</dt> <dt>

[<span data-ttu-id="698e2-181">**ISCardISO7816**</span><span class="sxs-lookup"><span data-stu-id="698e2-181">**ISCardISO7816**</span></span>](iscardiso7816.md)
</dt> </dl>

 

 
