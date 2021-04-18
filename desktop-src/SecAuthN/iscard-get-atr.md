---
description: Recupera una stringa ATR della smart card.
ms.assetid: 2021bd0c-6ef8-4679-be6c-9a9fd33d9fd6
title: 'Metodo IsValid:: get_Atr (Scardmgr. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCard.get_Atr
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 4f2a5688ee85318003ea366bbce614e8250a131a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106317065"
---
# <a name="iscardget_atr-method"></a><span data-ttu-id="3bb2f-103">Metodo IsValid:: Get \_ ATR</span><span class="sxs-lookup"><span data-stu-id="3bb2f-103">ISCard::get\_Atr method</span></span>

<span data-ttu-id="3bb2f-104">\[Il metodo **get \_ ATR** è disponibile per l'uso nei sistemi operativi specificati nella sezione requisiti.</span><span class="sxs-lookup"><span data-stu-id="3bb2f-104">\[The **get\_Atr** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="3bb2f-105">I [moduli Smart Card](/previous-versions/windows/desktop/secsmart/smart-card-modules) offrono funzionalità simili.\]</span><span class="sxs-lookup"><span data-stu-id="3bb2f-105">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="3bb2f-106">Il metodo **get \_ ATR** recupera una [*stringa ATR*](../secgloss/a-gly.md) della [*Smart Card*](../secgloss/s-gly.md).</span><span class="sxs-lookup"><span data-stu-id="3bb2f-106">The **get\_Atr** method retrieves an [*ATR string*](../secgloss/a-gly.md) of the [*smart card*](../secgloss/s-gly.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="3bb2f-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="3bb2f-107">Syntax</span></span>


```C++
HRESULT get_Atr(
  [out] LPBYTEBUFFER *ppAtr
);
```



## <a name="parameters"></a><span data-ttu-id="3bb2f-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="3bb2f-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3bb2f-109">*ppAtr* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="3bb2f-109">*ppAtr* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="3bb2f-110">Puntatore a un buffer di byte sotto forma di [**IStream**](/windows/win32/api/objidl/nn-objidl-istream) che conterrà la stringa ATR al ritorno.</span><span class="sxs-lookup"><span data-stu-id="3bb2f-110">Pointer to a byte buffer in the form of an [**IStream**](/windows/win32/api/objidl/nn-objidl-istream) that will contain the ATR string on return.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3bb2f-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="3bb2f-111">Return value</span></span>

<span data-ttu-id="3bb2f-112">Il metodo restituisce uno dei valori possibili seguenti.</span><span class="sxs-lookup"><span data-stu-id="3bb2f-112">The method returns one of the following possible values.</span></span>



| <span data-ttu-id="3bb2f-113">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="3bb2f-113">Return code</span></span>                                                                                   | <span data-ttu-id="3bb2f-114">Descrizione</span><span class="sxs-lookup"><span data-stu-id="3bb2f-114">Description</span></span>                                              |
|-----------------------------------------------------------------------------------------------|----------------------------------------------------------|
| <dl> <span data-ttu-id="3bb2f-115"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="3bb2f-115"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="3bb2f-116">Operazione completata correttamente.</span><span class="sxs-lookup"><span data-stu-id="3bb2f-116">Operation completed successfully.</span></span><br/>             |
| <dl> <span data-ttu-id="3bb2f-117"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="3bb2f-117"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="3bb2f-118">Il parametro *ppAtr* non è valido.</span><span class="sxs-lookup"><span data-stu-id="3bb2f-118">The *ppAtr* parameter is not valid.</span></span><br/>           |
| <dl> <span data-ttu-id="3bb2f-119"><dt>**\_puntatore E**</dt></span><span class="sxs-lookup"><span data-stu-id="3bb2f-119"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="3bb2f-120">Un puntatore errato è stato passato in *ppAtr*.</span><span class="sxs-lookup"><span data-stu-id="3bb2f-120">A bad pointer was passed in *ppAtr*.</span></span><br/>          |
| <dl> <span data-ttu-id="3bb2f-121"><dt>**E \_ OutOfMemory**</dt></span><span class="sxs-lookup"><span data-stu-id="3bb2f-121"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="3bb2f-122">La memoria per soddisfare la richiesta non è disponibile.</span><span class="sxs-lookup"><span data-stu-id="3bb2f-122">Memory to satisfy the request is unavailable.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="3bb2f-123">Commenti</span><span class="sxs-lookup"><span data-stu-id="3bb2f-123">Remarks</span></span>

<span data-ttu-id="3bb2f-124">Oltre ai codici di errore COM elencati sopra, questa interfaccia può restituire un codice di errore della smart card se è stata chiamata una funzione Smart Card per completare la richiesta.</span><span class="sxs-lookup"><span data-stu-id="3bb2f-124">In addition to the COM error codes listed above, this interface may return a smart card error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="3bb2f-125">Per ulteriori informazioni, vedere [valori restituiti della smart card](authentication-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="3bb2f-125">For more information, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="examples"></a><span data-ttu-id="3bb2f-126">Esempio</span><span class="sxs-lookup"><span data-stu-id="3bb2f-126">Examples</span></span>

<span data-ttu-id="3bb2f-127">Nell'esempio seguente viene illustrato come recuperare la stringa ATR dalla smart card.</span><span class="sxs-lookup"><span data-stu-id="3bb2f-127">The following example shows retrieving the ATR string from the smart card.</span></span>


```C++
// Retrieve the ATR.
// pISCard is a pointer to a previously instantiated ISCard.
// pAtr is a pointer to a previously instantiated IByteBuffer.
hr = pISCard->get_Atr(&pAtr);
if (FAILED(hr))
{
    printf("Failed get_Atr\n");
    // Take other error handling action.
}
// Success, you can now use IByteBuffer::Read to access ATR bytes.
BYTE  byAtr[32];
   long  lBytesRead, i;
   // Read the ATR string into a byte array.
   hr = pAtr->Read(byAtr, 32, &lBytesRead);
   // Use the ATR value. (This example merely displays the bytes.)
   for ( i = 0; i < lBytesRead; i++)
       printf("%c", *(byAtr + i));
   printf("\n");
```



## <a name="requirements"></a><span data-ttu-id="3bb2f-128">Requisiti</span><span class="sxs-lookup"><span data-stu-id="3bb2f-128">Requirements</span></span>



| <span data-ttu-id="3bb2f-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="3bb2f-129">Requirement</span></span> | <span data-ttu-id="3bb2f-130">Valore</span><span class="sxs-lookup"><span data-stu-id="3bb2f-130">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="3bb2f-131">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3bb2f-131">Minimum supported client</span></span><br/> | <span data-ttu-id="3bb2f-132">\[Solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="3bb2f-132">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="3bb2f-133">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3bb2f-133">Minimum supported server</span></span><br/> | <span data-ttu-id="3bb2f-134">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="3bb2f-134">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="3bb2f-135">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="3bb2f-135">End of client support</span></span><br/>    | <span data-ttu-id="3bb2f-136">Windows XP</span><span class="sxs-lookup"><span data-stu-id="3bb2f-136">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="3bb2f-137">Fine del supporto server</span><span class="sxs-lookup"><span data-stu-id="3bb2f-137">End of server support</span></span><br/>    | <span data-ttu-id="3bb2f-138">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="3bb2f-138">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="3bb2f-139">Intestazione</span><span class="sxs-lookup"><span data-stu-id="3bb2f-139">Header</span></span><br/>                   | <dl> <span data-ttu-id="3bb2f-140"><dt>Scardmgr. h</dt></span><span class="sxs-lookup"><span data-stu-id="3bb2f-140"><dt>Scardmgr.h</dt></span></span> </dl>   |
| <span data-ttu-id="3bb2f-141">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="3bb2f-141">Type library</span></span><br/>             | <dl> <span data-ttu-id="3bb2f-142"><dt>Scardmgr. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="3bb2f-142"><dt>Scardmgr.tlb</dt></span></span> </dl> |
| <span data-ttu-id="3bb2f-143">DLL</span><span class="sxs-lookup"><span data-stu-id="3bb2f-143">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3bb2f-144"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3bb2f-144"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="3bb2f-145">IID</span><span class="sxs-lookup"><span data-stu-id="3bb2f-145">IID</span></span><br/>                      | <span data-ttu-id="3bb2f-146">La \_ scheda IID è definita come 1461AAC3-6810-11D0-918F-00AA00C18068</span><span class="sxs-lookup"><span data-stu-id="3bb2f-146">IID\_ISCard is defined as 1461AAC3-6810-11D0-918F-00AA00C18068</span></span><br/>               |



## <a name="see-also"></a><span data-ttu-id="3bb2f-147">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="3bb2f-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3bb2f-148">**ottenere \_ CardHandle**</span><span class="sxs-lookup"><span data-stu-id="3bb2f-148">**get\_CardHandle**</span></span>](iscard-get-cardhandle.md)
</dt> <dt>

[<span data-ttu-id="3bb2f-149">**ottenere il \_ contesto**</span><span class="sxs-lookup"><span data-stu-id="3bb2f-149">**get\_Context**</span></span>](iscard-get-context.md)
</dt> <dt>

[<span data-ttu-id="3bb2f-150">**ottenere il \_ protocollo**</span><span class="sxs-lookup"><span data-stu-id="3bb2f-150">**get\_Protocol**</span></span>](iscard-get-protocol.md)
</dt> <dt>

[<span data-ttu-id="3bb2f-151">**ottenere \_ lo stato**</span><span class="sxs-lookup"><span data-stu-id="3bb2f-151">**get\_Status**</span></span>](iscard-get-status.md)
</dt> <dt>

[<span data-ttu-id="3bb2f-152">**Scheda di**</span><span class="sxs-lookup"><span data-stu-id="3bb2f-152">**ISCard**</span></span>](iscard.md)
</dt> <dt>

[<span data-ttu-id="3bb2f-153">**IByteBuffer:: Read**</span><span class="sxs-lookup"><span data-stu-id="3bb2f-153">**IByteBuffer::Read**</span></span>](ibytebuffer-read.md)
</dt> </dl>

 

 
