---
description: Il metodo ReadBinary costruisce un comando APDU (Application Protocol Data Unit) che acquisisce un messaggio di risposta che fornisce tale parte del contenuto di un file elementare con struttura trasparente.
ms.assetid: 15394c21-1e07-4ea1-8f11-817e07b31f9b
title: 'Metodo ISCardISO7816:: ReadBinary (scardssp. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardISO7816.ReadBinary
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: a29093d8725a3390df9837f4e2f395cfcf2eef29
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103884490"
---
# <a name="iscardiso7816readbinary-method"></a><span data-ttu-id="0eb7f-103">Metodo ISCardISO7816:: ReadBinary</span><span class="sxs-lookup"><span data-stu-id="0eb7f-103">ISCardISO7816::ReadBinary method</span></span>

<span data-ttu-id="0eb7f-104">\[Il metodo **ReadBinary** è disponibile per l'uso nei sistemi operativi specificati nella sezione requisiti.</span><span class="sxs-lookup"><span data-stu-id="0eb7f-104">\[The **ReadBinary** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="0eb7f-105">Non è disponibile per l'utilizzo in Windows Server 2003 con Service Pack 1 (SP1) e versioni successive, Windows Vista, Windows Server 2008 e versioni successive del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="0eb7f-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="0eb7f-106">I [moduli Smart Card](/previous-versions/windows/desktop/secsmart/smart-card-modules) offrono funzionalità simili.\]</span><span class="sxs-lookup"><span data-stu-id="0eb7f-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="0eb7f-107">Il metodo **ReadBinary** costruisce un comando APDU ( [*Application Protocol Data Unit*](../secgloss/a-gly.md) ) che acquisisce un messaggio di risposta che fornisce tale parte del contenuto di un file elementare con struttura trasparente.</span><span class="sxs-lookup"><span data-stu-id="0eb7f-107">The **ReadBinary** method constructs an [*application protocol data unit*](../secgloss/a-gly.md) (APDU) command that acquires a response message that gives that part of the contents of a transparent-structured elementary file.</span></span>

## <a name="syntax"></a><span data-ttu-id="0eb7f-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="0eb7f-108">Syntax</span></span>


```C++
HRESULT ReadBinary(
  [in]      BYTE       byP1,
  [in]      BYTE       byP2,
  [in]      LONG       lBytesToRead,
  [in, out] LPSCARDCMD *ppCmd
);
```



## <a name="parameters"></a><span data-ttu-id="0eb7f-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="0eb7f-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0eb7f-110">*byP1* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="0eb7f-110">*byP1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0eb7f-111">Il campo P1-P2, offset al primo byte da leggere dall'inizio del file.</span><span class="sxs-lookup"><span data-stu-id="0eb7f-111">The P1-P2 field, offset to the first byte to be read from the beginning of the file.</span></span> <span data-ttu-id="0eb7f-112">Se B8 = 1 in P1, B7 e B6 di P1 sono impostati su zero (RFU bit), B5 a B1 di P1 sono un identificatore EF breve e P2 è l'offset del primo byte da leggere in unità dati dall'inizio del file.</span><span class="sxs-lookup"><span data-stu-id="0eb7f-112">If b8=1 in P1, then b7 and b6 of P1 are set to zero (RFU bits), b5 to b1 of P1 are a short EF identifier and P2 is the offset of the first byte to be read in data units from the beginning of the file.</span></span> <span data-ttu-id="0eb7f-113">Se B8 = 0 in P1, P1 \| \| P2 è l'offset del primo byte da leggere nelle unità dati dall'inizio del file.</span><span class="sxs-lookup"><span data-stu-id="0eb7f-113">If b8=0 in P1, then P1\|\|P2 is the offset of the first byte to be read in data units from the beginning of the file.</span></span>

</dd> <dt>

<span data-ttu-id="0eb7f-114">*byP2* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="0eb7f-114">*byP2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0eb7f-115">Il campo P1-P2, offset al primo byte da leggere dall'inizio del file.</span><span class="sxs-lookup"><span data-stu-id="0eb7f-115">The P1-P2 field, offset to the first byte to be read from the beginning of the file.</span></span> <span data-ttu-id="0eb7f-116">Se B8 = 1 in P1, B7 e B6 di P1 sono impostati su zero (RFU bit), B5 a B1 di P1 sono un identificatore EF breve e P2 è l'offset del primo byte da leggere in unità dati dall'inizio del file.</span><span class="sxs-lookup"><span data-stu-id="0eb7f-116">If b8=1 in P1, then b7 and b6 of P1 are set to zero (RFU bits), b5 to b1 of P1 are a short EF identifier and P2 is the offset of the first byte to be read in data units from the beginning of the file.</span></span> <span data-ttu-id="0eb7f-117">Se B8 = 0 in P1, P1 \| \| P2 è l'offset del primo byte da leggere nelle unità dati dall'inizio del file.</span><span class="sxs-lookup"><span data-stu-id="0eb7f-117">If b8=0 in P1, then P1\|\|P2 is the offset of the first byte to be read in data units from the beginning of the file.</span></span>

</dd> <dt>

<span data-ttu-id="0eb7f-118">*lBytesToRead* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="0eb7f-118">*lBytesToRead* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0eb7f-119">Numero di byte da leggere dall'EF trasparente.</span><span class="sxs-lookup"><span data-stu-id="0eb7f-119">Number of bytes to read from the transparent EF.</span></span>

<span data-ttu-id="0eb7f-120">Se il campo le contiene solo zeri, entro il limite di 256 per la lunghezza breve o 65536 per la lunghezza estesa, tutti i byte fino alla fine del file devono essere letti.</span><span class="sxs-lookup"><span data-stu-id="0eb7f-120">If the Le field contains only zeros, then within the limit of 256 for short length or 65536 for extended length, all the bytes until the end of the file should be read.</span></span>

</dd> <dt>

<span data-ttu-id="0eb7f-121">*ppCmd* \[ in uscita\]</span><span class="sxs-lookup"><span data-stu-id="0eb7f-121">*ppCmd* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="0eb7f-122">In input, un puntatore a un oggetto di interfaccia [**ISCardCmd**](iscardcmd.md) o **null**.</span><span class="sxs-lookup"><span data-stu-id="0eb7f-122">On input, a pointer to an [**ISCardCmd**](iscardcmd.md) interface object or **NULL**.</span></span>

<span data-ttu-id="0eb7f-123">Al ritorno, viene compilato con il comando APDU creato da questa operazione.</span><span class="sxs-lookup"><span data-stu-id="0eb7f-123">On return, it is filled with the APDU command constructed by this operation.</span></span> <span data-ttu-id="0eb7f-124">Se *ppCmd* è stato impostato su **null**, un oggetto [**ISCardCmd**](iscardcmd.md) della [*Smart Card*](../secgloss/s-gly.md) viene creato e restituito internamente utilizzando il puntatore *ppCmd* .</span><span class="sxs-lookup"><span data-stu-id="0eb7f-124">If *ppCmd* was set to **NULL**, a [*smart card*](../secgloss/s-gly.md) [**ISCardCmd**](iscardcmd.md) object is internally created and returned using the *ppCmd* pointer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0eb7f-125">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="0eb7f-125">Return value</span></span>

<span data-ttu-id="0eb7f-126">Il metodo restituisce uno dei valori possibili seguenti.</span><span class="sxs-lookup"><span data-stu-id="0eb7f-126">The method returns one of the following possible values.</span></span>



| <span data-ttu-id="0eb7f-127">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="0eb7f-127">Return code</span></span>                                                                                   | <span data-ttu-id="0eb7f-128">Descrizione</span><span class="sxs-lookup"><span data-stu-id="0eb7f-128">Description</span></span>                                  |
|-----------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="0eb7f-129"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="0eb7f-129"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="0eb7f-130">Operazione completata correttamente.</span><span class="sxs-lookup"><span data-stu-id="0eb7f-130">Operation completed successfully.</span></span><br/> |
| <dl> <span data-ttu-id="0eb7f-131"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="0eb7f-131"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="0eb7f-132">Parametro non valido.</span><span class="sxs-lookup"><span data-stu-id="0eb7f-132">Invalid parameter.</span></span><br/>                |
| <dl> <span data-ttu-id="0eb7f-133"><dt>**\_puntatore E**</dt></span><span class="sxs-lookup"><span data-stu-id="0eb7f-133"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="0eb7f-134">È stato passato un puntatore non valido.</span><span class="sxs-lookup"><span data-stu-id="0eb7f-134">A bad pointer was passed in.</span></span><br/>      |
| <dl> <span data-ttu-id="0eb7f-135"><dt>**E \_ OutOfMemory**</dt></span><span class="sxs-lookup"><span data-stu-id="0eb7f-135"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="0eb7f-136">Memoria insufficiente.</span><span class="sxs-lookup"><span data-stu-id="0eb7f-136">Out of memory.</span></span><br/>                    |



 

## <a name="remarks"></a><span data-ttu-id="0eb7f-137">Commenti</span><span class="sxs-lookup"><span data-stu-id="0eb7f-137">Remarks</span></span>

<span data-ttu-id="0eb7f-138">Il comando incapsulato può essere eseguito solo se lo stato di sicurezza della [*Smart Card*](../secgloss/s-gly.md) soddisfa gli attributi di sicurezza del file elementare elaborato.</span><span class="sxs-lookup"><span data-stu-id="0eb7f-138">The encapsulated command can only be performed if the security status of the [*smart card*](../secgloss/s-gly.md) satisfies the security attributes of the elementary file being processed.</span></span>

<span data-ttu-id="0eb7f-139">Quando il comando contiene un identificatore elementare breve valido, imposta il file come file elementare corrente.</span><span class="sxs-lookup"><span data-stu-id="0eb7f-139">When the command contains a valid short elementary identifier, it sets the file as current elementary file.</span></span>

<span data-ttu-id="0eb7f-140">Non è possibile cancellare i file elementari senza una struttura trasparente.</span><span class="sxs-lookup"><span data-stu-id="0eb7f-140">Elementary files without a transparent structure cannot be erased.</span></span> <span data-ttu-id="0eb7f-141">Il comando incapsulato viene interrotto se applicato a un file elementare senza una struttura trasparente.</span><span class="sxs-lookup"><span data-stu-id="0eb7f-141">The encapsulated command aborts if applied to an elementary file without a transparent structure.</span></span>

<span data-ttu-id="0eb7f-142">Per un elenco di tutti i metodi forniti da questa interfaccia, vedere [**ISCardISO7816**](iscardiso7816.md).</span><span class="sxs-lookup"><span data-stu-id="0eb7f-142">For a list of all the methods provided by this interface, see [**ISCardISO7816**](iscardiso7816.md).</span></span>

<span data-ttu-id="0eb7f-143">Oltre ai codici di errore COM elencati sopra, questa interfaccia può restituire un codice di errore della smart card se è stata chiamata una funzione Smart Card per completare la richiesta.</span><span class="sxs-lookup"><span data-stu-id="0eb7f-143">In addition to the COM error codes listed above, this interface may return a smart card error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="0eb7f-144">Per ulteriori informazioni, vedere [valori restituiti della smart card](authentication-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="0eb7f-144">For more information, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="0eb7f-145">Requisiti</span><span class="sxs-lookup"><span data-stu-id="0eb7f-145">Requirements</span></span>



| <span data-ttu-id="0eb7f-146">Requisito</span><span class="sxs-lookup"><span data-stu-id="0eb7f-146">Requirement</span></span> | <span data-ttu-id="0eb7f-147">Valore</span><span class="sxs-lookup"><span data-stu-id="0eb7f-147">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="0eb7f-148">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0eb7f-148">Minimum supported client</span></span><br/> | <span data-ttu-id="0eb7f-149">\[Solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="0eb7f-149">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="0eb7f-150">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0eb7f-150">Minimum supported server</span></span><br/> | <span data-ttu-id="0eb7f-151">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="0eb7f-151">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="0eb7f-152">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="0eb7f-152">End of client support</span></span><br/>    | <span data-ttu-id="0eb7f-153">Windows XP</span><span class="sxs-lookup"><span data-stu-id="0eb7f-153">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="0eb7f-154">Fine del supporto server</span><span class="sxs-lookup"><span data-stu-id="0eb7f-154">End of server support</span></span><br/>    | <span data-ttu-id="0eb7f-155">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="0eb7f-155">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="0eb7f-156">Intestazione</span><span class="sxs-lookup"><span data-stu-id="0eb7f-156">Header</span></span><br/>                   | <dl> <span data-ttu-id="0eb7f-157"><dt>Scardssp. h</dt></span><span class="sxs-lookup"><span data-stu-id="0eb7f-157"><dt>Scardssp.h</dt></span></span> </dl>   |
| <span data-ttu-id="0eb7f-158">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="0eb7f-158">Type library</span></span><br/>             | <dl> <span data-ttu-id="0eb7f-159"><dt>Scardsrv. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="0eb7f-159"><dt>Scardsrv.tlb</dt></span></span> </dl> |
| <span data-ttu-id="0eb7f-160">DLL</span><span class="sxs-lookup"><span data-stu-id="0eb7f-160">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0eb7f-161"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0eb7f-161"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="0eb7f-162">IID</span><span class="sxs-lookup"><span data-stu-id="0eb7f-162">IID</span></span><br/>                      | <span data-ttu-id="0eb7f-163">IID \_ ISCardISO7816 è definito come 53B6AA68-3F56-11D0-916B-00AA00C18068</span><span class="sxs-lookup"><span data-stu-id="0eb7f-163">IID\_ISCardISO7816 is defined as 53B6AA68-3F56-11D0-916B-00AA00C18068</span></span><br/>        |



## <a name="see-also"></a><span data-ttu-id="0eb7f-164">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="0eb7f-164">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0eb7f-165">**EraseBinary**</span><span class="sxs-lookup"><span data-stu-id="0eb7f-165">**EraseBinary**</span></span>](iscardiso7816-erasebinary.md)
</dt> <dt>

[<span data-ttu-id="0eb7f-166">**ISCardISO7816**</span><span class="sxs-lookup"><span data-stu-id="0eb7f-166">**ISCardISO7816**</span></span>](iscardiso7816.md)
</dt> <dt>

[<span data-ttu-id="0eb7f-167">**UpdateBinary**</span><span class="sxs-lookup"><span data-stu-id="0eb7f-167">**UpdateBinary**</span></span>](iscardiso7816-updatebinary.md)
</dt> <dt>

[<span data-ttu-id="0eb7f-168">**WriteBinary**</span><span class="sxs-lookup"><span data-stu-id="0eb7f-168">**WriteBinary**</span></span>](iscardiso7816-writebinary.md)
</dt> </dl>

 

 
