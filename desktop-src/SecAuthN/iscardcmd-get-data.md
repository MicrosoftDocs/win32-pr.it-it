---
description: Recupera il campo dati dall'unità dati del protocollo dell'applicazione (APDU), inserendolo in un oggetto buffer di byte.
ms.assetid: fbffeeeb-56e5-4484-b294-8b6f59c919eb
title: 'Metodo ISCardCmd:: get_Data (Scarddat. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardCmd.get_Data
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: feb6a8c28316bd4fd08160063606d3e15054fd87
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104530222"
---
# <a name="iscardcmdget_data-method"></a><span data-ttu-id="ccc7b-103">Metodo ISCardCmd:: Get \_ Data</span><span class="sxs-lookup"><span data-stu-id="ccc7b-103">ISCardCmd::get\_Data method</span></span>

<span data-ttu-id="ccc7b-104">\[Il metodo **get \_ Data** è disponibile per l'uso nei sistemi operativi specificati nella sezione requisiti.</span><span class="sxs-lookup"><span data-stu-id="ccc7b-104">\[The **get\_Data** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="ccc7b-105">Non è disponibile per l'utilizzo in Windows Server 2003 con Service Pack 1 (SP1) e versioni successive, Windows Vista, Windows Server 2008 e versioni successive del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="ccc7b-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="ccc7b-106">I [moduli Smart Card](/previous-versions/windows/desktop/secsmart/smart-card-modules) offrono funzionalità simili.\]</span><span class="sxs-lookup"><span data-stu-id="ccc7b-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="ccc7b-107">Il metodo **get \_ Data** Recupera il campo dati dall' [*unità dati del protocollo dell'applicazione*](../secgloss/a-gly.md) (APDU), inserendolo in un oggetto buffer di byte.</span><span class="sxs-lookup"><span data-stu-id="ccc7b-107">The **get\_Data** method retrieves the data field from the [*application protocol data unit*](../secgloss/a-gly.md) (APDU), placing it in a byte buffer object.</span></span>

## <a name="syntax"></a><span data-ttu-id="ccc7b-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="ccc7b-108">Syntax</span></span>


```C++
HRESULT get_Data(
  [out] LPBYTEBUFFER *ppData
);
```



## <a name="parameters"></a><span data-ttu-id="ccc7b-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="ccc7b-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ccc7b-110">*ppData* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="ccc7b-110">*ppData* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ccc7b-111">Puntatore all'oggetto **IStream**(byte buffer Object) che include il campo dati APDU al ritorno.</span><span class="sxs-lookup"><span data-stu-id="ccc7b-111">Pointer to the byte buffer object (**IStream**) that holds the APDU data field on return.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ccc7b-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="ccc7b-112">Return value</span></span>

<span data-ttu-id="ccc7b-113">Il metodo restituisce uno dei valori possibili seguenti.</span><span class="sxs-lookup"><span data-stu-id="ccc7b-113">The method returns one of the following possible values.</span></span>



| <span data-ttu-id="ccc7b-114">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="ccc7b-114">Return code</span></span>                                                                                   | <span data-ttu-id="ccc7b-115">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ccc7b-115">Description</span></span>                                      |
|-----------------------------------------------------------------------------------------------|--------------------------------------------------|
| <dl> <span data-ttu-id="ccc7b-116"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="ccc7b-116"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="ccc7b-117">Operazione completata correttamente.</span><span class="sxs-lookup"><span data-stu-id="ccc7b-117">Operation completed successfully.</span></span><br/>     |
| <dl> <span data-ttu-id="ccc7b-118"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="ccc7b-118"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="ccc7b-119">Il parametro *ppData* non è valido.</span><span class="sxs-lookup"><span data-stu-id="ccc7b-119">The *ppData* parameter is not valid.</span></span><br/>  |
| <dl> <span data-ttu-id="ccc7b-120"><dt>**\_puntatore E**</dt></span><span class="sxs-lookup"><span data-stu-id="ccc7b-120"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="ccc7b-121">Un puntatore errato è stato passato in *ppData*.</span><span class="sxs-lookup"><span data-stu-id="ccc7b-121">A bad pointer was passed in *ppData*.</span></span><br/> |
| <dl> <span data-ttu-id="ccc7b-122"><dt>**E \_ OutOfMemory**</dt></span><span class="sxs-lookup"><span data-stu-id="ccc7b-122"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="ccc7b-123">Memoria insufficiente.</span><span class="sxs-lookup"><span data-stu-id="ccc7b-123">Out of memory.</span></span><br/>                        |



 

## <a name="remarks"></a><span data-ttu-id="ccc7b-124">Commenti</span><span class="sxs-lookup"><span data-stu-id="ccc7b-124">Remarks</span></span>

<span data-ttu-id="ccc7b-125">Per impostare il campo dati di APDU, chiamare [**put \_ Data**](iscardcmd-put-data.md).</span><span class="sxs-lookup"><span data-stu-id="ccc7b-125">To set the data field of the APDU, call [**put\_Data**](iscardcmd-put-data.md).</span></span>

<span data-ttu-id="ccc7b-126">Per un elenco di tutti i metodi forniti da questa interfaccia, vedere [**ISCardCmd**](iscardcmd.md).</span><span class="sxs-lookup"><span data-stu-id="ccc7b-126">For a list of all the methods provided by this interface, see [**ISCardCmd**](iscardcmd.md).</span></span>

