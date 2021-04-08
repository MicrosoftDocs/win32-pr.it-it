---
description: Recupera il APDU di risposta, inserendolo in un buffer di byte specifico.
ms.assetid: ab349e7a-350f-4e72-98b4-4c6431b6e380
title: 'Metodo ISCardCmd:: get_ApduReply (Scarddat. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardCmd.get_ApduReply
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 2ce11ec2d3d8202574ab23074531c393c9fecb98
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104058316"
---
# <a name="iscardcmdget_apdureply-method"></a><span data-ttu-id="c1350-103">Metodo ISCardCmd:: Get \_ ApduReply</span><span class="sxs-lookup"><span data-stu-id="c1350-103">ISCardCmd::get\_ApduReply method</span></span>

<span data-ttu-id="c1350-104">\[Il metodo **get \_ ApduReply** è disponibile per l'uso nei sistemi operativi specificati nella sezione requisiti.</span><span class="sxs-lookup"><span data-stu-id="c1350-104">\[The **get\_ApduReply** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="c1350-105">Non è disponibile per l'utilizzo in Windows Server 2003 con Service Pack 1 (SP1) e versioni successive, Windows Vista, Windows Server 2008 e versioni successive del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="c1350-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="c1350-106">I [moduli Smart Card](/previous-versions/windows/desktop/secsmart/smart-card-modules) offrono funzionalità simili.\]</span><span class="sxs-lookup"><span data-stu-id="c1350-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="c1350-107">Il metodo **get \_ ApduReply** Recupera il [*APDU di risposta*](../secgloss/r-gly.md), inserendolo in un buffer di byte specifico.</span><span class="sxs-lookup"><span data-stu-id="c1350-107">The **get\_ApduReply** method retrieves the [*reply APDU*](../secgloss/r-gly.md), placing it in a specific byte buffer.</span></span> <span data-ttu-id="c1350-108">La risposta potrebbe essere **null** se non è stata eseguita alcuna [*transazione*](../secgloss/t-gly.md) sul comando APDU.</span><span class="sxs-lookup"><span data-stu-id="c1350-108">The reply may be **NULL** if no [*transaction*](../secgloss/t-gly.md) has been performed on the command APDU.</span></span>

## <a name="syntax"></a><span data-ttu-id="c1350-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="c1350-109">Syntax</span></span>


```C++
HRESULT get_ApduReply(
  [out] LPBYTEBUFFER *ppReplyApdu
);
```



## <a name="parameters"></a><span data-ttu-id="c1350-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="c1350-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c1350-111">*ppReplyApdu* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="c1350-111">*ppReplyApdu* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c1350-112">Puntatore al buffer di byte (mappato tramite un oggetto **IStream** ) che contiene il messaggio di risposta APDU al ritorno.</span><span class="sxs-lookup"><span data-stu-id="c1350-112">Pointer to the byte buffer (mapped through an **IStream** object) that contains the APDU reply message on return.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c1350-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="c1350-113">Return value</span></span>

<span data-ttu-id="c1350-114">Il metodo restituisce uno dei valori possibili seguenti.</span><span class="sxs-lookup"><span data-stu-id="c1350-114">The method returns one of the following possible values.</span></span>



| <span data-ttu-id="c1350-115">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="c1350-115">Return code</span></span>                                                                                   | <span data-ttu-id="c1350-116">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c1350-116">Description</span></span>                                           |
|-----------------------------------------------------------------------------------------------|-------------------------------------------------------|
| <dl> <span data-ttu-id="c1350-117"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="c1350-117"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="c1350-118">Operazione completata correttamente.</span><span class="sxs-lookup"><span data-stu-id="c1350-118">Operation completed successfully.</span></span><br/>          |
| <dl> <span data-ttu-id="c1350-119"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="c1350-119"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="c1350-120">Il parametro *ppReplyApdu* non è valido.</span><span class="sxs-lookup"><span data-stu-id="c1350-120">The *ppReplyApdu* parameter is not valid.</span></span><br/>  |
| <dl> <span data-ttu-id="c1350-121"><dt>**\_puntatore E**</dt></span><span class="sxs-lookup"><span data-stu-id="c1350-121"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="c1350-122">Un puntatore errato è stato passato in *ppReplyApdu*.</span><span class="sxs-lookup"><span data-stu-id="c1350-122">A bad pointer was passed in *ppReplyApdu*.</span></span><br/> |
| <dl> <span data-ttu-id="c1350-123"><dt>**E \_ OutOfMemory**</dt></span><span class="sxs-lookup"><span data-stu-id="c1350-123"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="c1350-124">Memoria insufficiente.</span><span class="sxs-lookup"><span data-stu-id="c1350-124">Out of memory.</span></span><br/>                             |



 

## <a name="remarks"></a><span data-ttu-id="c1350-125">Commenti</span><span class="sxs-lookup"><span data-stu-id="c1350-125">Remarks</span></span>

<span data-ttu-id="c1350-126">Per determinare la lunghezza della risposta APDU, chiamare [**get \_ ApduReplyLength**](iscardcmd-get-apdureplylength.md).</span><span class="sxs-lookup"><span data-stu-id="c1350-126">To determine the length of the APDU reply, call [**get\_ApduReplyLength**](iscardcmd-get-apdureplylength.md).</span></span>

<span data-ttu-id="c1350-127">Per impostare un nuovo APDU di risposta, chiamare [**put \_ ApduReply**](iscardcmd-put-apdureply.md).</span><span class="sxs-lookup"><span data-stu-id="c1350-127">To set a new reply APDU, call [**put\_ApduReply**](iscardcmd-put-apdureply.md).</span></span>

<span data-ttu-id="c1350-128">Per un elenco di tutti i metodi forniti da questa interfaccia, vedere [**ISCardCmd**](iscardcmd.md).</span><span class="sxs-lookup"><span data-stu-id="c1350-128">For a list of all the methods provided by this interface, see [**ISCardCmd**](iscardcmd.md).</span></span>

<span data-ttu-id="c1350-129">Oltre ai codici di errore COM elencati sopra, questa interfaccia può restituire un codice di errore della [*Smart Card*](../secgloss/s-gly.md) se è stata chiamata una funzione Smart Card per completare la richiesta.</span><span class="sxs-lookup"><span data-stu-id="c1350-129">In addition to the COM error codes listed above, this interface may return a [*smart card*](../secgloss/s-gly.md) error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="c1350-130">Per ulteriori informazioni, vedere [valori restituiti della smart card](authentication-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="c1350-130">For more information, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="examples"></a><span data-ttu-id="c1350-131">Esempio</span><span class="sxs-lookup"><span data-stu-id="c1350-131">Examples</span></span>

<span data-ttu-id="c1350-132">Nell'esempio seguente viene illustrato come recuperare i dati di risposta.</span><span class="sxs-lookup"><span data-stu-id="c1350-132">The following example shows how to retrieve reply data.</span></span> <span data-ttu-id="c1350-133">Nell'esempio si presuppone che lLe sia una variabile di tipo **Long** il cui valore è stato impostato da una chiamata precedente al metodo [**ISCardCmd:: Get \_ ApduReplyLength**](iscardcmd-get-apdureplylength.md) , che pIByteReply è un puntatore valido a un'istanza dell'interfaccia [**IByteBuffer**](ibytebuffer.md) e che pISCardCmd è un puntatore valido a un'istanza dell'interfaccia [**ISCardCmd**](iscardcmd.md) .</span><span class="sxs-lookup"><span data-stu-id="c1350-133">The example assumes that lLe is a variable of type **LONG** whose value was set by a previous call to the [**ISCardCmd::get\_ApduReplyLength**](iscardcmd-get-apdureplylength.md) method, that pIByteReply is a valid pointer to an instance of the [**IByteBuffer**](ibytebuffer.md) interface, and that pISCardCmd is a valid pointer to an instance of the [**ISCardCmd**](iscardcmd.md) interface.</span></span>


```C++
HRESULT      hr;

if (lLe > 0)
{
    // Get reply data if available.
    hr = pISCardCmd->get_ApduReply(&pIByteReply);
    if (FAILED(hr)) 
    {
        printf("Failed ISCardCmd::get_ApduReply.\n");
        // Take other error handling action as needed.
    }
    else
    {
        BYTE byReplyBytes[256];
        LONG lBytesRead;

        hr = pIByteReply->Read(byReplyBytes, lLe, &lBytesRead);
        if (FAILED(hr))
        {
            printf("Failed IByteBuffer::Read.\n");
            // Take other error handling action as needed.
        }
        // Use the bytes in byReplyBytes as needed.
    }
}
```



## <a name="requirements"></a><span data-ttu-id="c1350-134">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c1350-134">Requirements</span></span>



| <span data-ttu-id="c1350-135">Requisito</span><span class="sxs-lookup"><span data-stu-id="c1350-135">Requirement</span></span> | <span data-ttu-id="c1350-136">Valore</span><span class="sxs-lookup"><span data-stu-id="c1350-136">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c1350-137">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c1350-137">Minimum supported client</span></span><br/> | <span data-ttu-id="c1350-138">\[Solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="c1350-138">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="c1350-139">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c1350-139">Minimum supported server</span></span><br/> | <span data-ttu-id="c1350-140">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="c1350-140">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="c1350-141">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="c1350-141">End of client support</span></span><br/>    | <span data-ttu-id="c1350-142">Windows XP</span><span class="sxs-lookup"><span data-stu-id="c1350-142">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="c1350-143">Fine del supporto server</span><span class="sxs-lookup"><span data-stu-id="c1350-143">End of server support</span></span><br/>    | <span data-ttu-id="c1350-144">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="c1350-144">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="c1350-145">Intestazione</span><span class="sxs-lookup"><span data-stu-id="c1350-145">Header</span></span><br/>                   | <dl> <span data-ttu-id="c1350-146"><dt>Scarddat. h</dt></span><span class="sxs-lookup"><span data-stu-id="c1350-146"><dt>Scarddat.h</dt></span></span> </dl>   |
| <span data-ttu-id="c1350-147">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="c1350-147">Type library</span></span><br/>             | <dl> <span data-ttu-id="c1350-148"><dt>Scarddat. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="c1350-148"><dt>Scarddat.tlb</dt></span></span> </dl> |
| <span data-ttu-id="c1350-149">DLL</span><span class="sxs-lookup"><span data-stu-id="c1350-149">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c1350-150"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c1350-150"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="c1350-151">IID</span><span class="sxs-lookup"><span data-stu-id="c1350-151">IID</span></span><br/>                      | <span data-ttu-id="c1350-152">IID \_ ISCardCmd è definito come D5778AE3-43DE-11D0-9171-00AA00C18068</span><span class="sxs-lookup"><span data-stu-id="c1350-152">IID\_ISCardCmd is defined as D5778AE3-43DE-11D0-9171-00AA00C18068</span></span><br/>            |



## <a name="see-also"></a><span data-ttu-id="c1350-153">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="c1350-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c1350-154">**ottenere \_ ApduReplyLength**</span><span class="sxs-lookup"><span data-stu-id="c1350-154">**get\_ApduReplyLength**</span></span>](iscardcmd-get-apdureplylength.md)
</dt> <dt>

[<span data-ttu-id="c1350-155">**ISCardCmd**</span><span class="sxs-lookup"><span data-stu-id="c1350-155">**ISCardCmd**</span></span>](iscardcmd.md)
</dt> <dt>

[<span data-ttu-id="c1350-156">**Inserisci \_ ApduReply**</span><span class="sxs-lookup"><span data-stu-id="c1350-156">**put\_ApduReply**</span></span>](iscardcmd-put-apdureply.md)
</dt> </dl>

 

 
