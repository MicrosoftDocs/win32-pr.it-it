---
description: Il metodo WriteBinary costruisce un comando APDU (Application Protocol Data Unit) che scrive valori binari in un file elementare.
ms.assetid: e38273d5-4eb0-4c0b-829a-c78e511a38bc
title: 'Metodo ISCardISO7816:: WriteBinary (scardssp. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardISO7816.WriteBinary
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 330e817bc501c451026589087991fb43c0b5ac57
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103966453"
---
# <a name="iscardiso7816writebinary-method"></a><span data-ttu-id="00a29-103">Metodo ISCardISO7816:: WriteBinary</span><span class="sxs-lookup"><span data-stu-id="00a29-103">ISCardISO7816::WriteBinary method</span></span>

<span data-ttu-id="00a29-104">\[Il metodo **WriteBinary** è disponibile per l'uso nei sistemi operativi specificati nella sezione requisiti.</span><span class="sxs-lookup"><span data-stu-id="00a29-104">\[The **WriteBinary** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="00a29-105">Non è disponibile per l'utilizzo in Windows Server 2003 con Service Pack 1 (SP1) e versioni successive, Windows Vista, Windows Server 2008 e versioni successive del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="00a29-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="00a29-106">I [moduli Smart Card](/previous-versions/windows/desktop/secsmart/smart-card-modules) offrono funzionalità simili.\]</span><span class="sxs-lookup"><span data-stu-id="00a29-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="00a29-107">Il metodo **WriteBinary** costruisce un comando APDU ( [*Application Protocol Data Unit*](../secgloss/a-gly.md) ) che scrive valori binari in un file elementare.</span><span class="sxs-lookup"><span data-stu-id="00a29-107">The **WriteBinary** method constructs an [*application protocol data unit*](../secgloss/a-gly.md) (APDU) command that writes binary values into an elementary file.</span></span>

<span data-ttu-id="00a29-108">A seconda degli attributi del file, il comando esegue una delle operazioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="00a29-108">Depending upon the file attributes, the command performs one of the following operations:</span></span>

-   <span data-ttu-id="00a29-109">L'OR logico dei bit già presenti nella scheda con i bit specificati nel comando APDU (lo stato di cancellazione logica dei bit del file è 0).</span><span class="sxs-lookup"><span data-stu-id="00a29-109">The logical OR of the bits already present in the card with the bits given in the command APDU (logical erased state of the bits of the file is 0).</span></span>
-   <span data-ttu-id="00a29-110">Il AND logico dei bit già presenti nella scheda con i bit specificati nel comando APDU (lo stato di cancellazione logica dei bit del file è 1).</span><span class="sxs-lookup"><span data-stu-id="00a29-110">The logical AND of the bits already present in the card with the bits given in the command APDU (logical erased state of the bits of the file is 1).</span></span>
-   <span data-ttu-id="00a29-111">Scrittura singola nella scheda dei bit specificati nel comando APDU.</span><span class="sxs-lookup"><span data-stu-id="00a29-111">The one-time write in the card of the bits given in the command APDU.</span></span>

<span data-ttu-id="00a29-112">Quando non viene specificata alcuna indicazione nel byte di codifica dei dati, viene applicato il comportamento logico OR.</span><span class="sxs-lookup"><span data-stu-id="00a29-112">When no indication is given in the data coding byte, the logical OR behavior applies.</span></span>

## <a name="syntax"></a><span data-ttu-id="00a29-113">Sintassi</span><span class="sxs-lookup"><span data-stu-id="00a29-113">Syntax</span></span>


```C++
HRESULT WriteBinary(
  [in]      BYTE         byP1,
  [in]      BYTE         byP2,
  [in]      LPBYTEBUFFER pData,
  [in, out] LPSCARDCMD   *ppCmd
);
```



## <a name="parameters"></a><span data-ttu-id="00a29-114">Parametri</span><span class="sxs-lookup"><span data-stu-id="00a29-114">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="00a29-115">*byP1* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="00a29-115">*byP1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="00a29-116">Offset alla posizione di scrittura dall'inizio del file binario (EF).</span><span class="sxs-lookup"><span data-stu-id="00a29-116">Offset to the write location from the beginning of the binary file (EF).</span></span> <span data-ttu-id="00a29-117">Se B8 = 1 in P1, B7 e B6 di P1 sono impostati su zero (RFU bit), B5 a B1 di P1 sono un identificatore EF breve e P2 è l'offset del primo byte da scrivere in unità dati dall'inizio del file.</span><span class="sxs-lookup"><span data-stu-id="00a29-117">If b8=1 in P1, then b7 and b6 of P1 are set to zero (RFU bits), b5 to b1 of P1 are a short EF identifier and P2 is the offset of the first byte to be written in data units from the beginning of the file.</span></span> <span data-ttu-id="00a29-118">Se B8 = 0 in P1, P1 \| \| P2 è l'offset del primo byte da scrivere in unità dati a partire dall'inizio del file.</span><span class="sxs-lookup"><span data-stu-id="00a29-118">If b8=0 in P1, then P1\|\|P2 is the offset of the first byte to be written in data units from the beginning of the file.</span></span>

</dd> <dt>

<span data-ttu-id="00a29-119">*byP2* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="00a29-119">*byP2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="00a29-120">Offset alla posizione di scrittura dall'inizio del file binario (EF).</span><span class="sxs-lookup"><span data-stu-id="00a29-120">Offset to the write location from the beginning of the binary file (EF).</span></span> <span data-ttu-id="00a29-121">Se B8 = 1 in P1, B7 e B6 di P1 sono impostati su zero (RFU bit), B5 a B1 di P1 sono un identificatore EF breve e P2 è l'offset del primo byte da scrivere in unità dati dall'inizio del file.</span><span class="sxs-lookup"><span data-stu-id="00a29-121">If b8=1 in P1, then b7 and b6 of P1 are set to zero (RFU bits), b5 to b1 of P1 are a short EF identifier and P2 is the offset of the first byte to be written in data units from the beginning of the file.</span></span> <span data-ttu-id="00a29-122">Se B8 = 0 in P1, P1 \| \| P2 è l'offset del primo byte da scrivere in unità dati a partire dall'inizio del file.</span><span class="sxs-lookup"><span data-stu-id="00a29-122">If b8=0 in P1, then P1\|\|P2 is the offset of the first byte to be written in data units from the beginning of the file.</span></span>

</dd> <dt>

<span data-ttu-id="00a29-123">*pData* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="00a29-123">*pData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="00a29-124">Puntatore alla stringa di unità dati da scrivere.</span><span class="sxs-lookup"><span data-stu-id="00a29-124">Pointer to the string of data units to be written.</span></span>

</dd> <dt>

<span data-ttu-id="00a29-125">*ppCmd* \[ in uscita\]</span><span class="sxs-lookup"><span data-stu-id="00a29-125">*ppCmd* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="00a29-126">In input, un puntatore a un oggetto di interfaccia [**ISCardCmd**](iscardcmd.md) o **null**.</span><span class="sxs-lookup"><span data-stu-id="00a29-126">On input, a pointer to an [**ISCardCmd**](iscardcmd.md) interface object or **NULL**.</span></span>

<span data-ttu-id="00a29-127">Al ritorno, viene compilato con il comando APDU creato da questa operazione.</span><span class="sxs-lookup"><span data-stu-id="00a29-127">On return, it is filled with the APDU command constructed by this operation.</span></span> <span data-ttu-id="00a29-128">Se *ppCmd* è stato impostato su **null**, un oggetto [**ISCardCmd**](iscardcmd.md) della [*Smart Card*](../secgloss/s-gly.md) viene creato e restituito internamente tramite il puntatore *ppCmd* .</span><span class="sxs-lookup"><span data-stu-id="00a29-128">If *ppCmd* was set to **NULL**, a [*smart card*](../secgloss/s-gly.md) [**ISCardCmd**](iscardcmd.md) object is internally created and returned via the *ppCmd* pointer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="00a29-129">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="00a29-129">Return value</span></span>

<span data-ttu-id="00a29-130">Il metodo restituisce uno dei valori possibili seguenti.</span><span class="sxs-lookup"><span data-stu-id="00a29-130">The method returns one of the following possible values.</span></span>



| <span data-ttu-id="00a29-131">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="00a29-131">Return code</span></span>                                                                                   | <span data-ttu-id="00a29-132">Descrizione</span><span class="sxs-lookup"><span data-stu-id="00a29-132">Description</span></span>                                  |
|-----------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="00a29-133"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="00a29-133"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="00a29-134">Operazione completata correttamente.</span><span class="sxs-lookup"><span data-stu-id="00a29-134">Operation completed successfully.</span></span><br/> |
| <dl> <span data-ttu-id="00a29-135"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="00a29-135"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="00a29-136">Parametro non valido.</span><span class="sxs-lookup"><span data-stu-id="00a29-136">Invalid parameter.</span></span><br/>                |
| <dl> <span data-ttu-id="00a29-137"><dt>**\_puntatore E**</dt></span><span class="sxs-lookup"><span data-stu-id="00a29-137"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="00a29-138">È stato passato un puntatore non valido.</span><span class="sxs-lookup"><span data-stu-id="00a29-138">A bad pointer was passed in.</span></span><br/>      |
| <dl> <span data-ttu-id="00a29-139"><dt>**E \_ OutOfMemory**</dt></span><span class="sxs-lookup"><span data-stu-id="00a29-139"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="00a29-140">Memoria insufficiente.</span><span class="sxs-lookup"><span data-stu-id="00a29-140">Out of memory.</span></span><br/>                    |



 

## <a name="remarks"></a><span data-ttu-id="00a29-141">Commenti</span><span class="sxs-lookup"><span data-stu-id="00a29-141">Remarks</span></span>

<span data-ttu-id="00a29-142">Il comando incapsulato può essere eseguito solo se lo stato di sicurezza della [*Smart Card*](../secgloss/s-gly.md) soddisfa gli attributi di sicurezza del file elementare elaborato.</span><span class="sxs-lookup"><span data-stu-id="00a29-142">The encapsulated command can only be performed if the security status of the [*smart card*](../secgloss/s-gly.md) satisfies the security attributes of the elementary file being processed.</span></span>

<span data-ttu-id="00a29-143">Quando il comando contiene un identificatore elementare breve valido, imposta il file come file elementare corrente.</span><span class="sxs-lookup"><span data-stu-id="00a29-143">When the command contains a valid short elementary identifier, it sets the file as current elementary file.</span></span>

<span data-ttu-id="00a29-144">Quando un'operazione di scrittura binaria è stata applicata a un'unità dati di un EF di scrittura monouso, eventuali altre operazioni di scrittura che fanno riferimento a questa unità dati verranno interrotte se il contenuto dell'unità dati o l'indicatore di stato cancellato logico (se presente) collegato a questa unità dati è diverso dallo stato di cancellazione logica.</span><span class="sxs-lookup"><span data-stu-id="00a29-144">When a write binary operation has been applied to a data unit of a one-time write EF, any further write operation referring to this data unit will be aborted if the content of the data unit or the logical erased state indicator (if any) attached to this data unit is different from the logical erased state.</span></span>

<span data-ttu-id="00a29-145">Non è possibile scrivere i file elementari senza una struttura trasparente.</span><span class="sxs-lookup"><span data-stu-id="00a29-145">Elementary files without a transparent structure cannot be written to.</span></span> <span data-ttu-id="00a29-146">Il comando incapsulato viene interrotto se applicato a un file elementare senza una struttura trasparente.</span><span class="sxs-lookup"><span data-stu-id="00a29-146">The encapsulated command aborts if applied to an elementary file without a transparent structure.</span></span>

<span data-ttu-id="00a29-147">Per un elenco di tutti i metodi forniti da questa interfaccia, vedere [**ISCardISO7816**](iscardiso7816.md).</span><span class="sxs-lookup"><span data-stu-id="00a29-147">For a list of all the methods provided by this interface, see [**ISCardISO7816**](iscardiso7816.md).</span></span>

<span data-ttu-id="00a29-148">Oltre ai codici di errore COM elencati sopra, questa interfaccia può restituire un codice di errore della smart card se è stata chiamata una funzione Smart Card per completare la richiesta.</span><span class="sxs-lookup"><span data-stu-id="00a29-148">In addition to the COM error codes listed above, this interface may return a smart card error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="00a29-149">Per ulteriori informazioni, vedere [valori restituiti della smart card](authentication-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="00a29-149">For more information, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="00a29-150">Requisiti</span><span class="sxs-lookup"><span data-stu-id="00a29-150">Requirements</span></span>



| <span data-ttu-id="00a29-151">Requisito</span><span class="sxs-lookup"><span data-stu-id="00a29-151">Requirement</span></span> | <span data-ttu-id="00a29-152">Valore</span><span class="sxs-lookup"><span data-stu-id="00a29-152">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="00a29-153">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="00a29-153">Minimum supported client</span></span><br/> | <span data-ttu-id="00a29-154">\[Solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="00a29-154">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="00a29-155">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="00a29-155">Minimum supported server</span></span><br/> | <span data-ttu-id="00a29-156">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="00a29-156">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="00a29-157">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="00a29-157">End of client support</span></span><br/>    | <span data-ttu-id="00a29-158">Windows XP</span><span class="sxs-lookup"><span data-stu-id="00a29-158">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="00a29-159">Fine del supporto server</span><span class="sxs-lookup"><span data-stu-id="00a29-159">End of server support</span></span><br/>    | <span data-ttu-id="00a29-160">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="00a29-160">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="00a29-161">Intestazione</span><span class="sxs-lookup"><span data-stu-id="00a29-161">Header</span></span><br/>                   | <dl> <span data-ttu-id="00a29-162"><dt>Scardssp. h</dt></span><span class="sxs-lookup"><span data-stu-id="00a29-162"><dt>Scardssp.h</dt></span></span> </dl>   |
| <span data-ttu-id="00a29-163">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="00a29-163">Type library</span></span><br/>             | <dl> <span data-ttu-id="00a29-164"><dt>Scardsrv. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="00a29-164"><dt>Scardsrv.tlb</dt></span></span> </dl> |
| <span data-ttu-id="00a29-165">DLL</span><span class="sxs-lookup"><span data-stu-id="00a29-165">DLL</span></span><br/>                      | <dl> <span data-ttu-id="00a29-166"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="00a29-166"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="00a29-167">IID</span><span class="sxs-lookup"><span data-stu-id="00a29-167">IID</span></span><br/>                      | <span data-ttu-id="00a29-168">IID \_ ISCardISO7816 è definito come 53B6AA68-3F56-11D0-916B-00AA00C18068</span><span class="sxs-lookup"><span data-stu-id="00a29-168">IID\_ISCardISO7816 is defined as 53B6AA68-3F56-11D0-916B-00AA00C18068</span></span><br/>        |



## <a name="see-also"></a><span data-ttu-id="00a29-169">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="00a29-169">See also</span></span>

<dl> <dt>

[<span data-ttu-id="00a29-170">**EraseBinary**</span><span class="sxs-lookup"><span data-stu-id="00a29-170">**EraseBinary**</span></span>](iscardiso7816-erasebinary.md)
</dt> <dt>

[<span data-ttu-id="00a29-171">**ISCardISO7816**</span><span class="sxs-lookup"><span data-stu-id="00a29-171">**ISCardISO7816**</span></span>](iscardiso7816.md)
</dt> <dt>

[<span data-ttu-id="00a29-172">**ReadBinary**</span><span class="sxs-lookup"><span data-stu-id="00a29-172">**ReadBinary**</span></span>](iscardiso7816-readbinary.md)
</dt> <dt>

[<span data-ttu-id="00a29-173">**UpdateBinary**</span><span class="sxs-lookup"><span data-stu-id="00a29-173">**UpdateBinary**</span></span>](iscardiso7816-updatebinary.md)
</dt> </dl>

 

 
