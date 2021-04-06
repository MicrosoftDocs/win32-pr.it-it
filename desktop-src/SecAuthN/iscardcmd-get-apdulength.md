---
description: Determina la lunghezza, in byte, dell'unità dati del protocollo dell'applicazione (APDU).
ms.assetid: 005345d0-afdd-4534-9926-12378546d0ef
title: 'Metodo ISCardCmd:: get_ApduLength (Scarddat. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardCmd.get_ApduLength
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 1535d2b4b67861b42719506ebd48cca4c49d5c38
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103760115"
---
# <a name="iscardcmdget_apdulength-method"></a><span data-ttu-id="4784d-103">Metodo ISCardCmd:: Get \_ ApduLength</span><span class="sxs-lookup"><span data-stu-id="4784d-103">ISCardCmd::get\_ApduLength method</span></span>

<span data-ttu-id="4784d-104">\[Il metodo **get \_ ApduLength** è disponibile per l'uso nei sistemi operativi specificati nella sezione requisiti.</span><span class="sxs-lookup"><span data-stu-id="4784d-104">\[The **get\_ApduLength** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="4784d-105">Non è disponibile per l'utilizzo in Windows Server 2003 con Service Pack 1 (SP1) e versioni successive, Windows Vista, Windows Server 2008 e versioni successive del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="4784d-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="4784d-106">I [moduli Smart Card](/previous-versions/windows/desktop/secsmart/smart-card-modules) offrono funzionalità simili.\]</span><span class="sxs-lookup"><span data-stu-id="4784d-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="4784d-107">Il metodo **get \_ ApduLength** determina la lunghezza, in byte, dell' [*unità dati del protocollo dell'applicazione*](../secgloss/a-gly.md) (APDU).</span><span class="sxs-lookup"><span data-stu-id="4784d-107">The **get\_ApduLength** method determines the length, in bytes, f the [*application protocol data unit*](../secgloss/a-gly.md) (APDU).</span></span>

## <a name="syntax"></a><span data-ttu-id="4784d-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="4784d-108">Syntax</span></span>


```C++
HRESULT get_ApduLength(
  [out] LONG *plSize
);
```



## <a name="parameters"></a><span data-ttu-id="4784d-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="4784d-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4784d-110">*plSize* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="4784d-110">*plSize* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="4784d-111">Puntatore alla lunghezza di APDU.</span><span class="sxs-lookup"><span data-stu-id="4784d-111">Pointer to the length of the APDU.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4784d-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="4784d-112">Return value</span></span>

<span data-ttu-id="4784d-113">Il metodo restituisce uno dei valori possibili seguenti.</span><span class="sxs-lookup"><span data-stu-id="4784d-113">The method returns one of the following possible values.</span></span>



| <span data-ttu-id="4784d-114">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="4784d-114">Return code</span></span>                                                                                   | <span data-ttu-id="4784d-115">Descrizione</span><span class="sxs-lookup"><span data-stu-id="4784d-115">Description</span></span>                                      |
|-----------------------------------------------------------------------------------------------|--------------------------------------------------|
| <dl> <span data-ttu-id="4784d-116"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="4784d-116"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="4784d-117">Operazione completata correttamente.</span><span class="sxs-lookup"><span data-stu-id="4784d-117">Operation completed successfully.</span></span><br/>     |
| <dl> <span data-ttu-id="4784d-118"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="4784d-118"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="4784d-119">Il parametro *plSize* non è valido.</span><span class="sxs-lookup"><span data-stu-id="4784d-119">The *plSize* parameter is not valid.</span></span><br/>  |
| <dl> <span data-ttu-id="4784d-120"><dt>**\_puntatore E**</dt></span><span class="sxs-lookup"><span data-stu-id="4784d-120"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="4784d-121">Un puntatore errato è stato passato in *plSize*.</span><span class="sxs-lookup"><span data-stu-id="4784d-121">A bad pointer was passed in *plSize*.</span></span><br/> |
| <dl> <span data-ttu-id="4784d-122"><dt>**E \_ OutOfMemory**</dt></span><span class="sxs-lookup"><span data-stu-id="4784d-122"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="4784d-123">Memoria insufficiente.</span><span class="sxs-lookup"><span data-stu-id="4784d-123">Out of memory.</span></span><br/>                        |



 

## <a name="remarks"></a><span data-ttu-id="4784d-124">Commenti</span><span class="sxs-lookup"><span data-stu-id="4784d-124">Remarks</span></span>

<span data-ttu-id="4784d-125">Per recuperare l' [*unità dati del protocollo applicazione*](../secgloss/a-gly.md) (APDU) non elaborata dal buffer di byte mappato tramite un **IStream** che contiene il messaggio APDU, chiamare [**get \_ APDU**](iscardcmd-get-apdu.md).</span><span class="sxs-lookup"><span data-stu-id="4784d-125">To retrieve the raw [*application protocol data unit*](../secgloss/a-gly.md) (APDU) from the byte buffer mapped through an **IStream** that contains the APDU message, call [**get\_Apdu**](iscardcmd-get-apdu.md).</span></span>