<span data-ttu-id="ccc7b-127">Oltre ai codici di errore COM elencati sopra, questa interfaccia può restituire un codice di errore della [*Smart Card*](../secgloss/s-gly.md) se è stata chiamata una funzione Smart Card per completare la richiesta.</span><span class="sxs-lookup"><span data-stu-id="ccc7b-127">In addition to the COM error codes listed above, this interface may return a [*smart card*](../secgloss/s-gly.md) error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="ccc7b-128">Per ulteriori informazioni, vedere [valori restituiti della smart card](authentication-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="ccc7b-128">For more information, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="examples"></a><span data-ttu-id="ccc7b-129">Esempio</span><span class="sxs-lookup"><span data-stu-id="ccc7b-129">Examples</span></span>

<span data-ttu-id="ccc7b-130">Nell'esempio seguente viene illustrato come recuperare il campo dati dell' [*unità dati del protocollo dell'applicazione*](../secgloss/a-gly.md) (APDU).</span><span class="sxs-lookup"><span data-stu-id="ccc7b-130">The following example shows how to retrieve the data field of the [*application protocol data unit*](../secgloss/a-gly.md) (APDU).</span></span> <span data-ttu-id="ccc7b-131">Nell'esempio si presuppone che pIByteData sia un puntatore valido a un'istanza dell'interfaccia [**IByteBuffer**](ibytebuffer.md) e che pISCardCmd sia un puntatore valido a un'istanza dell'interfaccia [**ISCardCmd**](iscardcmd.md) .</span><span class="sxs-lookup"><span data-stu-id="ccc7b-131">The example assumes that pIByteData is a valid pointer to an instance of the [**IByteBuffer**](ibytebuffer.md) interface, and that pISCardCmd is a valid pointer to an instance of the [**ISCardCmd**](iscardcmd.md) interface.</span></span>


```C++
HRESULT    hr;

// pIByteData is a pointer to an instance of IByteBuffer.
// Retrieve the data.
hr = pISCardCmd->get_Data(&pIByteData);
if (FAILED(hr)) 
{
    printf("Failed get_Data.\n");
    // Take other error handling action as needed.
}
```



## <a name="requirements"></a><span data-ttu-id="ccc7b-132">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ccc7b-132">Requirements</span></span>



| <span data-ttu-id="ccc7b-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="ccc7b-133">Requirement</span></span> | <span data-ttu-id="ccc7b-134">Valore</span><span class="sxs-lookup"><span data-stu-id="ccc7b-134">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="ccc7b-135">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ccc7b-135">Minimum supported client</span></span><br/> | <span data-ttu-id="ccc7b-136">\[Solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="ccc7b-136">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="ccc7b-137">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ccc7b-137">Minimum supported server</span></span><br/> | <span data-ttu-id="ccc7b-138">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="ccc7b-138">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="ccc7b-139">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="ccc7b-139">End of client support</span></span><br/>    | <span data-ttu-id="ccc7b-140">Windows XP</span><span class="sxs-lookup"><span data-stu-id="ccc7b-140">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="ccc7b-141">Fine del supporto server</span><span class="sxs-lookup"><span data-stu-id="ccc7b-141">End of server support</span></span><br/>    | <span data-ttu-id="ccc7b-142">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="ccc7b-142">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="ccc7b-143">Intestazione</span><span class="sxs-lookup"><span data-stu-id="ccc7b-143">Header</span></span><br/>                   | <dl> <span data-ttu-id="ccc7b-144"><dt>Scarddat. h</dt></span><span class="sxs-lookup"><span data-stu-id="ccc7b-144"><dt>Scarddat.h</dt></span></span> </dl>   |
| <span data-ttu-id="ccc7b-145">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="ccc7b-145">Type library</span></span><br/>             | <dl> <span data-ttu-id="ccc7b-146"><dt>Scarddat. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="ccc7b-146"><dt>Scarddat.tlb</dt></span></span> </dl> |
| <span data-ttu-id="ccc7b-147">DLL</span><span class="sxs-lookup"><span data-stu-id="ccc7b-147">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ccc7b-148"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ccc7b-148"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="ccc7b-149">IID</span><span class="sxs-lookup"><span data-stu-id="ccc7b-149">IID</span></span><br/>                      | <span data-ttu-id="ccc7b-150">IID \_ ISCardCmd è definito come D5778AE3-43DE-11D0-9171-00AA00C18068</span><span class="sxs-lookup"><span data-stu-id="ccc7b-150">IID\_ISCardCmd is defined as D5778AE3-43DE-11D0-9171-00AA00C18068</span></span><br/>            |



## <a name="see-also"></a><span data-ttu-id="ccc7b-151">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="ccc7b-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ccc7b-152">**ISCardCmd**</span><span class="sxs-lookup"><span data-stu-id="ccc7b-152">**ISCardCmd**</span></span>](iscardcmd.md)
</dt> <dt>

[<span data-ttu-id="ccc7b-153">**Inserisci \_ dati**</span><span class="sxs-lookup"><span data-stu-id="ccc7b-153">**put\_Data**</span></span>](iscardcmd-put-data.md)
</dt> </dl>

 

 
