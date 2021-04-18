---
description: Il metodo UpdateBinary costruisce un comando APDU (Application Protocol Data Unit) che aggiorna i bit presenti in un file elementare con i bit specificati nel comando APDU.
ms.assetid: 14ac6ad9-efcf-48ea-8712-19caeee47521
title: 'Metodo ISCardISO7816:: UpdateBinary (scardssp. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardISO7816.UpdateBinary
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: d9651189cab228eaa5dacc9c2f5963201bbc65c8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106313737"
---
# <a name="iscardiso7816updatebinary-method"></a><span data-ttu-id="8580e-103">Metodo ISCardISO7816:: UpdateBinary</span><span class="sxs-lookup"><span data-stu-id="8580e-103">ISCardISO7816::UpdateBinary method</span></span>

<span data-ttu-id="8580e-104">\[Il metodo **UpdateBinary** è disponibile per l'uso nei sistemi operativi specificati nella sezione requisiti.</span><span class="sxs-lookup"><span data-stu-id="8580e-104">\[The **UpdateBinary** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="8580e-105">Non è disponibile per l'utilizzo in Windows Server 2003 con Service Pack 1 (SP1) e versioni successive, Windows Vista, Windows Server 2008 e versioni successive del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="8580e-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="8580e-106">I [moduli Smart Card](/previous-versions/windows/desktop/secsmart/smart-card-modules) offrono funzionalità simili.\]</span><span class="sxs-lookup"><span data-stu-id="8580e-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="8580e-107">Il metodo **UpdateBinary** costruisce un comando APDU ( [*Application Protocol Data Unit*](../secgloss/a-gly.md) ) che aggiorna i bit presenti in un file elementare con i bit specificati nel comando APDU.</span><span class="sxs-lookup"><span data-stu-id="8580e-107">The **UpdateBinary** method constructs an [*application protocol data unit*](../secgloss/a-gly.md) (APDU) command that updates the bits present in an elementary file with the bits given in the APDU command.</span></span>

## <a name="syntax"></a><span data-ttu-id="8580e-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="8580e-108">Syntax</span></span>


```C++
HRESULT UpdateBinary(
  [in]      BYTE         byP1,
  [in]      BYTE         byP2,
  [in]      LPBYTEBUFFER pData,
  [in, out] LPSCARDCMD   *ppCmd
);
```



## <a name="parameters"></a><span data-ttu-id="8580e-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="8580e-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8580e-110">*byP1* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="8580e-110">*byP1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8580e-111">Offset al percorso di scrittura (aggiornamento) nel file binario dall'inizio del file binario.</span><span class="sxs-lookup"><span data-stu-id="8580e-111">Offset to the write (update) location into the binary from the start of the binary.</span></span> <span data-ttu-id="8580e-112">Se B8 = 1 in P1, B7 e B6 di P1 sono impostati su zero (RFU bit), B5 a B1 di P1 sono un identificatore EF breve e P2 è l'offset del primo byte da aggiornare in unità dati dall'inizio del file.</span><span class="sxs-lookup"><span data-stu-id="8580e-112">If b8=1 in P1, then b7 and b6 of P1 are set to zero (RFU bits), b5 to b1 of P1 are a short EF identifier and P2 is the offset of the first byte to be updated in data units from the beginning of the file.</span></span> <span data-ttu-id="8580e-113">Se B8 = 0 in P1, P1 \| \| P2 è l'offset del primo byte da aggiornare in unità dati dall'inizio del file.</span><span class="sxs-lookup"><span data-stu-id="8580e-113">If b8=0 in P1, then P1 \|\| P2 is the offset of the first byte to be updated in data units from the beginning of the file.</span></span>

</dd> <dt>

<span data-ttu-id="8580e-114">*byP2* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="8580e-114">*byP2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8580e-115">Offset al percorso di scrittura (aggiornamento) nel file binario dall'inizio del file binario.</span><span class="sxs-lookup"><span data-stu-id="8580e-115">Offset to the write (update) location into the binary from the start of the binary.</span></span> <span data-ttu-id="8580e-116">Se B8 = 1 in P1, B7 e B6 di P1 sono impostati su zero (RFU bit), B5 a B1 di P1 sono un identificatore EF breve e P2 è l'offset del primo byte da aggiornare in unità dati dall'inizio del file.</span><span class="sxs-lookup"><span data-stu-id="8580e-116">If b8=1 in P1, then b7 and b6 of P1 are set to zero (RFU bits), b5 to b1 of P1 are a short EF identifier and P2 is the offset of the first byte to be updated in data units from the beginning of the file.</span></span> <span data-ttu-id="8580e-117">Se B8 = 0 in P1, P1 \| \| P2 è l'offset del primo byte da aggiornare in unità dati dall'inizio del file.</span><span class="sxs-lookup"><span data-stu-id="8580e-117">If b8=0 in P1, then P1 \|\| P2 is the offset of the first byte to be updated in data units from the beginning of the file.</span></span>

</dd> <dt>

<span data-ttu-id="8580e-118">*pData* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="8580e-118">*pData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8580e-119">Puntatore alla stringa di unità dati da aggiornare.</span><span class="sxs-lookup"><span data-stu-id="8580e-119">Pointer to the string of data units to be updated.</span></span>

</dd> <dt>

<span data-ttu-id="8580e-120">*ppCmd* \[ in uscita\]</span><span class="sxs-lookup"><span data-stu-id="8580e-120">*ppCmd* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="8580e-121">In input, un puntatore a un oggetto di interfaccia [**ISCardCmd**](iscardcmd.md) o **null**.</span><span class="sxs-lookup"><span data-stu-id="8580e-121">On input, a pointer to an [**ISCardCmd**](iscardcmd.md) interface object or **NULL**.</span></span>

<span data-ttu-id="8580e-122">Al ritorno, viene compilato con il comando APDU creato da questa operazione.</span><span class="sxs-lookup"><span data-stu-id="8580e-122">On return, it is filled with the APDU command constructed by this operation.</span></span> <span data-ttu-id="8580e-123">Se *ppCmd* è stato impostato su **null**, un oggetto [**ISCardCmd**](iscardcmd.md) della [*Smart Card*](../secgloss/s-gly.md) viene creato e restituito internamente utilizzando il puntatore *ppCmd* .</span><span class="sxs-lookup"><span data-stu-id="8580e-123">If *ppCmd* was set to **NULL**, a [*smart card*](../secgloss/s-gly.md) [**ISCardCmd**](iscardcmd.md) object is internally created and returned using the *ppCmd* pointer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8580e-124">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="8580e-124">Return value</span></span>

<span data-ttu-id="8580e-125">Il metodo restituisce uno dei valori possibili seguenti.</span><span class="sxs-lookup"><span data-stu-id="8580e-125">The method returns one of the following possible values.</span></span>



| <span data-ttu-id="8580e-126">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="8580e-126">Return code</span></span>                                                                                   | <span data-ttu-id="8580e-127">Descrizione</span><span class="sxs-lookup"><span data-stu-id="8580e-127">Description</span></span>                                  |
|-----------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="8580e-128"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="8580e-128"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="8580e-129">Operazione completata correttamente.</span><span class="sxs-lookup"><span data-stu-id="8580e-129">Operation completed successfully.</span></span><br/> |
| <dl> <span data-ttu-id="8580e-130"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="8580e-130"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="8580e-131">Parametro non valido.</span><span class="sxs-lookup"><span data-stu-id="8580e-131">Invalid parameter.</span></span><br/>                |
| <dl> <span data-ttu-id="8580e-132"><dt>**\_puntatore E**</dt></span><span class="sxs-lookup"><span data-stu-id="8580e-132"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="8580e-133">È stato passato un puntatore non valido.</span><span class="sxs-lookup"><span data-stu-id="8580e-133">A bad pointer was passed in.</span></span><br/>      |
| <dl> <span data-ttu-id="8580e-134"><dt>**E \_ OutOfMemory**</dt></span><span class="sxs-lookup"><span data-stu-id="8580e-134"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="8580e-135">Memoria insufficiente.</span><span class="sxs-lookup"><span data-stu-id="8580e-135">Out of memory.</span></span><br/>                    |



 

## <a name="remarks"></a><span data-ttu-id="8580e-136">Commenti</span><span class="sxs-lookup"><span data-stu-id="8580e-136">Remarks</span></span>

<span data-ttu-id="8580e-137">Il comando incapsulato può essere eseguito solo se lo stato di sicurezza della smart card soddisfa gli attributi di sicurezza del file elementare elaborato.</span><span class="sxs-lookup"><span data-stu-id="8580e-137">The encapsulated command can only be performed if the security status of the smart card satisfies the security attributes of the elementary file being processed.</span></span>

<span data-ttu-id="8580e-138">Quando il comando contiene un identificatore elementare breve valido, imposta il file come file elementare corrente.</span><span class="sxs-lookup"><span data-stu-id="8580e-138">When the command contains a valid short elementary identifier, it sets the file as current elementary file.</span></span>

<span data-ttu-id="8580e-139">Non è possibile cancellare i file elementari senza una struttura trasparente.</span><span class="sxs-lookup"><span data-stu-id="8580e-139">Elementary files without a transparent structure cannot be erased.</span></span> <span data-ttu-id="8580e-140">Il comando incapsulato viene interrotto se applicato a un file elementare senza una struttura trasparente.</span><span class="sxs-lookup"><span data-stu-id="8580e-140">The encapsulated command aborts if applied to an elementary file without a transparent structure.</span></span>

<span data-ttu-id="8580e-141">Per un elenco di tutti i metodi forniti da questa interfaccia, vedere [**ISCardISO7816**](iscardiso7816.md).</span><span class="sxs-lookup"><span data-stu-id="8580e-141">For a list of all the methods provided by this interface, see [**ISCardISO7816**](iscardiso7816.md).</span></span>

<span data-ttu-id="8580e-142">Oltre ai codici di errore COM elencati sopra, questa interfaccia può restituire un codice di errore della smart card se è stata chiamata una funzione Smart Card per completare la richiesta.</span><span class="sxs-lookup"><span data-stu-id="8580e-142">In addition to the COM error codes listed above, this interface may return a smart card error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="8580e-143">Per ulteriori informazioni, vedere [valori restituiti della smart card](authentication-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="8580e-143">For more information, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="8580e-144">Requisiti</span><span class="sxs-lookup"><span data-stu-id="8580e-144">Requirements</span></span>



| <span data-ttu-id="8580e-145">Requisito</span><span class="sxs-lookup"><span data-stu-id="8580e-145">Requirement</span></span> | <span data-ttu-id="8580e-146">Valore</span><span class="sxs-lookup"><span data-stu-id="8580e-146">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="8580e-147">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="8580e-147">Minimum supported client</span></span><br/> | <span data-ttu-id="8580e-148">\[Solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="8580e-148">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="8580e-149">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="8580e-149">Minimum supported server</span></span><br/> | <span data-ttu-id="8580e-150">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="8580e-150">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="8580e-151">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="8580e-151">End of client support</span></span><br/>    | <span data-ttu-id="8580e-152">Windows XP</span><span class="sxs-lookup"><span data-stu-id="8580e-152">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="8580e-153">Fine del supporto server</span><span class="sxs-lookup"><span data-stu-id="8580e-153">End of server support</span></span><br/>    | <span data-ttu-id="8580e-154">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="8580e-154">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="8580e-155">Intestazione</span><span class="sxs-lookup"><span data-stu-id="8580e-155">Header</span></span><br/>                   | <dl> <span data-ttu-id="8580e-156"><dt>Scardssp. h</dt></span><span class="sxs-lookup"><span data-stu-id="8580e-156"><dt>Scardssp.h</dt></span></span> </dl>   |
| <span data-ttu-id="8580e-157">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="8580e-157">Type library</span></span><br/>             | <dl> <span data-ttu-id="8580e-158"><dt>Scardsrv. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="8580e-158"><dt>Scardsrv.tlb</dt></span></span> </dl> |
| <span data-ttu-id="8580e-159">DLL</span><span class="sxs-lookup"><span data-stu-id="8580e-159">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8580e-160"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8580e-160"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="8580e-161">IID</span><span class="sxs-lookup"><span data-stu-id="8580e-161">IID</span></span><br/>                      | <span data-ttu-id="8580e-162">IID \_ ISCardISO7816 è definito come 53B6AA68-3F56-11D0-916B-00AA00C18068</span><span class="sxs-lookup"><span data-stu-id="8580e-162">IID\_ISCardISO7816 is defined as 53B6AA68-3F56-11D0-916B-00AA00C18068</span></span><br/>        |



## <a name="see-also"></a><span data-ttu-id="8580e-163">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="8580e-163">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8580e-164">**EraseBinary**</span><span class="sxs-lookup"><span data-stu-id="8580e-164">**EraseBinary**</span></span>](iscardiso7816-erasebinary.md)
</dt> <dt>

[<span data-ttu-id="8580e-165">**ISCardISO7816**</span><span class="sxs-lookup"><span data-stu-id="8580e-165">**ISCardISO7816**</span></span>](iscardiso7816.md)
</dt> <dt>

[<span data-ttu-id="8580e-166">**ReadBinary**</span><span class="sxs-lookup"><span data-stu-id="8580e-166">**ReadBinary**</span></span>](iscardiso7816-readbinary.md)
</dt> <dt>

[<span data-ttu-id="8580e-167">**WriteBinary**</span><span class="sxs-lookup"><span data-stu-id="8580e-167">**WriteBinary**</span></span>](iscardiso7816-writebinary.md)
</dt> </dl>

 

 
