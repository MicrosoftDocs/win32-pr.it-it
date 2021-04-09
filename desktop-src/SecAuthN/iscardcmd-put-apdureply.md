---
description: Imposta un nuovo APDU di risposta.
ms.assetid: 1d058c89-0de9-4809-b008-ae24c62acc5b
title: 'ISCardCmd: metodo:p ut_ApduReply (Scarddat. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardCmd.put_ApduReply
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 0292f3ebd4e5f18638ad496cdf15cd9f5c4320f5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103879278"
---
# <a name="iscardcmdput_apdureply-method"></a><span data-ttu-id="ee348-103">ISCardCmd::p UT \_ ApduReply metodo</span><span class="sxs-lookup"><span data-stu-id="ee348-103">ISCardCmd::put\_ApduReply method</span></span>

<span data-ttu-id="ee348-104">\[Il metodo **put \_ ApduReply** è disponibile per l'uso nei sistemi operativi specificati nella sezione requisiti.</span><span class="sxs-lookup"><span data-stu-id="ee348-104">\[The **put\_ApduReply** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="ee348-105">Non è disponibile per l'utilizzo in Windows Server 2003 con Service Pack 1 (SP1) e versioni successive, Windows Vista, Windows Server 2008 e versioni successive del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="ee348-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="ee348-106">I [moduli Smart Card](/previous-versions/windows/desktop/secsmart/smart-card-modules) offrono funzionalità simili.\]</span><span class="sxs-lookup"><span data-stu-id="ee348-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="ee348-107">Il metodo **put \_ ApduReply** imposta un nuovo [*APDU di risposta*](../secgloss/r-gly.md).</span><span class="sxs-lookup"><span data-stu-id="ee348-107">The **put\_ApduReply** method sets a new [*reply APDU*](../secgloss/r-gly.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="ee348-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="ee348-108">Syntax</span></span>


```C++
HRESULT put_ApduReply(
  [in] LPBYTEBUFFER pReplyApdu
);
```



## <a name="parameters"></a><span data-ttu-id="ee348-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="ee348-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ee348-110">*pReplyApdu* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ee348-110">*pReplyApdu* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ee348-111">Puntatore al buffer di byte (mappato tramite un oggetto **IStream** ) che contiene il messaggio di riproduzione APDU al ritorno.</span><span class="sxs-lookup"><span data-stu-id="ee348-111">Pointer to the byte buffer (mapped through an **IStream** object) that contains the replay APDU message on return.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ee348-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="ee348-112">Return value</span></span>

<span data-ttu-id="ee348-113">Il metodo restituisce uno dei valori possibili seguenti.</span><span class="sxs-lookup"><span data-stu-id="ee348-113">The method returns one of the following possible values.</span></span>



| <span data-ttu-id="ee348-114">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="ee348-114">Return code</span></span>                                                                                   | <span data-ttu-id="ee348-115">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ee348-115">Description</span></span>                                          |
|-----------------------------------------------------------------------------------------------|------------------------------------------------------|
| <dl> <span data-ttu-id="ee348-116"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="ee348-116"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="ee348-117">Operazione completata correttamente.</span><span class="sxs-lookup"><span data-stu-id="ee348-117">Operation completed successfully.</span></span><br/>         |
| <dl> <span data-ttu-id="ee348-118"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="ee348-118"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="ee348-119">Il parametro *pReplyApdu* non è valido.</span><span class="sxs-lookup"><span data-stu-id="ee348-119">The *pReplyApdu* parameter is not valid.</span></span><br/>  |
| <dl> <span data-ttu-id="ee348-120"><dt>**\_puntatore E**</dt></span><span class="sxs-lookup"><span data-stu-id="ee348-120"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="ee348-121">Un puntatore errato è stato passato in *pReplyApdu*.</span><span class="sxs-lookup"><span data-stu-id="ee348-121">A bad pointer was passed in *pReplyApdu*.</span></span><br/> |
| <dl> <span data-ttu-id="ee348-122"><dt>**E \_ OutOfMemory**</dt></span><span class="sxs-lookup"><span data-stu-id="ee348-122"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="ee348-123">Memoria insufficiente.</span><span class="sxs-lookup"><span data-stu-id="ee348-123">Out of memory.</span></span><br/>                            |



 

## <a name="remarks"></a><span data-ttu-id="ee348-124">Commenti</span><span class="sxs-lookup"><span data-stu-id="ee348-124">Remarks</span></span>

<span data-ttu-id="ee348-125">Per ottenere un APDU di risposta esistente, chiamare [**get \_ ApduReply**](iscardcmd-get-apdureply.md).</span><span class="sxs-lookup"><span data-stu-id="ee348-125">To get an existing reply APDU, call [**get\_ApduReply**](iscardcmd-get-apdureply.md).</span></span>

<span data-ttu-id="ee348-126">Per un elenco di tutti i metodi forniti da questa interfaccia, vedere [**ISCardCmd**](iscardcmd.md).</span><span class="sxs-lookup"><span data-stu-id="ee348-126">For a list of all the methods provided by this interface, see [**ISCardCmd**](iscardcmd.md).</span></span>

<span data-ttu-id="ee348-127">Oltre ai codici di errore COM elencati sopra, questa interfaccia può restituire un codice di errore della smart card se è stata chiamata una funzione Smart Card per completare la richiesta.</span><span class="sxs-lookup"><span data-stu-id="ee348-127">In addition to the COM error codes listed above, this interface may return a smart card error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="ee348-128">Per ulteriori informazioni, vedere [valori restituiti della smart card](authentication-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="ee348-128">For more information, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="examples"></a><span data-ttu-id="ee348-129">Esempio</span><span class="sxs-lookup"><span data-stu-id="ee348-129">Examples</span></span>

<span data-ttu-id="ee348-130">Nell'esempio seguente viene illustrato come impostare un nuovo [*APDU di risposta*](../secgloss/r-gly.md).</span><span class="sxs-lookup"><span data-stu-id="ee348-130">The following example shows how to set a new [*reply APDU*](../secgloss/r-gly.md).</span></span> <span data-ttu-id="ee348-131">Nell'esempio si presuppone che pIByteReply sia un puntatore valido a un'istanza di [**IByteBuffer**](ibytebuffer.md)e che pISCardCmd sia un puntatore valido a un'istanza dell'interfaccia [**ISCardCmd**](iscardcmd.md) .</span><span class="sxs-lookup"><span data-stu-id="ee348-131">The example assumes that pIByteReply is a valid pointer to an instance of [**IByteBuffer**](ibytebuffer.md), and that pISCardCmd is a valid pointer to an instance of the [**ISCardCmd**](iscardcmd.md) interface.</span></span>


```C++
HRESULT    hr;

// Set the reply data.
hr = pISCardCmd->put_ApduReply(pIByteReply);
if (FAILED(hr)) 
{
    printf("Failed put_ApduReply.\n");
    // Take other error handling action as needed.
}
```



## <a name="requirements"></a><span data-ttu-id="ee348-132">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ee348-132">Requirements</span></span>



| <span data-ttu-id="ee348-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="ee348-133">Requirement</span></span> | <span data-ttu-id="ee348-134">Valore</span><span class="sxs-lookup"><span data-stu-id="ee348-134">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="ee348-135">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ee348-135">Minimum supported client</span></span><br/> | <span data-ttu-id="ee348-136">\[Solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="ee348-136">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="ee348-137">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ee348-137">Minimum supported server</span></span><br/> | <span data-ttu-id="ee348-138">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="ee348-138">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="ee348-139">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="ee348-139">End of client support</span></span><br/>    | <span data-ttu-id="ee348-140">Windows XP</span><span class="sxs-lookup"><span data-stu-id="ee348-140">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="ee348-141">Fine del supporto server</span><span class="sxs-lookup"><span data-stu-id="ee348-141">End of server support</span></span><br/>    | <span data-ttu-id="ee348-142">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="ee348-142">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="ee348-143">Intestazione</span><span class="sxs-lookup"><span data-stu-id="ee348-143">Header</span></span><br/>                   | <dl> <span data-ttu-id="ee348-144"><dt>Scarddat. h</dt></span><span class="sxs-lookup"><span data-stu-id="ee348-144"><dt>Scarddat.h</dt></span></span> </dl>   |
| <span data-ttu-id="ee348-145">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="ee348-145">Type library</span></span><br/>             | <dl> <span data-ttu-id="ee348-146"><dt>Scarddat. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="ee348-146"><dt>Scarddat.tlb</dt></span></span> </dl> |
| <span data-ttu-id="ee348-147">DLL</span><span class="sxs-lookup"><span data-stu-id="ee348-147">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ee348-148"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ee348-148"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="ee348-149">IID</span><span class="sxs-lookup"><span data-stu-id="ee348-149">IID</span></span><br/>                      | <span data-ttu-id="ee348-150">IID \_ ISCardCmd è definito come D5778AE3-43DE-11D0-9171-00AA00C18068</span><span class="sxs-lookup"><span data-stu-id="ee348-150">IID\_ISCardCmd is defined as D5778AE3-43DE-11D0-9171-00AA00C18068</span></span><br/>            |



## <a name="see-also"></a><span data-ttu-id="ee348-151">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="ee348-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ee348-152">**ottenere \_ ApduReply**</span><span class="sxs-lookup"><span data-stu-id="ee348-152">**get\_ApduReply**</span></span>](iscardcmd-get-apdureply.md)
</dt> <dt>

[<span data-ttu-id="ee348-153">**ottenere \_ ApduReplyLength**</span><span class="sxs-lookup"><span data-stu-id="ee348-153">**get\_ApduReplyLength**</span></span>](iscardcmd-get-apdureplylength.md)
</dt> <dt>

[<span data-ttu-id="ee348-154">**ISCardCmd**</span><span class="sxs-lookup"><span data-stu-id="ee348-154">**ISCardCmd**</span></span>](iscardcmd.md)
</dt> </dl>

 

 
