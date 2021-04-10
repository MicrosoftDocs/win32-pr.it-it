---
description: Il metodo ListCardInterfaces recupera gli identificatori (GUID) di tutte le interfacce supportate per la smart card specificata.
ms.assetid: c9dfd17e-f4a9-47d3-974e-66e78bc4b06a
title: 'Metodo ISCardDatabase:: ListCardInterfaces (Scardmgr. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardDatabase.ListCardInterfaces
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: d52324edd4a502388ac6064de07a6ab58a68074d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104225900"
---
# <a name="iscarddatabaselistcardinterfaces-method"></a><span data-ttu-id="08868-103">Metodo ISCardDatabase:: ListCardInterfaces</span><span class="sxs-lookup"><span data-stu-id="08868-103">ISCardDatabase::ListCardInterfaces method</span></span>

<span data-ttu-id="08868-104">\[Il metodo **ListCardInterfaces** è disponibile per l'uso nei sistemi operativi specificati nella sezione requisiti.</span><span class="sxs-lookup"><span data-stu-id="08868-104">\[The **ListCardInterfaces** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="08868-105">Non è disponibile per l'utilizzo in Windows Server 2003 con Service Pack 1 (SP1) e versioni successive, Windows Vista, Windows Server 2008 e versioni successive del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="08868-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="08868-106">I [moduli Smart Card](/previous-versions/windows/desktop/secsmart/smart-card-modules) offrono funzionalità simili.\]</span><span class="sxs-lookup"><span data-stu-id="08868-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="08868-107">Il metodo **ListCardInterfaces** recupera gli identificatori (Guid) di tutte le interfacce supportate per la [*Smart Card*](../secgloss/s-gly.md)specificata.</span><span class="sxs-lookup"><span data-stu-id="08868-107">The **ListCardInterfaces** method retrieves the identifiers (GUIDs) of all the interfaces supported for the specified [*smart card*](../secgloss/s-gly.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="08868-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="08868-108">Syntax</span></span>


```C++
HRESULT ListCardInterfaces(
  [in]  BSTR        bstrCardName,
  [out] LPSAFEARRAY *ppInterfaceGuids
);
```



## <a name="parameters"></a><span data-ttu-id="08868-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="08868-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="08868-110">*bstrCardName* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="08868-110">*bstrCardName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="08868-111">Nome della smart card.</span><span class="sxs-lookup"><span data-stu-id="08868-111">Name of the smart card.</span></span>

</dd> <dt>

<span data-ttu-id="08868-112">*ppInterfaceGuids* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="08868-112">*ppInterfaceGuids* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="08868-113">Puntatore ai GUID dell'interfaccia in caso di esito positivo; **Null** se l'operazione non è riuscita.</span><span class="sxs-lookup"><span data-stu-id="08868-113">Pointer to the interface GUIDs if successful; **NULL** if operation failed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="08868-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="08868-114">Return value</span></span>

<span data-ttu-id="08868-115">Il metodo restituisce uno dei valori possibili seguenti.</span><span class="sxs-lookup"><span data-stu-id="08868-115">The method returns one of the following possible values.</span></span>



| <span data-ttu-id="08868-116">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="08868-116">Return code</span></span>                                                                                   | <span data-ttu-id="08868-117">Descrizione</span><span class="sxs-lookup"><span data-stu-id="08868-117">Description</span></span>                                                |
|-----------------------------------------------------------------------------------------------|------------------------------------------------------------|
| <dl> <span data-ttu-id="08868-118"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="08868-118"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="08868-119">Operazione completata correttamente.</span><span class="sxs-lookup"><span data-stu-id="08868-119">Operation completed successfully.</span></span><br/>               |
| <dl> <span data-ttu-id="08868-120"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="08868-120"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="08868-121">Parametro non valido.</span><span class="sxs-lookup"><span data-stu-id="08868-121">Invalid parameter.</span></span><br/>                              |
| <dl> <span data-ttu-id="08868-122"><dt>**\_puntatore E**</dt></span><span class="sxs-lookup"><span data-stu-id="08868-122"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="08868-123">Un puntatore errato è stato passato in *ppInterfaceGuids*.</span><span class="sxs-lookup"><span data-stu-id="08868-123">A bad pointer was passed in *ppInterfaceGuids*.</span></span><br/> |
| <dl> <span data-ttu-id="08868-124"><dt>**E \_ OutOfMemory**</dt></span><span class="sxs-lookup"><span data-stu-id="08868-124"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="08868-125">Memoria insufficiente.</span><span class="sxs-lookup"><span data-stu-id="08868-125">Out of memory.</span></span><br/>                                  |



 

## <a name="remarks"></a><span data-ttu-id="08868-126">Commenti</span><span class="sxs-lookup"><span data-stu-id="08868-126">Remarks</span></span>

<span data-ttu-id="08868-127">Per recuperare il [*provider di servizi primario*](../secgloss/p-gly.md) della smart card, chiamare [**GetProviderCardId**](iscarddatabase-getprovidercardid.md).</span><span class="sxs-lookup"><span data-stu-id="08868-127">To retrieve the [*primary service provider*](../secgloss/p-gly.md) of the smart card, call [**GetProviderCardId**](iscarddatabase-getprovidercardid.md).</span></span>

<span data-ttu-id="08868-128">Per recuperare tutte le [*Smart Card*](../secgloss/s-gly.md), i [*Reader*](../secgloss/r-gly.md)e i [*gruppi di Reader*](../secgloss/r-gly.md) noti, chiamare rispettivamente [**ListCards**](iscarddatabase-listcards.md), [**ListReaders**](iscarddatabase-listreaders.md)e [**ListReaderGroups**](iscarddatabase-listreadergroups.md) .</span><span class="sxs-lookup"><span data-stu-id="08868-128">To retrieve all known [*smart cards*](../secgloss/s-gly.md), [*readers*](../secgloss/r-gly.md), and [*reader groups*](../secgloss/r-gly.md) call [**ListCards**](iscarddatabase-listcards.md), [**ListReaders**](iscarddatabase-listreaders.md), and [**ListReaderGroups**](iscarddatabase-listreadergroups.md) respectively.</span></span>

<span data-ttu-id="08868-129">Per un elenco di tutti i metodi forniti da questa interfaccia, vedere [**ISCardDatabase**](iscarddatabase.md).</span><span class="sxs-lookup"><span data-stu-id="08868-129">For a list of all the methods provided by this interface, see [**ISCardDatabase**](iscarddatabase.md).</span></span>

<span data-ttu-id="08868-130">Oltre ai codici di errore COM elencati sopra, questa interfaccia può restituire un codice di errore della smart card se è stata chiamata una funzione Smart Card per completare la richiesta.</span><span class="sxs-lookup"><span data-stu-id="08868-130">In addition to the COM error codes listed above, this interface may return a smart card error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="08868-131">Per ulteriori informazioni, vedere [valori restituiti della smart card](authentication-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="08868-131">For more information, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="examples"></a><span data-ttu-id="08868-132">Esempio</span><span class="sxs-lookup"><span data-stu-id="08868-132">Examples</span></span>

<span data-ttu-id="08868-133">Nell'esempio seguente viene illustrato il recupero degli identificatori delle interfacce supportate per la smart card specificata.</span><span class="sxs-lookup"><span data-stu-id="08868-133">The following example shows retrieving the identifiers of the interfaces supported for the specified smart card.</span></span>


```C++
BSTR         bstrCard = NULL;
LPSAFEARRAY  pGuids = NULL;
HRESULT      hr;

bstrCard = SysAllocString(L"GemSAFE");
// Call the function for the specified card.
hr = pISCDataBase->ListCardInterfaces(bstrCard,
                                      &pGuids);
if (FAILED(hr))
{
   printf("Failed ListCardInterfaces\n");
   // Take other error handling action as needed.
}
else
{
   // Use the safe array as needed.
   // ...
   // Free BSTR when done.
   if (bstrCard)
       SysFreeString(bstrCard);
}
```



## <a name="requirements"></a><span data-ttu-id="08868-134">Requisiti</span><span class="sxs-lookup"><span data-stu-id="08868-134">Requirements</span></span>



| <span data-ttu-id="08868-135">Requisito</span><span class="sxs-lookup"><span data-stu-id="08868-135">Requirement</span></span> | <span data-ttu-id="08868-136">Valore</span><span class="sxs-lookup"><span data-stu-id="08868-136">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="08868-137">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="08868-137">Minimum supported client</span></span><br/> | <span data-ttu-id="08868-138">\[Solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="08868-138">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="08868-139">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="08868-139">Minimum supported server</span></span><br/> | <span data-ttu-id="08868-140">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="08868-140">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="08868-141">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="08868-141">End of client support</span></span><br/>    | <span data-ttu-id="08868-142">Windows XP</span><span class="sxs-lookup"><span data-stu-id="08868-142">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="08868-143">Fine del supporto server</span><span class="sxs-lookup"><span data-stu-id="08868-143">End of server support</span></span><br/>    | <span data-ttu-id="08868-144">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="08868-144">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="08868-145">Intestazione</span><span class="sxs-lookup"><span data-stu-id="08868-145">Header</span></span><br/>                   | <dl> <span data-ttu-id="08868-146"><dt>Scardmgr. h</dt></span><span class="sxs-lookup"><span data-stu-id="08868-146"><dt>Scardmgr.h</dt></span></span> </dl>   |
| <span data-ttu-id="08868-147">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="08868-147">Type library</span></span><br/>             | <dl> <span data-ttu-id="08868-148"><dt>Scardmgr. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="08868-148"><dt>Scardmgr.tlb</dt></span></span> </dl> |
| <span data-ttu-id="08868-149">DLL</span><span class="sxs-lookup"><span data-stu-id="08868-149">DLL</span></span><br/>                      | <dl> <span data-ttu-id="08868-150"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="08868-150"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="08868-151">IID</span><span class="sxs-lookup"><span data-stu-id="08868-151">IID</span></span><br/>                      | <span data-ttu-id="08868-152">IID \_ ISCardDatabase è definito come 1461AAC8-6810-11D0-918F-00AA00C18068</span><span class="sxs-lookup"><span data-stu-id="08868-152">IID\_ISCardDatabase is defined as 1461AAC8-6810-11D0-918F-00AA00C18068</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="08868-153">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="08868-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="08868-154">**GetProviderCardId**</span><span class="sxs-lookup"><span data-stu-id="08868-154">**GetProviderCardId**</span></span>](iscarddatabase-getprovidercardid.md)
</dt> <dt>

[<span data-ttu-id="08868-155">**ISCardDatabase**</span><span class="sxs-lookup"><span data-stu-id="08868-155">**ISCardDatabase**</span></span>](iscarddatabase.md)
</dt> <dt>

[<span data-ttu-id="08868-156">**ListCards**</span><span class="sxs-lookup"><span data-stu-id="08868-156">**ListCards**</span></span>](iscarddatabase-listcards.md)
</dt> <dt>

[<span data-ttu-id="08868-157">**ListReaderGroups**</span><span class="sxs-lookup"><span data-stu-id="08868-157">**ListReaderGroups**</span></span>](iscarddatabase-listreadergroups.md)
</dt> <dt>

[<span data-ttu-id="08868-158">**ListReaders**</span><span class="sxs-lookup"><span data-stu-id="08868-158">**ListReaders**</span></span>](iscarddatabase-listreaders.md)
</dt> </dl>

 

 