<span data-ttu-id="4784d-126">Per un elenco di tutti i metodi forniti da questa interfaccia, vedere [**ISCardCmd**](iscardcmd.md).</span><span class="sxs-lookup"><span data-stu-id="4784d-126">For a list of all the methods provided by this interface, see [**ISCardCmd**](iscardcmd.md).</span></span>

<span data-ttu-id="4784d-127">Oltre ai codici di errore COM elencati sopra, questa interfaccia può restituire un codice di errore della smart card se è stata chiamata una funzione Smart Card per completare la richiesta.</span><span class="sxs-lookup"><span data-stu-id="4784d-127">In addition to the COM error codes listed above, this interface may return a smart card error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="4784d-128">Per ulteriori informazioni, vedere [valori restituiti della smart card](authentication-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="4784d-128">For more information, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="examples"></a><span data-ttu-id="4784d-129">Esempio</span><span class="sxs-lookup"><span data-stu-id="4784d-129">Examples</span></span>

<span data-ttu-id="4784d-130">Nell'esempio seguente viene illustrato come recuperare la lunghezza dell' [*unità dati del protocollo dell'applicazione*](../secgloss/a-gly.md) (APDU).</span><span class="sxs-lookup"><span data-stu-id="4784d-130">The following example shows how to retrieve the [*application protocol data unit*](../secgloss/a-gly.md) (APDU) length.</span></span> <span data-ttu-id="4784d-131">Nell'esempio si presuppone che pISCardCmd sia un puntatore valido a un'istanza dell'interfaccia [**ISCardCmd**](iscardcmd.md) .</span><span class="sxs-lookup"><span data-stu-id="4784d-131">The example assumes that pISCardCmd is a valid pointer to an instance of the [**ISCardCmd**](iscardcmd.md) interface.</span></span>


```C++
LONG    lLen;
HRESULT hr;

// Retrieve the APDU length.
hr = pISCardCmd->get_ApduLength(&lLen);
if (FAILED(hr))
{
    printf("Failed get_ApduLength\n");
    // Take other error handling action.
}
else
    printf("Length returned is %d\n", lLen);
```



## <a name="requirements"></a><span data-ttu-id="4784d-132">Requisiti</span><span class="sxs-lookup"><span data-stu-id="4784d-132">Requirements</span></span>



| <span data-ttu-id="4784d-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="4784d-133">Requirement</span></span> | <span data-ttu-id="4784d-134">Valore</span><span class="sxs-lookup"><span data-stu-id="4784d-134">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="4784d-135">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4784d-135">Minimum supported client</span></span><br/> | <span data-ttu-id="4784d-136">\[Solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="4784d-136">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="4784d-137">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4784d-137">Minimum supported server</span></span><br/> | <span data-ttu-id="4784d-138">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="4784d-138">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="4784d-139">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="4784d-139">End of client support</span></span><br/>    | <span data-ttu-id="4784d-140">Windows XP</span><span class="sxs-lookup"><span data-stu-id="4784d-140">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="4784d-141">Fine del supporto server</span><span class="sxs-lookup"><span data-stu-id="4784d-141">End of server support</span></span><br/>    | <span data-ttu-id="4784d-142">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="4784d-142">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="4784d-143">Intestazione</span><span class="sxs-lookup"><span data-stu-id="4784d-143">Header</span></span><br/>                   | <dl> <span data-ttu-id="4784d-144"><dt>Scarddat. h</dt></span><span class="sxs-lookup"><span data-stu-id="4784d-144"><dt>Scarddat.h</dt></span></span> </dl>   |
| <span data-ttu-id="4784d-145">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="4784d-145">Type library</span></span><br/>             | <dl> <span data-ttu-id="4784d-146"><dt>Scarddat. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="4784d-146"><dt>Scarddat.tlb</dt></span></span> </dl> |
| <span data-ttu-id="4784d-147">DLL</span><span class="sxs-lookup"><span data-stu-id="4784d-147">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4784d-148"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4784d-148"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="4784d-149">IID</span><span class="sxs-lookup"><span data-stu-id="4784d-149">IID</span></span><br/>                      | <span data-ttu-id="4784d-150">IID \_ ISCardCmd è definito come D5778AE3-43DE-11D0-9171-00AA00C18068</span><span class="sxs-lookup"><span data-stu-id="4784d-150">IID\_ISCardCmd is defined as D5778AE3-43DE-11D0-9171-00AA00C18068</span></span><br/>            |



## <a name="see-also"></a><span data-ttu-id="4784d-151">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="4784d-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4784d-152">**ottenere \_ APDU**</span><span class="sxs-lookup"><span data-stu-id="4784d-152">**get\_Apdu**</span></span>](iscardcmd-get-apdu.md)
</dt> <dt>

[<span data-ttu-id="4784d-153">**ISCardCmd**</span><span class="sxs-lookup"><span data-stu-id="4784d-153">**ISCardCmd**</span></span>](iscardcmd.md)
</dt> </dl>

 

 
