---
description: Costruisce un comando APDU (Application Protocol Data Unit) che imposta sequenzialmente parte del contenuto di un file elementare sullo stato logico cancellato, a partire da un offset specificato.
ms.assetid: 89e2371e-e27d-475b-9427-bbf6d614c473
title: 'Metodo ISCardISO7816:: EraseBinary (scardssp. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardISO7816.EraseBinary
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: a9bad21bbb35b7ac16209ac0075267ef7300fe21
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106317747"
---
# <a name="iscardiso7816erasebinary-method"></a><span data-ttu-id="a65b2-103">Metodo ISCardISO7816:: EraseBinary</span><span class="sxs-lookup"><span data-stu-id="a65b2-103">ISCardISO7816::EraseBinary method</span></span>

<span data-ttu-id="a65b2-104">\[Il metodo **EraseBinary** è disponibile per l'uso nei sistemi operativi specificati nella sezione requisiti.</span><span class="sxs-lookup"><span data-stu-id="a65b2-104">\[The **EraseBinary** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="a65b2-105">Non è disponibile per l'utilizzo in Windows Server 2003 con Service Pack 1 (SP1) e versioni successive, Windows Vista, Windows Server 2008 e versioni successive del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="a65b2-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="a65b2-106">I [moduli Smart Card](/previous-versions/windows/desktop/secsmart/smart-card-modules) offrono funzionalità simili.\]</span><span class="sxs-lookup"><span data-stu-id="a65b2-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="a65b2-107">Il metodo **EraseBinary** costruisce un comando APDU ( [*Application Protocol Data Unit*](../secgloss/a-gly.md) ) che imposta sequenzialmente parte del contenuto di un file elementare sullo stato logico cancellato, a partire da un offset specificato.</span><span class="sxs-lookup"><span data-stu-id="a65b2-107">The **EraseBinary** method constructs an [*application protocol data unit*](../secgloss/a-gly.md) (APDU) command that sequentially sets part of the content of an elementary file to its logical erased state, starting from a given offset.</span></span>

## <a name="syntax"></a><span data-ttu-id="a65b2-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="a65b2-108">Syntax</span></span>


```C++
HRESULT EraseBinary(
  [in]      BYTE         byP1,
  [in]      BYTE         byP2,
  [in]      LPBYTEBUFFER pData,
  [in, out] LPSCARDCMD   *ppCmd
);
```



## <a name="parameters"></a><span data-ttu-id="a65b2-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="a65b2-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a65b2-110">*byP1* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a65b2-110">*byP1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a65b2-111">Posizione RFU.</span><span class="sxs-lookup"><span data-stu-id="a65b2-111">RFU position.</span></span>

<span data-ttu-id="a65b2-112">Se B8 = 1 in P1, B7 e B6 di P1 sono impostati su zero (RFU bit), B5 a B1 di P1 sono un identificatore EF breve e P2 è l'offset del primo byte da cancellare (in unità dati) dall'inizio del file.</span><span class="sxs-lookup"><span data-stu-id="a65b2-112">If b8=1 in P1, then b7 and b6 of P1 are set to zero (RFU bits), b5 to b1 of P1 are a short EF identifier and P2 is the offset of the first byte to be erased (in data units) from the beginning of the file.</span></span>

<span data-ttu-id="a65b2-113">Se B8 = 0 in P1, P1 \| \| P2 è l'offset del primo byte da cancellare (in unità dati) dall'inizio del file.</span><span class="sxs-lookup"><span data-stu-id="a65b2-113">If b8=0 in P1, then P1 \|\| P2 is the offset of the first byte to be erased (in data units) from the beginning of the file.</span></span>

<span data-ttu-id="a65b2-114">Se il campo dati è presente, codifica l'offset della prima unità dati da cancellare.</span><span class="sxs-lookup"><span data-stu-id="a65b2-114">If the data field is present, it codes the offset of the first data unit not to be erased.</span></span> <span data-ttu-id="a65b2-115">Questo offset deve essere superiore a quello codificato in P1-P2.</span><span class="sxs-lookup"><span data-stu-id="a65b2-115">This offset shall be higher than the one coded in P1-P2.</span></span> <span data-ttu-id="a65b2-116">Quando il campo dati è vuoto, il comando cancella fino alla fine del file.</span><span class="sxs-lookup"><span data-stu-id="a65b2-116">When the data field is empty, the command erases up to the end of the file.</span></span>

</dd> <dt>

<span data-ttu-id="a65b2-117">*byP2* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a65b2-117">*byP2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a65b2-118">Posizione RFU.</span><span class="sxs-lookup"><span data-stu-id="a65b2-118">RFU position.</span></span>

<span data-ttu-id="a65b2-119">Se B8 = 1 in P1, B7 e B6 di P1 sono impostati su zero (RFU bit), B5 a B1 di P1 sono un identificatore EF breve e P2 è l'offset del primo byte da cancellare (in unità dati) dall'inizio del file.</span><span class="sxs-lookup"><span data-stu-id="a65b2-119">If b8=1 in P1, then b7 and b6 of P1 are set to zero (RFU bits), b5 to b1 of P1 are a short EF identifier and P2 is the offset of the first byte to be erased (in data units) from the beginning of the file.</span></span>

<span data-ttu-id="a65b2-120">Se B8 = 0 in P1, P1 \| \| P2 è l'offset del primo byte da cancellare (in unità dati) dall'inizio del file.</span><span class="sxs-lookup"><span data-stu-id="a65b2-120">If b8=0 in P1, then P1 \|\| P2 is the offset of the first byte to be erased (in data units) from the beginning of the file.</span></span>

<span data-ttu-id="a65b2-121">Se il campo dati è presente, codifica l'offset della prima unità dati da cancellare.</span><span class="sxs-lookup"><span data-stu-id="a65b2-121">If the data field is present, it codes the offset of the first data unit not to be erased.</span></span> <span data-ttu-id="a65b2-122">Questo offset deve essere superiore a quello codificato in P1-P2.</span><span class="sxs-lookup"><span data-stu-id="a65b2-122">This offset shall be higher than the one coded in P1-P2.</span></span> <span data-ttu-id="a65b2-123">Quando il campo dati è vuoto, il comando cancella fino alla fine del file.</span><span class="sxs-lookup"><span data-stu-id="a65b2-123">When the data field is empty, the command erases up to the end of the file.</span></span>

</dd> <dt>

<span data-ttu-id="a65b2-124">*pData* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a65b2-124">*pData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a65b2-125">Puntatore ai dati che specifica l'intervallo di cancellazione.</span><span class="sxs-lookup"><span data-stu-id="a65b2-125">A pointer to the data that specifies the erase range.</span></span> <span data-ttu-id="a65b2-126">Questo parametro può essere **null**.</span><span class="sxs-lookup"><span data-stu-id="a65b2-126">This parameter may be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="a65b2-127">*ppCmd* \[ in uscita\]</span><span class="sxs-lookup"><span data-stu-id="a65b2-127">*ppCmd* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="a65b2-128">In input, un puntatore a un oggetto di interfaccia [**ISCardCmd**](iscardcmd.md) o **null**.</span><span class="sxs-lookup"><span data-stu-id="a65b2-128">On input, a pointer to an [**ISCardCmd**](iscardcmd.md) interface object or **NULL**.</span></span>

<span data-ttu-id="a65b2-129">Al ritorno, viene compilato con il comando APDU creato da questa operazione.</span><span class="sxs-lookup"><span data-stu-id="a65b2-129">On return, it is filled with the APDU command constructed by this operation.</span></span> <span data-ttu-id="a65b2-130">Se *ppCmd* è stato impostato su **null**, un oggetto [**ISCardCmd**](iscardcmd.md) della [*Smart Card*](../secgloss/s-gly.md) viene creato e restituito internamente utilizzando il puntatore *ppCmd* .</span><span class="sxs-lookup"><span data-stu-id="a65b2-130">If *ppCmd* was set to **NULL**, a [*smart card*](../secgloss/s-gly.md) [**ISCardCmd**](iscardcmd.md) object is internally created and returned by using the *ppCmd* pointer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a65b2-131">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="a65b2-131">Return value</span></span>

<span data-ttu-id="a65b2-132">Il metodo restituisce uno dei valori possibili seguenti.</span><span class="sxs-lookup"><span data-stu-id="a65b2-132">The method returns one of the following possible values.</span></span>



| <span data-ttu-id="a65b2-133">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="a65b2-133">Return code</span></span>                                                                                   | <span data-ttu-id="a65b2-134">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a65b2-134">Description</span></span>                                          |
|-----------------------------------------------------------------------------------------------|------------------------------------------------------|
| <dl> <span data-ttu-id="a65b2-135"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="a65b2-135"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="a65b2-136">Operazione riuscita.</span><span class="sxs-lookup"><span data-stu-id="a65b2-136">The operation completed successfully.</span></span><br/>     |
| <dl> <span data-ttu-id="a65b2-137"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="a65b2-137"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="a65b2-138">È stato passato un parametro non valido.</span><span class="sxs-lookup"><span data-stu-id="a65b2-138">A parameter that is not valid was passed.</span></span><br/> |
| <dl> <span data-ttu-id="a65b2-139"><dt>**\_puntatore E**</dt></span><span class="sxs-lookup"><span data-stu-id="a65b2-139"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="a65b2-140">È stato passato un puntatore non valido.</span><span class="sxs-lookup"><span data-stu-id="a65b2-140">A bad pointer was passed in.</span></span><br/>              |
| <dl> <span data-ttu-id="a65b2-141"><dt>**E \_ OutOfMemory**</dt></span><span class="sxs-lookup"><span data-stu-id="a65b2-141"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="a65b2-142">Memoria insufficiente.</span><span class="sxs-lookup"><span data-stu-id="a65b2-142">Out of memory.</span></span><br/>                            |



 

## <a name="remarks"></a><span data-ttu-id="a65b2-143">Commenti</span><span class="sxs-lookup"><span data-stu-id="a65b2-143">Remarks</span></span>

<span data-ttu-id="a65b2-144">Il comando incapsulato può essere eseguito solo se lo stato di sicurezza della [*Smart Card*](../secgloss/s-gly.md) soddisfa gli attributi di sicurezza del file elementare elaborato.</span><span class="sxs-lookup"><span data-stu-id="a65b2-144">The encapsulated command can only be performed if the security status of the [*smart card*](../secgloss/s-gly.md) satisfies the security attributes of the elementary file being processed.</span></span>

<span data-ttu-id="a65b2-145">Quando il comando contiene un identificatore elementare breve valido, imposta il file come file elementare corrente.</span><span class="sxs-lookup"><span data-stu-id="a65b2-145">When the command contains a valid short elementary identifier, it sets the file as current elementary file.</span></span>

<span data-ttu-id="a65b2-146">Non è possibile cancellare i file elementari senza una struttura trasparente.</span><span class="sxs-lookup"><span data-stu-id="a65b2-146">Elementary files without a transparent structure cannot be erased.</span></span> <span data-ttu-id="a65b2-147">Il comando incapsulato viene interrotto se applicato a un file elementare senza una struttura trasparente.</span><span class="sxs-lookup"><span data-stu-id="a65b2-147">The encapsulated command aborts if applied to an elementary file without a transparent structure.</span></span>

<span data-ttu-id="a65b2-148">Per un elenco di tutti i metodi forniti da questa interfaccia, vedere [**ISCardISO7816**](iscardiso7816.md).</span><span class="sxs-lookup"><span data-stu-id="a65b2-148">For a list of all the methods provided by this interface, see [**ISCardISO7816**](iscardiso7816.md).</span></span>

<span data-ttu-id="a65b2-149">Oltre ai codici di errore COM elencati sopra, questa interfaccia può restituire un codice di errore della smart card se è stata chiamata una funzione Smart Card per completare la richiesta.</span><span class="sxs-lookup"><span data-stu-id="a65b2-149">In addition to the COM error codes listed above, this interface may return a smart card error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="a65b2-150">Per ulteriori informazioni, vedere [valori restituiti della smart card](authentication-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="a65b2-150">For more information, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="a65b2-151">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a65b2-151">Requirements</span></span>



| <span data-ttu-id="a65b2-152">Requisito</span><span class="sxs-lookup"><span data-stu-id="a65b2-152">Requirement</span></span> | <span data-ttu-id="a65b2-153">Valore</span><span class="sxs-lookup"><span data-stu-id="a65b2-153">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a65b2-154">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a65b2-154">Minimum supported client</span></span><br/> | <span data-ttu-id="a65b2-155">\[Solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="a65b2-155">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="a65b2-156">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a65b2-156">Minimum supported server</span></span><br/> | <span data-ttu-id="a65b2-157">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="a65b2-157">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="a65b2-158">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="a65b2-158">End of client support</span></span><br/>    | <span data-ttu-id="a65b2-159">Windows XP</span><span class="sxs-lookup"><span data-stu-id="a65b2-159">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="a65b2-160">Fine del supporto server</span><span class="sxs-lookup"><span data-stu-id="a65b2-160">End of server support</span></span><br/>    | <span data-ttu-id="a65b2-161">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="a65b2-161">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="a65b2-162">Intestazione</span><span class="sxs-lookup"><span data-stu-id="a65b2-162">Header</span></span><br/>                   | <dl> <span data-ttu-id="a65b2-163"><dt>Scardssp. h</dt></span><span class="sxs-lookup"><span data-stu-id="a65b2-163"><dt>Scardssp.h</dt></span></span> </dl>   |
| <span data-ttu-id="a65b2-164">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="a65b2-164">Type library</span></span><br/>             | <dl> <span data-ttu-id="a65b2-165"><dt>Scardsrv. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="a65b2-165"><dt>Scardsrv.tlb</dt></span></span> </dl> |
| <span data-ttu-id="a65b2-166">DLL</span><span class="sxs-lookup"><span data-stu-id="a65b2-166">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a65b2-167"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a65b2-167"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="a65b2-168">IID</span><span class="sxs-lookup"><span data-stu-id="a65b2-168">IID</span></span><br/>                      | <span data-ttu-id="a65b2-169">IID \_ ISCardISO7816 è definito come 53B6AA68-3F56-11D0-916B-00AA00C18068</span><span class="sxs-lookup"><span data-stu-id="a65b2-169">IID\_ISCardISO7816 is defined as 53B6AA68-3F56-11D0-916B-00AA00C18068</span></span><br/>        |



## <a name="see-also"></a><span data-ttu-id="a65b2-170">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a65b2-170">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a65b2-171">**ISCardISO7816**</span><span class="sxs-lookup"><span data-stu-id="a65b2-171">**ISCardISO7816**</span></span>](iscardiso7816.md)
</dt> <dt>

[<span data-ttu-id="a65b2-172">**ReadBinary**</span><span class="sxs-lookup"><span data-stu-id="a65b2-172">**ReadBinary**</span></span>](iscardiso7816-readbinary.md)
</dt> <dt>

[<span data-ttu-id="a65b2-173">**UpdateBinary**</span><span class="sxs-lookup"><span data-stu-id="a65b2-173">**UpdateBinary**</span></span>](iscardiso7816-updatebinary.md)
</dt> <dt>

[<span data-ttu-id="a65b2-174">**WriteBinary**</span><span class="sxs-lookup"><span data-stu-id="a65b2-174">**WriteBinary**</span></span>](iscardiso7816-writebinary.md)
</dt> </dl>

 

 
