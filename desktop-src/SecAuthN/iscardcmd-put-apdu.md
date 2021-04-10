---
description: Copia l'unità dati del protocollo dell'applicazione (APDU) dall'oggetto IByteBuffer (IStream) in APDU di cui è stato eseguito il wrapper in questo oggetto interfaccia.
ms.assetid: 28dac222-ee7a-40aa-903b-e9c0b7757c9c
title: 'ISCardCmd: metodo:p ut_Apdu (Scarddat. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardCmd.put_Apdu
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: ee615e7f2e8d7555cfed276658e8de1a97ddf73a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103966699"
---
# <a name="iscardcmdput_apdu-method"></a><span data-ttu-id="e80fa-103">ISCardCmd::p UT \_ APDU metodo</span><span class="sxs-lookup"><span data-stu-id="e80fa-103">ISCardCmd::put\_Apdu method</span></span>

<span data-ttu-id="e80fa-104">\[Il metodo **put \_ APDU** è disponibile per l'uso nei sistemi operativi specificati nella sezione requisiti.</span><span class="sxs-lookup"><span data-stu-id="e80fa-104">\[The **put\_Apdu** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="e80fa-105">Non è disponibile per l'utilizzo in Windows Server 2003 con Service Pack 1 (SP1) e versioni successive, Windows Vista, Windows Server 2008 e versioni successive del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="e80fa-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="e80fa-106">I [moduli Smart Card](/previous-versions/windows/desktop/secsmart/smart-card-modules) offrono funzionalità simili.\]</span><span class="sxs-lookup"><span data-stu-id="e80fa-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="e80fa-107">Il **metodo Put \_ APDU** copia l' [*unità dati del protocollo dell'applicazione*](../secgloss/a-gly.md) (APDU) dall'oggetto [**IByteBuffer**](ibytebuffer.md) (**IStream**) nel APDU di cui è stato eseguito il wrapper in questo oggetto interfaccia.</span><span class="sxs-lookup"><span data-stu-id="e80fa-107">The **put\_Apdu** method copies the [*application protocol data unit*](../secgloss/a-gly.md) (APDU) from the [**IByteBuffer**](ibytebuffer.md) (**IStream**) object into the APDU wrapped in this interface object.</span></span>

## <a name="syntax"></a><span data-ttu-id="e80fa-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="e80fa-108">Syntax</span></span>


```C++
HRESULT put_Apdu(
  [in] LPBYTEBUFFER pApdu
);
```



## <a name="parameters"></a><span data-ttu-id="e80fa-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="e80fa-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e80fa-110">*pApdu* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e80fa-110">*pApdu* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e80fa-111">Puntatore al APDU ISO 7816-4 da copiare in.</span><span class="sxs-lookup"><span data-stu-id="e80fa-111">Pointer to the ISO 7816-4 APDU to be copied in.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e80fa-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="e80fa-112">Return value</span></span>

<span data-ttu-id="e80fa-113">Il metodo restituisce uno dei valori possibili seguenti.</span><span class="sxs-lookup"><span data-stu-id="e80fa-113">The method returns one of the following possible values.</span></span>



| <span data-ttu-id="e80fa-114">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="e80fa-114">Return code</span></span>                                                                                   | <span data-ttu-id="e80fa-115">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e80fa-115">Description</span></span>                                     |
|-----------------------------------------------------------------------------------------------|-------------------------------------------------|
| <dl> <span data-ttu-id="e80fa-116"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="e80fa-116"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="e80fa-117">Operazione completata correttamente.</span><span class="sxs-lookup"><span data-stu-id="e80fa-117">Operation completed successfully.</span></span><br/>    |
| <dl> <span data-ttu-id="e80fa-118"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="e80fa-118"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="e80fa-119">Il parametro *pApdu* non è valido.</span><span class="sxs-lookup"><span data-stu-id="e80fa-119">The *pApdu* parameter is not valid.</span></span><br/>  |
| <dl> <span data-ttu-id="e80fa-120"><dt>**\_puntatore E**</dt></span><span class="sxs-lookup"><span data-stu-id="e80fa-120"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="e80fa-121">Un puntatore errato è stato passato in *pApdu*.</span><span class="sxs-lookup"><span data-stu-id="e80fa-121">A bad pointer was passed in *pApdu*.</span></span><br/> |
| <dl> <span data-ttu-id="e80fa-122"><dt>**E \_ OutOfMemory**</dt></span><span class="sxs-lookup"><span data-stu-id="e80fa-122"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="e80fa-123">Memoria insufficiente.</span><span class="sxs-lookup"><span data-stu-id="e80fa-123">Out of memory.</span></span><br/>                       |



 

## <a name="remarks"></a><span data-ttu-id="e80fa-124">Commenti</span><span class="sxs-lookup"><span data-stu-id="e80fa-124">Remarks</span></span>

<span data-ttu-id="e80fa-125">Per recuperare il APDU non elaborato dal buffer di byte mappato tramite un **IStream** che contiene il messaggio APDU, chiamare [**get \_ APDU**](iscardcmd-get-apdu.md).</span><span class="sxs-lookup"><span data-stu-id="e80fa-125">To retrieve the raw APDU from the byte buffer mapped through an **IStream** that contains the APDU message, call [**get\_Apdu**](iscardcmd-get-apdu.md).</span></span>

