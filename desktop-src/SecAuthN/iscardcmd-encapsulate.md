---
description: Il metodo incapsula incapsula l'unità dati del protocollo dell'applicazione del comando specificata (APDU) in un altro comando APDU per la trasmissione a una smart card.
ms.assetid: dfffad09-046b-46cb-b6fd-286a4bbf1066
title: 'Metodo ISCardCmd:: Encapsulate (Scarddat. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardCmd.Encapsulate
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: cd671a11edd9977695eeaf858e38f962b3dd0962
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106315880"
---
# <a name="iscardcmdencapsulate-method"></a><span data-ttu-id="bfd48-103">Metodo ISCardCmd:: incapsulate</span><span class="sxs-lookup"><span data-stu-id="bfd48-103">ISCardCmd::Encapsulate method</span></span>

<span data-ttu-id="bfd48-104">\[Il metodo **incapsula** è disponibile per l'uso nei sistemi operativi specificati nella sezione requisiti.</span><span class="sxs-lookup"><span data-stu-id="bfd48-104">\[The **Encapsulate** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="bfd48-105">Non è disponibile per l'utilizzo in Windows Server 2003 con Service Pack 1 (SP1) e versioni successive, Windows Vista, Windows Server 2008 e versioni successive del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="bfd48-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="bfd48-106">I [moduli Smart Card](/previous-versions/windows/desktop/secsmart/smart-card-modules) offrono funzionalità simili.\]</span><span class="sxs-lookup"><span data-stu-id="bfd48-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="bfd48-107">Il metodo **incapsula** incapsula l' [*unità dati del protocollo dell'applicazione*](../secgloss/a-gly.md) del comando specificata (APDU) in un altro comando APDU per la trasmissione a una [*Smart Card*](../secgloss/s-gly.md).</span><span class="sxs-lookup"><span data-stu-id="bfd48-107">The **Encapsulate** method encapsulates the given command [*application protocol data unit*](../secgloss/a-gly.md) (APDU) into another command APDU for transmission to a [*smart card*](../secgloss/s-gly.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="bfd48-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="bfd48-108">Syntax</span></span>


```C++
HRESULT Encapsulate(
  [in] LPBYTEBUFFER  pApdu,
  [in] ISO_APDU_TYPE ApduType
);
```



## <a name="parameters"></a><span data-ttu-id="bfd48-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="bfd48-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bfd48-110">*pApdu* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="bfd48-110">*pApdu* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bfd48-111">Puntatore a APDU da incapsulare.</span><span class="sxs-lookup"><span data-stu-id="bfd48-111">Pointer to the APDU to be encapsulated.</span></span>

</dd> <dt>

<span data-ttu-id="bfd48-112">*ApduType* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="bfd48-112">*ApduType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bfd48-113">ISO 7816-4 caso per trasmissioni [*T = 0*](../secgloss/t-gly.md) .</span><span class="sxs-lookup"><span data-stu-id="bfd48-113">ISO 7816-4 case for [*T=0*](../secgloss/t-gly.md) transmissions.</span></span>

<dl><span id="ISO_CASE_1"></span><span id="iso_case_1"></span><dt>

<span data-ttu-id="bfd48-114">**\_Caso ISO \_ 1**</span><span class="sxs-lookup"><span data-stu-id="bfd48-114">**ISO\_CASE\_1**</span></span>
</dt><span id="ISO_CASE_2"></span><span id="iso_case_2"></span><dt>

<span data-ttu-id="bfd48-115">**\_Caso ISO \_ 2**</span><span class="sxs-lookup"><span data-stu-id="bfd48-115">**ISO\_CASE\_2**</span></span>
</dt><span id="ISO_CASE_3"></span><span id="iso_case_3"></span><dt>

<span data-ttu-id="bfd48-116">**\_Caso ISO \_ 3**</span><span class="sxs-lookup"><span data-stu-id="bfd48-116">**ISO\_CASE\_3**</span></span>
</dt><span id="ISO_CASE_4"></span><span id="iso_case_4"></span><dt>

<span data-ttu-id="bfd48-117">**\_Caso ISO \_ 4**</span><span class="sxs-lookup"><span data-stu-id="bfd48-117">**ISO\_CASE\_4**</span></span>
</dt> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bfd48-118">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="bfd48-118">Return value</span></span>

<span data-ttu-id="bfd48-119">Il metodo restituisce uno dei valori possibili seguenti.</span><span class="sxs-lookup"><span data-stu-id="bfd48-119">The method returns one of the following possible values.</span></span>



| <span data-ttu-id="bfd48-120">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="bfd48-120">Return code</span></span>                                                                                   | <span data-ttu-id="bfd48-121">Descrizione</span><span class="sxs-lookup"><span data-stu-id="bfd48-121">Description</span></span>                                     |
|-----------------------------------------------------------------------------------------------|-------------------------------------------------|
| <dl> <span data-ttu-id="bfd48-122"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="bfd48-122"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="bfd48-123">Operazione completata correttamente.</span><span class="sxs-lookup"><span data-stu-id="bfd48-123">Operation completed successfully.</span></span><br/>    |
| <dl> <span data-ttu-id="bfd48-124"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="bfd48-124"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="bfd48-125">Parametro non valido.</span><span class="sxs-lookup"><span data-stu-id="bfd48-125">Invalid parameter.</span></span><br/>                   |
| <dl> <span data-ttu-id="bfd48-126"><dt>**\_puntatore E**</dt></span><span class="sxs-lookup"><span data-stu-id="bfd48-126"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="bfd48-127">Un puntatore errato è stato passato in *pApdu*.</span><span class="sxs-lookup"><span data-stu-id="bfd48-127">A bad pointer was passed in *pApdu*.</span></span><br/> |
| <dl> <span data-ttu-id="bfd48-128"><dt>**E \_ OutOfMemory**</dt></span><span class="sxs-lookup"><span data-stu-id="bfd48-128"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="bfd48-129">Memoria insufficiente.</span><span class="sxs-lookup"><span data-stu-id="bfd48-129">Out of memory.</span></span><br/>                       |



 

## <a name="remarks"></a><span data-ttu-id="bfd48-130">Commenti</span><span class="sxs-lookup"><span data-stu-id="bfd48-130">Remarks</span></span>

<span data-ttu-id="bfd48-131">Per compilare un comando APDU, chiamare [**BuildCmd**](iscardcmd-buildcmd.md).</span><span class="sxs-lookup"><span data-stu-id="bfd48-131">To build a command APDU, call [**BuildCmd**](iscardcmd-buildcmd.md).</span></span>

<span data-ttu-id="bfd48-132">Per un elenco di tutti i metodi forniti da questa interfaccia, vedere [**ISCardCmd**](iscardcmd.md).</span><span class="sxs-lookup"><span data-stu-id="bfd48-132">For a list of all the methods provided by this interface, see [**ISCardCmd**](iscardcmd.md).</span></span>

<span data-ttu-id="bfd48-133">Oltre ai codici di errore COM elencati sopra, questa interfaccia può restituire un codice di errore della smart card se è stata chiamata una funzione Smart Card per completare la richiesta.</span><span class="sxs-lookup"><span data-stu-id="bfd48-133">In addition to the COM error codes listed above, this interface may return a smart card error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="bfd48-134">Per ulteriori informazioni, vedere [valori restituiti della smart card](authentication-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="bfd48-134">For more information, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="examples"></a><span data-ttu-id="bfd48-135">Esempio</span><span class="sxs-lookup"><span data-stu-id="bfd48-135">Examples</span></span>

<span data-ttu-id="bfd48-136">Nell'esempio seguente viene illustrato come incapsulare un comando APDU.</span><span class="sxs-lookup"><span data-stu-id="bfd48-136">The following example shows how to encapsulate a command APDU.</span></span> <span data-ttu-id="bfd48-137">Nell'esempio si presuppone che pIByteApdu sia un puntatore valido a un'istanza dell'interfaccia [**IByteBuffer**](ibytebuffer.md) .</span><span class="sxs-lookup"><span data-stu-id="bfd48-137">The example assumes that pIByteApdu is a valid pointer to an instance of the [**IByteBuffer**](ibytebuffer.md) interface.</span></span>


```C++
HRESULT    hr;

// pIByteApdu is a pointer to an instance of IByteBuffer.
// Encapsulate the APDU.
hr = pISCardCmd->Encapsulate(pIByteApdu, ISO_CASE_1);
if (FAILED(hr)) 
{
    printf("Failed Encapsulate.\n");
    // Take other error handling action as needed.
}
```



## <a name="requirements"></a><span data-ttu-id="bfd48-138">Requisiti</span><span class="sxs-lookup"><span data-stu-id="bfd48-138">Requirements</span></span>



| <span data-ttu-id="bfd48-139">Requisito</span><span class="sxs-lookup"><span data-stu-id="bfd48-139">Requirement</span></span> | <span data-ttu-id="bfd48-140">Valore</span><span class="sxs-lookup"><span data-stu-id="bfd48-140">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="bfd48-141">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="bfd48-141">Minimum supported client</span></span><br/> | <span data-ttu-id="bfd48-142">\[Solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="bfd48-142">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="bfd48-143">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="bfd48-143">Minimum supported server</span></span><br/> | <span data-ttu-id="bfd48-144">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="bfd48-144">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="bfd48-145">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="bfd48-145">End of client support</span></span><br/>    | <span data-ttu-id="bfd48-146">Windows XP</span><span class="sxs-lookup"><span data-stu-id="bfd48-146">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="bfd48-147">Fine del supporto server</span><span class="sxs-lookup"><span data-stu-id="bfd48-147">End of server support</span></span><br/>    | <span data-ttu-id="bfd48-148">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="bfd48-148">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="bfd48-149">Intestazione</span><span class="sxs-lookup"><span data-stu-id="bfd48-149">Header</span></span><br/>                   | <dl> <span data-ttu-id="bfd48-150"><dt>Scarddat. h</dt></span><span class="sxs-lookup"><span data-stu-id="bfd48-150"><dt>Scarddat.h</dt></span></span> </dl>   |
| <span data-ttu-id="bfd48-151">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="bfd48-151">Type library</span></span><br/>             | <dl> <span data-ttu-id="bfd48-152"><dt>Scarddat. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="bfd48-152"><dt>Scarddat.tlb</dt></span></span> </dl> |
| <span data-ttu-id="bfd48-153">DLL</span><span class="sxs-lookup"><span data-stu-id="bfd48-153">DLL</span></span><br/>                      | <dl> <span data-ttu-id="bfd48-154"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bfd48-154"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="bfd48-155">IID</span><span class="sxs-lookup"><span data-stu-id="bfd48-155">IID</span></span><br/>                      | <span data-ttu-id="bfd48-156">IID \_ ISCardCmd è definito come D5778AE3-43DE-11D0-9171-00AA00C18068</span><span class="sxs-lookup"><span data-stu-id="bfd48-156">IID\_ISCardCmd is defined as D5778AE3-43DE-11D0-9171-00AA00C18068</span></span><br/>            |



## <a name="see-also"></a><span data-ttu-id="bfd48-157">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="bfd48-157">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bfd48-158">**BuildCmd**</span><span class="sxs-lookup"><span data-stu-id="bfd48-158">**BuildCmd**</span></span>](iscardcmd-buildcmd.md)
</dt> <dt>

[<span data-ttu-id="bfd48-159">**ISCardCmd**</span><span class="sxs-lookup"><span data-stu-id="bfd48-159">**ISCardCmd**</span></span>](iscardcmd.md)
</dt> </dl>

 

 
