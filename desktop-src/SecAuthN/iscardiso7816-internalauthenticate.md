---
description: Costruisce un comando APDU (Application Protocol Data Unit) che avvia il calcolo dei dati di autenticazione dalla scheda usando i dati di richiesta di verifica inviati dal dispositivo di interfaccia e un segreto pertinente, ad esempio una chiave, archiviati nella scheda.
ms.assetid: cb0b2535-6e5b-4fb2-b540-cd037259baab
title: 'Metodo ISCardISO7816:: InternalAuthenticate (scardssp. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardISO7816.InternalAuthenticate
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 1e30dbb06373907c5cea07e45d4f7a390b773349
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104049823"
---
# <a name="iscardiso7816internalauthenticate-method"></a><span data-ttu-id="41c20-103">Metodo ISCardISO7816:: InternalAuthenticate</span><span class="sxs-lookup"><span data-stu-id="41c20-103">ISCardISO7816::InternalAuthenticate method</span></span>

<span data-ttu-id="41c20-104">\[Il metodo **InternalAuthenticate** è disponibile per l'uso nei sistemi operativi specificati nella sezione requisiti.</span><span class="sxs-lookup"><span data-stu-id="41c20-104">\[The **InternalAuthenticate** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="41c20-105">Non è disponibile per l'utilizzo in Windows Server 2003 con Service Pack 1 (SP1) e versioni successive, Windows Vista, Windows Server 2008 e versioni successive del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="41c20-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="41c20-106">I [moduli Smart Card](/previous-versions/windows/desktop/secsmart/smart-card-modules) offrono funzionalità simili.\]</span><span class="sxs-lookup"><span data-stu-id="41c20-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="41c20-107">Il metodo **InternalAuthenticate** costruisce un comando APDU ( [*Application Protocol Data Unit*](../secgloss/a-gly.md) ) che avvia il calcolo dei dati di autenticazione dalla scheda usando i dati di richiesta di verifica inviati dal dispositivo di interfaccia e un segreto pertinente, ad esempio una chiave, archiviati nella scheda.</span><span class="sxs-lookup"><span data-stu-id="41c20-107">The **InternalAuthenticate** method constructs an [*application protocol data unit*](../secgloss/a-gly.md) (APDU) command that initiates the computation of the authentication data by the card using the challenge data sent from the interface device and a relevant secret (for example, a key) stored in the card.</span></span>

<span data-ttu-id="41c20-108">Quando il segreto pertinente è collegato a MF, il comando può essere usato per autenticare la scheda nel suo complesso.</span><span class="sxs-lookup"><span data-stu-id="41c20-108">When the relevant secret is attached to the MF, the command may be used to authenticate the card as a whole.</span></span>

<span data-ttu-id="41c20-109">Quando il segreto pertinente è collegato a un altro DF, il comando può essere usato per autenticare tale DF.</span><span class="sxs-lookup"><span data-stu-id="41c20-109">When the relevant secret is attached to another DF, the command may be used to authenticate that DF.</span></span>

## <a name="syntax"></a><span data-ttu-id="41c20-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="41c20-110">Syntax</span></span>


```C++
HRESULT InternalAuthenticate(
  [in]      BYTE         byAlgorithmRef,
  [in]      BYTE         bySecretRef,
  [in]      LPBYTEBUFFER pChallenge,
  [in]      LONG         lReplyBytes,
  [in, out] LPSCARDCMD   *ppCmd
);
```



## <a name="parameters"></a><span data-ttu-id="41c20-111">Parametri</span><span class="sxs-lookup"><span data-stu-id="41c20-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="41c20-112">*byAlgorithmRef* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="41c20-112">*byAlgorithmRef* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="41c20-113">Riferimento dell'algoritmo nella scheda.</span><span class="sxs-lookup"><span data-stu-id="41c20-113">Reference of the algorithm in the card.</span></span>

<span data-ttu-id="41c20-114">Se questo valore è zero, indica che non viene fornita alcuna informazione.</span><span class="sxs-lookup"><span data-stu-id="41c20-114">If this value is zero, this indicates that no information is given.</span></span> <span data-ttu-id="41c20-115">Il riferimento dell'algoritmo è noto prima di emettere il comando o viene fornito nel campo dati.</span><span class="sxs-lookup"><span data-stu-id="41c20-115">The reference of the algorithm is known either before issuing the command or is provided in the data field.</span></span>

</dd> <dt>

<span data-ttu-id="41c20-116">*bySecretRef* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="41c20-116">*bySecretRef* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="41c20-117">Riferimento del segreto.</span><span class="sxs-lookup"><span data-stu-id="41c20-117">Reference of the secret.</span></span>



| <span data-ttu-id="41c20-118">Valore</span><span class="sxs-lookup"><span data-stu-id="41c20-118">Value</span></span>                                                                                                                                                                                    | <span data-ttu-id="41c20-119">Significato</span><span class="sxs-lookup"><span data-stu-id="41c20-119">Meaning</span></span>                                                                                                                                                                         |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="No_Info"></span><span id="no_info"></span><span id="NO_INFO"></span><dl> <span data-ttu-id="41c20-120"><dt>**Nessuna informazione**</dt></span><span class="sxs-lookup"><span data-stu-id="41c20-120"><dt>**No Info**</dt></span></span> </dl>                     | <span data-ttu-id="41c20-121">Posizione bit: 00000000</span><span class="sxs-lookup"><span data-stu-id="41c20-121">Bit position: 00000000</span></span> <br/> <span data-ttu-id="41c20-122">Non viene fornita alcuna informazione.</span><span class="sxs-lookup"><span data-stu-id="41c20-122">No information is given.</span></span> <span data-ttu-id="41c20-123">Il riferimento del segreto è noto prima di emettere il comando o viene fornito nel campo dati.</span><span class="sxs-lookup"><span data-stu-id="41c20-123">The reference of the secret is known either before issuing the command or is provided in the data field.</span></span><br/> |
| <span id="Global_ref"></span><span id="global_ref"></span><span id="GLOBAL_REF"></span><dl> <span data-ttu-id="41c20-124"><dt>**Riferimento globale**</dt></span><span class="sxs-lookup"><span data-stu-id="41c20-124"><dt>**Global ref**</dt></span></span> </dl>         | <span data-ttu-id="41c20-125">Posizione bit: 0-------</span><span class="sxs-lookup"><span data-stu-id="41c20-125">Bit position: 0-------</span></span> <br/> <span data-ttu-id="41c20-126">Dati di riferimento globali (chiave specifica MF).</span><span class="sxs-lookup"><span data-stu-id="41c20-126">Global reference data (an MF specific key).</span></span><br/>                                                                                       |
| <span id="Specific_ref"></span><span id="specific_ref"></span><span id="SPECIFIC_REF"></span><dl> <span data-ttu-id="41c20-127"><dt>**Riferimento specifico**</dt></span><span class="sxs-lookup"><span data-stu-id="41c20-127"><dt>**Specific ref**</dt></span></span> </dl> | <span data-ttu-id="41c20-128">Posizione bit: 1-------</span><span class="sxs-lookup"><span data-stu-id="41c20-128">Bit position: 1-------</span></span><br/> <span data-ttu-id="41c20-129">Dati di riferimento specifici (chiave specifica DF).</span><span class="sxs-lookup"><span data-stu-id="41c20-129">Specific reference data (a DF specific key).</span></span><br/>                                                                                       |
| <span id="RFU"></span><span id="rfu"></span><dl> <span data-ttu-id="41c20-130"><dt>**RFU**</dt></span><span class="sxs-lookup"><span data-stu-id="41c20-130"><dt>**RFU**</dt></span></span> </dl>                                                           | <span data-ttu-id="41c20-131">Posizione bit:-XX-----</span><span class="sxs-lookup"><span data-stu-id="41c20-131">Bit position: -xx-----</span></span><br/> <span data-ttu-id="41c20-132">00 (gli altri valori sono RFU).</span><span class="sxs-lookup"><span data-stu-id="41c20-132">00 (other values are RFU).</span></span><br/>                                                                                                         |
| <span id="Secret"></span><span id="secret"></span><span id="SECRET"></span><dl> <span data-ttu-id="41c20-133"><dt>**Segreto**</dt></span><span class="sxs-lookup"><span data-stu-id="41c20-133"><dt>**Secret**</dt></span></span> </dl>                         | <span data-ttu-id="41c20-134">Posizione bit:---xxxxx</span><span class="sxs-lookup"><span data-stu-id="41c20-134">Bit position: ---xxxxx</span></span><br/> <span data-ttu-id="41c20-135">Numero del segreto.</span><span class="sxs-lookup"><span data-stu-id="41c20-135">Number of the secret.</span></span><br/>                                                                                                              |



 

</dd> <dt>

<span data-ttu-id="41c20-136">*pChallenge* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="41c20-136">*pChallenge* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="41c20-137">Puntatore ai dati correlati all'autenticazione (ad esempio, Challenge).</span><span class="sxs-lookup"><span data-stu-id="41c20-137">Pointer to the authentication-related data (for example, challenge).</span></span>

</dd> <dt>

<span data-ttu-id="41c20-138">*lReplyBytes* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="41c20-138">*lReplyBytes* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="41c20-139">Numero massimo di byte previsti nella risposta.</span><span class="sxs-lookup"><span data-stu-id="41c20-139">Maximum number of bytes expected in response.</span></span>

</dd> <dt>

<span data-ttu-id="41c20-140">*ppCmd* \[ in uscita\]</span><span class="sxs-lookup"><span data-stu-id="41c20-140">*ppCmd* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="41c20-141">In input, un puntatore a un oggetto di interfaccia [**ISCardCmd**](iscardcmd.md) o **null**.</span><span class="sxs-lookup"><span data-stu-id="41c20-141">On input, a pointer to an [**ISCardCmd**](iscardcmd.md) interface object or **NULL**.</span></span>

<span data-ttu-id="41c20-142">Al ritorno, viene compilato con il comando APDU creato da questa operazione.</span><span class="sxs-lookup"><span data-stu-id="41c20-142">On return, it is filled with the APDU command constructed by this operation.</span></span> <span data-ttu-id="41c20-143">Se *ppCmd* è stato impostato su **null**, un oggetto [**ISCardCmd**](iscardcmd.md) della [*Smart Card*](../secgloss/s-gly.md) viene creato e restituito internamente utilizzando il puntatore *ppCmd* .</span><span class="sxs-lookup"><span data-stu-id="41c20-143">If *ppCmd* was set to **NULL**, a [*smart card*](../secgloss/s-gly.md) [**ISCardCmd**](iscardcmd.md) object is internally created and returned using the *ppCmd* pointer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="41c20-144">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="41c20-144">Return value</span></span>

<span data-ttu-id="41c20-145">Il metodo restituisce uno dei valori possibili seguenti.</span><span class="sxs-lookup"><span data-stu-id="41c20-145">The method returns one of the following possible values.</span></span>



| <span data-ttu-id="41c20-146">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="41c20-146">Return code</span></span>                                                                                   | <span data-ttu-id="41c20-147">Descrizione</span><span class="sxs-lookup"><span data-stu-id="41c20-147">Description</span></span>                                  |
|-----------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="41c20-148"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="41c20-148"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="41c20-149">Operazione completata correttamente.</span><span class="sxs-lookup"><span data-stu-id="41c20-149">Operation completed successfully.</span></span><br/> |
| <dl> <span data-ttu-id="41c20-150"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="41c20-150"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="41c20-151">Parametro non valido.</span><span class="sxs-lookup"><span data-stu-id="41c20-151">Invalid parameter.</span></span><br/>                |
| <dl> <span data-ttu-id="41c20-152"><dt>**\_puntatore E**</dt></span><span class="sxs-lookup"><span data-stu-id="41c20-152"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="41c20-153">È stato passato un puntatore non valido.</span><span class="sxs-lookup"><span data-stu-id="41c20-153">A bad pointer was passed in.</span></span><br/>      |
| <dl> <span data-ttu-id="41c20-154"><dt>**E \_ OutOfMemory**</dt></span><span class="sxs-lookup"><span data-stu-id="41c20-154"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="41c20-155">Memoria insufficiente.</span><span class="sxs-lookup"><span data-stu-id="41c20-155">Out of memory.</span></span><br/>                    |



 

## <a name="remarks"></a><span data-ttu-id="41c20-156">Commenti</span><span class="sxs-lookup"><span data-stu-id="41c20-156">Remarks</span></span>

<span data-ttu-id="41c20-157">La corretta esecuzione del comando può essere soggetta a un completamento corretto dei comandi precedenti (ad esempio, VERIFY o SELECT FILE) o Selects (ad esempio, il segreto pertinente).</span><span class="sxs-lookup"><span data-stu-id="41c20-157">The successful execution of the command may be subject to successful completion of prior commands (for example, VERIFY or SELECT FILE) or selections (for example, the relevant secret).</span></span>

<span data-ttu-id="41c20-158">Se durante l'esecuzione del comando sono attualmente selezionati una chiave e un algoritmo, il comando può usare in modo implicito la chiave e l'algoritmo.</span><span class="sxs-lookup"><span data-stu-id="41c20-158">If a key and an algorithm are currently selected when issuing the command, then the command may implicitly use the key and the algorithm.</span></span>

<span data-ttu-id="41c20-159">Il numero di volte in cui il comando viene emesso può essere registrato nella scheda per limitare il numero di tentativi successivi di utilizzo del segreto pertinente o dell'algoritmo.</span><span class="sxs-lookup"><span data-stu-id="41c20-159">The number of times the command is issued may be recorded in the card to limit the number of further attempts of using the relevant secret or the algorithm.</span></span>

<span data-ttu-id="41c20-160">Per un elenco di tutti i metodi forniti da questa interfaccia, vedere [**ISCardISO7816**](iscardiso7816.md).</span><span class="sxs-lookup"><span data-stu-id="41c20-160">For a list of all the methods provided by this interface, see [**ISCardISO7816**](iscardiso7816.md).</span></span>

<span data-ttu-id="41c20-161">Oltre ai codici di errore COM elencati sopra, questa interfaccia può restituire un codice di errore della smart card se è stata chiamata una funzione Smart Card per completare la richiesta.</span><span class="sxs-lookup"><span data-stu-id="41c20-161">In addition to the COM error codes listed above, this interface may return a smart card error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="41c20-162">Per ulteriori informazioni, vedere [valori restituiti della smart card](authentication-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="41c20-162">For more information, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="41c20-163">Requisiti</span><span class="sxs-lookup"><span data-stu-id="41c20-163">Requirements</span></span>



| <span data-ttu-id="41c20-164">Requisito</span><span class="sxs-lookup"><span data-stu-id="41c20-164">Requirement</span></span> | <span data-ttu-id="41c20-165">Valore</span><span class="sxs-lookup"><span data-stu-id="41c20-165">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="41c20-166">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="41c20-166">Minimum supported client</span></span><br/> | <span data-ttu-id="41c20-167">\[Solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="41c20-167">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="41c20-168">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="41c20-168">Minimum supported server</span></span><br/> | <span data-ttu-id="41c20-169">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="41c20-169">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="41c20-170">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="41c20-170">End of client support</span></span><br/>    | <span data-ttu-id="41c20-171">Windows XP</span><span class="sxs-lookup"><span data-stu-id="41c20-171">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="41c20-172">Fine del supporto server</span><span class="sxs-lookup"><span data-stu-id="41c20-172">End of server support</span></span><br/>    | <span data-ttu-id="41c20-173">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="41c20-173">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="41c20-174">Intestazione</span><span class="sxs-lookup"><span data-stu-id="41c20-174">Header</span></span><br/>                   | <dl> <span data-ttu-id="41c20-175"><dt>Scardssp. h</dt></span><span class="sxs-lookup"><span data-stu-id="41c20-175"><dt>Scardssp.h</dt></span></span> </dl>   |
| <span data-ttu-id="41c20-176">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="41c20-176">Type library</span></span><br/>             | <dl> <span data-ttu-id="41c20-177"><dt>Scardsrv. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="41c20-177"><dt>Scardsrv.tlb</dt></span></span> </dl> |
| <span data-ttu-id="41c20-178">DLL</span><span class="sxs-lookup"><span data-stu-id="41c20-178">DLL</span></span><br/>                      | <dl> <span data-ttu-id="41c20-179"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="41c20-179"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="41c20-180">IID</span><span class="sxs-lookup"><span data-stu-id="41c20-180">IID</span></span><br/>                      | <span data-ttu-id="41c20-181">IID \_ ISCardISO7816 è definito come 53B6AA68-3F56-11D0-916B-00AA00C18068</span><span class="sxs-lookup"><span data-stu-id="41c20-181">IID\_ISCardISO7816 is defined as 53B6AA68-3F56-11D0-916B-00AA00C18068</span></span><br/>        |



## <a name="see-also"></a><span data-ttu-id="41c20-182">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="41c20-182">See also</span></span>

<dl> <dt>

[<span data-ttu-id="41c20-183">**ExternalAuthenticate**</span><span class="sxs-lookup"><span data-stu-id="41c20-183">**ExternalAuthenticate**</span></span>](iscardiso7816-externalauthenticate.md)
</dt> <dt>

[<span data-ttu-id="41c20-184">**ISCardISO7816**</span><span class="sxs-lookup"><span data-stu-id="41c20-184">**ISCardISO7816**</span></span>](iscardiso7816.md)
</dt> </dl>

 

 