<span data-ttu-id="e80fa-126">Per un elenco di tutti i metodi forniti da questa interfaccia, vedere [**ISCardCmd**](iscardcmd.md).</span><span class="sxs-lookup"><span data-stu-id="e80fa-126">For a list of all the methods provided by this interface, see [**ISCardCmd**](iscardcmd.md).</span></span>

<span data-ttu-id="e80fa-127">Oltre ai codici di errore COM elencati sopra, questa interfaccia può restituire un codice di errore della [*Smart Card*](../secgloss/s-gly.md) se è stata chiamata una funzione Smart Card per completare la richiesta.</span><span class="sxs-lookup"><span data-stu-id="e80fa-127">In addition to the COM error codes listed above, this interface may return a [*smart card*](../secgloss/s-gly.md) error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="e80fa-128">Per ulteriori informazioni, vedere [valori restituiti della smart card](authentication-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="e80fa-128">For more information, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="examples"></a><span data-ttu-id="e80fa-129">Esempio</span><span class="sxs-lookup"><span data-stu-id="e80fa-129">Examples</span></span>

<span data-ttu-id="e80fa-130">Nell'esempio seguente viene illustrato come copiare un APDU da un oggetto [**IByteBuffer**](ibytebuffer.md) (**IStream**) in APDU di cui è stato eseguito il wrapper in un oggetto di interfaccia.</span><span class="sxs-lookup"><span data-stu-id="e80fa-130">The following example shows how to copy an APDU from an [**IByteBuffer**](ibytebuffer.md) (**IStream**) object into the APDU wrapped in an interface object.</span></span> <span data-ttu-id="e80fa-131">Nell'esempio si presuppone che pIByteApdu sia un puntatore valido a un'istanza di **IByteBuffer** e che pISCardCmd sia un puntatore valido a un'istanza dell'interfaccia [**ISCardCmd**](iscardcmd.md) .</span><span class="sxs-lookup"><span data-stu-id="e80fa-131">The example assumes that pIByteApdu is a valid pointer to an instance of **IByteBuffer** and that pISCardCmd is a valid pointer to an instance of the [**ISCardCmd**](iscardcmd.md) interface.</span></span>


```C++
HRESULT    hr;


// Set the APDU.
hr = pISCardCmd->put_Apdu(pIByteApdu);
if (FAILED(hr)) 
{
    printf("Failed put_Apdu.\n");
    // Take other error handling action as needed.
}
```



## <a name="requirements"></a><span data-ttu-id="e80fa-132">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e80fa-132">Requirements</span></span>



| <span data-ttu-id="e80fa-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="e80fa-133">Requirement</span></span> | <span data-ttu-id="e80fa-134">Valore</span><span class="sxs-lookup"><span data-stu-id="e80fa-134">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e80fa-135">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e80fa-135">Minimum supported client</span></span><br/> | <span data-ttu-id="e80fa-136">\[Solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="e80fa-136">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="e80fa-137">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e80fa-137">Minimum supported server</span></span><br/> | <span data-ttu-id="e80fa-138">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="e80fa-138">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="e80fa-139">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="e80fa-139">End of client support</span></span><br/>    | <span data-ttu-id="e80fa-140">Windows XP</span><span class="sxs-lookup"><span data-stu-id="e80fa-140">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="e80fa-141">Fine del supporto server</span><span class="sxs-lookup"><span data-stu-id="e80fa-141">End of server support</span></span><br/>    | <span data-ttu-id="e80fa-142">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="e80fa-142">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="e80fa-143">Intestazione</span><span class="sxs-lookup"><span data-stu-id="e80fa-143">Header</span></span><br/>                   | <dl> <span data-ttu-id="e80fa-144"><dt>Scarddat. h</dt></span><span class="sxs-lookup"><span data-stu-id="e80fa-144"><dt>Scarddat.h</dt></span></span> </dl>   |
| <span data-ttu-id="e80fa-145">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="e80fa-145">Type library</span></span><br/>             | <dl> <span data-ttu-id="e80fa-146"><dt>Scarddat. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="e80fa-146"><dt>Scarddat.tlb</dt></span></span> </dl> |
| <span data-ttu-id="e80fa-147">DLL</span><span class="sxs-lookup"><span data-stu-id="e80fa-147">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e80fa-148"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e80fa-148"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="e80fa-149">IID</span><span class="sxs-lookup"><span data-stu-id="e80fa-149">IID</span></span><br/>                      | <span data-ttu-id="e80fa-150">IID \_ ISCardCmd è definito come D5778AE3-43DE-11D0-9171-00AA00C18068</span><span class="sxs-lookup"><span data-stu-id="e80fa-150">IID\_ISCardCmd is defined as D5778AE3-43DE-11D0-9171-00AA00C18068</span></span><br/>            |



## <a name="see-also"></a><span data-ttu-id="e80fa-151">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e80fa-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e80fa-152">**ottenere \_ APDU**</span><span class="sxs-lookup"><span data-stu-id="e80fa-152">**get\_Apdu**</span></span>](iscardcmd-get-apdu.md)
</dt> <dt>

[<span data-ttu-id="e80fa-153">**ISCardCmd**</span><span class="sxs-lookup"><span data-stu-id="e80fa-153">**ISCardCmd**</span></span>](iscardcmd.md)
</dt> </dl>

 

 
