---
description: Il metodo ListCards recupera tutti i nomi delle smart card che corrispondono agli identificatori di interfaccia specificati (GUID), alla stringa ATR specificata o a entrambi.
ms.assetid: a1cf8186-0746-4c4d-917d-40d6c3542036
title: 'Metodo ISCardDatabase:: ListCards (Scardmgr. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardDatabase.ListCards
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: e8a5bf56aa27a044d29e2e0153698bfefe69e1d1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103751682"
---
# <a name="iscarddatabaselistcards-method"></a><span data-ttu-id="31a8a-103">Metodo ISCardDatabase:: ListCards</span><span class="sxs-lookup"><span data-stu-id="31a8a-103">ISCardDatabase::ListCards method</span></span>

<span data-ttu-id="31a8a-104">\[Il metodo **ListCards** è disponibile per l'uso nei sistemi operativi specificati nella sezione requisiti.</span><span class="sxs-lookup"><span data-stu-id="31a8a-104">\[The **ListCards** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="31a8a-105">Non è disponibile per l'utilizzo in Windows Server 2003 con Service Pack 1 (SP1) e versioni successive, Windows Vista, Windows Server 2008 e versioni successive del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="31a8a-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="31a8a-106">I [moduli Smart Card](/previous-versions/windows/desktop/secsmart/smart-card-modules) offrono funzionalità simili.\]</span><span class="sxs-lookup"><span data-stu-id="31a8a-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="31a8a-107">Il metodo **ListCards** recupera tutti i nomi delle smart card che corrispondono agli identificatori di interfaccia specificati (Guid), alla [*stringa ATR*](../secgloss/a-gly.md)specificata o a entrambi.</span><span class="sxs-lookup"><span data-stu-id="31a8a-107">The **ListCards** method retrieves all of the smart card names that match the specified interface identifiers (GUIDs), the specified [*ATR string*](../secgloss/a-gly.md), or both.</span></span>

## <a name="syntax"></a><span data-ttu-id="31a8a-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="31a8a-108">Syntax</span></span>


```C++
HRESULT ListCards(
  [in]  LPBYTEBUFFER pAtr,
  [in]  LPSAFEARRAY  pInterfaceGuids,
  [in]  LONG         localeId,
  [out] LPSAFEARRAY  *ppCardNames
);
```



## <a name="parameters"></a><span data-ttu-id="31a8a-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="31a8a-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="31a8a-110">*pAtr* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="31a8a-110">*pAtr* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="31a8a-111">Puntatore a una stringa ATR della [*Smart Card*](../secgloss/s-gly.md) .</span><span class="sxs-lookup"><span data-stu-id="31a8a-111">Pointer to a [*smart card*](../secgloss/s-gly.md) ATR string.</span></span> <span data-ttu-id="31a8a-112">La stringa ATR deve essere assemblata in un [**IByteBuffer**](ibytebuffer.md).</span><span class="sxs-lookup"><span data-stu-id="31a8a-112">The ATR string must be packaged into an [**IByteBuffer**](ibytebuffer.md).</span></span>

</dd> <dt>

<span data-ttu-id="31a8a-113">*pInterfaceGuids* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="31a8a-113">*pInterfaceGuids* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="31a8a-114">Puntatore a un SAFEARRAY di identificatori di interfaccia COM (GUID) in formato BSTR.</span><span class="sxs-lookup"><span data-stu-id="31a8a-114">Pointer to a SAFEARRAY of COM interface identifiers (GUIDs) in BSTR format.</span></span>

</dd> <dt>

<span data-ttu-id="31a8a-115">*LocaleID* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="31a8a-115">*localeId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="31a8a-116">Identificatore di localizzazione della lingua.</span><span class="sxs-lookup"><span data-stu-id="31a8a-116">Language localization identifier.</span></span>

</dd> <dt>

<span data-ttu-id="31a8a-117">*ppCardNames* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="31a8a-117">*ppCardNames* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="31a8a-118">Puntatore a un SAFEARRAY di BSTR che contiene i nomi delle smart card che soddisfano i parametri di ricerca in caso di esito positivo; **Null** se l'operazione non è riuscita.</span><span class="sxs-lookup"><span data-stu-id="31a8a-118">Pointer to a SAFEARRAY of BSTRs that contains the names of the smart cards that satisfied the search parameters if successful; **NULL** if the operation failed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="31a8a-119">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="31a8a-119">Return value</span></span>

<span data-ttu-id="31a8a-120">Il metodo restituisce uno dei valori possibili seguenti.</span><span class="sxs-lookup"><span data-stu-id="31a8a-120">The method returns one of the following possible values.</span></span>



| <span data-ttu-id="31a8a-121">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="31a8a-121">Return code</span></span>                                                                                   | <span data-ttu-id="31a8a-122">Descrizione</span><span class="sxs-lookup"><span data-stu-id="31a8a-122">Description</span></span>                                  |
|-----------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="31a8a-123"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="31a8a-123"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="31a8a-124">Operazione completata correttamente.</span><span class="sxs-lookup"><span data-stu-id="31a8a-124">Operation completed successfully.</span></span><br/> |
| <dl> <span data-ttu-id="31a8a-125"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="31a8a-125"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="31a8a-126">Parametro non valido.</span><span class="sxs-lookup"><span data-stu-id="31a8a-126">Invalid parameter.</span></span><br/>                |
| <dl> <span data-ttu-id="31a8a-127"><dt>**\_puntatore E**</dt></span><span class="sxs-lookup"><span data-stu-id="31a8a-127"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="31a8a-128">È stato passato un puntatore non valido.</span><span class="sxs-lookup"><span data-stu-id="31a8a-128">A bad pointer was passed in.</span></span><br/>      |
| <dl> <span data-ttu-id="31a8a-129"><dt>**E \_ OutOfMemory**</dt></span><span class="sxs-lookup"><span data-stu-id="31a8a-129"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="31a8a-130">Memoria insufficiente.</span><span class="sxs-lookup"><span data-stu-id="31a8a-130">Out of memory.</span></span><br/>                    |



 

## <a name="remarks"></a><span data-ttu-id="31a8a-131">Commenti</span><span class="sxs-lookup"><span data-stu-id="31a8a-131">Remarks</span></span>

<span data-ttu-id="31a8a-132">Per recuperare tutti i [*Reader*](../secgloss/r-gly.md) o [*Reader*](../secgloss/r-gly.md)noti, chiamare rispettivamente [**ListReaders**](iscarddatabase-listreaders.md) o [**ListReaderGroups**](iscarddatabase-listreadergroups.md) .</span><span class="sxs-lookup"><span data-stu-id="31a8a-132">To retrieve all known [*readers*](../secgloss/r-gly.md) or [*reader*](../secgloss/r-gly.md), call [**ListReaders**](iscarddatabase-listreaders.md) or [**ListReaderGroups**](iscarddatabase-listreadergroups.md) respectively.</span></span>

<span data-ttu-id="31a8a-133">Per recuperare rispettivamente il [*servizio primario*](../secgloss/p-gly.md) o le interfacce di una scheda specifica [**GetProviderCardId**](iscarddatabase-getprovidercardid.md) o [**ListCardInterfaces**](iscarddatabase-listcardinterfaces.md) .</span><span class="sxs-lookup"><span data-stu-id="31a8a-133">To retrieve the [*primary service*](../secgloss/p-gly.md) or the interfaces of a specific card [**GetProviderCardId**](iscarddatabase-getprovidercardid.md) or [**ListCardInterfaces**](iscarddatabase-listcardinterfaces.md) respectively.</span></span>

<span data-ttu-id="31a8a-134">Per un elenco di tutti i metodi forniti da questa interfaccia, vedere [**ISCardDatabase**](iscarddatabase.md).</span><span class="sxs-lookup"><span data-stu-id="31a8a-134">For a list of all the methods provided by this interface, see [**ISCardDatabase**](iscarddatabase.md).</span></span>

<span data-ttu-id="31a8a-135">Oltre ai codici di errore COM elencati sopra, questa interfaccia può restituire un codice di errore della smart card se è stata chiamata una funzione Smart Card per completare la richiesta.</span><span class="sxs-lookup"><span data-stu-id="31a8a-135">In addition to the COM error codes listed above, this interface may return a smart card error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="31a8a-136">Per ulteriori informazioni, vedere [valori restituiti della smart card](authentication-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="31a8a-136">For more information, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="examples"></a><span data-ttu-id="31a8a-137">Esempio</span><span class="sxs-lookup"><span data-stu-id="31a8a-137">Examples</span></span>

<span data-ttu-id="31a8a-138">Nell'esempio seguente viene illustrato come recuperare i nomi delle smart card che corrispondono alla stringa ATR specificata.</span><span class="sxs-lookup"><span data-stu-id="31a8a-138">The following example shows retrieving the smart card names that match the specified ATR string.</span></span>


```C++
// Define or determine byAtr as needed for your ATR use.
BYTE byAtr[] = {0x3b,0x27,0x00,0x80,0x65,0xa2,0x0c,0x01,0x01,0x37};
LPSAFEARRAY pSafeArray = NULL;
HRESULT          hr;

// pIByteBuff is a pointer to an instance of IByteBuffer.
hr = pIByteBuff->Initialize(sizeof(byAtr), byAtr);

// Call the function for the specified ATR.
hr = pISCDataBase->ListCards(pIByteBuff,
                             NULL,
                             0,
                             &pSafeArray);
if (FAILED(hr))
{
   printf("Failed ListCards\n");
   // Take other error handling action as needed.
}
else
{
   // Use the safe array as needed.
}
```



## <a name="requirements"></a><span data-ttu-id="31a8a-139">Requisiti</span><span class="sxs-lookup"><span data-stu-id="31a8a-139">Requirements</span></span>



| <span data-ttu-id="31a8a-140">Requisito</span><span class="sxs-lookup"><span data-stu-id="31a8a-140">Requirement</span></span> | <span data-ttu-id="31a8a-141">Valore</span><span class="sxs-lookup"><span data-stu-id="31a8a-141">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="31a8a-142">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="31a8a-142">Minimum supported client</span></span><br/> | <span data-ttu-id="31a8a-143">\[Solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="31a8a-143">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="31a8a-144">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="31a8a-144">Minimum supported server</span></span><br/> | <span data-ttu-id="31a8a-145">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="31a8a-145">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="31a8a-146">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="31a8a-146">End of client support</span></span><br/>    | <span data-ttu-id="31a8a-147">Windows XP</span><span class="sxs-lookup"><span data-stu-id="31a8a-147">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="31a8a-148">Fine del supporto server</span><span class="sxs-lookup"><span data-stu-id="31a8a-148">End of server support</span></span><br/>    | <span data-ttu-id="31a8a-149">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="31a8a-149">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="31a8a-150">Intestazione</span><span class="sxs-lookup"><span data-stu-id="31a8a-150">Header</span></span><br/>                   | <dl> <span data-ttu-id="31a8a-151"><dt>Scardmgr. h</dt></span><span class="sxs-lookup"><span data-stu-id="31a8a-151"><dt>Scardmgr.h</dt></span></span> </dl>   |
| <span data-ttu-id="31a8a-152">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="31a8a-152">Type library</span></span><br/>             | <dl> <span data-ttu-id="31a8a-153"><dt>Scardmgr. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="31a8a-153"><dt>Scardmgr.tlb</dt></span></span> </dl> |
| <span data-ttu-id="31a8a-154">DLL</span><span class="sxs-lookup"><span data-stu-id="31a8a-154">DLL</span></span><br/>                      | <dl> <span data-ttu-id="31a8a-155"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="31a8a-155"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="31a8a-156">IID</span><span class="sxs-lookup"><span data-stu-id="31a8a-156">IID</span></span><br/>                      | <span data-ttu-id="31a8a-157">IID \_ ISCardDatabase è definito come 1461AAC8-6810-11D0-918F-00AA00C18068</span><span class="sxs-lookup"><span data-stu-id="31a8a-157">IID\_ISCardDatabase is defined as 1461AAC8-6810-11D0-918F-00AA00C18068</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="31a8a-158">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="31a8a-158">See also</span></span>

<dl> <dt>

[<span data-ttu-id="31a8a-159">**GetProviderCardId**</span><span class="sxs-lookup"><span data-stu-id="31a8a-159">**GetProviderCardId**</span></span>](iscarddatabase-getprovidercardid.md)
</dt> <dt>

[<span data-ttu-id="31a8a-160">**ISCardDatabase**</span><span class="sxs-lookup"><span data-stu-id="31a8a-160">**ISCardDatabase**</span></span>](iscarddatabase.md)
</dt> <dt>

[<span data-ttu-id="31a8a-161">**ListCardInterfaces**</span><span class="sxs-lookup"><span data-stu-id="31a8a-161">**ListCardInterfaces**</span></span>](iscarddatabase-listcardinterfaces.md)
</dt> <dt>

[<span data-ttu-id="31a8a-162">**ListReaderGroups**</span><span class="sxs-lookup"><span data-stu-id="31a8a-162">**ListReaderGroups**</span></span>](iscarddatabase-listreadergroups.md)
</dt> <dt>

[<span data-ttu-id="31a8a-163">**ListReaders**</span><span class="sxs-lookup"><span data-stu-id="31a8a-163">**ListReaders**</span></span>](iscarddatabase-listreaders.md)
</dt> </dl>

 

 
