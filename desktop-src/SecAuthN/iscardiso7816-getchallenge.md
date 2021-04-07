---
description: Il metodo getchallenge costruisce un comando APDU (Application Protocol Data Unit) che invia una richiesta di verifica, ad esempio un numero casuale, da utilizzare in una procedura correlata alla sicurezza.
ms.assetid: 61f6db1c-b83a-4c1f-8ace-0222a12560ff
title: 'Metodo ISCardISO7816:: getchallenge (scardssp. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardISO7816.GetChallenge
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 05fe18ad73de6c7c3ea30f986c7bb3420bc465b9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104057970"
---
# <a name="iscardiso7816getchallenge-method"></a><span data-ttu-id="08c07-103">Metodo ISCardISO7816:: getchallenge</span><span class="sxs-lookup"><span data-stu-id="08c07-103">ISCardISO7816::GetChallenge method</span></span>

<span data-ttu-id="08c07-104">\[Il metodo **getchallenge** è disponibile per l'uso nei sistemi operativi specificati nella sezione requisiti.</span><span class="sxs-lookup"><span data-stu-id="08c07-104">\[The **GetChallenge** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="08c07-105">Non è disponibile per l'utilizzo in Windows Server 2003 con Service Pack 1 (SP1) e versioni successive, Windows Vista, Windows Server 2008 e versioni successive del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="08c07-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="08c07-106">I [moduli Smart Card](/previous-versions/windows/desktop/secsmart/smart-card-modules) offrono funzionalità simili.\]</span><span class="sxs-lookup"><span data-stu-id="08c07-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="08c07-107">Il metodo **getchallenge** costruisce un comando APDU ( [*Application Protocol Data Unit*](../secgloss/a-gly.md) ) che invia una richiesta di verifica, ad esempio un numero casuale, da utilizzare in una procedura correlata alla sicurezza.</span><span class="sxs-lookup"><span data-stu-id="08c07-107">The **GetChallenge** method constructs an [*application protocol data unit*](../secgloss/a-gly.md) (APDU) command that issue a challenge (for example, a random number) for use in a security-related procedure.</span></span>

## <a name="syntax"></a><span data-ttu-id="08c07-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="08c07-108">Syntax</span></span>


```C++
HRESULT GetChallenge(
  [in]      LONG       lBytesExpected,
  [in, out] LPSCARDCMD *ppCmd
);
```



## <a name="parameters"></a><span data-ttu-id="08c07-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="08c07-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="08c07-110">*lBytesExpected* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="08c07-110">*lBytesExpected* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="08c07-111">Lunghezza massima della risposta prevista.</span><span class="sxs-lookup"><span data-stu-id="08c07-111">Maximum length of the expected response.</span></span>

</dd> <dt>

<span data-ttu-id="08c07-112">*ppCmd* \[ in uscita\]</span><span class="sxs-lookup"><span data-stu-id="08c07-112">*ppCmd* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="08c07-113">In input, un puntatore a un oggetto di interfaccia [**ISCardCmd**](iscardcmd.md) o **null**.</span><span class="sxs-lookup"><span data-stu-id="08c07-113">On input, a pointer to an [**ISCardCmd**](iscardcmd.md) interface object or **NULL**.</span></span>

<span data-ttu-id="08c07-114">Al ritorno, viene compilato con il comando APDU creato da questa operazione.</span><span class="sxs-lookup"><span data-stu-id="08c07-114">On return, it is filled with the APDU command constructed by this operation.</span></span> <span data-ttu-id="08c07-115">Se *ppCmd* è stato impostato su **null**, un oggetto [**ISCardCmd**](iscardcmd.md) della [*Smart Card*](../secgloss/s-gly.md) viene creato e restituito internamente tramite il puntatore *ppCmd* .</span><span class="sxs-lookup"><span data-stu-id="08c07-115">If *ppCmd* was set to **NULL**, a [*smart card*](../secgloss/s-gly.md) [**ISCardCmd**](iscardcmd.md) object is internally created and returned via the *ppCmd* pointer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="08c07-116">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="08c07-116">Return value</span></span>

<span data-ttu-id="08c07-117">Il metodo restituisce uno dei valori possibili seguenti.</span><span class="sxs-lookup"><span data-stu-id="08c07-117">The method returns one of the following possible values.</span></span>



| <span data-ttu-id="08c07-118">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="08c07-118">Return code</span></span>                                                                                   | <span data-ttu-id="08c07-119">Descrizione</span><span class="sxs-lookup"><span data-stu-id="08c07-119">Description</span></span>                                  |
|-----------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="08c07-120"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="08c07-120"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="08c07-121">Operazione completata correttamente.</span><span class="sxs-lookup"><span data-stu-id="08c07-121">Operation completed successfully.</span></span><br/> |
| <dl> <span data-ttu-id="08c07-122"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="08c07-122"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="08c07-123">Parametro non valido.</span><span class="sxs-lookup"><span data-stu-id="08c07-123">Invalid parameter.</span></span><br/>                |
| <dl> <span data-ttu-id="08c07-124"><dt>**\_puntatore E**</dt></span><span class="sxs-lookup"><span data-stu-id="08c07-124"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="08c07-125">È stato passato un puntatore non valido.</span><span class="sxs-lookup"><span data-stu-id="08c07-125">A bad pointer was passed in.</span></span><br/>      |
| <dl> <span data-ttu-id="08c07-126"><dt>**E \_ OutOfMemory**</dt></span><span class="sxs-lookup"><span data-stu-id="08c07-126"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="08c07-127">Memoria insufficiente.</span><span class="sxs-lookup"><span data-stu-id="08c07-127">Out of memory.</span></span><br/>                    |



 

## <a name="remarks"></a><span data-ttu-id="08c07-128">Commenti</span><span class="sxs-lookup"><span data-stu-id="08c07-128">Remarks</span></span>

<span data-ttu-id="08c07-129">La richiesta di verifica è valida almeno per il comando successivo.</span><span class="sxs-lookup"><span data-stu-id="08c07-129">The challenge is valid at least for the next command.</span></span>

<span data-ttu-id="08c07-130">Per un elenco di tutti i metodi forniti da questa interfaccia, vedere [**ISCardISO7816**](iscardiso7816.md).</span><span class="sxs-lookup"><span data-stu-id="08c07-130">For a list of all the methods provided by this interface, see [**ISCardISO7816**](iscardiso7816.md).</span></span>

<span data-ttu-id="08c07-131">Oltre ai codici di errore COM elencati sopra, questa interfaccia può restituire un codice di errore della smart card se è stata chiamata una funzione Smart Card per completare la richiesta.</span><span class="sxs-lookup"><span data-stu-id="08c07-131">In addition to the COM error codes listed above, this interface may return a smart card error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="08c07-132">Per ulteriori informazioni, vedere [valori restituiti della smart card](authentication-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="08c07-132">For more information, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="08c07-133">Requisiti</span><span class="sxs-lookup"><span data-stu-id="08c07-133">Requirements</span></span>



| <span data-ttu-id="08c07-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="08c07-134">Requirement</span></span> | <span data-ttu-id="08c07-135">Valore</span><span class="sxs-lookup"><span data-stu-id="08c07-135">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="08c07-136">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="08c07-136">Minimum supported client</span></span><br/> | <span data-ttu-id="08c07-137">\[Solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="08c07-137">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="08c07-138">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="08c07-138">Minimum supported server</span></span><br/> | <span data-ttu-id="08c07-139">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="08c07-139">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="08c07-140">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="08c07-140">End of client support</span></span><br/>    | <span data-ttu-id="08c07-141">Windows XP</span><span class="sxs-lookup"><span data-stu-id="08c07-141">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="08c07-142">Fine del supporto server</span><span class="sxs-lookup"><span data-stu-id="08c07-142">End of server support</span></span><br/>    | <span data-ttu-id="08c07-143">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="08c07-143">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="08c07-144">Intestazione</span><span class="sxs-lookup"><span data-stu-id="08c07-144">Header</span></span><br/>                   | <dl> <span data-ttu-id="08c07-145"><dt>Scardssp. h</dt></span><span class="sxs-lookup"><span data-stu-id="08c07-145"><dt>Scardssp.h</dt></span></span> </dl>   |
| <span data-ttu-id="08c07-146">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="08c07-146">Type library</span></span><br/>             | <dl> <span data-ttu-id="08c07-147"><dt>Scardsrv. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="08c07-147"><dt>Scardsrv.tlb</dt></span></span> </dl> |
| <span data-ttu-id="08c07-148">DLL</span><span class="sxs-lookup"><span data-stu-id="08c07-148">DLL</span></span><br/>                      | <dl> <span data-ttu-id="08c07-149"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="08c07-149"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="08c07-150">IID</span><span class="sxs-lookup"><span data-stu-id="08c07-150">IID</span></span><br/>                      | <span data-ttu-id="08c07-151">IID \_ ISCardISO7816 è definito come 53B6AA68-3F56-11D0-916B-00AA00C18068</span><span class="sxs-lookup"><span data-stu-id="08c07-151">IID\_ISCardISO7816 is defined as 53B6AA68-3F56-11D0-916B-00AA00C18068</span></span><br/>        |



## <a name="see-also"></a><span data-ttu-id="08c07-152">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="08c07-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="08c07-153">**ExternalAuthenticate**</span><span class="sxs-lookup"><span data-stu-id="08c07-153">**ExternalAuthenticate**</span></span>](iscardiso7816-externalauthenticate.md)
</dt> <dt>

[<span data-ttu-id="08c07-154">**InternalAuthenticate**</span><span class="sxs-lookup"><span data-stu-id="08c07-154">**InternalAuthenticate**</span></span>](iscardiso7816-internalauthenticate.md)
</dt> <dt>

[<span data-ttu-id="08c07-155">**ISCardISO7816**</span><span class="sxs-lookup"><span data-stu-id="08c07-155">**ISCardISO7816**</span></span>](iscardiso7816.md)
</dt> </dl>

 

 
