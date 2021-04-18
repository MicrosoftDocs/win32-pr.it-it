---
description: Il metodo GetResponse costruisce un comando APDU (Application Protocol Data Unit) che trasmette i comandi APDU (o parte di un comando APDU) che altrimenti non potevano essere trasmessi dai protocolli disponibili.
ms.assetid: 1aa83d38-d46d-4d3b-8f57-0256e5875e35
title: 'Metodo ISCardISO7816:: GetResponse (scardssp. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardISO7816.GetResponse
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 0b74fe9620aefc390957b88f9cf286f7871c1d18
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106315436"
---
# <a name="iscardiso7816getresponse-method"></a><span data-ttu-id="e4e4c-103">Metodo ISCardISO7816:: GetResponse</span><span class="sxs-lookup"><span data-stu-id="e4e4c-103">ISCardISO7816::GetResponse method</span></span>

<span data-ttu-id="e4e4c-104">\[Il metodo **GetResponse** è disponibile per l'uso nei sistemi operativi specificati nella sezione requisiti.</span><span class="sxs-lookup"><span data-stu-id="e4e4c-104">\[The **GetResponse** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="e4e4c-105">Non è disponibile per l'utilizzo in Windows Server 2003 con Service Pack 1 (SP1) e versioni successive, Windows Vista, Windows Server 2008 e versioni successive del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="e4e4c-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="e4e4c-106">I [moduli Smart Card](/previous-versions/windows/desktop/secsmart/smart-card-modules) offrono funzionalità simili.\]</span><span class="sxs-lookup"><span data-stu-id="e4e4c-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="e4e4c-107">Il metodo **GetResponse** costruisce un comando APDU ( [*Application Protocol Data Unit*](../secgloss/a-gly.md) ) che trasmette i comandi APDU (o parte di un comando APDU) che altrimenti non potevano essere trasmessi dai protocolli disponibili.</span><span class="sxs-lookup"><span data-stu-id="e4e4c-107">The **GetResponse** method constructs an [*application protocol data unit*](../secgloss/a-gly.md) (APDU) command that transmits APDU commands (or part of an APDU command) which otherwise could not be transmitted by the available protocols.</span></span>

## <a name="syntax"></a><span data-ttu-id="e4e4c-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="e4e4c-108">Syntax</span></span>


```C++
HRESULT GetResponse(
  [in]      BYTE       byP1,
  [in]      BYTE       byP2,
  [in]      LONG       lDataLength,
  [in, out] LPSCARDCMD *ppCmd
);
```



## <a name="parameters"></a><span data-ttu-id="e4e4c-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="e4e4c-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e4e4c-110">*byP1* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e4e4c-110">*byP1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e4e4c-111">Per la ISO 7816-4, P1 deve essere zero (RFU).</span><span class="sxs-lookup"><span data-stu-id="e4e4c-111">Per the ISO 7816-4, P1 should be zero (RFU).</span></span>

</dd> <dt>

<span data-ttu-id="e4e4c-112">*byP2* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e4e4c-112">*byP2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e4e4c-113">Per ISO 7816-4, P2 deve essere zero (RFU).</span><span class="sxs-lookup"><span data-stu-id="e4e4c-113">Per the ISO 7816-4, P2 should be zero (RFU).</span></span>

</dd> <dt>

<span data-ttu-id="e4e4c-114">*lDataLength* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e4e4c-114">*lDataLength* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e4e4c-115">Lunghezza dei dati trasmessi.</span><span class="sxs-lookup"><span data-stu-id="e4e4c-115">Length of data transmitted.</span></span>

</dd> <dt>

<span data-ttu-id="e4e4c-116">*ppCmd* \[ in uscita\]</span><span class="sxs-lookup"><span data-stu-id="e4e4c-116">*ppCmd* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="e4e4c-117">In input, un puntatore a un oggetto di interfaccia [**ISCardCmd**](iscardcmd.md) o **null**.</span><span class="sxs-lookup"><span data-stu-id="e4e4c-117">On input, a pointer to an [**ISCardCmd**](iscardcmd.md) interface object or **NULL**.</span></span>

<span data-ttu-id="e4e4c-118">Al ritorno, viene compilato con il comando APDU creato da questa operazione.</span><span class="sxs-lookup"><span data-stu-id="e4e4c-118">On return, it is filled with the APDU command constructed by this operation.</span></span> <span data-ttu-id="e4e4c-119">Se *ppCmd* è stato impostato su **null**, un oggetto [**ISCardCmd**](iscardcmd.md) della [*Smart Card*](../secgloss/s-gly.md) viene creato e restituito internamente tramite il puntatore *ppCmd* .</span><span class="sxs-lookup"><span data-stu-id="e4e4c-119">If *ppCmd* was set to **NULL**, a [*smart card*](../secgloss/s-gly.md) [**ISCardCmd**](iscardcmd.md) object is internally created and returned via the *ppCmd* pointer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e4e4c-120">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="e4e4c-120">Return value</span></span>

<span data-ttu-id="e4e4c-121">Il metodo restituisce uno dei valori possibili seguenti.</span><span class="sxs-lookup"><span data-stu-id="e4e4c-121">The method returns one of the following possible values.</span></span>



| <span data-ttu-id="e4e4c-122">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="e4e4c-122">Return code</span></span>                                                                                   | <span data-ttu-id="e4e4c-123">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e4e4c-123">Description</span></span>                                  |
|-----------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="e4e4c-124"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="e4e4c-124"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="e4e4c-125">Operazione completata correttamente.</span><span class="sxs-lookup"><span data-stu-id="e4e4c-125">Operation completed successfully.</span></span><br/> |
| <dl> <span data-ttu-id="e4e4c-126"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="e4e4c-126"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="e4e4c-127">Parametro non valido.</span><span class="sxs-lookup"><span data-stu-id="e4e4c-127">Invalid parameter.</span></span><br/>                |
| <dl> <span data-ttu-id="e4e4c-128"><dt>**\_puntatore E**</dt></span><span class="sxs-lookup"><span data-stu-id="e4e4c-128"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="e4e4c-129">È stato passato un puntatore non valido.</span><span class="sxs-lookup"><span data-stu-id="e4e4c-129">A bad pointer was passed in.</span></span><br/>      |
| <dl> <span data-ttu-id="e4e4c-130"><dt>**E \_ OutOfMemory**</dt></span><span class="sxs-lookup"><span data-stu-id="e4e4c-130"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="e4e4c-131">Memoria insufficiente.</span><span class="sxs-lookup"><span data-stu-id="e4e4c-131">Out of memory.</span></span><br/>                    |



 

## <a name="remarks"></a><span data-ttu-id="e4e4c-132">Commenti</span><span class="sxs-lookup"><span data-stu-id="e4e4c-132">Remarks</span></span>

<span data-ttu-id="e4e4c-133">Per un elenco di tutti i metodi forniti da questa interfaccia, vedere [**ISCardISO7816**](iscardiso7816.md).</span><span class="sxs-lookup"><span data-stu-id="e4e4c-133">For a list of all the methods provided by this interface, see [**ISCardISO7816**](iscardiso7816.md).</span></span>

<span data-ttu-id="e4e4c-134">Oltre ai codici di errore COM elencati sopra, questa interfaccia può restituire un codice di errore della smart card se è stata chiamata una funzione Smart Card per completare la richiesta.</span><span class="sxs-lookup"><span data-stu-id="e4e4c-134">In addition to the COM error codes listed above, this interface may return a smart card error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="e4e4c-135">Per ulteriori informazioni, vedere [valori restituiti della smart card](authentication-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="e4e4c-135">For more information, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="e4e4c-136">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e4e4c-136">Requirements</span></span>



| <span data-ttu-id="e4e4c-137">Requisito</span><span class="sxs-lookup"><span data-stu-id="e4e4c-137">Requirement</span></span> | <span data-ttu-id="e4e4c-138">Valore</span><span class="sxs-lookup"><span data-stu-id="e4e4c-138">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e4e4c-139">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e4e4c-139">Minimum supported client</span></span><br/> | <span data-ttu-id="e4e4c-140">\[Solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="e4e4c-140">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="e4e4c-141">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e4e4c-141">Minimum supported server</span></span><br/> | <span data-ttu-id="e4e4c-142">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="e4e4c-142">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="e4e4c-143">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="e4e4c-143">End of client support</span></span><br/>    | <span data-ttu-id="e4e4c-144">Windows XP</span><span class="sxs-lookup"><span data-stu-id="e4e4c-144">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="e4e4c-145">Fine del supporto server</span><span class="sxs-lookup"><span data-stu-id="e4e4c-145">End of server support</span></span><br/>    | <span data-ttu-id="e4e4c-146">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="e4e4c-146">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="e4e4c-147">Intestazione</span><span class="sxs-lookup"><span data-stu-id="e4e4c-147">Header</span></span><br/>                   | <dl> <span data-ttu-id="e4e4c-148"><dt>Scardssp. h</dt></span><span class="sxs-lookup"><span data-stu-id="e4e4c-148"><dt>Scardssp.h</dt></span></span> </dl>   |
| <span data-ttu-id="e4e4c-149">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="e4e4c-149">Type library</span></span><br/>             | <dl> <span data-ttu-id="e4e4c-150"><dt>Scardsrv. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="e4e4c-150"><dt>Scardsrv.tlb</dt></span></span> </dl> |
| <span data-ttu-id="e4e4c-151">DLL</span><span class="sxs-lookup"><span data-stu-id="e4e4c-151">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e4e4c-152"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e4e4c-152"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="e4e4c-153">IID</span><span class="sxs-lookup"><span data-stu-id="e4e4c-153">IID</span></span><br/>                      | <span data-ttu-id="e4e4c-154">IID \_ ISCardISO7816 è definito come 53B6AA68-3F56-11D0-916B-00AA00C18068</span><span class="sxs-lookup"><span data-stu-id="e4e4c-154">IID\_ISCardISO7816 is defined as 53B6AA68-3F56-11D0-916B-00AA00C18068</span></span><br/>        |



## <a name="see-also"></a><span data-ttu-id="e4e4c-155">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e4e4c-155">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e4e4c-156">**ISCardISO7816**</span><span class="sxs-lookup"><span data-stu-id="e4e4c-156">**ISCardISO7816**</span></span>](iscardiso7816.md)
</dt> </dl>

 

 
